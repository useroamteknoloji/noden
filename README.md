# Noden — SSH, SFTP, RDP & serial console for macOS

<p align="center">
  <img src="https://noden.useroamteknoloji.com/noden-icon.png?v=2" width="128" alt="Noden app icon">
</p>

<p align="center">
  <strong>A native macOS client for everything you connect to.</strong><br>
  SSH terminals, SFTP transfers, Windows remote desktops and console cables — with a Touch ID password vault and an AI assistant that knows which machine it is on.<br>
  A Windows desktop, two Linux shells and a file manager, open at once, side by side, in one window.
</p>

<p align="center">
  <a href="https://github.com/useroamteknoloji/noden/releases/latest"><img src="https://img.shields.io/github/v/release/useroamteknoloji/noden?label=release&color=3ad0ac" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/macOS-13%2B-333" alt="macOS 13 Ventura or later">
  <img src="https://img.shields.io/badge/arch-Apple%20Silicon%20%26%20Intel-333" alt="Apple Silicon and Intel">
  <img src="https://img.shields.io/badge/built%20with-Swift%20%26%20SwiftUI-333" alt="Native Swift and SwiftUI, no Electron">
  <a href="https://apps.apple.com/us/app/noden-ssh-sftp-rdp-vault/id6786746277?mt=12"><img src="https://img.shields.io/badge/Mac%20App%20Store-available-3ad0ac" alt="On the Mac App Store"></a>
</p>

<p align="center">
  <a href="https://noden.useroamteknoloji.com/">Website</a> ·
  <a href="https://noden.useroamteknoloji.com/docs.html">Documentation</a> ·
  <a href="https://apps.apple.com/us/app/noden-ssh-sftp-rdp-vault/id6786746277?mt=12">Mac App Store</a> ·
  <a href="https://github.com/useroamteknoloji/homebrew-tap">Homebrew tap</a> ·
  <a href="https://github.com/useroamteknoloji/noden/releases">Releases</a>
</p>

