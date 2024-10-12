from openai import AzureOpenAI

# 创建 Azure OpenAI 客户端
client = AzureOpenAI(
    api_key="your-azure-api-key",  # 替换为你的 Azure API 密钥
    api_base="https://your-resource-name.openai.azure.com/",  # 替换为你的 Azure 资源名称
    api_version="2023-05-15"  # 设置 Azure OpenAI API 版本
)

# 发起一个 ChatCompletion 请求
async def get_chat_completion():
    response = await client.chat.completions.create(
        engine="your-deployment-name",  # 替换为你的实际部署名称
        messages=[
            {"role": "system", "content": "You are a helpful assistant."},
            {"role": "user", "content": "Tell me a joke."}
        ],
        temperature=0.7
    )
    return response['choices'][0]['message']['content']

# 异步执行获取聊天完成结果
import asyncio
result = asyncio.run(get_chat_completion())
print(result)
