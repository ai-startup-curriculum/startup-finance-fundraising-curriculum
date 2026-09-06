# Exercise 03 — Down-Round and Pay-to-Play Modelling

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 3 (Down Round Mechanics — Pay-to-Play and Senior-Preference Stacking). Familiarity with mod-104 (Cap Tables and Equity Compensation) chapter 4 exit-scenario waterfalls, mod-108 chapter 2 (liquidation preferences), mod-108 chapter 3 (preferred-stock waterfall math), and mod-108 chapter 4 (anti-dilution formulae).

## Problem statement

For a specified stressed-runway scenario, model a down-round Series-B with pay-to-play mechanics applied across three existing preferred series, quantify the "pull-your-participation-or-convert-to-common" consequence for each existing preferred investor, and produce the pro-forma exit waterfall the CFO delivers to the board before the term sheet is signed. The point of the drill is to build the pre-signing artifact set (waterfall workbook + participation-vs-consequence memo + break-even-exit table) that makes the pay-to-play mechanic *persuadable* rather than *arbitrary* — the existing preferred sign because the arithmetic tells them to, not because the CFO tells them to.

The exercise is deliberately structured against a stack that has already had three prior rounds, because a two-round stack is small enough that a simple extension almost always fits. Pay-to-play becomes the load-bearing tool at the third and later down rounds, when the incumbent stack is deep enough that non-participation genuinely damages the incumbent.

## Scenario — the situation

Use this specific scenario for the drill. (For extra depth, run the same drill against the two additional scenarios in the extensions section.)

**Company:** B2B SaaS company, ~140 employees, incorporated in Delaware. Three prior priced preferred rounds on the cap table.

**Prior rounds.**

| Round | Post-money | Price/share | New money | Lead | Instrument |
|---|---|---|---|---|---|
| Series Seed | $10M | $1.00 | $2M | Seed Fund A | Series Seed Preferred, 1x non-participating, broad-based weighted-average anti-dilution |
| Series A | $40M | $2.50 | $10M | VC Fund B (lead) | Series A Preferred, 1x non-participating, broad-based weighted-average anti-dilution, standard pro-rata |
| Series B | $110M | $5.50 | $25M | Growth Fund C (lead) | Series B Preferred, 1x non-participating, broad-based weighted-average anti-dilution, standard pro-rata |

Assume clean pari-passu preference across the three existing series (each is 1x non-participating; in a sale, the total preference stack is $2M + $10M + $25M = $37M paid pari-passu before common recovers). Assume the option pool has been topped up at each round to hold ~15% of post-money fully-diluted.

**Simplified pre-down-round cap table** (use these round-number figures for the drill; feel free to reconcile more precisely for extra rigor):

- Founders (common): 12,000,000 shares
- Employees (common, vested + unvested from option pool): 3,500,000 shares (approx)
- Series Seed Preferred: 2,000,000 shares held by Seed Fund A
- Series A Preferred: 4,000,000 shares held pro-rata by Seed Fund A (25%) and VC Fund B (75%)
- Series B Preferred: 4,545,454 shares held by Growth Fund C (60%), VC Fund B (25%), Seed Fund A (15%) — reflecting pro-rata rights exercised across the syndicate

Assume the option pool has approximately 2,500,000 unallocated shares available for grants.

**Current KPI trajectory.** ARR $12M (Series-B underwrote against $20M ARR at month 18); net-new-ARR trending flat over trailing six months; NRR 105% (weakened from 118% at Series B); gross margin 72%; CAC payback 26 months. Last-round Series-B was priced against a plan that the company clearly missed.

**Runway.** $6M cash, $1.1M/month burn. 5-6 months of runway. The CFO has been running the 6-month trigger from chapter 1; plan B is now the primary path.

**The incoming Series-C.** Growth Fund D, a distressed / value-oriented growth-stage lead, is prepared to lead a Series-C at **$60M pre-money / $85M post-money** (a materially-down round from the $110M Series-B post-money) with a **$25M new-money check**. Terms include:

