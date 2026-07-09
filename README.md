# NexaPay Landing

This repository contains the public landing page for NexaPay.

NexaPay is a mobile-first payment application designed for African mobile money workflows. It helps users manage multiple mobile money wallets, send money, recharge airtime, pay bills, scan merchant QR codes, and follow transaction history from one clear interface.

## Public Website

The website is a static GitHub Pages landing page:

```text
https://rolln7drktayau.github.io/NexaPayLanding/
```

If the URL returns `404` after a fresh push, enable GitHub Pages:

```text
Settings -> Pages -> Deploy from a branch -> main / root
```

## What NexaPay Covers

- Multiple mobile money wallets by country and operator.
- Wallet selection before transfers, top-ups, bills, and merchant payments.
- QR payment flow for merchants and wallet-based receive codes.
- Bill payment flow with verification before payment.
- Airtime recharge using the user's own wallets as payment sources.
- Transfer history with detailed transaction information.
- Demo mode with fictive balances and simulated operations.
- Privacy-first architecture: payment provider secrets stay on the backend.

## Payment Channels

NexaPay distinguishes between payment routes:

- Same-operator or local operator flows can prepare USSD codes when appropriate.
- Inter-operator, merchant, bill, and provider-backed flows are expected to pass through the backend and Maviance/SmobilPay S3P where supported.
- The mobile app must not embed Maviance secrets or signing keys.

## Maviance Technical Report

A technical report for Maviance is available here:

```text
maviance_partner_report_fr.pdf
```

The report focuses only on the staging S3P signature issue observed during integration tests.

## Files

- `index.html` - public landing page.
- `privacy.html` - privacy policy page.
- `maviance_partner_report_fr.pdf` - technical report for Maviance.
- `.nojekyll` - disables Jekyll processing on GitHub Pages.

## Security Note

This repository must remain public-only. Do not add:

- Flutter source code.
- Backend source code.
- Firebase configuration.
- Maviance credentials.
- `.env` files.
- internal `todo/` or `maviance/` folders.
- APK signing keys or private documents.
