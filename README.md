<div align="center">

```
███████╗██╗   ██╗███╗   ██╗████████╗██╗  ██╗███████╗██╗  ██╗
╚══███╔╝╚██╗ ██╔╝████╗  ██║╚══██╔══╝██║  ██║██╔════╝╚██╗██╔╝
  ███╔╝  ╚████╔╝ ██╔██╗ ██║   ██║   ███████║█████╗   ╚███╔╝ 
 ███╔╝    ╚██╔╝  ██║╚██╗██║   ██║   ██╔══██║██╔══╝   ██╔██╗ 
███████╗   ██║   ██║ ╚████║   ██║   ██║  ██║███████╗██╔╝ ██╗
╚══════╝   ╚═╝   ╚═╝  ╚═══╝   ╚═╝   ╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝
```

<h3>Zynthex — A feature-rich Discord bot paired with a sleek Next.js dashboard</h3>
<p><b>Developed & Owned by AD Development (zyro)</b></p>

<p>
  <a href="https://python.org"><img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white"/></a>
  <a href="https://nextjs.org"><img src="https://img.shields.io/badge/Next.js-14+-000000?style=for-the-badge&logo=nextdotjs&logoColor=white"/></a>
  <a href="https://fastapi.tiangolo.com"><img src="https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi&logoColor=white"/></a>
  <a href="https://discordpy.readthedocs.io"><img src="https://img.shields.io/badge/Discord.py-v2-5865F2?style=for-the-badge&logo=discord&logoColor=white"/></a>
</p>
<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge"/></a>
  <a href="https://discord.gg/zynthex"><img src="https://img.shields.io/badge/Discord-Zynthex-5865F2?style=for-the-badge&logo=discord&logoColor=white"/></a>
</p>

</div>

---

## ✦ Overview

**Zynthex** is an all-in-one Discord bot and security engine built with a modern Next.js 14 web dashboard. Created and maintained by **zyro**, it provides security, antinuke, moderation, music, ticketing, verification, join-to-create voice channels, and live metrics.

```
Zynthex-AIO-With-Dashboard/
├── 🤖  bot/                   Python Discord bot + FastAPI backend
│   ├── api/                   Dashboard REST API (FastAPI)
│   ├── cogs/                  All bot features (commands, events, antinuke, automod…)
│   ├── core/                  Bot client, context, cog base
│   ├── utils/                 Shared utilities (config, emoji, tools, cloudflare tunnel…)
│   ├── Zynthex.py             Main Bot Entry Point
│   └── CodeX.py               Compatibility Entry Point
│
└── 🌐  dashboard/             Next.js frontend
    ├── app/                   App Router pages & API routes
    ├── components/            Reusable UI components
    ├── hooks/                 Custom React hooks
    ├── lib/                   API helpers & utilities
    └── types/                 TypeScript type definitions
```

---

## ✦ APIs Needed to Run the Bot

To fully run **Zynthex** and its web dashboard, the following APIs and external service integrations are required:

| API / Integration | Environment Variable(s) | Description |
| :--- | :--- | :--- |
| **Discord Bot Token API** | `TOKEN` | Discord Gateway and API authentication token for the bot client. |
| **Lavalink Music API** | `LAVALINK_HOST`, `LAVALINK_PASSWORD`, `LAVALINK_PORT`, `LAVALINK_SECURE` | Lavalink v4 node connection for audio streaming and music playback commands. |
| **Spotify Web API** | `SPOTIFY_CLIENT_ID`, `SPOTIFY_CLIENT_SECRET` | Required for Spotify track, album, and playlist resolution in music commands. |
| **Discord OAuth2 API** | `DISCORD_CLIENT_ID`, `DISCORD_CLIENT_SECRET` | Used by the Next.js web dashboard to log users in with Discord credentials. |
| **Dashboard REST API & Key** | `API_PORT`, `API_ENABLED`, `DASHBOARD_API_KEY`, `NEXT_PUBLIC_API_URL`, `NEXT_PUBLIC_DASHBOARD_API_KEY`, `NEXTAUTH_SECRET` | Secure REST API bridge connecting the bot backend to the Next.js dashboard. |
| **Discord Webhooks API** | `WEBHOOK_URL`, `CMD_WEBHOOK_URL` | Used for logging command execution, guild updates, and error alerts. |
| **Cloudflare Tunnel API** | `TUNNEL_ENABLED`, `CF_TUNNEL_TOKEN`, `CF_TUNNEL_URL` | Cloudflared connector tunnel providing secure public HTTPS endpoints for the API server. |

---

## ✦ Features

- **🛡️ Security & Antinuke**: Anti-ban, anti-kick, anti-channel/role flood, anti-webhook, anti-bot add, anti-prune, and emergency lockdown.
- **🎵 Music**: Powered by Lavalink v4 & Spotify Web API with queue, loop, shuffle, search, and controls.
- **⚙️ Management**: Moderation, ticketing system, join-to-create channels, reaction roles, vanity roles, invite tracker, and verification.
- **🌐 Web Dashboard**: Real-time server management via Next.js 14, NextAuth Discord OAuth2, and FastAPI backend.

---

## ✦ Getting Started

### 1. Bot Setup
```bash
cd bot
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your TOKEN, SPOTIFY_CLIENT_ID, LAVALINK details, etc.
python Zynthex.py
```

### 2. Dashboard Setup
```bash
cd dashboard
npm install
cp .env.example .env
# Edit .env with DISCORD_CLIENT_ID, DISCORD_CLIENT_SECRET, NEXTAUTH_SECRET, etc.
npm run dev
```

---

## ✦ License & Ownership

Developed and owned by **AD Development** (zyro).
Licensed under the [Proprietary & Confidential License](LICENSE) — Copyright (c) 2026 **AD Development**. All Rights Reserved.
