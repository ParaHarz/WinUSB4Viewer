<div align="center">

# WinUSB4Viewer

**The USB4 domain information Windows Settings shows — on one screen and on one command.**

[![License](https://img.shields.io/badge/License-Proprietary-lightgrey.svg)](LICENSE.txt)

Everything Windows Settings reports about your USB4 domain — topology, silicon identity,
USB4 version, and DisplayPort adapter counts — for every host router and each connected
device router on the machine.

**Download:** [`WinUSB4Viewer-1.0.0-win64.zip`](https://github.com/ParaHarz/WinUSB4Viewer/releases/download/v1.0.0/WinUSB4Viewer-1.0.0-win64.zip) — free, two .exe files, nothing to install.

SHA-256: `70B5902671EE81659AED90BD4BDE07B0726AF9D1C95678158B239B0B105E5158`

</div>

---

## What it shows

- **Topology** — the USB4 domain tree: host router, connected device routers, topology IDs, upstream links
- **Silicon identity** — vendor ID, product ID, silicon revision, manufacturer and model names
- **USB4 version** — router and connection manager versions, device firmware version
- **Link details** — current speed, negotiated width, lane bonding, TBT3-compatible mode, HEC error counters
- **DisplayPort adapters** — total and tunneled DP IN adapter counts

## Features

- **Read-only** — never modifies system state
- **Two front-ends** — pick the GUI or the command line:
  - **WinUSB4Viewer.exe** — native Windows interface with Refresh, Copy, and About
  - **WinUSB4ViewerCli.exe** — command-line output for scripting and diagnostics
- **Zero dependencies** — no runtimes, no installer, runs on a clean Windows 11 machine

## Requirements

- Windows 11 (64-bit)
- USB4-capable hardware with the Windows USB4 host-router driver loaded
- Administrator rights for the command-line tool

## Quick start

1. Download the zip and extract it anywhere you like (e.g. `C:\Tools\WinUSB4Viewer`)
2. Run `WinUSB4Viewer.exe` — your host routers and connected devices appear as cards
3. **Copy** puts the full report on the clipboard; **About** shows version and publisher
4. Optional: script it — `WinUSB4ViewerCli.exe` from an elevated terminal

## Command line

```text
WinUSB4ViewerCli.exe [--duration seconds] [--diagnostics] [--rescan]
```

| Option | Description |
| --- | --- |
| `--duration <seconds>` | Capture duration, 1–300 seconds (default: 2) |
| `--diagnostics` | Print properties and counters |
| `--rescan` | Request a native Plug and Play device-tree re-enumeration during capture |
| `-h`, `--help` | Print command-line help |

Running the executable with no arguments also prints command-line help.

Exit codes: `0` successful snapshot · `1` argument or Windows API error ·
`2` no provider events observed · `3` one or more events could not be decoded.

## Publisher

| | |
| --- | --- |
| Publisher | ParaHarz Software |
| Website | https://www.paraharz.com |
| Support | support@paraharz.com |
| Copyright | © 2024 ParaHarz Software |

## License

[Proprietary](LICENSE.txt) © 2024 ParaHarz Software — see `LICENSE.txt` for the full text,
including restrictions on AI or machine-learning use.
