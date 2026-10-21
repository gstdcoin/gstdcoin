# GSTD — decentralized AI compute on TON

Ask an AI, link a TON wallet, and run a node on your own hardware. GSTD is an early-stage, source-available project; everything runs on Cloudflare's free tier.

[![Website](https://img.shields.io/badge/site-gstdtoken.com-00d2ff?style=flat-square)](https://gstdtoken.com)
[![App](https://img.shields.io/badge/app-app.gstdtoken.com-0ea5e9?style=flat-square)](https://app.gstdtoken.com)
[![Telegram bot](https://img.shields.io/badge/Telegram-@gstdaibot-26a5e4?style=flat-square)](https://t.me/gstdaibot)
[![Channel](https://img.shields.io/badge/channel-@gstdtoken-26a5e4?style=flat-square)](https://t.me/gstdtoken)

## Try it

- **Chat with the AI** — [@gstdaibot](https://t.me/gstdaibot) in Telegram, or [app.gstdtoken.com](https://app.gstdtoken.com).
- **Run a node** — `curl -fsSL https://raw.githubusercontent.com/gstdcoin/gstdbot/main/install.sh | bash`
- **Check the network** — [live stats](https://app.gstdtoken.com/api/v1/network/stats). They are the source of truth for nodes, tasks and payouts.

## Repositories

| Repository | What it is |
|---|---|
| [web](https://github.com/gstdcoin/web) | Public website — Next.js on Cloudflare Workers, EN/RU |
| [ai](https://github.com/gstdcoin/ai) | Platform app, node/task API, network stats and the Telegram bot |
| [gstdbot](https://github.com/gstdcoin/gstdbot) | Node software: install, heartbeats, inference tasks, sovereign core |
| [A2A](https://github.com/gstdcoin/A2A) | Experimental clients and a local MCP server for AI agents |
| [contracts](https://github.com/gstdcoin/contracts) | TON smart contracts in Tact (partially deployed, unaudited) |
| [gstd-bridge](https://github.com/gstdcoin/gstd-bridge) | Bridge research scaffold (deferred, not deployed) |

## Principles

- **Honest numbers.** No invented nodes, tasks or earnings. When the network is empty, the site and the bot say so.
- **No promises of income.** Rewards depend on real demand and are not guaranteed; nothing here is investment advice.
- **Source-available.** Code is under the PolyForm Noncommercial License with a permission for taking part in the network.
