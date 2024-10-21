import torch

# 假设你有4个 answer 的概率，每个是不同长度的序列
log_probs = [
    torch.tensor([0.1, 0.2, 0.3]),         # 长度为3
    torch.tensor([0.4, 0.5]),              # 长度为2
    torch.tensor([0.6, 0.7, 0.8, 0.9]),    # 长度为4
    torch.tensor([0.3, 0.1])               # 长度为2
]

# 假设 prompt 段的长度是统一的5, 每个prompt用一个固定的张量表示
prompt_log_probs = torch.tensor([0.0, 0.0, 0.1, 0.2, 0.3])  # 长度为5

# 1. 首先找到最长的 answer 序列长度
max_answer_len = max([len(p) for p in log_probs])

# 2. 填充每个 answer 的 log_probs 序列，使其长度统一
# 使用 pad_sequence 函数，指定填充位置
padded_answers = torch.nn.utils.rnn.pad_sequence(log_probs, batch_first=True, padding_value=0.0)

# 3. 拼接 prompt 和 answer 的 log_probs
# 假设每个样本的 prompt 段相同，可以直接扩展为 batch 的形式
batch_size = len(log_probs)
prompts = prompt_log_probs.unsqueeze(0).expand(batch_size, -1)  # 扩展到 batch 的维度

# 4. 最后，拼接 prompt 和 padded answer log_probs
full_batch_log_probs = torch.cat([prompts, padded_answers], dim=1)

# 查看结果
print(full_batch_log_probs)
