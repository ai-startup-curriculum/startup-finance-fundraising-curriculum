# Exercise 02 — Quarterly Board Pack Authoring

**Estimated time:** ~6 hours
**Prerequisites:** Chapter 2 (the quarterly board pack — architecture, reconciliation, and the 72-hour rule). Chapters 4 (consents / action items) and 5 (decision memos) are referenced by the risks / decisions / consents section; you can complete this exercise before doing exercise 04 or 05 by using placeholder resolution and memo drafts. Familiarity with mod-102 KPI definitions and mod-103 three-statement models is expected.

## Problem statement

Author a complete quarterly board pack for a specified Series-B company — CEO letter, KPI dashboard, financials in the actuals-vs.-budget-vs.-prior-quarter frame, one strategic deep-dive, and the risks / decisions / consents section — and produce the 72-hour pre-read distribution artefact (subject line, cover email, pack format, board-member distribution list, and pre-read call schedule). The pack must reconcile: every KPI number ties to the P&L and balance sheet numbers, which tie to the general ledger, and the KPI-definition table is republished in the appendix.

The exercise is the module's core authoring drill. It integrates the chapter-2 architecture with the reconciliation discipline and the 72-hour cadence, and it produces the single reference artefact the rest of the module — meetings, consents, decision memos, and committees — hangs off.

## Scenario — build your own Series-B company

Author the company context this pack will cover.

**Company context.** B2B SaaS at $12M-$18M ARR, growing 5-8% MoM, 75-110 employees, closed a $30-50M Series-B 8-14 months ago at a $150-250M post-money. Board composition (five to seven directors): two founder-CEO / co-founder seats, one Series-B lead director, one Series-A lead director (still on the board), one to two independents. Cash on hand $25-40M with $1.2-1.8M monthly burn (12-24 months of runway). Current-quarter is the Q3 pack (September-end close for a fiscal-year-aligned company).

Document the company context on a "context" page: name (fictional), stage, ARR entering the quarter, headcount, cash / burn / runway, product category, sector (SaaS-general or vertical), board roster with roles and independent-vs.-affiliated status.

**The quarter under review.** Design a plausible mixed quarter. ARR grew 6% MoM average across Q3 against a plan of 8%; the miss is concentrated in the enterprise segment; NRR held at 118%; gross margin softened by 100 basis points due to a hosting-cost step-change; headcount grew per plan; two senior hires closed and one senior departure occurred. Cash on hand slightly ahead of plan due to a delayed vendor payment. This is not a disaster quarter and it is not a strong quarter; it is a normal-mixed quarter, which is what the pack most often has to represent honestly.

**The strategic deep-dive topic for this meeting** was selected at the prior meeting: the go-to-market segment-focus decision. The operating team is bringing a memo to the board recommending a specific segment-focus shift over the next four quarters. This is a decision item; the board is being asked to affirm the segment-focus direction (see requirement 4 below).

## Requirements

Produce the full board pack as a submission directory.

1. **The company-context page** (`00-context.md`). One page. The internal reference; not part of the pack sent to the board.

2. **The KPI-definition table** (`kpi-definitions.md`). Ten to fifteen KPIs (ARR, net-new-ARR, NRR, gross retention, gross margin, CAC payback, headcount, burn multiple, magic number, cash, runway, and 3-5 company-appropriate additional metrics). For each: the exact calculation, the data source, the update cadence, and the responsible owner. This gets republished as an appendix in every pack for the year (chapter 2).

3. **The CEO letter** (`01-ceo-letter.md`). One-to-three pages. The CEO's narrative for the quarter. What happened, the CEO's read, the next quarter's focus, and what the CEO specifically wants from the board this meeting. Voice is the CEO's; consistency with the KPI dashboard is the CFO's edit.

4. **The KPI dashboard** (`02-kpi-dashboard.md`). Two-to-four pages. Each KPI on a row (or a grid layout equivalent) with: current-quarter actual, current-quarter plan, prior-quarter actual, YTD actual, YTD plan, and a trailing-12-month chart for the top three. Definitional footnote reference for every non-obvious metric. Variance callouts (a footnote number tied to the narrative below the table) for material misses or beats.

5. **The financials section** (`03-financials.md`). Four-to-eight pages. Full P&L, balance sheet, and cash flow in the eight-column format (current-quarter actual | current-quarter budget | variance | prior-quarter actual | QoQ delta | YTD actual | YTD budget | updated full-year forecast). Variance callouts above a materiality threshold (name your threshold explicitly; the chapter-2 heuristic is ±10% of the budget line or ±$100K, whichever is greater). One narrative paragraph per statement. A dedicated cash-and-runway page or half-page including current cash, trailing-three-month burn, forward runway on the updated forecast, and distance from each of the mod-109 12 / 9 / 6-month triggers. Two-to-three balance-sheet items called out in a short narrative (AR aging, deferred revenue and its tie to ARR, and any debt / warrant / preference balance).

