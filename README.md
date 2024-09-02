worker-0 >> Traceback (most recent call last):
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 203, in _new_conn
worker-0 >>     sock = connection.create_connection(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/util/connection.py", line 85, in create_connection
worker-0 >>     raise err
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/util/connection.py", line 73, in create_connection
worker-0 >>     sock.connect(sa)
worker-0 >> ConnectionRefusedError: [Errno 111] Connection refused
worker-0 >> The above exception was the direct cause of the following exception:
worker-0 >> Traceback (most recent call last):
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 791, in urlopen
worker-0 >>     response = self._make_request(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 497, in _make_request
worker-0 >>     conn.request(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 395, in request
worker-0 >>     self.endheaders()
worker-0 >>   File "/opt/conda/lib/python3.10/http/client.py", line 1278, in endheaders
worker-0 >>     self._send_output(message_body, encode_chunked=encode_chunked)
worker-0 >>   File "/opt/conda/lib/python3.10/http/client.py", line 1038, in _send_output
worker-0 >>     self.send(msg)
worker-0 >>   File "/opt/conda/lib/python3.10/http/client.py", line 976, in send
worker-0 >>     self.connect()
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 243, in connect
worker-0 >>     self.sock = self._new_conn()
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/connection.py", line 218, in _new_conn
worker-0 >>     raise NewConnectionError(
worker-0 >> urllib3.exceptions.NewConnectionError: <urllib3.connection.HTTPConnection object at 0x7fc7937321d0>: Failed to establish a new connection: [Errno 111] Connection refused
worker-0 >> The above exception was the direct cause of the following exception:
worker-0 >> Traceback (most recent call last):
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/requests/adapters.py", line 486, in send
worker-0 >>     resp = conn.urlopen(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/connectionpool.py", line 845, in urlopen
worker-0 >>     retries = retries.increment(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/urllib3/util/retry.py", line 515, in increment
worker-0 >>     raise MaxRetryError(_pool, url, reason) from reason  # type: ignore[arg-type]
worker-0 >> urllib3.exceptions.MaxRetryError: HTTPConnectionPool(host='127.0.0.1', port=8265): Max retries exceeded with url: /api/version (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7fc7937321d0>: Failed to establish a new connection: [Errno 111] Connection refused'))
worker-0 >> During handling of the above exception, another exception occurred:
worker-0 >> Traceback (most recent call last):
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 262, in _check_connection_and_version_with_url
worker-0 >>     r = self._do_request("GET", url)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 303, in _do_request
worker-0 >>     return requests.request(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/requests/api.py", line 59, in request
worker-0 >>     return session.request(method=method, url=url, **kwargs)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/requests/sessions.py", line 589, in request
worker-0 >>     resp = self.send(prep, **send_kwargs)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/requests/sessions.py", line 703, in send
worker-0 >>     r = adapter.send(request, **kwargs)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/requests/adapters.py", line 519, in send
worker-0 >>     raise ConnectionError(e, request=request)
worker-0 >> requests.exceptions.ConnectionError: HTTPConnectionPool(host='127.0.0.1', port=8265): Max retries exceeded with url: /api/version (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7fc7937321d0>: Failed to establish a new connection: [Errno 111] Connection refused'))
worker-0 >> During handling of the above exception, another exception occurred:
worker-0 >> Traceback (most recent call last):
worker-0 >>   File "/opt/conda/bin/ray", line 8, in <module>
worker-0 >>     sys.exit(main())
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/scripts/scripts.py", line 2612, in main
worker-0 >>     return cli()
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1157, in __call__
worker-0 >>     return self.main(*args, **kwargs)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1078, in main
worker-0 >>     rv = self.invoke(ctx)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1688, in invoke
worker-0 >>     return _process_result(sub_ctx.command.invoke(sub_ctx))
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1688, in invoke
worker-0 >>     return _process_result(sub_ctx.command.invoke(sub_ctx))
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1434, in invoke
worker-0 >>     return ctx.invoke(self.callback, **ctx.params)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 783, in invoke
worker-0 >>     return __callback(*args, **kwargs)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/cli_utils.py", line 54, in wrapper
worker-0 >>     return func(*args, **kwargs)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/autoscaler/_private/cli_logger.py", line 856, in wrapper
worker-0 >>     return f(*args, **kwargs)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/cli.py", line 264, in submit
worker-0 >>     client = _get_sdk_client(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/cli.py", line 29, in _get_sdk_client
worker-0 >>     client = JobSubmissionClient(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/sdk.py", line 109, in __init__
worker-0 >>     self._check_connection_and_version(
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 248, in _check_connection_and_version
worker-0 >>     self._check_connection_and_version_with_url(min_version, version_error_message)
worker-0 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 278, in _check_connection_and_version_with_url
worker-0 >>     raise ConnectionError(
worker-0 >> ConnectionError: Failed to connect to Ray at address: http://127.0.0.1:8265.
worker-1 >> 2024-08-30 07:28:01,887	INFO dashboard_sdk.py:338 -- Uploading package gcs://_ray_pkg_4e296bf30bb3da59.zip.
worker-1 >> 2024-08-30 07:28:01,888	INFO packaging.py:530 -- Creating a file package for local directory '/vepfs/DI/user/zhaoyue/openRLHF/'.
worker-1 >> 2024-08-30 07:28:01,797	INFO cli.py:36 -- Job submission server address: http://127.0.0.1:8265
worker-1 >> Traceback (most recent call last):
worker-1 >>   File "/opt/conda/bin/ray", line 8, in <module>
worker-1 >>     sys.exit(main())
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/ray/scripts/scripts.py", line 2612, in main
worker-1 >>     return cli()
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1157, in __call__
worker-1 >>     return self.main(*args, **kwargs)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1078, in main
worker-1 >>     rv = self.invoke(ctx)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1688, in invoke
worker-1 >>     return _process_result(sub_ctx.command.invoke(sub_ctx))
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1688, in invoke
worker-1 >>     return _process_result(sub_ctx.command.invoke(sub_ctx))
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 1434, in invoke
worker-1 >>     return ctx.invoke(self.callback, **ctx.params)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/click/core.py", line 783, in invoke
worker-1 >>     return __callback(*args, **kwargs)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/cli_utils.py", line 54, in wrapper
worker-1 >>     return func(*args, **kwargs)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/ray/autoscaler/_private/cli_logger.py", line 856, in wrapper
worker-1 >>     return f(*args, **kwargs)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/cli.py", line 273, in submit
worker-1 >>     job_id = client.submit_job(
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/sdk.py", line 254, in submit_job
worker-1 >>     self._raise_error(r)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/dashboard_sdk.py", line 283, in _raise_error
worker-1 >>     raise RuntimeError(
worker-1 >> RuntimeError: Request failed with status code 500: Traceback (most recent call last):
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/job_head.py", line 287, in submit_job
worker-1 >>     resp = await job_agent_client.submit_job_internal(submit_request)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/ray/dashboard/modules/job/job_head.py", line 73, in submit_job_internal
worker-1 >>     async with self._session.post(
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/aiohttp/client.py", line 1194, in __aenter__
worker-1 >>     self._resp = await self._coro
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/aiohttp/client.py", line 605, in _request
worker-1 >>     await resp.start(conn)
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/aiohttp/client_reqrep.py", line 966, in start
worker-1 >>     message, payload = await protocol.read()  # type: ignore[union-attr]
worker-1 >>   File "/opt/conda/lib/python3.10/site-packages/aiohttp/streams.py", line 622, in read
worker-1 >>     await self._waiter
worker-1 >> aiohttp.client_exceptions.ServerDisconnectedError: Server disconnected
worker-1 >> .
