# The Cohort Table — Construction and Reading

## Why this matters

The cohort table is the single most important artefact in a CFO-authored unit-economics pack. It is the source table from which cohort LTV (chapter 2), payback period (chapter 1), NRR / GRR (chapter 5), and retention curves are all derived. Every other number in the pack is a summary, aggregation, or reformatting of the cohort table. A CFO who cannot produce and read the cohort table cannot defend any of the metrics on top of it.

The failure mode: an early-stage founder reports "our retention is great" without ever producing the cohort view, and then in diligence the investor asks for a cohort chart and the founder ships a blended chart (all customers, over time, on the same axis) which shows a superficially positive trend that turns out to be a mix effect from a rapidly growing top of funnel. The un-blend into cohorts reveals that the recent cohorts are churning much faster than the older cohorts, and the trend is actually deteriorating. This is the single most common "the number on the deck is not the number the data says" moment in Series-A and Series-B diligence.

This chapter installs the standard cohort-table construction, the five layered views a CFO produces from it, and the four readings a board or an investor should be able to lift directly off the table without further analysis.

## What a cohort is, precisely

A cohort is the set of customers who signed up in a specific period — usually a calendar month, sometimes a calendar quarter for lower-volume enterprise businesses. Every customer belongs to exactly one cohort (their signup cohort). The cohort table tracks that cohort's behaviour over time as *cohort-relative months*: month 0 (signup month), month 1 (one month later), month 2, and so on.

The cohort dimension is usually the signup month. Alternate dimensions occasionally used:

- **Acquisition-channel cohort** — customers who signed up via the same channel in the same period. Combines the un-blend from chapter 1 with the temporal cohort view.
- **Pricing-plan cohort** — customers on the same pricing plan. Useful for companies with material pricing changes over time.
- **Product cohort** — for multi-product companies, customers whose first product was product X.
- **Geography cohort** — for internationally-expanding companies, customers in the same region.

For a Series-A unit-economics pack the standard is monthly signup cohorts. Additional dimensions are added when the story requires it. A cohort table sliced across two dimensions (e.g., signup month × acquisition channel) quickly becomes unwieldy; either commit to a primary dimension and produce secondary views, or use a pivot-table tool that handles the multi-dimensional slice.

## The five-layer cohort table

A defensible cohort table is built as five stacked layers, each transforming the layer above it. Every downstream analysis is a read on one of these layers.

**Layer 1 — Signup count.** Rows are signup cohorts (Jan 2024, Feb 2024, ..., Dec 2024). Columns are cohort-relative months (M0, M1, M2, ..., M12+). The M0 cell for the Jan 2024 cohort is the count of customers who signed up in Jan 2024. Every other cell in that row is the count of customers from the Jan 2024 cohort still retained (still an active paying customer) in the corresponding cohort-relative month.

The Jan 2024 row typically declines monotonically — you don't gain new members of a cohort after M0. The exception: some companies define cohort membership by first-paid-month rather than first-signup-month, which can cause the M0 count to grow if there's a free-tier-to-paid conversion lag.

**Layer 2 — Retention percentage.** Same shape as layer 1, but each cell is expressed as a percentage of the M0 count. The Jan 2024 row starts at 100% (M0) and typically declines to some floor over time. This is the layer that produces the classic "retention curve" chart: cohort-relative months on the x-axis, retention percentage on the y-axis, one line per cohort.

The shape of the retention curve is diagnostic:

- **Steep initial drop with a flat plateau** — the "healthy SaaS" pattern; a fraction of customers churn in the first 30-90 days but the retained base is sticky.
- **Steady linear decline** — a challenging pattern; suggests no meaningful sticky segment and continuous customer erosion.
- **Steep drop with no plateau** — a very unhealthy pattern; suggests fundamental product-market-fit issues.
- **Rising retention percentage** — indicates a data-collection issue. Retention as defined here cannot exceed 100% (revenue expansion doesn't add new customers to a cohort). If your layer 2 shows values above 100%, you're computing revenue retention, not customer retention — see layer 4.

**Layer 3 — Revenue per cohort per month.** Cells contain total monthly recurring revenue produced by the cohort's retained customers in the corresponding month. This layer combines the retained count from layer 1 with ARPU per retained customer at that cohort-month.

Layer 3 is where expansion first shows up. If a cohort's per-customer ARPU grows over time — customers upgrading plans, adding seats, cross-selling into new products — then per-customer revenue in later cohort months exceeds per-customer revenue at signup, and layer 3 can decline more slowly than layer 1 or even increase.

**Layer 4 — Net dollar retention per cohort.** Cells are layer-3 values divided by the M0 layer-3 value, expressed as a percentage. This is the "net dollar retention curve" per cohort: what fraction of the original cohort's revenue is the cohort producing at cohort-month M?

A cohort with 90% M12 layer-2 (customer retention) but 120% M12 layer-4 (net dollar retention) is a cohort where 10% of customers churned but the remaining 90% expanded enough to overcompensate for the lost revenue. This is the *net-negative-churn* pattern that Best Cloud Companies reports (Bessemer, Meritech) associate with a defensible SaaS moat.

**Layer 5 — Cohort gross profit and cumulative gross profit.** Cells are layer-3 revenue values multiplied by the cohort's gross margin (chapter 3). A separate column at the right shows cumulative gross profit for the cohort through the current cohort month.

Layer 5 is the layer that answers the two most-asked unit-economics questions:

- **Payback period.** The cohort-month M where cumulative gross profit first crosses the fully-loaded CAC for that cohort (chapter 1). Read directly off the cumulative column.
- **Cohort LTV.** The sum of the discounted per-month gross profits over the truncation horizon (chapter 2). One formula on the row.

The whole unit-economics story compresses into these five layers.

## Data preparation — what you need before you can build the table

The cohort table cannot be assembled from summary metrics. It requires transaction-level data:

- **A customer-account list** with signup date and current status (active, churned, downgraded).
- **A monthly-recurring-revenue history per customer** — for every customer, MRR (or ARR ÷ 12) at each month-end since signup, including changes. This is typically pulled from the billing system (Stripe, Chargebee, Zuora, Recurly) or the CRM's ARR-tracking module (Salesforce with a subscription-management overlay).
- **A cohort assignment per customer** — the signup month (or the alternate dimension chosen).
- **A gross-margin mapping per customer or per cohort per month** — the cost-to-serve model from chapter 3.

The single hardest data problem is *change events* — plan upgrades, downgrades, seat adds, seat removals, product cross-sells, contract expansions and contractions. A well-designed billing system produces an *MRR movement ledger* — one row per customer per event, with the MRR delta and the reason code (new, upgrade, downgrade, churn, resurrection). Companies that don't have this ledger have to reconstruct it from invoice history, which is possible but error-prone.

Before building the cohort table, produce a data-quality report:

- Every active customer has a signup date.
- Every customer's MRR history reconciles to their invoice history.
- The sum of MRR across all customers at month-end reconciles to the ARR / MRR on the P&L (within a documented reconciliation adjustment for non-recurring revenue, credits, and refunds).
- Every churn event has a churn date and, ideally, a churn reason code.

Without this data-quality baseline, the cohort table will contain errors that propagate to every downstream metric. Producing the reconciliation report is often the multi-week work item that precedes the actual cohort-table build.

## Building the table — mechanics

The cohort-table build is straightforward once the underlying data is clean. Pseudocode:

```
for each customer c:
    cohort[c] = signup_month(c)
    for each month m in observation window:
        if c is retained at month m:
            m_rel = m - cohort[c]                # cohort-relative month
            retained_count[cohort[c]][m_rel] += 1
            revenue[cohort[c]][m_rel] += MRR(c, m)

for each cohort k, each m_rel:
    retention_pct[k][m_rel] = retained_count[k][m_rel] / retained_count[k][0]
    ndr[k][m_rel] = revenue[k][m_rel] / revenue[k][0]
    gross_profit[k][m_rel] = revenue[k][m_rel] * cohort_gm[k][m_rel]
    cum_gp[k][m_rel] = sum(gross_profit[k][0..m_rel])
```

In a spreadsheet, this is a pivot table with signup month on rows, cohort-relative month on columns, and the various measures (count, revenue, GP) as the values. The messy part is aligning cohort-relative month against calendar month for the cross-tab: a customer who signed up in Jan 2024 has their M6 in Jul 2024; a customer who signed up in Feb 2024 has their M6 in Aug 2024. The formula that computes cohort-relative month from calendar month and signup month is `MONTHS(observation_month) - MONTHS(signup_month)`.

For companies with fewer than ~1,000 cohort-months of data (e.g., under 3 years of monthly cohorts of any material size), a well-organised spreadsheet is sufficient. Beyond that, a purpose-built cohort-analysis tool (embedded in a BI tool like Looker or ThoughtSpot, or a SaaS-analytics tool like Mixpanel or ChartMogul or Cube) is more scalable and more auditable. Regardless of tool, the source table with cohort × cohort-relative-month × measure must be reproducible from the underlying billing data.

## The four readings a CFO produces off the table

Once built, the cohort table produces four specific artefacts that appear in the unit-economics pack. Each reads directly off one of the five layers.

**Reading 1 — Retention curves.** The classic chart: cohort-relative months on the x-axis, retention percentage on the y-axis, one line per signup cohort. A healthy pattern shows recent cohorts tracking above or with older cohorts (retention is improving); a deteriorating pattern shows recent cohorts falling below older cohorts. The chart is layer 2 plotted; the reading is qualitative but the direction and slope of recent-cohort curves is the specific investor question.

Two versions are typically shown side by side: customer retention (layer 2) and net dollar retention (layer 4). If the two diverge significantly for a cohort — customer retention is 65% at M12 but NDR is 115% at M12 — the story is "we lose small customers but the ones that stay expand aggressively," which is a specific enterprise-SaaS pattern that investors recognise and value.

**Reading 2 — Payback period per cohort.** The cohort-month at which cumulative gross profit from layer 5 first crosses the cohort's fully-loaded CAC. Present as a table:

| Cohort | Cohort size (M0) | Fully-loaded CAC per customer | Payback month |
|---|---|---|---|
| 2024-01 | 42 | $8,400 | M11 |
| 2024-02 | 51 | $8,100 | M10 |
| ... | ... | ... | ... |

Trend direction (payback compressing or extending across recent cohorts) is what a board or investor absorbs. Compressing payback under a growing top of funnel is the healthy pattern; extending payback is a red flag that either CAC is inflating or cohorts are shrinking in ARPU or retention.

**Reading 3 — Cohort LTV and LTV:CAC ratio.** For each cohort, the discounted cumulative gross profit through the truncation horizon (chapter 2), divided by the cohort's fully-loaded CAC. Present as the same table shape:

| Cohort | Cohort LTV (36-mo discounted @35%) | Fully-loaded CAC | LTV:CAC ratio |
|---|---|---|---|
| 2024-01 | $28,300 | $8,400 | 3.4:1 |
| 2024-02 | $31,200 | $8,100 | 3.9:1 |
| ... | ... | ... | ... |

For older cohorts where M36 has not yet been observed, the number is partly empirical and partly extrapolated; disclose the split. For very young cohorts (under 6 months old), LTV is almost entirely extrapolated and should not be reported as a hard number.

**Reading 4 — Cohort NDR at fixed cohort ages.** A cross-cohort comparison of net dollar retention at a fixed cohort age (e.g., "NDR at M12 by cohort"), presented as a trend chart:

```
Cohort NDR at M12
2023-01: 108%
2023-02: 112%
2023-03: 115%
...
2024-06: 122%
2024-07: 125%
```

The trend is the story. A rising NDR-at-M12 across successive cohorts is one of the strongest signals a SaaS company can present because it isolates a specific vintage effect from all other confounders. A falling NDR-at-M12 requires an explanation.

## Reading behaviour — the four cohort-shape patterns

The cohort table encodes four common patterns that a CFO should be able to name from the shape alone.

**Pattern A — "Smiling cohorts" (net-negative churn).** Layer 4 (NDR) declines briefly in the first few cohort months as some early churn plays out, then recovers and *exceeds* 100% as expansion revenue from the retained base overwhelms churn losses. This is the pattern that gives large enterprise SaaS companies their compounding revenue base. Bessemer's Cloud 100 companies exhibit this pattern; it is the pattern that supports NRR in the 130-150% range.

**Pattern B — "Healthy plateau."** Layer 2 (customer retention) drops in the first 90 days as unfit customers churn out, then plateaus at a level that persists for many cohort months. Layer 4 (NDR) stays around 100-110% — some expansion, some contraction, roughly netting. This is the typical mid-market SaaS pattern.

**Pattern C — "Steady leak."** Layer 2 declines linearly at a persistent rate, with no plateau. Layer 4 also declines because there is no expansion to compensate. The LTV that comes out of this pattern is bounded and typically produces a payback that extends beyond acceptable ranges. Investor conversations at this stage are about *why* the retention curve doesn't plateau — is it a customer-fit issue (wrong ICP), a product-value issue (customers don't get lasting value), or a competitive issue (customers switch)?

