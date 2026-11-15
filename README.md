# NFWinTools

A native Windows software manager built on Windows Package Manager (**WinGet**) for discovering, updating, cleaning, and migrating desktop applications.

> **Official Distribution Repository** — This repository hosts verified public installers and release notes for NFWinTools.  
> **[Download the Latest Release](https://github.com/sirfnomi/NFWinTools-Releases/releases/latest)**

---

## Core Capabilities

- **Software Updates & Automation** — Scans for available updates on launch, supports one-click and batch updates, and runs configurable Windows Task Scheduler background checks (notify-only, selected apps, or safe updates) that pause on metered networks.
- **Installed Apps** — View, search, and uninstall installed software from a unified inventory.
- **Search & Discover** — Search and install packages across WinGet and Microsoft Store catalogs.
- **Storage & Caches** — Inspect and clean leftover installer and package caches to reclaim disk space.
- **Migration & Backup** — Export and import application bundles to set up or restore software across Windows machines.
- **Diagnostics & Logs** — Monitor WinGet health, package sources, and operation logs.
- **Verified Self-Updates** — In-app updates strictly verify `SHA256SUMS.txt` before launching the installer.

---

## System Requirements

| Requirement | Details |
| :--- | :--- |
| **Operating System** | Windows 10 (version 1809 / build 17763 or later) or Windows 11 |
| **Architecture** | 64-bit (`x64`) |
| **Dependency** | Windows Package Manager (**WinGet** / *App Installer*) |
| **Runtime** | None required — distributed as a self-contained installer |

---

## Installation

1. Open **[Releases](https://github.com/sirfnomi/NFWinTools-Releases/releases/latest)** and download `NFWinTools-Setup-v<version>-win-x64.exe`.
2. Run the installer and choose either **All Users** (administrator) or **Current User** installation scope.

### Unattended / Silent Installation

For automated deployments or scripting:

```powershell
.\NFWinTools-Setup-v<version>-win-x64.exe /SILENT /SUPPRESSMSGBOXES /NORESTART /CLOSEAPPLICATIONS
```

Uninstalling NFWinTools through Windows **Installed Apps** cleanly removes the application and its scheduled background task (`\NFWinTools\BackgroundAutoUpdater`).

---

## Verifying Downloads

Every release includes a `SHA256SUMS.txt` manifest. To verify the installer before running it:

```powershell
Get-FileHash .\NFWinTools-Setup-v<version>-win-x64.exe -Algorithm SHA256
```

Confirm that the output hash matches the entry in `SHA256SUMS.txt` from the same release.

---

## Support & Feedback

- **Bug Reports & Feature Requests:** [Open an Issue](https://github.com/sirfnomi/NFWinTools-Releases/issues)