- Series C Preferred at $3.75 per share (below the Series-B $5.50).
- 1x non-participating preference for Series C.
- **Senior** to the Series A and Series B (which remain pari-passu with each other, junior to Series C). Seed Preferred remains junior to Series A and Series B.
- Pay-to-play: existing Series Seed, Series A, and Series B preferred that does not participate at 100% of pro-rata is converted to **shadow preferred with 1x preference but no anti-dilution, no protective provisions, no pro-rata rights**, and forfeits the anti-dilution recalculation on the Series-C down-round issuance.
- Broad-based weighted-average anti-dilution on the Series-C (protecting the incoming lead going forward).
- 20% post-close option-pool top-up funded out of pre-Series-C fully-diluted (i.e., dilutes the pre-Series-C holders, not the Series-C).

**Existing investor readable stance** (assume, for the drill):

- **Growth Fund C** (Series B lead) — has follow-on capacity but is deeply frustrated by the miss to the plan. Will participate at pro-rata (or above) if the pro-forma waterfall shows their participation preserves value. Will not participate if it does not.
- **VC Fund B** (Series A lead) — has partial follow-on capacity ($3M available). Would like to participate but is fund-lifecycle-constrained.
- **Seed Fund A** — no follow-on capacity. This is a seed fund with all reserves deployed. The fund partners understand what non-participation means but cannot write the check.

## Requirements

Produce a single deliverable pack containing the following.

### Part A — the pre-down-round waterfall baseline

1. **Pre-down-round exit waterfall.** Build the waterfall model for the current cap table across five illustrative exit prices: $30M, $60M, $110M (par to the Series-B post-money), $200M, $400M. For each price, show:
   - The preference-stack recovery (Series Seed, Series A, Series B), each at 1x.
   - The as-converted recovery for each series (the amount they would receive if they converted to common instead of taking preference).
   - Whether each series takes preference or converts (holder-favorable choice).
   - The common recovery (founders and employees).
   - The total distribution reconciles to the exit price.
2. **Ownership summary.** Fully-diluted percentage ownership on the pre-Series-C cap table, by holder (Founders, Employees, Seed Fund A total, VC Fund B total, Growth Fund C total).

### Part B — model the Series-C down round under three participation scenarios

3. **Series-C pro-forma.** Compute the Series-C issuance mechanics:
   - Series-C shares issued: $25M / $3.75 = 6,666,666 shares.
   - Post-Series-C cap table pre-option-pool-top-up.
   - Series-C post-money = $85M (verify against price × total shares × post-money price).
   - Broad-based weighted-average anti-dilution recalculation for the Series Seed, Series A, and Series B on the Series-C issuance. Compute the adjusted conversion price and adjusted as-converted share count for each series.
   - Option pool top-up: 20% of post-close FD, funded out of pre-Series-C. Compute the new option-pool shares.
   - Full post-Series-C cap table (fully diluted, in share counts and percentages).
4. **Scenario A — full participation.** Every existing preferred series participates at 100% of pro-rata in the Series-C.
   - Compute each series' pro-rata share of the $25M new money (based on their pre-Series-C fully-diluted ownership).
   - Compute how many additional Series-C shares each existing series takes (at the $3.75 price).
   - Compute the post-Series-C cap table with the additional shares layered in.
   - Compute the exit waterfall at each of the five prices from Part A, now with the Series-C senior tier layered on top and the Series A / B / Seed preferences (with anti-dilution recalc) below.
5. **Scenario B — mixed participation** (the realistic case).
   - Growth Fund C participates at 150% of pro-rata (they super-pro-rata to defend their position).
   - VC Fund B participates at 30% of pro-rata (they can write $3M against the pro-rata ask of ~$10M).
   - Seed Fund A does not participate at all (no follow-on capacity).
   - Compute for each of the three existing series:
     - Which portion is participating (retains full preferred rights, gets anti-dilution recalc).
     - Which portion is non-participating (converted to shadow preferred, forfeits anti-dilution recalc, loses protective provisions).
   - **Note:** the mechanics of splitting a partially-participating holder's position into "participating shares" vs. "shadow shares" is a term-sheet drafting question. For this drill, model the pay-to-play as a per-holder threshold — a holder that participates below 100% of pro-rata is treated as non-participating for the *entire* pre-existing preferred position they held (the strictest form). Then re-run under a softer version: pro-rata-fraction-based (participating fraction retains full rights on the pro-rata fraction of pre-existing shares).
   - Compute the post-Series-C cap table under both drafting variants.
   - Compute the exit waterfall at each of the five exit prices under both drafting variants.
