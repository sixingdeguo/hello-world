"OpenRLHF only supports vLLM >= 0.4.1"
[Errno 28] No space left on device



ERROR: Could not install packages due to an OSError: [('/opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libtorch_cuda.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cuda.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libtorch_cuda.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libtorch.so', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libtorch.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libtorch.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libtorch.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_cnn_infer.so.8', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_cnn_infer.so.8', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_cnn_infer.so.8' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_cnn_infer.so.8'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_python.so', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libtorch_python.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_python.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libtorch_python.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libcaffe2_nvrtc.so', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcaffe2_nvrtc.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libcaffe2_nvrtc.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcaffe2_nvrtc.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cpu.so', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libtorch_cpu.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libtorch_cpu.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libtorch_cpu.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_cnn_train.so.8', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_cnn_train.so.8', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_cnn_train.so.8' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_cnn_train.so.8'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_adv_train.so.8', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_adv_train.so.8', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_adv_train.so.8' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_adv_train.so.8'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libc10_cuda.so', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libc10_cuda.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libc10_cuda.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libc10_cuda.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libc10.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libc10.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libc10.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_ops_train.so.8', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_ops_train.so.8', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_ops_train.so.8' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_ops_train.so.8'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn.so.8', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn.so.8', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn.so.8' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn.so.8'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_adv_infer.so.8', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_adv_infer.so.8', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libcudnn_adv_infer.so.8' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcudnn_adv_infer.so.8'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libcupti-ae79a72e.so.11.8', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcupti-ae79a72e.so.11.8', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libcupti-ae79a72e.so.11.8' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libcupti-ae79a72e.so.11.8'"), ('/opt/conda/lib/python3.10/site-packages/torch/lib/libshm.so', '/opt/conda/lib/python3.10/site-packages/~orch/lib/libshm.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/lib/libshm.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/lib/libshm.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/fft', '/opt/conda/lib/python3.10/site-packages/~orch/fft', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/~orch/fft'"), ('/opt/conda/lib/python3.10/site-packages/torch/_subclasses', '/opt/conda/lib/python3.10/site-packages/~orch/_subclasses', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/~orch/_subclasses'"), ('/opt/conda/lib/python3.10/site-packages/torch/signal', '/opt/conda/lib/python3.10/site-packages/~orch/signal', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/~orch/signal'"), ('/opt/conda/lib/python3.10/site-packages/torch/_jit_internal.py', '/opt/conda/lib/python3.10/site-packages/~orch/_jit_internal.py', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/_jit_internal.py' -> '/opt/conda/lib/python3.10/site-packages/~orch/_jit_internal.py'"), ('/opt/conda/lib/python3.10/site-packages/torch/optim', '/opt/conda/lib/python3.10/site-packages/~orch/optim', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/~orch/optim'"), ('/opt/conda/lib/python3.10/site-packages/torch/_C.cpython-310-x86_64-linux-gnu.so', '/opt/conda/lib/python3.10/site-packages/~orch/_C.cpython-310-x86_64-linux-gnu.so', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/_C.cpython-310-x86_64-linux-gnu.so' -> '/opt/conda/lib/python3.10/site-packages/~orch/_C.cpython-310-x86_64-linux-gnu.so'"), ('/opt/conda/lib/python3.10/site-packages/torch/types.py', '/opt/conda/lib/python3.10/site-packages/~orch/types.py', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/types.py' -> '/opt/conda/lib/python3.10/site-packages/~orch/types.py'"), ('/opt/conda/lib/python3.10/site-packages/torch/__init__.py', '/opt/conda/lib/python3.10/site-packages/~orch/__init__.py', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/__init__.py' -> '/opt/conda/lib/python3.10/site-packages/~orch/__init__.py'"), ('/opt/conda/lib/python3.10/site-packages/torch/jit', '/opt/conda/lib/python3.10/site-packages/~orch/jit', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/~orch/jit'"), ('/opt/conda/lib/python3.10/site-packages/torch/_tensor_docs.py', '/opt/conda/lib/python3.10/site-packages/~orch/_tensor_docs.py', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/_tensor_docs.py' -> '/opt/conda/lib/python3.10/site-packages/~orch/_tensor_docs.py'"), ('/opt/conda/lib/python3.10/site-packages/torch/_deploy.py', '/opt/conda/lib/python3.10/site-packages/~orch/_deploy.py', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/_deploy.py' -> '/opt/conda/lib/python3.10/site-packages/~orch/_deploy.py'"), ('/opt/conda/lib/python3.10/site-packages/torch/serialization.py', '/opt/conda/lib/python3.10/site-packages/~orch/serialization.py', "[Errno 28] No space left on device: '/opt/conda/lib/python3.10/site-packages/torch/serialization.py' -> '/opt/conda/lib/python3.10/site-packages/~orch/serialization.py'")]
