<h1 align="center">Echo-X Monitor</h1>

<p align="center"><b>Network latency monitor with ping/MTR, alarms and drag-and-drop hosts</b></p>

<p align="center">
  ![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)
  ![Platform](https://img.shields.io/badge/platform-Windows-0078D6?logo=windows&logoColor=white)
  ![Updated](https://img.shields.io/badge/updated-2026-04-15-success)
  [![Releases](https://img.shields.io/badge/downloads-Releases-blue)](https://github.com/alisadhk/echo-x-monitor/releases/latest)
</p>

---

## Overview
Echo-X Monitor is a PyQt5 network monitoring tool. It pings and traces (MTR) many destinations, colors each host by latency and raises sound alarms when a host becomes slow or unreachable. Predefined locations can use SSH sources to measure latency from remote probes.

## Features
- Ping and MTR to any destination
- Latency thresholds with four colors (good, medium, warning, error)
- Sound alarms (Windows beep or your own WAV) and softer warnings
- Drag and drop host ordering, column count and font-size controls
- Snooze and host keys shortcuts
- License activation dialog

## Screenshots
<p align="center"><img src="screenshots/screenshot-1.png" alt="Echo-X Monitor screenshot" width="720"></p>

## Download and install
### Option A - Ready-to-run download (recommended)
1. Open the **[Releases page](https://github.com/alisadhk/echo-x-monitor/releases/latest)**.
2. Download the file(s) listed under **Assets**:

| File | Size |
|---|---|
| `Echo-X-Monitor.exe` | 38.1 MB |
| `Echo-X-Monitor-archive.rar` | 37.7 MB |

3. Run it. 

### Option B - Run from source
Requirements: Windows 10/11 and Python 3.10+.

```bash
git clone https://github.com/alisadhk/echo-x-monitor.git
cd echo-x-monitor
python -m pip install -r requirements.txt
python 666.py
```

## How to use
1. Enter a destination (for example 8.8.8.8) and press **Ping** or **MTR**.
2. Open **Settings** to set the ping thresholds, colors and alarm sounds.
3. Use **Host Keys** to bind shortcuts and **Snooze** to mute alarms temporarily.
4. Use **Clear All** to reset the dashboard.

## Configuration and privacy
- All sensitive values from the original private version (passwords, tokens, license codes, user names, internal IP addresses, personal names and links) were replaced with `*****`.
- The LOCATIONS table (SSH hosts, users, passwords and source IPs) is fully masked. Fill in your own probes to use the remote-source feature.
- The license key is masked; set your own in 666.py.

## Build the executable yourself
```bash
python -m pip install pyinstaller
python -m PyInstaller --noconfirm 666.spec
```
The executable is created in the `dist/` folder.

## Notes
- Windows only (uses Windows sound and ping behavior).

---

<p align="center">Maintained by <a href="https://github.com/alisadhk">@alisadhk</a> - last update 2026-04-15</p>