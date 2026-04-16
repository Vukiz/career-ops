# Compensation Memory

Use this file as the reusable compensation layer for `career-ops`.

Purpose:
- store known salary targets already stated to recruiters or HR,
- avoid re-researching compensation from scratch for every application,
- keep role-family anchors, company-specific notes, and negotiation context in one place.

Rules:
- Prefer numbers already stored here over repeating market searches.
- Use the closest stored company or role-family anchor as the base point for a new evaluation.
- Use web research only when:
  - this file has no relevant anchor,
  - the role is in a new geography or currency,
  - the existing number is obviously stale or too vague.
- Never invent compensation history.
- Treat company-specific numbers stated to recruiters as negotiation anchors, not guaranteed market truth.

## Role Family Anchors

| Role Family | Geography | Currency | Target | Minimum / Walk-away | Notes |
|---|---|---:|---:|---:|---|
| Engineering Manager | Australia | AUD | 200,000 |  | User-stated anchor already used with Riot HR |
| Software Engineering Manager | Australia | AUD | 200,000 |  | Use as the default starting point for Riot-like game/tech manager roles unless new evidence suggests otherwise |
| Engineering Manager | Europe remote | EUR | 115,000 | 99,000 | Baseline Europe manager anchor using Amsterdam market benchmark as proxy |
| Backend / Platform Engineering Manager | Europe remote | EUR | 114,000 | 99,000 | Baseline backend/platform manager anchor using Amsterdam software engineering manager benchmark as proxy |
| Senior Backend Engineer (Go) | Europe remote | EUR | 84,000 | 71,000 | Baseline Europe senior backend anchor using Amsterdam senior backend engineer benchmark as proxy |
| Senior Backend Engineer (Go) | Global remote, geo-agnostic pay | USD | 185,000 | 147,000 | High-end global remote anchor from current remote senior backend benchmark; use only when the company clearly pays global-remote rates |

## Company-Specific History

| Company | Role | Geography | Currency | Number | Type | Source | Date | Notes |
|---|---|---|---:|---:|---|---|---|---|
| Riot Games | Engineering Manager | Australia | AUD | 200,000 | Target stated to HR | User-provided | 2026-04-16 | Use as the stored anchor for Riot manager compensation discussions |

## Market Benchmarks

| Role Family | Geography | Currency | Benchmark | Type | Source | Date | Notes |
|---|---|---:|---:|---|---|---|---|
| Engineering Manager | Amsterdam, Netherlands | EUR | 115,000 | Median market benchmark | MasloJobs Amsterdam Engineering Manager salary guide | 2026-04-16 | Use as a fintech/European manager base point when the company does not publish a band |
| Engineering Manager | Amsterdam, Netherlands | EUR | 90,000-148,000 | Market range | MasloJobs Amsterdam Engineering Manager salary guide | 2026-04-16 | 25th to 75th percentile range |
| Engineering Manager | Netherlands | EUR | 122,000 | Median total pay benchmark | Glassdoor Amsterdam Engineering Manager estimate | 2026-04-16 | Used in Yuno evaluation as a directional benchmark |
| Software Engineering Manager | Amsterdam, Netherlands | EUR | 114,000 | Median total pay benchmark | Glassdoor Amsterdam Software Engineering Manager estimate | 2026-04-16 | Useful proxy for backend/platform engineering manager roles in Europe |
| Software Engineering Manager | Amsterdam, Netherlands | EUR | 99,000-142,000 | Total pay range | Glassdoor Amsterdam Software Engineering Manager estimate | 2026-04-16 | Practical Europe manager range when no company band is published |
| Senior Backend Engineer | Amsterdam, Netherlands | EUR | 84,000 | Median total pay benchmark | Glassdoor Amsterdam Senior Backend Engineer estimate | 2026-04-16 | Good Europe proxy for senior backend and senior Go roles |
| Senior Backend Engineer | Amsterdam, Netherlands | EUR | 71,000-99,000 | Total pay range | Glassdoor Amsterdam Senior Backend Engineer estimate | 2026-04-16 | Practical Europe IC range when the company pays local-Europe rates |
| Senior Backend Engineer | Remote | USD | 185,000 | Median total pay benchmark | Glassdoor Remote Senior Backend Engineer estimate | 2026-04-16 | Use only for companies with clearly geo-agnostic or global remote compensation |
| Senior Backend Engineer | Remote | USD | 147,000-224,000 | Total pay range | Glassdoor Remote Senior Backend Engineer estimate | 2026-04-16 | Useful upside anchor for strong global-remote employers |

## Recent Evaluation Notes

| Company | Role | Geography | Result | Date | Notes |
|---|---|---|---|---|---|
| Yuno | Engineering Manager | Europe time zones / Amsterdam-preferred | No posted band found; used Amsterdam engineering manager market benchmark | 2026-04-16 | Good manager fit, but compensation should be verified early and Georgia eligibility is unclear |

## Negotiation Notes

- Priority is strong compensation, not just title.
- Avoid spending time on roles that are materially below the stored anchor unless the role is unusually strong on scope, brand, or upside.
- For company-specific conversations, prefer saying the target confidently and then calibrating only if scope, level, or location materially changes.

## Gaps To Fill Over Time

Add entries here when any of the following becomes known:
- recruiter-provided salary bands,
- posted compensation ranges,
- successful negotiation anchors by geography,
- role-family minima for backend/platform IC roles,
- stock/equity patterns that materially change the package quality.
