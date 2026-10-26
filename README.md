# WinUSB4Viewer

**Version 1.0.0.0** · Windows 11 · x64

WinUSB4Viewer is a native Windows utility that reports the USB4 domain information shown by
Windows Settings: topology, silicon identity, USB4 version, and DisplayPort adapter counts —
for every USB4 host router and each connected device router on the machine.

## Features

- USB4 domain topology across host and device routers (topology IDs, depth, upstream links)
- Silicon identity: vendor ID, product ID, silicon revision, manufacturer and model names
- USB4 version (router and connection manager) and device firmware version
- Link details: current speed, negotiated width, lane bonding, TBT3-compatible mode,
  HEC error counters
- DisplayPort adapter counts, including tunneled adapters
- Read-only: never modifies system state
- Two front-ends:
  - **WinUSB4Viewer.exe** — native Windows interface with Refresh, Copy, and About actions
  - **WinUSB4ViewerCli.exe** — command-line output for scripting and diagnostics

## Requirements

- Windows 11 (x64)
- USB4-capable hardware with the Windows USB4 host-router driver loaded
- Administrator rights for the command-line tool

## Command-line usage

Run from an elevated terminal:

```text
WinUSB4ViewerCli.exe [--duration seconds] [--diagnostics] [--rescan]
```

| Option | Description |
| --- | --- |
| `--duration <seconds>` | Capture duration, 1–300 seconds (default: 2). |
| `--diagnostics` | Print properties and counters. |
| `--rescan` | Request a native Plug and Play device-tree re-enumeration during capture. |
| `-h`, `--help` | Print command-line help. |

Running the executable with no arguments also prints command-line help.

Exit codes: `0` successful snapshot · `1` argument or Windows API error ·
`2` no provider events observed · `3` one or more events could not be decoded.

## Downloads

Binary releases for Windows x64 (no installation required) are published on the
[Releases page](../../releases) of this repository. Each package ships `WinUSB4Viewer.exe`,
`WinUSB4ViewerCli.exe`, and `LICENSE.txt`.

## Legal

WinUSB4Viewer is proprietary software. See `LICENSE.txt` for the distribution and use license,
including restrictions on AI or machine-learning use.

- Publisher: ParaHarz Software
- Contact: support@paraharz.com
- Website: https://www.paraharz.com
