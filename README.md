# BTC15 Signal V3

Mobile-first BTC 15-minute decision-support dashboard.

V3 uses the Cloudflare Worker at `btc15-api.huntergunther52.workers.dev/api/current` as the primary source for the open Kalshi `KXBTC15M` market, target, YES/NO asks, close time, and Kalshi event live-data samples.

Highlights:
- No manual target entry.
- Uses the market's actual `close_time`, not a locally guessed quarter-hour.
- Final-60-second running average and locked sample count.
- Required remaining average and live cushion.
- Kalshi YES/NO ask prices and experimental model edge.
- YES / NO / PASS gating: a directional signal requires >=62% model probability and >=8¢ estimated edge; otherwise PASS.
- Stale-data protection.
- Coinbase websocket is display-only fallback and is explicitly treated as indicative; it is never mixed into official final-60 settlement samples while Kalshi data is available.
- V3 service-worker cache invalidation so iPhone installs update cleanly.

Upload/replace all five files in the root of the `btc15-signal` GitHub repository. GitHub Pages should redeploy automatically.

Important: the probability model is experimental and unvalidated. This tool does not guarantee Kalshi settlement or trading profit.
