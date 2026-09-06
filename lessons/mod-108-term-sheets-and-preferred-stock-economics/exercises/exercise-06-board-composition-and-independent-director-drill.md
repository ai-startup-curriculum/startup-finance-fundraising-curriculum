# Exercise 06 — Board Composition and Independent-Director Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 7 (seed / Series-A / Series-B board patterns, independent-director selection mechanics, Voting Agreement).

## Problem statement

Design the Series-A board for a hypothetical company under three different offered board structures from the lead investor. For each, produce the founder-side counter, the specific Voting Agreement nomination-and-removal drafting notes, and an independent-director sourcing plan. Then author the memo the CFO writes to the CEO comparing the three structures across the axes that matter — founder-control durability, independent-director recruitability, and Series-B/Series-C evolution risk.

The exercise trains the specific mechanics of board-composition negotiation at Series-A, which is the round at which the seed-founder-heavy board is reshaped into the multi-year governance structure the company operates under between rounds. Chapter 7 walked the pattern; this exercise applies it to specific offered structures and forces the founder-side counter and the sourcing plan.

## Scenario — the pre-Series-A state

**Post-seed cap table** (before the Series-A close):

- Common: 8,000,000 shares (Founder A: 4,500,000; Founder B: 3,500,000). Founder A is CEO; Founder B is CTO.
- Options granted / unissued: 800,000 shares.
- Seed Preferred: 1,500,000 shares. Raised $3,000,000 at $2.00 per share, held by seed lead (60%, $1.8M) and three angels (~40% split). 1x non-participating, broad-based WA, NVCA-standard protective provisions.
- Fully-diluted: 10,300,000 shares.
- Board today: three directors — Founder A (CEO), Founder B (CTO), Seed Lead partner. The board has met quarterly; consents handle most decisions.

**Series-A round** (in negotiation now):

- Series A Preferred: raising $12M at $30M pre / $42M post. Price per share: $30M / 10,300,000 ≈ $2.913.
- Series A shares issued: $12M / $2.913 ≈ 4,120,000 shares. Post-Series-A FD: ~14,420,000 shares.
- Post-Series-A ownership: founders combined ~55%, seed preferred ~10%, Series-A preferred ~29%, pool ~5% (assumes a small pool top-up placed pre-money; ignore rounding).
- The Series-A lead is an institutional venture fund with a strong Series-A / Series-B portfolio in the sector.

## Three offered board structures

The Series-A lead has proposed three alternative board structures in the term sheet. All are offered as "market-standard variants"; the CFO must pick and counter.

**Structure A — three-director board.**

- 1 founder director (elected by common).
- 1 Series-A director (elected by Series-A preferred).
- 1 independent director (mutually agreed by common and Series-A preferred; nomination process TBD).

**Structure B — five-director board, founder-favourable.**

- 2 founder directors (elected by common).
- 1 Series-A director (elected by Series-A preferred).
- 2 independent directors (one elected by common, one jointly nominated and elected by common + Series-A voting together).

**Structure C — five-director board, investor-swing.**

