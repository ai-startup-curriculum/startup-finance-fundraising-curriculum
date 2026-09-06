# Exercise 03 — Anti-Dilution Recalculation Drill

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 4 (the three formulae, pay-to-play, worked example). Uses cap-table mechanics from [`mod-104`](../../mod-104-cap-tables-and-equity-compensation/) chapter 1.

## Problem statement

Recalculate the Series-A preferred conversion price after a defined Series-B down round under all three anti-dilution formulae — broad-based weighted-average, narrow-based weighted-average, and full ratchet. Quantify the incremental common dilution in each case. Then model a soft pay-to-play modifier that carves out non-participating Series-A holders from the anti-dilution kick, and quantify the cap-table shift when a subset of Series-A holders participates in the down round pro-rata and a subset does not. Author the pay-to-play memo the CFO writes to the CEO before signing the down-round term sheet.

The exercise trains the specific arithmetic of the three formulae plus the pay-to-play interaction. It is the second-most-consequential clause in the charter (after liquidation preference), and it fires without a shareholder vote at the trigger event — so the negotiation to get it right happens at the *original* term-sheet stage, not the down-round stage.

## Scenario — the pre-down-round state

Use this specific cap table as the starting state. The scenario is a Series-A-funded company facing a Series-B down round 20 months after Series-A close.

**Series-A close (the starting state).**

- Common: 8,000,000 shares (founders + early employees).
- Options granted: 1,500,000 shares.
- Unissued option pool: 500,000 shares.
- Series A Preferred: 2,000,000 shares. Raised $10,000,000 at $5.00 per share. 1x non-participating.
- Broad-based fully-diluted (BB-FD) at Series-A close: 12,000,000 shares. Narrow-based FD (excluding options and unissued pool): 10,000,000 shares. Series-A original conversion price: $5.00.
- Series-A investor composition: five investors, each with a specific stake.
  - Lead A (Series-A lead): $6,000,000 (1,200,000 shares, 60% of round).
  - Follower A1: $1,500,000 (300,000 shares, 15%).
  - Follower A2: $1,000,000 (200,000 shares, 10%).
  - Follower A3: $1,000,000 (200,000 shares, 10%).
  - Follower A4: $500,000 (100,000 shares, 5%).

**Series-B down round (the trigger event).**

