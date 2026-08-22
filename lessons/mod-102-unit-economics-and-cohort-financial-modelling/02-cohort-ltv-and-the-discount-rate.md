# Cohort LTV and the Discount Rate

## Why this matters

Almost every founder-authored LTV number is some version of `ARPU × gross margin ÷ monthly churn`. That formula has three problems: it uses a blended ARPU that hides cohort-level heterogeneity, it treats churn as a constant when real cohorts decay non-linearly, and it *does not discount future gross profit at all* — a $50/mo customer whose cohort produces gross profit for 60 months is booked in the number at 60× current gross profit, as if a dollar in month 60 were worth the same as a dollar today. Every serious venture investor rejects the undiscounted number on sight because they know that early-stage cash has an enormous opportunity cost. If your Series-A deck reports an LTV computed this way, the diligence firm will recompute a discounted version, and the number will typically be a fraction of what you claimed.

This chapter installs the CFO-grade LTV: the **present value** of a cohort's gross-profit stream, discounted at a **venture-appropriate risk-adjusted rate**, truncated at a defensible horizon. It also names the two decisions that dominate the number's defensibility — the discount rate you pick and the horizon you truncate at — and shows why both should be documented in the same methodology memo that documents CAC (chapter 1).

## The wrong formula, walked through

The naïve LTV formula:

```
LTV = ARPU × gross margin ÷ monthly churn
```

For a hypothetical SaaS company with $500/mo ARPU, 80% gross margin, and 2%/mo customer churn:

```
LTV = $500 × 0.80 ÷ 0.02 = $20,000
```

Paired with a CAC of $2,500, the LTV:CAC ratio is 8:1 — a number that reads spectacular. Every one of the following is wrong or fragile in that computation:

- **The "1 ÷ monthly churn" term is a horizon of 1 ÷ 0.02 = 50 months of expected life.** That assumes the retention curve is a memoryless exponential with constant hazard, which real cohorts virtually never exhibit — most SaaS cohorts have front-loaded churn (first 90 days) that flattens dramatically for retained accounts. The exponential-decay assumption is either too optimistic (early churn is higher, so cumulative lifetime revenue never reaches the geometric-series limit) or too pessimistic (post-90-day cohorts are much stickier than the average churn rate implies).
- **No discounting.** A dollar of gross profit in month 50 is treated as equivalent to a dollar of gross profit in month 1. At any venture-appropriate discount rate, the month-50 dollar is a fraction of the month-1 dollar.
- **No expansion.** Real cohorts often expand (upgrades, seat adds, cross-sell); the formula misses expansion entirely, making it too conservative in one direction while being too aggressive in the other.
- **ARPU is blended.** New-customer ARPU and mature-customer ARPU can diverge by 2-3× in a company with strong expansion motion. The blend obscures which cohort segments are actually valuable.
- **Gross margin is blended.** Cost-to-serve varies by cohort — enterprise cohorts consume more support and CSM time; PLG cohorts consume more free-tier infrastructure. Chapter 3 covers the decomposition.

The formula's only virtue is that it fits on a napkin. It has no place on a Series-A deck.

## The right computation — cohort LTV as a present-value stream

The CFO-grade LTV is computed off the cohort table (built in chapter 4). Conceptually:

$$
\text{LTV}_{\text{cohort}} = \sum_{m=1}^{N} \frac{\text{GP}_m}{(1 + r)^m}
$$

where:

- $\text{GP}_m$ is the gross profit produced by the *retained portion of the cohort* in month $m$ after acquisition — that is, (retained customer count in month $m$) × (ARPU in month $m$) × (gross margin in month $m$).
- $r$ is the monthly discount rate (below).
- $N$ is the truncation horizon (below).

In plain English: take the cohort's monthly gross-profit contribution as it actually plays out on the cohort table — accounting for real churn shape, real expansion, real ARPU drift — discount each month back to the acquisition date, and sum. That's LTV.

The number is smaller than the naïve formula's output in almost every case, and it is defensible: every number in the sum can be traced back to a row of the cohort table, which itself can be traced back to real customer-account records. A diligence firm can recompute it and reach approximately the same number.

## The discount rate — the number that has to be defended

For a mature public company, the discount rate for a DCF is the weighted-average cost of capital (WACC), typically in the 6-12% annual range depending on the industry, leverage, and beta. Applying WACC to a venture-stage LTV is wrong for one reason: the WACC is a return required by a diversified investor buying a diversified equity, not the required return of a venture investor buying an illiquid concentrated position in a company that has a real probability of returning nothing.

