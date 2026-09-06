# Exercise 07 — Fenwick / WSGR / Carta Quarterly Deal-Terms Read

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 9 (Fenwick, WSGR, Carta as the market-conditions reference). Complementary to [`mod-106`](../../mod-106-startup-valuation-frameworks/) exercise 05 (which reads the same sources for valuation; this exercise reads them for term-sheet features).

## Problem statement

Read the current-quarter Fenwick Silicon Valley Venture Survey, Wilson Sonsini Entrepreneurs Report, and the most recent Carta State of Private Markets (and any adjacent Carta liquidation-preference / deal-terms release) as the term-sheet-feature reference for a specific in-progress Series-A negotiation. Produce a market-conditions memo that anchors the negotiation posture on each of the eight major term-sheet clauses covered in chapters 2-8, cites the specific report vintage for every quantitative claim, and hands the CEO the specific data points that will be cited live in the term-sheet negotiation.

The exercise trains the specific research discipline that separates a defensible term-sheet negotiation from a hand-wavy one. Every clause classification in the earlier exercises assumed a "typical" market; this exercise makes the CFO do the current-quarter check and rebuild the classification in light of it.

## Scenario — the target negotiation

You are the CFO of a Series-A-stage company (numbers from exercise 01 or the mod-107 Series-A candidate profile). You have received a term sheet and are producing the market-conditions memo before opening negotiation. The memo will:

- Sit behind exercise 01's classification table as the current-quarter anchor.
- Be cited by the CEO in the negotiation-round conversations with the lead.
- Be re-read at Series-B (with a fresh vintage) as the anchor for that round's classification.

## Sources to read

Access the current-vintage published editions of:

