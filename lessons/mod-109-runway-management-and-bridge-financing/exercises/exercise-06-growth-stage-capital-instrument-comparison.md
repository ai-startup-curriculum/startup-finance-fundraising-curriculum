# Exercise 06 — Growth-Stage Capital-Instrument Comparison

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 7 (Growth-Stage Capital Instruments — ATM, PIPE, Reg A+, and Rule 144A). Familiarity with mod-106 (Startup Valuation Frameworks) for the crossover-round pricing framing, mod-107 (Fundraising Strategy) for the investor-targeting framing, and mod-105 chapter 6 (Reg D exemptions) for the private-placement mechanics.

## Problem statement

For a specified late-stage growth company, evaluate five capital-instrument options — a traditional Series-C priced round, an ATM offering (assuming the company is post-IPO), a PIPE (both a pre-IPO crossover PIPE and a public-company PIPE variant), a Reg A+ Tier 2 offering, and a Rule 144A convertible-debt placement — against the same funding need, and author the CFO's instrument-selection memo defending the recommendation to the board. The point of the drill is to build the muscle for reading the growth-stage capital menu holistically rather than defaulting to whichever instrument the company's banker or existing investors happen to know best.

Two versions of the scenario are provided. Run the drill against both.

## Scenario A — Late-stage private company, pre-IPO

**Company.** Vertical B2B SaaS company, ~350 employees, ARR $85M growing 35% YoY, NRR 128%, gross margin 79%, operating loss ~$25M annually and narrowing. Series-B closed 30 months ago at $500M post-money. Series-C not yet raised. Currently profitable-on-adjusted-EBITDA basis; GAAP still operating at a loss. Cash on hand $60M, burn ~$2M/month — 30 months of runway. Board is beginning to discuss the IPO path with a 18-30 month planning horizon.

**Funding need.** $150M to fund the two-year path to IPO — accelerating GTM investment in adjacent geographies, funding a strategic acquisition in the $50-80M range, building the finance/legal/IR infrastructure needed for the S-1 and post-IPO reporting. The company could also do less ($75-100M) and defer the acquisition.

**The five options.**

