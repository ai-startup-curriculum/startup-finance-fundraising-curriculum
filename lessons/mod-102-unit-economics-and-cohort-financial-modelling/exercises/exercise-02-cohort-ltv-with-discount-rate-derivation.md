# Exercise 02 — Cohort LTV with Discount Rate Derivation

**Estimated time:** ~3 hours
**Prerequisites:** Chapters 1 (fully-loaded CAC), 2 (cohort LTV and the discount rate), and 3 (gross margin) — Exercise 01 provides CAC inputs.

## Problem statement

Compute cohort LTV three ways for one mature cohort (12+ months of observation) — (a) the naïve `ARPU × gross margin ÷ churn` shortcut, (b) an undiscounted cumulative-cohort-gross-profit sum across a 60-month horizon, and (c) a properly-discounted present-value cohort LTV at a defensible discount rate and truncation horizon. Compare all three to the fully-loaded CAC for the cohort, produce the LTV:CAC ratio under each view, and defend the discount rate choice in the methodology memo.

The point of the exercise is to feel the size of the delta between the three views and to internalise why an "undiscounted 5-year LTV" is a specific pattern investors will not accept.

## Scenario — build your own

Use a real or hypothetical company with:

- One cohort with at least 12 full months of retention and revenue observation data — 40-150 customers in the M0 count is a reasonable range.
- A cohort-level MRR history — for each cohort-month M, the total MRR produced by the retained portion of the cohort.
- A per-cohort cost-to-serve model — the gross margin applicable to this cohort's revenue in each cohort-month (which may differ from the blended company gross margin per chapter 3).
- A fully-loaded CAC for the cohort — the per-customer CAC computed via the exercise-01 methodology, or a defensible placeholder.
- Optional but preferred: retention data from 2-3 successive cohorts so you can benchmark this cohort against a trend.

If constructing hypothetical data, model a retention curve with a realistic shape — steep early drop (first 90 days), plateau, then modest slow decline — rather than a smooth exponential.

## Requirements

Produce the following:

1. **Cohort data table (input).** For the chosen cohort: M0 customer count, retained customer count at each cohort-month M through M+12 (or M+24 if data supports), MRR per retained customer at each cohort-month, and cohort gross margin at each cohort-month.
2. **Naïve LTV computation.** Apply `ARPU × gross margin ÷ monthly churn`, using the cohort's M0 ARPU, blended cohort gross margin, and the implied monthly customer-count churn rate from the cohort's observed retention curve. Report the number.
3. **Undiscounted cumulative cohort GP.** For each cohort-month M, compute (retained count at M) × (ARPU at M) × (cohort GM at M) = monthly gross profit. Sum over M = 0 through M = 60. This is the undiscounted 60-month cohort LTV.
4. **Discounted cohort LTV — three discount-rate views.** Compute the present value of the same gross-profit stream under three discount rates: 0% (equivalent to undiscounted), 25% annual, and 35% annual. Truncate at 36 months for the 25%/35% views (Series-A convention).
5. **Extended-horizon view (optional).** Extend the 35% discounted view to 60 months and compare to the 36-month truncation, showing how much of the total PV comes from months 37-60.
6. **Discount-rate defence memo (max half a page).** State the discount rate chosen for the headline view, cite the venture-stage rationale (Damodaran on private-company cost of equity, Kupor on inside-the-VC-firm required IRRs, Feld & Mendelson on venture-return distributions, or the current-year Cambridge Associates / Preqin private-equity return data), and explain why a lower rate (e.g., mature-company WACC) is not defensible for the stage.
7. **Horizon-defence memo (max half a page).** State the truncation horizon chosen for the headline view (24, 36, or 60 months), and defend it against the observed cohort data (how much of the retention curve is empirical vs. extrapolated).
8. **LTV:CAC ratio comparison table.** For each of the four LTV views (naïve, undiscounted 60-month, discounted 36-month at 25%, discounted 36-month at 35%), show LTV, LTV:CAC ratio, and payback period. Order from most-optimistic to most-conservative.
9. **Diligence-defensibility memo (max one page).** Which of the four LTV views would you put on the fundraise deck? Which would you cite in the appendix / methodology? Which would you never show? What specifically is the failure mode of each view you exclude?

## Starter guidance

- Start with the cohort table — it drives everything. If you don't have real cohort data, model a retention curve: 100% at M0, drop to 80-85% by M3, drop to 70-75% by M6, drop to 65-70% by M12, flatten toward 55-60% by M24.
- For the naïve view, use monthly customer-count churn — total-customer-life is 1 / monthly churn rate, and LTV = ARPU × GM ÷ monthly churn. This will produce the largest number.
- For the discounted views, convert the annual rate to monthly: `r_monthly = (1 + r_annual)^(1/12) - 1`. At 35% annual this is ~2.53% monthly.
- For a cohort with real expansion (per-customer ARPU rising over time), the discounted 36-month view can approach or exceed the undiscounted 60-month view. Interesting cohort data will show this crossover.
- The extended-horizon view (M37 to M60) usually contributes a small fraction of total PV at 35% discount rates — a specific empirical demonstration that truncating at 36 months doesn't cost much.

## Acceptance criteria

- **All four LTV views produce a specific dollar number.** No hand-waves; each number is computable from the cohort data table with a documented formula.
- **The four numbers are ordered as expected** — naïve LTV > undiscounted 60-month > discounted 36-month at low rate > discounted 36-month at high rate. If your ordering differs, either the arithmetic is wrong or the cohort has an unusual expansion profile (in which case, name it).
- **The delta between the highest and lowest LTV is at least 2×.** If it isn't, either the discount rate is too low or the retention curve is too front-loaded for the effect to materialise.
- **The discount-rate defence cites a specific source.** Not "we chose 35% because it seemed right"; a specific reference (Damodaran, Cambridge Associates, Preqin, an explicit inside-the-VC-firm return-target chain).
- **The horizon defence names the empirical-vs-extrapolated split.** For a 36-month horizon on a 12-month-old cohort, 24 months are extrapolated; disclose it.
- **The diligence-defensibility memo names the failure mode of the excluded views.** "The naïve view is wrong because…" — a specific sentence per view.

## Deliverables

- Spreadsheet or notebook with the cohort data, the four LTV computations, and the LTV:CAC comparison table.
- Discount-rate defence memo.
- Horizon defence memo.
- Diligence-defensibility memo.

## Extensions (optional)

- Repeat for three cohorts of different vintages and show how LTV per cohort has trended.
- Add explicit expansion modelling — model per-customer ARPU as growing 1-2% per cohort-month for the retained population — and show the effect on cohort LTV.
- Compute the sensitivity of LTV to a 500-bps change in the discount rate. What is the elasticity?
- Author the appendix slide (one page) that would go into the fundraise deck's methodology section, showing all three cohort-LTV views with a discount-rate footnote.
