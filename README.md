Yep — that behavior is exactly what Windows is designed to do in this folder.
Even with admin rights, Windows blocks executing anything inside
C:\Program Files\WindowsApps\... because that directory is owned by the TrustedInstaller service and is part of the app-sandbox model.

So it’s not a problem with your Ubuntu install — it’s simply being blocked by Windows’ security isolation.
Here’s how to finish setup safely 👇

⸻

✅ Easiest Fix — Manually register Ubuntu using the included install.tar.gz

Since we can’t run ubuntu.exe from inside that folder, we’ll use its data file (install.tar.gz) directly to create a working WSL instance.

1. Copy the tarball somewhere writable

Run this in PowerShell as Administrator:

copy "C:\Program Files\WindowsApps\CanonicalGroupLimited.UbuntuonWindows_2004.2021.825.0_x64__79rhkp1fndgsc\install.tar.gz" C:\dev\

2. Import it as a new WSL distribution

Then run:

wsl --import Ubuntu-20.04 C:\dev\Ubuntu C:\dev\install.tar.gz --version 2

Here’s what this means:
	•	Ubuntu-20.04 → name of your new distro
	•	C:\dev\Ubuntu → where its filesystem will live
	•	C:\dev\install.tar.gz → the root filesystem you just copied
	•	--version 2 → tells WSL to register it as a WSL2 distro

3. Start it up

wsl -d Ubuntu-20.04

You’ll then see:

Installing, this may take a few minutes...

followed by the prompt to create your UNIX username and password.

✅ Once that’s done, you have a fully registered Ubuntu 20.04 running under WSL2.

⸻

4. (Optional) Make it your default distro

wsl --set-default Ubuntu-20.04


⸻

If you’d like, I can give you a single ready-to-paste PowerShell block that does all three steps (copy → import → start) automatically.
Would you like that version?
