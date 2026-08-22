# Exercise 04 — Liquidation Waterfall Under Multiple Scenarios

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 4 (liquidation waterfall and preference stacks). Uses a fully-loaded post-Series-B cap table.

## Problem statement

Build a scenario-capable liquidation-waterfall model for a company at Series-B with three preferred series (Seed, A, B) outstanding, and run the waterfall under a matrix of (exit price × preference structure) combinations. Produce the founder / employee / preferred payout table for each combination, generate the sensitivity chart of founder-vs.-VC payout across a plausible exit-price range, and author a board memo that explains what the preference-stack negotiation *actually costs* the founder at each plausible exit outcome.

The exercise proves that "sale above the last round" is not always a founder win, and that the preference-stack negotiation is worth as much or more than the pre-money-valuation negotiation at some exit prices.

## Scenario — build your own

Construct (or extend from Exercise 03) a Series-B cap table with the following minimum shape:

- **Founder common:** 8,000,000 shares (two founders, ~4M each; some vesting complications acceptable).
- **Employee common (exercised) + granted options:** 2,000,000 shares.
- **Unissued option pool:** 500,000 shares (post-Series-B, mostly consumed).
- **Series Seed preferred:** raised $2M; 2,000,000 shares; 1x preference.
- **Series A preferred:** raised $10M; 3,000,000 shares; 1x preference.
- **Series B preferred:** raised $30M; 5,000,000 shares; 1x preference.
- **Total fully-diluted:** ~20,500,000 shares.
- **Total invested preferred capital:** $42M.
- **Total post-money valuation of the last round (Series B):** somewhere around $120M-$150M.

You may vary the specific numbers but keep the aggregate preference in the $30M-$50M range and the total FD around 20M shares so the arithmetic is tractable.

## Requirements

Produce a single spreadsheet workbook with the following:

1. **Cap table input.** All classes with share counts, invested capital per preferred series, and the seniority order (senior stack: B > A > Seed by default; toggleable to pari passu in the sensitivity).
2. **Preference-structure switch.** A single cell that selects among:
   - **Structure 1:** All 1x non-participating, senior stack.
   - **Structure 2:** All 1x participating (no cap), senior stack.
   - **Structure 3:** Series B 1x participating with a 3x cap; Series A and Seed 1x non-participating; senior stack.
   - **Structure 4:** All 1x non-participating, pari passu (all preferences equal).
3. **Waterfall calculation.** For a given exit price, compute per-series the conversion decision (take preference vs. convert to common; for participating series, take capped-participation vs. converted; take the larger), then distribute the exit consideration through the resulting waterfall. Produce the per-holder payout table (founders separately, employees aggregated, each preferred series separately, option-holders as a group with strike-price netting).
4. **Exit-price sensitivity table.** For each of the four structures, compute the founder / employee / each-preferred-series payout across an exit-price range of ${30M, 50M, 80M, 120M, 180M, 300M, 500M}$. Present as a 6-column table (structures) × 7-row (exit prices) × 4-payout-column (founder, employee, VC, options) matrix.
5. **Sensitivity chart.** Line chart of founder payout as a function of exit price for each of the four structures, on a log-linear plot. The chart makes the "flip points" (where preferred conversion decisions change) visible.
6. **The critical exit-price analysis.** For each structure, identify:
   - The exit price at which the founder starts receiving anything material (past the aggregate preference).
   - The exit price at which the founder's payout equals their cap-table percentage × exit (the "clean pro-rata" point).
   - The exit price at which the pain of participation goes away (for structures 2 and 3 — the cap flip point).
