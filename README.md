Excellent — that example gives the full picture ✅

This message:

Expected sha256 3a5002057...
Got        7b9d701a5...

means pip downloaded the pip-tools wheel, but its hash doesn’t match what your environment expects.

You don’t actually have a requirements file issue here — the problem is that your Python environment is using a mirrored or cached repository that serves a slightly different package than PyPI (very likely your internal Nexus mirror).

⸻

🧩 Why This Happens

Because you’re in a corporate network using

https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple

your system downloads packages from the Nexus mirror, not from PyPI.org.
If Nexus’ copy of the package has changed or been rebuilt, its hash will differ — triggering this exact error.

⸻

✅ Fix Option 1 (Recommended): Use the official PyPI for this install

You can override the internal index temporarily:

py -m pip install --no-cache-dir --index-url https://pypi.org/simple pip-tools

That fetches the package directly from PyPI and should succeed.

⸻

✅ Fix Option 2: Clear your pip cache

Sometimes pip caches a bad or outdated wheel.
Try:

py -m pip cache purge

Then re-run:

py -m pip install pip-tools


⸻

✅ Fix Option 3: Disable hash verification (only if you trust your source)

If your corporate Nexus repo is required, and you’re confident it’s safe:

py -m pip install --no-deps --no-cache-dir --no-hashes pip-tools

⚠️ This skips hash integrity checks — safe only on trusted internal mirrors.

⸻

✅ Fix Option 4: Tell pip to ignore the config file entirely

You can override your global config with:

py -m pip install --no-cache-dir --no-config --index-url https://pypi.org/simple pip-tools

This ignores any custom index URLs or hash policies from pip.ini.

⸻

Try Option 1 first — if it works, we’ve confirmed the Nexus mirror is serving a mismatched file.
Would you like me to show how to reset pip’s config so it no longer points to your internal Nexus by default (so you don’t have to override it every time)?
