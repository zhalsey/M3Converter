# M3 Converter

**[m3converter.com](https://m3converter.com)** — Convert $/MBF to Currency/M³ with live exchange rates.

A fast, single-page tool for lumber traders to convert US Dollar per thousand board feet ($/MBF) pricing into any major world currency per cubic meter.

## Features

- **20 currencies** — EUR, CAD, GBP, JPY, CNY, AUD, NZD, SEK, NOK, CHF, MXN, BRL, INR, KRW, IDR, MYR, SGD, ZAR, PLN, TRY
- **Live exchange rates** from ECB via Frankfurter API, with 3 fallback API sources
- **Toggle currencies** on/off — preferences saved in localStorage
- **Clear error states** — no conversions shown until live rates load; stale rate warnings
- **Mobile-optimized** — large touch targets, numeric keyboard, responsive layout
- **Zero dependencies** — single HTML file, no build step

## Conversion

Uses the NHLA standard nominal board foot conversion:

- 1 Board Foot = 144 in³
- 1 M³ = 61,023.84 in³
- **1 M³ = 423.78 BF**
- **1 MBF = 2.3597 M³**

## Exchange Rate Sources (tried in order)

1. [Frankfurter API](https://api.frankfurter.dev) (ECB reference rates)
2. [Frankfurter mirror](https://api.frankfurter.app)
3. [ExchangeRate-API](https://open.er-api.com) (open access)
4. [Currency-API CDN](https://github.com/fawazahmed0/exchange-api) (jsDelivr)

Rates are ECB daily reference midpoints updated ~16:00 CET. **For indicative use only — verify rates with your bank before executing trades.**

## Deploy

Static site — deploy anywhere. Designed for Vercel:

```bash
# Push to GitHub, connect to Vercel, point m3converter.com DNS
```

No environment variables, no API keys, no server-side code.

## Related Tools

- [LumberNumber.com](https://lumbernumber.com) — Lumber conversion calculator
- [LumberMargin.com](https://lumbermargin.com) — Margin & pricing calculator
