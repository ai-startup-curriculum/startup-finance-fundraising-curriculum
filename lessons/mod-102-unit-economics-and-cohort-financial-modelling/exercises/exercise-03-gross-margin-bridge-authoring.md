# Exercise 03 — Gross-Margin Bridge Authoring

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 3 (gross-margin decomposition and bridge). Chapter 1 useful for the S&M / COGS distinction.

## Problem statement

Take one hypothetical startup's accrual-basis P&L for a quarter, plus its supporting cost-allocation records, and produce the gross-margin bridge — the reconciliation from revenue down to gross profit that names every material COGS bucket. Benchmark the result against published SaaS-margin bands (or marketplace take-rate bands, if applicable), and author the CFO narrative explaining the trend and the driver of any deviation from the benchmark.

The point of the exercise is to install the decomposition discipline: which lines go in COGS, which don't, how to defend the classification, and how to present the bridge to a board.

## Scenario — build your own

Use a real or hypothetical startup with:

- Accrual-basis P&L for a full quarter, with revenue at minimum $500K and a gross-margin story worth telling (either a healthy 75%+ SaaS margin, a distressed sub-70% SaaS margin, or a marketplace take-rate case).
- At least two prior quarters (for trend analysis) and, if possible, a year-ago quarter.
- Cost-allocation records that include: cloud-infrastructure bill (broken out by cost centre / environment if possible), third-party per-customer costs (payment processing, inference, telephony, or similar), headcount roster with function tagging (support / CS / delivery / R&D / SRE / G&A), and any professional-services or delivery revenue and cost tracked separately.
- A defensible split between subscription revenue and professional-services / delivery revenue if the company has both.

If constructing hypothetical data, pick a specific business type — pure SaaS, AI-native SaaS with material inference costs, marketplace, hardware-plus-software, or a hybrid — and build the P&L accordingly. Make sure at least one classification decision is genuinely ambiguous (a CSM whose role blends implementation and account management, an SRE team split between production ops and platform engineering, a payment-processing line that could be COGS or contra-revenue).

## Requirements

Produce the following:

1. **P&L (input).** Accrual-basis P&L for the quarter. Standard format — revenue at the top, cost of revenue, gross profit, S&M, R&D, G&A, operating income (loss), non-operating items, net income.
2. **Cost-allocation ledger (input).** Every material cost line with the classification decision: which bucket (COGS-hosting / COGS-third-party / COGS-support / COGS-CS-delivery / COGS-tenant-hosting / S&M / R&D / G&A) and the reason for the classification.
3. **Classification-decision memo.** For every ambiguous classification (at least three should exist), a specific paragraph naming the choice, the alternative, and the reason. The three most common ambiguities: (a) CSM headcount split between delivery (COGS) and account management (S&M), (b) SRE headcount split between production ops (COGS) and platform engineering (R&D), (c) third-party inference costs booked as COGS vs. R&D. If your scenario doesn't have all three, name the equivalent ambiguities that apply.
4. **The gross-margin bridge (headline artefact).** Revenue → COGS decomposed into five (or fewer) canonical buckets → gross profit, presented as a table with dollar values, percentage of revenue, and comparison to the prior quarter and the year-ago quarter. Include a benchmark comparison against the published band (Bessemer / Meritech / OpenView cite one specifically) for the company's segment.
5. **Product-line gross margin (if applicable).** If the company has material professional-services revenue, report subscription gross margin and services gross margin separately, both reconciling to the P&L blended number.
6. **Cohort gross-margin bridge (if data supports).** For one recent cohort, the cost-to-serve allocation to that cohort and the resulting cohort-specific gross margin. Compare to the blended company gross margin.
7. **Trend chart.** Gross margin by quarter for the last 4-6 quarters with a brief narrative explaining major inflection points.
8. **CFO narrative (max one page).** The story a CFO tells a board about the current-quarter gross margin. Includes: the current-quarter number, the movement from prior quarter (dollars and basis points), the driver(s) of the movement, the trajectory forecast, and any planned intervention.
9. **Diligence-defence memo (max half a page).** A short memo naming the classification decisions most likely to be challenged in diligence and the defence for each. If any classification is above the "aggressive" band (e.g., CSM entirely in S&M when 40% is delivery), name it explicitly and justify.

## Starter guidance

- Start with the P&L and produce it in its as-reported form. Then produce the classification ledger — every material line item tagged.
- For headcount-heavy classifications (support, CS, SRE), use fully-loaded compensation (salary × 1.30 or your scenario's burden rate, plus SBC if material). Salary-only loading understates COGS meaningfully.
- For the ambiguous classifications, don't pick the friendliest one — pick the defensible one. A CSM who spends 60% on implementation and 40% on account management belongs 60% in COGS and 40% in S&M.
- For the benchmark comparison, cite the specific published data source and its year. If the current-year data is unavailable at your workstation, note the date of the most recent available data in the citation.
- For the trend, look for step changes (a new product launch that shifted margin, a hosting-optimisation project, a mix shift toward enterprise or SMB) and name them explicitly.
- The CFO narrative is the artefact that goes to the board. Practice keeping it under one page — the trend + the driver + the forecast + the intervention, in that order.

## Acceptance criteria

- **The bridge ties to the P&L.** Revenue on the bridge equals revenue on the P&L; each COGS bucket sums to the P&L's cost-of-revenue line; gross profit ties.
- **The five canonical COGS buckets are named.** Hosting, third-party COGS, support, CS delivery / professional services, application hosting for customer environments. Not every bucket will be material for every company; a company with no professional-services revenue can drop that line, but the empty categories should be noted so a reviewer sees they were considered.
- **Every material classification decision has a written justification.** Not just "it's COGS" — the reason for the classification.
- **The benchmark comparison names the specific band and the source.** "Bessemer 2024 SotC benchmark for Series-B SaaS is 74-80% subscription gross margin" is a defensible statement; "typical SaaS margin is 70-80%" is not.
- **If the margin is below the investor-scepticism threshold, the narrative names the reason and the path back.** A 65% SaaS gross margin needs a story ("high inference costs in the new AI product line, projected to compress to 72% within 18 months as inference caching completes"). A margin above the band also needs a note — an unusually high number invites the question "what am I missing?"
- **The diligence-defence memo names at least three classification decisions that will be challenged.** These are the specific line items a diligence firm will re-classify.

## Deliverables

- Spreadsheet or notebook with the P&L, the cost-allocation ledger, the gross-margin bridge, and the trend chart.
- Classification-decision memo (Markdown or PDF).
- CFO narrative (one page).
- Diligence-defence memo (half a page).

## Extensions (optional)

- Repeat the analysis for a marketplace scenario — GMV, take-rate, and take-rate gross margin — with a benchmark comparison against Bill Gurley / a16z marketplace take-rate ranges.
- Model a mix-shift scenario: what does the gross margin look like if the company's next-year mix shifts 20% from SMB to enterprise?
- Model an AI-native scenario with inference costs at 15% of revenue: what would the gross margin need to look like in 24 months for the company to be defensible against the 70% SaaS benchmark?
- Author the appendix slide (one page) that would go into a fundraise deck — the gross-margin bridge with the benchmark comparison and the CFO narrative.
