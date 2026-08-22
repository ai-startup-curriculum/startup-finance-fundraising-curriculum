# The Rule of 40 and Growth-Adjusted Multiples

## Why this matters

Chapter 3 anchored a Series-A / B / C valuation to a public-comp EV/NTM revenue multiple. What it did not do is answer the specific question: *where in the comp-set range should this specific target's multiple sit?* If the filtered comp set trades at a 6× to 20× EV/NTM range with a 12× median, is the target a 6×, a 12×, or a 20× company?

The empirical answer is that revenue multiples in software correlate strongly with two variables: **growth rate** and **profitability** (typically expressed as FCF margin or operating margin). A company growing faster earns a higher multiple; a company that is profitable at scale earns a higher multiple; a company that is both very high-growth and profitable — the top of the class — earns the highest multiple in the set.

The two working frameworks that operationalise this relationship:

- **The Rule of 40** — a single scalar (`growth % + FCF margin %`) that ranks companies on the combined dimension. Threshold: 40% is the number a "good" software company should exceed.
- **The growth-adjusted multiple** — an explicit regression (or line-fit) of EV/NTM revenue against NTM growth across the comp set, producing a fitted multiple for the target given its specific growth rate.

Both operationalise the empirical relationship in slightly different ways. The Rule of 40 is a screening heuristic; the growth-adjusted multiple is the multiple derivation. Both are used together in practice: the Rule of 40 tells you whether the target belongs in the top or bottom of the comp set, and the growth-adjusted multiple derivation tells you the specific number to apply.

The chapter also handles the "growth band" bucketing that makes the same comp-set data actionable at negotiation time.

## The Rule of 40 — origin and definition

**Origin.** The Rule of 40 originated in the SaaS-investor community and was popularised in the mid-2010s by Brad Feld, Techstars, and by SaaS-focused funds including SaaS Capital and OpenView Venture Partners. It has been adopted broadly across the SaaS community and cited in most modern practitioner references (Bessemer, ChartMogul, SaaStr — see [`resources.md`](resources.md)).

**Definition.** The Rule of 40 is a scalar sum:

```
Rule of 40 = NTM revenue growth % + FCF margin %
```

Where:

- **NTM revenue growth %** is next-twelve-months revenue growth over the prior twelve months, expressed as a percentage.
- **FCF margin %** is free cash flow over the same twelve-month period, expressed as a percentage of revenue.

If the sum is ≥ 40, the company "passes" the Rule of 40. If not, it does not.

Common variants:

- **Growth + EBITDA margin.** EBITDA (or non-GAAP operating income) instead of FCF. Simpler to compute for companies that don't disclose FCF; slightly less rigorous because it excludes working-capital dynamics that matter for software.
- **Growth + operating income margin.** Similar to EBITDA-margin variant.
- **Growth + adjusted-EBITDA margin.** Excludes stock-based compensation. More flattering to software companies with large SBC.
- **Rule of X (broader term).** Any growth+margin sum against any threshold. "Rule of 50" for the top-tier bar; "Rule of 30" for a lower bar sometimes used at early growth stage.

The specific choice of margin depends on the analytical audience. Public-market equity analysts often use FCF margin; growth-stage investors sometimes use adjusted-EBITDA margin. Meritech and Bessemer both publish Rule of 40 values in their comp tables using FCF margin as the standard.

## Rule of 40 as a ranking heuristic

The Rule of 40 is designed to solve a specific problem: comparing a high-growth-money-losing company to a lower-growth-profitable company on a single scale.

- A 70% grower losing 25% on FCF has a Rule of 40 score of 45. Passes.
- A 15% grower generating 30% FCF has a Rule of 40 score of 45. Passes at the same score.
- A 35% grower breaking even has a Rule of 40 score of 35. Fails.

The scalar sum implicitly trades growth for profitability at a 1:1 exchange rate. That trade is not literally accurate — the market does not value 1 point of growth equivalently to 1 point of margin at every level — but it is a first-order-defensible starting point.

**Illustrative Rule of 40 ranking on a filtered comp set.**

| Company | NTM growth | FCF margin | Rule of 40 | Passes? |
|---|---|---|---|---|
| Alpha | 65% | -30% | 35 | No |
| Beta | 55% | -15% | 40 | Yes (at threshold) |
| Gamma | 45% | +5% | 50 | Yes |
| Delta | 35% | +15% | 50 | Yes |
| Epsilon | 25% | +20% | 45 | Yes |
| Zeta | 15% | +10% | 25 | No |
| **Median** | 40% | -3% | 43 | Yes |

