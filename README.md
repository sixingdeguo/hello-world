# hello-world
hello world
21213131

PKU SMS
Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 203, in _new_conn
    sock = connection.create_connection(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/util/connection.py", line 85, in create_connection
    raise err
  File "/opt/conda/lib/python3.10/site-packages/urllib3/util/connection.py", line 73, in create_connection
    sock.connect(sa)
OSError: [Errno 101] Network is unreachable

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 791, in urlopen
    response = self._make_request(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 492, in _make_request
    raise new_e
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 468, in _make_request
    self._validate_conn(conn)
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 1097, in _validate_conn
    conn.connect()
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 611, in connect
    self.sock = sock = self._new_conn()
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 218, in _new_conn
    raise NewConnectionError(
urllib3.exceptions.NewConnectionError: <urllib3.connection.HTTPSConnection object at 0x7fa248b01420>: Failed to establish a new connection: [Errno 101] Network is unreachable

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/requests/adapters.py", line 486, in send
    resp = conn.urlopen(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 845, in urlopen
    retries = retries.increment(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/util/retry.py", line 515, in increment
    raise MaxRetryError(_pool, url, reason) from reason  # type: ignore[arg-type]
urllib3.exceptions.MaxRetryError: HTTPSConnectionPool(host='huggingface.co', port=443): Max retries exceeded with url: /meta-llama/Meta-Llama-3-8B/resolve/main/config.json (Caused by NewConnectionError('<urllib3.connection.HTTPSConnection object at 0x7fa248b01420>: Failed to establish a new connection: [Errno 101] Network is unreachable'))

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/file_download.py", line 1751, in _get_metadata_or_catch_error
    metadata = get_hf_file_metadata(
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/utils/_validators.py", line 114, in _inner_fn
    return fn(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/file_download.py", line 1673, in get_hf_file_metadata
    r = _request_wrapper(
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/file_download.py", line 376, in _request_wrapper
    response = _request_wrapper(
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/file_download.py", line 399, in _request_wrapper
    response = get_session().request(method=method, url=url, **params)
  File "/opt/conda/lib/python3.10/site-packages/requests/sessions.py", line 589, in request
    resp = self.send(prep, **send_kwargs)
  File "/opt/conda/lib/python3.10/site-packages/requests/sessions.py", line 703, in send
    r = adapter.send(request, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/utils/_http.py", line 66, in send
    return super().send(request, *args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/requests/adapters.py", line 519, in send
    raise ConnectionError(e, request=request)
requests.exceptions.ConnectionError: (MaxRetryError("HTTPSConnectionPool(host='huggingface.co', port=443): Max retries exceeded with url: /meta-llama/Meta-Llama-3-8B/resolve/main/config.json (Caused by NewConnectionError('<urllib3.connection.HTTPSConnection object at 0x7fa248b01420>: Failed to establish a new connection: [Errno 101] Network is unreachable'))"), '(Request ID: 07d45434-e2f9-4079-bfb2-aca9be9608b7)')

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/transformers/utils/hub.py", line 402, in cached_file
    resolved_file = hf_hub_download(
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/utils/_deprecation.py", line 101, in inner_f
    return f(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/utils/_validators.py", line 114, in _inner_fn
    return fn(*args, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/file_download.py", line 1240, in hf_hub_download
    return _hf_hub_download_to_cache_dir(
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/file_download.py", line 1347, in _hf_hub_download_to_cache_dir
    _raise_on_head_call_error(head_call_error, force_download, local_files_only)
  File "/opt/conda/lib/python3.10/site-packages/huggingface_hub/file_download.py", line 1857, in _raise_on_head_call_error
    raise LocalEntryNotFoundError(
huggingface_hub.utils._errors.LocalEntryNotFoundError: An error happened while trying to locate the file on the Hub and we cannot find the requested files in the local cache. Please check your connection and try again or make sure your Internet connection is on.

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/runpy.py", line 196, in _run_module_as_main
    return _run_code(code, main_globals, None,
  File "/opt/conda/lib/python3.10/runpy.py", line 86, in _run_code
    exec(code, run_globals)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/cli/train_sft.py", line 211, in <module>
    train(args)
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/cli/train_sft.py", line 21, in train
    model = Actor(
  File "/vepfs/DI/user/zhaoyue/OpenRLHF/openrlhf/models/actor.py", line 65, in __init__
    self.model = AutoModelForCausalLM.from_pretrained(
  File "/opt/conda/lib/python3.10/site-packages/transformers/models/auto/auto_factory.py", line 524, in from_pretrained
    config, kwargs = AutoConfig.from_pretrained(
  File "/opt/conda/lib/python3.10/site-packages/transformers/models/auto/configuration_auto.py", line 972, in from_pretrained
    config_dict, unused_kwargs = PretrainedConfig.get_config_dict(pretrained_model_name_or_path, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/transformers/configuration_utils.py", line 632, in get_config_dict
    config_dict, kwargs = cls._get_config_dict(pretrained_model_name_or_path, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/transformers/configuration_utils.py", line 689, in _get_config_dict
    resolved_config_file = cached_file(
  File "/opt/conda/lib/python3.10/site-packages/transformers/utils/hub.py", line 445, in cached_file
    raise EnvironmentError(
OSError: We couldn't connect to 'https://huggingface.co' to load this file, couldn't find it in the cached files and it looks like meta-llama/Meta-Llama-3-8B is not the path to a directory containing a file named config.json.
Checkout your internet connection or see how to run the library in offline mode at 'https://huggingface.co/docs/transformers/installation#offline-mode'.


https://huggingface.co/OpenRLHF

from transformers import AutoModelForCausalLM, AutoTokenizer

model_name = "model_name"  # 替换为实际的模型名称，例如 "gpt2"
model = AutoModelForCausalLM.from_pretrained(model_name)
tokenizer = AutoTokenizer.from_pretrained(model_name)

