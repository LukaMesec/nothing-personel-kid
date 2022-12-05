### How do I activate Windows? (10/11)
https://github.com/massgravel/Microsoft-Activation-Scripts

HWID mimics upgrade activation to generate a permanent legitimate license.
(Does not work on VL editions that need KMS, avoid VL/KMS)

**Which version should I install?**
- Home/Pro
Comes with bloatware apps (games, music, news, weather, etc)
- Education/Workstation/Enterprise
Comes with basic system apps.
- LTSC / IoT LTSC
LTSC = 5 years support, VL/KMS only
IoT LTSC = 10 years support, HWID only
Comes with Win32 system apps, no MS Store, no feature updates, security updates only.
If you need MS Store, run this in cmd: wsreset -i
There are no compatibility differences between versions.

**Do I even need IoT LTSC?**
- W10 Home/Pro/Edu/WS/Ent editions end support in 10/2025, LTSC in 2027, IoT LTSC lasts until 2032.

**How do I activate Office?**
- https://github.com/abbodi1406/KMS_VL_ALL_AIO/releases
Installs a KMS server emulator, not ideal as KMS trips AV sometimes and deactivates. Alternatively, use MSOffice through your browser since it's free. As a last resort, you can try LibreOffice and set it to save as Office file formats.

**Where can I get Windows/Office ISOs?**
- https://massgrave.dev/genuine-installation-media.html
- Other sources:
https://pastebin.com/p6b3N9w2

**Is Optimize-Offline worth it?**
**Should I debloat?**

If you need to ask, then no. You WILL break something and then come crying about updates/store/feature not working.
If you know what you're doing:
- https://www.oo-software.com/en/shutup10
- https://wpd.app
- https://github.com/builtbybel/LoveWindowsAgain/releases
- https://github.com/AveYo/fox/blob/main/Edge_Removal.bat

**Windows/Office installation guide**
https://pastebin.com/Q4ced4rE

**B-b-b-but muh Windows 7!**
OpenShell

WinInfo Pasta:
https://rentry.org/fwt

***th-thanks /g/***
### Win 7 (x64) -> Win 10 update error 0x80072F8F - 0x20000 FIX

- enable win update service
- enable wecsvc service
- enable windows event log update service
- empty /Windows/SoftwareDistribution
- download Update for Windows 7 for x64-based Systems (KB3140245) from [here](https://catalog.update.microsoft.com/search.aspx?q=kb3140245)
- download easy fix from [here](https://support.microsoft.com/en-us/topic/update-to-enable-tls-1-1-and-tls-1-2-as-default-secure-protocols-in-winhttp-in-windows-c4bd73d2-31d7-761e-0178-11268bb10392#:~:text=Enable%20TLS%201.1%20and%201.2%20on%20Windows%207%20at%20the,set%20it%20to%20%220%22)