**Pattern D — "Falling out of bed."** Layer 2 declines steeply and continues to decline. Layer 4 tracks layer 2. This is a product-market-fit crisis and no unit-economics narrative rescues it — the CFO's job is to name the pattern to the board and the CEO's job is to fix the product or the ICP definition.

The pattern is a *cohort-by-cohort* judgement, not a company-wide one. A company can have pattern A for enterprise cohorts and pattern C for SMB cohorts in the same table. That fact is the story — it names which segment has healthy unit economics and which does not, and it usually shapes the S&M investment reallocation the CFO recommends.

## Cross-cohort drift — the deteriorating-recent-cohorts red flag

The specific pattern investors watch for most closely: successive cohorts have *systematically worse* early retention than older cohorts. Read off layer 2: the M3 retention percentage for the Jan 2024 cohort is 82%; for Feb 2024 it is 79%; for Mar it is 75%; for Apr it is 71%. Recent cohorts are worse than older cohorts by a persistent margin.

Common causes:

- **Marketing has moved down-market.** Recent acquisitions are lower-fit customers acquired via lower-cost channels (paid social with broad targeting, content that ranks for informational-not-commercial keywords). The CAC looks better but the LTV is worse.
- **Product has drifted from the ICP.** A pivot or feature-portfolio expansion has attracted customers whose use case the product doesn't serve well.
- **Competitive pressure.** A new entrant is picking off certain customers faster than before.
- **A pricing change.** A recent price increase priced out marginal customers.

