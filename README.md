# GSTD — decentralized AI compute on TON

Use AI in the main app, manage a TON-linked balance there, or run a compute node on your own hardware. GSTD is an early-stage, source-available project; the website and platform use Cloudflare, while compute runs on operators' hardware.

[![Website](https://img.shields.io/badge/site-gstdtoken.com-00d2ff?style=flat-square)](https://gstdtoken.com)
[![App](https://img.shields.io/badge/app-app.gstdtoken.com-0ea5e9?style=flat-square)](https://app.gstdtoken.com)
[![Telegram bot](https://img.shields.io/badge/Telegram-@gstdaibot-26a5e4?style=flat-square)](https://t.me/gstdaibot)
[![Channel](https://img.shields.io/badge/channel-@gstdtoken-26a5e4?style=flat-square)](https://t.me/gstdtoken)

The [public website](https://gstdtoken.com) explains the project, installation and documentation. The [app](https://app.gstdtoken.com/chat) is the workspace for model selection, chat, balance and rewards; the website demo is an optional introduction.

## Try it

- **Chat with the AI** — [@gstdaibot](https://t.me/gstdaibot) in Telegram, or the [main app chat](https://app.gstdtoken.com/chat).
- **Run a node** — `curl -fsSL https://raw.githubusercontent.com/gstdcoin/gstdbot/main/install.sh | bash`
- **Check the network** — [live stats](https://app.gstdtoken.com/api/v1/network/stats). They report current node and workload counters; counters do not prove an on-chain payout.

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

## Current release and payments

The compute node is on the 3.7 release line. Its default is local inference; sending a request to another node is an explicit choice. Operators earn **85%** of accepted paid work; **10%** goes to the protocol and **5%** to the reserve. There are no presence rewards or guaranteed hourly income.

Use [Payments](https://app.gstdtoken.com/payments) for backed balances, rewards and withdrawal requests. Blockchain payouts currently require the custody owner signature; the platform charges no additional GSTD withdrawal fee. Free and promotional requests do not create withdrawable GSTD.

[Release readiness and remaining gates](https://github.com/gstdcoin/ai/blob/main/docs/READINESS.md) distinguish tested code from end-to-end mainnet validation. The deployment currently has one physical compute node; multi-operator resilience is not established. Bridge and fine-tuning research are outside the production compute profile.
