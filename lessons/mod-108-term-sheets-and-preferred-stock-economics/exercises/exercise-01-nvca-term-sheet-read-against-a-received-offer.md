# Exercise 01 — NVCA Term-Sheet Read Against a Received Offer

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 1 (the NVCA reference stack and the four-tier classification). Familiarity with chapters 2 (liquidation preferences), 4 (anti-dilution), 6 (protective provisions), and 7 (board composition) helps but is not required — the exercise trains the *reading discipline* and produces the memo output; the specific mechanics get their own dedicated drills in exercises 02-06.

## Problem statement

You are the CFO / fundraising lead of a Series-A-stage company. A lead investor has just delivered a term sheet. Read it against the NVCA model term sheet and Model Certificate of Incorporation, classify every material clause into the four tiers (market-standard / negotiated but market / aggressive / unusual), and produce the internal red-line memo the CEO and counsel will work from before you open negotiation.

The exercise trains the discipline of *reading a received document against a reference*, not the mechanics of any single clause. The output — the classification table and the priority-ask memo — is the artefact a real CFO produces in the first 48 hours after receiving an offer.

## Scenario — build your own received term sheet

Author the term sheet you will read against. Do not just copy the NVCA model — a copy would produce a trivial classification (every clause matches market). Instead, take the NVCA model term sheet as a base and edit it to include a plausible mix of clauses across the four tiers.

**Company context.**

- B2B SaaS or B2B fintech company, currently at $1.8M-$3.5M ARR, growing 6-10% MoM.
- Team of 20-35 across engineering, GTM, and G&A.
- Prior capital: one priced seed of $3M-$5M raised 18-24 months ago, some SAFEs from angels and an accelerator. Existing seed lead has one board seat and pro-rata rights.
- Raising Series A: target $12M-$20M new money on a pre-money valuation in the $30M-$60M range.
- Cap table pre-Series-A: founders own ~50-60%, employees ~10-15%, seed preferred ~15-20%, SAFEs / notes ~5-10%, pool ~5-10%.

Document the company context on a "context" tab or in a preamble to the term sheet. Anonymise if using a real company.

**Term-sheet construction.** Draft a full Series-A term sheet (2-4 pages, numbered clauses) covering — at minimum — the sections the NVCA model term sheet covers: security type and price, capitalisation (pre- and post-money), dividends, liquidation preference (multiple, participation, seniority), voting rights, protective provisions, mandatory conversion, anti-dilution, redemption, drag-along, pro-rata / preemptive rights, ROFR / co-sale, information rights, registration rights, board composition, employee vesting acceleration, D&O insurance, no-shop, expenses, conditions to close, confidentiality. Include:

- **At least 4 tier-1 clauses** — parameters at the current-market default. Examples: 1x non-participating preferred; broad-based weighted-average anti-dilution; 20-30-day no-shop; standard registration rights; MRL for VCOC funds.
- **At least 3 tier-2 clauses** — inside the market envelope but with parameters up for negotiation. Examples: board composition (three seats vs. five); protective-provisions list length (12 items vs. 18); pro-rata rights extended only to Major Investors above a specific threshold; mandatory-conversion price multiple; dividend rate at 0% vs. 6% non-cumulative.
- **At least 2 tier-3 (aggressive) clauses.** Examples: 1x participating preferred (capped or uncapped); narrow-based weighted-average anti-dilution; a protective-provisions list of 22+ items with operating-decision items included; a majority-of-preferred-only drag; a cumulative dividend; a specific-series (not combined) class vote on protective provisions.
- **At least 1 tier-4 (unusual) clause.** Examples: full ratchet anti-dilution; short-fuse mandatory redemption (3-5 years, unqualified); a "loss of protective vote on sitting out a round" clause; a drag-along at 50% of preferred with no common vote; a 2x or 3x preference multiple.

Blend these across the term sheet so that the mix looks like something an actual lead investor's counsel might have drafted — not a caricature. Real received term sheets are usually about 70% tier-1, 20% tier-2, 8% tier-3, 2% tier-4. Do not make the term sheet a stack of tier-4 clauses; make it realistic.

Save the drafted term sheet as `received-term-sheet.md` in your submission directory.

## Requirements

Produce four deliverables in a submission directory.

1. **The received term sheet** (`received-term-sheet.md`) — the artefact you authored above.

2. **The clause-by-clause classification table** (`classification-table.md` or a spreadsheet). One row per material term-sheet clause. Columns:
   - **#** — the term-sheet clause number and title.
   - **Received language** — a compact quote or summary of the received clause (parameter values are what matter, not full text).
   - **NVCA-model default** — the corresponding NVCA-model position in one line.
   - **Classification** — tier 1 (market) / tier 2 (negotiated) / tier 3 (aggressive) / tier 4 (unusual). Justify the classification with a one-line rationale referencing the specific parameter that drives the tier.
   - **Current-quarter market read** — a one-line note on the current-quarter incidence of the received parameter across Fenwick / WSGR / Carta (cite a specific report and vintage, or mark `<!-- needs-research: ... -->` if the number is not sourced).
   - **Proposed counter-language** — the specific red-line you would ask for. Concrete, not "push back."
   - **Negotiation priority** — P1 (must-have) / P2 (strong preference) / P3 (worth surfacing but concede if needed). Justify.

