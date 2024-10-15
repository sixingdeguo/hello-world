import json

def extract_first_sentences(file_path):
    # 打开并读取JSON文件
    with open(file_path, 'r', encoding='utf-8') as file:
        for line in file:
            # 加载每一行的 JSON 数据
            debate_data = json.loads(line)
            # 检查 messages 键是否存在
            if 'messages' in debate_data:
                first_message = debate_data['messages'][1]  # 通常第一句对话是第二条信息，跳过 system 信息
                first_sentence = first_message['content'].split('.')[0] + '.'
                print(f"角色: {first_message['role']}，第一句对话: {first_sentence}")

# 调用函数，传入你的 JSON 文件路径
extract_first_sentences('path_to_your_file.json')
