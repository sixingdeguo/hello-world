import openai

# 配置 Azure OpenAI API 的基本信息
openai.api_type = "azure"
openai.api_base = "https://<your-resource-name>.openai.azure.com/"  # 你的 Azure 资源 URL
openai.api_version = "2023-10-01-preview"  # Azure OpenAI API 版本号
openai.api_key = "<your-api-key>"  # 你的 Azure API 密钥

def call_azure_openai(deployment_name, prompt):
    try:
        # 调用 Azure OpenAI API
        response = openai.Completion.create(
            engine=deployment_name,  # 你的部署名称
            prompt=prompt,
            max_tokens=100,
            temperature=0.7,
            n=1
        )
        return response['choices'][0]['text'].strip()
    except Exception as e:
        print(f"Error calling Azure OpenAI: {e}")
        return None

if __name__ == "__main__":
    deployment_name = "<your-deployment-name>"  # Azure 部署的模型名称
    prompt = "What are the benefits of using Azure OpenAI?"

    result = call_azure_openai(deployment_name, prompt)
    if result:
        print("Response from Azure OpenAI:")
        print(result)
