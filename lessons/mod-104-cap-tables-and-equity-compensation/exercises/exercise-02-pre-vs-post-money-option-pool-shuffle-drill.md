# Exercise 02 — Pre vs. Post-Money and the Option-Pool Shuffle Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 2 (pre-money vs. post-money math and the option-pool shuffle). Builds on the cap-table skeleton from Exercise 01.

## Problem statement

Take a Series-A term sheet with a specified pre-money valuation, investment amount, and target post-close option pool, and model the resulting post-close cap table under three treatments: (1) the pre-money pool shuffle (term-sheet default), (2) the post-money pool treatment, and (3) a split treatment (half pre / half post). Quantify the founder-dilution difference across the three treatments in dollars and percentage points. Author a term-sheet negotiation memo that recommends a specific counter-position on the pool clause and quantifies its value.

The exercise proves the core arithmetic claim of the chapter: the pool-vs.-pre-money combined footprint controls 2-5% of the founder's stake, and the pool clause is the fine-print battle worth fighting.

## Scenario — build your own

Use the cap table from Exercise 01 as the pre-close starting point (or construct a fresh one with the same shape). Then set up the Series-A term sheet with:

- **Pre-money valuation:** $30M (or pick a number defensible against the company you built in Exercise 01).
- **Investment amount:** $10M.
- **Target post-close option pool:** 12% of post-money fully diluted (a common Series-A ask; you may vary between 10% and 15% if you want to see the sensitivity).
- **Preferred class:** Series A, 1x non-participating (the founder-favourable baseline).
- **Assume the outstanding SAFEs from Exercise 01 convert at this round** under their own mechanics — post-money SAFEs at their caps, pre-money SAFEs at their caps + priced-round dilution.

## Requirements

Produce a single spreadsheet or notebook with the following:

1. **Pre-close cap table** carried forward from Exercise 01 or reconstructed. Fully-diluted breakdown by class, with as-converted SAFE share counts.
2. **Treatment 1 — pre-money pool shuffle.** The 12% pool sits on the post-money base, achieved by expanding the pool *before* the money hits. Compute:
   - Post-expansion pre-money fully-diluted share count.
   - Share price = pre-money valuation / post-expansion pre-money FD.
   - Series A shares issued = investment / share price.
   - Post-close fully-diluted cap table (all classes, with percents).
   - Founder ownership post-close.
3. **Treatment 2 — post-money pool.** The 12% pool sits on the post-money base, expanded *after* the money hits. Compute:
   - Share price = pre-money valuation / pre-close pre-money FD (no pool expansion).
   - Series A shares issued = investment / share price.
   - Additional pool shares needed to reach 12% of the post-close FD (this requires iteration because the pool sits inside the denominator).
   - Post-close fully-diluted cap table (all classes, with percents).
   - Founder ownership post-close.
   - Effective post-close Series A ownership — it will be lower than 25% because the pool now sits alongside the investor rather than under them.
4. **Treatment 3 — split.** The pool is expanded partly pre-money (say, 8%) and partly post-money (say, 4%). Compute as in Treatment 1 but with the reduced pre-money expansion, then add the remaining post-money expansion. Founder ownership post-close falls between Treatments 1 and 2.
5. **Sensitivity table.** For each of the three treatments, vary the target pool size across {8%, 10%, 12%, 14%, 16%} and produce a matrix of founder ownership post-close. The chart shows the founder-dilution slope per percentage-point of pool.
6. **Effective pre-money per share.** For each treatment, compute the effective per-share price paid by the incoming investor (i.e., the post-close per-share price). The pre-money shuffle produces a lower per-share price than the post-money treatment; the difference is the visible cost of the shuffle. Report this as `$X.XX per share` for each treatment, and as a percentage discount vs. the headline "pre-money / pre-close FD" naïve calculation.
7. **Negotiation memo (1-2 pages).** Written to the founder / CEO. Contents:
   - The current term-sheet clause on the option pool (in one sentence).
   - The three treatments' outcomes for founder ownership, in a table.
   - The dollar value of the founder-dilution difference at a plausible exit price (pick $150M-$300M and use the founder's post-close percent × exit price as the residual — ignore waterfall for now).
   - The recommended counter-position on the pool clause — either a specific red-line to the pool-treatment language, or a smaller pool sized to a hiring plan (which you can gesture at without fully building — Exercise 03 builds it), or a trade of pool size against pre-money valuation.
   - The recommended counter-position, in the specific words that would go into a term-sheet response email.

## Starter guidance

- **Model the SAFE conversion at the round.** Post-money SAFEs convert to their `investment / post-money cap` share of the post-conversion company at their own cap, unrelated to the Series-A pricing. Pre-money SAFEs convert to their `investment / pre-money cap` share of the pre-conversion company, then get diluted by the Series-A shares. This is the specific mechanic where founders regularly miscalculate.
- **The pool-in-denominator iteration** in Treatment 2 is where most spreadsheets break. Either use a small iterative-calc formula (Google Sheets and Excel both support iterative calculation via settings), or solve the linear equation by hand: `pool_new = (target% × total_new) - pool_existing`, and `total_new = pre-close_ex_pool + pool_new + Series_A_shares`. Substitute.
- **The founder-dilution comparison must hold everything else constant.** In particular, hold Series A investor's target ownership at whatever the treatment produces — do not "make it fair" by artificially forcing 25% in Treatment 2 (the natural outcome in Treatment 2 is less than 25% because the pool now dilutes them too).
- **The effective per-share price is the diagnostic.** Two term sheets can quote the same pre-money and produce very different effective per-share prices depending on the pool treatment. This is the number to internalise.
- **The negotiation memo should not read like a math exercise.** It should read like a memo to the CEO that they could hand to their lawyer for a term-sheet response. Include the specific words to send.

## Acceptance criteria

- **All three treatments produce internally-consistent post-close cap tables.** Fully-diluted percents sum to 100%.
- **Treatment 1 founder ownership is materially lower than Treatment 2.** (Typically 2-5 percentage points; the exact number depends on your setup.)
- **Treatment 3 sits between Treatments 1 and 2.**
- **The sensitivity table shows the linear-ish relationship** between pool size and founder dilution under each treatment. The slope is different for each treatment.
- **The effective per-share price is computed for each treatment**, in dollars per share and as a discount to the naïve headline.
- **The negotiation memo names a specific counter-position** and quantifies its dollar value to the founder at a plausible exit.
- **The SAFE conversion mechanic is correct for both post-money and pre-money variants.**

## Deliverables

- The workbook (.xlsx or Google Sheets link) with all cap-table treatments and the sensitivity table.
- The 1-2-page negotiation memo (Markdown or PDF), or a memo tab in the workbook.

## Extensions (optional)

- Add a fourth treatment: shares-based pool sizing (pool specified as an absolute share number derived from a hiring plan, rather than as a percent of post-money). Compare to Treatment 2.
- Model the Series-B round on top, with another pool top-up under each of the three treatments. Compute compounding founder dilution from formation through Series-B.
- Add anti-dilution mechanics from the Series Seed preferred (broad-based weighted-average) if the Series A price-per-share is below the Seed price-per-share. Show the recalculation of the Seed conversion ratio and the impact on the Series-A round math. (Full anti-dilution treatment is mod-108; this exercise just needs to acknowledge the mechanic.)
- Interview a founder or CFO who has closed a Series-A about how the pool clause was actually negotiated in their round. Compare the negotiation dynamics in real life to the mechanical analysis in this exercise.
