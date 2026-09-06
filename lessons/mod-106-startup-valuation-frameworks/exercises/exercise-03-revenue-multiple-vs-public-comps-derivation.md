# Exercise 03 — Revenue-Multiple Derivation Against Public Comparables

**Estimated time:** ~5 hours
**Prerequisites:** Chapter 3 (revenue multiples and public comps); familiarity with [mod-103](../../mod-103-three-statement-model-and-driver-based-forecasting/) driver-based forecasting for the NTM revenue projection input.

## Problem statement

Build the full revenue-multiple valuation for a hypothetical Series-B SaaS target. Construct a target-specific public-comp set from either the Meritech Enterprise SaaS comparables or the Bessemer Cloud Index (preferably both, cross-checked). Filter the universe to the applicable growth-and-margin band. Compute the median and interquartile range. Apply an explicit private-market discount. Derive the target's applicable multiple range and the implied pre-money valuation. Author the valuation memo that walks the derivation from public-comp median through to private-market anchor.

The drill's goal is to install the discipline of comp-set construction as an explicit, defensible, auditable process — where every inclusion / exclusion decision, every filter, and every discount is named, sourced, and defensible against a counterparty who is running the same analysis with different (possibly aggressive) choices.

## Scenario — build your own

Construct a hypothetical Series-B target company:

- Delaware C-corp, incorporated 4 years ago.
- Vertical SaaS for a specific industry (pick one you can plausibly describe — e.g., legal-tech, healthcare-provider admin, construction PM, restaurant ops, logistics workflow).
- Business model: subscription (monthly or annual contracts, dominant recurring revenue).
- Buyer profile: mid-market or enterprise (pick one; note the ACV band).
- NTM revenue projection: **$30M** (base case, from your driver-based model).
- NTM revenue growth: **60% YoY** (base case).
- Gross margin: **78%** (base case).
- NTM FCF margin: **-20%** (base case).
- Net revenue retention (NRR): **115%** (base case).
- CAC payback: **~18 months**.
- Fundraising target: **$25M Series-B round** on a pre-money to be determined.

Extend the scenario with any additional detail needed to make the comp-set filter decisions coherent (buyer profile, sales motion, expansion vs. new-logo mix, etc.).

## Requirements

Produce a single workbook (Excel or Google Sheets) with the following tabs, plus a valuation memo:

