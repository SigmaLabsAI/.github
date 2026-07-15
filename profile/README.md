<div align="center">

<img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/banner.jpg" alt="insiders.bot" width="100%" />

<br/>

**The only Telegram bot & Webterminal you need for Polymarket.**

A real-time data engine that runs 10 to 20 seconds ahead of Polymarket, streaming every trade on-chain and mapping it to off-chain metadata, so you see the move before their own frontend does.

<br/>

[![Site](https://img.shields.io/badge/insiders.bot-1D4ED8?style=for-the-badge&logo=googlechrome&logoColor=white)](https://insiders.bot)
[![Docs](https://img.shields.io/badge/Docs-000000?style=for-the-badge&logo=gitbook&logoColor=white)](https://insidersbot.gitbook.io/insiders.bot)
[![Twitter](https://img.shields.io/badge/@insidersdotbot-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/insidersdotbot)
[![Telegram](https://img.shields.io/badge/@insiderscommunity-229ED9?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/insiderscommunity)

![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=flat-square&logo=clickhouse&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Polygon](https://img.shields.io/badge/Polygon-7B3FE4?style=flat-square&logo=polygon&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logo=socketdotio&logoColor=white)

</div>

---

<div align="center">

**$1,468,705+** volume routed, **2,963** traders, **hundreds of GBs** indexed, **~$0** streaming cost

</div>

---

## The wins


No words just pow ( proof of winning ). 

<div align="center">
  <img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/signals.jpg" alt="Pro Signals ranked by gain" width="100%" />
</div>


---

Our AI agent called the Portugal FIFA match (+350%) and the Congo match (+600%) live on stream, then suggested Canada to win with over 2.5 goals.

<div align="center">
  <img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/wins-ai.jpg" alt="insiders.bot AI agent predictions on stream" width="60%" />
</div>

---

## What we power

Everything below runs on the same real-time pipeline, on the web app, in the Telegram bot, and over our own WebSockets.

### Live markets + AI

Every Polymarket market, live and filterable (5-min crypto, politics, sports, geopolitics), with an AI you can ask in plain language to scan wallets, compare markets, or describe a trade.

<div align="center">
  <img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/home.jpg" alt="insiders.bot live markets and AI assistant" width="100%" />
</div>

### Live terminal

Full order book, real-time price, trade feed, take-profit / stop-loss, and returns-by-bet-size on any market, down to the second.

<div align="center">
  <img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/terminal.jpg" alt="insiders.bot live trading terminal" width="100%" />
</div>

### Wallet tracking

Every wallet on Polymarket, indexed and filterable by volume, PnL, ROI, win rate, trades and markets. **1.7M+ wallets, 2.4B+ trades.**

<div align="center">
  <img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/wallets.jpg" alt="insiders.bot wallet filter" width="100%" />
</div>

### Signals

Live bets from Polymarket's most profitable wallets, which smart wallets are buying which side, their win rates, avg entry and upside. Filterable by World, Politics, Geopolitics, Esports, Cricket, Finance and Crypto Launch.

<div align="center">
  <img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/signals-web.png" alt="insiders.bot signals, live bets from the most profitable wallets" width="100%" />
</div>

And delivered straight to Telegram, DMs and group topics, the moment they fire.

<div align="center">
  <img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/tg-signal.jpg" alt="insiders.bot Telegram signal" width="45%" />
</div>

---

## How we built it

Most people build on top of Polymarket's APIs, which sit 10 to 20 seconds behind the chain. We built underneath them.

Almost everything is already on-chain. You just can't use it until you connect the dots:

```
Asset IDs → Condition IDs → Market Titles → Outcome Names
```

Map that once, and you can stream the blockchain in real time instead of waiting on their APIs.

<div align="center">
  <img src="https://raw.githubusercontent.com/SigmaLabsAI/.github/main/profile/assets/architecture.jpg" alt="insiders.bot architecture, how we got 10 to 20 seconds ahead of Polymarket" width="90%" />
</div>

> Solid = live pipeline today. Dashed = legacy, since retired.

### The hardware
```
1x AMD Ryzen 9950X, 16c/32t, 4.3GHz
192GB DDR5
2x 4TB NVMe
```

### The RPCs
- Ethereum / Polygon, Alchemy
- Solana, Helius
- TON, their own APIs

Polymarket's own Polygon RPC is wide open, no rate limits, $0 cost. That became one of the biggest building blocks of the whole pipeline.

### The stream
We decode every buy, sell and fill on-chain in real time, which outcome, which condition id, and stitch it to the protocol's off-chain metadata.

### Store everything
Copy-trading isn't supposed to be possible on Polymarket. So we store it all, every trade, every wallet, every fill, every market, and build a schema that connects it. The DB runs to hundreds of GBs. Storage is cheap.

### Postgres to ClickHouse
Started on Postgres. Once queries hit *"markets traded by 1,000+ traders, under $1M volume, in a probability range"* over millions of markets, they took 60s+. ClickHouse brought them back in milliseconds, 100x to 1,000x faster on heavy aggregations.

### Hasura to our own APIs
Hasura gave us instant GraphQL/REST on Postgres and saved us weeks. ClickHouse didn't play the same way, so we built every API and WebSocket by hand.

---

## Stack

`Polygon RPC`, `Alchemy`, `Helius`, `PostgreSQL`, `ClickHouse`, custom `REST` + `WebSocket` APIs

---

<div align="center">

### Find us

**[insiders.bot](https://insiders.bot)**, **[Docs](https://insidersbot.gitbook.io/insiders.bot)**, **[@insidersdotbot](https://x.com/insidersdotbot)**, **[@insiderscommunity](https://t.me/insiderscommunity)**

</div>
