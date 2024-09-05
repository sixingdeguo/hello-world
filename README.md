Episode [1/1]:   0%|          | 0/625 [00:00<?, ?it/s]/opt/conda/lib/python3.10/site-packages/transformers/generation/configuration_utils.py:615: UserWarning: `num_beams` is set to 1. However, `early_stopping` is set to `True` -- this flag is only used in beam-based generation modes. You should set `num_beams>1` or unset `early_stopping`.
  warnings.warn(
[rank2]:[E ProcessGroupNCCL.cpp:523] [Rank 2] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800218 milliseconds before timing out.
[rank2]:[E ProcessGroupNCCL.cpp:537] Some NCCL operations have failed or timed out. Due to the asynchronous nature of CUDA kernels, subsequent GPU operations might run on corrupted/incomplete data.
[rank2]:[E ProcessGroupNCCL.cpp:543] To avoid data inconsistency, we are taking the entire process down.
[rank2]:[E ProcessGroupNCCL.cpp:1182] [Rank 2] NCCL watchdog thread terminated with exception: [Rank 2] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800218 milliseconds before timing out.
Exception raised from checkTimeout at ../torch/csrc/distributed/c10d/ProcessGroupNCCL.cpp:525 (most recent call first):
frame #0: c10::Error::Error(c10::SourceLocation, std::string) + 0x57 (0x7f45c28ced87 in /opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so)
frame #1: c10d::ProcessGroupNCCL::WorkNCCL::checkTimeout(std::optional<std::chrono::duration<long, std::ratio<1l, 1000l> > >) + 0x1e6 (0x7f4574682f66 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #2: c10d::ProcessGroupNCCL::workCleanupLoop() + 0x19d (0x7f45746864bd in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #3: c10d::ProcessGroupNCCL::ncclCommWatchdog() + 0x119 (0x7f45746870b9 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #4: <unknown function> + 0xdbbf4 (0x7f45c20c7bf4 in /opt/conda/bin/../lib/libstdc++.so.6)
frame #5: <unknown function> + 0x94ac3 (0x7f45c3511ac3 in /usr/lib/x86_64-linux-gnu/libc.so.6)
frame #6: <unknown function> + 0x126a40 (0x7f45c35a3a40 in /usr/lib/x86_64-linux-gnu/libc.so.6)
[rank7]:[E ProcessGroupNCCL.cpp:523] [Rank 7] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800225 milliseconds before timing out.
[rank7]:[E ProcessGroupNCCL.cpp:537] Some NCCL operations have failed or timed out. Due to the asynchronous nature of CUDA kernels, subsequent GPU operations might run on corrupted/incomplete data.
[rank7]:[E ProcessGroupNCCL.cpp:543] To avoid data inconsistency, we are taking the entire process down.
[rank7]:[E ProcessGroupNCCL.cpp:1182] [Rank 7] NCCL watchdog thread terminated with exception: [Rank 7] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800225 milliseconds before timing out.
Exception raised from checkTimeout at ../torch/csrc/distributed/c10d/ProcessGroupNCCL.cpp:525 (most recent call first):
frame #0: c10::Error::Error(c10::SourceLocation, std::string) + 0x57 (0x7fcf274ced87 in /opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so)
frame #1: c10d::ProcessGroupNCCL::WorkNCCL::checkTimeout(std::optional<std::chrono::duration<long, std::ratio<1l, 1000l> > >) + 0x1e6 (0x7fced9282f66 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #2: c10d::ProcessGroupNCCL::workCleanupLoop() + 0x19d (0x7fced92864bd in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #3: c10d::ProcessGroupNCCL::ncclCommWatchdog() + 0x119 (0x7fced92870b9 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #4: <unknown function> + 0xdbbf4 (0x7fcf26cc7bf4 in /opt/conda/bin/../lib/libstdc++.so.6)
frame #5: <unknown function> + 0x94ac3 (0x7fcf280feac3 in /usr/lib/x86_64-linux-gnu/libc.so.6)
frame #6: <unknown function> + 0x126a40 (0x7fcf28190a40 in /usr/lib/x86_64-linux-gnu/libc.so.6)
[rank5]:[E ProcessGroupNCCL.cpp:523] [Rank 5] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800230 milliseconds before timing out.
[rank5]:[E ProcessGroupNCCL.cpp:537] Some NCCL operations have failed or timed out. Due to the asynchronous nature of CUDA kernels, subsequent GPU operations might run on corrupted/incomplete data.
[rank5]:[E ProcessGroupNCCL.cpp:543] To avoid data inconsistency, we are taking the entire process down.
[rank5]:[E ProcessGroupNCCL.cpp:1182] [Rank 5] NCCL watchdog thread terminated with exception: [Rank 5] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800230 milliseconds before timing out.
Exception raised from checkTimeout at ../torch/csrc/distributed/c10d/ProcessGroupNCCL.cpp:525 (most recent call first):
frame #0: c10::Error::Error(c10::SourceLocation, std::string) + 0x57 (0x7f114c0f4d87 in /opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so)
frame #1: c10d::ProcessGroupNCCL::WorkNCCL::checkTimeout(std::optional<std::chrono::duration<long, std::ratio<1l, 1000l> > >) + 0x1e6 (0x7f10fde82f66 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #2: c10d::ProcessGroupNCCL::workCleanupLoop() + 0x19d (0x7f10fde864bd in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #3: c10d::ProcessGroupNCCL::ncclCommWatchdog() + 0x119 (0x7f10fde870b9 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #4: <unknown function> + 0xdbbf4 (0x7f114b8c7bf4 in /opt/conda/bin/../lib/libstdc++.so.6)
frame #5: <unknown function> + 0x94ac3 (0x7f114cd76ac3 in /usr/lib/x86_64-linux-gnu/libc.so.6)
frame #6: <unknown function> + 0x126a40 (0x7f114ce08a40 in /usr/lib/x86_64-linux-gnu/libc.so.6)
[rank6]:[E ProcessGroupNCCL.cpp:523] [Rank 6] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800236 milliseconds before timing out.
[rank6]:[E ProcessGroupNCCL.cpp:537] Some NCCL operations have failed or timed out. Due to the asynchronous nature of CUDA kernels, subsequent GPU operations might run on corrupted/incomplete data.
[rank6]:[E ProcessGroupNCCL.cpp:543] To avoid data inconsistency, we are taking the entire process down.
[rank6]:[E ProcessGroupNCCL.cpp:1182] [Rank 6] NCCL watchdog thread terminated with exception: [Rank 6] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800236 milliseconds before timing out.
Exception raised from checkTimeout at ../torch/csrc/distributed/c10d/ProcessGroupNCCL.cpp:525 (most recent call first):
frame #0: c10::Error::Error(c10::SourceLocation, std::string) + 0x57 (0x7fb214139d87 in /opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so)
frame #1: c10d::ProcessGroupNCCL::WorkNCCL::checkTimeout(std::optional<std::chrono::duration<long, std::ratio<1l, 1000l> > >) + 0x1e6 (0x7fb1c5a82f66 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #2: c10d::ProcessGroupNCCL::workCleanupLoop() + 0x19d (0x7fb1c5a864bd in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #3: c10d::ProcessGroupNCCL::ncclCommWatchdog() + 0x119 (0x7fb1c5a870b9 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #4: <unknown function> + 0xdbbf4 (0x7fb2134c7bf4 in /opt/conda/bin/../lib/libstdc++.so.6)
frame #5: <unknown function> + 0x94ac3 (0x7fb214abdac3 in /usr/lib/x86_64-linux-gnu/libc.so.6)
frame #6: <unknown function> + 0x126a40 (0x7fb214b4fa40 in /usr/lib/x86_64-linux-gnu/libc.so.6)
[rank4]:[E ProcessGroupNCCL.cpp:523] [Rank 4] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800244 milliseconds before timing out.
[rank4]:[E ProcessGroupNCCL.cpp:537] Some NCCL operations have failed or timed out. Due to the asynchronous nature of CUDA kernels, subsequent GPU operations might run on corrupted/incomplete data.
[rank4]:[E ProcessGroupNCCL.cpp:543] To avoid data inconsistency, we are taking the entire process down.
[rank4]:[E ProcessGroupNCCL.cpp:1182] [Rank 4] NCCL watchdog thread terminated with exception: [Rank 4] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800244 milliseconds before timing out.
Exception raised from checkTimeout at ../torch/csrc/distributed/c10d/ProcessGroupNCCL.cpp:525 (most recent call first):
frame #0: c10::Error::Error(c10::SourceLocation, std::string) + 0x57 (0x7f361ff81d87 in /opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so)
frame #1: c10d::ProcessGroupNCCL::WorkNCCL::checkTimeout(std::optional<std::chrono::duration<long, std::ratio<1l, 1000l> > >) + 0x1e6 (0x7f35d1c82f66 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #2: c10d::ProcessGroupNCCL::workCleanupLoop() + 0x19d (0x7f35d1c864bd in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #3: c10d::ProcessGroupNCCL::ncclCommWatchdog() + 0x119 (0x7f35d1c870b9 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #4: <unknown function> + 0xdbbf4 (0x7f361f6c7bf4 in /opt/conda/bin/../lib/libstdc++.so.6)
frame #5: <unknown function> + 0x94ac3 (0x7f3620c35ac3 in /usr/lib/x86_64-linux-gnu/libc.so.6)
frame #6: <unknown function> + 0x126a40 (0x7f3620cc7a40 in /usr/lib/x86_64-linux-gnu/libc.so.6)
[rank1]:[E ProcessGroupNCCL.cpp:523] [Rank 1] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800249 milliseconds before timing out.
[rank1]:[E ProcessGroupNCCL.cpp:537] Some NCCL operations have failed or timed out. Due to the asynchronous nature of CUDA kernels, subsequent GPU operations might run on corrupted/incomplete data.
[rank1]:[E ProcessGroupNCCL.cpp:543] To avoid data inconsistency, we are taking the entire process down.
[rank1]:[E ProcessGroupNCCL.cpp:1182] [Rank 1] NCCL watchdog thread terminated with exception: [Rank 1] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=8388608, NumelOut=67108864, Timeout(ms)=1800000) ran for 1800249 milliseconds before timing out.
Exception raised from checkTimeout at ../torch/csrc/distributed/c10d/ProcessGroupNCCL.cpp:525 (most recent call first):
frame #0: c10::Error::Error(c10::SourceLocation, std::string) + 0x57 (0x7ff0e8d81d87 in /opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so)
frame #1: c10d::ProcessGroupNCCL::WorkNCCL::checkTimeout(std::optional<std::chrono::duration<long, std::ratio<1l, 1000l> > >) + 0x1e6 (0x7ff09aa82f66 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #2: c10d::ProcessGroupNCCL::workCleanupLoop() + 0x19d (0x7ff09aa864bd in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #3: c10d::ProcessGroupNCCL::ncclCommWatchdog() + 0x119 (0x7ff09aa870b9 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #4: <unknown function> + 0xdbbf4 (0x7ff0e84c7bf4 in /opt/conda/bin/../lib/libstdc++.so.6)
frame #5: <unknown function> + 0x94ac3 (0x7ff0e99e6ac3 in /usr/lib/x86_64-linux-gnu/libc.so.6)
frame #6: <unknown function> + 0x126a40 (0x7ff0e9a78a40 in /usr/lib/x86_64-linux-gnu/libc.so.6)
[rank3]:[E ProcessGroupNCCL.cpp:523] [Rank 3] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=1024, NumelOut=8192, Timeout(ms)=1800000) ran for 1800333 milliseconds before timing out.
[rank3]:[E ProcessGroupNCCL.cpp:537] Some NCCL operations have failed or timed out. Due to the asynchronous nature of CUDA kernels, subsequent GPU operations might run on corrupted/incomplete data.
[rank3]:[E ProcessGroupNCCL.cpp:543] To avoid data inconsistency, we are taking the entire process down.
[rank3]:[E ProcessGroupNCCL.cpp:1182] [Rank 3] NCCL watchdog thread terminated with exception: [Rank 3] Watchdog caught collective operation timeout: WorkNCCL(SeqNum=15074, OpType=_ALLGATHER_BASE, NumelIn=1024, NumelOut=8192, Timeout(ms)=1800000) ran for 1800333 milliseconds before timing out.
Exception raised from checkTimeout at ../torch/csrc/distributed/c10d/ProcessGroupNCCL.cpp:525 (most recent call first):
frame #0: c10::Error::Error(c10::SourceLocation, std::string) + 0x57 (0x7f061a581d87 in /opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so)
frame #1: c10d::ProcessGroupNCCL::WorkNCCL::checkTimeout(std::optional<std::chrono::duration<long, std::ratio<1l, 1000l> > >) + 0x1e6 (0x7f05cc282f66 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #2: c10d::ProcessGroupNCCL::workCleanupLoop() + 0x19d (0x7f05cc2864bd in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #3: c10d::ProcessGroupNCCL::ncclCommWatchdog() + 0x119 (0x7f05cc2870b9 in /opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so)
frame #4: <unknown function> + 0xdbbf4 (0x7f0619cc7bf4 in /opt/conda/bin/../lib/libstdc++.so.6)
frame #5: <unknown function> + 0x94ac3 (0x7f061b1dbac3 in /usr/lib/x86_64-linux-gnu/libc.so.6)
frame #6: <unknown function> + 0x126a40 (0x7f061b26da40 in /usr/lib/x86_64-linux-gnu/libc.so.6)
[2024-09-05 09:14:29,066] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 4984
[2024-09-05 09:14:51,384] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 4985
[2024-09-05 09:15:21,411] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 4986
[2024-09-05 09:15:21,411] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 4987
[2024-09-05 09:15:51,429] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 4988
[2024-09-05 09:16:21,435] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 4989
[2024-09-05 09:16:51,440] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 4990
[2024-09-05 09:17:21,445] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 4991
[2024-09-05 09:17:51,446] [ERROR] [launch.py:325:sigkill_handler] ['/opt/conda/bin/python', '-u', '-m', 'openrlhf.cli.train_ppo', '--local_rank=7', '--pretrain', '/vepfs/DI/beijing-public/models/Qwen2-72B', '--reward_pretrain', '/vepfs/DI/user/zhaoyue/exp_result/rm_Qwen_1.5_0', '--save_path', '/vepfs/DI/user/zhaoyue/exp_result/openrlhf_0904_dev/Qwen2-70+1.5B-PPO', '--save_steps', '100', '--logging_steps', '1', '--eval_steps', '20', '--micro_train_batch_size', '1', '--train_batch_size', '32', '--micro_rollout_batch_size', '1', '--rollout_batch_size', '32', '--max_epochs', '1', '--prompt_max_len', '512', '--generate_max_len', '512', '--zero_stage', '3', '--bf16', '--actor_learning_rate', '5e-7', '--critic_learning_rate', '9e-6', '--init_kl_coef', '0.01', '--prompt_data', '/vepfs/DI/beijing-public/datasets/preference/OpenRLHF/prompt-collection-v0.1', '--input_key', 'context_messages', '--max_samples', '5000', '--normalize_reward', '--adam_offload', '--flash_attn', '--gradient_checkpointing', '--max_ckpt_num', '50', '--ckpt_path', '/vepfs/DI/user/zhaoyue/exp_result/openrlhf_0904_dev/Qwen2-70+1.5B-PPO/ckpt', '--use_tensorboard', '--tensorboard_logdir', '/vepfs/DI/user/zhaoyue/exp_result/openrlhf_0904_dev/Qwen2-70+1.5B-PPO', '--max_ckpt_mem', '50000'] exits with return code = -6
