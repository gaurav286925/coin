# CoinCart — React + Vite storefront demo

A responsive ecommerce frontend prototype with product browsing, search and filters, product detail pages, cart, checkout, simulated Google sign-in, order history, and a coins wallet.

## Run locally

Requires Node.js 20.19+ (or 22.12+).

```bash
npm install
npm run dev
```

Open the local URL printed by Vite.

## Deploy using GitHub + Vercel

1. Create a new GitHub repository, e.g. `coincart`.
2. Upload **all files and folders inside this project** to the repository root (`src/`, `index.html`, `package.json`, `vite.config.js`, etc.). Do not upload `node_modules`.
3. Go to https://vercel.com/new and import your GitHub repository.
4. Vercel should detect Vite. Set framework **Vite**, build command **npm run build**, and output directory **dist** if not auto-filled.
5. Click **Deploy**. Subsequent pushes to GitHub will trigger new deployments.

## Coin behavior

Demo orders award coins equal to the sum of product prices multiplied by quantities. Delivery is free in this demo. Cart, demo user, order history, and coins are persisted in the current browser via `localStorage`. There is **no coin redemption feature** yet.

## IMPORTANT — frontend demo only

- The "Continue with Google" button is a **simulated login**. It does not contact Google or authenticate anyone.
- Checkout and payment methods are **simulated**. No real payment occurs.
- Coin balance is **not secure**: it is derived from demo orders saved in the browser, and browser storage can be edited by users.
- Orders are not transmitted to a server, and browser data does not sync across devices.
- Before production launch, implement real Google OAuth, backend authentication, product inventory, verified payment webhooks, order management, a transactional coin ledger, refund/reversal handling, fraud controls, and legal/compliance review of rewards and redemption.

## Project layout

```
index.html
src/
  main.jsx    React UI, navigation, cart, checkout and demo order state
  data.js     Sample catalog
  style.css   Responsive styling
vite.config.js
vercel.json
```

Change products and prices in `src/data.js`. Adjust branding/colors in `src/style.css`.
