# Noden — SSH, SFTP & RDP for macOS

<p align="center">
  <img src="https://noden.useroamteknoloji.com/noden-icon.png?v=2" width="128" alt="Noden app icon">
</p>

<p align="center">
  A native macOS client for SSH, SFTP and RDP. A Windows desktop, two Linux shells and a file manager — open at once, side by side, in one window.
</p>

<p align="center">
  <a href="https://noden.useroamteknoloji.com/">Website</a> ·
  <a href="https://noden.useroamteknoloji.com/docs.html">Documentation</a> ·
  <a href="https://noden.useroamteknoloji.com/">Direct download</a> ·
  <a href="https://github.com/useroamteknoloji/homebrew-tap">Homebrew tap</a>
</p>

![Noden multi-session SSH terminal](https://noden.useroamteknoloji.com/shots/shot-5.png)

## What is Noden?

Three tools that usually need three apps — a terminal, a file manager and a remote-desktop client — built to work together in one window, plus an assistant that knows which machine it is on.

**Terminal**

- Saved SSH connections with password, Ed25519 and ECDSA key authentication
- Tabs or a resizable one-to-four-column grid
- Per-tab latency, so a slow host is visible at a glance
- Broadcast one line to every open tab
- Searchable command history with autocomplete, snippets, and ⌘P to jump anywhere
- SSH tunnels and jump-host (ProxyJump) support
- Imports the keys already in `~/.ssh` and your `~/.ssh/config`

**SFTP file manager**

- Dual-pane local/remote with drag-and-drop from Finder
- Native table: resizable, sortable, remembers your layout
- Edit a remote file in your own editor; Noden syncs it back when you save
- Quick Look with a tap of Space
- Conflict prompt on large copies: replace, skip, or all

**RDP remote desktop**

- Windows machines open as a tab next to your Linux shells, or in the grid beside them
- Clipboard and file copy-paste in both directions, and folder sharing into the session
- RD Gateway, admin/console session, domain logins, auto-reconnect
- Resolution follows the window as you resize

![Windows RDP session in a Noden tab](https://noden.useroamteknoloji.com/shots/shot-rdp.png)

**Everywhere**

- Credentials stored in the macOS Keychain — never on our servers, and file contents are never collected
- Touch ID lock on launch
- Password-encrypted connection backups
- Available in English, Türkçe, Deutsch, Español and Français
- Automatic updates (direct build)

Noden supports macOS 13 Ventura and later on Apple Silicon and Intel Macs.

## Install

### Homebrew

```bash
brew install --cask useroamteknoloji/tap/noden
```

### Direct download

Download the notarized DMG from the [official Noden website](https://noden.useroamteknoloji.com/).

## Free and Pro

The free version includes the SSH terminal, the SFTP file manager and RDP, up to five saved connections and the latest 50 command-history entries. Noden Pro costs USD 10 per year and adds unlimited connections, full history and the AI assistant.

A Team plan is planned but **not on sale yet**; everything listed under it on the website is still in development.

## AI command assistant

Describe a server task in plain English and Noden responds for the machine you are actually on. On a Linux host it writes the shell command and offers to run it — every command is displayed before execution and requires approval, and potentially dangerous operations are flagged. On a Windows machine it drops the command talk and answers like a Windows engineer.

Use the built-in assistant, or bring your own key — OpenAI, Claude, Kimi, Groq, OpenRouter or a local model.

![Noden AI command assistant](https://noden.useroamteknoloji.com/shots/shot-3.png)

## MobaXterm alternative for Mac

MobaXterm is a Windows application. Noden covers its core workflow on macOS: saved sessions, split terminals, graphical SFTP transfers and RDP in the same window. Noden does not provide VNC or an X11 server; users who need those protocols should use a dedicated tool alongside it.

Read the full [MobaXterm alternative for Mac comparison](https://noden.useroamteknoloji.com/mobaxterm-alternative-for-mac.html).

## Support

- Documentation: https://noden.useroamteknoloji.com/docs.html
- Email: noden@useroamteknoloji.com
- Issues: use this repository's issue tracker for reproducible bugs and feature requests

## About this repository

Noden is proprietary software developed by [Useroam Teknoloji](https://useroamteknoloji.com/). This public repository is the official home for product information, release links, issue tracking and community feedback; it does not contain the application source code.
