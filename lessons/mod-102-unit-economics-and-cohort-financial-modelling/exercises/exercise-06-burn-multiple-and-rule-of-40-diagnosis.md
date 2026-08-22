# Exercise 06 — Burn Multiple, Cash Conversion Score, and Rule of 40 Diagnosis

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 6 (capital-efficiency instruments). Chapters 1, 3, and 5 for the inputs (CAC, gross margin, NRR).

## Problem statement

Take one startup's trailing-twelve-month financials, its historical capital-raise records, and its ARR trend, and produce the three capital-efficiency scorecard metrics — burn multiple, cash conversion score, and Rule of 40 — benchmarked against current-year published data. Diagnose which of the four levers (top-line growth, gross margin, S&M efficiency, R&D allocation) is failing and author the CFO's board memo prescribing corrective action.

The point of the exercise is to install the scorecard mechanics, the benchmark-lookup discipline, and — most importantly — the diagnostic move from "the number is bad" to "here's specifically what is causing it and what we're doing about it."

## Scenario — build your own

Use a real or hypothetical startup with:

- Trailing-twelve-month accrual financials (P&L, balance sheet snapshots for start and end, cash-flow statement for the TTM).
- ARR series by month for the TTM (starting and ending ARR; ideally monthly snapshots).
- Complete capital-raise history: every priced round and every convertible instrument, with the amount raised and the date.
- Current cash balance.
- Function-level expense breakdown: S&M, R&D, G&A as percentages of revenue.
- The unit-economics numbers from prior exercises: fully-loaded CAC by channel, cohort GM, NRR / GRR.

Pick a scenario that is *diagnostically interesting* — a company where at least one of the three scorecard metrics is outside the healthy band. A perfectly healthy company doesn't test the diagnostic skill. Consider:

- A company at $22M ARR with 80% growth but a 2.5× burn multiple (S&M inefficiency likely).
- A company at $10M ARR with a 0.25 cash conversion score (cumulative capital efficiency is weak).
- A company at $40M ARR with a Rule of 40 score of 25 (the growth-vs-profitability balance is off).

## Requirements

Produce the following:

1. **Financial-summary input.** Compact financial snapshot: TTM revenue, TTM ARR (start and end), gross profit (dollars and %), operating expenses by function (S&M, R&D, G&A), operating income / loss, cash used in operations, cash used in investing, cash from financing, ending cash.
2. **Capital-raise history table.** One row per instrument (SAFE, note, priced round, debt), amount, date. Sum to total capital raised.
3. **Burn multiple computation.** Net burn = (cash used in operations + cash used in investing), TTM. Net-new ARR = ending ARR − starting ARR. Ratio. Present computation stepwise with the source of each input.
4. **Cash conversion score computation.** Current ARR ÷ (total capital raised − current cash). Present computation stepwise.
5. **Rule of 40 computation.** YoY ARR growth (%) + TTM FCF margin (%). Present computation stepwise. Note the specific definition of FCF used (operating cash flow − capex is the standard).
6. **Benchmark-lookup table.** For each of the three metrics, the current-year published benchmark from at least one authoritative source (OpenView, Bessemer, KeyBanc, Meritech). Include the specific report name, year, and the segment / ARR band cited.
7. **Scorecard summary.** A single table:

   | Metric | Value | Benchmark band (source, year) | Status | Diagnosis (one sentence) |
   |---|---|---|---|---|
   | Growth rate | X% | Y-Z% | ✓/✗ | ... |
   | Gross margin | X% | Y-Z% | ✓/✗ | ... |
   | Burn multiple | X× | Y-Z× | ✓/✗ | ... |
   | Cash conversion score | X | Y-Z | ✓/✗ | ... |
   | Rule of 40 | X% | Y-Z% | ✓/✗ | ... |
   | NRR | X% | Y-Z% | ✓/✗ | ... |
   | GRR | X% | Y-Z% | ✓/✗ | ... |
   | Payback (median cohort) | X mo | Y-Z mo | ✓/✗ | ... |