6. **Scenario C — hard blocking.** Growth Fund C, on reviewing the term sheet, decides *not* to participate at all (they take the mark). VC Fund B still participates at 30%. Seed Fund A still cannot participate. The Series-C incoming lead re-underwrites the deal on the reduced insider participation — assume they now demand a **1.5x senior preference** on the Series-C to compensate.
   - Recompute the Series-C issuance mechanics with the 1.5x preference (each Series-C dollar now claims $1.50 of preference before junior classes recover).
   - Recompute the post-Series-C cap table.
   - Recompute the exit waterfall at each of the five exit prices. Note especially where the Series A/B/Seed recover *less* under scenario C than under scenario B, and where they recover *more* (if anywhere).

### Part C — the participation-consequence memo

7. **Per-investor participation-consequence table.** For each of the three existing preferred investors (Growth Fund C, VC Fund B, Seed Fund A), build a table with rows for each of the five exit prices and columns for:
   - Recovery if participate at 100% of pro-rata (under Scenario A, or a per-investor variant of B).
   - Recovery if do not participate (under the participating-shadow-preferred variant of Scenario B).
   - Delta = recovery-if-participate − recovery-if-not-participate.
   - Check size required to participate at 100% of pro-rata.
   - Break-even exit price: the exit price above which the delta exceeds the check size. Below this price, non-participation is cheaper than participation; above this price, participation is cheaper. **This is the persuasion number.**
8. **Investor-by-investor memo.** For each of the three investors, write a one-page memo the CFO would deliver, containing:
   - The per-investor participation-consequence table.
   - A one-paragraph narrative walking the investor through what participation preserves and what non-participation costs, using the specific dollar numbers.
   - The explicit check-size ask (in dollars) and the explicit alternative (shadow preferred if not participating).
   - The specific timing ask (participation commitment by date X, wire by date Y).
   - Signed by the CFO (or CEO), addressed to the specific partner at the investor.

### Part D — the board-facing consolidated memo

9. **Board memo, 3-4 pages.** Contents:
   - Situation summary: current KPIs, current runway, why a down round is unavoidable given the alternatives.
   - The incoming Series-C term sheet, marked up. Note specifically:
     - The 1x-vs-1.5x preference decision (draft strategy for holding the preference at 1x).
     - The senior-preference stacking (Series-C senior over Series A/B, which remain pari-passu).
     - The pay-to-play mechanic (shadow preferred with anti-dilution forfeiture — argue the participating-fraction drafting is the middle ground).
     - The anti-dilution flavour (broad-based weighted-average on Series-C is market; fight any narrow-based or full-ratchet ask).
     - The option-pool top-up size and dilution allocation.
   - The three scenarios (A, B, C) with their post-Series-C cap tables and their exit-waterfall results at the five exit prices.
   - The break-even exit-price table for each investor.
   - The specific asks: board approval of the term sheet, board approval to open the participation-consequence conversation with each existing investor, board authority to proceed to definitive documents on the specified timeline.
10. **Pro-forma founder-and-employee-ownership summary.** A one-page table showing:
    - Pre-Series-C founder ownership (%) and employee-pool ownership (%).
    - Post-Series-C ownership under Scenario A (full participation, no shadow preferred fires).
    - Post-Series-C ownership under Scenario B (mixed participation, some shadow preferred fires).
    - Post-Series-C ownership under Scenario C (hard blocking, 1.5x preference).
    - Note the shadow-preferred conversion effect: in scenarios where Seed Fund A's Seed Preferred is converted to shadow, the founders and employees benefit modestly from the reduced-preference stack in some exit prices — this is the specific mechanic worth highlighting.

## Starter guidance

