PS C:\dev\Developer\sk-sandbox-backend> py -m pip config list
global.cert='C:\\dev\\certs\\ca-certificates.crt'
global.index-url='https://mhL48uC-:----@tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple'
global.trusted-host='tools.rbspeople.com'
PS C:\dev\Developer\sk-sandbox-backend> py -m pip install -r .\requirements.txt
Looking in indexes: https://mhL48uC-:****@tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple
Collecting annotated-types==0.6.0 (from -r .\requirements.txt (line 1))
  Using cached https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/annotated-types/0.6.0/annotated_types-0.6.0-py3-none-any.whl (12 kB)
Collecting anyio==4.3.0 (from -r .\requirements.txt (line 2))
  Using cached https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/anyio/4.3.0/anyio-4.3.0-py3-none-any.whl (85 kB)
Collecting asn1crypto==1.5.1 (from -r .\requirements.txt (line 3))
  Using cached https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/asn1crypto/1.5.1/asn1crypto-1.5.1-py2.py3-none-any.whl (105 kB)
Collecting certifi==2024.2.2 (from -r .\requirements.txt (line 4))
  Using cached https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/certifi/2024.2.2/certifi-2024.2.2-py3-none-any.whl (163 kB)
Collecting cffi==1.16.0 (from -r .\requirements.txt (line 5))
  Using cached https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/packages/cffi/1.16.0/cffi-1.16.0.tar.gz (512 kB)
  Installing build dependencies ... done
  Getting requirements to build wheel ... error
  error: subprocess-exited-with-error

  × Getting requirements to build wheel did not run successfully.
  │ exit code: 1
  ╰─> [36 lines of output]
      Traceback (most recent call last):
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\pyproject_hooks\_in_process\_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\pyproject_hooks\_in_process\_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages\pip\_vendor\pyproject_hooks\_in_process\_in_process.py", line 143, in get_requires_for_build_wheel
          return hook(config_settings)
        File "C:\Users\dzikohn\AppData\Local\Temp\pip-build-env-p8trkzdn\overlay\Lib\site-packages\setuptools\build_meta.py", line 331, in get_requires_for_build_wheel
          return self._get_build_requires(config_settings, requirements=[])
                 ~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Temp\pip-build-env-p8trkzdn\overlay\Lib\site-packages\setuptools\build_meta.py", line 301, in _get_build_requires
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "C:\Users\dzikohn\AppData\Local\Temp\pip-build-env-p8trkzdn\overlay\Lib\site-packages\setuptools\build_meta.py", line 317, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 126, in <module>
        File "<string>", line 105, in uses_msvc
        File "C:\Users\dzikohn\AppData\Local\Temp\pip-build-env-p8trkzdn\overlay\Lib\site-packages\setuptools\_distutils\command\config.py", line 213, in try_compile
          self._compile(body, headers, include_dirs, lang)
          ~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Temp\pip-build-env-p8trkzdn\overlay\Lib\site-packages\setuptools\_distutils\command\config.py", line 129, in _compile
          self.compiler.compile([src], include_dirs=include_dirs)
          ~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "C:\Users\dzikohn\AppData\Local\Temp\pip-build-env-p8trkzdn\overlay\Lib\site-packages\setuptools\_distutils\compilers\C\msvc.py", line 384, in compile
          self.initialize()
          ~~~~~~~~~~~~~~~^^
        File "C:\Users\dzikohn\AppData\Local\Temp\pip-build-env-p8trkzdn\overlay\Lib\site-packages\setuptools\_distutils\compilers\C\msvc.py", line 294, in initialize
          vc_env = _get_vc_env(plat_spec)
        File "C:\Users\dzikohn\AppData\Local\Temp\pip-build-env-p8trkzdn\overlay\Lib\site-packages\setuptools\_distutils\compilers\C\msvc.py", line 155, in _get_vc_env
          raise DistutilsPlatformError(
          ...<3 lines>...
          )
      distutils.errors.DistutilsPlatformError: Microsoft Visual C++ 14.0 or greater is required. Get it with "Microsoft C++ Build Tools": https://visualstudio.microsoft.com/visual-cpp-build-tools/
      [end of output]

  note: This error originates from a subprocess, and is likely not a problem with pip.
error: subprocess-exited-with-error

× Getting requirements to build wheel did not run successfully.
│ exit code: 1
╰─> See above for output.

note: This error originates from a subprocess, and is likely not a problem with pip.
PS C:\dev\Developer\sk-sandbox-backend>