Diagnosing the cause is a product-and-GTM exercise (owned by the Head of Growth or the CPO, chapter 7). The CFO's job is to *surface* the pattern before it appears in a diligence deck.

## The cohort table's relationship to the accrual P&L

The cohort table is monthly-recurring-revenue-based; the accrual P&L is ASC-606-recognised-revenue-based. For SaaS companies with mostly-ratable recognition and mostly-monthly billing, the two reconcile closely. For companies with material one-time revenue (implementation fees, professional services, milestone-billed contracts), the two diverge and the reconciliation is a specific piece of the model.

The convention: the cohort table tracks *subscription* MRR only. Non-recurring revenue and services revenue are tracked separately and neither enters the cohort table nor the LTV computation. The cohort-table-based revenue view will therefore always be smaller than the P&L revenue by the non-recurring portion, and the reconciliation should be documented. This is often the third-week diligence-recon exercise; producing it up front saves that cycle.

## Common cohort-table mistakes

Pre-diligence checklist:

- **Cohort assignment drift.** Customers whose signup date changes because of a data-migration or re-classification event show up in a different cohort than they started in, breaking the layer-1 monotonic-decline invariant.
- **Retention counted at the wrong grain.** Counting a customer as retained if *any* subscription is active, when the customer has actually downgraded from a $500/mo plan to a $50/mo plan. Layer 2 looks fine; layer 3 collapses.
- **Free-tier and paid mixed.** For PLG motions, mixing free-tier signups and paid-conversion cohorts in the same table without disclosure. Report both separately.
- **Non-subscription revenue included.** One-time revenue booked in a cohort's early months inflates the M0 and M1 revenue and creates an artificial retention drop when the one-time revenue rolls off. Track subscription MRR only.
- **Gross margin not per-cohort per-month.** Using a blended gross margin instead of the cohort-and-month-specific number, which understates or overstates layer 5 for some cohorts.
- **Cohort chart with too many cohorts.** A retention chart with 36 lines is unreadable. Group cohorts by quarter or half-year for the chart; keep the underlying table monthly.

## Summary

- A cohort is the set of customers who signed up in a specific period; the cohort table tracks the cohort's behaviour over cohort-relative months.
- The table is built in five layers: signup count → retention percentage → revenue → net dollar retention → gross profit and cumulative gross profit.
- Data preparation is the hard part — a clean MRR movement ledger is required; produce a data-quality reconciliation before building the table.
- Four readings come off the table: retention curves, payback per cohort, cohort LTV and LTV:CAC, and NDR-at-fixed-age trend.
- Four cohort-shape patterns are diagnostic: smiling (net-negative churn), healthy plateau, steady leak, falling-out-of-bed. Recognise the pattern from the shape.
- Cross-cohort drift — recent cohorts systematically worse than older cohorts — is the red flag investors look for hardest.
- The cohort table tracks subscription MRR only; reconcile to the accrual P&L up front.

Chapter 5 uses layer 4 of the cohort table to derive NRR and GRR at the company level. Chapter 6 turns to the capital-efficiency instruments that pair with unit economics in the CFO's diagnostic scorecard.
