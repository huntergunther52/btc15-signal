# BTC15 Signal V2

Upgrade for the existing GitHub Pages app.

- Auto-discovers the current open Kalshi `KXBTC15M` market.
- Auto-loads the target and available YES price from Kalshi public market data.
- Attempts Kalshi `GET /live_data/events/{event_ticker}?range=15min` for the event underlying data.
- Explicitly labels Coinbase as **INDICATIVE** whenever Kalshi event live data is unavailable.
- Keeps the final-60-second accumulator, required remaining average, cushion, momentum, volatility, and experimental probability model.

Upload all five files to the root of the existing `btc15-signal` repository and replace the old versions.

**Important:** probability remains experimental/unvalidated. Feed source is shown in-app and must be checked before relying on settlement calculations.
