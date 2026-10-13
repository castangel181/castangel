# CastAngel — Cast your screen. Deliver your files.

> Browser-based remote desktop & file transfer for Windows 7 SP1 – 11.  
> Zero install. Zero cloud. Zero subscription. One portable `.exe`.

[![Windows](https://img.shields.io/badge/Windows-7%20SP1%20%E2%86%92%2011-blue?logo=windows)](https://castangel.com)
[![Architecture](https://img.shields.io/badge/Arch-32%20%26%2064--bit-green)](https://castangel.com/download/)
[![License](https://img.shields.io/badge/License-Proprietary-orange)](https://castangel.com/eula/)
[![Price](https://img.shields.io/badge/Price-from%20%2429%20one--time-success)](https://castangel.com/#pricing)

**[Website](https://castangel.com)** · **[Download](https://castangel.com/download/)** · **[Buy](https://castangel.com/#pricing)** · **[Guide](https://castangel.com/guide/)** · **[FAQ](https://castangel.com/faq/)** · **[Blog](https://castangel.com/blog/)**

---

## What is CastAngel?

CastAngel turns any Windows PC into a **browser-accessible remote desktop and file drop**. Run the portable `.exe` on the PC you want to reach, open the URL on any device on the same network, and you're in — full screen, mouse, keyboard, clipboard, and file transfer.

No install wizard. No cloud relay. No monthly subscription. No account. Just one `.exe` and a browser.

### Why CastAngel?

- **IT support techs** — reach a colleague's PC without installing anything on your machine
- **Shop floor / factory PCs** — remote into aging Windows 7 machines from a phone or tablet
- **Churches & non-profits** — assist members' computers, transfer files, no IT budget needed
- **Home networks** — help parents with their PC from the couch, without TeamViewer lag
- **File collection** — set up a file drop where multiple people upload to your desktop, auto-organized by name

---

## Features

### Remote Desktop
- **Browser-based viewer** — open a URL, get the screen. Any modern browser, any OS, nothing to install on the viewer.
- **WebSocket streaming** — real-time mouse, keyboard, and clipboard control.
- **Delta-compressed frames** — 64×64 macroblock inter-frame diffing keeps bandwidth low, even at 1080p. ~10 fps tuned for responsiveness over slow links.

### File Transfer
- **4 MB chunked upload** — push huge files without stalling. Broken uploads are cleaned up automatically.
- **Multi-user isolation** — each browser session gets its own sandboxed folder. Users can only see and delete their own files.
- **Path-traversal safe** — uploads can't escape the user folder.
- **Auto-file to desktop** — each person's files land in a desktop folder named after them. 张三's files → 「张三」, Alice's → 「Alice」.

### Security & Licensing
- **Hardware-bound license** — activation locks to SMBIOS + CPUID. No phone-home, no account, no telemetry.
- **LAN-only by design** — no cloud relay, no external servers, no port forwarding needed.
- **Tray-resident** — lives in the system tray, no console window. Blue = idle, green = connected.
- **Optional boot auto-start** — for always-on PCs.

### Compatibility
- **Windows 7 SP1 → 11** — built with the v141 toolset and Win7-safe APIs.
- **32-bit & 64-bit** — ship both builds. Works on legacy Atom tablets and modern workstations.
- **Statically linked (`/MT`)** — no runtime dependencies, no VCRedist needed.

---

## Quick Start

1. **Download** the appropriate `.exe` from [castangel.com/download/](https://castangel.com/download/) or the [GitHub Releases](../../releases) page.
2. **Double-click** the `.exe` on the PC you want to reach. It drops into the tray and starts two local ports.
3. **Open the URL** CastAngel shows you (e.g. `http://192.168.1.42:12377`) on any device on the same network.
4. **You're in** — full screen, mouse, keyboard, clipboard, and a file drop.

### Activation

When you first run CastAngel, it shows a **Machine ID**. Copy it, then go to [castangel.com/#pricing](https://castangel.com/#pricing) to purchase a license. After payment, you'll receive a license key by email — paste it into the activation window and you're done.

> **Free for churches** — forever free, no time limit. See [castangel.com/free-apply/](https://castangel.com/free-apply/).

---

## Download

| Version | Language | Architecture | Size |
|---------|----------|-------------|------|
| [CastAngel-CN-64.exe](../../releases/latest) | 中文 | 64-bit | ~1.5 MB |
| [CastAngel-CN-32.exe](../../releases/latest) | 中文 | 32-bit | ~1.25 MB |
| [CastAngel-EN-64.exe](../../releases/latest) | English | 64-bit | ~1.51 MB |
| [CastAngel-EN-32.exe](../../releases/latest) | English | 32-bit | ~1.26 MB |

> Download from **[GitHub Releases](../../releases/latest)** or **[castangel.com/download/](https://castangel.com/download/)**.

---

## Pricing

Pay once. Use forever. No subscriptions, no per-seat SaaS, no annual fees.

| Plan | Price | Devices | Features |
|------|-------|---------|----------|
| **Solo** | $29 | 1 | All features, email support, 14-day refund |
| **Pro** ⭐ | $49 | 5 | All features, boot auto-start, priority support |
| **Team** | $99 | 20 | All features, boot auto-start, priority support |

> Volume licensing & reseller terms — [sales@castangel.com](mailto:sales@castangel.com)

---

## How It Works

```
┌──────────────────────────────────────────────────┐
│  PC running CastAngel (.exe)                     │
│  ┌─────────────┐    ┌─────────────┐             │
│  │ Screen :12377│    │ Files :12399│             │
│  │ (WebSocket)  │    │ (HTTP)      │             │
│  └──────┬──────┘    └──────┬──────┘             │
│         │                  │                     │
│  ┌──────┴──────────────────┴──────┐             │
│  │        System Tray (blue)       │             │
│  └─────────────────────────────────┘             │
└──────────────────┬───────────────────────────────┘
                   │ LAN (same subnet)
    ┌──────────────┼──────────────┐
    │              │              │
┌───┴───┐    ┌────┴───┐    ┌─────┴──┐
│ Phone │    │ Tablet │    │ Laptop │
│Browser│    │Browser │    │Browser │
└───────┘    └────────┘    └────────┘
```

---

## Documentation

- **[Full Guide](https://castangel.com/guide/)** — step-by-step setup and usage
- **[FAQ](https://castangel.com/faq/)** — common questions and answers
- **[Screen Mirroring](https://castangel.com/screen-mirror/)** — detailed remote desktop docs
- **[File Transfer](https://castangel.com/file-transfer/)** — detailed file transfer docs
- **[EULA](https://castangel.com/eula/)** — end-user license agreement
- **[Privacy Policy](https://castangel.com/privacy/)** — privacy policy
- **[Blog](https://castangel.com/blog/)** — tutorials, tips, and updates

---

## System Requirements

- **OS**: Windows 7 SP1, 8, 8.1, 10, or 11
- **Architecture**: x86 (32-bit) or x64 (64-bit)
- **Network**: LAN/WiFi (same subnet as the viewer device)
- **Viewer**: Any modern browser (Chrome, Firefox, Edge, Safari, Opera)
- **No install, no admin rights, no runtime dependencies**

---

## FAQ

**Is CastAngel open source?**  
No. CastAngel is proprietary software with a one-time purchase model. Source code is not publicly available.

**Does CastAngel send any data to the cloud?**  
No. CastAngel is LAN-only by design. No cloud relay, no telemetry, no phone-home. Your machine ID never leaves your device.

**Can I use CastAngel over the internet?**  
CastAngel is designed for LAN use. For remote access over the internet, use a VPN or SSH tunnel to reach the same network.

**What's the refund policy?**  
14-day no-questions-asked refund. Email [78671932@qq.com](mailto:78671932@qq.com).

**Is it really free for churches?**  
Yes, forever free, no time limit, no feature gating. See [castangel.com/free-apply/](https://castangel.com/free-apply/) for details.

---

## Contact

- **Website**: [castangel.com](https://castangel.com)
- **Sales**: [sales@castangel.com](mailto:sales@castangel.com)
- **Support**: [78671932@qq.com](mailto:78671932@qq.com)
- **Issues**: Use GitHub Issues on this repository

---

## License

Proprietary. See [EULA](https://castangel.com/eula/) for details. All rights reserved.

Copyright © 2026 CastAngel. All rights reserved.