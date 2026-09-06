# Exercise 05 — Protective-Provisions Negotiation Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 6 (the NVCA-standard list, the veto-heavy overreach patterns, the class-vote drafting parameters).

## Problem statement

Receive a term sheet with a 22-item protective-provisions list. Classify each item against the NVCA-standard cluster (chapter 6). Red-line the list down to a defensible market position. Author the counter-memo the CFO sends back with the specific items to strip, the items to move from class-vote to board-approval, and the items to accept as-is.

The exercise trains the specific reading discipline of the protective-provisions clause — the clause whose drafting parameters most often push a Series-A term sheet from "market-standard" into "investor operational control" without the founder noticing. A CFO who cannot classify a 22-item list against the NVCA-standard ~10-14-item cluster is a CFO who accepts every item on the list.

## Scenario — the received list

The term sheet on the table includes the following protective-provisions list. All items require the affirmative consent of a majority of the Series-A preferred (voting as a separate class) before the company may take the action.

1. Amend, alter, or repeal any provision of the Certificate of Incorporation or Bylaws.
2. Liquidate, dissolve, or wind up the affairs of the Corporation.
3. Effect any Deemed Liquidation Event (merger, sale, or similar transaction).
4. Reclassify or amend any existing security in a way that senior-ranks it.
5. Create, authorise, or issue any new class or series of stock ranking senior to or pari passu with the Series A Preferred.
6. Increase or decrease the authorised number of shares of Preferred Stock or of any series.
7. Redeem, repurchase, or otherwise acquire shares of the Corporation.
8. Pay or declare any dividend or distribution.
9. Incur indebtedness in excess of $250,000 in the aggregate at any time.
10. Enter into any related-party transaction.
11. Change the size or composition of the Board of Directors.
12. Approve the annual operating budget or business plan, or any material amendment thereto.
13. Approve any hire or termination of any employee at or above the level of Director or with a base salary above $180,000.
14. Approve any capital expenditure or non-recurring commitment exceeding $150,000.
15. Approve or amend the Equity Incentive Plan; approve any individual equity grant above 25,000 shares.
16. Approve, form, or dispose of any subsidiary or joint venture; enter or exit any material line of business.
17. Approve any lease or commitment for real property above $50,000 per year.
18. Approve any new debt facility, credit line, or refinancing regardless of amount.
19. Approve any customer contract with a term exceeding 24 months or a contract value exceeding $500,000.
20. Approve any acquisition or investment by the Company.
21. Approve any change in the CEO, CFO, or CTO — appointment or termination.
22. Approve any action outside the ordinary course of business.

**Additional drafting parameters in the received term sheet.**

- Class vote is a separate Series-A class vote (not combined with other series if additional series exist).
- Threshold: majority of Series-A.
- The list applies without qualification — no "except for actions in the ordinary course," no dollar-threshold escalators as ARR grows, no sunset provisions.
- The list applies at both the board level (director must vote for) and the company level (class vote of preferred is required in addition).

## Requirements

Produce three deliverables.

1. **Classification table** (`protective-provisions-classification.md` or spreadsheet). One row per item (22 rows). Columns:
   - **#** — item number.
   - **Received language** — a compact summary of the item.
   - **NVCA-standard cluster match** — which of the NVCA-standard categories (corporate-existence, class-related, financial, optional-tier-2) the item corresponds to, or "not in NVCA-standard cluster" if it doesn't.
   - **Chapter-6 classification** — tier 1 (market) / tier 2 (negotiated) / tier 3 (aggressive) / tier 4 (unusual).
   - **Rationale** — one line: why this tier. Reference the specific parameter (dollar threshold, class-vote scope, drafting scope) that drives the tier.
   - **Recommended action** — one of: (a) accept as-is; (b) accept with a specific parameter change (e.g., "raise dollar threshold to $2M"); (c) move from class-vote to board-approval; (d) strip entirely.
   - **Counter-language** — the specific red-line, in the words that would go back to counsel. Not "push back" — concrete language.

2. **Counter-memo** (`counter-memo.md`, 2 pages). Written to counsel and — as the internal-alignment memo — to the CEO. Structure:
   - **Bottom-line summary.** One paragraph: "The received list has 22 items. Twelve match the NVCA-standard cluster and are tier-1 or tier-2 accept-with-modification. Ten items push into tier-3 or tier-4 operational-control territory and require specific counters: five to strip, four to move to board-approval, one to accept with a materially raised threshold."
   - **The strip list.** Five items (or however many you land on): item number, the specific reason to strip, the anticipated lead-investor pushback and your response.
   - **The move-to-board list.** Four items (or however many): why board-approval is the appropriate governance level rather than class-vote, the board-composition dependency (this ties to exercise 06 and chapter 7).
   - **The accept-with-modification list.** The tier-1 and tier-2 items with specific parameter changes — dollar thresholds raised, "ordinary course" carve-outs added, sunset triggers introduced.
   - **The class-vote-scope ask.** A separate section on the drafting parameter (single-series vs. combined-preferred; majority vs. supermajority). Recommend a specific position and justify.
   - **The current-quarter market anchor.** One paragraph citing Fenwick / WSGR / Carta on protective-provisions list length and specific-item incidence at Series-A. Cite specific vintages or flag `<!-- needs-research: ... -->`.

