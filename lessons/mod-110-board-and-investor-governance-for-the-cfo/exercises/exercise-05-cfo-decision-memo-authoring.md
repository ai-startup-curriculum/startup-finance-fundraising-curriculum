# Exercise 05 — CFO Decision Memo Authoring

**Estimated time:** ~5 hours
**Prerequisites:** Chapter 5 (decision memo authoring and CEO-CFO pre-alignment). Familiarity with mod-103 (driver-based model), mod-107 (fundraising strategy), mod-108 (term-sheet economics), and mod-109 (runway management and bridge financing) is expected; the two memos draw on those modules for the underlying analytics.

## Problem statement

Author two board decision memos in the chapter-5 reference structure (context / decision-required / options / recommendation / risks) — a fundraise memo (a Series-B raise decision) and a major-capex memo (a data-platform rebuild) — with the CEO-CFO pre-alignment work explicit on the page. Each memo must be board-ready: 5-8 pages plus appendix, one specific decision-required statement, three directly-comparable options, a specific recommendation with the conditions under which it would change, and three-to-five risks with mitigation plans.

The exercise trains the memo-authoring discipline that separates a governance-grade decision from a deferred one. A board asked to vote on a decision without a memo will defer, punt, or approve on limited information; a board given a well-structured memo will decide at the meeting, and — even when the board disagrees with the recommendation — the disagreement produces a better second-round conversation because the memo has framed the decision space.

## Scenario — the same Series-B company

Use the Series-B company from exercise 02 (or comparable: $15M ARR, 90 employees, $220M Series-B post-money 12 months ago, cash on hand $28M, $1.6M monthly burn, 17 months of runway, six directors).

**Memo 1 — the fundraise decision.** The company is approaching the Series-B one-year mark. On the current trajectory, the runway is 17 months but the KPI bar for a strong Series-C (typically $30M+ ARR growing 5%+ MoM at Series-C open) is 6-9 months out. The CFO-CEO team must decide whether to open a Series-C raise now (with a smaller round size at a modestly-lower valuation and against a not-yet-hit milestone bar), wait 6 months (with a stronger milestone but tighter runway when the round opens), pursue an insider extension via a Series-B-2 or a note from existing investors (extending runway without a full priced round), or hold the raise for 9-12 months and re-plan to a leaner burn (extending runway operationally).

**Memo 2 — the major-capex decision.** The CTO has proposed a comprehensive rebuild of the company's data platform (customer-data-warehouse, product-analytics, and internal-BI stack): estimated $2.4M one-time build cost over 9 months, plus $600K/year ongoing incremental hosting and personnel cost. Alternative approaches: incremental refactor of the existing stack ($800K over 6 months, plus $200K/year incremental ongoing); "buy" via a data-platform vendor ($400K one-time integration cost plus $900K/year subscription, no ongoing incremental headcount); status quo (accept the current stack's operational risk with no material investment). The full rebuild is the CTO's preferred path; the CFO's initial read is skeptical of the ROI. The decision is on the Q3 meeting's agenda because the CTO has flagged that further deferral will push the rebuild into the following fiscal year and create hiring / budget-cycle complications.

**The pre-alignment context.** For memo 1 (fundraise), the CEO's initial position is "raise now — the market window is closing and we should not miss it." The CFO's initial position is "wait 6 months and raise from a stronger milestone bar; the market window is more open than the CEO reads, per current-quarter Fenwick / WSGR / Carta data." Pre-alignment work is needed to reach a shared recommendation. For memo 2 (data-platform rebuild), the CTO's position is "full rebuild, and here is why." The CEO is agnostic. The CFO is initially skeptical but has committed to reading the CTO's specific analysis and reconciling. Pre-alignment work is needed to reach the CFO's own position and then to align CFO-CEO before the memo circulates.

## Requirements

Produce a submission directory containing the following.

### Part A — the fundraise memo

1. **The pre-alignment memo — fundraise** (`01-fundraise-prealignment.md`). Two-to-three pages. The CFO's internal pre-alignment memo to the CEO, drafted 3-4 weeks before the memo circulates to the board. Includes:
   - The CFO's initial read of the decision space (in the CFO's own voice, before compromise).
   - The specific point of CEO-CFO disagreement.
   - The specific data or analysis that would resolve the disagreement one way or the other.
   - Two-to-three questions the CFO plans to work through with the CEO in the pre-alignment discussion.
   - A "recommended alignment path" — what the CFO believes the two of them should converge on, and the specific concession the CFO is prepared to make.