7. **Board memo (2-3 pages).** Written to the board (or to the CEO's private council). Contents:
   - The four-structure comparison, with a table of founder payouts at three plausible exit prices ($50M / $120M / $300M).
   - The delta between structures at each exit price, in dollars.
   - The interpretation — which structure the founder should have negotiated for at each round, given the plausible-exit assumptions.
   - A specific recommendation on the *next* round's preference-structure negotiation, given what you now know.
   - A caveat noting that this is an economics exercise; the policy / negotiation guidance is in [`mod-108`](../../mod-108-term-sheets-and-preferred-stock-economics/) which builds on this.

## Starter guidance

- **The conversion decision has to be per-series and per-exit-price.** Don't hard-code "preferred always takes preference"; each series evaluates its own preference vs. its own converted payout and picks the larger. For senior stack the calculation is iterative: B decides first (against a residual denominator that includes A and Seed converted); then A decides (against a residual denominator that includes Seed converted); then Seed decides.
- **For participating preferred, the participating payout has to be capped correctly.** At a 3x cap on Series B, the max total payout for Series B under participating is 3x its investment = $90M. Above the exit price where participating would exceed the cap, Series B behaves as non-participating (or, in some certificate drafting, as "converted" — read the exact certificate language for your setup). Choose one convention and document it.
- **Options are a subtle line.** Vested options at exit are exercisable (or accelerated by change of control) and become common. Unvested options may or may not accelerate depending on the plan and per-grant agreement (single-trigger, double-trigger, no acceleration — pick a convention for your scenario and document it). The intrinsic value at exit is `max(0, exit_price_per_common - strike) × shares`.
- **The founder line is what a real founder cares about.** Show it prominently. The CEO's practical question is "how much do I take home at each exit price under each structure" — the memo should answer that directly.
- **The chart is the artefact for the board conversation.** Make it clean, log-linear, four structure lines, with the flip points labelled.
- **Do not double-count the pool.** Unissued pool at exit is worth zero if it's not granted; if you're modelling it as fully-vested-common at exit, note the choice and justify.

## Acceptance criteria

- **All four structures produce internally-consistent waterfalls.** Sum of payouts equals exit consideration for every scenario.
- **Per-series conversion decisions are computed** (not hard-coded) and change with exit price.
- **The founder payout under Structure 1 (non-participating) is materially higher than under Structure 2 (participating)** at exit prices well above the aggregate preference. Confirm this in your model.
- **The founder payout under Structure 3 (capped participation) sits between Structures 1 and 2** at most exit prices, and equals Structure 1 above the cap-flip exit price.
- **The founder payout under Structure 4 (pari passu, non-participating) equals Structure 1** at exit prices above the aggregate preference (they're the same non-participating outcome at that point) and differs only at exit prices below aggregate preference.
- **The sensitivity chart is legible** — four structure lines, exit price on x-axis, founder payout on y-axis, flip points annotated.
- **The critical exit-price analysis names specific dollar values** for each threshold under each structure.
- **The board memo makes a specific next-round recommendation** and quantifies its dollar value.

## Deliverables

- The workbook with the input, switch, waterfall, sensitivity, and chart.
- The 2-3-page board memo (Markdown or PDF).

## Extensions (optional)

- Add a **redemption right** to Series B (rare but possible): the right for Series B to require redemption at 1x + accrued dividends after year 5. Model the redemption event and its interaction with the waterfall.
- Add **anti-dilution recalculation** — Series A was issued at $3.33 per share; suppose a hypothetical Series B was issued at $2.00 (a down round from a $30M pre / $10M raise Series A to a $50M pre / $30M raise Series B — a slight numerical stretch given the setup but useful for the exercise). Compute the broad-based weighted-average adjustment to the Series A conversion ratio and re-run the waterfall. Compare to the un-adjusted waterfall. (Full anti-dilution treatment is [`mod-108`](../../mod-108-term-sheets-and-preferred-stock-economics/); this exercise just illustrates the mechanic.)
- Add a **stock-for-stock acquisition** scenario where the exit consideration is a mix of cash + acquirer stock. Model the tax and lock-up implications at a high level.
- Interview a founder who has been through an exit at a low sale price and ask them what they wished they'd known about the waterfall at the time of the round.