3. **The internal red-line memo** (`red-line-memo.md`, 2-3 pages). Structure per chapter 1:
   - **Bottom-line summary** — one paragraph. Total classification (how many clauses in each tier), the three-to-five negotiation asks, the overall temperature of the term sheet ("close to market with three specific fights," "aggressive across multiple axes and requires wholesale re-negotiation," etc.).
   - **The three-to-five P1 asks.** For each: the received-clause parameter, why it is aggressive or unusual, the counter, the specific market data that anchors the counter, the fallback position if the lead resists.
   - **The concessions.** The specific tier-2 or tier-3 clauses you will *accept as-is* to signal seriousness and to build negotiation capital for the P1 asks. This is the load-bearing discipline of chapter 1: not every clause gets red-lined.
   - **The market-conditions context** — one paragraph anchoring the overall negotiation posture in the current-quarter Fenwick / WSGR / Carta reading (cite the specific vintage of each source or mark `<!-- needs-research -->` if unavailable).
   - **Open questions for counsel.** Items where you need company counsel's legal read before setting the negotiation position (e.g., "is a floor on the drag price enforceable in Delaware?").

4. **The counsel-facing red-line** (`counsel-red-line.md`). A separate document written *to* company counsel. Two sections:
   - **Term-sheet clauses to red-line.** The specific proposed counter-language (from the classification table) grouped by NVCA-document destination (term sheet only vs. term-sheet-and-charter vs. IRA vs. Voting Agreement vs. ROFR-Co-Sale).
   - **Definitive-document watch items.** Clauses where the term-sheet language is accepted but the charter / IRA drafting has to reflect a specific parameter (e.g., "term sheet says 'weighted-average anti-dilution' — the charter must implement broad-based, not narrow-based").

## Starter guidance

- **Read the NVCA model term sheet first**, before you start drafting the received one. You cannot classify against a reference you have not read. Open the NVCA model term sheet and Model Certificate of Incorporation side-by-side and treat them as the base.
- **Use chapter 1's four-tier framework as the check.** For every clause you draft into the received term sheet, decide first *which tier* you are placing it in, then draft the parameter values that put it there. This gives you the classification "answer key" as you go.
- **Do not stack every aggressive clause on top of another.** Real term sheets are heterogeneous — a lead may push hard on liquidation preference but leave board and anti-dilution at market. If your term sheet is uniformly tier-3, the exercise loses its texture and the memo becomes trivial.
- **Cite specific market data or mark `needs-research`.** For every tier classification and every counter, the exercise expects a specific citation to Fenwick, WSGR, Carta, or Cooley GO — with the report year — or a `<!-- needs-research: ... -->` marker describing what should be verified. Do not fabricate percentages.
- **Keep the memo short.** The chapter-1 discipline is that a good red-line memo is 2-3 pages, not 8. If you can't fit the three-to-five asks and the market context in 3 pages, you have not compressed the read enough.
- **Concede visibly.** The counsel-facing red-line document should *not* red-line every clause you have concerns about. The negotiation-signalling point of chapter 1 is that the CFO who reds-line everything looks inexperienced. Pick your three-to-five and concede on the rest.

## Acceptance criteria

- **The received term sheet is realistic.** It covers all the NVCA-model term-sheet sections. It has a plausible mix of tier-1 through tier-4 clauses (not uniformly aggressive; not uniformly market). Parameter values are internally consistent (e.g., the pre-money and post-money reconcile with the raise and the share price).
- **The classification table has one row per material clause** — at minimum 15-20 rows covering the standard term-sheet sections. Every row has a classification, a one-line rationale, and a proposed counter.
- **The classification is defensible against the NVCA reference.** Tier-1 clauses match the NVCA-model default. Tier-3 or tier-4 assignments quote the specific deviation.
- **The red-line memo lists three-to-five P1 asks** — not fewer, not more. Each ask has a counter, a market-data anchor (or `needs-research`), and a fallback.
- **The memo names visible concessions.** At least one tier-2 or tier-3 clause is explicitly listed as "accept as-is" with a reason.
- **The current-quarter market context is cited to specific sources** with vintages named, or explicitly flagged with `<!-- needs-research: ... -->`.
- **The counsel-facing red-line separates term-sheet-level changes from definitive-document watch items.** No hand-waving of "counsel will handle it"; the CFO's red-line points to specific NVCA-document destinations.
- **No fabricated market statistics.** Every quantitative claim traces to a real source (with vintage) or is flagged `needs-research`.

## Deliverables

- `received-term-sheet.md` — the drafted received term sheet.
- `classification-table.md` (or `.xlsx`) — the clause-by-clause classification table.
- `red-line-memo.md` — the internal 2-3 page memo to CEO and counsel.
- `counsel-red-line.md` — the counsel-facing document with red-line asks and definitive-document watch items.

## Extensions (optional)

- **Rewrite the term sheet as the lead's counter.** After the CEO signs off on the counter-memo, produce the version of the term sheet that would come back from the lead after one negotiation round (accepting some, rejecting some, splitting the difference on others). Update the classification table and the priority-ask memo. Preview of exercise 08.
- **Add a second lead's competing term sheet.** Draft a second, meaningfully-different term sheet from a hypothetical second bidder. Run the same classification against both. Produce a comparison memo that reads which term sheet is genuinely more founder-favourable *after* accounting for the classification, not just on the headline pre-money.
- **Model the founder-outcome delta.** For the two-to-three highest-priority tier-3 asks (e.g., participating vs. non-participating), quantify the dollar delta to the founder's exit proceeds across three exit-price scenarios (1x, 3x, 10x the post-money). Preview of exercise 02.
- **Convert the classification to a fund-facing memo.** Write the same read from the lead investor's side — how the lead would defend the tier-3 clauses to the CEO in the negotiation. Trains the two-sided reading that produces better counters.