6. **The strategic deep-dive memo** (`04-strategic-deep-dive.md`). Five-to-ten pages on the go-to-market segment-focus decision. Executive summary (one page), context (one to two pages), the specific option set (three options with directly-comparable evaluation dimensions — segment mix, sales-team implications, dollar impact, execution risk), recommendation (one page), risks (one page). This memo also serves as the decision memo (chapter 5) for the affirmation the board is being asked to give.

7. **The risks / decisions / consents section** (`05-risks-decisions-consents.md`). Two-to-four pages.
   - **Risks:** three-to-five bulleted risks. For each: the risk, the operating team's assessment (probability × impact or qualitative equivalent), the mitigation plan, the escalation trigger.
   - **Decisions:** cross-reference the strategic deep-dive memo (from requirement 6); name the specific ask ("we are seeking board affirmation of the segment-focus direction recommended in Section 4"). Draft one additional decision item (e.g., approval to hire a VP International, or authorisation of a specific $500K capex on a data-platform rebuild) with a placeholder for the decision memo (a real memo is written in exercise 05).
   - **Consents:** three-to-five consent items. Include ordinary quarterly consents (409A refresh approval, an ISO-and-RSU option-grant approval, prior-quarter minutes approval) and at least one non-standard consent (e.g., authorisation of an insider-note or venture-debt facility term-sheet). Cross-reference the specific resolution (placeholder; a full consent is drafted in exercise 04).

8. **Appendices** (`06-appendices/`). Cohort table (or a description of the cohort table), a functional-team update from one function (e.g., product roadmap update or engineering hiring plan), the KPI-definition table (from requirement 2), the prior-meeting action-item register status (placeholder if you have not done exercise 04).

