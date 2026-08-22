# Exercise 06 — Rule 701 Cap Monitoring Drill

**Estimated time:** ~2.5 hours
**Prerequisites:** Chapter 6 (Rule 701 caps and Form S-8 graduation).

## Problem statement

Build a rolling-12-month Rule 701 consumption tracker for a Series-B-stage startup across 24 months of grant activity. Compute the three alternative caps ($1M / 15% of assets / 15% of outstanding common) at each month-end, identify the binding cap, and monitor headroom. Then design a **grant-scheduling recommendation** for a $12M-of-notional VP hire whose grant would push the company past the $10M disclosure threshold in a rolling 12-month window, and produce the required disclosure package if the grant proceeds.

The exercise builds the monitoring discipline and the disclosure-package readiness that late-stage private companies actually need.

## Scenario — build your own

Design a Series-B company grant / financial-position timeline over 24 months. Suggested minimum shape:

- **Month 0:** Series-B closes at $30M raised, post-money $150M. Total assets $40M ($30M cash + $10M other). Common outstanding: 10M shares at current 409A FMV $2.00. Existing option pool: 3M shares reserved, 2M granted.
- **Grants per month:** average 100K-300K options granted per month (varying — some quiet months, some big-hire months), at the then-current 409A strike.
- **Month 3:** Fresh 409A: FMV $2.20/share.
- **Month 8:** A single large grant: VP Sales hire, 500K shares at then-current FMV of $2.20 = $1.1M nominal.
- **Month 9:** Fresh 409A after a strong quarter: FMV $2.60/share.
- **Month 12:** Series-B annual audit completes; financial statements now audited.
- **Month 15:** Cash still $22M, total assets $35M. Common outstanding 10.5M (some options exercised). 409A: FMV $3.00/share.
- **Month 18:** Very-large VP grant proposed: VP Product, 4M shares at $3.00 = $12M nominal in one grant. This is what pushes past $10M in a rolling 12-month window when combined with the prior year's normal grant activity.
- **Month 24:** End of drill window; produce a report of the year in Rule 701.

You may vary the specific numbers but keep the shape so the $10M disclosure threshold is hit in a plausible way.

## Requirements

Produce a single spreadsheet workbook with the following:

1. **Monthly grant register.** One row per month with the total grant activity in that month (options granted × strike, RSU shares × FMV, restricted stock × purchase price). Show the specific large grants (VP hires) as separate line items so they're identifiable.
2. **Monthly balance-sheet snapshot.** Total assets and common outstanding at each month-end, drawn from your assumed trajectory.
3. **Monthly cap calculation.** For each month:
   - Alternative 1: $1,000,000.
   - Alternative 2: 15% of total assets from the most recent quarter-end balance sheet.
   - Alternative 3: 15% × common outstanding × current FMV.
   - Binding cap = MAX of the three, in $.
4. **Monthly rolling-12-month consumption.** Sum of grant activity in the trailing 12 months in $.
5. **Headroom column.** Binding cap − trailing-12-month consumption. Flag any month where headroom is negative (cap breach) or where trailing-12 exceeds $10M (disclosure threshold triggered).
6. **Report tab.** Chart of trailing-12-month consumption vs. binding cap and vs. the $10M disclosure threshold over the 24 months.
7. **Month-18 grant-scheduling memo (2 pages).** The VP Product grant will push trailing-12 above $10M (compute the specific amount). Options:
   - **Option A: Proceed with the full grant now.** Trigger the disclosure obligation. Prepare the disclosure package (see item 8).
   - **Option B: Phase the grant.** Break the 4M-share grant into two tranches — 1.5M now, 2.5M at month 21 or on a milestone — to keep trailing-12 under $10M. Analyse whether this defers or eliminates the disclosure trigger.
   - **Option C: Structure differently.** Grant partly as an ISO / NSO stack + partly as an RSU with a first-vest / settlement timed to reduce measurement. Discuss what this would achieve.
   Recommend one, with rationale and specific mechanics.
8. **Disclosure package (2-3 page outline).** If Option A is chosen, sketch the disclosure package the company would provide to each grantee above the $10M threshold. Include:
   - The equity incentive plan document reference.
   - The set of risk factors (5-8 specific risks) tailored to this company.
   - The specific financial statements to be provided (audited or unaudited; balance sheet as-of date; income-statement period; cash-flow-statement period).
   - A cover memo explaining what the disclosure is and why the grantee is receiving it.
   - The specific date each element will be provided (must be a reasonable period before the grant date).
9. **Corporate-governance checklist.** For the chosen option, list the board / stockholder actions required (board consent for the grant; possibly stockholder consent if the grant exceeds pool authorisation; documentation of the disclosure delivery).

## Starter guidance

- **The rolling-12-month calculation is not a calendar year.** At month 18, the rolling window is months 7-18 inclusive. Make sure your formula rolls correctly.
- **Measurement convention.** For options, the consumption is exercise price × shares underlying, measured at grant date. Some CFOs use exercise price alone; some (more conservatively) use exercise price + spread at grant. If your assumed grants are struck at FMV, spread at grant is zero so both give the same answer — but note the convention.
- **The $10M threshold is aggregate**, not per-grantee. Trailing-12 across all grants combined. Don't allocate per-grantee.
- **The 15%-of-assets alternative usually dominates at Series-B stage.** Total assets includes cash, AR, prepaids, PPE, intangibles. If your assumed asset base is $35-40M, the 15% cap is $5.25-6M — likely binding.
- **The disclosure package is a real document.** Sketching it forces you to think about *what* a grantee would actually need to know. The risk factors should read like a mini-S-1 risk-factors section, not a boilerplate list.
- **The grant-scheduling recommendation should be actionable.** If Option B is chosen, specify the tranche amounts and dates; don't just say "phase it."

## Acceptance criteria

- **All three cap alternatives are correctly computed** each month, and the binding cap is identified.
- **Rolling-12-month consumption is correctly rolling** (i.e., month 18's number is months 7-18 sum, not months 1-18 sum).
- **The chart shows the year in Rule 701** — consumption trajectory, binding cap trajectory, and $10M threshold clearly plotted.
- **Any cap breach or threshold crossing is flagged** with a specific month and amount.
- **The Month-18 grant-scheduling memo names all three options**, quantifies each, and makes a specific recommendation.
- **The disclosure package outline names specific risk factors and specific financial statements** — not generic placeholders.
- **The corporate-governance checklist is executable** (a board / GC could follow it to implement the chosen option).

## Deliverables

- The workbook with the register, cap calculation, rolling consumption, headroom, and chart.
- The 2-page grant-scheduling memo (Markdown or PDF).
- The 2-3-page disclosure package outline.
- The corporate-governance checklist (may be a subsection of the memo).

## Extensions (optional)

- Model a **repricing event** at month 20 (fresh 409A after a market reset shows FMV falling from $3.00 to $1.80). Compute the Rule 701 consumption implications — repricings can create fresh Rule 701 consumption on the repricied options in some interpretations. Document your treatment.
- Extend the timeline through pre-IPO (month 30 S-1 draft; month 34 IPO priced with Form S-8 filed at IPO). Show how the Rule 701 constraint dissolves at S-8 filing.
- Author a **historical audit** of the company's Rule 701 posture over the last 3 years — the pre-IPO due-diligence workstream. Identify any cap breaches or missed disclosures, and design the remediation.
- Compare the Rule 701 disclosure obligation trigger ($10M / 12 months) to the SEC's other private-company disclosure regimes (Reg D, Reg A, Rule 144A) and discuss where the boundary sits.
