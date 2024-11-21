[post_command] Sending request to http://127.0.0.1:8080 with data: {'id': '1732181498.768338', 'action': 'idle'}
[post_command] RequestException occurred: HTTPConnectionPool(host='127.0.0.1', port=8080): Max retries exceeded with url: / (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7f2cbc879b40>: Failed to establish a new connection: [Errno 111] Connection refused'))
Traceback (most recent call last):
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connection.py", line 199, in _new_conn
    sock = connection.create_connection(
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/util/connection.py", line 85, in create_connection
    raise err
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/util/connection.py", line 73, in create_connection
    sock.connect(sa)
ConnectionRefusedError: [Errno 111] Connection refused

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connectionpool.py", line 789, in urlopen
    response = self._make_request(
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connectionpool.py", line 495, in _make_request
    conn.request(
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connection.py", line 441, in request
    self.endheaders()
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/http/client.py", line 1278, in endheaders
    self._send_output(message_body, encode_chunked=encode_chunked)
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/http/client.py", line 1038, in _send_output
    self.send(msg)
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/http/client.py", line 976, in send
    self.connect()
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connection.py", line 279, in connect
    self.sock = self._new_conn()
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connection.py", line 214, in _new_conn
    raise NewConnectionError(
urllib3.exceptions.NewConnectionError: <urllib3.connection.HTTPConnection object at 0x7f2cbc879b40>: Failed to establish a new connection: [Errno 111] Connection refused

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/requests/adapters.py", line 667, in send
    resp = conn.urlopen(
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connectionpool.py", line 873, in urlopen
    return self.urlopen(
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connectionpool.py", line 873, in urlopen
    return self.urlopen(
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connectionpool.py", line 873, in urlopen
    return self.urlopen(
  [Previous line repeated 2 more times]
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/connectionpool.py", line 843, in urlopen
    retries = retries.increment(
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/urllib3/util/retry.py", line 519, in increment
    raise MaxRetryError(_pool, url, reason) from reason  # type: ignore[arg-type]
urllib3.exceptions.MaxRetryError: HTTPConnectionPool(host='127.0.0.1', port=8080): Max retries exceeded with url: / (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7f2cbc879b40>: Failed to establish a new connection: [Errno 111] Connection refused'))

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/home/geely-wubantu/code/virtualhome-master/virtualhome/simulation/environment/../unity_simulator/comm_unity.py", line 91, in post_command
    resp = self.requests_retry_session().post(self._address, json=request_dict)
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/requests/sessions.py", line 637, in post
    return self.request("POST", url, data=data, json=json, **kwargs)
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/requests/sessions.py", line 589, in request
    resp = self.send(prep, **send_kwargs)
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/requests/sessions.py", line 703, in send
    r = adapter.send(request, **kwargs)
  File "/home/geely-wubantu/anaconda3/envs/twosome/lib/python3.10/site-packages/requests/adapters.py", line 700, in send
    raise ConnectionError(e, request=request)
requests.exceptions.ConnectionError: HTTPConnectionPool(host='127.0.0.1', port=8080): Max retries exceeded with url: / (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7f2cbc879b40>: Failed to establish a new connection: [Errno 111] Connection refused'))
