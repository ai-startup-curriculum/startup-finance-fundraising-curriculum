# Stacking Multiple Convertibles — The Priced-Round Pro-Forma

## Why this matters

Chapters 1-3 handled one instrument at a time. In real life the priced-round CFO sits down two weeks before closing with a stack: three or five or seven SAFEs signed over the last eighteen months, a note or two from the friends-and-family bridge, an MFN'd side letter from the second closing, and a term sheet that wants a specific target ownership for the incoming Series-A lead. The job is to produce a single pro-forma cap table that reconciles all of this to the closing math the term sheet promises.

That pro-forma is the artefact the founder actually cares about. It is also the artefact the diligence firm reviews line by line and the artefact the lead investor's counsel red-lines in the closing docs. Every number on it derives from the instruments in the stack, the priced-round terms, and the option-pool decision from [`mod-104`](../mod-104-cap-tables-and-equity-compensation/02-pre-vs-post-money-math-and-the-option-pool-shuffle.md). Every number has to tie back to a specific instrument in the corporate record (mod-104 chapter 1).

This chapter walks the mechanics end to end.

## The pro-forma stack — a realistic example

Set up a company at the moment of Series-A closing negotiations:

**Existing capital (pre-priced-round):**
- Founder common: 8,000,000 shares (two founders, 4M each, both 24 months into a 4-year vest).
- Employee common (exercised): 100,000 shares.
- Granted options (unexercised): 400,000 shares.
- Unissued option pool: 500,000 shares.

**Stacked convertibles (in the order they were signed):**
- SAFE 1 — Post-money, cap only, $250K, $5M post-money cap. Signed 18 months before Series A. Friends-and-family closing.
- SAFE 2 — Post-money, cap only, $500K, $6M post-money cap. Signed 15 months before Series A. Angel closing.
- SAFE 3 — Post-money, cap + discount, $500K, $8M post-money cap, 20% discount. Signed 10 months before Series A. YC batch closing.
- SAFE 4 — Post-money, cap only with MFN clause, $1,000K, $10M post-money cap, MFN active. Signed 6 months before Series A. Institutional seed lead.
- SAFE 5 — Post-money, cap only, $750K, $12M post-money cap. Signed 2 months before Series A. Small institutional co-invest.
- Note 1 — Convertible note, $500K principal, 6% simple interest, 24-month maturity, 20% discount, $10M pre-money cap, QF threshold $2M. Signed 8 months before Series A.

**Priced-round terms (as offered on the term sheet):**
- Raise: $10,000,000 new money.
- Pre-money valuation: $30,000,000.
- Post-money valuation: $40,000,000.
- Target post-close option pool: 10% of post-money, placed pre-money per the term-sheet default (the option-pool shuffle from mod-104 ch. 2).

Everything about this stack is realistic for a seed-programme-to-Series-A conversion. It is also nasty to model correctly. This chapter walks it.

## Step 1 — freeze the pre-priced-round base

The first job is a clean pre-priced-round fully-diluted number that does not yet include any SAFE conversions, note conversions, or pool top-ups. Call this the "starting FD."

```
Founder common:                    8,000,000
Employee common (exercised):         100,000
Granted options (unexercised):       400,000
Unissued option pool:                500,000
----------------------------------------------
Starting FD:                       9,000,000
```

Every SAFE and note conversion will be added to this base; the pool top-up will be added last. Nothing in the starting FD is contingent — it is the actual pre-priced-round cap table before any convertible triggers.

## Step 2 — apply MFN cascades and side-letter amendments

Before touching the conversion arithmetic, adjudicate the MFN and side-letter effects on each SAFE's *effective* terms. This is where chapter 5's material becomes load-bearing: an MFN clause on an earlier SAFE may adopt the more-favourable terms of a later SAFE.

For the example stack:

- SAFE 4 has an active MFN. SAFE 4's terms are `$10M cap, no discount`.
- SAFEs 3 and 5 exist as "later" instruments relative to SAFE 4 chronologically? No — SAFE 4 was signed *before* SAFE 5. The MFN typically looks *forward* (adopting later terms), not backward. So SAFE 4's MFN examines SAFEs 5 and beyond.
- SAFE 5's cap is $12M (worse for the SAFE holder — a higher cap means fewer shares per dollar), and it has no discount. Nothing to adopt.
- No SAFE signed between SAFE 4 and Series A has better terms than SAFE 4's $10M cap. So the MFN in SAFE 4 does not trigger.

In a different scenario — if SAFE 5 had been $750K at $8M cap with a 15% discount — SAFE 4's MFN would amend SAFE 4 to adopt those terms, and SAFE 4 would convert as if it were `$1M at $8M cap with 15% discount`. Chapter 5 walks this in more detail.