1. **Traditional Series-C priced round.** Target $150M at $1.6-2.0B post-money, led by a growth-stage venture fund (Insight / Iconiq / General Atlantic / TCV pattern) with participation from existing investors and one or two crossover investors.
2. **Pre-IPO crossover PIPE.** $150M crossover round from a mix of mutual-fund crossover investors (Fidelity, T. Rowe Price, Baillie Gifford), hedge funds (Coatue, D1, Whale Rock), and one or two traditional VCs, structured as a private placement under Reg D at $1.6-2.0B post-money. Investors expect to hold through the IPO.
3. **Reg A+ Tier 2 offering.** Up to $75M in a Tier 2 offering to a mixed retail-and-institutional base. Requires SEC qualification of a Form 1-A; ongoing 1-K / 1-SA / 1-U reporting. The company would still need to raise a supplemental $75M via one of the other paths.
4. **Rule 144A convertible-debt placement.** $150M in convertible notes placed to QIBs. Note terms: 5-year tenor, 3% coupon, 20% conversion premium above the last-round-priced-per-share (implied by the pre-money ~$1.5B). Banker-underwritten; QIB-only resale.
5. **ATM offering.** Not available for Scenario A — the company is not public, so no shelf and no ATM. (This is a diagnostic — the CFO's memo has to state clearly which options are on the menu and which are not.)

## Scenario B — Newly-public company, 18 months post-IPO

**Company.** Same company as Scenario A but 18 months later. The company IPO'd 18 months ago at $28/share ($3.5B market cap on the offering; $4.2B post-IPO trading peak, currently $32/share = ~$4.0B market cap). Q4 revenue $145M, revenue growth 40% YoY, operating margin still negative but improving. Cash on hand $180M (from IPO proceeds + operating cash), burn ~$8M/month, but this is a growth-mode burn including the acquired-business integration.

**Funding need.** $200M to fund a specific strategic acquisition of a competitor ($120M cash) and to top up the balance sheet for the post-acquisition operating plan. The acquisition target is under LOI; the funding is time-sensitive (need to close in 60-90 days).

**The five options.**

1. **Traditional Series-C priced round.** Not available for Scenario B — the company is public, so any equity issuance is a public-company transaction, not a private preferred round. (The CFO's memo notes this.)
2. **Public-company PIPE.** $200M private placement to institutional investors, priced at a 5-15% discount to the current market ($32/share). 8-K disclosure at signing. Registration-rights obligation to file a resale registration within 30-90 days.
3. **Reg A+ Tier 2 offering.** Not typically a fit for a listed public company (Reg A+ is a pre-IPO / non-listed vehicle). Note in the memo.
4. **Rule 144A convertible-debt placement.** $200M in convertible notes placed to QIBs. Note terms: 5-year tenor, 1.5% coupon, 25% conversion premium above the current market ($32 × 1.25 = $40). Banker-underwritten; QIB-only resale. Optionally paired with a capped-call transaction with the underwriters to raise the effective conversion premium and reduce dilution.
5. **ATM offering.** The company has an effective shelf (S-3) and can establish an ATM programme. Sales at prevailing market prices, 1-2% agent commission. Estimated take-up: $50-100M over 6-12 months at current volumes, without pressuring the price.
6. **Hybrid.** Some combination — e.g., $120M convertible 144A + $80M ATM over 6-12 months, or $150M PIPE + $50M ATM.

## Requirements

Produce a single deliverable pack containing the following. The pack covers both scenarios.

### Part A — the instrument-by-instrument comparison

1. **Comparison table across the seven dimensions from chapter 7.** For each of the instruments in each scenario, populate a table with:
   - Size (achievable in the required window).
   - Cost (explicit fees; implicit discount; dilution).
   - Regulatory friction (filings, disclosures, ongoing reporting).
   - Investor base (institutional / retail / mixed).
   - Signalling (positive / neutral / stress signal).
   - Time to close.
   - Prerequisites (S-3 eligibility, listing status, etc.).
2. **Prerequisites gate.** Explicitly flag which instruments are unavailable in each scenario (Series-C for Scenario B; ATM for Scenario A; Reg A+ generally ill-fitting for Scenario B) and confirm the CFO understands why.

### Part B — the illustrative modelling

3. **Illustrative model for each instrument** (in each scenario where the instrument is on the menu):
   - Cash proceeds at close (or over the drawn horizon for ATM).
   - Explicit costs (commission, banker fees, legal fees, SEC filing fees).
   - Implicit costs (discount to current market for a PIPE; discount to face value for a Reg A+; dilution equivalent for a Series-C).
   - Resulting cap-table impact — new shares issued (or convertible-shares issuable on conversion for the 144A convert), pre-vs-post ownership summary for founders / existing preferred / new investors / public float (if applicable).
   - Per-share EPS impact (for the public-company scenario) — using a share count consistent with the treasury-stock method for the convert.
   - Cash position post-close.
   - Notes on any anti-dilution / reset / make-whole mechanics in the specific term structure.
4. **PIPE reset sensitivity (for the convertible-PIPE case).** In Scenario A, assume the crossover PIPE includes a "make-whole" reset if the eventual IPO prices below the PIPE post-money by more than 20%. Model the additional shares issued to the PIPE investors under three IPO-price scenarios (par to PIPE post-money; 30% below; 50% below). Show the dilution effect on the founders in each case.
5. **Convertible-144A dilution modelling (Scenario B).** Compute the fully-diluted share count assuming the convert is entirely converted at the conversion premium. Compute the incremental dilution to existing shareholders. Model the same with a capped-call hedge raising the effective conversion premium to, say, 75% above the current market — quantify the dilution difference and the additional cash cost of the capped call.
6. **ATM cumulative dilution (Scenario B).** Assume the company runs the ATM programme over 12 months, selling at an average price 5% below the current $32. Compute the total shares issued for $80M raise. Compute the cumulative dilution to pre-ATM shareholders and note the pattern effect (retail sees the incremental dilution and may pressure the price further; model a 5% additional price decline assuming that pattern).

### Part C — the regulatory-and-execution checklist

7. **Regulatory-and-execution checklist for each recommended path.** For each of the two scenarios, produce a per-instrument checklist covering:
   - SEC filings required and timing (S-1 for Series-C? None — private. S-3 for ATM? Already effective. 8-K for PIPE close. Form 1-A for Reg A+ qualification. 8-K + registration statement for 144A convert).
   - Board consents required (financing authority; convertible-debt authority; ATM equity-distribution-agreement authority).
   - Preferred-stock protective-provision consent, if applicable.
   - Any shareholder-vote requirement (typically not for these instruments; exception for Reg A+ if the offering exceeds a defined float threshold or for a convert with an unusual conversion feature).
   - Existing-lender consent under negative-covenant clauses (venture debt if any).
   - Banker / advisor engagement timeline.
   - Legal counsel engagement (securities counsel for the SEC-registered instruments; corporate counsel for the private placements).
   - Disclosure plan (how the transaction will be described to the market on the next earnings call or in the S-1).

### Part D — the CFO's instrument-selection memo

8. **Instrument-selection memo (2-3 pages per scenario, so 4-6 pages total).** For each scenario:
   - Situation summary: funding need, timing, business context (pre-IPO planning; acquisition financing).
   - The five (or fewer) available instruments and the comparison across the seven dimensions.
   - The specific instrument (or hybrid) the CFO recommends.
   - Defence of the recommendation against each of the alternatives — what the alternative would have done better, what it would have done worse, and why the recommendation wins on balance.
   - Regulatory and execution timeline.
   - Board approval request: specifically what the board is being asked to authorise.
   - Disclosure and communication plan: how the transaction will be presented on the earnings call / IPO roadshow / analyst update.

### Part E — the transaction-execution boundary

9. **Boundary memo (half a page).** Note explicitly what parts of the transaction the CFO owns and what parts hand off to bankers, counsel, and — for the IPO path — the `startup-exit-curriculum` scope. The instrument-selection decision and the term-negotiation are CFO-owned; the running of the process (banker engagement, buyer outreach, roadshow choreography, book-building, allocation) is not. Confirm the boundary explicitly.

## Starter guidance

- **Scenario A's crossover PIPE and Series-C look similar on the term-sheet surface** — both are priced private placements. The key difference is the investor base (crossover PIPE brings in mutual-fund and hedge-fund names that anchor the IPO book; a traditional Series-C brings in growth-VC follow-on investors). Read the strategic value of the anchor investors into the comparison.
- **Reg A+ at $75M plus another $75M is often less attractive than a single $150M path.** Two capital events cost more in aggregate fees and disclosure work than one; and the Reg A+ investor base (retail-heavy) is a different constituency the company would then have to manage across the S-1 and post-IPO.
- **The 144A convert with a capped call is the growth-tech default for post-IPO acquisition financing at Scenario-B scale.** The convert delivers cash at a low coupon; the capped call reduces effective dilution to a level that founder-led companies can live with. It is more expensive than an ATM in raw cash terms but delivers all the capital at once and does not depend on the market price cooperating.
- **The ATM is the "opportunistic" tool.** Its right-fit case is incremental capital raised over months at market prices the company would accept. Its wrong-fit case is time-sensitive capital raised in bulk; you cannot ATM $200M in 60 days without moving the price against yourself.
- **The PIPE-reset modelling matters even if the reset feels unlikely.** In a stressed IPO market, the reset can fire and dilute the founders by materially more than the initial PIPE numbers implied. Model it explicitly.
- **The regulatory-and-execution checklist is the point where the CFO becomes the coordinator, not the doer.** The bankers file the S-1, counsel drafts the definitives, IR handles the earnings-call script. The CFO's job is to know what the timeline is, who owns each piece, and where the schedule can slip.
- **The instrument-selection memo is a board memo, not a banker deck.** The board wants the CFO's judgement on which instrument fits, with the alternatives fairly represented so the board can push back. Bankers deliver the marketing materials for the chosen path; the CFO delivers the decision framework.
- **Scenario A's ATM row and Scenario B's Series-C / Reg A+ rows are diagnostic — they should be filled in with "not available; here's why."** The CFO who doesn't recognise a prerequisite gate is the CFO who wastes cycles on options that were never on the menu.

## Acceptance criteria

- **The comparison table covers all five (or fewer, per prerequisites) instruments in each scenario across all seven dimensions.**
- **Instruments unavailable in a scenario are explicitly flagged** with the specific prerequisite that rules them out.
- **Every recommended path has an illustrative model** with cash proceeds, explicit and implicit costs, cap-table impact, and (for Scenario B) EPS impact.
- **The PIPE-reset and convert-with-capped-call modelling produce quantitative outputs** — additional-shares-issued under stress scenarios; cost of the capped-call hedge.
- **The regulatory-and-execution checklist is instrument-specific** — the SEC filings, board consents, and disclosure obligations are correct for each instrument.
- **The instrument-selection memo makes a specific recommendation for each scenario** with a defensible reason and a fair comparison to the alternatives.
- **The boundary memo correctly separates CFO-owned decision work from banker / counsel / IR execution work** and identifies the M&A / IPO transaction-execution handoff to `startup-exit-curriculum`.

## Deliverables

- The comparison-table workbook (spreadsheet or Markdown table).
- The illustrative-modelling workbook (spreadsheet).
- The regulatory-and-execution checklists (Markdown or PDF).
- The two instrument-selection memos (Markdown or PDF; can be one document with sections).
- The boundary memo (Markdown or PDF).

## Extensions (optional)

- **De-SPAC PIPE alternative for Scenario A.** Add a sixth option: a de-SPAC merger with an existing SPAC vehicle plus a de-SPAC PIPE of $150M. Note the specific mechanics (SPAC redemption risk, PIPE anchor, merger vote, forward-purchase agreements). Compare to the traditional S-1 IPO path in the same memo.
- **Reg S + 144A cross-border structure for Scenario B.** Model the 144A placement paired with a Regulation S offshore offering. Note the incremental investor base (non-US institutional) and any incremental regulatory obligations.
- **ATM programme design.** For Scenario B, design the ATM programme in detail: aggregate cap, tranche pattern, sales-instruction protocol, blackout-window handling, MNPI protocols, disclosure cadence. Produce a one-page programme document.
- **PIPE with warrant coverage.** Assume the Scenario A crossover PIPE includes warrant coverage (5% of the PIPE size at a strike above the current price). Compute the incremental dilution and effective yield to the PIPE investors. Compare to a no-warrant version.
- **Capped-call design.** For Scenario B's 144A convert, design the capped-call transaction in detail: notional size (matching or overhedging the convert), strike prices (lower = the convert conversion price; upper = the effective raised conversion price), cost (typically a few percent of the convert notional). Explain why bankers routinely propose the capped call alongside the convert and where the added cash cost is worth the reduced dilution.
- **Retrospective at S-1.** For Scenario A, assume the company chose the crossover PIPE and files the S-1 12 months later. Draft the "capital raises in the two years preceding the offering" section of the S-1 covering the crossover PIPE. Compare to what would have been filed if the company had chosen the Series-C instead.
