import vllm
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/opt/conda/lib/python3.10/site-packages/vllm/__init__.py", line 3, in <module>
    from vllm.engine.arg_utils import AsyncEngineArgs, EngineArgs
  File "/opt/conda/lib/python3.10/site-packages/vllm/engine/arg_utils.py", line 6, in <module>
    from vllm.config import (CacheConfig, DecodingConfig, DeviceConfig,
  File "/opt/conda/lib/python3.10/site-packages/vllm/config.py", line 11, in <module>
    from vllm.logger import init_logger
  File "/opt/conda/lib/python3.10/site-packages/vllm/logger.py", line 74, in <module>
    logger = init_logger(__name__)
  File "/opt/conda/lib/python3.10/site-packages/vllm/logger.py", line 60, in init_logger
    logger.setLevel(os.getenv("LOG_LEVEL"))
  File "/opt/conda/lib/python3.10/logging/__init__.py", line 1452, in setLevel
    self.level = _checkLevel(level)
  File "/opt/conda/lib/python3.10/logging/__init__.py", line 198, in _checkLevel
    raise ValueError("Unknown level: %r" % level)
ValueError: Unknown level: 'debug'
>>> 
>>> import vllm
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/opt/conda/lib/python3.10/site-packages/vllm/__init__.py", line 3, in <module>
    from vllm.engine.arg_utils import AsyncEngineArgs, EngineArgs
  File "/opt/conda/lib/python3.10/site-packages/vllm/engine/arg_utils.py", line 6, in <module>
    from vllm.config import (CacheConfig, DecodingConfig, DeviceConfig,
  File "/opt/conda/lib/python3.10/site-packages/vllm/config.py", line 11, in <module>
    from vllm.logger import init_logger
  File "/opt/conda/lib/python3.10/site-packages/vllm/logger.py", line 74, in <module>
    logger = init_logger(__name__)
  File "/opt/conda/lib/python3.10/site-packages/vllm/logger.py", line 60, in init_logger
    logger.setLevel(os.getenv("LOG_LEVEL"))
  File "/opt/conda/lib/python3.10/logging/__init__.py", line 1452, in setLevel
    self.level = _checkLevel(level)
  File "/opt/conda/lib/python3.10/logging/__init__.py", line 198, in _checkLevel
    raise ValueError("Unknown level: %r" % level)
ValueError: Unknown level: 'debug'
