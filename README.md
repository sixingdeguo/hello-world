
  File "/opt/conda/lib/python3.10/runpy.py", line 196, in _run_module_as_main
    return _run_code(code, main_globals, None,
  File "/opt/conda/lib/python3.10/runpy.py", line 86, in _run_code
    exec(code, run_globals)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/cli/train_sft.py", line 209, in <module>
    train(args)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/cli/train_sft.py", line 128, in train
    trainer.fit(args)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/trainer/sft_trainer.py", line 134, in fit
    self.strategy.optimizer_step(self.optimizer, self.model, self.scheduler)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/utils/deepspeed.py", line 110, in optimizer_step
    model.step()
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/engine.py", line 2204, in step
    self._take_model_step(lr_kwargs)
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/engine.py", line 2110, in _take_model_step
    self.optimizer.step()
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/zero/stage_1_and_2.py", line 1853, in step
    scaled_global_grad_norm = self.scaled_global_norm()
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/zero/stage_1_and_2.py", line 1794, in scaled_global_norm
    norm_groups.append(self.get_grad_norm_direct(self.averaged_gradients[i], self.params_in_partition[i]))
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/zero/stage_1_and_2.py", line 1690, in get_grad_norm_direct
    for g, p in zip(gradients, params):
TypeError: 'NoneType' object is not iterable
