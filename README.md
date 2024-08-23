    self.strategy.optimizer_step(self.actor_optim, self.actor, self.actor_scheduler, name="actor")
  File "/tmp/ray/session_2024-08-23_03-41-32_382611_4751/runtime_resources/working_dir_files/_ray_pkg_d9f21ced79d56673/openrlhf/utils/deepspeed.py", line 109, in optimizer_step
    model.step()
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/engine.py", line 2160, in step
    self._take_model_step(lr_kwargs)
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/engine.py", line 2066, in _take_model_step
    self.optimizer.step()
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/utils/nvtx.py", line 15, in wrapped_fn
    ret_val = func(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/zero/stage3.py", line 2050, in step
    self._optimizer_step(sub_group_id)
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/runtime/zero/stage3.py", line 939, in _optimizer_step
    cpu_loss = self.optimizer.step()
  File "/opt/conda/lib/python3.10/site-packages/torch/optim/lr_scheduler.py", line 75, in wrapper
    return wrapped(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/torch/optim/optimizer.py", line 385, in wrapper
    out = func(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/torch/utils/_contextlib.py", line 115, in decorate_context
    return func(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/deepspeed/ops/adam/cpu_adam.py", line 163, in step
    self.ds_opt_adam.adam_update(self.opt_id, state['step'], group['lr'], beta1, beta2, group['eps'],
