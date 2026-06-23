# BeaconFinTalent-Analysis

Monthly analysis dashboard for Beacon FinTalent website performance — built for People & Culture and Marketing leadership.

## Files

- **`index.html`** — Main dashboard (single source of truth)
- **`fintalent-performance.html`** — Redirects to `index.html` for backward compatibility

## Monthly update workflow

When adding a new month (e.g. June 2026):

1. Copy the previous month's object in `MONTHLY_DATA` inside `index.html`
2. Change the key (e.g. `june2026`) and update all metric/chart values
3. Write `executiveAnalysis` with:
   - `headline` — one-sentence monthly story
   - `health` — `on-track` | `needs-attention` | `at-risk`
   - `win`, `watch`, `action` — bullets answering P&C and Marketing stakeholder questions
4. Add `recommendations` array to the **new latest month only** (shown in the **Deep Dive** tab)
5. Set `recommendations: null` on the previous latest month
6. Append the new key to `MONTH_ORDER` (newest last)

## Data sources

Google Analytics 4 (GA4) and Google Search Console (GSC).
