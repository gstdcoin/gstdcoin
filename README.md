# GSTD — decentralized AI compute on TON

[Project map / Карта проекта](https://github.com/gstdcoin/ai/blob/main/docs/INDEX.md) · [Release evidence](https://github.com/gstdcoin/ai/blob/main/docs/READINESS.md) · [Repository maintenance](https://github.com/gstdcoin/ai/blob/main/docs/REPOSITORY_MAINTENANCE.md)

Default branch: `main`.

Use AI in the main app, manage a TON-linked balance there, or run a compute node on your own hardware. GSTD is an early-stage, source-available project; the website and platform use Cloudflare, while compute runs on operators' hardware.

[![Website](https://img.shields.io/badge/site-gstdtoken.com-00d2ff?style=flat-square)](https://gstdtoken.com)
[![App](https://img.shields.io/badge/app-app.gstdtoken.com-0ea5e9?style=flat-square)](https://app.gstdtoken.com)
[![Telegram bot](https://img.shields.io/badge/Telegram-@gstdaibot-26a5e4?style=flat-square)](https://t.me/gstdaibot)
[![Channel](https://img.shields.io/badge/channel-@gstdtoken-26a5e4?style=flat-square)](https://t.me/gstdtoken)

The [public website](https://gstdtoken.com) explains the project, installation and documentation. The [app](https://app.gstdtoken.com/chat) is the workspace for model selection, chat, balance and rewards; the website demo is an optional introduction.

[Start here / Начните здесь](https://gstdtoken.com/docs#get-started) · [Detailed bilingual guide](https://github.com/gstdcoin/ai/blob/main/docs/START_HERE.md)

## Try it

- **Chat with the AI** — [@gstdaibot](https://t.me/gstdaibot) in Telegram, or the [main app chat](https://app.gstdtoken.com/chat).
- **Run a node / Запустить ноду** — start with the [operator guide](https://github.com/gstdcoin/gstdbot/blob/main/docs/OPERATOR_PANEL.md) and [signed release status](https://github.com/gstdcoin/ai/blob/main/docs/SIGNED_NODE_RELEASES.md).
- **Check the network** — [live stats](https://app.gstdtoken.com/api/v1/network/stats). They report current node and workload counters; counters do not prove an on-chain payout.

## Repositories

| Репозиторий / Repository | Назначение / Purpose | Документация / Docs |
| --- | --- | --- |
| [gstdcoin](https://github.com/gstdcoin/gstdcoin) | Навигация по проекту / Project profile and navigation | [Пошаговое руководство / Start here](https://github.com/gstdcoin/ai/blob/main/docs/START_HERE.md) |
| [web](https://github.com/gstdcoin/web) | Публичный сайт, справка и демо / Public website, guides and demo | [README](https://github.com/gstdcoin/web#readme) |
| [ai](https://github.com/gstdcoin/ai) | Приложение Cloudflare, реестр, платёжный учёт и Telegram / Platform, registry, ledger, escrow and Telegram webhook | [Карта платформы / Platform guide](https://github.com/gstdcoin/ai/blob/main/docs/INDEX.md) |
| [gstdbot](https://github.com/gstdcoin/gstdbot) | Вычислительная нода Ollama и панель оператора / Ollama compute node and operator dashboard | [Руководство оператора / Operator guide](https://github.com/gstdcoin/gstdbot/blob/main/docs/OPERATOR_PANEL.md) |
| [contracts](https://github.com/gstdcoin/contracts) | Исходники TON-контрактов, Sandbox-тесты и записи развёртывания / TON sources, Sandbox tests and deployment records | [Текущий статус / Deployment status](https://github.com/gstdcoin/contracts#source-and-deployment-status) |
| [A2A](https://github.com/gstdcoin/A2A) | Экспериментальные клиенты и локальный MCP / Experimental clients and local MCP connector | [SDK and MCP setup](https://github.com/gstdcoin/A2A#readme) |
| [gstd-bridge](https://github.com/gstdcoin/gstd-bridge) | Отложенное исследование моста, без действующих переводов / Deferred bridge research without a live transfer service | [Ограничения / Research status](https://github.com/gstdcoin/gstd-bridge#readme) |

## Principles

- **Honest numbers.** No invented nodes, tasks or earnings. When the network is empty, the site and the bot say so.
- **No promises of income.** Rewards depend on real demand and are not guaranteed; nothing here is investment advice.
- **Clear usage rights.** Core repositories are source-available under PolyForm Noncommercial with a commercial GSTD network permission. The A2A client SDK is separately licensed under Apache-2.0.

## Current release and payments

The compute node is on the 3.7 release line. Its default is local inference; sending a request to another node is an explicit choice. Operators earn **85%** of accepted paid work; **10%** goes to the protocol and **5%** to the reserve. There are no presence rewards or guaranteed hourly income.

Use [Payments](https://app.gstdtoken.com/payments) for backed balances, rewards and withdrawal requests. Platform-ledger payouts require the custody owner signature. The separate [mainnet escrow open beta](https://app.gstdtoken.com/escrow-mainnet) uses per-job contracts and beneficiary-signed claims; contract funds do not migrate to the platform balance. A real mainnet payout is still unverified. There is no additional GSTD claim/withdrawal fee; signers pay TON network fees. Free and promotional requests do not create withdrawable GSTD.

[Release readiness and remaining gates](https://github.com/gstdcoin/ai/blob/main/docs/READINESS.md) distinguish tested code from end-to-end mainnet validation. The live registry reports current node counts; independent multi-operator resilience is not established. Bridge and fine-tuning research are outside the production compute profile.

## Release evidence checked on 2026-11-18

| Component | Published state and evidence |
| --- | --- |
| Platform | [Private preview and RPC deployment](https://github.com/gstdcoin/ai/actions/runs/44257765512/attempts/2) passed. Live health reported Redis and the catalog reported `rpc_configured:true`. |
| Compute node source | [Node PR 11](https://github.com/gstdcoin/gstdbot/pull/11) merged; [main CI](https://github.com/gstdcoin/gstdbot/actions/runs/44256785028), installer and container smoke checks passed. |
| Signed node manifest | Version 3.7.2, approved commit `ccf459c`; its public Ed25519 signature was verified. This is separate from newer main-branch source and an installed daemon. |
| Escrow v2 | [Contracts PR 7](https://github.com/gstdcoin/contracts/pull/7) merged; [75-test CI](https://github.com/gstdcoin/contracts/actions/runs/44252837614) and [public Testnet receipts](https://github.com/gstdcoin/contracts/blob/master/docs/ESCROW_V2_TESTNET.md) are available. Mainnet activation is separate. |
| Website | [Website PR 11](https://github.com/gstdcoin/web/pull/11) merged; [Cloudflare deployment](https://github.com/gstdcoin/web/actions/runs/44244093547) passed. |

Open proposals are tracked in one [repository maintenance and review queue](https://github.com/gstdcoin/ai/blob/main/docs/REPOSITORY_MAINTENANCE.md). A proposal, source merge, signed release and production deployment are different states. [Readiness](https://github.com/gstdcoin/ai/blob/main/docs/READINESS.md) records the remaining mainnet, operator and recovery checks.

## Licensing across the ecosystem

| Component | Current first-party code terms |
| --- | --- |
| [Node](https://github.com/gstdcoin/gstdbot/blob/main/LICENSE), [platform](https://github.com/gstdcoin/ai/blob/main/LICENSE), [website](https://github.com/gstdcoin/web/blob/main/LICENSE), [contracts](https://github.com/gstdcoin/contracts/blob/master/LICENSE), [deferred bridge](https://github.com/gstdcoin/gstd-bridge/blob/main/LICENSE) | PolyForm Noncommercial plus a common commercial network/app permission. Covered paid network compute settles in canonical GSTD. |
| [A2A SDK](https://github.com/gstdcoin/A2A/blob/master/LICENSE) | Apache-2.0 for first-party client code; no mandatory token condition imposed by the SDK license. |

Companies and individuals can build commercial integrations under the relevant permission without individual approval. The GSTD condition does not charge for installation, local execution, free requests or model downloads; TON gas and unrelated business fees remain separate. Bundling paid network compute does not exempt its underlying GSTD settlement.

Third-party code, dependencies, models and assets retain their own licenses. Earlier releases retain their earlier licenses. These terms cannot force independent implementations to use GSTD, do not promise earnings, and do not make any undeployed financial feature operational. This overview does not replace or relicense the linked repositories.

The first-party overview text in this index repository is available under [Apache-2.0](LICENSE), with [notices](NOTICE). This does not grant rights to linked code or third-party materials.
