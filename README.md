# Central Bank of Turkmenistan Exchange Rates API — central-bank-of-turkmenistan-exchange-rate

[![npm version](https://img.shields.io/npm/v/central-bank-of-turkmenistan-exchange-rate.svg)](https://www.npmjs.com/package/central-bank-of-turkmenistan-exchange-rate)
[![license](https://img.shields.io/npm/l/central-bank-of-turkmenistan-exchange-rate.svg)](https://github.com/AllRates-Today/central-bank-of-turkmenistan-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/central-bank-of-turkmenistan-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![USD/TMT today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fcbt%3Fsource%3DUSD%26target%3DTMT&query=%24.rate&label=USD%2FTMT%20published%20by%20Central%20Bank%20of%20Turkmenistan&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/cbt/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fcbt%3Fsource%3DUSD%26target%3DTMT&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/cbt/)

**Official Central Bank of Turkmenistan (Turkmenistan) daily exchange rates for Node.js and TypeScript. The published central bank rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers Central Bank of Turkmenistan itself prints, every business day.**

## 🚀 Why this client?

- 🏛️ **Official published rates** — Central Bank of Turkmenistan's own table, with the publisher's own `rate_date` on every response
- 📅 **History back to 2009** — point-in-time tables and daily series for any past date
- 🔀 **Published vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number Central Bank of Turkmenistan itself published, fixed once printed and carrying the central bank's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## ⚡ Try it without a key

The latest Central Bank of Turkmenistan table is also served keyless, CORS-open and edge-cached, for evaluation, embeds and AI agents:

```bash
curl "https://allratestoday.com/api/open/central-bank/cbt?source=USD&target=TMT"
```

```js
const r = await fetch('https://allratestoday.com/api/open/central-bank/cbt').then((x) => x.json());
console.log(r.rate_date, r.rates.length); // the central bank's latest published table, no key
```

The open endpoint serves the *latest* table only and asks for a visible attribution link. The client below uses the keyed API, which adds point-in-time tables, history, and CSV/XML/Excel output.

## 📈 Latest published table

Today's full Central Bank of Turkmenistan table, straight from the central bank's latest publication. On GitHub it is refreshed by [a daily Action](.github/workflows/daily-table.yml) that reads the keyless endpoint above and commits only when the central bank publishes a new table; the copy on npm is as of the package's publish date.

<!-- daily-table:start -->
Published **2026-10-09** by Central Bank of Turkmenistan — 47 rates. Updated 2026-10-09.

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| AED | TMT | reference | 0.953 |
| AFN | TMT | reference | 0.054046 |
| AMD | TMT | reference | 0.009722 |
| AUD | TMT | reference | 2.4346 |
| AZN | TMT | reference | 2.0649 |
| BYN | TMT | reference | 1.1421 |
| CAD | TMT | reference | 2.4549 |
| CHF | TMT | reference | 4.1946 |
| CNY | TMT | reference | 0.5222 |
| CZK | TMT | reference | 0.1605 |
| DKK | TMT | reference | 0.524 |
| EGP | TMT | reference | 0.0669 |
| EUR | TMT | reference | 3.9158 |
| GBP | TMT | reference | 4.6176 |
| GEL | TMT | reference | 1.3645 |
| HKD | TMT | reference | 0.446 |
| ILS | TMT | reference | 1.1384 |
| INR | TMT | reference | 0.036161 |
| IRR | TMT | reference | 0.00000198 |
| JPY | TMT | reference | 0.022122 |
| KGS | TMT | reference | 0.040023 |
| KRW | TMT | reference | 0.0026044 |
| KWD | TMT | reference | 11.3599 |
| KZT | TMT | reference | 0.007785 |
| MDL | TMT | reference | 0.1969 |
| MKD | TMT | reference | 0.063799 |
| MMK | TMT | reference | 0.001672 |
| MOP | TMT | reference | 0.433 |
| MRU | TMT | reference | 0.08755 |
| MYR | TMT | reference | 0.8562 |
| NOK | TMT | reference | 0.3658 |
| PKR | TMT | reference | 0.012645 |
| PLN | TMT | reference | 0.8946 |
| QAR | TMT | reference | 0.9602 |
| RON | TMT | reference | 0.7322 |
| RUB | TMT | reference | 0.040864 |
| SAR | TMT | reference | 0.9323 |
| SEK | TMT | reference | 0.3497 |
| SGD | TMT | reference | 2.7307 |
| THB | TMT | reference | 0.104012 |
| TJS | TMT | reference | 0.3813 |
| TRY | TMT | reference | 0.0711 |
| TWD | TMT | reference | 0.109642 |
| UAH | TMT | reference | 0.078 |
| USD | TMT | reference | 3.5 |
| UZS | TMT | reference | 0.0002966 |
| XDR | TMT | reference | 4.7327 |

Source: [Official rates published by CBT, served by AllRatesToday](https://allratestoday.com/central-bank-rates-api/cbt/). Rates are as printed by the central bank; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## 📦 Installation

```bash
npm install central-bank-of-turkmenistan-exchange-rate
```

```bash
yarn add central-bank-of-turkmenistan-exchange-rate
```

```bash
pnpm add central-bank-of-turkmenistan-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/central-bank-of-turkmenistan-exchange-rate`](https://www.npmjs.com/package/@allratestoday/central-bank-of-turkmenistan-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'central-bank-of-turkmenistan-exchange-rate';

const pair = await getRate('USD', 'TMT', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official Central Bank of Turkmenistan rate, on the central bank's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest published table
- [Full published table](#full-published-table) — everything the central bank printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the central bank does not print directly are resolved from its table and flagged (see *Published vs derived rates* below).

```js
const pair = await getRate('USD', 'TMT', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'cbt',
  name: 'Central Bank of Turkmenistan',
  rate_date: '2026-10-08',   // Central Bank of Turkmenistan's own publication date
  source: 'USD',
  target: 'TMT',
  rate: 3.5,
  rate_type: 'reference',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full published table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'central-bank-of-turkmenistan-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'cbt',
  name: 'Central Bank of Turkmenistan',
  rate_date: '2026-10-08',
  rates: [
    { "base": "USD", "quote": "TMT", "type": "reference", "value": 3.5 },
    // … the rest of the published table (48 currencies vs TMT)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 2009 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'central-bank-of-turkmenistan-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'USD', target: 'TMT' });
```

**Response:**

```javascript
{
  bank: 'cbt',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'central-bank-of-turkmenistan-exchange-rate';

const series = await getHistory(
  { source: 'USD', target: 'TMT', from: '2026-01-01', to: '2026-10-08' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'cbt',
  source: 'USD',
  target: 'TMT',
  from: '2026-01-01',
  to: '2026-10-08',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-10-08', rate: 3.5, rate_type: 'reference', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'USD' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

Central Bank of Turkmenistan currently publishes rates covering **48 currencies** against the TMT (as of the latest table):

🇦🇪 `AED` · 🇦🇫 `AFN` · 🇦🇲 `AMD` · 🇦🇺 `AUD` · 🇦🇿 `AZN` · 🇧🇾 `BYN` · 🇨🇦 `CAD` · 🇨🇭 `CHF` · 🇨🇳 `CNY` · 🇨🇿 `CZK` · 🇩🇰 `DKK` · 🇪🇬 `EGP` · 🇪🇺 `EUR` · 🇬🇧 `GBP` · 🇬🇪 `GEL` · 🇭🇰 `HKD` · 🇮🇱 `ILS` · 🇮🇳 `INR` · 🇮🇶 `IQD` · 🇮🇷 `IRR` · 🇯🇵 `JPY` · 🇰🇬 `KGS` · 🇰🇷 `KRW` · 🇰🇼 `KWD` · 🇰🇿 `KZT` · 🇲🇩 `MDL` · 🇲🇰 `MKD` · 🇲🇲 `MMK` · 🇲🇴 `MOP` · 🇲🇷 `MRU` · 🇲🇾 `MYR` · 🇳🇴 `NOK` · 🇵🇰 `PKR` · 🇵🇱 `PLN` · 🇶🇦 `QAR` · 🇷🇴 `RON` · 🇷🇺 `RUB` · 🇸🇦 `SAR` · 🇸🇪 `SEK` · 🇸🇬 `SGD` · 🇹🇭 `THB` · 🇹🇯 `TJS` · 🇹🇷 `TRY` · 🇹🇼 `TWD` · 🇺🇦 `UAH` · 🇺🇸 `USD` · 🇺🇿 `UZS` · `XDR`

## 🏛️ Source

The Central Bank of Turkmenistan publishes the official manat rates every business day, Monday to Saturday: about 45 currencies plus the SDR in manat per unit, from the US dollar, euro and pound to the currencies of the CIS and Central Asian neighbours, the Gulf, East Asia and the Indian subcontinent. The dollar has been fixed at 3.5000 manat since January 2015 and every other quote is a cross of that peg, so the table is the rate that Turkmen banks, customs and state enterprises convert at. Our archive runs from January 2009, the first weeks of the redenominated manat.

- Publisher's own page: [The exchange rate of the Central Bank](https://www.cbt.tm/kurs/kurs_today_en.html) · [www.cbt.tm](https://www.cbt.tm)
- Publication: every business day; the exact schedule, freshness status and any current delay are on the [Central Bank of Turkmenistan rates page](https://allratestoday.com/central-bank-rates-api/cbt/)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- Central Bank of Turkmenistan quotes **TMT per 1 unit of foreign currency** (e.g. `base: "USD", quote: "TMT"` means TMT per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- `rate_type` tells you which of the central bank's series a row belongs to (`reference` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official Central Bank of Turkmenistan rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/cbt/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('cbt')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate cbt ...` command
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Published vs derived rates

If Central Bank of Turkmenistan does not print a pair directly, the API resolves it from the central bank's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The central bank printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via TMT from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('USD', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by Central Bank of Turkmenistan |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'central-bank-of-turkmenistan-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('central-bank-of-turkmenistan-exchange-rate');

getRate('USD', 'TMT', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once per business day — cache the published table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the published table |
| `getLatestRates({ apiKey })` | Free | The central bank's full latest published table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 2009 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same published tables are mirrored daily as open data:

- Hugging Face: [AllRates/central-bank-exchange-rates](https://huggingface.co/datasets/AllRates/central-bank-exchange-rates) — one CSV per institution (`rates/cbt.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- CDN JSON: `https://cdn.jsdelivr.net/gh/AllRates-Today/central-bank-exchange-rates@main/data/cbt/latest.json`

## 🔗 Links

- [Central Bank of Turkmenistan rates page](https://allratestoday.com/central-bank-rates-api/cbt/) — live table, publication cadence, FAQ
- [All central bank sources](https://allratestoday.com/central-bank-rates-api/)
- [Package docs on the site](https://allratestoday.com/docs/sdk/central-bank-of-turkmenistan-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (free)](https://allratestoday.com/register) · [Pricing](https://allratestoday.com/pricing/)
- [GitHub](https://github.com/AllRates-Today/central-bank-of-turkmenistan-exchange-rate)

## 📜 License

MIT
