[2024-08-15 08:00:33,840] [INFO] [launch.py:139:main] 0 NV_LIBNCCL_PACKAGE_VERSION=2.15.5-1
[2024-08-15 08:00:33,840] [INFO] [launch.py:139:main] 0 NV_LIBNCCL_DEV_PACKAGE_VERSION=2.15.5-1
[2024-08-15 08:00:33,840] [INFO] [launch.py:139:main] 0 NV_LIBNCCL_PACKAGE_NAME=libnccl2
[2024-08-15 08:00:33,840] [INFO] [launch.py:139:main] 0 NV_LIBNCCL_DEV_PACKAGE_NAME=libnccl-dev
[2024-08-15 08:00:33,840] [INFO] [launch.py:139:main] 0 NV_LIBNCCL_PACKAGE=libnccl2=2.15.5-1+cuda11.8
[2024-08-15 08:00:33,840] [INFO] [launch.py:139:main] 0 NV_LIBNCCL_DEV_PACKAGE=libnccl-dev=2.15.5-1+cuda11.8
[2024-08-15 08:00:33,840] [INFO] [launch.py:139:main] 0 NCCL_VERSION=2.15.5-1
[2024-08-15 08:00:33,841] [INFO] [launch.py:146:main] WORLD INFO DICT: {'localhost': [0]}
[2024-08-15 08:00:33,841] [INFO] [launch.py:152:main] nnodes=1, num_local_procs=1, node_rank=0
[2024-08-15 08:00:33,841] [INFO] [launch.py:163:main] global_rank_mapping=defaultdict(<class 'list'>, {'localhost': [0]})
[2024-08-15 08:00:33,841] [INFO] [launch.py:164:main] dist_world_size=1
[2024-08-15 08:00:33,841] [INFO] [launch.py:168:main] Setting CUDA_VISIBLE_DEVICES=0
[2024-08-15 08:00:33,841] [INFO] [launch.py:256:main] process 5801 spawned with command: ['/opt/conda/bin/python', '-u', '-m', 'openrlhf.cli.train_rm', '--local_rank=0', '--save_path', '/vepfs/DI/user/zhaoyue/exp_result/openrlhf_0815_dev/Qwen2-1.5B-rm-yw', '--save_steps', '50', '--logging_steps', '1', '--nnodes', '1', '--eval_steps', '50', '--train_batch_size', '12', '--micro_train_batch_size', '12', '--pretrain', '/vepfs/DI/beijing-public/models/Qwen2-1.5B', '--bf16', '--max_epochs', '1', '--max_len', '2048', '--zero_stage', '1', '--learning_rate', '9e-6', '--dataset', '/vepfs/DI/user/zhaoyue/data_process/split_res.json', '--apply_chat_template', '--prompt_key', 'prompt', '--chosen_key', 'chosen', '--rejected_key', 'rejected', '--gradient_checkpointing', '--adam_offload', '--max_ckpt_num', '40', '--ckpt_path', '/vepfs/DI/user/zhaoyue/exp_result/openrlhf_0815_dev/Qwen2-1.5B-rm-yw/ckpt', '--use_tensorboard', '--tensorboard_logdir', '/vepfs/DI/user/zhaoyue/exp_result/openrlhf_0815_dev/Qwen2-1.5B-rm-yw', '--max_ckpt_mem', '5000']
[2024-08-15 08:00:37,742] [INFO] [real_accelerator.py:203:get_accelerator] Setting ds_accelerator to cuda (auto detect)
