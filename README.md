nohup: ignoring input
2024-08-21 10:51:26,996	INFO dashboard_sdk.py:338 -- Uploading package gcs://_ray_pkg_8ea6db8336ab93a9.zip.
2024-08-21 10:51:26,996	INFO packaging.py:530 -- Creating a file package for local directory '/vepfs/DI/user/zhaoyue/openRLHF/'.
2024-08-21 10:51:26,874	INFO cli.py:36 -- [37mJob submission server address[39m: [1mhttp://127.0.0.1:8265[22m
2024-08-21 10:51:27,072	SUCC cli.py:60 -- [32m-------------------------------------------------------[39m
2024-08-21 10:51:27,072	SUCC cli.py:61 -- [32mJob 'raysubmit_AUsan4rdgQPB1615' submitted successfully[39m
2024-08-21 10:51:27,072	SUCC cli.py:62 -- [32m-------------------------------------------------------[39m
2024-08-21 10:51:27,072	INFO cli.py:286 -- [36mNext steps[39m
2024-08-21 10:51:27,072	INFO cli.py:287 -- Query the logs of the job:
2024-08-21 10:51:27,073	INFO cli.py:289 -- [1mray job logs raysubmit_AUsan4rdgQPB1615[22m
2024-08-21 10:51:27,073	INFO cli.py:291 -- Query the status of the job:
2024-08-21 10:51:27,073	INFO cli.py:293 -- [1mray job status raysubmit_AUsan4rdgQPB1615[22m
2024-08-21 10:51:27,073	INFO cli.py:295 -- Request the job to be stopped:
2024-08-21 10:51:27,073	INFO cli.py:297 -- [1mray job stop raysubmit_AUsan4rdgQPB1615[22m
2024-08-21 10:51:27,075	INFO cli.py:304 -- Tailing logs until the job exits (disable with --no-wait):
[2024-08-21 10:51:30,203] [INFO] [real_accelerator.py:203:get_accelerator] Setting ds_accelerator to cuda (auto detect)
[93m [WARNING] [0m async_io requires the dev libaio .so object and headers but these were not found.
[93m [WARNING] [0m async_io: please install the libaio-dev package with apt
[93m [WARNING] [0m If libaio is already installed (perhaps from source), try setting the CFLAGS and LDFLAGS environment variables to where it can be found.
[93m [WARNING] [0m Please specify the CUTLASS repo directory as environment variable $CUTLASS_PATH
[93m [WARNING] [0m sparse_attn requires a torch version >= 1.5 and < 2.0 but detected 2.1
[93m [WARNING] [0m using untested triton version (2.1.0), only 1.0.0 is known to be compatible
/opt/conda/lib/python3.10/site-packages/transformers/deepspeed.py:24: FutureWarning: transformers.deepspeed module is deprecated and will be removed in a future version. Please import deepspeed modules directly from transformers.integrations
  warnings.warn(
2024-08-21 10:51:32,553	INFO worker.py:1429 -- Using address 10.132.206.205:6379 set in the environment variable RAY_ADDRESS
2024-08-21 10:51:32,553	INFO worker.py:1564 -- Connecting to existing Ray cluster at address: 10.132.206.205:6379...
2024-08-21 10:51:32,559	INFO worker.py:1740 -- Connected to Ray cluster. View the dashboard at [1m[32m127.0.0.1:8265 [39m[22m
[36m(pid=41311)[0m [2024-08-21 10:51:36,105] [INFO] [real_accelerator.py:203:get_accelerator] Setting ds_accelerator to cuda (auto detect)
[36m(pid=41311)[0m [93m [WARNING] [0m async_io requires the dev libaio .so object and headers but these were not found.
[36m(pid=41311)[0m [93m [WARNING] [0m async_io: please install the libaio-dev package with apt
[36m(pid=41311)[0m [93m [WARNING] [0m If libaio is already installed (perhaps from source), try setting the CFLAGS and LDFLAGS environment variables to where it can be found.
[36m(pid=41311)[0m [93m [WARNING] [0m Please specify the CUTLASS repo directory as environment variable $CUTLASS_PATH
[36m(pid=41311)[0m [93m [WARNING] [0m sparse_attn requires a torch version >= 1.5 and < 2.0 but detected 2.1
[36m(pid=41311)[0m [93m [WARNING] [0m using untested triton version (2.1.0), only 1.0.0 is known to be compatible
[36m(pid=41311)[0m /opt/conda/lib/python3.10/site-packages/transformers/deepspeed.py:24: FutureWarning: transformers.deepspeed module is deprecated and will be removed in a future version. Please import deepspeed modules directly from transformers.integrations
[36m(pid=41311)[0m   warnings.warn(
2024-08-21 11:09:52,197	INFO cli.py:86 -- Status for job 'raysubmit_AUsan4rdgQPB1615': RUNNING
2024-08-21 11:09:52,197	INFO cli.py:88 -- Status message: Job is currently running.