For now, the effective terms table for the stack:

| Instrument | Effective cap | Effective discount | Notes |
|---|---|---|---|
| SAFE 1 | $5M post-money | — | |
| SAFE 2 | $6M post-money | — | |
| SAFE 3 | $8M post-money | 20% | Cap + discount — holder picks better |
| SAFE 4 | $10M post-money | — | MFN inactive (no later SAFE triggers it) |
| SAFE 5 | $12M post-money | — | |
| Note 1 | $10M pre-money | 20% | Cap + discount — noteholder picks better; principal + interest at conversion |

## Step 3 — accrue interest on notes

Note 1's principal at signing was $500,000. Elapsed time from signing to Series-A closing: 8 months, then... assume Series A closes now, so total accrual = 8 months at 6% simple = `$500,000 × 0.06 × (8/12) = $20,000`. Effective note value at conversion = $520,000.

Update the effective terms table to reflect Note 1's $520,000 effective investment amount.

## Step 4 — solve for the conversion prices

This is the arithmetic-heavy step. Under the post-money SAFE mechanic, each post-money SAFE holder's shares are:

`SAFE_i shares = investment_i / SAFE_i price`, where `SAFE_i price = SAFE_i cap / (starting-FD + all-SAFE-shares + note-shares + pool-top-up-shares)`.

The pool top-up depends on the total post-close FD (a target of 10% of post-money), which depends on all the SAFE and note share counts, which depend on the pool top-up. Circular. Solve iteratively.

For a post-money SAFE, the identity `investment_i / cap_i = % of pre-new-money post-conversion company` holds — that's the point of the post-money form (chapter 1). So each SAFE holder's target percentage of the pre-new-money post-conversion base is:

- SAFE 1: $250K / $5M = 5.00%
- SAFE 2: $500K / $6M = 8.33%
- SAFE 3: $500K / $8M = 6.25%
- SAFE 4: $1,000K / $10M = 10.00%
- SAFE 5: $750K / $12M = 6.25%

Combined SAFE percentage: **35.83%** of the pre-new-money post-conversion company.

For the note, the conversion price is `min(discounted QF price, cap-implied price)`. The QF price = `$30M / (pre-new-money post-conversion FD)`. The cap-implied price = `$10M / (pre-money FD)`. We solve after fixing the SAFE shares.

For SAFE 3 (cap + discount), the SAFE holder picks the lower of the cap-implied price and the discounted priced-round price. Under the post-money cap, the SAFE 3 holder's shares are `$500K / SAFE_3 price`, where `SAFE_3 price = min(cap_3 / (starting-FD + all-SAFE-shares + note-shares + pool-top-up-shares), 0.80 × QF price)`. If the discount price is lower, SAFE 3 gets more shares than the cap-only calculation would suggest.

To solve cleanly, first assume the cap controls for SAFE 3 (typically true when the priced round is well above the cap). Then compute all SAFE shares and the note shares and the pool top-up. Then check the discount assumption; if the discounted QF price is lower than the cap-implied price for SAFE 3, redo with SAFE 3 converting at the discount instead of the cap. Iterate.

### The direct calculation using post-money SAFE identities

Because each post-money SAFE holder's target is `investment / cap` of the post-conversion base (pre-new-money), we can write:

- Let `X` = post-close total FD (after new money, after pool top-up, after all conversions).
- New investor = 25% × `X` (= $10M / $40M post-money).
- Post-close pool = 10% × `X`.
- Note-holder shares = `(principal + interest) / conversion price`. Let `n_shares` = note shares. Note-holder percentage of post-conversion pre-new-money base = `n_shares / (X - new-investor-shares - post-round-pool-fresh-shares)`. Complicated because the note's cap is pre-money, not post-money, and the note's discount fires against the QF price.

Simplification: solve the SAFE stack first using post-money identities, then compute the note against the resulting pre-new-money base and iterate.

**SAFE stack, closed-form.**

Combined SAFE percentage of pre-new-money post-conversion base = 35.83% (from above). Founder + employee common + granted options + unissued starting pool + note shares + pool top-up = the remaining 64.17% of the pre-new-money post-conversion base.

Let the pre-new-money post-conversion base be `B`. Then:

- SAFE shares (aggregate) = 0.3583 × `B`.
- Founder + employee common + granted options + unissued starting pool = 8,000,000 + 100,000 + 400,000 + 500,000 = 9,000,000 shares. This is fixed.
- Note shares = `n_shares`. This adds to the same base.
- Pool top-up over the starting 500,000: also adds to the same base.

