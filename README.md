try:
    # 创建任务
    task: asyncio.Task = asyncio.create_task(self._func(*args, **kwargs))
    self._task_pool[key] = task

    # 等待任务完成
    result = await task

    # 更新响应
    self[key].response = APIResponse(
        finished=True, cancelled=False, error=None, result=result
    )
