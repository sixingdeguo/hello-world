import json
import csv

# 读取 JSON 文件
with open('res.json', 'r') as json_file:
    data = json.load(json_file)

# 打开一个 CSV 文件用于写入
with open('output.csv', 'w', newline='') as csv_file:
    writer = csv.writer(csv_file)

    # 写入 CSV 表头
    header = ['index_id', 'a', 'b']
    writer.writerow(header)

    # 遍历 JSON 中的每条记录并写入 CSV
    for entry in data:
        index_id = entry['index_id']
        a_values = entry['a']
        b_values = entry['b']

        # 写入行数据
        writer.writerow([index_id, a_values, b_values])

print("Conversion complete!")
