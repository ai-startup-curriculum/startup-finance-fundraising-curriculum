# Revenue Multiples and Public Comparables

## Why this matters

Once a company has enough revenue to project a defensible next-twelve-months (NTM) number, the industry-standard valuation anchor for SaaS and other recurring-revenue software companies stops being the anchor bracket (chapter 1) or the VC method (chapter 2) and becomes a **revenue multiple** — typically enterprise value divided by NTM revenue — anchored to a set of publicly-traded comparable companies whose multiples are visible every trading day. That transition happens around Series-A for capital-efficient companies and reliably by Series-B for most SaaS companies.

The reason the anchor moves is that at that stage the founder-CFO has:

- A cohort model (mod-102) that supports a defensible next-twelve-months revenue projection.
- A three-statement model (mod-103) that ties the revenue projection to gross margin, operating expense, and burn.
- Enough revenue history that the retention and expansion pattern (NRR / GRR) is legible.

And the market has:

- A public comparable set — publicly-traded SaaS or software companies whose enterprise value and NTM revenue are both known at every close — that trades continuously.
- A well-documented private-market discount to public-comp multiples that reflects the illiquidity and stage-risk of a private company.
- A set of well-known adjustments (growth rate, gross margin, Rule of 40 — chapter 4) that map an individual company's fundamentals to the range within the comp set where its multiple should sit.

This chapter installs the mechanics of the revenue-multiple approach: what EV/NTM revenue is, where to find the comp sets (Meritech Enterprise SaaS comparables, Bessemer Cloud Index), how to build a comparable set for a specific target, how to apply the private-market discount, and the common failure modes of applying the framework off-band.

Chapter 4 handles the growth-adjustment mechanics (Rule of 40 and growth-adjusted multiples) that determine where inside the comp-set range a specific target's multiple should sit. Chapter 5 handles the DCF triangulation that becomes relevant at growth stage.

## The EV / NTM revenue multiple

**Definition.**

- **Enterprise value (EV):** for a public company, market capitalisation + debt - cash. For a private company being priced, the closest equivalent is the post-money valuation minus the net cash on the balance sheet at close (in practice, most private-round pricing is quoted on a **post-money** or **pre-money** basis directly, and the EV framing is used only when computing the multiple from a public-comp benchmark and applying it to derive a private valuation).
- **NTM revenue:** consensus (for public companies) or model-derived (for private companies) revenue for the next twelve months from the reference date.

The multiple: `EV / NTM revenue`.

**Why EV, not market cap.** Enterprise value is the value of the operating business independent of the capital structure. Two companies with identical operating businesses but different capital structures (one funded entirely by equity, one carrying $200M of debt against $50M of cash) have the same enterprise value but different market capitalisations. EV normalises for capital structure. For SaaS companies, which are typically low-debt / high-cash, EV and market cap converge, but the framing is still important for growth-stage companies that may carry venture debt.

**Why NTM, not TTM.** Trailing-twelve-months (TTM) revenue is a historical fact. Next-twelve-months (NTM) revenue is a forward projection. Software companies with 30-100% growth rates have very different TTM and NTM revenues, and the enterprise value of a growing SaaS company reflects the market's expectation of future revenue, not the trailing revenue. NTM is the standard denominator for growth software; TTM is used for slower-growth software and for non-software companies where the growth rate is close to zero.

An analyst working with public-company data will find both multiples in the standard databases (S&P Capital IQ, FactSet, PitchBook). Meritech's public-comp table (see below) publishes both EV/NTM and EV/CY24 (calendar-year) revenue. Bessemer's cloud index publishes an EV/NTM multiple as its primary metric.

**Illustrative arithmetic.** A public SaaS company trading at a $10B market cap, with $500M of cash and $200M of debt, has an EV of $10B + $0.2B - $0.5B = $9.7B. If its NTM revenue consensus is $970M, its EV/NTM revenue multiple is 10.0×.

## The public comp sets

Two publicly-published public-comp sets dominate as anchor references for SaaS valuation:

### The Meritech Enterprise SaaS comparables

**Publisher:** Meritech Capital Partners, a growth-stage venture firm with a durable practice around enterprise software investing.