The pre-new-money post-conversion base `B` includes the *pre-money* option pool (i.e., the starting 500K pool plus the top-up brought in by the priced round). Under the pre-money shuffle default (mod-104 ch. 2), the pool is topped up to reach 10% of post-money, and post-money = `B / (1 - new_investor_%)` = `B / 0.75`.

- Post-money = `B / 0.75`.
- Post-close pool target = 10% of post-money = 0.10 × `B / 0.75` = `B × 0.1333`.
- Pool top-up = 0.1333 × `B` - 500,000.

So `B = 9,000,000 - 500,000 + (0.1333 × B) + n_shares + 0.3583 × B` (writing the starting FD without the pool, then adding the pool as topped up).

Wait — let me restructure. `B = existing-common-and-granted-options + full-pool + SAFE-shares + note-shares`.

- Existing common + granted options = 8,000,000 + 100,000 + 400,000 = 8,500,000.
- Full pool (topped up) = 0.1333 × `B`.
- SAFE shares = 0.3583 × `B`.
- Note shares = `n_shares`.

So `B = 8,500,000 + 0.1333 × B + 0.3583 × B + n_shares`, i.e. `B × (1 - 0.1333 - 0.3583) = 8,500,000 + n_shares`, i.e. `0.5083 × B = 8,500,000 + n_shares`, i.e. `B = (8,500,000 + n_shares) / 0.5083`.

We need `n_shares` to close this. Fix the note-holder mechanic:

**Note conversion arithmetic.** Note has principal + interest = $520,000, 20% discount, $10M pre-money cap. Pre-money FD (for the cap-implied price) is the pre-new-money post-conversion base excluding the note itself and excluding the SAFEs? No — read the note carefully.

The typical note definition of "pre-money valuation cap" references the pre-money FD of the priced round *including* pool top-up and *including* other converted SAFEs and notes. So the cap-implied note price is `$10M / (B - n_shares - anything the note explicitly excludes)`. If the note excludes only its own shares, price = `$10M / (B - n_shares)`.

QF price (post-shuffle) = `$30M / (B)`. Discounted QF price = `$0.80 × $30M / B = $24M / B`.

Note conversion price = `min($10M / (B - n_shares), $24M / B)`. To identify which controls:

- If cap controls: `n_shares = $520,000 / ($10M / (B - n_shares)) = $520,000 × (B - n_shares) / $10M = 0.052 × (B - n_shares)`, so `n_shares × 1.052 = 0.052 × B`, so `n_shares = 0.0494 × B`.
- If discount controls: `n_shares = $520,000 / ($24M / B) = $520,000 × B / $24,000,000 = 0.02167 × B`.

Cap gives 4.94% × B; discount gives 2.17% × B. The larger share count (better for the note-holder) is the cap. So cap controls. `n_shares = 0.0494 × B`.

Substitute back: `B = (8,500,000 + 0.0494 × B) / 0.5083`, i.e. `B × 0.5083 = 8,500,000 + 0.0494 × B`, i.e. `B × (0.5083 - 0.0494) = 8,500,000`, i.e. `B × 0.4589 = 8,500,000`, i.e. `B = 18,516,000`.

Now back-solve:

- Note shares: 0.0494 × 18,516,000 = 914,690 shares. Note-holder ownership of pre-new-money post-conversion base = 4.94%.
- SAFE shares (aggregate): 0.3583 × 18,516,000 = 6,634,290 shares. Distribute across the five SAFEs by their `investment / cap` ratios:
  - SAFE 1: 5.00% × 18,516,000 = 925,800 shares.
  - SAFE 2: 8.33% × 18,516,000 = 1,542,383 shares.
  - SAFE 3: 6.25% × 18,516,000 = 1,157,250 shares.
  - SAFE 4: 10.00% × 18,516,000 = 1,851,600 shares.
  - SAFE 5: 6.25% × 18,516,000 = 1,157,250 shares.
  - Total: 6,634,283 shares (rounding).
- Pool topped-up: 0.1333 × 18,516,000 = 2,468,183 shares. Pool top-up over starting 500K = 1,968,183 new pool shares.
- Post-money total FD: `B / 0.75` = 18,516,000 / 0.75 = 24,688,000 shares.
- New investor: 0.25 × 24,688,000 = 6,172,000 shares of Series-A preferred.

**Priced-round price per share.** `$30M / B` = $30,000,000 / 18,516,000 = **$1.62 per share**. New investor cheque `$10M / $1.62 = 6,172,000 shares`. Matches.

