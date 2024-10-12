import time

import openai
import json
import io
# from loguru import logger
# import random
# import re
# from mysql_utils import insert_one, _init_table, insert_many, select_distinct, update_one
# import tqdm
import random

openai.api_type = "azure"
openai.api_version = "2023-05-15"
list_keys = [
    ["https://geely-12-chatgpt-005.openai.azure.com/", "c1a7e754ea9541599f8cd36971d650c1"],
    ["https://geely-12-chatgpt-006.openai.azure.com/", "b612e2835bdf4d438bc1328514895ee6"],
    ["https://geely-13-chatgpt-005.openai.azure.com/", "1643e9002cd44a4a9bcc41b9241777df"],
    ["https://geely-13-chatgpt-006.openai.azure.com/", "9c8fd0f5e5234760a525237ebd25d54c"],
    ["https://geely-14-chatgpt-005.openai.azure.com/", "3491ef1f39be4f6e8fa61e732da4016d"],
    ["https://geely-14-chatgpt-006.openai.azure.com/", "b909d8b8afb545f7a281bb21ec2252c9"]]


def _generate(message):
    key = random.sample(list_keys, 1)[0]
    openai.api_base = key[0]
    openai.api_key = key[1]
    try:
        response = openai.ChatCompletion.create(
            engine="gpt4",
            messages=message,
            # request_timeout=300,
            # max_retries=1,
            temperature=0.7,
            n=1
        )
        text = response.get("choices")[0]["message"]["content"]
    except Exception as e:
        print(e)
        print(time.sleep(1))
        key = random.sample(list_keys, 1)[0]
        openai.api_base = key[0]
        openai.api_key = key[1]
        response = openai.ChatCompletion.create(
            engine="gpt4",
            messages=message,
            # request_timeout=300,
            # max_retries=1,
            temperature=0.7,
            n=1
        )
        try:
            text = response.get("choices")[0]["message"]["content"]
        except:
            text = ""
    return text


if __name__ == '__main__':
    messages =[]
    messages.append({"role": "system", "content": '要求生活中的两个人类好友Human与Assistant进行多轮对话，并以#对话要求#的风格要求进行。对话是根据##提供信息##的内容开展的，并以#对话规划#的格式进行输出，以<start_chat>开始，以<end_chat>结束。'})
    messages.append({"role": "user", "content": '你好'})
    messages.append({"role": "assistant", "content": '你好，有什么可以帮助你的吗？'})
    messages.append({"role": "user", "content": '今天天气'})
    # messages.append(
    #     {
    #         "role": "user",
    #         "content": '''今天天气怎么样？'''
    #     }
    # )
    a = time.time()
    print(_generate(messages))
    print(time.time()-a)