Companies passing the Rule of 40 in a comp set typically trade at higher multiples than those that don't. Companies with Rule-of-40 scores > 60 ("Rule of 60") often trade at the top of the comp-set multiple range.

## The growth-adjusted multiple — deriving the specific multiple

The Rule of 40 is a screening heuristic. The **growth-adjusted multiple** is the specific multiple derivation.

The empirical claim: in most market conditions, EV/NTM revenue multiples across a coherent comp set fit reasonably well against NTM growth rate. Higher-growth companies trade at higher multiples, in a relationship that is roughly linear over the middle of the growth range and increasingly convex at the very top.

The mechanical process:

**Step 1. Build the comp set.** Same construction as chapter 3 (filtered on vertical, business model, buyer, and roughly-comparable margin band).

**Step 2. Tabulate `(growth %, EV/NTM multiple)` pairs.**

**Step 3. Fit a line (or a slightly-curved fit) across the pairs.** In practice most analysts run a linear regression:

```
EV/NTM = a + b × growth %
```

Where `a` is the intercept (the multiple a hypothetical zero-growth company would trade at) and `b` is the slope (the incremental multiple per percentage point of growth). A curved fit (polynomial, log) may be more accurate at the extremes but a linear fit is defensible for most analyses.

**Step 4. Apply the fitted line to the target's growth rate.**

**Step 5. Cross-check the result against the comp-set median and interquartile range.** If the fitted multiple is well outside the range, the fit is being driven by outliers or the target's growth rate is outside the comp-set band.

**Illustrative regression.**

Using the six-company comp set from the Rule of 40 table above and their EV/NTM multiples:

| Company | NTM growth | EV/NTM |
|---|---|---|
| Alpha | 65% | 16× |
| Beta | 55% | 14× |
| Gamma | 45% | 12× |
| Delta | 35% | 10× |
| Epsilon | 25% | 8× |
| Zeta | 15% | 5× |

A linear regression on these six points produces roughly:

```
EV/NTM ≈ 2 + 0.22 × growth %
```

Applied to a target growing at 50% NTM, the fitted multiple is `2 + 0.22 × 50 = 13×`. Applied to a target growing at 40%, the fitted multiple is `2 + 0.22 × 40 = 10.8×`.

The fitted multiple is the **public-market anchor** for the target's specific growth rate. Apply the private-market discount (chapter 3) to reach the private-market multiple.

## Growth-and-margin bands as the negotiation frame

In practice, the negotiation over which multiple to apply concentrates in **which growth band the target sits in** and **which margin sub-band within that band**. The typical structure:

**Growth bands (NTM revenue growth):**

- **Hyper-growth:** 60%+
- **High-growth:** 30-60%
- **Steady-growth:** 15-30%
- **Low-growth / mature:** <15%

**Margin bands (FCF margin at maturity):**

- **Top-tier:** 20%+ FCF margin
- **Solid:** 5-20%
- **Break-even:** -5% to +5%
- **Loss-making at scale:** worse than -5%

The cross-tab produces a 4×4 grid, and each cell has a characteristic multiple range in a given quarter's market. A "high-growth × solid-margin" company sits in a specific cell; the median multiple of the public-comp constituents in that cell is a defensible anchor.

Some public-comp data providers publish exactly this cross-tab. Meritech, for example, publishes a "high-growth" subset alongside its full universe; Bessemer publishes an "efficient growth" subset. Rolling your own cross-tab from either dataset is a routine analytical exercise.

**The negotiation lever.** A target company's band placement is often debatable at the boundary:

- A company at 32% growth can defensibly place itself in the "high-growth" band, but a counterparty may push for "steady-growth" if the trailing quarters were slowing.
- A company at 60% growth is in "hyper-growth" but a counterparty may argue the growth is unsustainable and the forward-band placement should be "high-growth."
- Margin band placement often turns on whether one-time or non-recurring items are treated as recurring (aggressive) or excluded (conservative).

The productive negotiation is to agree on which cell of the grid the target belongs in, then anchor to the median multiple of that cell. Trying to argue a specific multiple in isolation is a losing negotiation move; arguing the cell placement with the fundamentals is defensible.