**Cap-implied note price** for verification: `$10M / (B - n_shares)` = $10,000,000 / (18,516,000 - 914,690) = $10,000,000 / 17,601,310 = **$0.568 per share**. The note holder converts at $0.568 vs. a discounted priced-round price of `$1.62 × 0.80 = $1.296`. The cap is well below the discount, so the cap controls, confirming the assumption.

## Step 5 — assemble the pro-forma cap table

```
Class                           Shares       % Post-money  % Pre-money-FD
-----------------------------------------------------------------------------
Founder common                    8,000,000       32.40%        43.20%
Employee common (exercised)         100,000        0.41%         0.54%
Granted options (unexercised)       400,000        1.62%         2.16%
Post-close option pool            2,468,183       10.00%        13.33%
SAFE 1 as-converted                 925,800        3.75%         5.00%
SAFE 2 as-converted               1,542,383        6.25%         8.33%
SAFE 3 as-converted               1,157,250        4.69%         6.25%
SAFE 4 as-converted               1,851,600        7.50%        10.00%
SAFE 5 as-converted               1,157,250        4.69%         6.25%
Note 1 as-converted                 914,690        3.70%         4.94%
Series-A preferred                6,172,000       25.00%          n/a
-----------------------------------------------------------------------------
Total post-close FD              24,688,156      100.00%       100.00%
```

The pool top-up is 1,968,183 new shares over the starting 500,000. The founder's post-close percentage is 32.40% (down from an implied 88.89% before any convertible or new-round dilution had happened — 8,000,000 / 9,000,000). The convertibles + new investor + pool absorbed 56.5 percentage points of founder ownership.

## Step 6 — reconcile against the term sheet

The lead investor's counsel will run this same calculation and produce a cap-table exhibit for the closing documents. The pro-forma above should match line-by-line. Common reconciliation issues:

- **Investor percentage doesn't match term sheet.** Term sheet says 25%; pro-forma shows 24.5% or 25.5%. Usually a pool-target rounding difference (10.0% exactly vs. 10.0% target-with-integer-shares) or a SAFE-conversion assumption difference (e.g., the note conversion price being computed on a slightly different denominator). Reconcile the denominators.
- **Pool doesn't match target.** Term sheet says 10% post-close pool; pro-forma shows 9.6% or 10.4%. Usually the difference between "pool of 10% including or excluding this round's grants" or "pool sizing including or excluding the note conversion." Both parties have to agree on which convention.
- **SAFE percentages sum to something the SAFE holders don't expect.** If a SAFE holder computed `investment / cap` and got 10% and now sees 7.5% on the pro-forma post-money view, they will question it. The gap is the pool top-up (which is a share-count add that dilutes SAFE holders on a post-money-of-post-close basis but does not dilute them on a pre-new-money post-conversion basis) — the SAFE holder's 10% is 10% of pre-new-money, which is 7.5% of post-money = pre-new-money × 0.75. Explain this before the SAFE holder complains.
- **Note interest accrual doesn't match investor expectations.** The noteholder computed accrued interest on a different day-count convention (30/360 vs. actual/actual, or including or excluding the closing day). Small differences but real.

## Step 7 — build the sensitivity block

The pro-forma above is the base case. The CFO should also produce a sensitivity block on the two axes that matter most:

**Pre-money valuation.** Rerun with pre-money at $25M and $35M in addition to the $30M base. The founder cares because the pre-money is the main negotiation lever; the founder sees the founder-percent under each and can then decide how hard to hold on the $30M line.

**Pool size.** Rerun with pool at 8%, 10%, 12%. This surfaces the option-pool shuffle from mod-104 chapter 2 in the specific context of this stack — the founder can see how much of their dilution comes from the pool vs. from the raise itself.

**Combined footprint sensitivity.** The right way to think about pool + pre-money is combined footprint. A table with pre-money on the horizontal axis and pool on the vertical axis, showing founder-percent in each cell, is the artefact that lets the founder negotiate the whole envelope.

## The pool top-up interaction with the SAFE stack

A subtle point buried in the arithmetic above: the pool top-up is placed pre-money (the term-sheet default), which means the top-up shares are added to the pre-new-money post-conversion base *before* the post-money SAFE identity fires. If the pool target were placed post-money instead — i.e., the top-up happens after the new money hits, and the top-up dilutes everyone including the new investor — the SAFE holders would still get their fixed `investment / cap` percentage of the pre-new-money base, but the pool top-up itself would come out of the founder + new investor rather than just the founder.

Rerun for the post-money pool placement:

- Pool target = 10% of post-money.
- Under post-money placement, the pool top-up is added to post-money, and existing pre-new-money holders (founder, SAFE holders, note holder) are diluted alongside the new investor.
- The mechanic: new investor = 25% × X_pre, SAFE holders keep `investment / cap` × X_pre where X_pre is the pre-new-money base *including* the pool top-up post-money. If the pool is placed post-money, the pool top-up doesn't sit inside X_pre.

