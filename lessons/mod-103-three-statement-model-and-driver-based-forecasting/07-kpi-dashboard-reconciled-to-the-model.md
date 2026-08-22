# KPI Dashboard Reconciled to the Model

## Why this matters

Every board pack has a dashboard slide. The slide has 8-15 numbers on it — ARR, MRR, growth rate, NRR, GRR, burn, runway, magic number, Rule of 40, CAC payback, and a handful of others. Board members read these numbers first and last, and they are what determines the tone of every subsequent discussion. If the numbers on the dashboard don't match the numbers in the model, the CFO has a credibility problem that no amount of subsequent context can fix.

The failure mode is the "dashboard as separate document": a CFO or an FP&A analyst types numbers into a slide from the model each month. Over time the dashboard's number and the model's number drift. The board sees ARR of $8.2M on the dashboard; the P&L sums to $8.05M; the ARR walk in the appendix uses $8.4M. Three numbers, three tabs, no reconciliation. The next diligence conversation surfaces the drift and everyone loses confidence in the whole pack.

This chapter installs the KPI dashboard as a tab in the model that references every cell from a driver, statement, or schedule — never a typed number. Change any driver in the model and every dashboard cell updates. The dashboard cannot drift because it is not a separate document.

## The dashboard tab — architecture

The dashboard tab has one function: pull the right numbers from the right places in the model, format them for board consumption, and produce the standard views (current-period snapshot, trailing-12 monthly trend, plan-vs.-actual, scenario comparison).

Structural conventions:

- **No typed numbers.** Every cell is a formula, a link, or a reference to a chart source range.
- **One section per KPI family.** ARR & growth; retention; unit economics; efficiency / burn; hiring; cash.
- **Both current-period and trend.** The trailing-12 monthly view of each KPI is as important as the current-period value.
- **Reconciliation source called out.** Every KPI has a small "source: tab X, row Y" footnote so the reader can trace back to the underlying calculation.

The tab is organised so that the board slide can be built directly from it — copy the current-period section into the slide, copy the trailing-12 chart into the slide, done. No re-typing.

## The KPI set — SaaS canonical

The canonical KPI set for a Series-A B2B SaaS startup, grouped by family:

### ARR and growth

- **ARR (Annual Recurring Revenue)** — total MRR × 12 at period-end. Sourced from the cohort revenue schedule (chapter 4).
- **New ARR added in period** — sum of new-bookings ACV closed in the period.
- **Expansion ARR** — increase in ARR from existing customers (upsells, cross-sells, plan upgrades).
- **Contraction ARR** — decrease in ARR from existing customers (downgrades) that don't fully churn.
- **Churned ARR** — ARR lost from cancellations.
- **Net new ARR** — new + expansion − contraction − churned. Should tie to `Ending ARR − Beginning ARR`.
- **MoM growth rate** — `Ending ARR / Prior-month Ending ARR − 1`.
- **YoY growth rate** — `Ending ARR / Same-month-prior-year Ending ARR − 1`.

### Retention

- **NRR — Net Revenue Retention.** For a cohort of customers active 12 months ago, `today's ARR from that cohort / 12-month-ago ARR from that cohort`. Numbers >100% indicate that expansion is exceeding contraction and churn.
- **GRR — Gross Revenue Retention.** Same denominator, but the numerator excludes expansion — only what's left of the original ARR from that cohort. Always ≤ 100%; the delta between NRR and GRR is the expansion contribution.
- **Logo retention** — for the same cohort, `today's customer count / 12-month-ago customer count`. Distinct from dollar retention; small customers can churn without a large dollar impact.

### Unit economics

