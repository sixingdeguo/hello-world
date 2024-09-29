import requests

# 设置服务的地址和端口
url = "http://0.0.0.0:8505/v1/chat/completions"

# 定义请求的头信息（可选）
headers = {
    "Authorization": "Bearer EMPTY",  # 使用实际的 API 密钥替换 EMPTY
    "Content-Type": "application/json"
}

# 定义请求的 JSON 数据
data = {
    "model": "Qwen2-1.5B",  # 使用您服务中使用的模型名
    "messages": [
        {
            "role": "user",
            "content": "Hello, how can I use this service?"
        }
    ],
    "max_tokens": 150  # 生成的最大 token 数量
}

# 发送 POST 请求
response = requests.post(url, headers=headers, json=data)

# 检查响应状态码
if response.status_code == 200:
    # 打印响应内容
    print("Response:", response.json())
else:
    print("Error:", response.status_code, response.text)
