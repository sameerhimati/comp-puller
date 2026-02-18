# comp-puller

Pulls comparable sale and lease data for commercial real estate submarkets. Benchmarks rent/SF, cap rates, and sale prices against market.

## What it replaces
Analysts manually pulling comps from CoStar and building market comparison spreadsheets.

## Usage
```bash
comp-puller sales --submarket "DFW Industrial" --sf 10000-50000 --period 12m
comp-puller leases --submarket "Houston Industrial" --sf 10000-30000
comp-puller benchmark --property property.json
```

## Data Points
- Sale comps: price/SF, cap rate, date, buyer/seller
- Lease comps: rent/SF, lease type (NNN, gross, modified gross), term
- Market stats: avg rent, avg cap rate, vacancy rate by submarket

## Input / Output

**Input:**
- CLI flags: `--submarket`, `--sf` (SF range), `--period` (lookback, e.g. "12m")
- Benchmark mode: `--property property.json` (subject property to compare against comps)
- Pre-authenticated browser session (Playwright storage state) for CoStar

**Output:**
- Comps JSON/CSV: `{ "address", "sale_price", "price_per_sf", "cap_rate", "sale_date", "buyer", "seller", "sqft" }`
- Benchmark mode: subject property metrics vs comp set averages (JSON + Rich table)
- Cached locally in SQLite (avoid re-pulling same submarket)
- Exit code 0 on success, 1 on failure

## Stack
- Python 3.14
- browser-use + Playwright (for CoStar comp data)
- Typer + Rich for CLI

## Status
🟡 Not started
