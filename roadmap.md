# comp-puller Roadmap

## v0.1 — Manual Comp Entry
- [ ] Project setup (venv, requirements.txt, CLI skeleton)
- [ ] Comp data model (Pydantic: SaleComp, LeaseComp)
- [ ] Local comp store (SQLite)
- [ ] CLI: `comp-puller add-sale`, `comp-puller add-lease` (manual entry)
- [ ] CLI: `comp-puller benchmark --property`
- [ ] Summary statistics (avg, median, range by submarket)

## v0.2 — CoStar Integration
- [ ] browser-use agent for CoStar comp extraction
- [ ] Auto-pull comps for a submarket
- [ ] Dedup and merge with existing comp store

## v0.3 — Analysis
- [ ] Trend analysis (rent/cap rate over time)
- [ ] Submarket ranking
- [ ] Export to PDF/Excel for deal memos