**Where to find it:** [meritechcapital.com/public-comparables/enterprise-saas](https://www.meritechcapital.com/public-comparables/enterprise-saas). The public table lists a defined universe of publicly-traded enterprise SaaS companies with their live valuation multiples, growth rates, and gross margins. Meritech also publishes a *high-growth* subset and a *cloud* subset. The table is updated regularly and is one of the most-cited public references for SaaS valuation.

**What the table contains for each company:**

- Ticker, company name, market cap.
- Enterprise value.
- Last-twelve-months (LTM) revenue and NTM revenue.
- EV/LTM and EV/NTM revenue multiples.
- Revenue growth rate (YoY).
- Gross margin.
- Free cash flow margin.
- Rule of 40 score (growth + FCF margin).
- Sometimes: net revenue retention (NRR), sales efficiency, magic number.

**How to use it.** Filter the table to companies that match the target on the specific dimensions that matter for pricing:

- **Vertical:** horizontal SaaS, vertical SaaS, developer tools, security, data infrastructure, etc.
- **Buyer:** SMB / mid-market / enterprise.
- **Business model:** subscription / consumption / hybrid.
- **Growth band:** 20-30% / 30-50% / 50%+.
- **Margin profile:** gross margin band (70-80% / 80%+), FCF margin band.

The filtered subset produces the comparable multiple range for the target. If Meritech's high-growth subset (30%+ growth) is trading at a median EV/NTM of 10× with a range of 6-16×, that is the range within which the target — if it is in the high-growth band — should be priced (subject to the private-market discount below).

### The Bessemer Cloud Index

**Publisher:** Bessemer Venture Partners, a large multi-stage venture firm with a durable cloud practice.

**Where to find it:** [cloudindex.bvp.com](https://cloudindex.bvp.com/). The Bessemer Cloud Index is a market-capitalisation-weighted index of publicly-traded cloud companies, with the underlying constituent list published on the same page. Bessemer updates the index in real time (during US market hours) and publishes a public dashboard with:

- Index level and historical time series (allowing you to see whether cloud multiples are compressing or expanding relative to historical medians).
- Median EV/NTM revenue multiple for the index and for a high-growth subset.
- Constituent-level data: ticker, market cap, EV, revenue growth, gross margin, EV/NTM.

**How to use it.** Same as Meritech, with two additional uses:

- **The historical time series** lets the CFO cite a "current-quarter median vs. 5-year median" comparison to establish whether the market is currently trading at a premium or discount to historical multiples. That framing is important for the market-conditions read (chapter 6) and for defending a specific multiple in a negotiation.
- **The index-level chart** produces a "cloud multiples have compressed X% over the past N months" statement that can be cited in valuation memos and board packs.

### Reconciling the two sources

Meritech and Bessemer will not always show identical multiples for identical periods because:

- Their constituent lists differ (Meritech is enterprise-SaaS-only; Bessemer's cloud index is broader).
- Their filter and grouping logic differ.
- Their update cadence and consensus-forecast sources may differ.

In practice, most CFOs use one as primary and the other as a cross-check. The Meritech table is often preferred for enterprise SaaS specifically; the Bessemer index is often preferred as the "public cloud" benchmark and for its time-series analytics.

Other public-comp sources that appear in valuation memos: S&P Capital IQ / FactSet (subscription-only, but the industry standard for equity research), Damodaran's dataset at NYU Stern (free, updated annually, broader coverage — see [`resources.md`](resources.md) for the direct link), and PitchBook's software analytics (subscription).

## Constructing a comparable set for a specific target

The published Meritech and Bessemer tables are the anchor, but the CFO typically has to construct a **target-specific comp set** — a subset of the published universe that best matches the target on the dimensions that matter. The construction:

**Step 1. Universe.** Start from the Meritech or Bessemer universe, or from a Damodaran / Capital-IQ pull.

**Step 2. Filter by vertical and business model.** Remove companies that don't match the target's:

- Vertical (a horizontal-SaaS collaboration tool is not a comparable for a vertical SaaS in healthcare).
- Business model (subscription SaaS is not directly comparable to a consumption/usage-based data infrastructure company; the multiples move very differently with growth).
- Buyer profile (SMB self-serve, mid-market inside sales, enterprise field sales — these have different unit economics and different multiples).

**Step 3. Filter by growth band.** Growth is the single strongest driver of multiple. A 60%-growth company is not a comparable for a 20%-growth company even in the same vertical. The most common band structure is:

- **Hyper-growth:** 60%+ NTM growth.
- **High-growth:** 30-60% NTM growth.
- **Steady-growth:** 15-30% NTM growth.
- **Low-growth / mature:** <15% NTM growth.

The target should be placed in a growth band and compared to the constituents inside that band, not to the universe median.

**Step 4. Filter by margin profile.** Rule of 40 (chapter 4) and gross margin band both matter. Two companies with identical growth rates but very different margin profiles will not trade at the same multiple.

**Step 5. Note the outliers.** In any comp set of 15-30 companies, one or two will be trading at extreme multiples for company-specific reasons (imminent product cycle, recent acquisition rumour, an activist investor pushing for a sale). Excluding or discounting those outliers is defensible; leaving them in the median calculation without noting them is a diligence red-flag.

**Step 6. Compute the median and interquartile range.** The median is the anchor. The interquartile range (25th to 75th percentile) is the reasonable band around it. The min-max is the "extreme scenario" band; typical private-round pricing lands somewhere between the median and the 75th percentile if the target is in the top half of the comp set on the fundamentals.

**Illustrative comp-set construction.**

Target: Series-B vertical SaaS for healthcare-provider administration; consensus NTM revenue $30M; NTM growth 65%; gross margin 78%; FCF margin -20%.

Meritech universe, filtered to vertical SaaS with 50%+ growth and 75%+ gross margin. Suppose the filtered set is 6 public companies with EV/NTM multiples of 8×, 10×, 12×, 14×, 16×, 20×. Median = 13×. Interquartile range = 10× to 16×.

The target's public-comp anchor multiple is 13× on the median; the reasonable range is 10-16×. Now apply the private-market discount (below) and the growth-adjustment mechanics (chapter 4) to derive the target's applicable multiple.

## The private-market discount

A private company does not trade at the same multiple as an otherwise-identical public company. The discount reflects several structural differences:

- **Illiquidity.** Private-company shares cannot be sold on a moment's notice. Buyers demand a lower price to compensate.
- **Diligence uncertainty.** Public-company financials are audited, disclosed on a defined cadence, and subject to SEC oversight. Private-company financials are much less transparent.
- **Governance opacity.** Public-company board and executive compensation is disclosed. Private-company governance is not.
- **Concentration of ownership.** Private-company ownership is concentrated in a small number of investors and founders, which affects control dynamics.
- **Stage risk.** A private company at Series-B has execution risk that a mature public company does not (product-market fit at scale, GTM repeatability, cross-functional scaling — a set of risks that public companies have largely resolved).

The size of the discount varies with market conditions, stage, and specific-company factors. Published academic and practitioner ranges:

- **Series-A / early Series-B:** discounts of 30-50% to the public-comp median are common in most market conditions.
- **Late Series-B / Series-C:** discounts of 20-40%.
- **Late-stage / pre-IPO:** discounts of 10-25%, sometimes zero or even a premium if the private round is being priced above the current public-comp trading level (which happened during 2020-2021 in certain sectors and is generally read as a market-signal to be careful about).

**Where the discount comes from empirically.** Aswath Damodaran's work on illiquidity discounts (see [`resources.md`](resources.md)) is the standard academic reference — his textbook and NYU Stern page publish updated discount estimates by revenue and profitability profile. Practitioner references include the annual valuation reports from Duff & Phelps (now Kroll) and the AICPA's Practice Aid on valuation of privately-held company equity securities issued as compensation.

**Applying the discount.**

- Median public-comp multiple for the filtered set: 13× (from the running example).
- Assumed private-market discount at Series-B: 35%.
- Target multiple: 13× × (1 - 0.35) = **8.45×**.
- NTM revenue: $30M.
- Anchor valuation: 8.45× × $30M = **$253.5M**.

The $253.5M is the anchor. Growth-adjusted-multiple work (chapter 4) and the negotiation dynamics (chapter 8) may adjust it up or down, but it is the market-anchored starting point rather than a founder-narrative starting point.

## Which "revenue" — the specific-number footguns

The multiplier is applied to a specific revenue number. Which number matters. The typical footguns:

- **ARR vs. revenue.** Annualised recurring revenue (ARR) is a snapshot metric ("last month's monthly recurring revenue × 12"). Revenue is a period metric ("recognised revenue over the last twelve months" or "expected recognised revenue over the next twelve months"). For a fast-growing company, ARR at end-of-period is significantly higher than TTM revenue — because the revenue in the earlier months of the period was smaller. The multiple base for public companies is **revenue**, not ARR. Applying a public-comp revenue multiple to a private company's ARR overstates the valuation by the amount of the growth gap. Some private-market memos use ARR intentionally (a "10× ARR" transaction) but then implicitly reference a lower "revenue multiple." Be explicit about which number is being multiplied.
- **NTM revenue vs. current-year revenue vs. exit-year revenue.** Public-comp multiples use NTM revenue by convention. Occasionally a memo will multiply by "next-fiscal-year" revenue, which is a longer forward period, producing a lower multiple against a higher revenue base. Be explicit about the period.
- **GAAP revenue vs. bookings vs. billings.** [mod-101 chapter 3](../mod-101-startup-accounting-foundations/03-bookings-billings-revenue-cash.md) walks the distinction. Multiples apply to **revenue** in the GAAP sense (ASC 606 recognised). Applying a revenue multiple to bookings or billings inflates the answer.
- **Revenue in aggregate vs. subscription-only.** Some SaaS companies have material services or one-time revenue. The public-comp revenue multiples apply to *aggregate* revenue but implicitly assume the aggregate is dominated by recurring revenue. If the target has a material services component, either apply the multiple to the recurring subset (and use a separate multiple or DCF for services) or discount the aggregate multiple.

Each of these is a decision the CFO has to make explicitly in the valuation memo. The memo should name which revenue number is being multiplied and why.

## The comp-set choice as a negotiating lever

The choice of comparable set has more valuation impact than the multiple applied within a comp set. Two comp-set decisions that dominate:

- **The vertical scope.** A vertical SaaS company in a large market can defensibly compare itself either to (a) other vertical-SaaS companies in adjacent verticals or (b) horizontal SaaS at similar scale. The two sets often trade at different multiples. The comp-set choice is a defensible negotiation lever, but has to be defended with a specific argument for why the chosen set is the right one.
- **The growth-band membership.** A company at 45% growth can defensibly place itself in the 30-60% or the 40-70% band, and the median multiple of those bands can differ meaningfully. Placing yourself in a higher band is defensible if the growth trajectory is on that band's path; placing yourself in a higher band when the trailing growth is at the lower end of your chosen band is a red flag.

The counterparty will do the same analysis and may propose a different comp set. The productive negotiation is to walk the specific inclusion / exclusion decisions and reach an agreed comp set. Most Series-B and later term-sheet negotiations that end up in disagreement over pre-money end up disagreeing over the comp set, not over the multiple applied within it.

## Common founder traps

- **Applying a public-comp multiple to ARR without adjustment.** Overstates the valuation by the growth gap between ARR and TTM revenue.
- **Ignoring the private-market discount.** Quoting the median public-comp multiple as the private-round anchor produces a valuation the market won't clear. The discount is real and has to be applied.
- **Cherry-picking outliers.** Anchoring to the 90th-percentile constituent of a comp set with an argument like "we're just as good as them" is a red flag. The negotiation shifts to defending the specific comparable, and the counterparty will usually win that argument.
- **Using a comp set that doesn't match the business model.** A subscription-SaaS comp set is not a defensible anchor for a consumption/usage-based data infrastructure company; the growth dynamics and multiples differ.
- **Failing to update the comp set for market conditions.** Public multiples move quarter-to-quarter. A memo using six-month-old multiples in a market that has compressed 30% is not defensible.
- **Not separating recurring from non-recurring revenue.** Applying a SaaS multiple to a revenue base with 30% services / one-time revenue overstates the valuation because services revenue does not warrant the same multiple.
- **Confusing enterprise value with market cap.** Especially for companies carrying venture debt or preferred with liquidation preferences, EV ≠ market cap ≠ pre-money. Be precise about which number the multiple produces.

## What good looks like

A finance leader building a revenue-multiple valuation:

- Pulls the current-day Meritech and Bessemer public-comp tables and constructs a target-specific filtered subset.
- Documents the filter criteria (vertical, business model, buyer, growth band, margin band) and the reason for each.
- Notes and excludes (or discounts) any comp-set outliers with company-specific factors.
- Computes the median and interquartile range of the filtered set.
- Applies an explicit private-market discount with a specific justification for the discount level chosen.
- Cross-checks against a second comp source (Damodaran / Capital IQ / PitchBook) for consistency.
- Names the specific revenue number being multiplied (NTM GAAP revenue, aggregate or recurring-only) and defends the choice.
- Presents the output as a **range** anchored to the median, not as a single point, and identifies the specific point within the range the target is being priced at with a growth-adjustment argument (chapter 4).

## Summary

- Once a company has a defensible NTM revenue projection, EV / NTM revenue becomes the primary valuation anchor at Series-A and later. Enterprise value normalises for capital structure; NTM revenue is the forward number the market prices against.
- Two public-comp sources dominate: Meritech Capital's Enterprise SaaS comparables and the Bessemer Cloud Index. Both publish live constituent-level data and can be filtered to a target-specific comp set.
- A comp set is built by filtering the universe on vertical, business model, buyer, growth band, and margin profile. The median of the filtered set is the anchor; the interquartile range is the reasonable band.
- Private companies trade at a discount to public-comp multiples. The discount is typically 30-50% at early Series-B, tapering toward zero at pre-IPO. Damodaran's illiquidity work is the standard academic reference.
- The specific revenue number multiplied (NTM revenue, TTM revenue, aggregate vs. recurring-only, GAAP vs. ARR) has to be named explicitly. Different choices produce very different valuations.
- The choice of comp set is the largest single valuation lever and is where negotiations tend to concentrate. Cherry-picking, model-mismatch, and stale filters are the primary failure modes.

Chapter 4 turns to the growth-adjustment mechanics — Rule of 40 and growth-adjusted multiples — that determine where inside the comp-set range a specific target's multiple should sit, given its own growth and margin profile.
