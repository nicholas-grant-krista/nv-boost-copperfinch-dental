# Client Profile — Copperfinch Dental Studio (DEMO)

**FICTIONAL demo client — dry run NV-2026-DRY-001. Placeholder data throughout.**

## Identity

- Name: Copperfinch Dental Studio
- Location / service area: Bend, Oregon
- Website: none (placeholder domain copperfinchdental.example)
- Contact: Dr. Elena Marsh · elena.marsh@copperfinchdental.example · (541) 555-0177

## Agreement

- Agreement no.: NV-2026-DRY-001 · Provider signatory: Taylor R., North Vista Marketing
- Term: 12 months from 2026-07-13, auto-renew · Fees: $2,500/mo management · Ad spend: $1,000/mo (client-funded) · Billing: Net 15

## Scope of Work — Boost handling

| # | Contract line | Class | Handling |
|---|---|---|---|
| D1 | Local conversion landing page (Bend) | artifact | local-landing-page-builder → docs/ |
| D2a | Google Search campaign build (keywords, RSA, negatives, upload sheet) | artifact | google-search-campaign-builder → campaigns/ (CSV) |
| D2b | Campaign activation + management | ongoing_service | HELD — spend gate; no campaign-level Ads tools yet |
| D3 | Monthly SEO blog + ad copy | artifact | nvm-seo-blog-builder → docs/ + campaigns/ (deferred from dry run) |
| D4 | Initial SEO site audit | precursor | HELD — demo client has no crawlable site |
| D5 | GBP setup + optimization | ongoing_service | SKILL BACKLOG (partial: GHL create_citation) |
| D6 | Monthly performance report | ongoing_service | SKILL BACKLOG |

## Brand & voice

No live site — demo fallbacks per downstream skill rules: warm/professional local-practice voice, teal (#0f766e) + copper (#b45309) palette and Lora/Inter type, all labeled as fallbacks in page CSS. No testimonials or stats invented.

## Delivery Log

| Date | Line | Deliverable | Commit | Status |
|---|---|---|---|---|
| 2026-07-10 | Boost Engine | Workspace provisioned from template (public, demo, noindex) | 56df716 | done |
| 2026-07-10 | Local Pages | Bend local conversion landing page (docs/index.html) | ad70164 | done — illustrative (demo fallbacks) |
| 2026-07-10 | Paid Search | Campaign spec + keyword CSV (spec-only; activation held at spend gate) | 99acf2e | done — illustrative figures |
| 2026-07-10 | Boost Engine | Run manifest (reports/2026-07-10-run-manifest.md) | this commit | done |
