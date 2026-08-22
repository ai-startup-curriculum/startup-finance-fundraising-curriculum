# Exercise 02 — Pre-Money vs. Post-Money SAFE Cap-Table Comparison

**Estimated time:** ~3 hours
**Prerequisites:** Chapters 1 and 2 (post-money SAFE anatomy, pre-money legacy SAFE mechanics).

## Problem statement

Take a single hypothetical seed-stage company with the same set of SAFE investors and the same $ amounts and the same caps, and run the conversion at a priced Series-A twice: once modelling every SAFE as a **pre-money legacy** SAFE, once modelling every SAFE as a **post-money** SAFE. Produce side-by-side pro-forma cap tables under both mechanics and quantify the founder-dilution delta. Then take a third pass with a **mixed stack** (some SAFEs pre-money, some post-money) and show how the two mechanics interact in the same conversion.

The point of the drill is to see the mechanical difference between the two SAFE mechanics concretely — the same headline `investment / cap` produces materially different founder outcomes — and to build the recognition and modelling skill you need when the real cap table on your desk has both flavours on it.

## Scenario — build your own

Construct a hypothetical company at the moment of Series-A pro-forma with the following:

- **Pre-priced-round cap table:**
  - Founder common: 8,000,000 shares.
  - Granted options: 200,000 shares.
  - Unissued option pool: 800,000 shares.
  - Starting FD (pre-SAFE-conversion): 9,000,000 shares.

- **SAFE stack (four SAFEs, all same terms across the two runs):**
  - SAFE 1: $250,000 investment, $5,000,000 cap, no discount. Signed 18 months before Series A.
  - SAFE 2: $500,000 investment, $8,000,000 cap, no discount. Signed 12 months before Series A.
  - SAFE 3: $500,000 investment, $10,000,000 cap, 20% discount. Signed 6 months before Series A.
  - SAFE 4: $750,000 investment, $12,000,000 cap, no discount. Signed 2 months before Series A.
  - Aggregate investment: $2,000,000. Aggregate cap-weighted percentage: `Σ (investment / cap) = 5% + 6.25% + 5% + 6.25% = 22.5%` (if all post-money).

- **Priced round:** $10,000,000 raised on $30,000,000 pre-money / $40,000,000 post-money, with a 10% post-close option pool placed pre-money per the term-sheet default.

## Requirements

Produce a single workbook with the following:

1. **SAFE register tab.** One row per SAFE with variant, investment, cap, discount, closing date, corporate-record reference. Two columns for treatment: "run 1 — all pre-money" and "run 2 — all post-money."
2. **Pre-money conversion tab.** Solve the four-SAFE conversion under the pre-money legacy mechanic (chapter 2). This requires iterative solving because each SAFE's shares depend on the shared pre-money FD denominator. Produce per-SAFE share count, per-SAFE percentage of pre-new-money FD, per-SAFE percentage of post-money FD, and the pool top-up sizing.
3. **Post-money conversion tab.** Solve the same four-SAFE conversion under the post-money mechanic (chapter 1). Use the `investment / post-money cap` identity to sanity-check, then produce the same set of per-SAFE outputs.
4. **Side-by-side comparison tab.** A summary table showing, for each SAFE and for the founder:
   - Pre-money share count.
   - Post-money share count.
   - Pre-money percentage of post-round FD.
   - Post-money percentage of post-round FD.
   - Difference (post-money minus pre-money) in absolute shares and in percentage points.
   Highlight the row for the founder: what is the delta on the founder's post-round percentage between the two mechanics? Express both in percentage points and in dollar value at the $40M post-money valuation.
