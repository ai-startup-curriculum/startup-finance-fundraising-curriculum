# Top-Down vs. Bottom-Up Reconciliation

## Why this matters

A Series-A investor asks two revenue-forecast questions in the same diligence conversation:

- *"Show me your bottom-up plan. How many customers close each month, how many SDRs and AEs do you have, what's the funnel?"*
- *"Show me the top-down view. How large is your market, what penetration rate is this ARR at year 3 implying, and does that penetration rate look feasible?"*

A CFO who has only one of the two answers has lost half the diligence conversation. A CFO whose two views are wildly inconsistent — bottom-up says $25M ARR at year 3, top-down TAM × 5% says $500M ARR is achievable — hasn't reconciled the two and doesn't know which one is real.

The reconciliation is a discipline: build both views, tie them where they can be tied, and *when they disagree*, do the work to understand why. The disagreement is often the most useful diagnostic in the whole model — it names which of the assumption stacks is wrong (or which is aspirational without an operational backing plan). This chapter installs the top-down build, the bottom-up build, the walk between them, and the CFO narrative that emerges from the reconciliation.

## The bottom-up build — what chapter 4 produced

Chapter 4 covered the bottom-up view in detail. In summary:

```
S&M spend  →  Leads  →  MQLs  →  SQLs  →  Opps  →  Closed-won × ACV  →  Bookings
                                                                              │
                                                                              ▼
                                                            × Cohort retention & expansion
                                                                              │
                                                                              ▼
                                                                    Monthly recognised revenue
                                                                              │
                                                                              ▼
                                                                     ARR at each month-end
```

The bottom-up view produces `ARR at year 3 = $Y`. It has three characteristics:

- **Operationally grounded.** Every step is a rate or a count that the sales and marketing organisation can plan against.
- **Sensitive to team scale.** The hiring plan drives SDR / AE headcount, which drives lead volume via cost-per-lead, and SQL volume via SQLs-per-SDR. If the hiring plan doesn't scale, the funnel doesn't scale.
- **Historically calibrated.** Every conversion rate comes from the last 6-12 months of actual data.

It fails when the market gets bigger than the assumed unit economics can penetrate — when the plan calls for 4,000 new logos in year 3 and there are only 2,000 companies in the ICP.

## The top-down build — TAM, SAM, SOM, penetration

The top-down view starts at the outside — the total market — and reasons inward.

**TAM (Total Addressable Market).** The total revenue opportunity if the product were sold at its natural price to every buyer in the world who could conceivably use it. In practical terms: TAM is the *ceiling*. For a workflow tool sold to marketing teams, TAM might be `(all marketing teams globally) × (average willingness-to-pay per team per year)`. TAM claims of "$100B market" that don't decompose into `count × price` are meaningless.

**SAM (Serviceable Addressable Market).** The subset of TAM reachable by the company's specific go-to-market motion — the market limited to the geography sold into, the buyer segments the sales motion targets, the language and localisation the product supports. If the product is English-only US-only, SAM is a fraction of the global TAM.

**SOM (Serviceable Obtainable Market).** The realistic slice of SAM that the company could win within a forecast horizon, given the competitive landscape and the go-to-market motion's realistic capacity. SOM is not a mathematical fraction of SAM; it is a judgment about competitive dynamics, timing, and speed.

**Penetration rate.** The share of SAM (or SOM) that a specific ARR represents. If SAM = $10B and current ARR = $20M, penetration = 0.2%. If year-3 ARR = $200M under the bottom-up plan, year-3 penetration = 2% of SAM.

The three usual TAM-construction methods:

1. **Top-down.** Start from a large industry research number ("$50B enterprise software spend on X category" from Gartner / IDC / Forrester / Statista) and apply layered filters to arrive at SAM. Fast to author, easy to critique on the filter assumptions.
2. **Bottom-up.** Multiply `number of target buyers × price per buyer × attach rate`. Requires the buyer count from a source (Crunchbase / ZoomInfo / SEC filings for public buyers / trade associations / government census data) and a price anchor from the company's own list price. Harder to build; harder to attack on methodology because every input is a countable thing.
3. **Analog-based.** Look at a comparable company's disclosed ARR at a comparable stage; assume the TAM is at least large enough to have supported that ARR. Useful as a sanity check, not as a primary method.