3. **Counsel-facing red-line** (`counsel-red-line.md`, half page). A compact document listing the exact language changes to send back on the term sheet. Not the memo; the diff. Group by NVCA-document destination — items that change the term-sheet language, items that will need to be reflected in the Amended and Restated Certificate of Incorporation, items that belong in the Voting Agreement or IRA.

## Starter guidance

- **Open the NVCA Model Certificate of Incorporation and the model term sheet before starting.** The NVCA-standard protective-provisions list is the reference. Every classification must be defensible against that list.
- **Use the chapter-6 four-tier framework as the scaffold.** Corporate-existence and structural actions are almost always tier-1. Class-related actions are tier-1. Financial-scale actions (debt, dividends, redemption) are tier-1 or tier-2 depending on threshold. Operational-decision items (budget, hires, contracts, capex, IP) are tier-3 or tier-4.
- **Do not blindly strip everything that is not NVCA-standard.** Some tier-2 or tier-3 items are legitimately negotiated by an experienced lead; the counter should raise thresholds, add ordinary-course carve-outs, or move to board-approval — not always strip.
- **The board-approval alternative is the load-bearing counter.** For items that are legitimately governance-level decisions (annual budget, senior hires, subsidiaries, material contracts), the correct level is *board* approval, not *class* approval. A board with a founder-friendly composition (chapter 7 / exercise 06) can approve without going to a class vote. The CFO's counter should redirect the item, not strip it.
- **Watch the specific-series class-vote parameter.** The received term sheet's separate Series-A class vote is tier-3 at Series-A (see chapter 6). A combined-preferred class vote is the market-standard.
- **Cite market data.** Do not assert "22 items is aggressive" without pointing at the current-quarter Fenwick / WSGR / Carta data. If you cannot source the specific number, flag `<!-- needs-research: median protective-provisions list length at Series-A per Fenwick Q?/YYYY -->`.
- **Do not draft your own operating agreement.** The exercise is not to rewrite the class-vote scope from scratch; it is to red-line the specific list against the NVCA reference. Keep the counter-language concrete and short.

## Acceptance criteria

- **All 22 items are classified** into one of the four tiers with a defensible rationale.
- **The tier-1 items match the NVCA-standard cluster.** At minimum items 1-8 (corporate-existence and class-related and financial-scale) should be tier-1.
- **The tier-3 / tier-4 items are named specifically.** At minimum items 12-22 (operational-decision, CEO/CFO consent, ordinary-course catch-all) should be flagged tier-3 or tier-4. The rationale is that they cross from "protect the investment" into "control the operation."
- **The counter-memo lists at least five items to strip and at least three items to move to board-approval.** Fewer than that suggests the classification has been too lenient; the received list was constructed to include a mix of aggressive items.
- **The class-vote-scope ask is present** — the recommendation to change from separate Series-A vote to combined-preferred vote is a specific ask.
- **The counsel-facing red-line groups items by NVCA-document destination.** Term sheet vs. Certificate of Incorporation vs. Voting Agreement / IRA.
- **Market data anchoring is present** with citations or `<!-- needs-research -->` flags.
- **No fabricated statistics.** Every incidence claim traces to a source or is flagged.

## Deliverables

- `protective-provisions-classification.md` (or `.xlsx`) — the 22-row table.
- `counter-memo.md` — the 2-page counter-memo.
- `counsel-red-line.md` — the half-page red-line document.

## Extensions (optional)

- **Add a Series-B round layer.** Assume the company has already raised a Series-B (with its own protective-provisions list of 14 items — some overlap, some distinct from the Series-A list). Redraft the class-vote scope: how do the Series-A and Series-B protective provisions interact when both series have separate class-vote rights? Which items should be combined, which should stay series-specific? Preview of chapter 6's stacked-series dynamics.
- **Sunset provisions.** Draft specific sunset language for the tier-2 items you accept (e.g., "the dollar threshold for indebtedness scales to $2M per year of trailing revenue, cap at $10M"). This is a real drafting technique for founder-side protective-provisions negotiation.
- **The board-approval fallback structure.** Draft, in specific voting-agreement-adjacent language, the mechanic by which items moved from class-vote to board-approval interact with the board's own vote thresholds. Include the interaction with a founder-favourable board composition from chapter 7.
- **Model the CEO/CFO consent trap.** Item 21 is a specific tier-4 pattern. Assume it is retained by the lead. Model the specific consequence: what happens when the founder-CEO wants to hire a new CFO and the Series-A lead vetoes the appointment? Author the escalation path.
- **Convert to the lead's view.** Write the memo the lead investor would send its own investment committee defending the 22-item list. This trains the two-sided reading and produces better counters (chapter 1's discipline).