- **Use mod-104 chapter 4 as the reference for waterfall math.** The chapter walks the participating-vs-non-participating logic and the "convert-or-take-preference" holder choice. Every waterfall row in this exercise re-uses that logic.
- **Use mod-108 chapter 4 for anti-dilution formulae.** Broad-based weighted-average is the formula that applies to the Series Seed, Series A, and Series B on the Series-C issuance. Compute the adjusted conversion price for each series before computing the as-converted share counts.
- **Distinguish the two pay-to-play drafting variants.** The strictest ("any short-fall of 100% pro-rata triggers shadow-preferred conversion of the entire position") is different from the pro-rata-fraction variant ("participating fraction retains full rights, non-participating fraction converts to shadow"). Both exist in the market; the drill asks you to model both.
- **Do not assume every existing investor will participate rationally.** Seed Fund A physically cannot; that constraint is real and worth naming in the memo. VC Fund B is partially constrained. The pay-to-play mechanic still has to be defensible against investors who genuinely cannot participate — the drill is partly about surfacing that tension.
- **The break-even exit price is the CFO's persuasion lever.** For an investor whose participation delta exceeds their check size at an exit price the company plausibly reaches, the arithmetic argues for participation. For an investor whose delta never covers their check size in any plausible exit, the mechanic is punitive without economic justification and the CFO should acknowledge that.
- **The 1x-vs-1.5x preference decision is the largest single lever in the term-sheet negotiation.** Multi-x preference has a material long-tail cost that will not show up until exit. Fight for 1x; if the deal will not close without a multiple, the multiple should be visible in the board memo, not silently signed.
- **Note the shadow-preferred beneficiary effect.** When Seed Preferred converts to shadow (or to common), the preference stack ahead of common shrinks; founders and employees can recover slightly more at moderate exit prices under scenarios where shadow-preferred fires broadly. Flag this in the memo without overstating it.

## Acceptance criteria

- **The pre-down-round waterfall reconciles at every exit price.** Total distribution = exit price. Series-by-series recovery matches the take-preference-or-convert logic.
- **The Series-C mechanics are computed correctly.** Anti-dilution recalculation applied to each existing series; option-pool top-up allocated out of pre-Series-C; post-Series-C cap table reconciles fully-diluted to the post-money price × share count.
- **All three scenarios (A, B, C) are modelled with the correct pay-to-play drafting.** Both drafting variants (strict and pro-rata-fraction) shown for Scenario B.
- **The per-investor break-even exit-price table is defensible** — the reader can trace how the break-even was computed from the recovery deltas and the check sizes.
- **The investor-by-investor memos are written to the specific investor** — Growth Fund C's memo is different from Seed Fund A's memo, because the two investors' economic situations are different.
- **The board memo names the specific term-sheet parameters to fight for and the specific parameters to concede** — this is not a "pass or fail" memo, it is a negotiation-plan memo.
- **The founder-and-employee-ownership summary correctly captures the shadow-preferred beneficiary effect** where it applies.

## Deliverables

- The pro-forma cap-table and waterfall workbook (spreadsheet) covering the pre-Series-C baseline and the three scenarios (A, B, C) under both drafting variants.
- The per-investor participation-consequence table (spreadsheet or Markdown).
- Three per-investor memos (one each for Growth Fund C, VC Fund B, Seed Fund A) — Markdown or PDF.
- The board memo (Markdown or PDF).
- The founder-and-employee-ownership summary (Markdown or PDF).

## Extensions (optional)

- **Alternative Scenario 1:** the incoming Series-C lead asks for **1x participating preferred** (participating up to a 3x cap). Re-model each of the three scenarios with the participation feature. Note the sharp difference in mid-price exit waterfall for common.
- **Alternative Scenario 2:** the incoming Series-C lead asks for **full-ratchet anti-dilution** on the Series-C going forward (protecting the incoming lead against subsequent down rounds). Model what a next-round-priced-below-$3.75 does to the incoming lead's as-converted share count under full-ratchet vs. under broad-based weighted-average. Quantify the incremental dilution to founders.
- **Recap alternative modelling.** Rather than pay-to-play, model a **recap** per chapter 4 that collapses Series Seed, Series A, and Series B entirely to common at defined ratios (1:1 for founder-favourable; 0.5:1 for lead-favourable; some intermediate mix). Compute the pro-forma cap table under both ratios. Compute the exit waterfall under both. Argue in a one-page memo which path (pay-to-play as modelled here vs. recap) creates less damage to the founder-and-employee economics for this specific stack.
- **Cram-down modelling.** Assume VC Fund B has a supermajority-vote block over Series-A protective provisions and refuses to consent to the charter amendment enacting the pay-to-play. Model the drag-along / blank-check-preferred / majority-vote paths chapter 4 describes and produce the counsel-facing memo on which mechanic is available and what the litigation-risk profile looks like under Delaware fiduciary-duty doctrine.
- **Retrospective at Series-D.** Assume the Series-C closes as modelled in Scenario B and the company grows into a plausible Series-D at $250M post-money in 18 months. Model the Series-D cap table with the participating and shadow-preferred holders. Write the retrospective memo the CFO delivers to the Series-C board — "did the pay-to-play structure hold up?"
