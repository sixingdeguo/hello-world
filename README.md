for param_id, state in optimizer.state.items():
    print(f"Parameter ID: {param_id}")
    for key, value in state.items():
        print(f"  {key}: {value}")

for i, param_group in enumerate(optimizer.param_groups):
    print(f"Param Group {i}:")
    for key, value in param_group.items():
        if key != 'params':  # Avoid printing large tensor data
            print(f"  {key}: {value}")
    print("  Parameters in this group:")
    for param in param_group['params']:
        print(f"    {param.shape} - Device: {param.device}")