2. **The board decision memo — fundraise** (`02-fundraise-decision-memo.md`). Six-to-eight pages plus appendix. Chapter-5 structure:
   - **Context** (1 page). Current runway, KPI trajectory, Series-B one-year mark, Series-C milestone bar, current market conditions (cite specific Fenwick / WSGR / Carta vintage or mark `needs-research`).
   - **Decision required** (0.5 page). The specific ask: raise now (with specific target size, valuation range, timing), raise in 6 months, insider extension, or defer 9-12 months. The board is being asked to affirm one of these paths.
   - **Options** (3 pages). Four options presented in a comparable frame. Each with: description, projected round size and dilution, cash-out date implication, KPI-bar readiness at the time of raise, execution risk, and market-window read. Include the "raise now at reduced size" option as a genuine option, not a strawman.
   - **Recommendation** (1 page). The specific recommendation (post-pre-alignment), the reasoning, and the specific conditions under which the recommendation would change ("if the next two quarters' NRR softens below 115%, the recommendation shifts to Option 3 / insider extension").
   - **Risks** (1 page). Three-to-five risks specific to the recommended option, with mitigation.
   - **Appendix.** The runway model reference (from mod-103), the Fenwick / WSGR / Carta market-conditions reference, the target-investor list (per mod-107 chapter 2), and a placeholder for the CFO's diligence-readiness memo.

3. **The pre-alignment reconciliation note** (`03-fundraise-alignment-note.md`). Half a page. A brief note documenting how the CEO's and CFO's initial positions reconciled to the memo's final recommendation. This note is *not* circulated to the board; it is the CFO's own record. Would be useful if the recommendation is challenged retrospectively.

### Part B — the major-capex memo

4. **The pre-alignment memo — data platform** (`04-dataplatform-prealignment.md`). Two-to-three pages. The CFO's internal pre-alignment memo. Includes:
   - The CFO's reading of the CTO's proposal (the specific technical claims the CFO has stress-tested with the CTO, the specific ROI calculation the CFO ran or asked for).
   - The CFO's initial recommendation (based on the CFO's own analysis, not the CTO's advocacy).
   - The specific point of CFO-CTO disagreement, if any (this is an unusual pre-alignment because the CFO is aligning across two counterparts: the CEO and the CTO).
   - A recommended alignment path: what the CFO believes the memo should recommend, and what the CFO is prepared to concede to secure CTO buy-in.

5. **The board decision memo — data platform** (`05-dataplatform-decision-memo.md`). Six-to-eight pages plus appendix. Chapter-5 structure:
   - **Context** (1 page). Current data-stack state, the specific operational or strategic driver for the rebuild consideration, the CTO's proposal history, the timing pressure the CTO has flagged.
   - **Decision required** (0.5 page). The specific ask: which of the four paths (full rebuild, incremental refactor, buy via vendor, status quo) the board is being asked to affirm, and the specific capital-and-headcount authorisation.
   - **Options** (3 pages). Four options in the comparable frame. Each with: description, one-time cost, ongoing cost, headcount implication, timeline, ROI or cost-of-capital calculation, execution risk. The status quo is a real option, not a strawman.
   - **Recommendation** (1 page). The recommendation (post-pre-alignment), the reasoning, and the specific conditions under which the recommendation would change. The recommendation must reconcile with the fundraise memo — a full data-platform rebuild during a runway-tight period is inconsistent with the fundraise decision framework.
   - **Risks** (1 page). Three-to-five risks with mitigation.
   - **Appendix.** The CTO's specific technical proposal (as an attached memo, referenced), the CFO's ROI reconciliation, the vendor-buy-option pricing reference.

6. **The pre-alignment reconciliation note — data platform** (`06-dataplatform-alignment-note.md`). Half a page. Documents how CFO / CTO / CEO reconciled.

### Part C — the memo-to-memo consistency check

7. **The consistency check memo** (`07-consistency-check.md`). One page. The two decisions must be internally consistent: the recommended data-platform path has to be affordable under the recommended fundraise path, and the recommended fundraise timing has to leave adequate runway for the recommended data-platform build. Explicitly note where the two decisions interact and confirm the consistency; if they do not reconcile, adjust one memo to fix the inconsistency and document the adjustment.

### Part D — the board discussion facilitation notes

8. **The board discussion facilitation notes** (`08-board-discussion-notes.md`). One-to-two pages. For each memo, the CFO's own notes for the meeting discussion:
   - The opening framing the CFO will use ("The memo recommends Option 2. The three questions we'd like the board to work through are ...").
   - The specific questions the CFO anticipates each named director will raise, and the specific response the CFO will offer.
   - The specific scenarios in which the CFO would recommend deferring the decision to a written consent or to a follow-up call, rather than pushing for a vote at the meeting.

## Starter guidance

