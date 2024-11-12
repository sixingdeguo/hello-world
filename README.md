2024-11-12 09:47:25.764540: I tensorflow/core/util/port.cc:153] oneDNN custom operations are on. You may see slightly different numerical results due to floating-point round-off errors from different computation orders. To turn them off, set the environment variable `TF_ENABLE_ONEDNN_OPTS=0`.
2024-11-12 09:47:25.770708: I external/local_xla/xla/tsl/cuda/cudart_stub.cc:32] Could not find cuda drivers on your machine, GPU will not be used.
2024-11-12 09:47:25.782365: E external/local_xla/xla/stream_executor/cuda/cuda_fft.cc:477] Unable to register cuFFT factory: Attempting to register factory for plugin cuFFT when one has already been registered
WARNING: All log messages before absl::InitializeLog() is called are written to STDERR
E0000 00:00:1731404845.800301     303 cuda_dnn.cc:8310] Unable to register cuDNN factory: Attempting to register factory for plugin cuDNN when one has already been registered
E0000 00:00:1731404845.805554     303 cuda_blas.cc:1418] Unable to register cuBLAS factory: Attempting to register factory for plugin cuBLAS when one has already been registered
2024-11-12 09:47:25.825782: I tensorflow/core/platform/cpu_feature_guard.cc:210] This TensorFlow binary is optimized to use available CPU instructions in performance-critical operations.
To enable the following instructions: AVX2 AVX512F AVX512_VNNI FMA, in other operations, rebuild TensorFlow with the appropriate compiler flags.

===================================BUG REPORT===================================
Welcome to bitsandbytes. For bug reports, please run

python -m bitsandbytes

 and submit this information together with your error trace to: https://github.com/TimDettmers/bitsandbytes/issues
================================================================================
bin /opt/conda/lib/python3.10/site-packages/bitsandbytes/libbitsandbytes_cuda118.so
/opt/conda/lib/python3.10/site-packages/bitsandbytes/cuda_setup/main.py:145: UserWarning: WARNING: The following directories listed in your path were found to be non-existent: {PosixPath('/opt/conda/lib/python3.10/site-packages/cv2/../../lib64'), PosixPath('/usr/local/nvidia/lib64'), PosixPath('/usr/local/nvidia/lib')}
  warn(msg)
/opt/conda/lib/python3.10/site-packages/bitsandbytes/cuda_setup/main.py:145: UserWarning: /opt/conda/lib/python3.10/site-packages/cv2/../../lib64:/usr/local/nvidia/lib:/usr/local/nvidia/lib64 did not contain ['libcudart.so', 'libcudart.so.11.0', 'libcudart.so.12.0'] as expected! Searching further paths...
  warn(msg)
/opt/conda/lib/python3.10/site-packages/bitsandbytes/cuda_setup/main.py:145: UserWarning: WARNING: The following directories listed in your path were found to be non-existent: {PosixPath('https'), PosixPath('//ccj1jfrf19tgfg8j3enj0.ml-platform-cn-huzhou-tongyong-d01.vestack.gee-cloud.com/devinstance/di-20241112165747-rtjsx/proxy/{{port}}')}
  warn(msg)
/opt/conda/lib/python3.10/site-packages/bitsandbytes/cuda_setup/main.py:145: UserWarning: WARNING: The following directories listed in your path were found to be non-existent: {PosixPath('unix')}
  warn(msg)
/opt/conda/lib/python3.10/site-packages/bitsandbytes/cuda_setup/main.py:145: UserWarning: WARNING: The following directories listed in your path were found to be non-existent: {PosixPath('/usr/local/nvidia/bin')}
  warn(msg)
CUDA_SETUP: WARNING! libcudart.so not found in any environmental path. Searching in backup paths...
/opt/conda/lib/python3.10/site-packages/bitsandbytes/cuda_setup/main.py:145: UserWarning: Found duplicate ['libcudart.so', 'libcudart.so.11.0', 'libcudart.so.12.0'] files: {PosixPath('/usr/local/cuda/lib64/libcudart.so'), PosixPath('/usr/local/cuda/lib64/libcudart.so.11.0')}.. We'll flip a coin and try one of these, in order to fail forward.
Either way, this might cause trouble in the future:
If you get `CUDA error: invalid device function` errors, the above might be the cause and the solution is to make sure only one ['libcudart.so', 'libcudart.so.11.0', 'libcudart.so.12.0'] in the paths that we search based on your env.
  warn(msg)
CUDA SETUP: CUDA runtime path found: /usr/local/cuda/lib64/libcudart.so
CUDA SETUP: Highest compute capability among GPUs detected: 8.0
CUDA SETUP: Detected CUDA version 118
CUDA SETUP: Loading binary /opt/conda/lib/python3.10/site-packages/bitsandbytes/libbitsandbytes_cuda118.so...
pygame 2.4.0 (SDL 2.26.4, Python 3.10.13)
Hello from the pygame community. https://www.pygame.org/contribute.html
Traceback (most recent call last):
  File "/vepfs/DI/user/zhaoyue/TWOSOME-main/twosome/overcooked/ppo_llm_pomdp.py", line 192, in <module>
    agent = LLMAgent(normalization_mode=args.normalization_mode, load_8bit=args.load_8bit, task=args.task)
  File "/vepfs/DI/user/zhaoyue/TWOSOME-main/twosome/overcooked/policy_pomdp.py", line 73, in __init__
    self.llama = self._init_llama()
  File "/vepfs/DI/user/zhaoyue/TWOSOME-main/twosome/overcooked/policy_pomdp.py", line 82, in _init_llama
    model = LlamaForCausalLM.from_pretrained(
  File "/opt/conda/lib/python3.10/site-packages/transformers/modeling_utils.py", line 3609, in from_pretrained
    max_memory = get_balanced_memory(
  File "/opt/conda/lib/python3.10/site-packages/accelerate/utils/modeling.py", line 955, in get_balanced_memory
    max_memory = get_max_memory(max_memory)
  File "/opt/conda/lib/python3.10/site-packages/accelerate/utils/modeling.py", line 823, in get_max_memory
    _ = torch.tensor([0], device=i)
RuntimeError: CUDA error: device kernel image is invalid
CUDA kernel errors might be asynchronously reported at some other API call, so the stacktrace below might be incorrect.
For debugging consider passing CUDA_LAUNCH_BLOCKING=1.
Compile with `TORCH_USE_CUDA_DSA` to enable device-side assertions.
