for param_id, state in optimizer.state.items():
    print(f"Parameter ID: {param_id}")
    for key, value in state.items():
        if isinstance(value, torch.Tensor):  # 如果状态是张量，打印设备信息
            print(f"  {key}: {value} (Device: {value.device})")
        else:
            print(f"  {key}: {value}")


for i, param_group in enumerate(optimizer.param_groups):
    print(f"Param Group {i}:")
    for key, value in param_group.items():
        if key != 'params':  # 排除参数本身，避免打印大张量的数据
            print(f"  {key}: {value}")
    print("  Parameters in this group:")
    for param in param_group['params']:
        print(f"    Shape: {param.shape}, Device: {param.device}")