Venture returns are famously *power-law distributed*. The empirical rule from Aswath Damodaran's academic work on private-company valuation and from the venture-industry literature (Kupor's *Secrets of Sagacious Investing*, Feld & Mendelson's *Venture Deals*, and the CFA Institute's private-equity readings) is that the required rate of return on venture-stage equity is much higher than the WACC of a comparable public company — because it has to compensate for illiquidity, for the concentration risk of a small portfolio, and for the failure rate at each stage.

Published venture-industry ranges for required rates of return by stage — used both by VCs constructing their own valuations and by CFOs constructing DCF-anchored LTVs — approximately:

| Stage | Typical required IRR (annual) | Rationale |
|---|---|---|
| Pre-seed / Seed | 50-100% | Very high mortality rate; wide outcome distribution; illiquid for a decade |
| Series A | 40-60% | Mortality lower; product-market-fit signal reduces some tail risk |
| Series B | 30-40% | Traction reduces mortality further; expansion capital, still illiquid |
| Series C / Growth | 20-30% | Late-stage; typically requires a credible IPO or acquisition path in a few years |
| Pre-IPO / crossover | 15-25% | Approaching the public-market discount curve |

These ranges are approximate and vary by data source and vintage year. <!-- needs-research: cite the current-year survey data for venture required rates of return, e.g., Preqin, Cambridge Associates, or Damodaran's most recent private-company valuation dataset --> For a CFO computing LTV to be used in a fundraise narrative at Series-A, a discount rate somewhere in the 30-40% annual range is the defensible default; going lower requires an argument (e.g., a public comparable set at a mature growth-stage that supports a lower cost of equity), and going higher signals you agree with a pessimistic view of your own company's mortality risk.

The monthly discount rate used in the LTV formula is the annual rate converted to monthly compounding:

$$
r_{\text{monthly}} = (1 + r_{\text{annual}})^{1/12} - 1
$$

At 35% annual, this is ~2.53% monthly. At 25% annual, ~1.88%. At 15% annual (a mature-company WACC), ~1.17%.

## Why the discount rate choice dominates the number

Consider a hypothetical cohort producing $100/month of gross profit every month for 60 months (no churn, no expansion — a stylised example to isolate the discount-rate sensitivity):

| Discount rate (annual) | LTV — undiscounted 60-mo sum | LTV — 60-mo discounted PV |
|---|---|---|
| 0% (the naïve formula) | $6,000 | $6,000 |
| 10% (mature-company WACC) | $6,000 | $4,725 |
| 25% (growth-stage) | $6,000 | $3,431 |
| 35% (Series-A default) | $6,000 | $2,853 |
| 50% (seed-appropriate) | $6,000 | $2,192 |

The number moves by more than 2× across the plausible range. The choice of discount rate is *the* single largest driver of the LTV number and therefore of the LTV:CAC ratio. Every deck's LTV number should disclose the rate; every methodology memo should defend it against a stated comparable.

The failure mode: a founder reports LTV using no discount rate ("undiscounted 60-month LTV") on a deck. The lead investor's diligence firm re-runs with a 35% rate. LTV falls from $6,000 to $2,853. LTV:CAC falls from a claimed 12:1 to a re-computed 5.7:1. Both numbers may still support the round, but the founder has now spent a diligence cycle defending the methodology instead of the business. The correct move is to lead with the discounted number in the deck itself.

## Truncation horizon — the second-most-defensible choice

The infinite geometric-series formula assumes the cohort produces gross profit indefinitely; the discounted stream converges but slowly. In practice CFOs truncate at a defensible horizon and disclose it.

Common truncation conventions:

- **24-month horizon** — used in some conservative frameworks, especially for consumer businesses where 2-year churn ceilings are visible in the data.
- **36-month horizon** — a common Series-A convention. It matches the typical VC hold-to-exit timeframe assumption at Series-A and is short enough that most of the retention curve is empirically observed rather than extrapolated.
- **60-month horizon** — common at Series-B and later, especially for enterprise SaaS where multi-year contracts and low churn make longer horizons empirically defensible.
- **"Empirical life" — until the retention curve crosses some floor** — the most defensible version, e.g., "we truncate LTV computation at the month the retention curve crosses 20% of the acquisition cohort." This ties the horizon to observable cohort behaviour rather than a calendar convention.

The rule of thumb: the truncation horizon should be *no longer than the oldest cohort you have real data for*. If your company is 30 months old, computing a 60-month LTV requires extrapolating 30 months of retention data past your observation window — a defensible move only if the retention curve has clearly flattened.

The undiscounted 5-year LTV — 60 months, no discount rate — that appears on many early-stage decks is a specific failure mode a Series-A investor will not accept. It combines the two errors: no discounting (which inflates the number 2-3×) *and* a horizon that extends beyond the company's own cohort observation window (which requires unwarranted extrapolation). The methodology memo pattern that survives diligence is: monthly cohort GP × discounted at a stated rate × truncated at a stated horizon, all three anchored to citable references.

