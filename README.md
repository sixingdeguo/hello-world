import torch
from torch.nn.utils.rnn import pad_sequence

# 创建一些不等长的张量
seq1 = torch.tensor([1, 2, 3])
seq2 = torch.tensor([4, 5])
seq3 = torch.tensor([6])

# 后面填充 (默认行为)
padded_seq = pad_sequence([seq1, seq2, seq3], batch_first=True)
print(padded_seq)




# 反转序列
reversed_seq = [seq.flip(0) for seq in [seq1, seq2, seq3]]

# 后面填充
padded_reversed_seq = pad_sequence(reversed_seq, batch_first=True)

# 再次反转回来
padded_seq = padded_reversed_seq.flip(1)

print(padded_seq)


import torch.nn.functional as F

# 找到最长的序列长度
max_len = max(len(seq1), len(seq2), len(seq3))

# 前面填充
padded_seq1 = F.pad(seq1, (max_len - len(seq1), 0))  # 前面填充
padded_seq2 = F.pad(seq2, (max_len - len(seq2), 0))  # 前面填充
padded_seq3 = F.pad(seq3, (max_len - len(seq3), 0))  # 前面填充

# 合并到一起
padded_seqs = torch.stack([padded_seq1, padded_seq2, padded_seq3])
print(padded_seqs)