- **Fenwick & West Silicon Valley Venture Survey** — [fenwick.com](https://www.fenwick.com/) → Insights → Publications. Read the most recent published quarter. If the specific report is behind a form-gate, note that in the memo.
- **Wilson Sonsini Entrepreneurs Report** — [wsgr.com](https://www.wsgr.com/) → Insights → Entrepreneurs Report (or the specific publication URL). Read the most recent published edition.
- **Carta State of Private Markets** — [carta.com/blog/state-of-private-markets/](https://carta.com/blog/state-of-private-markets/) or [carta.com/insights/](https://carta.com/insights/). Read the most recent published edition.
- **Any adjacent Carta releases** on liquidation preferences, participating-preferred incidence, or specific term-sheet features published in the last 6-12 months.

If any of these sources is not accessible for a current vintage at the time you author the exercise, use the most recent available and note the vintage explicitly in the memo. Do *not* substitute older data as if it were current-quarter — the discipline of naming the vintage is the load-bearing part of the exercise.

## Requirements

Produce three deliverables.

1. **The clause-by-clause market-read table** (`market-read-table.md` or spreadsheet). One row per major term-sheet clause. Columns:
   - **Clause** (e.g., "Liquidation preference — multiple", "Liquidation preference — participation", "Anti-dilution formula", "Board composition size", "Board composition — investor seats", "Protective-provisions list length", "Pro-rata Major Investor threshold", "Drag-along approval threshold", "Redemption rights presence", "Dividend rate and cumulation", "MFN presence").
   - **Fenwick current-quarter reading** — the specific published number (percentage incidence, median value, etc.) plus the specific quarter cited. E.g., "1x non-participating: 83% of Series-A financings; Fenwick Q?/YYYY."
   - **WSGR current-vintage reading** — the analogous number from the current WSGR report.
   - **Carta current-vintage reading** — the analogous number from Carta.
   - **Cross-source read** — one-line synthesis of the three numbers (do they agree? Which source is the most reliable for this specific clause and why?).
   - **Trailing 4-quarter trend** — direction (rising / flat / falling) with the specific data points cited if available.
   - **Implication for the target negotiation** — one line: does the current-quarter data support pushing on this clause? Softens the classification from tier-3 to tier-2? Hardens it? Or unchanged.

   At minimum cover: liquidation multiple, participation, seniority stacking, anti-dilution formula (BB-WA / NB-WA / full ratchet frequency), broad-based option-pool exclusions, pay-to-play frequency, protective-provisions list length, class-vote scope (single-series vs. combined), drag-along threshold, dividend rate and cumulation, redemption presence and terms, MFN presence, board composition (size, composition breakdown).

2. **The market-conditions memo** (`market-conditions-memo.md`, 2 pages). Written to the CEO and the board as the anchor for the term-sheet negotiation. Structure:
   - **Executive summary.** One paragraph: the current-quarter market environment (founder-favourable / neutral / stressed / investor-favourable) as read from the three sources, and the specific consequence for the term-sheet negotiation posture (are we pushing hard on preference and anti-dilution, or trading them for pre-money?).
   - **The seven-to-ten data points that will be cited in the negotiation.** For each: the specific number, the source and vintage, the specific clause it anchors, and the specific sentence the CEO or CFO can cite to the lead in a live conversation ("Fenwick's most recent quarter shows participating preferred at N% incidence at Series-A, which is Y percentage points below the trailing-4-quarter average; we see this deviation as investor-favourable relative to current market."). Do not fabricate specific numbers; either cite the actual current-quarter reading, or replace the number with `<!-- needs-research: specific figure from Fenwick Q?/YYYY -->`.
   - **The three clauses where the current-quarter data moves the classification.** From exercise 01's classification, name three specific clauses where the current-quarter reading changes the tier. E.g., "participating preferred was tier-3 aggressive in exercise 01's default classification; the current-quarter data softens it to tier-2 because incidence has risen materially in the stressed market — the posture should be to accept if the counter-lever is a higher pre-money."
   - **Trend narrative.** One paragraph on the trailing 4-quarter direction across the three sources.
   - **Watch items for the next vintage.** Two-to-three specific data points to re-read when the next quarter's reports drop, ahead of the next round.

3. **Sourcing methodology notes** (`sourcing-methodology.md`, half page). A short document naming:
   - The specific reports read (name, publisher, vintage, URL).
   - Any data cuts that were not available in the current vintage and flagged `<!-- needs-research -->`.
   - The methodology cross-check between the three sources — where they agree, where they diverge, and which source you defaulted to for a specific clause. This is the reproducibility artefact.

## Starter guidance

- **Read the three sources in order: Fenwick, WSGR, Carta.** Fenwick is the longest-running and most consistent methodology; use it as the base. Compare WSGR and Carta against Fenwick's numbers on the same clause. Divergences are informative; document them.
- **Cite specific quarters.** "Fenwick's most recent survey" is not enough — always name the specific quarter (Q?/YYYY) so the CEO can cite it and so the next-vintage read is reproducible.
- **Do not fabricate percentages.** The critical discipline of the exercise: if you cannot access a specific number from the current-vintage source, do not make one up. Flag `<!-- needs-research: specific figure X from Fenwick Q?/YYYY -->` and describe what should be looked up. Any fabricated percentage in the memo is a failure of the exercise.
- **Sample bias matters and should be noted.** Fenwick is Silicon Valley only; WSGR is national; Carta is skewed toward Carta-managed cap tables. When the three sources disagree, the sample-bias explanation is often the answer. Name it in the cross-source read.
- **The market environment overlay is the load-bearing summary.** A single sentence classifying the current quarter as founder-favourable / neutral / stressed / investor-favourable is what the CEO will act on. Justify with two-to-three specific data points.
- **The three-clauses-that-moved paragraph is where the exercise pays off.** The purpose of doing the market-read is to shift the negotiation posture on specific clauses. Name them.
- **Cross-reference exercise 01's classification.** If the classification in exercise 01 for a clause was tier-3, and the current-quarter data softens it to tier-2, say so explicitly. If the classification was tier-1 and the current-quarter data hardens it, say so.

## Acceptance criteria

- **The market-read table covers at least ten major term-sheet clauses** with all four data columns populated (Fenwick, WSGR, Carta, cross-source read) or explicitly `<!-- needs-research -->` where data is unavailable.
- **Every quantitative claim is cited to a specific report vintage** — quarter and year named. Uncited quantitative claims are a failure.
- **The memo names the current-quarter market environment** (founder-favourable / neutral / stressed / investor-favourable) with a two-to-three-point justification.
- **The memo lists seven-to-ten specific citable data points** with the specific sentence the CEO can use in the live negotiation.
- **The memo names three clauses where the market-conditions data moves the classification** from exercise 01's default. Each with a specific direction (softens / hardens / unchanged) and a specific new posture.
- **The trailing-4-quarter trend is named** in the trend paragraph, with data points where available.
- **The sourcing methodology notes name the specific reports read** and the specific unavailable data cuts.
- **The memo is 2 pages or less.** A longer memo signals the market read has not been compressed.

## Deliverables

- `market-read-table.md` (or `.xlsx`).
- `market-conditions-memo.md`.
- `sourcing-methodology.md`.

## Extensions (optional)

- **Compare current vintage against a two-year-old vintage.** Pull the same clause reads from a 2-years-earlier Fenwick / WSGR / Carta and compare. The direction of the two-year change is the specific "market drift" the CFO tracks. Add a section to the memo on the drift.
- **Compare with the cross-track valuation read.** For the same current quarter, also cite the specific pre-money medians from Fenwick / WSGR / Carta (per [`mod-106`](../../mod-106-startup-valuation-frameworks/) exercise 05). This ties the term-sheet-feature environment to the valuation environment.
- **Add PitchBook and CB Insights data.** These platforms publish adjacent term-sheet-feature data on subscription. If accessible, add a fourth column to the table with PitchBook / CB Insights numbers.
- **Add the down-round-frequency data.** Carta publishes down-round-frequency by quarter. Add a specific section to the memo on the down-round-frequency read, its interaction with the anti-dilution and pay-to-play clauses, and the implication for the target negotiation.
- **Model the "if market shifts" scenario.** If the current-quarter environment is founder-favourable and the negotiation cycle takes 3-4 months, the market could shift during the negotiation. Model the specific direction (stressed environment: preference moves toward participating; anti-dilution moves toward narrow-based; board seats compress) and preview the fallback posture for each clause.
- **Cross-reference to the term-sheet negotiation role-play** (exercise 08). Which of the market-read data points from this exercise would you cite in the role-play's round-2 push-back? Draft the specific negotiation script.
