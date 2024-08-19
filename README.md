python -m torch.distributed.launch --nproc_per_node <单个实例上的进程数> --master_addr $MLP_WORKER_0_HOST --node_rank $MLP_ROLE_INDEX --master_port $MLP_WORKER_0_PORT --nnodes $MLP_WORKER_NUM <代码文件的绝对路径>

torch.distributed.elastic.multiprocessing.errors.ChildFailedError: 
    from openrlhf.datasets import RewardDataset
ModuleNotFoundError: No module named 'openrlhf'