## Cohort LTV in three views for a deck

For CFO-authored external materials, the convention that survives diligence is to show three LTV numbers, all cohort-based:

1. **Undiscounted 24-month cohort LTV.** The literal sum of gross profit from a cohort's first 24 months, based on the cohort table's actual retained-customer counts. No discount rate, but a short horizon — the shortness alone protects against gross overstatement.
2. **Discounted 36-month cohort LTV at a stated rate (e.g., 35% annual).** The number a Series-A investor will most naturally recompute. Show this as the headline LTV number.
3. **Discounted "empirical life" cohort LTV.** For companies with rich cohort data (multiple years, thousands of customers per cohort), the horizon-until-retention-floor version. This is the most defensible number for a Series-B or later CFO who can justify a longer window.

Each number is accompanied by the LTV:CAC ratio (computed against the same period's fully-loaded CAC, chapter 1) and the payback period (computed off the cumulative gross-profit column of the cohort table, chapter 4).

## The relationship to enterprise valuation

An LTV number is not a valuation number. The link between the two is indirect:

- LTV × new customers per period × margin structure feeds a revenue and gross-profit forecast, which is one input to a revenue-multiple valuation ([`mod-106`](../mod-106-startup-valuation-frameworks/)).
- A high LTV:CAC ratio (typically ≥3:1 by the [Skok / a16z benchmark](https://www.forentrepreneurs.com/saas-metrics-2/)) supports a higher revenue multiple in the growth-adjusted range because it demonstrates that incremental S&M spend produces enterprise value.
- A short payback (typically under 12-18 months) supports a higher multiple because it demonstrates capital-efficient growth.

But LTV is not an enterprise-value estimate; the DCF-of-a-company is a different construction (all cohorts × the company's ongoing cost base × the terminal value × the corporate discount rate). Cohort LTV is a per-customer number that informs the unit-economics narrative and bounds the plausible S&M investment level — nothing more. Founders who use LTV × customer count as a valuation input are making a category error and get corrected by a lead investor in the first term-sheet meeting.

## Common CFO LTV mistakes

Even at CFO grade, a few mistakes recur; a checklist for review before an LTV number leaves the finance function:

- **Gross margin is stale.** The gross-margin bridge (chapter 3) must be the version that decomposes to hosting / support / CSM / delivery and matches the P&L. Using an "assumed 80% SaaS gross margin" when the actual number is 63% inflates LTV by 27%.
- **Churn is customer-count churn, not revenue churn.** For an ARPU-heterogeneous cohort, revenue churn (weighted by customer value) is the number that matters for LTV, not customer-count churn.
- **Expansion is missing.** Real cohorts often expand; leaving expansion out understates the number. Modelling expansion requires the NRR/GRR framing from chapter 5.
- **The cohort under measurement is atypical.** LTV should be reported at least two ways — a mature cohort (12+ months old, retention curve stabilised) and the trailing-12-month cohort weighted average. Reporting the friendliest single cohort as "our LTV" is a diligence-week retraction.
- **Free-tier PLG conversions are misattributed.** For a PLG motion, is the LTV the LTV of a paying customer, or the LTV of a signup (weighted by the paid-conversion rate)? Both are legitimate views; mixing them is not.

## Summary

- The naïve `ARPU × gross margin ÷ churn` LTV formula assumes constant ARPU, constant churn, no expansion, and — critically — no discounting. Every one of those assumptions is wrong for a real cohort.
- The CFO-grade LTV is the present value of a cohort's monthly gross-profit stream, read off the cohort table, discounted at a venture-appropriate rate, truncated at a defensible horizon.
- Discount rates for early-stage venture equity are far above mature-company WACCs: 30-40% at Series-A is a defensible default; 50-100% at seed reflects mortality risk.
- The discount rate choice can move the LTV number by 2×+; it is the single largest lever in the calculation and must be disclosed.
- The truncation horizon should not exceed the oldest cohort you have real data for. "Undiscounted 5-year LTV" combines the discount-rate error and the extrapolation error and is a specific pattern Series-A investors will not accept.
- Three LTV views on a deck — undiscounted 24-month, discounted 36-month at a stated rate, and (at Series-B+) discounted empirical-life — paired with a methodology memo, is what survives diligence.
- LTV is a per-customer number that informs unit-economics narrative and bounds S&M investment. It is not a valuation input.

Chapter 3 turns to the gross-margin decomposition that feeds the gross-profit column in the cohort table. Chapter 4 builds the table itself. Chapter 5 layers in NRR / GRR (which is how expansion enters the LTV number).