- **Read chapter 5 in full before drafting.** The context / decision-required / options / recommendation / risks structure is deceptively simple; the discipline is in each section's specificity. Attempting the memo without a re-read produces the two most common failure modes: a vague decision-required statement and a "recommendation" that is really a preference without a stated conditional.
- **Draft the pre-alignment memo first, then the board memo second.** The pre-alignment memo is the artefact that captures the CFO's initial position before compromise. Drafting it first forces the CFO to have a genuine position; drafting the board memo first tends to produce a memo that is already-compromised and reads as un-owned.
- **The decision-required section is the load-bearing section.** If a director cannot state, after reading the memo, exactly what vote is being asked, the memo is not ready. "We are seeking board approval to launch a Series-C raise in Q4, targeting $40-60M at $400-550M post-money, with the lead-investor list in Appendix B" is a decision-required statement. "We would like to discuss the fundraise strategy" is not.
- **The options must be directly comparable.** Every option is evaluated on the same dimensions in the same order. A memo where Option 1 lists five dimensions and Option 2 lists three is a memo where the reader is being led toward Option 1 by the presentation, not by the substance.
- **Include a "do nothing" or "status quo" option unless it is inarguably not viable.** Chapter 5's discipline. The status-quo option is often the strongest strawman-defeater and gives the recommendation its defensible frame.
- **The recommendation section is a specific option, not a hybrid.** "Option 1, as presented, with the following two specific adjustments" is a valid recommendation. "Elements of Options 1 and 2" is not.
- **The specific-conditions-under-which-the-recommendation-would-change clause is what makes the recommendation testable.** Without it, the recommendation reads as a fixed opinion; with it, the recommendation reads as a considered judgement.
- **The risks section is three-to-five items, not exhaustive.** A memo with a page of risks reads as hedging. Pick the top three-to-five decision-relevant risks.
- **The pre-alignment memo is honest about the disagreement.** If the CFO's initial read genuinely differs from the CEO's, the pre-alignment memo says so. This is the artefact that would be embarrassing to leak — and the discipline that makes it valuable.
- **The consistency check between the two memos is real.** The fundraise memo's recommended runway path constrains the data-platform memo's affordability. If the two are inconsistent, adjust one before circulating either.
- **The board discussion facilitation notes prepare the CFO for the meeting.** Not a script; a set of anticipated dynamics with prepared responses. Trains the meeting-preparation discipline that keeps decisions from deferring for lack of specific-question response readiness.
- **No fabricated market data.** Fenwick / WSGR / Carta references must cite specific reports and vintages, or be flagged `<!-- needs-research: ... -->`.

## Acceptance criteria

- **All eight deliverables present.** Pre-alignment memo (fundraise), board memo (fundraise), fundraise alignment note, pre-alignment memo (data platform), board memo (data platform), data-platform alignment note, consistency check, board discussion facilitation notes.
- **Each board memo follows the chapter-5 five-section structure** with the specified page counts (5-8 pages plus appendix).
- **The decision-required section of each board memo is a specific, actionable ask.** A director reading only the decision-required section would know what vote is being sought.
- **The options section of each memo presents at least three directly-comparable options** including a status-quo option unless explicitly justified otherwise.
- **The recommendation section of each memo is a specific option** (not a hybrid) with the specific conditions under which it would change.
- **The risks section of each memo is three-to-five items with mitigations.**
- **The pre-alignment memos are honest about the initial CFO-CEO disagreement** and specify what data or discussion would resolve it.
- **The alignment notes document the reconciliation path** from initial-CFO-position to memo-recommendation.
- **The consistency check reconciles the two memos.** No internal inconsistency between the recommended fundraise and the recommended data-platform paths.
- **The discussion facilitation notes prepare for the meeting** with specific expected questions and specific prepared responses.
- **No fabricated market data.** All benchmarks cite specific sources with vintages or are flagged `needs-research`.

## Deliverables

- `01-fundraise-prealignment.md`
- `02-fundraise-decision-memo.md`
- `03-fundraise-alignment-note.md`
- `04-dataplatform-prealignment.md`
- `05-dataplatform-decision-memo.md`
- `06-dataplatform-alignment-note.md`
- `07-consistency-check.md`
- `08-board-discussion-notes.md`

## Extensions (optional)

- **The M&A memo.** Draft a third decision memo covering a small tuck-in acquisition of a competitor product ($5-10M all-cash purchase price; team of 8-12; product complementary rather than substitutive). The memo shape follows the same chapter-5 structure. This adds a specific memo type from chapter 5's five-memo list and requires the same pre-alignment discipline (CFO / CEO alignment plus, in an M&A case, alignment with the seller-side counterparts).
- **The restructuring memo.** Draft a memo for a scenario where the runway trigger fires (per mod-109) and the recommended path is a 20% headcount reduction plus a strategic-shift toward a smaller product-line focus. The memo requires additional CFO discipline: the specific-people-affected planning cannot appear in a memo but the framework for it can.
- **The disagreement variant of the fundraise memo.** Rewrite the fundraise memo assuming pre-alignment did *not* converge — the CEO wants to raise now and the CFO wants to wait, and the memo goes to the board with both positions represented. Draft the specific "the CEO recommends Option 1; the CFO recommends Option 2" framing per chapter 5, and add the specific "board input we are asking for" statement.
- **The lead-director pre-alignment layer.** For the fundraise memo, add the pre-alignment work with the Series-B lead's board director. Draft the CFO's specific script for the pre-alignment call with the lead director: what the CFO shares, what the CFO asks, what the CFO is trying to surface before the meeting.
- **The retrospective — memo grade after the fact.** Assume the board voted for Option 2 on the fundraise (the CFO's initial preference) and 12 months later, the Series-C closed on stronger terms than an earlier raise would have produced. Also assume the data-platform memo landed on the buy-via-vendor path and the vendor implementation encountered specific problems 6 months in. Draft the CFO's retrospective memo on both decisions: what the memos got right, what they got wrong, and what discipline the CFO should carry forward.