5. **Mixed-stack scenario tab.** Run a third scenario in which SAFEs 1 and 2 are pre-money legacy and SAFEs 3 and 4 are post-money. Solve the coupled system correctly. Produce the pro-forma. Compare the founder's outcome to both homogeneous cases. Confirm the mixed-stack outcome sits between the two.
6. **Sensitivity chart.** A chart with the priced-round pre-money on the horizontal axis (varying from $15M to $50M) and the founder's post-round percentage on the vertical axis, with one line per mechanic (pre-money all-SAFEs, post-money all-SAFEs, mixed). The chart should show visually that the pre-money mechanic is founder-preserving as the priced-round valuation rises (SAFE holders share the priced-round dilution) while the post-money mechanic diverges from it (SAFE holders' slice is fixed).
7. **Two-page memo.** Written to the founder. Contents:
   - The two mechanics side-by-side with the specific arithmetic that distinguishes them.
   - The dollar cost of the difference at the modelled priced round.
   - Why the industry moved from pre-money to post-money in 2018 (from the SAFE holder's perspective).
   - What to do when you inherit a cap table with pre-money SAFEs on it: recognise it, model it, and consider whether to offer holders a conversion to post-money before the priced round.
   - What to do at the next SAFE signing: standardise on post-money for all new SAFEs; do not add a new post-money SAFE to a pre-money stack without disclosing to the pre-money holders.

## Starter guidance

- **Build the pre-money mechanic first.** It is more computationally demanding but conceptually simpler once you write the equations down. Use a spreadsheet with iterative calculation enabled, or use the closed-form solution when all SAFEs share a cap (see chapter 2 for the derivation).
- **The post-money mechanic can be verified two ways.** By solving the same iterative system with the redefined denominator, and by using the identity `investment / post-money cap = % of post-conversion pre-new-money company`. Both should agree.
- **The pool top-up placement matters.** Use the pre-money shuffle default (chapter 2 of mod-104). If you use a different pool placement, document it and be consistent across both runs.
- **The mixed stack is where the arithmetic gets fiddly.** The pre-money SAFEs and post-money SAFEs both add shares to the pre-new-money post-conversion base, but their share counts derive from different formulae. Solve the system: post-money SAFEs contribute a fixed percentage of the base; pre-money SAFEs contribute an amount that depends on the base and their cap. Two coupled equations.
- **Do not shortcut the pool.** The pool top-up sits inside the pre-money denominator and materially affects both mechanics' outcomes.
- **The founder-percentage delta between the two mechanics is not just a rounding difference.** Expect a 3-7 percentage point difference at typical seed-stage cap structures. If your model shows a difference under 1%, you've probably confused the mechanics.

## Acceptance criteria

- **Both mechanics are solved correctly**, verified by two independent methods (iterative solve and identity check for post-money; system of equations for pre-money).
- **The `investment / post-money cap` identity holds** for each post-money SAFE in the post-money run.
- **The per-SAFE percentages under the pre-money mechanic are lower than the `investment / cap` shortcut** would suggest (because pre-money SAFEs share the pool and the priced-round dilution).
- **The founder percentage under the pre-money mechanic is higher than under the post-money mechanic** for this specific setup (SAFEs share the priced-round dilution under pre-money but not under post-money).
- **The mixed-stack outcome sits between the two homogeneous cases** for the founder's percentage.
- **The sensitivity chart is legible** and shows the divergence between mechanics as the priced-round valuation rises.
- **The memo makes a specific recommendation** for handling a pre-money legacy SAFE inherited on a cap table, and quantifies the founder impact of the recognition-and-remediation choice.

## Deliverables

- The workbook with the register, pre-money, post-money, comparison, mixed-stack, and sensitivity tabs plus the chart.
- The two-page memo (Markdown or PDF).

## Extensions (optional)

- Add a **discount to two of the pre-money SAFEs** and recompute. The discount interacts with the cap in the pre-money mechanic in the same way as in the post-money mechanic (the holder picks the lower price), but the pre-money mechanic's shared-dilution property means the discount's benefit to the holder is different in absolute share terms.
- Add an **MFN clause to SAFE 1** and model what happens when SAFE 3's terms (cap + discount at $10M / 20%) trigger the MFN. Compare the pre-money and post-money mechanics for this scenario.
- Author a **conversion-amendment offer** the founder could send to a pre-money SAFE holder offering a switch to post-money terms in exchange for a modest cap improvement. Compute the specific cap improvement that would keep the SAFE holder economically indifferent, and the specific cap improvement that would meaningfully favour the SAFE holder in exchange for the switch.
- Interview a founder who signed pre-money SAFEs pre-2018 and ask them (or a proxy — a lawyer, a fund partner) what they wish they'd modelled before the priced round closed.
