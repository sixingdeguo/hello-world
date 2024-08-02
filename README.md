https://huggingface.co/OpenRLHF


https://huggingface.co/datasets/Open-Orca/OpenOrca
https://huggingface.co/datasets/OpenRLHF/preference_dataset_mixture2_and_safe_pku
https://huggingface.co/datasets/OpenRLHF/prompt-collection-v0.1
https://huggingface.co/datasets/OpenRLHF/preference_700K


数据读取错误

wandb: W&B API key is configured. Use `wandb login --relogin` to force relogin
Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/runpy.py", line 196, in _run_module_as_main
    return _run_code(code, main_globals, None,
  File "/opt/conda/lib/python3.10/runpy.py", line 86, in _run_code
    exec(code, run_globals)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/cli/train_sft.py", line 211, in <module>
    train(args)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/cli/train_sft.py", line 114, in train
    trainer = SFTTrainer(
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/trainer/sft_trainer.py", line 73, in __init__
    wandb.login(key=strategy.args.use_wandb)
  File "/opt/conda/lib/python3.10/site-packages/wandb/sdk/wandb_login.py", line 84, in login
    configured = _login(
  File "/opt/conda/lib/python3.10/site-packages/wandb/sdk/wandb_login.py", line 340, in _login
    wlogin.configure_api_key(key)
  File "/opt/conda/lib/python3.10/site-packages/wandb/sdk/wandb_login.py", line 221, in configure_api_key
    apikey.write_key(self._settings, key)
  File "/opt/conda/lib/python3.10/site-packages/wandb/sdk/lib/apikey.py", line 252, in write_key
    raise ValueError(
ValueError: API key must be 40 characters long, yours was 13
Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/runpy.py", line 196, in _run_module_as_main
    return _run_code(code, main_globals, None,
  File "/opt/conda/lib/python3.10/runpy.py", line 86, in _run_code
    exec(code, run_globals)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/cli/train_sft.py", line 211, in <module>
    train(args)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/cli/train_sft.py", line 114, in train
    trainer = SFTTrainer(
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/trainer/sft_trainer.py", line 73, in __init__
    wandb.login(key=strategy.args.use_wandb)
  File "/opt/conda/lib/python3.10/site-packages/wandb/sdk/wandb_login.py", line 84, in login
    configured = _login(
  File "/opt/conda/lib/python3.10/site-packages/wandb/sdk/wandb_login.py", line 340, in _login
    wlogin.configure_api_key(key)
  File "/opt/conda/lib/python3.10/site-packages/wandb/sdk/wandb_login.py", line 221, in configure_api_key
    apikey.write_key(self._settings, key)
  File "/opt/conda/lib/python3.10/site-packages/wandb/sdk/lib/apikey.py", line 252, in write_key
    raise ValueError(
ValueError: API key must be 40 characters long, yours was 13
[2024-08-02 03:43:23,037] [INFO] [launch.py:319:sigkill_handler] Killing subprocess 40473
[2024-08-02 03:43:23,037] [ERROR] [launch.py:325:sigkill_handler] ['/opt/conda/bin/python', '-u', '-m', 'openrlhf.cli.train_sft', '--local_rank=0', '--max_len', '4096', '--dataset', '/vepfs/DI/beijing-private/sft/datasets/general_sft/exp_0422/general_sft_dataset/general_sft_data_270-20240417.json', '--input_key', 'prompt', '--output_key', 'response', '--input_template', 'User: {}\\nAssistant: ', '--train_batch_size', '256', '--micro_train_batch_size', '2', '--max_samples', '500000', '--pretrain', '/vepfs/DI/beijing-public/models/Llama-2-7b-hf', '--save_path', './checkpoint/Llama-2-7b-hf', '--save_steps', '-1', '--logging_steps', '1', '--eval_steps', '-1', '--zero_stage', '2', '--max_epochs', '1', '--bf16', '--flash_attn', '--learning_rate', '5e-6', '--gradient_checkpointing', '--use_wandb', '{wandb_token}'] exits with return code = 1
