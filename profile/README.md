<div align="center">

<img width="1200" height="630" alt="carbium services: one API key for Solana RPC, WebSocket, Carbon Stream and a quote API" src="https://raw.githubusercontent.com/carbium-sh/.github/main/profile/banner.png" />

# Carbium

<h1 align="center">Solana APIs behind one key</h1>
<h2 align="center">RPC, WebSocket, Carbon Stream and a quote API for developers</h2>

<p align="center">
  <img alt="Solana" src="https://img.shields.io/badge/-Solana-000000?style=flat-square&logo=solana&logoColor=14F195">
  <img alt="RPC" src="https://img.shields.io/badge/-RPC-8b2fbf?style=flat-square">
  <img alt="DAS" src="https://img.shields.io/badge/-DAS-4f4ab8?style=flat-square">
  <img alt="WebSocket" src="https://img.shields.io/badge/-WebSocket-1e71ab?style=flat-square">
  <img alt="Carbon Stream" src="https://img.shields.io/badge/-Carbon%20Stream-c4221f?style=flat-square">
  <img alt="Quote API" src="https://img.shields.io/badge/-Quote%20API-8a6a1c?style=flat-square">
  <img alt="Webhooks" src="https://img.shields.io/badge/-Webhooks-3C3C3D?style=flat-square">
</p>

<p align="center">
  <a href="https://carbium.sh"><img alt="carbium.sh" src="https://img.shields.io/badge/carbium.sh-get%20a%20key-8b2fbf?style=flat-square"></a>
  <a href="https://carbium.sh/docs"><img alt="Docs" src="https://img.shields.io/badge/docs-carbium.sh%2Fdocs-0e0e0e?style=flat-square"></a>
  <a href="https://carbium.sh/skill.md"><img alt="skill.md" src="https://img.shields.io/badge/for%20agents-skill.md-0e0e0e?style=flat-square"></a>
  <a href="https://carbium.sh/llms.txt"><img alt="llms.txt" src="https://img.shields.io/badge/for%20agents-llms.txt-0e0e0e?style=flat-square"></a>
  <a href="https://carbium.sh/openapi.json"><img alt="openapi.json" src="https://img.shields.io/badge/account%20API-openapi.json-0e0e0e?style=flat-square&logo=openapiinitiative&logoColor=white"></a>
</p>

</div>

## Introduction

Carbium gives developers API access to Solana mainnet behind one key: JSON-RPC, WebSocket subscriptions, a
Yellowstone gRPC stream and a quote API that returns prices and unsigned transactions for your app to sign.
Plans are monthly and you can start on the free one.

## Services

| | |
|---|---|
| RPC | JSON-RPC 2.0 over HTTPS at `https://services.carbium.sh`, with the DAS methods on the same endpoint. |
| WebSocket | JSON-RPC subscriptions for accounts, programs, logs, signatures, slots and blocks at `wss://services.carbium.sh`. |
| Carbon Stream | Yellowstone gRPC at `https://services.carbium.sh:9443`, on the DEV, BUSINESS and PRO plans. It works with the standard Yellowstone clients. |
| Quote API | `quote`, `swap`, `prices` and `health` on the RPC endpoint. A swap comes back as an unsigned transaction that your own wallet signs. |
| Webhooks | A signed HTTPS POST for each finalized transaction that touches an address you list, on the DEV, BUSINESS and PRO plans. |
| Account API | Keys, webhooks and usage managed by API with an account key, described in [openapi.json](https://carbium.sh/openapi.json). |

### First call

```bash
curl -s https://services.carbium.sh \
  -H 'content-type: application/json' -H "x-api-key: $CARBIUM_KEY" \
  -d '{"jsonrpc":"2.0","id":1,"method":"getSlot"}'
```

Get a key at [carbium.sh](https://carbium.sh). The [docs](https://carbium.sh/docs) list every method with its limits and errors.

## For AI agents

[skill.md](https://carbium.sh/skill.md) is the whole API as one markdown skill for a coding agent, and
[llms.txt](https://carbium.sh/llms.txt) is the short index. An agent that holds a Solana keypair can sign up and
read its API key over HTTPS, with no browser and no inbox. Plans and prices are served as JSON at
[carbium.sh/v1/plans](https://carbium.sh/v1/plans).

## Our code

Our SDKs, CLI and agent tools are published in this organisation as they are released.

## Contact

[carbium.sh](https://carbium.sh) · [Docs](https://carbium.sh/docs) · support@carbium.sh

<p align="center">© 2026 Carbium</p>