1. **Assumptions tab.**
   - The scenario inputs above, plus explicit assumptions for base / bull / bear NTM revenue projections, growth-and-margin band placement rationale, and the specific comp-set filter criteria you will apply.
   - Cite the specific report date and download URL for the comp source you use (Meritech at [meritechcapital.com/public-comparables/enterprise-saas](https://www.meritechcapital.com/public-comparables/enterprise-saas) and/or Bessemer Cloud Index at [cloudindex.bvp.com](https://cloudindex.bvp.com/)).

2. **Universe tab.**
   - Full pull of the current-day Meritech Enterprise SaaS comparables (or Bessemer Cloud Index constituents), with the following columns for each constituent: ticker, name, market cap, enterprise value, LTM revenue, NTM revenue, EV/LTM, EV/NTM, NTM growth, gross margin, FCF margin, Rule of 40.
   - Note the source date on the tab. Multiples move; capture the specific timestamp.

3. **Filtered comp set tab.**
   - Apply the filter criteria explicitly:
     - **Vertical / horizontal SaaS split.** Exclude constituents whose product doesn't match the target's vertical scope.
     - **Business model.** Exclude usage-based / consumption companies if the target is subscription-only (or vice versa).
     - **Buyer profile.** Exclude SMB-only constituents if the target is mid-market / enterprise (or vice versa).
     - **Growth band.** Filter to the target's growth band ± reasonable margin (e.g., target at 60% → filter to 40-80% growth).
     - **Margin band.** Cross-filter on gross margin (± 5 percentage points from target).
   - Document each filter decision in the tab with a one-line rationale.
   - Flag any outliers (e.g., constituents at the extreme ends of the multiple range) and note the company-specific reason (recent acquisition, activist involvement, product cycle) for excluding or discounting them.
   - Compute median, mean, 25th percentile, 75th percentile of EV/NTM revenue for the filtered set.

4. **Private-market discount tab.**
   - Reference the Damodaran illiquidity discount data (Aswath Damodaran's [NYU Stern page](https://pages.stern.nyu.edu/~adamodar/) publishes the current-year illiquidity/private-company discount analysis; the *Investment Valuation* textbook is the primary source).
   - Cross-reference with the Kroll (formerly Duff & Phelps) Valuation Handbook or the AICPA Practice Aid on privately-held company equity securities as compensation.
   - Choose a discount level with an explicit rationale (typically 30-50% at Series-B; document the specific level and reasoning).
   - Show the calculation: `private-market multiple = public-comp median × (1 - discount)`.

5. **Target valuation tab.**
   - Compute the target's implied enterprise value at:
     - Median of the filtered comp set × NTM revenue, discounted.
     - 25th percentile × NTM revenue, discounted (bear anchor).
     - 75th percentile × NTM revenue, discounted (bull anchor).
   - Sensitise across base / bull / bear NTM revenue projections.
   - Produce the pre-money range: bear-to-median-to-bull.

6. **Cross-check tab.**
   - Cross-check the derived pre-money range against a second comp source (if you started with Meritech, cross-check against Bessemer; if you started with Bessemer, cross-check against Meritech; or against a Damodaran industry-average dataset from [pages.stern.nyu.edu/~adamodar/New_Home_Page/data.html](https://pages.stern.nyu.edu/~adamodar/New_Home_Page/data.html)).
   - Cross-check against the market-conditions data (chapters 6-7) — current-quarter Series-B median pre-money from PitchBook-NVCA, Wilson Sonsini, or Carta.
   - Note any divergence >25% between the derived pre-money and the market-conditions median and hypothesise the cause (comp-set filter mismatch, discount level, market-cycle placement).

7. **Valuation memo.**
   Written to the founder / CEO (2-3 pages, Markdown or PDF):
   - Executive summary: recommended pre-money range and specific defended point.
   - Comp-set construction walk-through: universe → filter → median → discount → target multiple → pre-money.
   - Named parameters and the argument for each (comp-set choice, discount level, growth-band placement).
   - The specific two or three arguments the CFO is prepared to defend against a counterparty who proposes a different comp set.
   - Market-conditions and cross-check reconciliation.
   - Walk-away floor and rationale.

## Starter guidance

- **Anchor on real, current-day data.** Do not use invented multiples. Pull the Meritech or Bessemer table at a specific timestamp and cite it. Multiples move quarter-to-quarter — a comp set that was defensible six months ago may not be defensible today.
- **The filter is the load-bearing decision.** Two analysts with the same universe and different filters can produce pre-money ranges that differ by 2×. Document every filter decision with a specific rationale, and be ready to defend it against a counterparty who proposes a different filter.
- **Do not cherry-pick.** The temptation is to include the constituents that support the highest multiple and exclude those that don't. Resist. The counterparty will run the same analysis; a filter that is provably aggressive damages credibility.
- **Note outliers explicitly.** Every comp set has one or two constituents trading at the extreme of the multiple range for company-specific reasons. Excluding them is defensible if named; leaving them in the median without noting them is a diligence red-flag.
- **Use NTM revenue, not ARR.** The public-comp multiples apply to GAAP revenue for the next twelve months. ARR is not the same thing; applying a revenue multiple to an ARR figure overstates the valuation by the growth gap.
- **Apply the private-market discount explicitly.** A memo that quotes the public median as the private-round anchor is a memo that the market won't clear. The discount is real; name the level and the source.
- **Distinguish enterprise value from pre-money.** EV = market cap + debt - cash for the public comp; the private-round equivalent involves netting cash on the balance sheet at close. For a Series-B target with material cash from the raise, be precise about which number you are producing.

## Acceptance criteria

- **The comp-set universe is a real, current-day pull** from Meritech or Bessemer (or both), with the source URL and timestamp cited.
- **Every filter decision is documented** with a one-line rationale.
- **Outliers are flagged and either excluded with rationale or included with a discount adjustment.**
- **The private-market discount is applied with a cited source** (Damodaran, Kroll / Duff & Phelps, or AICPA Practice Aid).
- **The sensitised pre-money range spans base / bull / bear cases** across NTM revenue and comp-set quartile.
- **The cross-check tab reconciles against a second comp source and against market-conditions data**, with divergences >25% hypothesised.
- **The memo produces a specific defensible pre-money point** with named parameters, walk-through, and the specific arguments prepared for negotiation.
- **The specific revenue number being multiplied is named** (NTM GAAP revenue, aggregate or recurring-only) and defended.

## Deliverables

- The workbook with all seven tabs.
- The valuation memo (Markdown or PDF, 2-3 pages).
- A one-slide summary suitable for a board pack showing the derivation walk (public median → filtered → discounted → target).

## Extensions (optional)

- **Add a Rule-of-40 layer.** Compute the Rule of 40 for every constituent in the filtered comp set, compare against the target's Rule of 40, and note whether the target's placement inside the filtered set is at the top, middle, or bottom of the Rule-of-40 distribution. Use this to justify a placement inside (or outside) the interquartile range. (This anticipates exercise 04.)
- **Author a counter-memo from the lead's side.** Play the lead investor. Produce a comp-set filter that supports a materially lower multiple (30-40% lower) using defensible-sounding filter choices. Argue against the founder's memo. Then produce the reconciliation — where would the negotiation land?
- **Add a services-revenue adjustment.** Assume the target has 20% of aggregate revenue as one-time professional services. Apply the SaaS multiple to the recurring subset only and value the services revenue at a lower multiple (or via a modest DCF). Compare against a naive application of the aggregate SaaS multiple.
- **Layer in a market-cycle overlay.** Pull the Bessemer Cloud Index historical time series and note whether the current-quarter median multiple sits above or below the 5-year median. If above, discount the derived pre-money by the market-cycle premium; if below, note the cyclical opportunity.
- **Rerun the exercise as a Series-C target.** Same company, 24 months later, $75M NTM revenue, 40% growth, -5% FCF margin. Note how the comp-set membership, the applicable multiple range, and the private-market discount all shift with stage.
