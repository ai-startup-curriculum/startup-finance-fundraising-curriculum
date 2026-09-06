# Exercise 02 — Liquidation-Preference Waterfall Across Exit Scenarios

**Estimated time:** ~5 hours
**Prerequisites:** Chapters 2 (preference structures) and 3 (waterfall arithmetic). Uses cap-table mechanics from [`mod-104`](../../mod-104-cap-tables-and-equity-compensation/) chapters 1-2.

## Problem statement

Build the preferred-stock waterfall for a Series-A + Series-B stack across seven exit prices under four preference structures. Identify the crossover points at which the founder's outcome shifts between regimes. Produce a founder-facing memo that translates the arithmetic into the specific "which preference structure costs us how much at which exit range" reading the CEO and board need to see before signing a term sheet.

The point of the exercise is to install the waterfall arithmetic as an operational muscle: the CFO who cannot produce the seven-exit-price × four-structure table in an afternoon cannot defend a preference-structure position to the board. Chapter 3 walked the algorithm; this exercise applies it to a stack and forces the crossover-identification and founder-memo output that a real Series-A close would require.

## Scenario — the two-round stack

Use this specific cap table as the base. Do not vary these numbers except in the extensions.

**Post-Series-A close (24 months before the exit):**

- Common: 8,000,000 shares (founders + early employees + granted options treated as common for waterfall purposes at exit).
- Series A Preferred: 2,000,000 shares. Raised $10,000,000 at $5.00 per share. 1x preference. No dividend.
- Fully-diluted Series-A close: 10,000,000 shares. Series-A as-converted: 20%.

**Post-Series-B close (the current state at exit-decision time):**

- Common: 8,000,000 shares (unchanged; assume no additional grants for simplicity).
- Series A Preferred: 2,000,000 shares (unchanged).
- Series B Preferred: 3,000,000 shares. Raised $30,000,000 at $10.00 per share. 1x preference. No dividend.
- Fully-diluted at Series-B close: 13,000,000 shares. Series-A as-converted: 15.38%. Series-B as-converted: 23.08%. Common: 61.54%.

**Transaction expenses at exit.** Assume 3% of gross exit price for banker + legal + escrow (deducted from gross before waterfall).

**Exit prices to model.** Seven all-cash scenarios: $30M, $60M, $90M, $120M, $180M, $300M, $500M.

## Preference structures to model

For each of the four structures below, run the full waterfall at each of the seven exit prices. Model both classes (Series A and Series B) under the same structure — i.e., all four combinations of *seniority and participation* apply consistently across the stack.

**Structure A — clean 1x non-participating stack, pari passu.** Both classes are 1x non-participating. The two classes split the preference pool pari passu (proportionally to their aggregate preferences) if the exit falls within the "preference-controls" regime for either class. Each class independently elects preference vs. as-converted.

**Structure B — 1x non-participating stack, senior Series B.** Both classes are 1x non-participating. Series B is senior: Series B's preference is paid in full before any dollars flow to Series A. Series A is paid after Series B (if any preference dollars remain). Each class independently elects preference vs. as-converted.

**Structure C — 1x participating stack, pari passu (uncapped).** Both classes are 1x participating uncapped. Preferences are paid first (pari passu across classes), then residual is distributed to common *plus* Series A *plus* Series B on an as-converted basis.

**Structure D — 1x capped participating stack (3x cap), senior Series B.** Both classes are 1x participating with a 3x cap. Series B is senior. Series B receives preference first, then participates in the residual up to its 3x cap. Series A receives its preference from the remaining preference pool, then participates in the residual after Series B, up to its 3x cap. Each class also has the "convert to common" option and elects the greater of (preference + participation up to cap) or (as-converted).

## Requirements

Produce a workbook (five tabs) plus a founder-facing memo.

1. **Setup tab.** The base cap table, the four preference structures documented, the seven exit prices, and the 3% transaction-expense assumption. Make each cell a labelled input.

2. **Structure-A waterfall tab.** For each of the seven exit prices, compute:
   - Net exit proceeds (gross − 3% expenses).
   - Preference vs. as-converted election for each class.
   - Preference pool distribution.
   - Residual to common.
   - Per-line dollars: Series A, Series B, Common (aggregate and per-share).
   - The regime label: "preference dominates" or "convert dominates" for each class.
   Reconcile: the sum of per-line dollars must equal net exit proceeds exactly at each exit.

3. **Structure-B waterfall tab.** Same as A but with senior Series B. The preference-pool distribution mechanic differs; document the mechanic in a note on the tab.

4. **Structure-C waterfall tab.** Same as A but with 1x participating uncapped. Both classes get preference *and* participation. Document that there is no election (both classes always get both).

5. **Structure-D waterfall tab.** Same as B but with 1x capped participating at 3x cap. Model the "convert to common instead of taking capped participation" election explicitly at each exit price for each class.

6. **Crossover tab.** For each structure and each class, compute algebraically the exit prices at which:
   - The class's preference-vs.-as-converted election flips (non-participating classes).
   - The class's cap starts to bind (structure D).
   - The class's convert-to-common election dominates its capped-participation take (structure D).
   - Across structures, the founder's per-share outcome equalises (e.g., the exit price at which the founder is indifferent between structures A and C).
   Show the arithmetic; do not just report the crossover numbers.