A defensible top-down build usually shows all three. Investors give more credit to bottom-up TAMs because they are auditable — every count and price can be traced to a source. Top-down TAMs from industry reports are treated as a floor sanity check rather than the primary reference.

## Where top-down and bottom-up should agree

The two views are two paths to the same year-3 ARR. Precisely, the bottom-up view produces an ARR trajectory and the top-down view produces a *feasibility ceiling*:

- If bottom-up year-3 ARR is $Y and SAM is $S, then implied penetration = Y / S.
- If implied penetration is "small" (<1-2% of SAM in year 3 for an early-stage company), the bottom-up plan does not require an unusual market share and the two views are consistent.
- If implied penetration is "large" (>5-10% of SAM in year 3 for an early-stage company), the bottom-up plan is implicitly assuming a market share that most companies cannot achieve within a Series-A horizon, and either the bottom-up plan is aspirational or the SAM is understated.

There is no bright-line "acceptable penetration." The rule of thumb from the SaaS-metrics practitioner canon is that market leaders in growing categories reach 5-15% category penetration at maturity, and reaching 1-3% within 3-5 years of Series-A is a strong performance. Numbers outside those bands need explanation.

## Where they usually disagree — the four common shapes

The interesting outputs of the reconciliation are the disagreements.

**Shape 1: Bottom-up penetration is tiny, TAM is enormous.** Year-3 ARR of $50M against a claimed TAM of $200B is 0.025% penetration. The bottom-up plan is not challenging the market; the TAM is either directionally right and the plan is deliberately conservative, or the TAM is broader than the company's actual reachable market. The reconciliation memo should decompose the TAM into SAM and SOM to see which is the case.

**Shape 2: Bottom-up penetration is aggressive, TAM is defensible.** Year-3 ARR of $200M against a SAM of $2B is 10% penetration in three years — a market-leader trajectory. Either the plan is aspirational (in which case it lacks operational backing) or the bottom-up plan assumes competitive share the funnel model does not support. The reconciliation should look at the win-rate assumption specifically — does 10% share require winning 40%+ of head-to-head competitive deals?

**Shape 3: Bottom-up penetration is fine, but the hiring plan can't produce it.** Year-3 ARR of $80M looks reasonable against SAM, and the funnel conversion rates are historical, but hitting the required SQL volume requires an SDR team of 60 people and the hiring plan has 25. The reconciliation surfaces a gap between the S&M capacity plan and the required funnel throughput. Either the hiring plan grows, the productivity assumption grows (with justification), or the ARR forecast shrinks.

**Shape 4: TAM analysis produces a different growth-rate ceiling than the bottom-up plan assumes.** Bottom-up plan assumes 12% MoM growth (roughly 4× annualised); top-down implies market growth of 20% per year. The bottom-up plan is taking substantial share from competitors, or the market is being expanded (the product is bringing new buyers into the category), or the growth-rate assumption is unsustainable past the immediate term. This is where the two views inform each other — the market context puts a shape on how long the bottom-up growth-rate assumption can hold.

## The reconciliation memo

The output of the reconciliation is a one-page memo that a CFO puts in front of a board or lead investor.

Structure:

- **Bottom-up ARR trajectory (with confidence interval).** Base case year-1, year-2, year-3 ARR, with the drivers named. Upside and downside cases from the scenario switch (chapter 6).
- **TAM decomposition.** TAM (top-down source), SAM (filtered), SOM (realistic 5-year obtainable). Method for each — bottom-up count × price, top-down industry-report allocation, analog comparison.
- **Implied penetration rates.** Base case year-3 ARR ÷ SAM. Called out as a percentage and compared against reference (market leaders, comparable companies at the same stage).
- **The gap (if any).** Where the two views agree, where they disagree, and the reason for the disagreement.
- **The action the disagreement drives.** If the bottom-up plan is aspirational, the hiring plan needs to scale (or the plan comes down). If the top-down TAM is understated, the SAM decomposition needs to expand (with justification). If both views agree, the memo says so.

The memo is a one-pager for a reason — the CEO and lead investor will read it in two minutes. The full workings are on the model tabs; the memo is the summary.

## The two questions the reconciliation answers for a Series-A investor

