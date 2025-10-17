PS C:\dev\Developer\sk-sandbox-backend> py -m pip install -r .\requirements.txt
Looking in indexes: https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple
User for tools.rbspeople.com: mhL48uC-
Password:
Collecting annotated-types==0.6.0 (from -r .\requirements.txt (line 1))
  Downloading https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/annotated-types/0.6.0/annotated_types-0.6.0-py3-none-any.whl (12 kB)
Collecting anyio==4.3.0 (from -r .\requirements.txt (line 2))
  Downloading https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/anyio/4.3.0/anyio-4.3.0-py3-none-any.whl (85 kB)
Collecting asn1crypto==1.5.1 (from -r .\requirements.txt (line 3))
  Downloading https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/asn1crypto/1.5.1/asn1crypto-1.5.1-py2.py3-none-any.whl (105 kB)
Collecting certifi==2024.2.2 (from -r .\requirements.txt (line 4))
  Downloading https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/certifi/2024.2.2/certifi-2024.2.2-py3-none-any.whl (163 kB)
Collecting cffi==1.16.0 (from -r .\requirements.txt (line 5))
  Downloading https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/cffi/1.16.0/cffi-1.16.0.tar.gz (512 kB)
  Installing build dependencies ... error
  error: subprocess-exited-with-error

  × pip subprocess to install build dependencies did not run successfully.
  │ exit code: 2
  ╰─> [86 lines of output]
      Looking in indexes: https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple
      User for tools.rbspeople.com: ERROR: Exception:
      Traceback (most recent call last):
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\cli\base_command.py", line 107, in _run_wrapper
          status = _inner_run()
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\cli\base_command.py", line 98, in _inner_run
          return self.run(options, args)
                 ~~~~~~~~^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\cli\req_command.py", line 71, in wrapper
          return func(self, options, args)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\commands\install.py", line 393, in run
          requirement_set = resolver.resolve(
              reqs, check_supported_wheels=not options.target_dir
          )
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\resolution\resolvelib\resolver.py", line 98, in resolve
          result = self._result = resolver.resolve(
                                  ~~~~~~~~~~~~~~~~^
              collected.requirements, max_rounds=limit_how_complex_resolution_can_be
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
          )
          ^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\resolvelib\resolvers\resolution.py", line 596, in resolve
          state = resolution.resolve(requirements, max_rounds=max_rounds)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\resolvelib\resolvers\resolution.py", line 429, in resolve
          self._add_to_criteria(self.state.criteria, r, parent=None)
          ~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\resolvelib\resolvers\resolution.py", line 150, in _add_to_criteria
          if not criterion.candidates:
                 ^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\resolvelib\structs.py", line 194, in __bool__
          return bool(self._sequence)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\resolution\resolvelib\found_candidates.py", line 165, in __bool__
          self._bool = any(self)
                       ~~~^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\resolution\resolvelib\found_candidates.py", line 149, in <genexpr>
          return (c for c in iterator if id(c) not in self._incompatible_ids)
                             ^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\resolution\resolvelib\found_candidates.py", line 35, in _iter_built
          for version, func in infos:
                               ^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\resolution\resolvelib\factory.py", line 300, in iter_index_candidate_infos
          result = self._finder.find_best_candidate(
              project_name=name,
              specifier=specifier,
              hashes=hashes,
          )
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\index\package_finder.py", line 915, in find_best_candidate
          candidates = self.find_all_candidates(project_name)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\index\package_finder.py", line 852, in find_all_candidates
          page_candidates = list(page_candidates_it)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\index\sources.py", line 196, in page_candidates
          yield from self._candidates_from_page(self._link)
                     ~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\index\package_finder.py", line 810, in process_project_url
          index_response = self._link_collector.fetch_response(project_url)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\index\collector.py", line 443, in fetch_response
          return _get_index_content(location, session=self.session)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\index\collector.py", line 347, in _get_index_content
          resp = _get_simple_response(url, session=session)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\index\collector.py", line 126, in _get_simple_response
          resp = session.get(
              url,
          ...<22 lines>...
              },
          )
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\requests\sessions.py", line 602, in get
          return self.request("GET", url, **kwargs)
                 ~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\network\session.py", line 528, in request
          return super().request(method, url, *args, **kwargs)
                 ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\requests\sessions.py", line 589, in request
          resp = self.send(prep, **send_kwargs)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\requests\sessions.py", line 710, in send
          r = dispatch_hook("response", hooks, r, **kwargs)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\requests\hooks.py", line 30, in dispatch_hook
          _hook_data = hook(hook_data, **kwargs)
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\network\auth.py", line 503, in handle_401
          username, password, save = self._prompt_for_password(parsed.netloc)
                                     ~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\network\auth.py", line 458, in _prompt_for_password
          username = ask_input(f"User for {netloc}: ") if self.prompting else None
                     ~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_internal\utils\misc.py", line 235, in ask_input
          return input(message)
      EOFError: EOF when reading a line
      [end of output]

  note: This error originates from a subprocess, and is likely not a problem with pip.
error: subprocess-exited-with-error

× pip subprocess to install build dependencies did not run successfully.
│ exit code: 2
╰─> See above for output.

note: This error originates from a subprocess, and is likely not a problem with pip.
PS C:\dev\Developer\sk-sandbox-backend>
