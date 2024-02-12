➜  dockers docker logs ldap_ui 
Process SpawnProcess-1:
Traceback (most recent call last):
  File "/usr/lib/python3.11/multiprocessing/process.py", line 314, in _bootstrap
    self.run()
  File "/usr/lib/python3.11/multiprocessing/process.py", line 108, in run
    self._target(*self._args, **self._kwargs)
  File "/usr/lib/python3.11/site-packages/hypercorn/asyncio/run.py", line 186, in asyncio_worker
    app = load_application(config.application_path, config.wsgi_max_body_size)
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.11/site-packages/hypercorn/utils.py", line 110, in load_application
    module = import_module(import_name)
             ^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.11/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "<frozen importlib._bootstrap>", line 1204, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1176, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1147, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 690, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 940, in exec_module
  File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
  File "/app/app.py", line 8, in <module>
    app.config.from_object('settings')
  File "/usr/lib/python3.11/site-packages/flask/config.py", line 256, in from_object
    obj = import_string(obj)
          ^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.11/site-packages/werkzeug/utils.py", line 595, in import_string
    __import__(import_name)
  File "/app/settings.py", line 15, in <module>
    assert BASE_DN, "BASE_DN environment variable must be set"
AssertionError: BASE_DN environment variable must be set

