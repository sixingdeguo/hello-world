# 查看模型梯度所在的设备
print("Model Gradient Devices:")
for name, param in model.named_parameters():
    if param.grad is not None:
        print(f"Parameter: {name}, Gradient Device: {param.grad.device}")
    else:
        print(f"Parameter: {name} has no gradient.")

# 查看优化器 state 所在的设备
print("\nOptimizer State Devices:")
for param_id, state in optimizer.state.items():
    print(f"Parameter ID: {param_id}")
    for key, value in state.items():
        if isinstance(value, torch.Tensor):
            print(f"  State {key} Device: {value.device}")
        else:
            print(f"  State {key} is not a tensor.")
