python -m torch.distributed.launch --nproc_per_node <单个实例上的进程数> --master_addr $MLP_WORKER_0_HOST --node_rank $MLP_ROLE_INDEX --master_port $MLP_WORKER_0_PORT --nnodes $MLP_WORKER_NUM <代码文件的绝对路径>

torch.distributed.elastic.multiprocessing.errors.ChildFailedError: 
    from openrlhf.datasets import RewardDataset
ModuleNotFoundError: No module named 'openrlhf'

`--address` is a required flag unless starting a head node with `--head`.
/opt/conda/bin/python3: Error while finding module specification for 'openrlhf.cli.train_ppo_ray' (ModuleNotFoundError: No module named 'openrlhf')

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/zipfile.py", line 1776, in write
    shutil.copyfileobj(src, dest, 1024*8)
  File "/opt/conda/lib/python3.10/shutil.py", line 198, in copyfileobj
    fdst_write(buf)
  File "/opt/conda/lib/python3.10/zipfile.py", line 1141, in write
    self._fileobj.write(data)
OSError: [Errno 28] No space left on device

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 418, in _zip_directory
    _dir_travel(dir_path, excludes, handler, logger=logger)
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 131, in _dir_travel
    _dir_travel(sub_path, excludes, handler, logger=logger)
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 131, in _dir_travel
    _dir_travel(sub_path, excludes, handler, logger=logger)
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 131, in _dir_travel
    _dir_travel(sub_path, excludes, handler, logger=logger)
  [Previous line repeated 1 more time]
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 128, in _dir_travel
    raise e
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 125, in _dir_travel
    handler(path)
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 415, in handler
    zip_handler.write(path, to_path)
  File "/opt/conda/lib/python3.10/zipfile.py", line 1775, in write
    with open(filename, "rb") as src, self.open(zinfo, 'w') as dest:
  File "/opt/conda/lib/python3.10/zipfile.py", line 1180, in close
    self._fileobj.seek(self._zinfo.header_offset)
OSError: [Errno 28] No space left on device

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/zipfile.py", line 1838, in close
    self.fp.seek(self.start_dir)
OSError: [Errno 28] No space left on device

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/opt/conda/bin/ray", line 8, in <module>
    sys.exit(main())
  File "/opt/conda/lib/python3.10/site-packages/ray/scripts/scripts.py", line 2612, in main
    return cli()
  File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1157, in __call__
    return self.main(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1078, in main
    rv = self.invoke(ctx)
  File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1688, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1688, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1434, in invoke
    return ctx.invoke(self.callback, **ctx.params)
  File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 783, in invoke
    return __callback(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/cli_utils.py", line 54, in wrapper
    return func(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/ray/autoscaler/_private/cli_logger.py", line 856, in wrapper
    return f(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/cli.py", line 273, in submit
    job_id = client.submit_job(
  File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/sdk.py", line 214, in submit_job
    self._upload_working_dir_if_needed(runtime_env)
  File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 398, in _upload_working_dir_if_needed
    upload_working_dir_if_needed(runtime_env, upload_fn=_upload_fn)
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/working_dir.py", line 98, in upload_working_dir_if_needed
    upload_fn(working_dir, excludes=excludes)
  File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 391, in _upload_fn
    self._upload_package_if_needed(
  File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 377, in _upload_package_if_needed
    self._upload_package(
  File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 345, in _upload_package
    create_package(
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 531, in create_package
    _zip_directory(
  File "/opt/conda/lib/python3.10/site-packages/ray/_private/runtime_env/packaging.py", line 396, in _zip_directory
    with ZipFile(pkg_file, "w") as zip_handler:
  File "/opt/conda/lib/python3.10/zipfile.py", line 1312, in __exit__
    self.close()
  File "/opt/conda/lib/python3.10/zipfile.py", line 1843, in close
    self._fpclose(fp)
  File "/opt/conda/lib/python3.10/zipfile.py", line 1943, in _fpclose
    fp.close()
OSError: [Errno 28] No space left on device


https://docs.ray.io/en/latest/cluster/running-applications/job-submission/index.html