Working through this carefully (leaving the algebra to a spreadsheet), the founder's stake improves by roughly 2-4 percentage points relative to the pre-money placement. This is the specific dollar cost of the shuffle for this particular stack. Chapter 2 of mod-104 covers the shuffle math generally; the stacked-SAFE case here is where it collides with the note and the SAFE stack.

## What the founder should walk into the closing with

- The pro-forma cap table above, at the term-sheet valuation and pool target.
- A sensitivity block on pre-money × pool.
- A **line-item ownership walk**: starting founder percent at pre-priced-round → dilution from each SAFE conversion → dilution from note conversion → dilution from pool top-up → dilution from new investor. This decomposes the total ~56 percentage points of founder dilution into its components so the founder can see which line item is the biggest.
- A **per-SAFE holder as-converted position** with each SAFE holder's specific share count and percentage. Attach the pro-rata side-letter status per SAFE holder so the round-size discussion knows how many pro-rata cheques will be requested.
- A **note maturity dashboard** showing this note (and any others) with the QF trigger and the actual conversion at this round. Confirm the QF threshold was met.
- The **reconciliation to the corporate record** — each row on the pro-forma tied to its instrument (SAFE 1 to its executed SAFE, note 1 to its executed note, pool to the board-authorised pool-expansion consent that would fire at closing, etc.).

## Common pro-forma failure modes

- **Not iterating.** The calculation is circular (SAFE prices depend on pool, pool depends on SAFE prices, note depends on both). Spreadsheet with iterative calc enabled, or an algebraic closed form using the post-money identity, is required. Hand-calculating misses the circularity.
- **Mixing pre-money and post-money mechanics.** If the SAFE stack has both, run the pre-money SAFEs through the pre-money mechanic (chapter 2) and the post-money SAFEs through the post-money mechanic (chapter 1) in the same solve. Do not use a single formula for both.
- **Applying MFN cascades late.** The MFN's effect on each SAFE's effective terms has to happen *before* the conversion arithmetic, not after. Otherwise the shares assigned to an MFN'd SAFE are wrong. Chapter 5 goes into detail.
- **Missing the note interest.** A material dollar amount that translates directly into shares.
- **Assuming the pool is post-money when the term sheet says pre-money.** The default in the NVCA term sheet is pre-money placement. Don't run a post-money-pool pro-forma against a pre-money-pool term sheet.
- **Founder walking into the meeting without the pro-forma.** The founder should have run this before signing the term sheet, not the day before closing. The term sheet is the moment to negotiate the pool size and the pre-money together (mod-104 ch. 2); the pro-forma quantifies the trade.

## What good looks like

A CFO or founder who has this material installed produces a Series-A pro-forma workbook that:

- Has one tab per convertible with the instrument's specific terms and its as-converted share count under the current base.
- Has a solver tab that iterates the SAFE, note, and pool arithmetic to convergence.
- Has a pro-forma summary tab identical in format to the mod-104 cap-table summary.
- Has a sensitivity block on pre-money × pool.
- Has a line-item founder-dilution walk.
- Ties every line back to a specific instrument.
- Is reviewed by counsel before signing the term sheet, not after.

## Summary

- The priced-round pro-forma is the artefact that reconciles the stack of seed convertibles to the priced-round terms. It is the single most important cap-table document at closing.
- The correct order of operations: freeze the pre-priced-round base, apply MFN cascades and side-letter amendments to each convertible's effective terms, accrue interest on notes, solve for the conversion shares iteratively (SAFE and note shares are coupled through the pool and the pre-money denominator), assemble the pro-forma, reconcile to the term sheet.
- Under the post-money SAFE mechanic, the aggregate SAFE percentage of the pre-new-money post-conversion company is just the sum of `investment / cap` across the SAFEs (a nice closed-form identity). The note and the pool top-up have to be layered on top.
- Under the pre-money mechanic (chapter 2), the SAFE stack requires a system of equations. Under mixed stacks, both mechanics run in the same solve.
- The pool placement (pre-money vs. post-money) interacts with the SAFE stack in a specific way: pre-money placement dilutes founder alone, post-money placement dilutes founder + SAFEs + note + new investor.
- The sensitivity block on pre-money × pool is what the founder brings to the term-sheet negotiation. Signing without the pro-forma concedes 2-5% of founder stake by default.

Chapter 5 handles the MFN and side-letter mechanics that quietly rewrite the pro-forma when triggered.