8. **Lever diagnosis (max one page).** Given the scorecard, which of the four levers (top-line growth, gross margin, S&M efficiency, R&D allocation) is the primary cause of the failing metric(s)? Include specific quantification — "S&M is 55% of revenue, benchmark is 40-45%; the excess $X of S&M spend produces the elevated burn multiple. Reduction to 45% would improve burn multiple to Y×."
9. **Function-mix analysis.** S&M / R&D / G&A as percentages of revenue, compared to segment benchmarks. Common ranges (verify against current sources):
   - S&M: 40-60% at Series-A/B, compressing to 30-45% at growth-stage.
   - R&D: 30-45% at Series-A/B, compressing to 20-30% at growth-stage.
   - G&A: 10-20% typically.
   Any function materially above the benchmark is a candidate lever.
10. **Corrective-action plan (max one page).** For the diagnosed lever(s), the specific operational actions the CFO recommends, the expected timeline for the scorecard metrics to reflect the action, and the risks (e.g., cutting S&M reduces burn multiple but also slows top-line growth — model the trade-off).
11. **CFO board memo (max one page).** The three-section board memo: (1) scorecard with benchmarks, (2) diagnosis, (3) corrective actions with timelines. The memo is what goes to the board; the rest of the exercise's artefacts are appendices.

## Starter guidance

- Start with the financial-summary input and validate that the numbers reconcile — TTM revenue on the P&L should equal the run rate implied by the last month's ARR (approximately, adjusting for non-recurring revenue).
- For burn multiple, "net burn" is *cash* burn from ops and investing; it excludes financing (equity and debt inflows). Some CFOs report burn multiple on gross burn — flag your convention.
- For cash conversion score, the denominator is *net* capital deployed (total raised − current cash). A company that just raised a large round has cash sitting on the balance sheet; subtracting it isolates the capital actually consumed.
- For Rule of 40, use ARR growth (not revenue growth or billings growth) for the growth term at private-company scale. FCF margin is standard = (operating cash flow − capex) / revenue.
- For the benchmark lookup, cite specific sources. If the current-year OpenView SaaS Benchmarks report isn't in your workstation, use the most recent year available and note the date. Do not invent bands.
- For the lever diagnosis, quantify. "S&M is high" is not a diagnosis; "S&M is 55% of revenue vs. 42% benchmark, representing $2.6M of excess spend at $20M revenue" is.
- The corrective-action plan should be operationally specific. "Improve S&M efficiency" is a slogan; "reduce paid-search spend by 30% and reallocate $600K of the freed budget to content, projected to reduce blended CAC from $8K to $6.5K within 6 months" is a plan.

## Acceptance criteria

- **All three scorecard metrics are computable to a single number.** No ranges; the computation is deterministic given the inputs.
- **Each metric is compared to a cited benchmark.** Source, year, and segment / ARR band. Not general folklore.
- **The failing metric(s) are traced to a specific lever.** With quantification — how much of the metric's shortfall is attributable to the lever.
- **The corrective-action plan includes a projected metric improvement and a timeline.** "This action improves burn multiple from 2.5× to 1.8× within 3 quarters" — a specific claim, defensible against the model.
- **The board memo is one page maximum** and follows the scorecard → diagnosis → action structure. Longer memos don't get read.

## Deliverables

- Spreadsheet or notebook with the financial-summary input, all three scorecard computations, and the function-mix analysis.
- Scorecard summary table.
- Lever-diagnosis memo (one page).
- Corrective-action plan (one page).
- CFO board memo (one page).

## Extensions (optional)

- Model the sensitivity of the scorecard to each corrective action. If the S&M reduction improves burn multiple by 0.7×, what happens to Rule of 40 (which depends on growth rate, which may fall)? Show the trade-off matrix.
- Produce a 4-quarter forward projection of the scorecard under the corrective-action plan, and compare to the "no action" counterfactual.
- Model a "raise more capital" scenario vs. a "cut burn to extend runway" scenario; which is the better response given the scorecard?
- Author the appendix slide for the fundraise deck (Series-B contexts): the scorecard with benchmarks and the trend chart. The version that goes to prospective investors, not the internal board version.
