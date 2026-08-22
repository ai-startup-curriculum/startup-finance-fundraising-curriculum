# Exercise 04 — Stacked Convertibles Priced-Round Pro-Forma

**Estimated time:** ~5 hours
**Prerequisites:** Chapters 1-4 (all four cover mechanics; chapter 4 is the target). Also uses [`mod-104`](../../mod-104-cap-tables-and-equity-compensation/) chapters 1-2.

## Problem statement

Take the stacked-convertible cap table from the worked example in chapter 4 (five SAFEs + one note + a full option-pool shuffle at Series-A closing) and build the full priced-round pro-forma workbook. The workbook must implement the iterative conversion arithmetic, reconcile against the term-sheet terms, produce a sensitivity block on pre-money × pool, and generate the founder-dilution walk from starting FD to post-close. Then extend the scenario in three ways: (a) add an MFN cascade that fires on one of the SAFEs; (b) replace one post-money SAFE with a pre-money legacy SAFE (creating a mixed stack); (c) run a "SAFE cleanup" scenario in which the founder converts the pre-money SAFEs to post-money before the priced round in exchange for a modest cap improvement.

This is the flagship modelling exercise for the module. It exercises every mechanic from chapters 1-4 in a single artefact.

## Scenario — start from the chapter 4 example

Use the chapter 4 worked-example stack verbatim as the base case:

- Founder common: 8,000,000 shares. Employee common: 100,000. Granted options: 400,000. Unissued pool: 500,000.
- SAFE 1: post-money, $250K at $5M post-money cap.
- SAFE 2: post-money, $500K at $6M post-money cap.
- SAFE 3: post-money cap + discount, $500K at $8M post-money cap, 20% discount.
- SAFE 4: post-money with MFN, $1,000K at $10M post-money cap.
- SAFE 5: post-money, $750K at $12M post-money cap.
- Note 1: convertible note, $500K principal, 6% simple, 24-month maturity, 20% discount, $10M pre-money cap, QF threshold $2M. Signed 8 months before Series A.
- Priced round: $10M raised on $30M pre / $40M post, target 10% post-close pool placed pre-money.

## Requirements

Produce a single workbook (tabs listed below) plus a reconciliation memo:

1. **Instrument register.** One row per instrument (5 SAFEs + 1 note). Columns: instrument type, variant, investment amount, cap, discount, MFN flag, pro-rata side letter flag, closing date, corporate-record reference. For the note: also principal, interest rate, maturity date, QF threshold, and accrued interest as of the closing date.
2. **Priced-round assumptions.** Pre-money valuation, raise size, target post-close pool percentage, pool placement (pre-money or post-money — default pre-money), assumed closing date.
3. **Pre-priced-round cap table.** The four-share-count header (authorised, issued, outstanding, fully diluted) per mod-104 chapter 1, showing the starting FD of 9,000,000 shares.
4. **Iterative solver.** A tab that computes, iteratively, the SAFE share counts, the note share count, the pool top-up, and the priced-round investor share count. Show the iteration explicitly (either via Excel/Sheets iterative-calc mode with the circular reference, or via a manual iteration loop with visible convergence).
5. **Pro-forma cap table.** The full post-close cap table with per-line share counts, per-line percentages of pre-new-money FD, and per-line percentages of post-money. Match the chapter 4 output to within rounding.
6. **Term-sheet reconciliation.** A table with the target term-sheet numbers on one side (new investor 25%, pool 10%, etc.) and the pro-forma actuals on the other, with the delta. Any material delta (>0.5 percentage points) called out and reconciled.
7. **Founder-dilution walk.** A waterfall chart or table showing the founder's percentage at each step: starting FD (88.89%), post-SAFE-1, post-SAFE-2, ..., post-note, post-pool-top-up, post-new-money. Attribute the percentage-point decline to each event.
8. **Sensitivity block.** A 5×5 grid with pre-money valuation on one axis (varying $20M, $25M, $30M, $35M, $40M) and pool percentage on the other ($8%, 9%, 10%, 11%, 12%). Cells: founder post-close percentage. Highlight the term-sheet base cell.
9. **Extension A — MFN cascade.** Assume SAFE 4's MFN triggers on SAFE 3 (hypothetical: SAFE 3's terms are more favourable than SAFE 4's original $10M cap; SAFE 4 elects). Rewrite SAFE 4's effective terms and re-run the pro-forma. Compare against the base case: how many percentage points of founder dilution does the MFN cost?
10. **Extension B — mixed pre/post stack.** Replace SAFE 1 with a pre-money legacy SAFE at the same $ and cap. Re-solve the coupled system (post-money SAFEs contribute a fixed percentage of the pre-new-money base; the pre-money SAFE contributes an amount that depends on the pre-money FD denominator). Compare against the all-post-money base.
11. **Extension C — SAFE cleanup.** Assume the founder offers the pre-money SAFE holder (SAFE 1 in extension B) an amendment: convert to post-money at a cap adjusted from $5M to $4M (a benefit to the SAFE holder equivalent to a modest cap reduction). Model the amendment, then re-run the pro-forma. Compare against extension B (mixed) and against the base case (all post-money).
12. **Reconciliation memo (2 pages).** Written to the founder and the lead investor's counsel. Contents:
    - The pro-forma bottom line: founder-percent, new-investor-percent, pool-percent, aggregate-SAFE-percent, note-percent.
    - The reconciliation to term sheet.
    - The sensitivity read: which of the three levers (pre-money, pool size, SAFE overhang) is the biggest driver of the founder's outcome.
    - The dollar cost of the MFN cascade (extension A).
    - The dollar cost of the mixed stack (extension B) vs. the SAFE cleanup (extension C).
    - Any recommended term-sheet changes based on the sensitivity read.