- **Blended CAC** — total S&M spend / new customers added in the period. Sourced from the P&L (S&M) and the funnel tab (new customers).
- **CAC payback** — CAC / (ARPU × gross margin per month). Read empirically off the cohort table (see [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/) chapter 4).
- **LTV** — cohort-based, discounted, from [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/) chapter 2. Sourced from the cohort schedule.
- **LTV:CAC ratio** — LTV / CAC. Target: 3:1 or higher (SaaS canon; see [ForEntrepreneurs](https://www.forentrepreneurs.com/)).
- **Gross margin (%)** — Gross profit / Revenue. Sourced from the P&L.

### Efficiency and burn

- **Monthly cash burn** — average monthly cash decrease over the trailing 3 months, excluding financing. Sourced from the cash-flow statement.
- **Net burn** — cash outflow after all sources of cash (including subscription revenue), before financing. This is the number that drives runway.
- **Runway (months)** — ending cash balance / trailing-3-month average net burn. If burning $500K/month and cash is $6M, runway is 12 months.
- **Cash-out date** — the specific month in which the forecast shows cash going to zero under the current scenario. Sourced from the cash line on the balance sheet or the CFS.
- **Burn multiple** — net burn / net new ARR. Introduced by [David Sacks](https://sacks.substack.com/) as a capital-efficiency instrument. Targets: <1 excellent, 1-2 great, 2-3 acceptable, >3 concerning at Series-A onward.
- **Magic number** — `(current-quarter revenue − prior-quarter revenue) × 4 / prior-quarter S&M spend`. Introduced by [Scale Venture Partners](https://www.scalevp.com/); a magic number >1 indicates S&M spend is producing more than a dollar of ARR per dollar spent.
- **Rule of 40** — `revenue growth rate (%) + EBITDA margin (%)`. Introduced by [Brad Feld](https://feld.com/) and formalised in the [Bessemer State of the Cloud](https://www.bvp.com/atlas/state-of-the-cloud) reports. Target: ≥40 for a healthy public-SaaS trajectory; earlier-stage companies typically show negative EBITDA margin and rely on the growth term.

### Hiring and organisational

- **Headcount at period-end** — total, split by department.
- **Hires added in period** — total, split by department.
- **Attrition in period** — total, and rate (departures / average headcount).
- **Revenue per employee** — annualised revenue / average headcount. Trending; the direction (up = leverage; down = organisational bloat) matters more than the level.

### Cash

- **Cash and equivalents at period-end** — sourced from the balance sheet.
- **Cash movement in period** — sum of CFO + CFI + CFF from the CFS.
- **Days of cash** — cash / (daily burn). Same information as runway; some CFOs prefer this framing.
- **Weeks-to-payroll** — cash / (weekly payroll cost). A more granular alarm bell than runway when cash is tight.

Not every dashboard shows all 25 numbers. A working board pack usually shows 8-12, with the rest available in the appendix or the data room. The choice of which subset is context-dependent — for a fast-growth Series-A, ARR / growth / burn / runway / magic number dominate; for a Series-B focused on unit economics, LTV:CAC / NRR / Rule of 40 dominate.

## The three views the dashboard produces

**Current-period snapshot.** One column of numbers, each with the current month's value. This is what appears on the "at a glance" slide of the board pack.

**Trailing-12 monthly trend.** For each KPI, a chart showing the trailing 12 months. This is what identifies whether a KPI is improving or deteriorating. A single-point number is misleading; a trend line surfaces the direction.

**Plan-vs.-actual.** For each KPI, the current-period value against the plan-of-record value. This is what identifies the specific KPIs that are off-track and drives the variance discussion in the board meeting.

**Scenario comparison** (less frequently shown, usually in fundraise-timing conversations). For each KPI, the base / upside / downside forecast values at a specific future month (e.g., 12 months out). This is what shows the range of outcomes the plan is exposed to.

The dashboard tab produces all four; the board pack picks the right view per slide.

## Reconciling every KPI to a model source

Every KPI on the dashboard has a specific model source. The convention: a footnote or comment on each KPI cell that names the source tab and row.

Examples:

- **ARR.** Source: cohort revenue schedule (drivers tab), sum of month-M cohort MRR × 12.
- **MoM growth rate.** Source: derived from ARR row, `ARR[M] / ARR[M-1] − 1`.
- **NRR.** Source: cohort schedule, ratio of (cohort C's revenue at M+12) to (cohort C's revenue at M+0), averaged across cohorts with 12+ months of data.
- **CAC.** Source: P&L S&M for period ÷ funnel closed-won for period.
- **Gross margin.** Source: P&L gross profit / revenue.
- **Monthly cash burn.** Source: CFS net change in cash excluding CFF, trailing-3-month average.
- **Runway.** Source: balance-sheet cash / trailing-3-month average net burn.
- **Cash-out date.** Source: the first forecast month where balance-sheet cash < 0.
- **Burn multiple.** Source: CFS net burn / ARR walk (net new ARR).
- **Magic number.** Source: P&L revenue delta × 4 / lag-quarter P&L S&M.
- **Rule of 40.** Source: derived, `YoY revenue growth (%) + LTM EBITDA margin (%)`.

The reconciliation is not just documentation — it is functional. Change the P&L S&M for a period and the CAC updates; change the cohort retention curve and the NRR updates; change the hiring plan and the runway updates. The dashboard cannot drift because it is the same underlying model.

## What the dashboard is not

The dashboard is not the P&L. The P&L is a financial statement with a specific presentation (GAAP-style, revenue → COGS → OpEx → Net Income). The dashboard is a management artefact with KPI framing (ARR, growth, retention, efficiency, burn, runway). They share underlying numbers but present them for different audiences.

The dashboard is also not the operating scorecard. Operating scorecards (sales pipeline health, product-usage metrics, customer-health scores) are the CRO's or COO's artefact; they live in the CRM / product-analytics tool / OKR system. The CFO's dashboard is the *financial* KPI pack, sourced from the model.

The overlap between the two is deliberate — pipeline coverage and win rate are both operating and financial metrics — but the CFO's dashboard covers the financial framing.

## Live vs. periodic — when to update

A quarterly board pack ships a snapshot dashboard for the quarter. Between board meetings, the dashboard is updated in one of three modes:

- **Live.** The model auto-pulls actuals from an accounting system (via Google Sheets IMPORTDATA, an API to QBO / NetSuite / Xero, or a BI tool like Sigma / Mode / Looker). The dashboard updates continuously. Powerful but requires an accounting-actuals data pipeline that is stable enough to trust.
- **Monthly.** A CFO or FP&A analyst refreshes the actuals column each month after close. The dashboard is current for the past month. The most common pattern at Series-A.
- **Quarterly.** Actuals refresh at quarterly close only. Adequate for a small early-stage company where monthly close isn't reliable enough for monthly reporting.

The move toward live dashboarding is one of the drivers of the FP&A-tooling category (Causal, Runway, Mosaic, Adaptive; see chapter 8). Spreadsheet models can be made "live" but require significant plumbing; purpose-built FP&A tools have this as a native feature.

The critical rule regardless of update frequency: the dashboard is *always* the same as the model, at whatever cadence the model is refreshed. There is no scenario where the dashboard has newer or different numbers than the model.

## Plan-vs.-actual and the variance narrative

The plan-vs.-actual column is the most-read section of the dashboard for a mature board. It compares the current-period actual against the plan-of-record set at the start of the year or the last quarterly re-forecast.

```
Metric               Actual    Plan     Variance    Variance %    Direction
ARR                  $8.2M    $8.5M    -$0.3M       -3.5%         Off
MRR                  $683K    $708K    -$25K        -3.5%         Off
New ARR              $1.1M    $1.3M    -$0.2M       -15%          Off
Expansion ARR        $0.4M    $0.3M    +$0.1M       +33%          On
NRR (12mo)           122%     118%     +4pt         +3.4%         On
CAC                  $28K     $23K     +$5K         +22%          Off
Burn                 $580K    $525K    +$55K        +10%          Off
Runway (months)      14       17       -3           -18%          Off
```

The variance narrative is the CFO's write-up of the "why" behind each Off row. For the above:

- *"New ARR missed by $200K driven by two enterprise deals slipping from Q2 to Q3 (retained pipeline; expected to close early Q3)."*
- *"CAC ran 22% over plan because paid-search inflation raised cost-per-lead from $130 to $175; ops team is rebalancing spend toward outbound where CAC is $15K vs. $32K on paid."*
- *"Burn ran 10% over plan because two Eng backfills went out earlier than planned; net cash consumption tracking to plan for the trailing 6-month view."*

The narrative is what makes the dashboard actionable. The numbers alone identify what is Off; the narrative names why and what the response is.

## The board-ready format

The dashboard tab in the model produces the numbers; the board slide presents them. A working format:

**Slide 1 — Snapshot.** 8-12 KPIs in a two-column table (KPI name, current value). Grouped by family. No formulas, no charts, just the numbers.

**Slide 2 — ARR walk.** The graphical version — bar or waterfall showing Beginning ARR + New + Expansion − Contraction − Churn = Ending ARR. Sourced from the ARR walk on the dashboard tab.

**Slide 3 — Trailing-12 trend.** The trend charts for the top 4-6 KPIs (ARR, MRR, burn, runway, NRR, CAC). Small multiples.

**Slide 4 — Plan-vs.-actual.** The variance table with the narrative below it. This is the slide the board spends the most time on.

**Slide 5 — Scenarios / cash outlook.** Base / upside / downside cash trajectory and cash-out date. This is the slide that drives the fundraise-timing discussion.

Every slide's numbers trace back to the dashboard tab; every dashboard tab number traces back to a model tab. The board pack is a formatted view of the model, not a separate authoring exercise.

## Summary

- The KPI dashboard is a tab in the model that references every cell from a driver, statement, or schedule; every number is a formula, never a typed value. This is the discipline that prevents the dashboard from drifting from the underlying financials.
- The canonical Series-A SaaS KPI set covers ARR & growth, retention (NRR / GRR / logo), unit economics (CAC / LTV / payback / gross margin), efficiency & burn (burn multiple, magic number, Rule of 40, runway, cash-out date), hiring, and cash.
- The dashboard produces four views: current-period snapshot, trailing-12 trend, plan-vs.-actual, and (occasionally) scenario comparison. The board pack pulls the right view per slide.
- Every KPI has a specific model source called out in a footnote or comment — CAC from P&L S&M / funnel closed-won, NRR from cohort schedule, runway from balance-sheet cash / net burn, and so on.
- Update cadence is either live (with an accounting-actuals data pipeline), monthly, or quarterly. Regardless of cadence, the dashboard is *always* consistent with the model.
- Plan-vs.-actual with a written variance narrative is the most-read section of a board pack; the numbers identify what is Off, the narrative names why and what the response is.
- The board slide format is derived from the dashboard tab; no re-typing. Snapshot, ARR walk, trend, plan-vs.-actual, scenarios.

Chapter 8 covers what breaks in the wild — the common model failure modes, the review checklist that catches them, and the CFO-level decision on when to graduate off spreadsheets onto Causal / Runway / Mosaic / Anaplan / Adaptive.