## Growth durability and the "compressed growth" adjustment

A subtle but material analytical adjustment: **growth durability**.

A company growing at 50% today with a shrinking growth rate (60% last year → 50% this year → 40% projected next year) does not trade at the same multiple as a company growing at 50% today with a stable or accelerating rate (40% last year → 50% this year → 55% projected next year). The market prices future growth, and a decelerating trajectory forecasts a lower future growth rate — and therefore a lower future revenue multiple, and therefore a lower current price.

Two mechanical ways to bake growth durability into the valuation:

- **Use forward-year rather than NTM revenue.** If the growth is decelerating from 50% NTM to 30% in year 2, applying the multiple to year-2 revenue (larger base, lower multiple) may produce a more-defensible valuation than NTM alone.
- **Explicit growth-persistence factor.** Some memos apply a "growth persistence" adjustment — a scalar that discounts the fitted multiple by the expected multi-year growth deceleration. A company projected to lose 15 percentage points of growth over three years may warrant a 10-15% discount to the fitted multiple.

Both adjustments are subjective. The point of naming them is to make the assumption explicit and defensible rather than to hide it inside a single number.

## The market-multiple cycle

Public-comp multiples move over time in cycles that are largely independent of company fundamentals. During periods of market compression (2022 SaaS multiple compression is a well-documented recent example), fitted multiples across the comp set contract regardless of any individual company's growth rate. During expansions (2020-2021), fitted multiples expanded even for companies with unchanged fundamentals.

A CFO building a valuation memo should:

- Note the **current-quarter fitted multiple** against a **historical median fitted multiple** (5-year or 10-year, both easy to compute from Bessemer's historical time series).
- Note the market-cycle context (compressed / expanded / at long-term median).
- Consider whether the market is at a cyclical extreme and, if so, how much of the current multiple is a durable market level versus a temporary condition.

This is the transition point where the market-conditions chapters (6-7) become directly relevant to the multiple-selection decision.

## Rule-of-40 failure modes and edge cases

The Rule of 40 is a useful heuristic but has known edge cases:

- **Unprofitable hyper-growers.** A company at 150% growth losing 100% on FCF has a Rule of 40 of 50 and "passes." In some cases that is a genuine top-tier company; in other cases the growth is unsustainable and the burn rate is a warning. The Rule of 40 does not distinguish.
- **Margin-only performers.** A 5%-growth, 40%-FCF-margin company has a Rule of 40 of 45 and "passes." In software, low-growth-high-margin often signals a company that has stopped executing on the growth playbook and is running for cash flow. The multiple will reflect that, and the Rule of 40 "pass" won't rescue it.
- **One-time margin distortions.** A company that just closed a large multi-year contract and recognised the up-front cash may have a temporarily inflated FCF margin. Rule of 40 without adjustment overstates. The corresponding CFO discipline is to normalise one-time items in the margin calculation.
- **Stock-based compensation (SBC) treatment.** Public SaaS companies typically have high SBC. Rule of 40 computed on FCF (which excludes SBC as a cash charge) is more flattering than Rule of 40 computed on GAAP operating margin (which includes SBC). Be explicit about which is used.
- **Growth definition.** ARR growth is not the same as revenue growth. A company with high ARR growth but a lag in revenue recognition (long ramp period, deferred-revenue-heavy contracts) may show very different Rule of 40 scores depending on which growth number is used.

## Combining Rule of 40 with the fitted multiple

A defensible growth-adjusted-multiple memo combines both frameworks:

**Step 1. Compute the target's Rule of 40.** Note whether it passes and by how much.

**Step 2. Build the fitted-multiple regression on the comp set.** Apply to the target's NTM growth rate.

**Step 3. Adjust the fitted multiple for the target's specific Rule of 40 vs. the comp-set median.**

- If the target's Rule of 40 is materially above the comp-set median (say, target at 60 vs. comp-set median at 40), a modest upward adjustment to the fitted multiple is defensible.
- If the target's Rule of 40 is materially below, a downward adjustment is defensible.

**Step 4. Apply the private-market discount (chapter 3).**

**Step 5. Compare to the comp-set interquartile range as a sanity check.**

Worked continuation of the running example. Target: 50% NTM growth, -20% FCF margin, Rule of 40 = 30. Fitted multiple = 13× (from the regression). Comp-set median Rule of 40 = 43. Target's Rule of 40 is meaningfully below the comp-set median, suggesting the fitted multiple over-values the target relative to its combined growth-and-margin profile. Apply a downward adjustment of ~10% for the Rule-of-40 gap: adjusted multiple = 13× × 0.9 = **11.7×**. Apply the private-market discount of 35% (from chapter 3): **7.6×**. On $30M NTM revenue, target valuation ≈ **$228M**.

The valuation memo presents the walk: fitted multiple → Rule-of-40 adjustment → private-market discount → target valuation. Each step is defensible.

## Common founder traps

- **Anchoring the pitch to Rule of 40 without addressing the growth durability question.** A company at 60% growth losing 20% on FCF has Rule of 40 = 40. If the growth is decelerating, the investor's underwriting is against a future Rule of 40 that is lower. The pitch has to defend the durability separately.
- **Using aggressive margin definitions to inflate Rule of 40.** Adjusted-EBITDA-with-SBC-excluded produces flattering numbers. Public-comp Rule of 40 is typically computed on FCF, not adjusted EBITDA. Match the definition to the comp-set convention.
- **Fitting a regression on too small a comp set.** A regression on 4-5 companies is noise, not signal. The fit needs at least 10-15 comparables to be defensible. If the comp set is smaller, use the median and interquartile range, not a regression.
- **Extrapolating the regression outside the comp-set range.** A regression fit on 20-50% growth companies does not defensibly extend to a 100%-growth company. Extrapolation beyond the comp-set range is not defensible.
- **Ignoring the market-cycle context.** A regression on the current-quarter data will fit the current-quarter multiples. Whether those multiples are cyclically high or low is a separate question that has to be addressed with the historical time series.
- **Applying a Rule of 40 pass to salvage a bad multiple.** "We pass the Rule of 40" is not by itself an argument for a higher multiple. The multiple derivation is the argument; the Rule of 40 is a companion diagnostic.

## What good looks like

A finance leader deriving a growth-adjusted multiple:

- Constructs the comp set per chapter 3, then computes each constituent's Rule of 40 alongside its multiple.
- Runs the fitted-multiple regression on the comp set and cross-checks the fit against the comp-set median.
- Places the target in the appropriate growth-and-margin band and identifies the median multiple of the constituents in that band.
- Applies an explicit Rule-of-40 adjustment (positive or negative) for the target's own Rule of 40 vs. the comp-set median, and documents the adjustment.
- Applies the private-market discount (chapter 3) and produces the final target multiple.
- Cross-checks against the comp-set interquartile range for sanity.
- Names the market-cycle context (current vs. historical multiples) and adjusts for it if the current cycle is at an extreme.

## Summary

- Revenue multiples in software correlate strongly with growth rate and profitability. The Rule of 40 (`growth % + FCF margin %`) is a scalar heuristic that ranks companies on the combined dimension; the growth-adjusted multiple (a fitted regression of multiple against growth) produces the specific multiple to apply.
- Rule of 40 passes at ≥ 40; top-tier companies pass at Rule of 50 or higher. Variants use different margin definitions (FCF, adjusted-EBITDA, operating income) — be explicit about which is used.
- The fitted multiple derivation runs a regression of EV/NTM against NTM growth across the filtered comp set, then applies the fit to the target's growth rate. Linear fits are defensible over most of the range; extrapolation outside the comp-set range is not.
- Growth-and-margin bands (hyper-growth / high-growth / steady-growth / low-growth × top-tier / solid / break-even / loss-making margins) produce a 4×4 grid; each cell has a characteristic multiple range that anchors the negotiation.
- Growth durability (the trajectory over multi-year windows), the market-multiple cycle (current-quarter vs. historical median), and the specific margin definition all shape the fitted multiple and should be addressed explicitly in the memo.
- Common failure modes: aggressive margin definitions to inflate Rule of 40, fitting on too small a comp set, extrapolating outside the range, and treating a Rule of 40 pass as a substitute for the multiple derivation.

Chapter 5 turns to the DCF-applicability boundary — where a growth-stage company's cash-flow projections become defensible enough to support a triangulating DCF alongside the multiples framework, and where early-stage projections remain too uncertain for DCF to add value.