![Noden on macOS with a Windows RDP session, two SSH terminals and an SFTP file browser open side by side in one window](https://noden.useroamteknoloji.com/shots/shot-grid.png)

## Install

```bash
brew install --cask useroamteknoloji/tap/noden
```

Or download the notarized DMG from the [Noden website](https://noden.useroamteknoloji.com/), or get it on the [Mac App Store](https://apps.apple.com/us/app/noden-ssh-sftp-rdp-vault/id6786746277?mt=12). The direct build updates itself; the App Store build updates through the App Store.

Requires macOS 13 Ventura or later. Universal binary — Apple Silicon and Intel. Notarized by Apple.

## What is Noden?

Four tools that usually need four apps — a terminal, a file manager, a remote-desktop client and a serial console — built to work together in one window, plus a password vault behind Touch ID and an assistant tuned for the command line.

The point is not that Noden has four protocols. It is that they share a window. The terminal for a server sits next to that same server's file tree; the Windows box you need to check is a tab away, not an app away. Nothing is lost switching between them, because you never switch.

Native Swift and SwiftUI. No Electron, no bundled browser. Available as a direct download, via Homebrew, and on the Mac App Store.

## Getting started

![Noden's New Connection dialog with host, port, username and authentication method](https://noden.useroamteknoloji.com/shots/shot-3.png)

Open Noden and press **New Connection**. Give it a host, a username and an authentication method — *Mac SSH Key* picks up the Ed25519 or ECDSA key already in your `~/.ssh` with nothing to configure. Existing `~/.ssh/config` hosts can be imported in one step. Connections can be grouped, and every group is searchable from the sidebar.

Full walkthrough in the [documentation](https://noden.useroamteknoloji.com/docs.html).

## Terminal

![Four SSH sessions in a two-by-two grid in Noden](https://noden.useroamteknoloji.com/shots/shot-2.png)

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

![Noden's dual-pane SFTP browser with the local Mac on the left and the remote server on the right](https://noden.useroamteknoloji.com/shots/shot-files.png)

- Dual-pane local/remote, drag and drop in either direction and straight from Finder
- Native table: resizable, reorderable, sortable columns that remember your layout
- Open a remote file in your own editor — Noden syncs it back the moment you save
- Quick Look with a tap of Space
- Conflict prompt on large copies: replace, skip, or apply to all
- Pop the file browser out into its own window next to a terminal

## RDP remote desktop

![A Windows desktop running as a tab inside Noden on macOS](https://noden.useroamteknoloji.com/shots/shot-rdp.png)

- Windows machines open as a tab next to your Linux shells, or in the grid beside them
- Rendered with Metal — clipboard and file copy-paste in both directions, and folder sharing into the session
- RD Gateway, admin/console session, domain logins, auto-reconnect
- Resolution follows the window as you resize
- Server certificates are verified, with a separate warning if one changes or the name does not match

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

Describe a server task in plain English and Noden answers for the machine you are actually on. On a Linux host it writes the shell command and offers to run it — every command is shown before execution and needs your approval, and potentially destructive ones are flagged first.

![Noden's AI assistant turning "show disk usage" into df -h on a Linux server](https://noden.useroamteknoloji.com/shots/shot-4.png)

On a Windows machine it drops the shell talk and answers like a Windows engineer — the same question comes back as PowerShell.

![The same assistant answering a PowerShell question inside a Windows RDP session](https://noden.useroamteknoloji.com/shots/shot-rdp-ai.png)

Use the built-in Noden AI, or bring your own key: presets for ChatGPT (OpenAI), Groq and OpenRouter, or any OpenAI-compatible endpoint including a local model (LM Studio, vLLM). Your key stays in your Mac's Keychain.

## Privacy and safety

- Passwords and keys live only in the macOS Keychain; file contents are never collected
- Touch ID lock on launch
- Password-encrypted backup and restore for connections, and a separate encrypted vault export
- Anonymous usage statistics can be switched off in Settings ▸ General ▸ Privacy
- Closing a live session asks first, so a stray ⌘W cannot drop a connection

Security reports: see [SECURITY.md](SECURITY.md).

## Free and Pro

Free is not a trial. The SSH terminal, the SFTP file manager, RDP and serial consoles all work without paying, within these limits:

| | Free | Pro |
|---|---|---|
| **Price** | USD 0 | **USD 5.99 first year, then USD 10.99 / year** |
| SSH terminal, split grid, tear-off windows | ✅ | ✅ |
| SFTP file commander | ✅ | ✅ |
| RDP remote desktop | ✅ | ✅ |
| Serial console | ✅ | ✅ |
| Saved connections | 5 | Unlimited |
| Vault secrets | 20 | Unlimited |
| Command history | Last 50 | Full history |
| AI command assistant | — | ✅ |

**Noden Pro costs USD 5.99 for the first year and USD 10.99 per year afterwards.** On the Mac App Store, Pro is an auto-renewing subscription managed by Apple; the direct build uses a licence key. A Team plan is planned but **not on sale yet**; everything listed under it on the website is still in development.

## Languages

English, Türkçe, Deutsch, Español, Français.

## What Noden does not do

Stated plainly, so nobody installs it expecting the wrong thing:

- **No VNC and no X11 server.** If you need those protocols, run a dedicated tool alongside Noden.
- **macOS only.** No Windows or Linux build, and none planned — Noden is native AppKit/SwiftUI, not a cross-platform shell.
- **Not open source.** This repository is the product's public home, not its source code. See [About this repository](#about-this-repository).

## Coming from another tool

Noden is built for people replacing a Windows habit or a stack of separate Mac apps. Each page below is an honest side-by-side — including what Noden does not cover.

| If you use | Read |
|---|---|
| **MobaXterm** on Windows | [MobaXterm alternative for Mac](https://noden.useroamteknoloji.com/mobaxterm-alternative-for-mac.html) — saved sessions, split terminals, SFTP and serial in one window |
| **PuTTY** on Windows | [PuTTY for Mac](https://noden.useroamteknoloji.com/putty-for-mac.html) — there is no native PuTTY on macOS; here is what to use instead |
| **WinSCP** on Windows | [WinSCP for Mac](https://noden.useroamteknoloji.com/winscp-alternative-for-mac.html) — dual-pane transfers, natively |
| **Termius** | [Termius alternative for Mac](https://noden.useroamteknoloji.com/termius-alternative-for-mac.html) |
| **Royal TSX** | [Royal TSX alternative for Mac](https://noden.useroamteknoloji.com/royal-tsx-alternative-for-mac.html) |
| **FileZilla** | [FileZilla alternative for Mac](https://noden.useroamteknoloji.com/filezilla-alternative-for-mac.html) |
| **Microsoft Remote Desktop** | [Microsoft Remote Desktop alternative for Mac](https://noden.useroamteknoloji.com/microsoft-remote-desktop-alternative-for-mac.html) |
| **iTerm2** | [iTerm2 for SSH](https://noden.useroamteknoloji.com/iterm2-ssh-alternative.html) — what saved connections, SFTP and AI add on top |
| **SSHive** | [Noden vs SSHive](https://noden.useroamteknoloji.com/noden-vs-sshive.html) |
| **Tempest** | [Noden vs Tempest](https://noden.useroamteknoloji.com/noden-vs-tempest.html) |

Still choosing? [Best SSH client for Mac (2026)](https://noden.useroamteknoloji.com/best-ssh-client-for-mac.html) covers the free and paid options, Noden included.

## Guides

- [How to use SSH on a Mac](https://noden.useroamteknoloji.com/how-to-use-ssh-on-mac.html) — Terminal.app first, then what a client adds
- [How to use SFTP on a Mac](https://noden.useroamteknoloji.com/how-to-use-sftp-on-mac.html) — command line and graphical transfers
- [macOS SSH client](https://noden.useroamteknoloji.com/macos-ssh-client.html) · [Mac SFTP client](https://noden.useroamteknoloji.com/mac-sftp-client.html) · [RDP client for Mac](https://noden.useroamteknoloji.com/rdp-client-for-mac.html)
- [SSH password manager for Mac](https://noden.useroamteknoloji.com/ssh-password-manager-mac.html) — where server passwords actually belong
- [AI SSH client](https://noden.useroamteknoloji.com/ai-ssh-client.html) — plain English to commands
- [SSH, SFTP and RDP in one Mac app](https://noden.useroamteknoloji.com/ssh-sftp-rdp-mac.html)

## FAQ

**Is Noden free?**
Yes, with limits. The terminal, SFTP, RDP and serial console are free, capped at 5 saved connections, 20 vault secrets and your last 50 commands. Pro lifts all three caps and adds the AI assistant.

**How much does Noden Pro cost?**
USD 5.99 for the first year, then USD 10.99 per year. One price for everything Pro unlocks — unlimited saved connections, unlimited vault secrets, the full command history and the AI command assistant. Buying on the Mac App Store makes it an Apple-managed auto-renewing subscription; buying directly gives you a licence key.

**Does Noden work on Apple Silicon?**
Yes — a universal binary for Apple Silicon and Intel, notarized by Apple, on macOS 13 Ventura and later.

**Can I connect to Windows machines?**
Yes. RDP sessions open as tabs beside your SSH terminals, with clipboard and file copy-paste in both directions, folder sharing, RD Gateway and domain logins.

**Where are my passwords stored?**
In your Mac's Keychain, unlocked with Touch ID or your login password. They are never sent to a server of ours. File contents, passwords and keys are never collected.

**Does the AI assistant run commands on its own?**
Only if you let it. Every command is shown before execution and needs your approval, and potentially destructive ones are flagged first.

**Can I use my own AI model?**
Yes. Bring an OpenAI, Groq or OpenRouter key, or point Noden at any OpenAI-compatible endpoint — including a local model in LM Studio or vLLM. The key stays in your Keychain.

**Does it use my existing SSH keys and config?**
Yes. Noden reads the Ed25519 and ECDSA keys in `~/.ssh` and imports hosts from your `~/.ssh/config`.

**Is there a Windows or Linux version?**
No. Noden is a native macOS application and there is no cross-platform build planned.

**What is the difference between the Mac App Store build and the direct download?**
Payment, updates and one sandbox detail. On the App Store, Pro is an Apple subscription and updates arrive through the App Store; the direct build uses a licence key and updates itself. Because the App Store build is sandboxed, its ⌘T local shell reaches your own Mac over SSH, which needs Remote Login enabled in System Settings ▸ General ▸ Sharing.

## Support

- Documentation: https://noden.useroamteknoloji.com/docs.html
- Email: noden@useroamteknoloji.com
- Issues: use this repository's [issue tracker](https://github.com/useroamteknoloji/noden/issues) for reproducible bugs and feature requests
- Support policy: [SUPPORT.md](SUPPORT.md)

## About this repository

Noden is proprietary software developed by [Useroam Teknoloji](https://useroamteknoloji.com/). This public repository is the official home for product information, release links, issue tracking and community feedback; it does not contain the application source code.