- 1 founder director (elected by common; the CEO).
- 1 Series-A director (elected by Series-A preferred).
- 1 seed-lead director (elected by seed preferred — grandfathering the seed lead's board seat).
- 2 independent directors (both jointly nominated and elected; both must be mutually acceptable to common and to Series-A preferred).

## Requirements

Produce five deliverables in a submission directory.

1. **Structure-comparison table** (`board-comparison.md`). One column per structure (A, B, C). Rows:
   - Total seats.
   - Founder seats.
   - Series-A investor seats.
   - Seed / other investor seats.
   - Independent seats.
   - Founder-plus-independent block (does founder plus independents have a majority?).
   - Series-A investor-plus-independent block.
   - "Deadlock" risk (structures with even splits or with mutual-approval requirements on the independent).
   - Two-year evolution risk: what happens at Series-B (add Series-B director; do founder seats compress; does one independent get replaced)?
   - CFO tier classification (chapter 1's four-tier framework): market / negotiated / aggressive / unusual.

2. **Counter-structure and Voting-Agreement drafting notes** (`counter-and-va-notes.md`). Two sections:
   - **The counter.** Pick one of A / B / C as the base and specify the exact modifications you would counter with — or propose a Structure D combining features. Justify from the comparison table. Recommend for this company (assume founder-favourable posture is the CEO's stated preference; the Series-A lead is not distressed and can absorb the counter).
   - **Voting Agreement drafting notes.** For your counter-structure, draft the specific Voting Agreement mechanics:
     - Who nominates each seat (common holders? Series-A holders? mutual?).
     - How many votes required to elect (majority of each electing class).
     - How a director is removed (removal by the electing class only; specific-cause vs. no-cause).
     - How a vacancy is filled (nomination path when a director resigns or is removed).
     - The specific handling of "independent" — the definition, the qualification criteria (unaffiliated with company, founders, or preferred; industry experience; audit-committee-eligibility for later stages), and the tie-break mechanic if the electing classes cannot agree on a mutually-acceptable candidate.
     - Board-meeting mechanics (frequency, quorum, notice, materials-delivery timing) — the Voting Agreement itself doesn't govern this but the CFO should note the interlock with the bylaws.
     - Observer rights — who gets them (seed lead as a step-down from their board seat? senior Series-A investors?), what they can attend, what they can access.

3. **Independent-director sourcing plan** (`independent-sourcing-plan.md`). A specific plan for filling the independent seat(s). Contents:
   - **Target profile.** The specific attributes the ideal independent would have — industry experience, functional expertise (GTM / product / operations / finance), stage experience, network for the next round. Distinguish for each independent seat if multiple.
   - **Sourcing channels.** Bolster, Extend, Boardsi, Directorpool, executive-search firms specialising in board placement, the Series-A lead's network, the CEO's advisory network, industry peer CEOs. Rank by expected fit and speed.
   - **The vetting mechanic.** Interviews, references, board-meeting observation, chemistry check with existing directors and the CEO.
   - **Compensation and commitment.** Standard Series-A independent compensation (equity grant range, cash retainer if any); time commitment (annual hours per director for board + committees + between-meeting availability).
   - **Timeline.** From term-sheet execution to the seated director. Realistic: 8-16 weeks for the first independent; second independent often lags (the "add one now, one within X months" pattern).
   - **The two-independent case.** If your counter-structure has two independents, address the joint-selection dynamic. One nominated by common; one nominated by common + Series-A (or however you drafted it in the Voting Agreement notes above).

4. **CEO-facing comparison memo** (`ceo-memo.md`, 1-2 pages). Structure:
   - **Bottom-line summary.** One paragraph: the three structures with a one-line classification each, the recommendation, the specific counter.
   - **The founder-control read.** Under each structure, does the founder-plus-independents block have a functional majority in normal-course votes? What happens when the block breaks down?
   - **The two-year evolution.** How does each structure evolve at Series-B / Series-C? Which structure risks compressing founder representation fastest?
   - **The independent-director recruitability read.** Which structure requires the hardest independent-recruit (mutual-approval independents are hardest; common-elected independents are easiest). What is the realistic timeline for each?
   - **The recommendation.** One sentence. The counter-structure name and the two-to-three specific parameter changes from the offered structure.

5. **Board-charter / bylaw watch items** (`board-charter-notes.md`, half page). The specific downstream items the CFO watches in the definitive documents that translate the Voting-Agreement drafting into operating mechanics: board-size cap and floor in the Amended and Restated Certificate; committee-composition provisions (audit / compensation / nominating committees); D&O insurance coverage minimums; director indemnification agreements. This is the "watch items after signing" list.

## Starter guidance

- **Do not go bigger than five directors at Series-A without a reason.** Seven-director Series-A boards exist but are unusual and typically only appear in specific late-Series-A patterns with two co-leads. The default is three or five.
- **Founder-plus-independents majority is the durable durability lever.** In any structure, count "founder seats plus independent seats" — that is the block that holds day-to-day authority against the investor director. Structures where founder + independents = 3-of-5 or 4-of-5 preserve founder control; structures where the count drops to 2-of-5 or below are functionally investor-controlled.
- **Mutual-approval independents are hard to fill.** They also produce genuinely-independent candidates because both sides must agree. Trade-off: recruitability vs. independence.
- **Draft the removal mechanic explicitly.** A director elected by common cannot be removed by the preferred, and vice versa. But the tie-breaking mechanic for a mutual-approval director's removal is a specific drafting question — is the mutual-approval independent removed only by both classes voting together, or by either? Chapter 7's typical drafting is "by joint vote of the electing classes."
- **Chapter 7's Series-B / Series-C evolution matters at Series-A.** The structures where a Series-B seat naturally slots in (six-director boards, expansion by one) are easier at Series-B than structures that require rejigging (three-director boards forced to five at Series-B, which requires renegotiating everyone's seats). The Series-A CFO negotiates for the shape that scales.
- **Cite the current-quarter market.** Fenwick / WSGR sometimes publish board-composition data; Carta has some. If the data isn't available, flag `<!-- needs-research: modal board size and composition at Series-A per Fenwick Q?/YYYY -->`.

## Acceptance criteria

- **The structure-comparison table covers all three structures on all listed rows** with specific numbers or specific patterns.
- **The tier classification of the three structures is defensible** — one of the three should be tier-3 or tier-4 aggressive (structure A's three-director board is very-lead-favourable at this ownership; structure C's investor-swing composition is compression-heavy for the founder). One should be closer to market (structure B; some variants).
- **The counter-structure is a specific structure** — not a range. Named, parameterised, and justified from the comparison.
- **The Voting Agreement notes address all seven drafting parameters** (nomination, election threshold, removal, vacancy, independent definition and tie-break, meeting mechanics, observer rights).
- **The independent-director sourcing plan has a realistic timeline** and names specific sourcing channels.
- **The two-independent case is addressed** if the counter has two independents.
- **The CEO memo makes a specific recommendation** and defends the three-to-five key differences between the counter and the offered structures.
- **Board-charter watch items name at least four specific downstream drafting items** (bylaws, committees, D&O, indemnification).
- **No fabricated data.** Board-composition incidence claims cited or `<!-- needs-research -->` flagged.

## Deliverables

- `board-comparison.md` — the three-structure comparison table.
- `counter-and-va-notes.md` — the counter-structure and Voting Agreement drafting notes.
- `independent-sourcing-plan.md` — the sourcing plan.
- `ceo-memo.md` — the CEO-facing comparison memo.
- `board-charter-notes.md` — the definitive-document watch items.

## Extensions (optional)

- **Model the Series-B evolution.** Roll the counter-structure forward to a Series-B ($30M raised on $90M pre). The Series-B lead requests a director seat. Redesign the structure for Series-B. Which independent seat (if any) is replaced? Does a founder seat compress? Produce the Series-B Voting Agreement amendment.
- **Model the CEO-succession scenario.** Assume Founder A steps down as CEO 18 months post-Series-A and Founder B becomes CEO. What are the specific Voting Agreement mechanics for reassigning the CEO seat? Does the "founder director" definition need to change? Draft the specific amendment.
- **Model the "founder is fired" scenario.** Series-A lead loses confidence in Founder A and wants to remove them as CEO (and as director). What are the specific mechanics under each of the three offered structures? Which is easiest for the preferred to execute; which is hardest? Preview of [mod-110](../../mod-110-board-and-investor-governance-for-the-cfo/).
- **The observer-rights sprawl.** Draft language limiting observer rights to specific investors above a threshold (e.g., Major Investors only, capped at three observers) and specifying access limits (materials, meetings, executive sessions).
- **Committee composition.** For your counter-structure, design the audit-committee and compensation-committee composition post-Series-A. Two-independent committees or one-independent-plus-one-founder? Which independents? What are the SEC-adjacent qualifications for audit-committee membership (relevant when the company is IPO-planning at Series-C or Series-D)?
