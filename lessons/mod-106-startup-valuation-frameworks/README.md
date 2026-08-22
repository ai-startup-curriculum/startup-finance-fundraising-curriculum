# mod-106 — Startup Valuation Frameworks

**Pre-Revenue, VC Method, Revenue Multiples, and Public Comps**

**Track:** [Startup Finance & Fundraising](../../CURRICULUM.md)
**Stage:** SEED / SERIES-A
**Hours:** 22 (8 chapters + 6 exercises + planned lab + planned quiz)

## What this module installs

A pre-revenue company has no revenue. A pre-product-market-fit company has no defensible revenue trajectory. A Series-A company is priced against public comps trading in a public market that closes at 4pm every business day. A growth-stage company with a clean unit-economics model and a modelable path to breakeven can support a triangulating DCF. Each of those stages needs a different valuation framework, and the framework the founder uses has to match the diligence framework the investor is running — otherwise the round doesn't clear.

This module installs the specific frameworks a CFO or finance lead needs to price a round from angel through late-growth. Specifically:

- The **pre-revenue anchor methods** — the Berkus Method (five 0-$500K components, capped historically at a $2.5M pre-money), the Payne Scorecard Method (industry-average pre-money × weighted-scorecard multiplier), and risk-factor summation (Ohio TechAngel Fund pattern) — and why these methods **bracket** an angel or pre-seed round rather than price it.
- The **VC method** — target return (10-30× at seed) worked back through a target-exit-value, an assumed dilution schedule across future rounds, and a back-solve to today's pre-money — and how a VC prices a seed round inside the partnership economics of their fund.
- **Revenue-multiple valuation** at Series-A and later — EV / NTM revenue anchored to the relevant public comparable set (Meritech Enterprise SaaS comparables, Bessemer Cloud Index), growth-adjusted (Rule of 40, growth-adjusted multiples), and the private-market discount to public-comp multiples that a growth-stage investor applies.
- **The Rule of 40** and **growth-adjusted multiples** — the specific arithmetic that converts a "10× ARR" headline number into an underwriting-defensible multiple that respects the company's growth-and-margin band.
- **Where DCF applies and where it fails** — early-stage cash-flow projections are too uncertain for a defensible DCF; a growth-stage company with a modelable path to breakeven and known unit economics can support a triangulating DCF. Knowing the boundary keeps the CFO from producing analytics that give false confidence.
- **The quarterly deal-terms reports** — Fenwick & West Silicon Valley Venture Survey, Wilson Sonsini's Entrepreneurs Report, PitchBook-NVCA Venture Monitor — the market-conditions context for a specific fundraising target: median pre-money by stage, up-round vs. down-round frequency, deal size and time between rounds.
- **The Carta State of Private Markets** as the primary-source benchmark against valuation targets — valuations by stage, dilution per round, ESOP sizing, secondary-transaction volume, down-round frequency, bridge-round frequency — drawn from Carta's proprietary cap-table data set.
- **The negotiation failure modes** — anchoring to the last round's post-money as this round's pre-money floor without adjustment for market conditions; chasing a public-comp multiple without respecting the growth-and-margin band; ignoring the target-return math the VC is running in their fund model — and the specific fix for each.

