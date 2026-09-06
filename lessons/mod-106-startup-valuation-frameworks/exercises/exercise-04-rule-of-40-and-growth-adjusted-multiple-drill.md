# Exercise 04 — Rule of 40 and Growth-Adjusted Multiple Drill

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 4 (Rule of 40 and growth-adjusted multiples); output from exercise 03 (comp-set construction) is a useful — but not required — starting point.

## Problem statement

For a filtered comp set of publicly-traded SaaS companies, compute Rule of 40 for every constituent, run a growth-adjusted-multiple regression across the set, place a hypothetical Series-B target inside the growth-and-margin grid, and defend a specific target multiple with the combined regression plus Rule-of-40 adjustment plus private-market discount walk. Sensitise across margin-definition choices and market-cycle placement.

The drill's goal is to install two disciplines: (a) the mechanical process of fitting a defensible multiple to a specific growth rate using a small comp set, and (b) the negotiation posture of arguing for a placement inside a growth-and-margin grid cell rather than for a specific headline multiple.

## Scenario — build your own

Reuse or adapt the scenario from exercise 03 (a Series-B vertical-SaaS target at $30M NTM revenue, 60% growth, 78% gross margin, -20% FCF margin), or construct a new scenario at a different growth-and-margin band placement. If reusing, extend with:

- Historical growth trajectory: 90% two years ago → 75% last year → 60% NTM (base) → 45% projected year 2 (deceleration case) *or* 60% NTM → 55% projected year 2 (durable case). Pick one and note the durability implication.
- Stock-based compensation as a % of revenue: **15%** (typical for a growth-stage SaaS; adjust as you prefer).
- Optional: one-time or non-recurring items (a large multi-year prepayment recognised in cash, a one-time acquisition cost) that would distort a naive FCF-margin calculation.

Construct or reuse a filtered public-comp set of at least 8-12 constituents (10-15 is preferred for regression). Sources: Meritech Enterprise SaaS comparables, Bessemer Cloud Index. Cite the source date.

## Requirements

Produce a single workbook plus a memo:

1. **Comp-set tab.**
   - The filtered comp set from exercise 03 or a freshly-constructed one. For each constituent: ticker, name, NTM revenue growth, gross margin, FCF margin (public consensus or trailing), EV/NTM revenue multiple.
   - Compute Rule of 40 for each constituent: `Rule of 40 = NTM growth % + FCF margin %`.
   - Rank the constituents by Rule of 40.

2. **Rule of 40 tab.**
   - Compute the target's Rule of 40 under three margin-definition variants:
     - Rule of 40 with FCF margin (Meritech / Bessemer convention).
     - Rule of 40 with EBITDA margin (excluding depreciation, amortisation).
     - Rule of 40 with adjusted-EBITDA margin (also excluding stock-based compensation).
   - Compare the target's Rule of 40 against the comp-set median under the same margin definition. Note the gap (target above / below).
   - Discuss which margin definition is most defensible for the target's pitch context and why.

3. **Growth-adjusted regression tab.**
   - Plot the (NTM growth, EV/NTM multiple) pairs from the filtered comp set.
   - Fit a linear regression: `EV/NTM = a + b × growth %`.
   - Report the fitted `a` (intercept), `b` (slope), and R² (goodness-of-fit).
   - Apply the fitted regression to the target's NTM growth rate.
   - Optionally also fit a polynomial (quadratic) or a log-transform and compare fit quality.
   - Flag any comp-set outliers that materially move the regression coefficients and rerun the regression excluding them; compare the two fits.

4. **Growth-and-margin grid tab.**
   - Build the 4×4 grid: growth bands (hyper-growth 60%+ / high-growth 30-60% / steady-growth 15-30% / low-growth <15%) crossed with margin bands (top-tier 20%+ FCF / solid 5-20% / break-even -5% to +5% / loss-making worse than -5%).
   - Place each comp-set constituent in a grid cell. Compute the median EV/NTM within each populated cell.
   - Place the target in a grid cell and identify the cell's median multiple.
   - Note border cases — constituents (and the target) sitting near the boundary between two cells — and the negotiation implication of a placement debate.

5. **Rule-of-40-adjusted multiple tab.**
   - Start from the fitted regression multiple for the target's growth rate.
   - Adjust up or down for the target's Rule of 40 vs. the comp-set median Rule of 40 (as discussed in chapter 4).
   - Cross-check the adjusted multiple against the grid-cell median from the previous tab.
   - Cross-check against the comp-set interquartile range.
   - Apply the private-market discount (per chapter 3 and exercise 03) to reach the target's private-market multiple.
   - Compute the implied enterprise value: `multiple × NTM revenue`.

6. **Growth-durability sensitivity tab.**
   - Rerun the fitted-multiple calculation using year-2 growth (the deceleration case) instead of NTM growth. Compare the resulting multiple.
   - Alternatively, apply an explicit growth-persistence factor: discount the fitted multiple by 10-15% for a decelerating trajectory; leave unadjusted for a durable trajectory.
   - Sensitise the target valuation across durable vs. decelerating growth cases.