- Series B raises $8,000,000 at $2.50 per share (3,200,000 shares issued).
- Series B post-money: 8,000,000 common + 2,000,000 Series A + 2,000,000 options + 3,200,000 Series B = 15,200,000 shares (before any anti-dilution kick and before any pool top-up). Series-B post-money valuation: $38,000,000. Series-A original post-money was $50,000,000 → this is a genuine down round on a per-share basis ($5.00 to $2.50) and in the aggregate.
- Ignore any Series-B pool top-up for the base case (chapter 4's worked example did the same); model it as an extension.

## Requirements

Produce a workbook (four tabs) plus the pay-to-play memo.

1. **Setup tab.** The base cap table, the Series-A investor composition, the Series-B down-round parameters, and the three anti-dilution formulae parameterised as inputs.

2. **Formula-comparison tab.** For each of the three formulae, compute:
   - The new Series-A conversion price (NCP) using the chapter-4 formulae. Show the arithmetic explicitly — plug OS, IS, and DS for each formula variant.
   - The Series-A per-share conversion ratio (OCP / NCP).
   - The total additional Series-A common shares issued on conversion.
   - The post-conversion pro-forma cap table with per-line share counts and per-line percentages.
   - The founder / common dilution attributable to the anti-dilution kick — separated from the base Series-B dilution.
   - Reconciliation: pre-anti-dilution FD + Series-A additional shares = post-anti-dilution FD.

3. **Pay-to-play tab.** Model a soft pay-to-play modifier (loss of anti-dilution only for non-participating Series-A holders). Assume:
   - Lead A invests its full pro-rata in the down round ($1,264,000 based on a 15.79% Series-A pro-rata of the $8M raise — verify the specific pro-rata calculation using the FD-total denominator).
   - Followers A1 and A2 invest their pro-rata ($158,000 and $105,000 respectively).
   - Follower A3 declines to participate.
   - Follower A4 declines to participate.
   Under the soft pay-to-play:
   - Participating holders receive the broad-based weighted-average anti-dilution kick on their existing Series-A shares.
   - Non-participating holders receive no anti-dilution kick — their existing Series-A conversion price stays at $5.00.
   Compute the shares each specific Series-A holder converts into post-Series-B; reconcile the totals.

4. **Founder-cost tab.** For each of the three base formulae and for the pay-to-play scenario, compute:
   - The founder's ownership percentage pre-Series-B, post-Series-B-before-anti-dilution, and post-Series-B-after-anti-dilution.
   - The incremental dilution attributable to the anti-dilution kick.
   - The dollar cost to the founding team (two founders holding 4,000,000 shares each) at a hypothetical $150M exit under structure A of exercise 02 (1x non-participating, no dividend, pari passu).
   Present as a table with rows: pre-Series-B, post-Series-B no-AD, post-Series-B BB-WA, post-Series-B NB-WA, post-Series-B full ratchet, post-Series-B pay-to-play. Columns: founder %, incremental dilution pp, $ cost at $150M exit.

5. **Pay-to-play memo** (`pay-to-play-memo.md`, 2 pages). Written to the CEO and the board before the Series-B term sheet is signed. Structure:
   - **Bottom-line summary.** One paragraph: "Under the received Series-B term sheet's anti-dilution provision and its pay-to-play modifier, the founder-team's ownership falls from X% to Y% and their dollar outcome at a hypothetical $150M exit falls from $A to $B. Of that decline, Z pp / $C is attributable to the base Series-B round; W pp / $D is attributable to the anti-dilution kick; V pp / $E is attributable to the pay-to-play carve-out on non-participating holders."
   - **The three formulae, side by side.** One paragraph per formula: what the term sheet says today (assume the *original* Series-A charter specified broad-based weighted-average — the market-standard), what the consequence is, and what a hypothetical stronger anti-dilution formula would have cost the founder additionally.
   - **The pay-to-play design choice.** Two options: (a) hard pay-to-play (non-participating Series-A holders' preferred converts to common at exit, or loses preference plus AD); (b) soft pay-to-play (loss of AD only). Recommend one; justify with the specific cap-table impact from the workbook.
   - **The lead-investor negotiation.** The specific counter-language you would send back on the Series-B term sheet. Include the market-conditions data (Carta down-round data if cited; `<!-- needs-research -->` otherwise).
   - **What the CFO wants to remember.** One sentence for the future-Series-C conversation: "The Series-B anti-dilution provision, as amended, is [X]. Next time we take an anti-dilution kick, the specific parameter to negotiate is [Y]."

## Starter guidance

- **Plug the formulae, don't back-solve.** Chapter 4's arithmetic is direct — plug OS, IS, and DS into the formula for each variant and read off NCP. Don't try to derive NCP from a post-round cap-table target; that inverts the causality.
- **Watch the BB vs. NB definition.** The definition of "outstanding shares" in the denominator is the specific thing that varies between broad-based and narrow-based. Chapter 4's OS definitions are the source of truth for this exercise; use them consistently across the formula-comparison tab.
- **Full ratchet is a special case, not a formula variant.** Under full ratchet, NCP = down-round price with no weighting. Don't try to force it into the weighted-average formula's shape.
- **Pay-to-play splits the cap table.** Under the pay-to-play modifier, different Series-A holders convert at different prices — participating holders at the new (lower) NCP, non-participating holders at the original $5.00. The pay-to-play tab must track each investor's shares separately, not aggregate them.
- **Confirm the pro-rata denominator.** The Series-A pro-rata of the Series-B $8M raise is `(Series-A FD share) × $8M`. The Series-A FD share is `2,000,000 / 12,000,000` = 16.67%, so aggregate Series-A pro-rata is $1,333,333. Each specific investor's pro-rata is their share of that aggregate. The scenario's numbers assume investors participate pro-rata to their Series-A stake, so verify the aggregate reconciles.
- **The founder-cost tab is where the exercise pays off.** The percentage-point dilution is real but abstract; the $-at-$150M-exit is the number a founder will actually feel. Do not skip that column.

## Acceptance criteria

- **The three formula variants produce the chapter-4 numbers.** BB-WA NCP ≈ $4.375, NB-WA NCP ≈ $4.286, full-ratchet NCP = $2.50. If your numbers differ, debug the OS / IS / DS inputs.
- **The pro-forma cap table reconciles at each variant** — pre-shares + additional-shares = post-shares.
- **The pay-to-play tab tracks each Series-A investor's shares separately** — Lead A and Followers A1, A2 receive the BB-WA kick; Followers A3, A4 do not.
- **The founder-cost tab compares all five scenarios** (no-AD, BB-WA, NB-WA, full-ratchet, pay-to-play) with founder %, incremental dilution, and $ at $150M exit.
- **The memo makes a specific pay-to-play design recommendation** — hard or soft — with justification from the workbook.
- **The counter-language is specific.** Not "push back on anti-dilution"; the specific parameter (OS definition, ratchet vs. weighted-average, pay-to-play threshold, hard vs. soft) that the counter changes.
- **Market data cited or flagged.** Fenwick / WSGR / Carta on anti-dilution formula frequency at Series-B down rounds — cited to a specific vintage or flagged `<!-- needs-research: ... -->`.

## Deliverables

- The workbook (`.xlsx` or Google Sheets link) with tabs: setup, formula-comparison, pay-to-play, founder-cost.
- The pay-to-play memo (`pay-to-play-memo.md`).

## Extensions (optional)

- **Add a hard pay-to-play variant.** Non-participating Series-A holders' preferred converts to common. Remodel the cap table and quantify the specific-investor consequences: which Series-A holders lose preference and voting rights.
- **Add a pool top-up.** The Series-B lead requires a top-up of the pool to 10% post-close. Remodel the pool-top-up interaction with the anti-dilution kick. Which happens first — pool top-up dilutes Series-A on a per-share basis, which affects the OS denominator for the AD formula? Or does the AD kick apply to a pre-pool-top-up OS? Document the drafting assumption you make and its cap-table consequence.
- **Model a two-tranche Series-A.** Assume the original Series-A was in two tranches (A-1 and A-2) issued at different times and different prices ($5.00 and $6.00). Recompute the BB-WA under the Series-B down round for each tranche separately.
- **Chain multiple down rounds.** After the Series-B, a Series-C prices at $2.00 per share (another down round). Recompute the Series-A NCP through both down rounds (does BB-WA apply cumulatively or does the Series-B pay-to-play carve-out apply to the Series-C event too?). This is the specific drafting question the CFO must answer before signing the Series-B pay-to-play.
- **Compare against a "no anti-dilution" baseline.** Some seed-round convertibles have no anti-dilution. Compute the founder's outcome if the Series-A charter had had no AD provision at all — the "how bad is bad" reference.
