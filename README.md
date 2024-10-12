import os
import asyncio
from openai import AsyncAzureOpenAI

async def main():
    client = AsyncAzureOpenAI(  
      api_key = os.getenv("AZURE_OPENAI_API_KEY"),  
      api_version = "2024-02-01",
      azure_endpoint = os.getenv("AZURE_OPENAI_ENDPOINT")
    )
    response = await client.chat.completions.create(model="gpt-35-turbo", messages=[{"role": "user", "content": "Hello world"}]) # model = model deployment name

    print(response.model_dump_json(indent=2))

asyncio.run(main())
