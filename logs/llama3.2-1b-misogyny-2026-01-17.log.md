```text
2026-01-17 15:54:23,690  INFO  invoked
2026-01-17 15:54:23,691  DEBUG  Loading configs from: /home/peter216/git/ossdev/garak/garak/resources/garak.core.yaml
2026-01-17 15:54:23,695  DEBUG  args - raw argument string received: ['-t', 'ollama', '-n', 'llama3.2:1b', '-p', 'lmrc.Misogyny', '-d', 'lmrc.Misogyny', '--report_prefix', 'llama3.2:1b.misogyny.2026-01-17']
2026-01-17 15:54:23,696  DEBUG  args - full argparse: Namespace(verbose=0, report_prefix='llama3.2:1b.misogyny.2026-01-17', narrow_output=False, parallel_requests=False, parallel_attempts=False, skip_unknown=False, seed=None, deprefix=True, eval_threshold=0.5, generations=5, config=None, target_type='ollama', target_name='llama3.2:1b', probes='lmrc.Misogyny', probe_tags=None, detectors='lmrc.Misogyny', extended_detectors=False, buffs=None, buff_option_file=None, buff_options=None, detector_option_file=None, detector_options=None, generator_option_file=None, generator_options=None, harness_option_file=None, harness_options=None, probe_option_file=None, probe_options=None, taxonomy=None, plugin_info=None, list_probes=False, list_detectors=False, list_generators=False, list_buffs=False, list_config=False, version=False, report=None, interactive=False, generate_autodan=False, fix=False)
2026-01-17 15:54:23,870  DEBUG  no site config found at: /home/peter216/.config/garak/garak.site.json, /home/peter216/.config/garak/garak.site.yaml, or /home/peter216/.config/garak/garak.site.yml
2026-01-17 15:54:23,870  DEBUG  Loading configs from: /home/peter216/git/ossdev/garak/garak/resources/garak.core.yaml
2026-01-17 15:54:23,872  DEBUG  args - cli_args&commands stored: Namespace(target_type='ollama', target_name='llama3.2:1b', probes='lmrc.Misogyny', detectors='lmrc.Misogyny', report_prefix='llama3.2:1b.misogyny.2026-01-17', verbose=0, list_detectors=False, list_probes=False, list_generators=False, list_buffs=False, list_config=False, plugin_info=None, interactive=False, report=None, version=False, fix=False)
2026-01-17 15:54:23,872  DEBUG  non-config params: [('probes', 'lmrc.Misogyny'), ('detectors', 'lmrc.Misogyny'), ('list_detectors', False), ('list_probes', False), ('list_generators', False), ('list_buffs', False), ('list_config', False), ('plugin_info', None), ('report', None), ('version', False), ('fix', False)]
2026-01-17 15:54:23,886  INFO  generator init: <garak.generators.ollama.OllamaGeneratorChat object at 0x774f1085c830>
2026-01-17 15:54:24,042  INFO  run started at 2026-01-17T15:54:23.686297
2026-01-17 15:54:24,043  DEBUG  relative report dir provided
2026-01-17 15:54:24,043  INFO  reporting to /home/peter216/.local/share/garak/garak_runs/llama3.2:1b.misogyny.2026-01-17.report.jsonl
2026-01-17 15:54:24,044  INFO  service import: garak.langservice
2026-01-17 15:54:25,377  INFO  harness init: <garak.harnesses.pxd.PxD object at 0x774f0f99f140>
2026-01-17 15:54:25,377  INFO  probe queue: probes.lmrc.Misogyny
2026-01-17 15:54:25,378  INFO  probe init: <garak.probes.lmrc.Misogyny object at 0x774ed247f320>
2026-01-17 15:54:25,378  DEBUG  langauge provision service: en,en
2026-01-17 15:54:28,656  INFO  detector init: <garak.detectors.lmrc.Misogyny object at 0x774ed247d970>
2026-01-17 15:54:28,656  DEBUG  Using cpu, based on torch environment evaluation
2026-01-17 15:54:28,658  DEBUG  Starting new HTTPS connection (1): huggingface.co:443
2026-01-17 15:54:32,455  DEBUG  https://huggingface.co:443 "HEAD /MilaNLProc/bert-base-uncased-ear-misogyny/resolve/main/config.json HTTP/1.1" 307 0
2026-01-17 15:54:32,479  DEBUG  https://huggingface.co:443 "HEAD /api/resolve-cache/models/MilaNLProc/bert-base-uncased-ear-misogyny/52fa40997a8ffc5eb00d3225eb33c5e300f75178/config.json HTTP/1.1" 200 0
2026-01-17 15:54:32,556  DEBUG  https://huggingface.co:443 "HEAD /MilaNLProc/bert-base-uncased-ear-misogyny/resolve/main/model.safetensors HTTP/1.1" 404 0
2026-01-17 15:54:32,563  DEBUG  Starting new HTTPS connection (1): huggingface.co:443
2026-01-17 15:54:32,671  DEBUG  https://huggingface.co:443 "GET /api/models/MilaNLProc/bert-base-uncased-ear-misogyny HTTP/1.1" 200 1725
2026-01-17 15:54:32,837  DEBUG  https://huggingface.co:443 "GET /api/models/MilaNLProc/bert-base-uncased-ear-misogyny/commits/main HTTP/1.1" 200 2390
2026-01-17 15:54:32,873  DEBUG  https://huggingface.co:443 "GET /api/models/MilaNLProc/bert-base-uncased-ear-misogyny/discussions?p=0 HTTP/1.1" 200 784
2026-01-17 15:54:33,028  DEBUG  https://huggingface.co:443 "HEAD /MilaNLProc/bert-base-uncased-ear-misogyny/resolve/main/tokenizer_config.json HTTP/1.1" 307 0
2026-01-17 15:54:33,052  DEBUG  https://huggingface.co:443 "HEAD /api/resolve-cache/models/MilaNLProc/bert-base-uncased-ear-misogyny/52fa40997a8ffc5eb00d3225eb33c5e300f75178/tokenizer_config.json HTTP/1.1" 200 0
2026-01-17 15:54:33,104  DEBUG  https://huggingface.co:443 "GET /api/models/MilaNLProc/bert-base-uncased-ear-misogyny/tree/main/additional_chat_templates?recursive=False&expand=False HTTP/1.1" 404 64
2026-01-17 15:54:33,145  DEBUG  https://huggingface.co:443 "GET /api/models/MilaNLProc/bert-base-uncased-ear-misogyny/commits/refs%2Fpr%2F1 HTTP/1.1" 200 3355
2026-01-17 15:54:33,147  DEBUG  harness: probe start for garak.probes.lmrc.Misogyny
2026-01-17 15:54:33,147  DEBUG  probe execute: <garak.probes.lmrc.Misogyny object at 0x774ed247f320>
2026-01-17 15:54:33,151  DEBUG  connect_tcp.started host='127.0.0.1' port=11434 local_address=None timeout=30 socket_options=None
2026-01-17 15:54:33,151  DEBUG  connect_tcp.complete return_value=<httpcore._backends.sync.SyncStream object at 0x774dbaeef740>
2026-01-17 15:54:33,151  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:54:33,151  DEBUG  send_request_headers.complete
2026-01-17 15:54:33,152  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:54:33,152  DEBUG  send_request_body.complete
2026-01-17 15:54:33,152  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:54:33,193  DEBUG  https://huggingface.co:443 "HEAD /MilaNLProc/bert-base-uncased-ear-misogyny/resolve/refs%2Fpr%2F1/model.safetensors.index.json HTTP/1.1" 404 0
2026-01-17 15:54:33,223  DEBUG  https://huggingface.co:443 "HEAD /MilaNLProc/bert-base-uncased-ear-misogyny/resolve/refs%2Fpr%2F1/model.safetensors HTTP/1.1" 302 0
2026-01-17 15:55:03,200  DEBUG  receive_response_headers.failed exception=ReadTimeout(TimeoutError('timed out'))
2026-01-17 15:55:03,200  DEBUG  response_closed.started
2026-01-17 15:55:03,200  DEBUG  response_closed.complete
2026-01-17 15:55:03,204  INFO  Backing off _call_model(...) for 0.3s (garak.exception.GeneratorBackoffTrigger)
2026-01-17 15:55:03,475  DEBUG  connect_tcp.started host='127.0.0.1' port=11434 local_address=None timeout=30 socket_options=None
2026-01-17 15:55:03,476  DEBUG  connect_tcp.complete return_value=<httpcore._backends.sync.SyncStream object at 0x774dba352150>
2026-01-17 15:55:03,476  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:55:03,476  DEBUG  send_request_headers.complete
2026-01-17 15:55:03,476  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:55:03,476  DEBUG  send_request_body.complete
2026-01-17 15:55:03,476  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:55:24,734  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:55:24 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 15:55:24,735  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:55:24,735  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:55:24,735  DEBUG  receive_response_body.complete
2026-01-17 15:55:24,735  DEBUG  response_closed.started
2026-01-17 15:55:24,735  DEBUG  response_closed.complete
2026-01-17 15:55:24,736  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:55:24,736  DEBUG  send_request_headers.complete
2026-01-17 15:55:24,736  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:55:24,736  DEBUG  send_request_body.complete
2026-01-17 15:55:24,736  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:55:37,186  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:55:37 GMT'), (b'Content-Length', b'1391')])
2026-01-17 15:55:37,186  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:55:37,186  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:55:37,186  DEBUG  receive_response_body.complete
2026-01-17 15:55:37,186  DEBUG  response_closed.started
2026-01-17 15:55:37,186  DEBUG  response_closed.complete
2026-01-17 15:55:37,187  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:55:37,187  DEBUG  send_request_headers.complete
2026-01-17 15:55:37,187  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:55:37,187  DEBUG  send_request_body.complete
2026-01-17 15:55:37,187  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:55:57,950  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:55:57 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 15:55:57,951  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:55:57,951  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:55:57,951  DEBUG  receive_response_body.complete
2026-01-17 15:55:57,951  DEBUG  response_closed.started
2026-01-17 15:55:57,951  DEBUG  response_closed.complete
2026-01-17 15:55:57,951  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:55:57,952  DEBUG  send_request_headers.complete
2026-01-17 15:55:57,952  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:55:57,952  DEBUG  send_request_body.complete
2026-01-17 15:55:57,952  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:56:16,766  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:56:16 GMT'), (b'Content-Length', b'1861')])
2026-01-17 15:56:16,766  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:56:16,766  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:56:16,766  DEBUG  receive_response_body.complete
2026-01-17 15:56:16,766  DEBUG  response_closed.started
2026-01-17 15:56:16,766  DEBUG  response_closed.complete
2026-01-17 15:56:16,767  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:56:16,767  DEBUG  send_request_headers.complete
2026-01-17 15:56:16,767  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:56:16,767  DEBUG  send_request_body.complete
2026-01-17 15:56:16,767  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:56:36,692  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:56:36 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 15:56:36,692  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:56:36,692  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:56:36,692  DEBUG  receive_response_body.complete
2026-01-17 15:56:36,692  DEBUG  response_closed.started
2026-01-17 15:56:36,692  DEBUG  response_closed.complete
2026-01-17 15:56:36,811  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:56:36,811  DEBUG  send_request_headers.complete
2026-01-17 15:56:36,811  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:56:36,811  DEBUG  send_request_body.complete
2026-01-17 15:56:36,811  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:57:05,345  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:57:05 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 15:57:05,346  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:57:05,346  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:57:05,346  DEBUG  receive_response_body.complete
2026-01-17 15:57:05,346  DEBUG  response_closed.started
2026-01-17 15:57:05,346  DEBUG  response_closed.complete
2026-01-17 15:57:05,346  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:57:05,346  DEBUG  send_request_headers.complete
2026-01-17 15:57:05,347  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:57:05,347  DEBUG  send_request_body.complete
2026-01-17 15:57:05,347  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:57:33,051  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:57:33 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 15:57:33,051  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:57:33,051  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:57:33,051  DEBUG  receive_response_body.complete
2026-01-17 15:57:33,051  DEBUG  response_closed.started
2026-01-17 15:57:33,051  DEBUG  response_closed.complete
2026-01-17 15:57:33,052  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:57:33,052  DEBUG  send_request_headers.complete
2026-01-17 15:57:33,052  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:57:33,052  DEBUG  send_request_body.complete
2026-01-17 15:57:33,052  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:57:39,594  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:57:39 GMT'), (b'Content-Length', b'814')])
2026-01-17 15:57:39,594  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:57:39,594  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:57:39,594  DEBUG  receive_response_body.complete
2026-01-17 15:57:39,594  DEBUG  response_closed.started
2026-01-17 15:57:39,594  DEBUG  response_closed.complete
2026-01-17 15:57:39,595  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:57:39,595  DEBUG  send_request_headers.complete
2026-01-17 15:57:39,595  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:57:39,595  DEBUG  send_request_body.complete
2026-01-17 15:57:39,595  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:58:06,361  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:58:06 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 15:58:06,361  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:58:06,361  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:58:06,361  DEBUG  receive_response_body.complete
2026-01-17 15:58:06,361  DEBUG  response_closed.started
2026-01-17 15:58:06,361  DEBUG  response_closed.complete
2026-01-17 15:58:06,362  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:58:06,362  DEBUG  send_request_headers.complete
2026-01-17 15:58:06,362  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:58:06,362  DEBUG  send_request_body.complete
2026-01-17 15:58:06,362  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:58:36,392  DEBUG  receive_response_headers.failed exception=ReadTimeout(TimeoutError('timed out'))
2026-01-17 15:58:36,392  DEBUG  response_closed.started
2026-01-17 15:58:36,392  DEBUG  response_closed.complete
2026-01-17 15:58:36,394  INFO  Backing off _call_model(...) for 0.1s (garak.exception.GeneratorBackoffTrigger)
2026-01-17 15:58:36,540  DEBUG  connect_tcp.started host='127.0.0.1' port=11434 local_address=None timeout=30 socket_options=None
2026-01-17 15:58:36,540  DEBUG  connect_tcp.complete return_value=<httpcore._backends.sync.SyncStream object at 0x774dba351970>
2026-01-17 15:58:36,540  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:58:36,541  DEBUG  send_request_headers.complete
2026-01-17 15:58:36,541  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:58:36,541  DEBUG  send_request_body.complete
2026-01-17 15:58:36,541  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:59:01,195  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:59:01 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 15:59:01,195  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:59:01,195  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:59:01,195  DEBUG  receive_response_body.complete
2026-01-17 15:59:01,195  DEBUG  response_closed.started
2026-01-17 15:59:01,195  DEBUG  response_closed.complete
2026-01-17 15:59:01,197  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:59:01,197  DEBUG  send_request_headers.complete
2026-01-17 15:59:01,197  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:59:01,197  DEBUG  send_request_body.complete
2026-01-17 15:59:01,197  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:59:14,150  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:59:14 GMT'), (b'Content-Length', b'1400')])
2026-01-17 15:59:14,151  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:59:14,151  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:59:14,151  DEBUG  receive_response_body.complete
2026-01-17 15:59:14,151  DEBUG  response_closed.started
2026-01-17 15:59:14,151  DEBUG  response_closed.complete
2026-01-17 15:59:14,152  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:59:14,152  DEBUG  send_request_headers.complete
2026-01-17 15:59:14,152  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:59:14,152  DEBUG  send_request_body.complete
2026-01-17 15:59:14,152  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:59:35,820  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:59:35 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 15:59:35,820  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:59:35,820  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:59:35,820  DEBUG  receive_response_body.complete
2026-01-17 15:59:35,821  DEBUG  response_closed.started
2026-01-17 15:59:35,821  DEBUG  response_closed.complete
2026-01-17 15:59:35,821  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:59:35,821  DEBUG  send_request_headers.complete
2026-01-17 15:59:35,821  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:59:35,821  DEBUG  send_request_body.complete
2026-01-17 15:59:35,821  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 15:59:52,892  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 20:59:52 GMT'), (b'Content-Length', b'1720')])
2026-01-17 15:59:52,892  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 15:59:52,892  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 15:59:52,892  DEBUG  receive_response_body.complete
2026-01-17 15:59:52,892  DEBUG  response_closed.started
2026-01-17 15:59:52,892  DEBUG  response_closed.complete
2026-01-17 15:59:52,893  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 15:59:52,893  DEBUG  send_request_headers.complete
2026-01-17 15:59:52,893  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 15:59:52,893  DEBUG  send_request_body.complete
2026-01-17 15:59:52,893  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:00:15,847  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:00:15 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 16:00:15,848  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:00:15,848  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:00:15,848  DEBUG  receive_response_body.complete
2026-01-17 16:00:15,848  DEBUG  response_closed.started
2026-01-17 16:00:15,848  DEBUG  response_closed.complete
2026-01-17 16:00:15,848  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:00:15,849  DEBUG  send_request_headers.complete
2026-01-17 16:00:15,849  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:00:15,849  DEBUG  send_request_body.complete
2026-01-17 16:00:15,849  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:00:42,919  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:00:42 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 16:00:42,920  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:00:42,920  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:00:42,920  DEBUG  receive_response_body.complete
2026-01-17 16:00:42,920  DEBUG  response_closed.started
2026-01-17 16:00:42,920  DEBUG  response_closed.complete
2026-01-17 16:00:42,921  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:00:42,922  DEBUG  send_request_headers.complete
2026-01-17 16:00:42,922  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:00:42,922  DEBUG  send_request_body.complete
2026-01-17 16:00:42,922  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:00:44,668  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:00:44 GMT'), (b'Content-Length', b'431')])
2026-01-17 16:00:44,669  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:00:44,669  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:00:44,669  DEBUG  receive_response_body.complete
2026-01-17 16:00:44,669  DEBUG  response_closed.started
2026-01-17 16:00:44,669  DEBUG  response_closed.complete
2026-01-17 16:00:44,669  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:00:44,670  DEBUG  send_request_headers.complete
2026-01-17 16:00:44,670  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:00:44,670  DEBUG  send_request_body.complete
2026-01-17 16:00:44,670  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:00:46,833  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:00:46 GMT'), (b'Content-Length', b'467')])
2026-01-17 16:00:46,833  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:00:46,833  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:00:46,833  DEBUG  receive_response_body.complete
2026-01-17 16:00:46,833  DEBUG  response_closed.started
2026-01-17 16:00:46,833  DEBUG  response_closed.complete
2026-01-17 16:00:46,834  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:00:46,834  DEBUG  send_request_headers.complete
2026-01-17 16:00:46,834  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:00:46,834  DEBUG  send_request_body.complete
2026-01-17 16:00:46,834  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:00:48,758  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:00:48 GMT'), (b'Content-Length', b'457')])
2026-01-17 16:00:48,758  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:00:48,758  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:00:48,758  DEBUG  receive_response_body.complete
2026-01-17 16:00:48,758  DEBUG  response_closed.started
2026-01-17 16:00:48,758  DEBUG  response_closed.complete
2026-01-17 16:00:48,758  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:00:48,759  DEBUG  send_request_headers.complete
2026-01-17 16:00:48,759  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:00:48,759  DEBUG  send_request_body.complete
2026-01-17 16:00:48,759  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:00:51,308  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:00:51 GMT'), (b'Content-Length', b'514')])
2026-01-17 16:00:51,308  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:00:51,309  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:00:51,309  DEBUG  receive_response_body.complete
2026-01-17 16:00:51,309  DEBUG  response_closed.started
2026-01-17 16:00:51,309  DEBUG  response_closed.complete
2026-01-17 16:00:51,309  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:00:51,309  DEBUG  send_request_headers.complete
2026-01-17 16:00:51,309  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:00:51,309  DEBUG  send_request_body.complete
2026-01-17 16:00:51,309  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:00:59,809  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:00:59 GMT'), (b'Content-Length', b'985')])
2026-01-17 16:00:59,809  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:00:59,809  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:00:59,809  DEBUG  receive_response_body.complete
2026-01-17 16:00:59,809  DEBUG  response_closed.started
2026-01-17 16:00:59,809  DEBUG  response_closed.complete
2026-01-17 16:00:59,811  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:00:59,811  DEBUG  send_request_headers.complete
2026-01-17 16:00:59,811  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:00:59,811  DEBUG  send_request_body.complete
2026-01-17 16:00:59,811  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:01:18,906  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:01:18 GMT'), (b'Content-Length', b'2034')])
2026-01-17 16:01:18,906  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:01:18,906  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:01:18,906  DEBUG  receive_response_body.complete
2026-01-17 16:01:18,906  DEBUG  response_closed.started
2026-01-17 16:01:18,906  DEBUG  response_closed.complete
2026-01-17 16:01:18,907  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:01:18,907  DEBUG  send_request_headers.complete
2026-01-17 16:01:18,907  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:01:18,907  DEBUG  send_request_body.complete
2026-01-17 16:01:18,907  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:01:37,522  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:01:37 GMT'), (b'Content-Length', b'1985')])
2026-01-17 16:01:37,522  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:01:37,522  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:01:37,522  DEBUG  receive_response_body.complete
2026-01-17 16:01:37,522  DEBUG  response_closed.started
2026-01-17 16:01:37,522  DEBUG  response_closed.complete
2026-01-17 16:01:37,523  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:01:37,523  DEBUG  send_request_headers.complete
2026-01-17 16:01:37,523  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:01:37,523  DEBUG  send_request_body.complete
2026-01-17 16:01:37,523  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:01:54,934  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:01:54 GMT'), (b'Content-Length', b'1849')])
2026-01-17 16:01:54,934  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:01:54,934  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:01:54,934  DEBUG  receive_response_body.complete
2026-01-17 16:01:54,934  DEBUG  response_closed.started
2026-01-17 16:01:54,934  DEBUG  response_closed.complete
2026-01-17 16:01:54,935  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:01:54,935  DEBUG  send_request_headers.complete
2026-01-17 16:01:54,935  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:01:54,935  DEBUG  send_request_body.complete
2026-01-17 16:01:54,935  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:02:13,003  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:02:13 GMT'), (b'Content-Length', b'1953')])
2026-01-17 16:02:13,003  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:02:13,003  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:02:13,003  DEBUG  receive_response_body.complete
2026-01-17 16:02:13,003  DEBUG  response_closed.started
2026-01-17 16:02:13,003  DEBUG  response_closed.complete
2026-01-17 16:02:13,004  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:02:13,004  DEBUG  send_request_headers.complete
2026-01-17 16:02:13,004  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:02:13,004  DEBUG  send_request_body.complete
2026-01-17 16:02:13,004  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:02:28,014  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:02:28 GMT'), (b'Content-Length', b'1701')])
2026-01-17 16:02:28,014  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:02:28,014  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:02:28,014  DEBUG  receive_response_body.complete
2026-01-17 16:02:28,014  DEBUG  response_closed.started
2026-01-17 16:02:28,014  DEBUG  response_closed.complete
2026-01-17 16:02:28,016  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:02:28,016  DEBUG  send_request_headers.complete
2026-01-17 16:02:28,016  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:02:28,016  DEBUG  send_request_body.complete
2026-01-17 16:02:28,016  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:02:31,517  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:02:31 GMT'), (b'Content-Length', b'567')])
2026-01-17 16:02:31,518  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:02:31,518  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:02:31,518  DEBUG  receive_response_body.complete
2026-01-17 16:02:31,518  DEBUG  response_closed.started
2026-01-17 16:02:31,518  DEBUG  response_closed.complete
2026-01-17 16:02:31,519  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:02:31,519  DEBUG  send_request_headers.complete
2026-01-17 16:02:31,519  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:02:31,519  DEBUG  send_request_body.complete
2026-01-17 16:02:31,519  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:02:34,157  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:02:34 GMT'), (b'Content-Length', b'497')])
2026-01-17 16:02:34,157  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:02:34,157  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:02:34,157  DEBUG  receive_response_body.complete
2026-01-17 16:02:34,157  DEBUG  response_closed.started
2026-01-17 16:02:34,157  DEBUG  response_closed.complete
2026-01-17 16:02:34,158  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:02:34,158  DEBUG  send_request_headers.complete
2026-01-17 16:02:34,158  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:02:34,158  DEBUG  send_request_body.complete
2026-01-17 16:02:34,158  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:02:37,820  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:02:37 GMT'), (b'Content-Length', b'558')])
2026-01-17 16:02:37,820  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:02:37,820  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:02:37,820  DEBUG  receive_response_body.complete
2026-01-17 16:02:37,820  DEBUG  response_closed.started
2026-01-17 16:02:37,820  DEBUG  response_closed.complete
2026-01-17 16:02:37,821  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:02:37,821  DEBUG  send_request_headers.complete
2026-01-17 16:02:37,821  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:02:37,821  DEBUG  send_request_body.complete
2026-01-17 16:02:37,821  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:02:41,414  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:02:41 GMT'), (b'Content-Length', b'545')])
2026-01-17 16:02:41,414  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:02:41,414  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:02:41,414  DEBUG  receive_response_body.complete
2026-01-17 16:02:41,414  DEBUG  response_closed.started
2026-01-17 16:02:41,414  DEBUG  response_closed.complete
2026-01-17 16:02:41,415  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:02:41,415  DEBUG  send_request_headers.complete
2026-01-17 16:02:41,415  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:02:41,415  DEBUG  send_request_body.complete
2026-01-17 16:02:41,415  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:02:44,813  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:02:44 GMT'), (b'Content-Length', b'539')])
2026-01-17 16:02:44,813  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:02:44,814  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:02:44,814  DEBUG  receive_response_body.complete
2026-01-17 16:02:44,814  DEBUG  response_closed.started
2026-01-17 16:02:44,814  DEBUG  response_closed.complete
2026-01-17 16:02:44,815  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:02:44,815  DEBUG  send_request_headers.complete
2026-01-17 16:02:44,815  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:02:44,816  DEBUG  send_request_body.complete
2026-01-17 16:02:44,816  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:03:03,046  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:03:03 GMT'), (b'Content-Length', b'1687')])
2026-01-17 16:03:03,046  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:03:03,047  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:03:03,047  DEBUG  receive_response_body.complete
2026-01-17 16:03:03,047  DEBUG  response_closed.started
2026-01-17 16:03:03,047  DEBUG  response_closed.complete
2026-01-17 16:03:03,047  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:03:03,047  DEBUG  send_request_headers.complete
2026-01-17 16:03:03,047  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:03:03,048  DEBUG  send_request_body.complete
2026-01-17 16:03:03,048  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:03:08,402  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:03:08 GMT'), (b'Content-Length', b'759')])
2026-01-17 16:03:08,402  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:03:08,402  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:03:08,402  DEBUG  receive_response_body.complete
2026-01-17 16:03:08,402  DEBUG  response_closed.started
2026-01-17 16:03:08,402  DEBUG  response_closed.complete
2026-01-17 16:03:08,403  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:03:08,403  DEBUG  send_request_headers.complete
2026-01-17 16:03:08,403  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:03:08,403  DEBUG  send_request_body.complete
2026-01-17 16:03:08,403  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:03:13,773  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:03:13 GMT'), (b'Content-Length', b'761')])
2026-01-17 16:03:13,774  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:03:13,774  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:03:13,774  DEBUG  receive_response_body.complete
2026-01-17 16:03:13,774  DEBUG  response_closed.started
2026-01-17 16:03:13,774  DEBUG  response_closed.complete
2026-01-17 16:03:13,775  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:03:13,775  DEBUG  send_request_headers.complete
2026-01-17 16:03:13,775  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:03:13,775  DEBUG  send_request_body.complete
2026-01-17 16:03:13,775  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:03:34,692  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:03:34 GMT'), (b'Transfer-Encoding', b'chunked')])
2026-01-17 16:03:34,692  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:03:34,692  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:03:34,692  DEBUG  receive_response_body.complete
2026-01-17 16:03:34,692  DEBUG  response_closed.started
2026-01-17 16:03:34,692  DEBUG  response_closed.complete
2026-01-17 16:03:34,693  DEBUG  send_request_headers.started request=<Request [b'POST']>
2026-01-17 16:03:34,693  DEBUG  send_request_headers.complete
2026-01-17 16:03:34,693  DEBUG  send_request_body.started request=<Request [b'POST']>
2026-01-17 16:03:34,693  DEBUG  send_request_body.complete
2026-01-17 16:03:34,693  DEBUG  receive_response_headers.started request=<Request [b'POST']>
2026-01-17 16:03:39,243  DEBUG  receive_response_headers.complete return_value=(b'HTTP/1.1', 200, b'OK', [(b'Content-Type', b'application/json; charset=utf-8'), (b'Date', b'Sat, 17 Jan 2026 21:03:39 GMT'), (b'Content-Length', b'669')])
2026-01-17 16:03:39,243  INFO  HTTP Request: POST http://127.0.0.1:11434/api/chat "HTTP/1.1 200 OK"
2026-01-17 16:03:39,243  DEBUG  receive_response_body.started request=<Request [b'POST']>
2026-01-17 16:03:39,243  DEBUG  receive_response_body.complete
2026-01-17 16:03:39,243  DEBUG  response_closed.started
2026-01-17 16:03:39,243  DEBUG  response_closed.complete
2026-01-17 16:03:39,245  DEBUG  probe return: <garak.probes.lmrc.Misogyny object at 0x774ed247f320> with 7 attempts
2026-01-17 16:03:39,245  DEBUG  harness: run detector garak.detectors.lmrc.Misogyny
2026-01-17 16:03:46,062  DEBUG  harness: probe list iteration completed
2026-01-17 16:03:46,063  INFO  run complete, ending
2026-01-17 16:03:46,097  INFO  garak run complete in 562.38s
```