Every reasonable Series-A lead asks two things about a revenue plan:

1. *"Can you actually execute this plan?"* — the operational question. The bottom-up model answers this. If the funnel conversion rates are historical, the hiring plan produces the required S&M spend and headcount, and the ACV assumption is consistent with the sales-motion mix, then yes.

2. *"Is the market big enough for the outcome the investor is underwriting?"* — the market-scale question. The top-down TAM answers this. If year-5 or year-10 ARR at plausible penetration produces an outcome large enough for the investor's fund model to require, then yes. Series-A funds typically underwrite for a 10× fund-returner outcome, which puts a floor on the addressable market (see [`mod-106`](../mod-106-startup-valuation-frameworks/) and [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/)).

A model that only answers one of the two is incomplete. A CFO who can walk the investor through both views in one meeting has removed a major diligence question before it becomes a diligence blocker.

## The forward-looking "capacity" check

A discipline from operator-blog canon (Christoph Janz, David Sacks, Dave Kellogg) that the reconciliation should include: a *capacity check* on the growth-rate assumption.

The idea: for a bottom-up plan that assumes 100% year-over-year growth into year 3, ask whether the S&M organisation being planned has the capacity to close 100% more logos than last year, given the historical productivity per rep and the ramp cost of new reps. If the plan says year-3 new logos is 2× year-2 but the AE team is only 1.4× larger and the ramp cost of new AEs is 3-6 months, the math doesn't work — the plan implicitly requires either higher productivity per rep (which needs a specific programme to justify) or more aggressive hiring.

The capacity check surfaces plans that "look reasonable" at the ARR level but fail at the operational-execution level. It is one of the fastest ways for a CFO to identify which quarters of a plan are at risk.

## What top-down for a market-creating product looks like

A common founder objection: *"our market didn't exist five years ago; there is no TAM to size."* This is the market-creating case (Zoom pre-2013, Snowflake pre-2014, Datadog pre-2010). Two approaches:

- **Adjacent-market anchor.** If the new market is displacing spend from an adjacent legacy market (Datadog against Splunk / on-prem monitoring; Snowflake against on-prem data warehouses), the adjacent market's size is a proxy for the TAM ceiling. This is defensible if the substitution story is credible.
- **Adoption-curve construction.** If the new market is truly greenfield, model it via the adoption curve of a comparable category — how quickly did cloud storage penetrate the enterprise? How quickly did SaaS displace on-prem in adjacent segments? This is a more assumption-heavy model but is the honest way to size a new category.

Investors who fund market-creating products are less rigorous about TAM (they cannot be — the number doesn't exist), but the CFO still needs to have thought about it. A memo that says *"we're market-creating; here's the adjacent market as the ceiling, here's why substitution is likely to happen"* is a completely acceptable answer.

## Summary

- A defensible Series-A revenue plan has both a bottom-up view (chapter 4's funnel) and a top-down view (TAM / SAM / SOM / penetration). Missing either half loses half the diligence conversation.
- Top-down TAM has three construction methods — top-down from industry reports, bottom-up count × price × attach, analog from comparable companies. Investors give the most credit to bottom-up TAMs because every input is auditable.
- Reconciliation between the two views produces four common shapes: tiny penetration + huge TAM (revisit SAM decomposition), aggressive penetration + defensible TAM (aspirational bottom-up), fine ARR + inadequate hiring (surfaces the capacity gap), mismatched growth-rate ceiling (surfaces sustainability of assumed growth).
- The reconciliation memo is a one-pager: bottom-up trajectory, TAM decomposition, implied penetration, the gap, the action. Full workings on the model tabs.
- The capacity check verifies that the assumed growth rate can be produced by the assumed headcount and productivity. Failing this check identifies the specific quarters of the plan that are at risk.
- Market-creating products use adjacent-market anchors or adoption-curve construction as substitutes for a canonical TAM. Investors expect the memo to have thought about it even when the number can't be constructed traditionally.
- The two views answer two different questions: can you execute this plan (bottom-up), and is the market large enough for the outcome the investor is underwriting (top-down). A defensible plan answers both.

Chapter 6 turns to scenario and sensitivity analysis — the discipline that turns a single-point forecast into a range of outcomes the CFO can defend under pressure.
