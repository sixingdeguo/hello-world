#!/usr/bin/env python
# -*- coding: utf-8 -*-
import glob
import hashlib
import json
import logging
import math
import os
import shutil
import subprocess
import sys
import time
import warnings
from concurrent.futures import ThreadPoolExecutor

import torch

sys.path.append('./tool')
sys.path.append('./main')
from tool.parsers_func import parse_args_func
from tool.get_json import get_config, read_json_line
from main.get_gpt4 import gpt4_run

warnings.filterwarnings("ignore")

logger = logging.getLogger(__name__)
logger.setLevel(logging.INFO)
logging.basicConfig(level=logging.INFO, format='%(asctime)s - %(levelname)s - %(message)s')

args = parse_args_func()
logger.info(f"The Task Args params: {args}")
task_config, model_config = get_config()
logger.info(f'Task_config INFO: {task_config[args.task_name]}')
logger.info(f'Model_config INFO: {model_config[args.model_type]}')


def get_hash():
    args_dict = vars(args)
    args_str = ' '.join([str(value) for key, value in args_dict.items()])
    return hashlib.sha1(args_str.encode()).hexdigest()


def llm_infer(ids, begin_id, data_path, devices, args):
    visible_devices_str = ','.join([str(x) for x in range(ids * devices, (ids + 1) * devices)])

    cmd = f'CUDA_VISIBLE_DEVICES={visible_devices_str} python ./main/run.py --id {ids} --begin {begin_id} --data_slices_path {data_path} '
    for key in args.__dict__.keys():
        if key == 'use_history' or key == 'use_fast':
            if args.__dict__[key]:
                cmd += f'--{key} '
        else:
            cmd += f'--{key} {args.__dict__[key]} '
    subprocess.run(cmd, shell=True, text=True)


def data_split(data_path, worker):
    text_lists = read_json_line(data_path)
    single_len = math.ceil(len(text_lists) / int(worker))
    split_path = ['/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash() + f'/Data_Part_{ids}.json' for ids in
                  range(worker)]
    for ids, path in enumerate(split_path):
        with open(path, 'w', encoding='utf-8') as f:
            json.dump(text_lists[ids * single_len: (ids + 1) * single_len], f, ensure_ascii=False, indent=4)
    return split_path


def main():
    data_file = ''
    workers = args.num_proc_per_machine
    all_workers = workers * args.num_workers
    if os.path.exists('/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash()):
        shutil.rmtree('/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash())
    os.mkdir('/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash())
    if os.path.exists('/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash() + '_generated'):
        shutil.rmtree('/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash() + '_generated')
    os.mkdir('/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash() + '_generated')

    if args.data_path is None:
        if task_config[args.task_name]['data_path']:
            data_file = task_config[args.task_name]['data_path']
        else:
            logger.error('数据地址不存在，请检查数据地址')
    else:
        data_file = args.data_path

    logger.info(f'Data dir：{data_file}')
    split_paths = data_split(data_file, all_workers)

    device_count = torch.cuda.device_count()
    assert device_count >= workers, print('GPU数不能小于并行任务数！')
    per_worker_devices = device_count // workers

    logger.info(f'Device count: {device_count}')
    with ThreadPoolExecutor() as executor:
        status = executor.map(llm_infer, range(workers), [args.worker_idx * workers] * workers,
                              split_paths[args.worker_idx * workers: (args.worker_idx + 1) * workers],
                              [per_worker_devices] * workers, [args] * workers)


if __name__ == '__main__':
    start_time = time.time()
    if args.model_type == 'gpt4':
        gpt4_run(args)
    else:
        main()


        def write_data(data):
            with open(args.output_path,
                      'a',
                      encoding='utf-8') as write_object:
                write_object.write(data + '\n')


        merged_data = []
        for filename in glob.glob(
                os.path.join(f'/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash() + '_generated',
                             '*.json')):
            with open(filename, 'r') as file:
                try:
                    for line in file:
                        dt = json.loads(line)
                        json_str = json.dumps(dt, ensure_ascii=False)
                        write_data(json_str)
                except json.JSONDecodeError as e:
                    logger.error(f"Error decoding JSON in {filename}: {e}")
        logger.info(f"Merged all json files into {args.output_path}")

        shutil.rmtree('/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash())
        shutil.rmtree('/vepfs/DI/user/turghunrahman/data/inference_temp/' + get_hash() + '_generated')

    end_time = time.time()
    total_time = end_time - start_time
    m, s = divmod(total_time, 60)
    logger.info(f'任务总共花费: {int(m)}分钟{s}秒')