The module deliberately covers valuation only as it is used in **fundraising** (a new-money priced round on an ongoing company). Transaction valuation for an M&A deal, an IPO, or a secondary sale — with its earn-outs, escrows, and deal-specific mechanics — defers to [`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum).

## Chapters

1. [`01-pre-revenue-anchor-methods-berkus-scorecard-risk-factor.md`](01-pre-revenue-anchor-methods-berkus-scorecard-risk-factor.md) — the three anchor methods for a pre-revenue round (Berkus, Payne Scorecard, risk-factor summation), and why they produce a defensible **bracket** rather than a defensible **price**.
2. [`02-vc-method-target-return-back-solve.md`](02-vc-method-target-return-back-solve.md) — target return → target exit value → assumed dilution schedule → back-solved pre-money, and how a VC prices a seed round inside their fund's partnership economics.
3. [`03-revenue-multiples-and-public-comps.md`](03-revenue-multiples-and-public-comps.md) — EV / NTM revenue at Series-A and later, the Meritech Enterprise SaaS comparables and the Bessemer Cloud Index as the anchor sets, and the private-market discount to public-comp multiples.
4. [`04-rule-of-40-and-growth-adjusted-multiples.md`](04-rule-of-40-and-growth-adjusted-multiples.md) — the Rule of 40 arithmetic (growth % + FCF margin %), the growth-adjusted multiple mechanics, and the growth-and-margin bands that determine which multiple in the comp set is the right one.
5. [`05-where-dcf-applies-and-where-it-fails.md`](05-where-dcf-applies-and-where-it-fails.md) — the DCF-applicability boundary; why early-stage projections are too uncertain and how a growth-stage company with a modelable breakeven and known unit economics can support a triangulating DCF.
6. [`06-fenwick-wsgr-pitchbook-nvca-deal-terms.md`](06-fenwick-wsgr-pitchbook-nvca-deal-terms.md) — reading the quarterly deal-terms surveys: median pre-money by stage, up-vs.-down-round frequency, deal-size trend, and time between rounds — as the market-conditions context for a specific target.
7. [`07-carta-state-of-private-markets.md`](07-carta-state-of-private-markets.md) — reading the Carta primary data: valuations by stage, dilution per round, ESOP sizing, secondary volume, down-round frequency, bridge-round frequency — as the primary-source benchmark against a valuation target.
8. [`08-valuation-negotiation-failure-modes-and-remediation.md`](08-valuation-negotiation-failure-modes-and-remediation.md) — the three characteristic negotiation failure modes (last-round-post-money anchoring, comp-multiple mis-application, ignoring VC fund math) and the prescribed fix for each; the boundary between this module and mod-108 / the exit-curriculum.

## Exercises

1. [`exercises/exercise-01-berkus-and-scorecard-pre-revenue-drill.md`](exercises/exercise-01-berkus-and-scorecard-pre-revenue-drill.md) — apply Berkus, Payne Scorecard, and risk-factor summation to the same hypothetical pre-revenue startup; produce the bracket and the memo.
2. [`exercises/exercise-02-vc-method-target-return-back-solve.md`](exercises/exercise-02-vc-method-target-return-back-solve.md) — build the VC-method back-solve model for a seed round through a Series-A / B / C dilution ladder to a defined exit; sensitivity across target-return and dilution assumptions.
3. [`exercises/exercise-03-revenue-multiple-vs-public-comps-derivation.md`](exercises/exercise-03-revenue-multiple-vs-public-comps-derivation.md) — build the public-comp table (Meritech / Bessemer construction, growth and margin bands), derive the applicable multiple range, and price the target Series-B.
4. [`exercises/exercise-04-rule-of-40-and-growth-adjusted-multiple-drill.md`](exercises/exercise-04-rule-of-40-and-growth-adjusted-multiple-drill.md) — compute Rule of 40 for a portfolio of comparables, produce a growth-adjusted multiple regression, and defend the target multiple against the regression.
5. [`exercises/exercise-05-fenwick-wsgr-carta-market-conditions-read.md`](exercises/exercise-05-fenwick-wsgr-carta-market-conditions-read.md) — read one recent Fenwick / WSGR quarterly report and one Carta State of Private Markets report; produce a market-conditions memo tied to a specific fundraising target.
6. [`exercises/exercise-06-valuation-negotiation-failure-teardown.md`](exercises/exercise-06-valuation-negotiation-failure-teardown.md) — tear down three fictional-but-realistic valuation negotiations that failed for each of the three canonical reasons; prescribe the specific fix and re-price the round.

## Lab

- `lab-01-end-to-end-valuation-memo-across-methods` — planned; walks the full valuation memo for a hypothetical Series-B target: pre-revenue anchor recap, VC method, public-comp derivation, DCF triangulation, market-conditions read, and the negotiation strategy that ties them together. Placeholder to be authored in a subsequent content cycle.

## Quiz

- `quiz-01` — planned; 12-15 questions covering the eight chapter objectives. Placeholder to be authored in a subsequent content cycle.

## Reference

- [`resources.md`](resources.md) — Berkus / Payne primary sources, Damodaran's academic-practitioner work on early-stage and private-company valuation, the Meritech and Bessemer public-comp datasets, the Fenwick / WSGR / PitchBook-NVCA quarterly reports, the Carta State of Private Markets, and Kupor / Feld / Suster for VC-side context.

## How this module fits

Directly depends on [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/) (unit economics — a revenue-multiple valuation is only defensible on top of a cohort model that can bridge the ARR to gross margin, NRR, and CAC payback), [`mod-103`](../mod-103-three-statement-model-and-driver-based-forecasting/) (the driver-based model that produces the NTM revenue forecast the multiple is applied to), [`mod-104`](../mod-104-cap-tables-and-equity-compensation/) (the pre-money / post-money / option-pool arithmetic every valuation resolves into), and [`mod-105`](../mod-105-convertible-instruments/) (the valuation cap on the outstanding SAFEs is a de facto ceiling on this round's pre-money).

Directly feeds [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/) (the valuation output sizes the round and shapes the investor-target list — a valuation the target investor pool won't pay is a valuation that ends the process), [`mod-108`](../mod-108-term-sheets-and-preferred-stock-economics/) (the term-sheet economics of the round the valuation prices — preferences, anti-dilution, protective provisions), and [`mod-109`](../mod-109-runway-management-and-bridge-financing/) (down-round mechanics, extension-round pricing, and the pay-to-play conversation that follows a valuation the market won't clear).

The module *does not* teach: term-sheet mechanics (that is mod-108), M&A / IPO / secondary-transaction valuation (that lives in [`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum) with the deal-specific earn-out, escrow, and structuring mechanics), or 409A tax-preferred common-stock valuation methodology (that is mod-104 chapter 5, which owns the tax-basis valuation for equity compensation). It teaches the CFO-level frameworks used to price a new-money priced round on an ongoing company.
