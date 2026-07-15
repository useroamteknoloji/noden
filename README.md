# Noden — SSH, SFTP & AI for macOS

<p align="center">
  <img src="https://noden.useroamteknoloji.com/noden-icon.png" width="128" alt="Noden app icon">
</p>

<p align="center">
  A native macOS SSH client with multi-session terminals, a dual-pane SFTP file manager and an optional AI command assistant.
</p>

<p align="center">
  <a href="https://noden.useroamteknoloji.com/">Website</a> ·
  <a href="https://noden.useroamteknoloji.com/docs.html">Documentation</a> ·
  <a href="https://noden.useroamteknoloji.com/downloads/Noden-1.0.dmg">Direct download</a> ·
  <a href="https://github.com/useroamteknoloji/homebrew-tap">Homebrew tap</a>
</p>

![Noden multi-session SSH terminal](https://noden.useroamteknoloji.com/shots/shot-5.png)

## What is Noden?

Noden brings the SSH tools Mac developers and server administrators use every day into one native app:

- Saved SSH connections with password, Ed25519 and ECDSA key authentication
- Multiple terminals in tabs or a one-to-four-column grid
- Dual-pane local/remote SFTP file management with drag-and-drop transfers
- Remote file editing with automatic upload after saving
- Searchable command history and autocomplete
- Import from `~/.ssh/config`
- Password-encrypted connection backups
- AI-generated shell commands that are shown for approval before execution
- Credentials stored in macOS Keychain

Noden supports macOS 13 Ventura and later on Apple Silicon and Intel Macs.

## Install

### Homebrew

```bash
brew install --cask useroamteknoloji/tap/noden
```

### Direct download

Download the notarized DMG from the [official Noden website](https://noden.useroamteknoloji.com/downloads/Noden-1.0.dmg).

## Free and Pro

The free version includes the SSH terminal, SFTP commander, up to five saved connections and the latest 50 command-history entries. Noden Pro costs USD 10 per year and adds unlimited connections, full history and the AI assistant.

## AI command assistant

Describe a server task in plain English and Noden proposes shell commands for the active SSH session. Every command is displayed before execution and requires approval. Potentially dangerous operations are flagged. You can use Noden's provider or configure OpenAI, Groq, OpenRouter or a local model.

![Noden AI command assistant](https://noden.useroamteknoloji.com/shots/shot-3.png)

## MobaXterm alternative for Mac

MobaXterm is a Windows application. Noden is designed specifically for macOS users who need its core SSH workflow: saved sessions, split terminals and graphical SFTP transfers. Noden does not provide RDP, VNC or an X11 server; users who need those protocols should use a dedicated tool alongside it.

Read the full [MobaXterm alternative for Mac comparison](https://noden.useroamteknoloji.com/mobaxterm-alternative-for-mac.html).

## Support

- Documentation: https://noden.useroamteknoloji.com/docs.html
- Email: noden@useroamteknoloji.com
- Issues: use this repository's issue tracker for reproducible bugs and feature requests

## About this repository

Noden is proprietary software developed by [Useroam Teknoloji](https://useroamteknoloji.com/). This public repository is the official home for product information, release links, issue tracking and community feedback; it does not contain the application source code.

