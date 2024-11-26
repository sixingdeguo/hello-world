Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 203, in _new_conn
    sock = connection.create_connection(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/util/connection.py", line 85, in create_connection
    raise err
  File "/opt/conda/lib/python3.10/site-packages/urllib3/util/connection.py", line 73, in create_connection
    sock.connect(sa)
ConnectionRefusedError: [Errno 111] Connection refused

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 791, in urlopen
    response = self._make_request(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 497, in _make_request
    conn.request(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 395, in request
    self.endheaders()
  File "/opt/conda/lib/python3.10/http/client.py", line 1278, in endheaders
    self._send_output(message_body, encode_chunked=encode_chunked)
  File "/opt/conda/lib/python3.10/http/client.py", line 1038, in _send_output
    self.send(msg)
  File "/opt/conda/lib/python3.10/http/client.py", line 976, in send
    self.connect()
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 243, in connect
    self.sock = self._new_conn()
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 218, in _new_conn
    raise NewConnectionError(
urllib3.exceptions.NewConnectionError: <urllib3.connection.HTTPConnection object at 0x7f4b98f50550>: Failed to establish a new connection: [Errno 111] Connection refused

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/opt/conda/lib/python3.10/site-packages/requests/adapters.py", line 486, in send
    resp = conn.urlopen(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 845, in urlopen
    retries = retries.increment(
  File "/opt/conda/lib/python3.10/site-packages/urllib3/util/retry.py", line 515, in increment
    raise MaxRetryError(_pool, url, reason) from reason  # type: ignore[arg-type]
urllib3.exceptions.MaxRetryError: HTTPConnectionPool(host='127.0.0.1', port=8080): Max retries exceeded with url: / (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7f4b98f50550>: Failed to establish a new connection: [Errno 111] Connection refused'))

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/vepfs/DI/user/zhaoyue/virtualhome-master/virtualhome/simulation/environment/../unity_simulator/comm_unity.py", line 92, in post_command
    resp = requests.post(self._address, json=request_dict, timeout=self.timeout_wait)
  File "/opt/conda/lib/python3.10/site-packages/requests/api.py", line 115, in post
    return request("post", url, data=data, json=json, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/requests/api.py", line 59, in request
    return session.request(method=method, url=url, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/requests/sessions.py", line 589, in request
    resp = self.send(prep, **send_kwargs)
  File "/opt/conda/lib/python3.10/site-packages/requests/sessions.py", line 703, in send
    r = adapter.send(request, **kwargs)
  File "/opt/conda/lib/python3.10/site-packages/requests/adapters.py", line 519, in send
    raise ConnectionError(e, request=request)
requests.exceptions.ConnectionError: HTTPConnectionPool(host='127.0.0.1', port=8080): Max retries exceeded with url: / (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7f4b98f50550>: Failed to establish a new connection: [Errno 111] Connection refused'))

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/vepfs/DI/user/zhaoyue/virtualhome-master/virtualhome/demo/test_unity_environment.py", line 14, in <module>
    env = UnityEnvironment(num_agents=2, executable_args=exec_args)
  File "/vepfs/DI/user/zhaoyue/virtualhome-master/virtualhome/demo/../simulation/environment/unity_environment.py", line 103, in __init__
    self.reset()
  File "/vepfs/DI/user/zhaoyue/virtualhome-master/virtualhome/demo/../simulation/environment/unity_environment.py", line 168, in reset
    self.comm.reset()
  File "/vepfs/DI/user/zhaoyue/virtualhome-master/virtualhome/simulation/environment/../unity_simulator/comm_unity.py", line 223, in reset
    response = self.post_command({'id': str(time.time()), 'action': 'reset',
  File "/vepfs/DI/user/zhaoyue/virtualhome-master/virtualhome/simulation/environment/../unity_simulator/comm_unity.py", line 98, in post_command
    raise UnityCommunicationException(str(e))
unity_simulator.comm_unity.UnityCommunicationException: HTTPConnectionPool(host='127.0.0.1', port=8080): Max retries exceeded with url: / (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7f4b98f50550>: Failed to establish a new connection: [Errno 111] Connection refused'))
