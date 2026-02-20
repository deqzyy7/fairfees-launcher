# FairFees Launcher

Token launcher for PumpFun with FairFees branding. Create tokens where creator fees are redistributed fairly to holders.

## How it works

1. Connect your Phantom wallet
2. Fill in token details (name, symbol, description, image)
3. Click "Launch Token" and approve the transaction in Phantom
4. Your token goes live on PumpFun

## Prerequisites

- [Phantom wallet](https://phantom.app/) browser extension
- SOL in your wallet (minimum ~0.02 SOL for transaction fees)

## Usage

Open `index.html` in your browser, or deploy to any static hosting (GitHub Pages, Vercel, Netlify).

## FairFees Integration

After launching your token, configure the [FairFees Bot](https://github.com/deqzyy7/bot-lelu) with your token's mint address to enable automatic creator fee redistribution to holders.

## Technical Details

- **Client-side only** — no backend, no API keys needed
- **Metadata upload** via PumpFun IPFS endpoint
- **Transaction building** via PumpPortal Local API
- **Signing** via Phantom wallet adapter
- **CDN dependency**: `@solana/web3.js` v1.98.0

## Security

- No private keys are stored or transmitted
- All transactions are signed locally in your Phantom wallet
- The mint keypair is generated client-side and never leaves the browser
