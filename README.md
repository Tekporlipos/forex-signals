Perfect — this is a classic corporate Nexus/PyPI proxy issue, and your output tells us exactly what’s happening.

Let’s break it down clearly 👇

⸻

💡 What’s happening

You’re installing from:

https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple

That’s an internal Nexus (private PyPI proxy).

When pip tries to build or install certain packages (like cffi), it spawns a subprocess that also tries to download dependencies — and that subprocess doesn’t inherit your authentication credentials.

So pip asks again:

User for tools.rbspeople.com:

But inside that subprocess, there’s no terminal input available, so input() raises:

EOFError: EOF when reading a line

That’s why it fails.

⸻

✅ How to fix it

Option 1: Use a pip config file with credentials

Create or edit this file:

Windows:

%APPDATA%\pip\pip.ini

Linux/macOS:

~/.config/pip/pip.conf

Add your internal repo and credentials (replace with your real username/password):

[global]
index-url = https://mhL48uC-:YOUR_PASSWORD@tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple
trusted-host = tools.rbspeople.com

🧠 Tip: if your password contains special characters (@, #, !, :), URL-encode them
e.g., p@ss!word → p%40ss%21word

Then rerun:

py -m pip install -r requirements.txt

Now pip (and its subprocesses) will authenticate automatically.

⸻

Option 2: Use an environment variable instead

If you don’t want to store credentials in plaintext:

$env:PIP_INDEX_URL = "https://mhL48uC-:YOUR_PASSWORD@tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple"
$env:PIP_TRUSTED_HOST = "tools.rbspeople.com"
py -m pip install -r requirements.txt


⸻

Option 3: (If allowed) temporarily use public PyPI for missing packages

If your Nexus repo doesn’t proxy all packages, you can fall back to public PyPI:

py -m pip install -r requirements.txt --extra-index-url https://pypi.org/simple


⸻

🧩 Bonus Tip: cffi build dependencies

If it still fails at cffi, you might need build tools for Python extensions.

Install them with:

py -m pip install wheel setuptools
py -m pip install --upgrade pip

And make sure Visual Studio Build Tools (C++ workload) are installed:

https://visualstudio.microsoft.com/visual-cpp-build-tools/


⸻

Would you like me to show you exactly what your pip.ini should look like with placeholders (so you can just paste and edit)?