## Starter guidance

- **Turn on iterative calculation** in Excel or Google Sheets and set the maximum iterations high (100+) with a small convergence threshold. The circular references are essential to the solve; do not try to break them with algebraic substitution unless you're comfortable with the closed-form derivation (which does exist — see chapter 4).
- **Verify the post-money identity for every SAFE.** `investment / cap` should equal the SAFE's percentage of pre-new-money post-conversion FD, to within rounding. If it doesn't, the denominator in your SAFE-price formula is wrong.
- **Accrue the note interest carefully.** Actual day-count from signing to closing, at 6% simple. A small dollar error here becomes a small share-count error, which is worth catching before the reconciliation.
- **The pool top-up requires its own convergence step.** The pool sits inside the pre-new-money base that the priced-round-and-SAFE math depends on; the pool's target size depends on the post-money valuation, which depends on the base. Iterate.
- **For the pre-money SAFE in extension B**, use the closed-form solution from chapter 2 for a single pre-money SAFE in an otherwise-post-money stack. The math is: the pre-money SAFE's shares depend on the shared pre-money FD denominator, which includes everything else (post-money SAFE shares, note shares, pool). Solve as one more equation in the iterative system.
- **For the SAFE cleanup in extension C**, the amendment converts the pre-money SAFE at the current pre-money FD moment. The post-conversion "post-money cap" is set so that the SAFE holder's shares are the same as they would have been under the pre-money mechanic converting today at the current denominator. Then the SAFE holder is "post-money" going forward, and any future dilution comes out of the founder only.
- **The founder-dilution walk should sum to the correct final founder percentage.** Confirm: starting founder-percent (88.89%) minus sum of dilution-events equals ending founder-percent (32.40% in the base case).

## Acceptance criteria

- **The pro-forma matches chapter 4's worked-example numbers** to within 0.1 percentage points (differences beyond that indicate a modelling error worth debugging).
- **Each SAFE's post-money identity holds** in the base case.
- **The iterative solver converges** to a stable answer within 20 iterations.
- **The term-sheet reconciliation shows no deltas over 0.5 percentage points** without a documented explanation for each.
- **The founder-dilution walk sums correctly** and attributes each event's specific dilution.
- **The sensitivity block populates cleanly** and shows monotonic behaviour: higher pre-money reduces founder dilution; lower pool reduces founder dilution.
- **Extension A quantifies the MFN cost** in percentage points and in dollars at the $40M post-money valuation.
- **Extension B correctly models the mixed stack** with pre-money and post-money mechanics both firing in the same solve.
- **Extension C's cleanup amendment leaves the SAFE holder economically indifferent** to the switch (per the design of the amendment), and produces the same founder outcome as the all-post-money base case (post-cleanup, the founder is in the same position as if the SAFE had been post-money all along, subject to the cap reduction offered as consideration).
- **The reconciliation memo makes a specific term-sheet recommendation** based on the sensitivity read.

## Deliverables

- The workbook with all 11 tabs / sections.
- The two-page reconciliation memo (Markdown or PDF, or as a memo tab).

## Extensions (optional)

- Add a **second lead investor** to the Series A (a co-lead) with a $3M cheque at the same terms. Model the two-lead pro-forma; the two leads share the 25% ownership target proportionally.
- Add **pro-rata rights side letters** to three of the five SAFEs and model the pro-rata cheques the SAFE holders would write at the Series A. Show how the pro-rata rights absorb allocation from the new lead's target.
- Model a **second priced round (Series B)** at $30M raised on $150M pre / $180M post 24 months later, and show how the Series-A preferred and the founder are re-diluted. This is largely covered in [`mod-108`](../../mod-108-term-sheets-and-preferred-stock-economics/), but the mechanic previewed here.
- Run the **post-money pool placement scenario** on the base case (chapter 2 of mod-104), quantify the founder-percent difference from the pre-money default, and produce the "post-money pool ask" red-line the founder would send to the term sheet.
