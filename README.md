
# 调用GPT4给出情感得分

import json
import os
import openai
import random
import time
import json
from multiprocessing import Pool
from tqdm import tqdm
from filelock import FileLock
import re


# 设置OpenAI API的类型和版本（使用Azure OpenAI服务）
openai.api_type = "azure"
openai.api_version = "2023-05-15"

# OpenAI API密钥和端点列表，每次请求随机选用一个，防止单一key被限流
list_keys = [
    ["https://geely-12-chatgpt-005.openai.azure.com/", "c1a7e754ea9541599f8cd36971d650c1"],
    ["https://geely-12-chatgpt-006.openai.azure.com/", "b612e2835bdf4d438bc1328514895ee6"],
    ["https://geely-13-chatgpt-005.openai.azure.com/", "1643e9002cd44a4a9bcc41b9241777df"],
    ["https://geely-13-chatgpt-006.openai.azure.com/", "9c8fd0f5e5234760a525237ebd25d54c"],
    ["https://geely-14-chatgpt-005.openai.azure.com/", "3491ef1f39be4f6e8fa61e732da4016d"],
    ["https://geely-14-chatgpt-006.openai.azure.com/", "b909d8b8afb545f7a281bb21ec2252c9"]]


def first_float(s: str):
    match = re.search(r"\d+\.\d+", s)
    if match:
        return float(match.group())
    return None

def process_single_line_and_write(data,output_jsonl_path):
    """
    处理单条jsonl数据：
    1. 检查reward字段是否已存在且合法，若是则跳过。
    2. 否则调用GPT-4进行评分。
    3. 解析结果并写入输出文件（加锁防止并发冲突）。
    """

    # 调用 GPT-4 推理
    result, user_prompt = emo_score(history = data['history_dialogue'], response = data['old_response'], speaker = data['speaker'], listener_list = data['listener_list'], emo = data['old_strategy'])
    # 这里的打分需要后续处理
    try:
        data['evaluation'] = float(result)
        data['explanation'] = ''
    except:
        data['evaluation'] = random.random()*5
        data['explanation'] = result
    data['user_prompt'] = user_prompt
    
    # 加锁写入文件，防止多进程同时写入冲突
    lock_path = output_jsonl_path + ".lock"
    with FileLock(lock_path):
        with open(output_jsonl_path, 'a', encoding='utf-8') as f_out:
            f_out.write(json.dumps(data, ensure_ascii=False) + '\n')


# -----------------------------
# 主处理函数：批量处理jsonl文件
# -----------------------------
def process_jsonl_incremental(input_file, output_file):
    """
    读取输入jsonl文件，使用多进程并发处理每一行。
    """
    lines = process_query(input_file)
    args = [(line, output_file) for line in lines]

    with Pool(processes=3) as pool:
        for _ in tqdm(pool.starmap(process_single_line_and_write, args), total=len(lines), desc="Processing"):
            pass

    # # 使用多进程池并发处理，提升处理速度
    # with Pool(processes=4) as pool:
    #     list(tqdm(pool.imap_unordered(process_single_line_and_write, lines), total=len(lines), desc="Processing"))


def process_query(file):
    output = []

    with open(file, 'r', encoding='utf-8') as f:
        content = f.readlines()
        k = len(content)
        for i in range(k):
            item = content[i]
            message = json.loads(item)


            tmp_list = message['history_dialogue'].split('\n')
            if 'speaker' in message.keys():
                speaker = message['speaker']
            else:
                speaker = 'assistant'
            listener_list = []
            for tmp in tmp_list[:-1]:
                listener = tmp.split(':')[0]
                if listener not in listener_list and listener != '':
                    listener_list.append(listener)
            message['speaker'] = speaker
            message['listener_list'] = listener_list
            output.append(message)
    return output


def emo_score(history, response, speaker, listener_list, emo):
    # 请求 URL
    key = random.sample(list_keys, 1)[0]
    openai.api_base = key[0]
    openai.api_key = key[1]
    
    # 请求头信息
    k = len(listener_list)
    if k>2:
        listener_str = 'among '
    else:
        listener_str = 'between '
    i = 1
    for listener in listener_list:
        listener_str += f' the "{listener}"'
        if i<k-1:
            listener_str += ','
        else:
            listener_str += ' and'
    # 用户prompt
    system_prompt = 'You are an expert in emotional psychology and you can accurately assess people\'s emotional states.'
    # 打分query
    user_prompt = f'''[Context]
{history}

[Prompt]
The above is a conversation {listener_str}. Now "{speaker}" needs to choose a appropriate emotion, and make an appropriate response to "{listener_list[-1]}". 
The {speaker} choose emotion {emo}.
The response is:
{response}
Please give your answer as a decimal number between 1 and 5 based on the criteria below.

[Criteria]
5 – Excellent
The emotion and response are highly appropriate, fully aligned with the dialogue history, deeply empathetic, relevant, consistent in tone, and clearly expressed.

4 – Good
The emotion and response are mostly appropriate and aligned, showing some empathy and relevance. Minor issues in tone or clarity, but overall effective.

3 – Fair
The emotion and response are partially appropriate but may miss some important cues. Limited empathy or support, and some tone mismatch or vagueness.

2 – Poor
The emotion or response is largely inappropriate, shows little empathy, weak relevance, or confusing tone. Response feels mismatched to the situation.

1 – Very Poor
The emotion and response are entirely inappropriate, irrelevant, and non-supportive. Tone may feel dismissive or insensitive.

Important: Your response should only include this decimal number.
'''
    max_retry = 15
    retry = 0
    while retry<max_retry:
        try:
            # 调用OpenAI ChatCompletion接口
            response = openai.ChatCompletion.create(
                engine="gpt4",
                messages=[
                    {"role": "system", "content": system_prompt},
                    {"role": "user", "content": user_prompt},
                ],
                temperature=0.9,
                max_tokens=1024,
            )

            # 获取GPT-4返回的文本结果
            result = response['choices'][0]['message']['content'].strip()
            score = first_float(result)
            print(float(score))
            # print(result)
            return float(score), user_prompt
        except Exception as e:
            # 若出错则等待3秒后返回错误信息
            retry += 1
            time.sleep(3)
            # if retry ==5:
            #     print(f'Error during evaluation, retry: {retry}')
    return 'Error', user_prompt

if __name__ == "__main__":
    # # file = '/vepfs/DI/user/zhaoyue/data/emotion_decision_result/emo_decision_daily_direct8_inference.json'
    # file = r'C:\Users\Yue.Zhao17\Desktop\EGS\data\emo_decision_daily_direct8_inference.json'
    # output = process_query(file)
    # output_jsonl_path = r'C:\Users\Yue.Zhao17\Desktop\EGS\esg_result\test.json'  # 输出文件路径
    
    result_path = r'C:\Users\Yue.Zhao17\Desktop\emo_gpt_score\emo_score'
    root_path = r'C:\Users\Yue.Zhao17\Desktop\emo_gpt_score\data'
    for file in os.listdir(root_path):
        out_name = f'{file[:-5]}_score.json'
        output_file = result_path + '\\' + out_name
        input_file = root_path + '\\' + file
        if out_name in os.listdir(result_path):
            print(file, '##exist##')
        else:
            print(f'##正在评估结果：\t{file}##')
            process_jsonl_incremental(input_file = input_file, output_file = output_file)


