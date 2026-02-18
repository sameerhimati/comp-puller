# comp-puller

## What This Is
Market comparable data extraction and benchmarking tool for CRE.

## Key Constraints
- Comps data primarily from CoStar (requires authenticated session)
- Cache comps locally — don't re-pull same submarket daily
- Output: structured JSON/CSV with comp details + summary statistics
- Benchmarking: compare a subject property against market averages

## Architecture
- Data sources: CoStar (primary), potentially public records (secondary)
- Comp store: local SQLite or JSON cache with TTL
- Benchmarking: compare subject property metrics against comp set
- CLI: pull comps, view cached comps, benchmark a property

## Tech
- Python 3.14, browser-use, Playwright, Typer + Rich
- SQLite for comp caching
- Use venv/bin/python and venv/bin/pytest
