# Noden — SSH, SFTP, RDP & serial console for macOS

<p align="center">
  <img src="https://noden.useroamteknoloji.com/noden-icon.png?v=2" width="128" alt="Noden app icon">
</p>

<p align="center">
  A native macOS client for everything you connect to — SSH, SFTP, Windows remote desktops and console cables — with a Touch ID password vault and an AI assistant that knows which machine it is on. A Windows desktop, two Linux shells and a file manager, open at once, side by side, in one window.
</p>

<p align="center">
  <a href="https://noden.useroamteknoloji.com/">Website</a> ·
  <a href="https://noden.useroamteknoloji.com/docs.html">Documentation</a> ·
  <a href="https://apps.apple.com/us/app/noden-ssh-sftp-rdp-vault/id6786746277?mt=12">Mac App Store</a> ·
  <a href="https://github.com/useroamteknoloji/homebrew-tap">Homebrew tap</a> ·
  <a href="https://github.com/useroamteknoloji/noden/releases">Releases</a>
</p>

![Noden multi-session SSH terminal](https://noden.useroamteknoloji.com/shots/shot-5.png)

## What is Noden?

Four tools that usually need four apps — a terminal, a file manager, a remote-desktop client and a serial console — built to work together in one window, plus a password vault behind Touch ID and an assistant tuned for the command line.

Native Swift, no Electron. macOS 13 Ventura and later, Apple Silicon and Intel, notarized by Apple. Available as a direct download, via Homebrew, and on the Mac App Store.

## Terminal

- Saved SSH connections with password, Ed25519 and ECDSA key authentication
- As many sessions as you like: tabs, or a resizable one-to-four-column grid to watch several servers at once
- **Tear a tab off into its own window** — the live session moves with it, the connection never drops, and it docks back when you drag the chip onto the tab bar or close the window
- Per-tab latency, so a slow host is visible at a glance
- Broadcast one line to every open tab
- Full xterm-compatible emulator: colour themes, custom fonts, adjustable cursor, scrollback, bell
- Searchable command history with autocomplete, snippets, and ⌘P to jump anywhere
- Jump hosts (ProxyJump) and local port forwarding — reach a database or web console behind a bastion
- Uses the keys already in your `~/.ssh` and imports your `~/.ssh/config`
- Host key verification on first connect, with a clear warning if a key ever changes
- ⌘T opens a shell on your own Mac, with your real PATH, Homebrew and dotfiles

## SFTP file commander

- Dual-pane local/remote, drag and drop in either direction and straight from Finder
- Native table: resizable, reorderable, sortable columns that remember your layout
- Open a remote file in your own editor — Noden syncs it back the moment you save
- Quick Look with a tap of Space
- Conflict prompt on large copies: replace, skip, or apply to all
- Pop the file browser out into its own window next to a terminal

## RDP remote desktop

- Windows machines open as a tab next to your Linux shells, or in the grid beside them
- Rendered with Metal — clipboard and file copy-paste in both directions, and folder sharing into the session
- RD Gateway, admin/console session, domain logins, auto-reconnect
- Resolution follows the window as you resize
- Server certificates are verified, with a separate warning if one changes or the name does not match

![Windows RDP session in a Noden tab](https://noden.useroamteknoloji.com/shots/shot-rdp.png)

## Serial console

- USB-to-serial console sessions for routers, switches, firewalls and embedded boards
- Vendor presets with the real factory speeds: Cisco IOS/Catalyst 9600, FortiGate 9600, **Sophos XG/XGS 38400**, MikroTik 115200, HPE Aruba AOS-CX 115200, Ubiquiti 115200 — all 8N1
- The device list refreshes itself while the dialog is open, so you can plug the cable in after you start

## Password vault

- A built-in manager for the secrets of server life: passwords, SSH private keys, API tokens and secure notes
- Protected by Touch ID (or your login password) and stored **only in your Mac's Keychain** — never on our servers
- Link a connection to a vault entry: change the secret once and every session that uses it follows — terminal, SFTP, jump host and RDP included
- Type a password straight into the terminal, ideal right after `sudo su` — it never enters your command history
- Answer a password prompt automatically on connect: give a connection an "On connect" command such as `sudo su` and pick which secret answers it
- Double-click an entry to copy it; the clipboard clears itself after 30 seconds
- Built-in password generator, and encrypted vault export/import for a new Mac

## AI command assistant

Describe a server task in plain English and Noden answers for the machine you are actually on. On a Linux host it writes the shell command and offers to run it — every command is shown before execution and needs your approval, and potentially destructive ones are flagged first. On a Windows machine it drops the shell talk and answers like a Windows engineer.

Use the built-in Noden AI, or bring your own key: presets for ChatGPT (OpenAI), Groq and OpenRouter, or any OpenAI-compatible endpoint including a local model (LM Studio, vLLM). Your key stays in your Mac's Keychain.

![Noden AI command assistant](https://noden.useroamteknoloji.com/shots/shot-3.png)

## Privacy and safety

- Passwords and keys live only in the macOS Keychain; file contents are never collected
- Touch ID lock on launch
- Password-encrypted backup and restore for connections, and a separate encrypted vault export
- Anonymous usage statistics can be switched off in Settings ▸ General ▸ Privacy
- Closing a live session asks first, so a stray ⌘W cannot drop a connection

## Install

```bash
brew install --cask useroamteknoloji/tap/noden
```

Or download the notarized DMG from the [Noden website](https://noden.useroamteknoloji.com/), or get it on the [Mac App Store](https://apps.apple.com/us/app/noden-ssh-sftp-rdp-vault/id6786746277?mt=12). The direct build updates itself; the App Store build updates through the App Store.

## Free and Pro

Free covers the SSH terminal, the SFTP file manager, RDP and serial consoles, with up to **5 saved connections, 20 vault secrets and your last 50 commands**.

**Noden Pro — USD 10 per year** — unlocks unlimited connections, unlimited vault secrets, the full command history and the AI assistant. On the Mac App Store this is an auto-renewing subscription managed by Apple; the direct build uses a licence key.

A Team plan is planned but **not on sale yet**; everything listed under it on the website is still in development.

## Languages

English, Türkçe, Deutsch, Español, Français.

## MobaXterm alternative for Mac

MobaXterm is a Windows application. Noden covers its core workflow on macOS: saved sessions, split terminals, graphical SFTP transfers, serial consoles and RDP in the same window. Noden does not provide VNC or an X11 server; if you need those protocols, use a dedicated tool alongside it.

Read the full [MobaXterm alternative for Mac comparison](https://noden.useroamteknoloji.com/mobaxterm-alternative-for-mac.html).

## Support

- Documentation: https://noden.useroamteknoloji.com/docs.html
- Email: noden@useroamteknoloji.com
- Issues: use this repository's issue tracker for reproducible bugs and feature requests

## About this repository

Noden is proprietary software developed by [Useroam Teknoloji](https://useroamteknoloji.com/). This public repository is the official home for product information, release links, issue tracking and community feedback; it does not contain the application source code.