7. **Comparison chart / table.** A single view — either a chart with exit price on the x-axis and per-common-share dollars on the y-axis, four lines (one per structure); or a table with structures across the top and exit prices down the side — showing the founder's per-share outcome across the seven exits and four structures. Identify the exit-price ranges where the four structures diverge most and least.

8. **Founder-facing memo** (`waterfall-memo.md`, 2 pages). Written to the CEO and the founding-team common holders. Structure:
   - **Bottom-line summary.** One paragraph: "Under structure A, at exits between $60M and $300M, the founder receives $X-$Y per common share. Under structure C, the founder receives $Z per share at the same exit range — a cost of $A-$B per share, or $M-$N million across the founding team." Use round numbers pulled directly from the workbook.
   - **The four structures, side-by-side.** One paragraph per structure summarising when it wins for the preferred, when it costs the common, and the specific exit-price range where the cost is largest.
   - **The "exit above post-money but common gets little" trap.** Use the workbook to show the specific structure and exit-price at which the exit is above the Series-B post-money ($130M) but the common's take is below intuition. This is the specific chapter-3 point.
   - **The mid-band vs. unicorn asymmetry.** Show the specific data point from the workbook: at what exit price does the participating penalty stop being a significant fraction of the founder's take?
   - **The recommendation.** One sentence: "For this cap table and the exit-scenario probability distribution we assume, the CFO recommends [structure X] and would accept [structure Y] as a fallback."

## Starter guidance

- **Build the algorithm once, apply it four times.** The waterfall algorithm from chapter 3 is the same across the four structures — what varies is the preference-pool computation, the participation mechanic, and the cap application. Structure the workbook so that a single formula bank drives all four tabs; only the parameter block varies. This makes debugging tractable and prevents copy-paste errors across tabs.
- **Verify per-exit reconciliation before moving on.** At each exit price on each tab, sum the per-line dollars and confirm they equal net exit proceeds to the cent. Any discrepancy is a bug.
- **Work the crossover algebraically first, verify numerically.** For structure A, the Series-A preference-vs-AC crossover is where `$10M preference = 15.38% × (Net exit)`, i.e., Net exit = $65M, or gross exit = $65M / 0.97 = $67M. Compute the algebraic crossover before extracting it from the numerical table.
- **Structure B's senior Series-B matters most at mid-band.** At a $50M exit, Series B takes $30M preference, Series A gets $10M preference (if it takes preference — check the election), common gets the residual. Under structure A pari-passu, both preferences would have shared the pool proportionally. Show the specific difference on the tab.
- **Structure D is the algorithmically hardest.** The cap interacts with the convert-to-common election in a non-monotonic way. Test with several exit prices and confirm the algorithm's decisions are correct before running the seven-scenario grid.
- **Do not simplify away transaction expenses.** They shift the crossover points meaningfully at mid-band exits and are a real feature of the arithmetic.

## Acceptance criteria

- **All four tabs reconcile exactly at each of the seven exit prices** — per-line dollars sum to net exit proceeds.
- **Each non-participating class's election is correctly modelled** on structures A, B, and D. The election flips at the correct exit price (verified against the algebraic crossover).
- **Structure D's cap and convert-to-common election** are both correctly modelled. At high exits, at least one of the classes should be converting to common and taking its as-converted share.
- **The crossover tab identifies at least six specific crossover exit prices**: Series-A preference-vs-AC (structures A and B); Series-B preference-vs-AC (structures A and B); Series-A cap-binding (structure D); Series-A convert-to-common vs cap (structure D); Series-B cap-binding (structure D); founder-indifference between structures A and C (a specific exit price where the common's per-share is equal).
- **The comparison chart / table** shows the four structures at the seven exit prices with correct founder-per-share dollars.
- **The founder-facing memo** identifies the specific "exit above post-money but common gets little" data point from structure C or D and quantifies it in $/share.
- **The memo makes a specific structure recommendation** with a fallback.
- **No hand-waving on the arithmetic.** Every dollar in the memo traces to a cell in the workbook.

## Deliverables

- The workbook (`.xlsx` or Google Sheets link) with tabs: setup, waterfall-A, waterfall-B, waterfall-C, waterfall-D, crossover, comparison.
- The founder-facing memo (`waterfall-memo.md`).

## Extensions (optional)

- **Add a dividend accrual.** Change Series A's preference to include a 6% cumulative dividend accruing over the 24-month post-close period. Recompute the waterfall under structure C. Quantify the additional preference-pool dollars and the additional common-cost. Preview of chapter 8.
- **Add a founder-shares-only common line.** Split the common into founder-common (4,000,000 shares held by two founders) and employee-common (4,000,000 shares held by ~50 employees under vesting). Track the founders' aggregate dollar outcome across the four structures. Add a line to the memo on "founder-specific" cost.
- **Add an options / warrant tranche.** Introduce 500,000 unvested options at a $2.00 strike. Model exercise-and-participation at each exit price (participants exercise only if the per-share proceeds exceed the strike). Recompute the waterfall with the strike-adjusted dilution.
- **Model a stock-and-cash exit.** Change the $300M and $500M exits to 60% cash / 40% acquirer stock, with the acquirer stock trading at $50/share and a 12-month lock-up. Add a note to the memo on how the acquirer-stock lock-up interacts with the preferred stack's take.
- **Add a Series-C round.** Layer a hypothetical Series-C of $40M raised at $200M pre / $240M post (all senior to A and B) 12 months before the exit. Re-run structures A and D. Show how the three-round senior stack collapses the common's take at mid-band exits.
