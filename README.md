import json
import asyncio

# 创建一个异步锁对象，用于防止并发写入冲突
write_lock = asyncio.Lock()

async def write_json_async(data, file_path):
    async with write_lock:  # 使用异步锁来防止写入冲突
        try:
            # 打开文件并异步写入 JSON 数据
            with open(file_path, "w") as file:
                json.dump(data, file, indent=4)
            print(f"写入 {file_path} 成功。")
        except Exception as e:
            print(f"写入 {file_path} 失败: {e}")

async def main():
    data1 = {"name": "Alice", "age": 30}
    data2 = {"name": "Bob", "age": 25}

    # 异步调用写入函数，防止写入冲突
    await asyncio.gather(
        write_json_async(data1, "data1.json"),
        write_json_async(data2, "data2.json")
    )

# 运行异步任务
asyncio.run(main())
