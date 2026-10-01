# BTC15 Signal — iPhone PWA MVP

This is a mobile-first installable web app for 15-minute BTC market analysis.

## What works now
- Live BTC-USD indicative feed from Coinbase Advanced Trade WebSocket
- Quarter-hour countdown
- Manual Kalshi target + YES price
- Final-60-second running average from one-second samples
- Remaining-average break-even calculation
- 15-second momentum and short volatility
- Approximate probability + model-vs-market edge
- PWA/Home Screen support

## Critical limitation
Kalshi's official crypto settlement uses the average of 60 one-second CF Benchmarks RTI observations during the expiration minute. This MVP uses Coinbase BTC-USD and MUST NOT be treated as the official settlement feed.

## Put it on your iPhone
The app must be served over HTTPS for Home Screen/PWA behavior.
1. Upload this folder to any static HTTPS host (GitHub Pages, Cloudflare Pages, Netlify, Vercel, etc.).
2. Open the HTTPS URL in Safari on iPhone.
3. Share -> Add to Home Screen.

No Kalshi private API key is stored in this build.