9. **The 72-hour pre-read distribution artefact** (`07-distribution.md`). Includes:
   - The cover email the CFO sends when the pack lands 72 hours before the meeting: subject line (identifies the meeting date), body (one paragraph — the pack is attached, the meeting is on [date/time], the strategic deep-dive topic is [topic], the specific decisions and consents in the pack are [list], the CFO will follow up individually to schedule pre-read calls with senior directors). Attachment or data-room link listed explicitly.
   - The distribution list: every board member (voting), every observer, the corporate counsel (typically CC'd), any advisor entitled to receive.
   - The pre-read call schedule: the two-to-three senior directors the CFO plans to talk with in the 72-hour window, the specific questions the CFO expects each to raise, and a proposed 15-30 minute call time for each.
   - The version-control convention: the pack filename with date and version, the location of the master (data-room folder path or portal URL), the policy for updates (addendum email only; no silent re-upload).

10. **The reconciliation memo** (`08-reconciliation-memo.md`, 1 page). The CFO's own reconciliation check. For each of ARR, net-new-ARR, gross margin, cash, runway, headcount, CAC / payback, and NRR: the source line in the pack, the source line in the financial model or general ledger, and a one-line confirmation that they tie. This memo is *not* sent to the board; it is the CFO's own artefact and, once mature, a template the CFO's finance team runs pre-pack as a QC step.

11. **The pack-preparation timeline** (`09-timeline.md`). Working backward from the meeting date, the specific dates (from day M-30 through day M+5) for each pack-preparation milestone. Names the specific people accountable at each milestone (CFO, finance controller, CEO, CFO's board-facing coordinator if one exists).

## Starter guidance

- **Re-read chapter 2 before drafting.** The five-section architecture, the reconciliation discipline, and the 72-hour rule are all specified in detail there. Attempting the pack without a re-read produces a walk-the-pack-shaped pack — a beautifully-designed slide deck that reads as marketing rather than governance.
- **Start with the KPI-definition table.** The rest of the pack cannot reconcile if the definitions are not locked. Write the definitions first; then draft the financials; then draft the KPI dashboard against those numbers; then draft the CEO letter last, so the narrative reflects the actuals rather than the CEO's memory of the quarter.
- **Use the eight-column financials format even if it feels wide.** The columns are the discipline. If the format does not fit on a page, split the balance sheet onto its own page rather than dropping columns.
- **Materiality-threshold callouts are load-bearing.** Pick your threshold explicitly at the top of the financials section, and mark every line that trips the threshold. A financials section without callouts reads as unanalysed data.
- **The strategic deep-dive is a decision memo, not a "here's an update on segment focus" memo.** Write it in the chapter-5 structure (context / decision-required / options / recommendation / risks). This alignment across chapter 2 and chapter 5 is not a coincidence; the deep-dive slot is the natural home for the decision memo when a decision is being asked.
- **The risks list is small and specific.** Three-to-five risks. Every risk has a mitigation and an escalation trigger. A ten-risk list reads as hedging. A risk that has been on the list for three consecutive quarters without escalation should be either escalated or removed (chapter 2).
- **Reconcile before you distribute.** The reconciliation memo (requirement 10) is a real check, not a formality. If a number in the KPI dashboard does not tie to the financials, the pack is not ready to send.
- **The 72-hour distribution is on the specific business-day calendar.** If the meeting is on a Tuesday, the pack lands the previous Friday morning — 72 hours before the meeting start time, on a business day so board members' inboxes are being read. A pack landing at 11pm on a Sunday for a 9am Tuesday meeting is technically 72 hours but functionally a same-day drop.
- **Do not fabricate industry benchmark data.** If the CEO letter or the deep-dive cites benchmark numbers (SaaS medians, sector NRR, competitor multiples), cite a specific report and vintage or mark `<!-- needs-research: ... -->`.

## Acceptance criteria

- **All 11 deliverables present.** Context page, KPI-definition table, CEO letter, KPI dashboard, financials (with cash-and-runway callout), strategic deep-dive, risks / decisions / consents, appendices, distribution artefact, reconciliation memo, and preparation timeline.
- **Every KPI in the dashboard has a definition in the KPI-definition table.** Every definition names a calculation, a source, a cadence, and an owner.
- **Every KPI number in the dashboard reconciles to a specific line in the financials.** The reconciliation memo demonstrates this explicitly for at least eight KPIs.
- **The financials section is in the eight-column format** with materiality-threshold variance callouts and a narrative paragraph per statement.
- **The strategic deep-dive is a real memo**, not a survey — 5-10 pages, chapter-5 structure, three directly-comparable options, a specific recommendation.
- **The risks / decisions / consents section names every decision and consent** and cross-references the underlying memo or resolution (placeholder or real).
- **The 72-hour cover email is realistic** — a subject line that identifies the meeting, a distribution list that includes every director and observer, a version-control convention, and a specific pre-read call schedule for at least two senior directors.
- **The reconciliation memo demonstrates that the pack reconciles to a single set of numbers.** No number in the pack is unaccounted-for.
- **The preparation timeline works backward from the meeting date** and names accountable owners at each milestone.
- **No fabricated benchmark data.** Any external benchmark or comparison is cited to a specific source or marked `needs-research`.

## Deliverables

- `00-context.md`
- `kpi-definitions.md`
- `01-ceo-letter.md`
- `02-kpi-dashboard.md`
- `03-financials.md`
- `04-strategic-deep-dive.md`
- `05-risks-decisions-consents.md`
- `06-appendices/` — with at least three appendix files inside.
- `07-distribution.md`
- `08-reconciliation-memo.md`
- `09-timeline.md`

## Extensions (optional)

- **The miss-quarter variant.** Rewrite the pack for a scenario where the same company misses ARR growth (2% MoM against 8% plan) and cash-out has advanced from month 20 to month 12. Add a decision item authorising a bridge-round exploration (per mod-109) and adjust the strategic deep-dive to cover the trajectory rather than segment focus. Practice the honest-signal discipline (chapter 8) inside the pack architecture.
- **The audit-committee packet.** For the same quarter, produce the audit-committee packet that precedes the quarterly full-board pack (per chapter 6). Assumes the Series-B company has an audit committee. Includes the quarter's financial-statement review, the auditor's status update (or the outside-auditor engagement letter if this is the first audit), a specific accounting-policy election memo, and the audit-committee-only executive-session agenda.
- **The addendum.** After the pack has been sent, a material customer loss occurs 48 hours before the meeting. Draft the addendum email to the board covering the loss, the impact on the current-quarter numbers, the updated forecast, and the mitigation. Practice the "addendum, not silent re-upload" pattern from chapter 2.
- **The pre-read call scripts.** For the two senior directors on the pre-read schedule, draft the CFO's specific opening for each call: what the CFO plans to raise, what the CFO expects the director to raise, and what specific commitment the CFO is trying to get before the meeting. Trains the pre-read call practice per chapter 2 and chapter 3.
- **The board-portal migration.** Draft the CFO's memo proposing a migration from the current PDF-attachment distribution to a dedicated board-portal (BoardEffect, Diligent, or OnBoard). Cover the cost, the workflow change, the audit-trail benefit, and the specific board-member preferences the migration has to accommodate.