7. **Market-cycle overlay tab.**
   - Pull the Bessemer Cloud Index historical time series ([cloudindex.bvp.com](https://cloudindex.bvp.com/)) and compute the current-quarter median EV/NTM multiple vs. the 5-year median.
   - Note whether the current cycle is at a premium or discount to the historical median, and by how much.
   - Discuss whether the target's derived multiple should be further adjusted for the market cycle (either downward for a cyclical peak or upward for a cyclical trough).

8. **Multiple-derivation memo.**
   Written to the CEO / lead investor as the substantive multiple-derivation section of the valuation memo (2 pages):
   - The target's Rule of 40 under each margin-definition variant and the chosen definition.
   - The fitted-multiple regression and its application to the target's growth rate.
   - The grid-cell placement of the target and the cell's median multiple.
   - The Rule-of-40 adjustment and the derived pre-discount multiple.
   - The private-market discount and the final target multiple.
   - The market-cycle context and any additional adjustment.
   - The implied pre-money and the walk-away floor.
   - A specific slide (or paragraph) preparing for the pushback the CFO expects at the negotiation — likely on grid-cell placement, on growth durability, or on the market-cycle interpretation.

## Starter guidance

- **A regression on <8 points is noise.** If your filtered comp set is fewer than 8 constituents, don't run the regression; use the median and interquartile range only. If you must run the regression on a small set, disclose the R² and treat it as suggestive.
- **Do not extrapolate.** A regression fit on 20-60% growth companies does not defensibly extend to a 100%-growth target or a 5%-growth target. Extrapolation is a red flag.
- **Match the margin definition to the comp-set convention.** Meritech and Bessemer use FCF margin as the Rule-of-40 default. If you pitch on adjusted-EBITDA (which is more flattering), the counterparty will restate on FCF and the multiple discussion resets. Disclose your definition and match the comp-set convention.
- **Grid-cell placement is the negotiation lever.** A target at 32% growth can defensibly place itself in the "high-growth" or "steady-growth" cell. The two cells often have materially different median multiples. Prepare a specific argument for the placement.
- **The Rule-of-40 adjustment is a soft factor.** A target with Rule of 40 = 60 in a comp set with median Rule of 40 = 40 supports a modest upward adjustment to the fitted multiple (maybe 10-15%). It does not support a 2× adjustment. Keep the adjustment proportionate.
- **Growth durability is the sharpest single input.** A target decelerating from 90% two years ago to 60% NTM to 45% in year 2 does not trade like a target with stable 60% growth. Apply an explicit persistence factor or run the multiple on year-2 revenue.
- **The market cycle matters.** In a compressed cycle, the fitted multiple is depressed relative to historical. In an expanded cycle, it's elevated. Note the placement in the memo.

## Acceptance criteria

- **Rule of 40 is computed for every comp-set constituent** and for the target under three margin-definition variants.
- **The regression is defensible** — 8+ constituents, R² reported, outliers flagged, linear or log fit chosen with rationale.
- **The 4×4 grid is populated** with cell medians and the target is placed with a rationale for placement.
- **The multiple walk is explicit** — fitted → grid-cell cross-check → Rule-of-40 adjustment → private-market discount → target multiple → implied pre-money.
- **Growth-durability sensitivity is quantified** with a specific comparison between durable and decelerating cases.
- **Market-cycle context is named** with a specific comparison of current-quarter vs. 5-year median from Bessemer or a comparable time series.
- **The memo is prepared for pushback** on grid-cell placement, growth durability, and market-cycle interpretation.

## Deliverables

- The workbook with all eight tabs.
- The multiple-derivation memo (Markdown or PDF, 2 pages).
- The specific slides or paragraphs prepared for negotiation pushback.

## Extensions (optional)

- **Include a Rule-of-50 top-tier subset.** Rerun the regression on constituents passing Rule of 50 only. Compare the fitted multiple to the full-set regression. Discuss when the Rule-of-50 subset is the defensible comp set (top-quartile targets) and when it isn't (mid-band targets).
- **Model an NRR overlay.** Extend the regression to include net revenue retention (NRR) as a second explanatory variable. Compare a two-variable fit (growth + NRR) against the single-variable fit. Discuss when NRR is a meaningful marginal explanatory variable and when it is subsumed by growth.
- **Add a magic-number / sales-efficiency layer.** Compute the "magic number" (net new ARR / prior-period sales-and-marketing spend) for each constituent where the disclosure supports it, and discuss whether targets at similar growth rates but different magic numbers trade at different multiples.
- **Cross-check against Damodaran's academic multiples.** Aswath Damodaran at NYU Stern publishes industry-median multiples annually ([pages.stern.nyu.edu/~adamodar/New_Home_Page/dataarchived.html](https://pages.stern.nyu.edu/~adamodar/New_Home_Page/dataarchived.html)). Compare his software industry EV/Sales to your fitted regression at the median growth rate; discuss any divergence.
- **Rerun with the market at cyclical extremes.** Pull the Bessemer Cloud Index at two historical dates — one at a cyclical peak (e.g., Q4 2021), one at a cyclical trough (e.g., Q4 2022) — and rerun the regression on each. Compute what the same target would have been priced at in each cycle. Discuss the implication for negotiation timing.
