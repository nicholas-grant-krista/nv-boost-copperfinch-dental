# Run Manifest — NV-2026-DRY-001 · Copperfinch Dental Studio (DEMO DRY RUN)

Run date: 2026-07-10 · Orchestrator: nv-contract-orchestrator v2.3.0 (AUTO-RUN) · Purpose: pre-live seam test

## Outcomes

| ID | Deliverable | Class | Skill | Decision | RESULT | Commit |
|---|---|---|---|---|---|---|
| P0 | Provision workspace (public, demo) | — | Boost Engine | run | ran — EXCEPT skills/ removal failed (delete_file unapproved) | 56df716 |
| P0b | Enable Pages + verify build | — | Boost Engine | run | ran — API verification blocked (workflow tools unapproved); verified out-of-band via live fetch: site up, noindex ✓ | — |
| D1 | Bend landing page | artifact | local-landing-page-builder | run | ran — illustrative (demo fallbacks; no live site to audit) | ad70164 |
| D2a | Campaign spec + keyword CSV | artifact | google-search-campaign-builder | run | ran — illustrative figures (SEMrush keyword tools missing); PDF+xlsx deliverables skipped (binary-no-storage-path) | 99acf2e |
| D2b | Campaign activation | ongoing_service | — | hold | held — spend hard gate + no campaign-level Ads tools | — |
| D3 | Monthly blog + ad copy | artifact | nvm-seo-blog-builder | run | deferred — dry-run scope (no new seams) | — |
| D4 | Initial SEO audit | precursor | SEMrush audit_completed | hold | held — demo client has no crawlable site | — |
| D5 | GBP setup/optimization | ongoing_service | — | backlog | skill gap (partial: GHL create_citation) | — |
| D6 | Monthly performance report | ongoing_service | — | backlog | skill gap | — |

## Findings for live readiness

1. **BLOCKER — skills/ exposed publicly:** delete_file unapproved → provisioning could not remove inherited skills/; this PUBLIC demo repo now exposes orchestrator source. Approve delete_file (or re-think skills/ location) before any live run.
2. **Governance:** approve wait_for_workflow_completion, list_workflow_runs (Pages verification), upload_release_asset + create_release (binary deliverables), create_repository (bootstrap).
3. **Extension gap:** SEMrush extension lacks keyword research tools required by google-search-campaign-builder Step 2 — real volume/CPC unpullable.
4. **Extension gap:** Google Ads extension is account-level only — no campaign push path; activation is manual Ads Editor import until built.
5. **Sandboxes:** Google Ads + SEMrush invokers are sandbox-credentialed.
6. **Role:** orchestrator assigned to MCP TEST only; production users need Krista MCP role.
7. **Worked clean:** create_from_template, atomic commit_files (multi-file JSON), enable_or_update_pages, krista_execute_skill client-mode round-trips, delivery-log-in-same-commit discipline, demo safety rails (collision check, noindex, labeled placeholders).

## Open items

D3 execution (full-scope re-run), D5/D6 skill builds, conversion tracking design for live clients.
