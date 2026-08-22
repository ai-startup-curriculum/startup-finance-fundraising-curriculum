# Exercise 05 — 409A Methodology and Refresh-Cadence Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 5 (409A methodology, FMV, and refresh cadence).

## Problem statement

For a hypothetical (or anonymised real) startup over an 18-24 month window from Series-A close through Series-B negotiation, produce a **409A refresh calendar** listing every 409A appraisal event, whether it was scheduled or triggered, and the specific trigger. For a specific 409A report received at one of those events, produce a **critical read** — a memo that identifies the methodology, questions the assumptions, and either accepts the number or requests revisions. Finally, author a **grant timing decision** for a specific hire whose offer is pending, deciding whether to grant now against the current 409A or wait for a fresh appraisal that is due imminently.

The exercise installs the three practical CFO decisions around 409A: *when do I refresh*, *how do I read the report I receive*, and *how do I sequence grants against the refresh cycle*.

## Scenario — build your own

Design a company timeline with the following events spread across 18-24 months. Anchor to specific dates so the calendar has real structure.

- **Month 0:** Series-A closes at $30M pre / $10M invested / $40M post. Grants are pending for two new hires (a Staff engineer and a VP Sales) once the 409A is in.
- **Month 1:** First post-Series-A 409A appraisal received.
- **Month 8:** Company signs its largest customer deal ever — 3x the next-largest customer, with a $2M annual contract. Debate: is this a material event?
- **Month 10:** Secondary tender offer proposal from an existing investor to buy 5% of the fully-diluted from employees at a per-share price 40% higher than the last 409A. Debate: is this a material event? Should the tender go forward before or after a fresh 409A?
- **Month 13:** Annual 409A refresh comes due (approx. 12 months after Month 1).
- **Month 15:** Preliminary Series-B term sheet signed with a lead investor at $80M pre / $20M invested / $100M post. Debate: is this a material event? Should grants be paused between signing and closing?
- **Month 17:** Series-B closes.
- **Month 18:** Fresh post-Series-B 409A appraisal received. Analyse the methodology.

You may modify the specific dates but keep the event sequence roughly similar.

## Requirements

Produce a spreadsheet or notebook and a memo package with the following:

1. **409A refresh calendar.** A table with columns: date, event, trigger type (scheduled 12-month refresh / new priced round / secondary tender / material projection change / other), whether a fresh 409A was ordered, and the rationale for the decision. Cover every event from Month 0 through Month 18.
2. **The safe-harbor status column.** For each grant date on the calendar, name which 409A report the grant would be issued against (i.e., which report provides the safe-harbor protection), and confirm the grant is within 12 months and no material event has intervened.
3. **The Month-13 report critical-read memo (1-2 pages).** The 409A appraiser has produced a report with the following characteristics (adapt to your scenario or invent plausible numbers):
   - Common FMV: $2.10 per share (up from $1.20 at the Month-1 report).
   - Methodology weighting: 40% backsolve from the Series-A round (18 months old at the report date), 40% public-comparables (2 SaaS comparables, EV/Revenue multiple applied to trailing revenue), 20% DCF (against the company's most recent forecast).
   - DLOM applied: 25%.
   - Volatility used in the OPM allocation: 55%.
   Critical-read the report. Questions to address in the memo:
   - Is the backsolve weighting defensible with an 18-month-old priced round? What should the appraiser have done differently?
   - Do the two public comparables look right for the company (name specific reasonable comparables for your scenario)?
   - Is the DLOM defensible for a Series-A-stage company that is well into its Series-B fundraise?
   - Does the common-to-preferred ratio (implied by the FMV vs. the current 409A-modelled preferred value) look right for a company at this stage?
   - Would you accept the report, request revisions, or seek a second-opinion appraisal?
4. **Grant-timing decision memo (1-page).** A senior engineer hire has accepted a written offer with a specified grant size in shares, contingent on closing paperwork. The offer letter says the strike price will be the FMV per the "most recent 409A appraisal" on the grant date. The current situation:
   - The Month-13 refresh is in-hand at $2.10/share.
   - The Series-B is under active negotiation, with a signed LOI expected in ~30 days at a valuation that will push the backsolve materially higher.
   - The company culture is pro-employee (i.e., a lower strike is better for the hire).
   - The GC has signalled the LOI is likely a material event that will trigger a fresh 409A.
   Decide: grant now at $2.10, or wait for the LOI + fresh 409A? Consider the employee's outcome, the company's 409A defensibility, the recruiting-signal risk of a delayed grant, and the equal-treatment implications (is the company also delaying other grants?).
5. **Corporate-record entries.** For each fresh 409A ordered in the calendar, sketch the specific board-consent language that would authorise the appraisal and, subsequently, the board-consent language that would authorise the next batch of option grants at the new FMV. Include the specific report reference (e.g., "Aranca 409A Report dated 15 March 2027, common FMV $2.10 per share") that the consent cites.

## Starter guidance

- **The calendar is where most CFOs get 409A wrong.** Not by failing to order the appraisal — by ordering it after a material event but continuing to issue grants against the stale report between the event and the new report's receipt. The safe-harbor status column is what surfaces the gap.
- **Any priced round is a material event.** Also secondary transactions above the current FMV. Also large customer wins that materially move the projections. Also LOIs / pending acquisitions.
- **The critical-read is where the CFO earns their fee.** The appraiser is not adversarial, but their default methodology weighting is production-line and may not fit the company's specific circumstances. Push back on backsolve with a stale round; push back on DLOM that doesn't reflect current secondary liquidity; push back on comparables that don't match business model.
- **The grant-timing decision has no universally right answer.** Reasonable CFOs decide differently. What matters is that the decision is *made* with the trade-offs surfaced, and documented in a memo the board and GC would accept.
- **The corporate-record entries are the diligence artefact.** A board consent that just says "grant options at fair market value" without a specific 409A citation is a diligence red flag.

## Acceptance criteria

- **The refresh calendar covers every event** and correctly identifies material vs. non-material.
- **The safe-harbor status column** proves that every hypothetical grant date is protected by a 409A report ≤ 12 months old with no intervening material event.
- **The critical-read memo asks specific methodology questions** on backsolve, DLOM, comparables, common-to-preferred ratio, and volatility — not generic observations.
- **The critical-read memo makes a recommendation** — accept / request revision / second opinion — with a specific rationale.
- **The grant-timing memo names the specific trade-offs** (employee benefit, company defensibility, recruiting signal, equal-treatment) and makes a decision with rationale.
- **The corporate-record language** cites the 409A report by name / date / per-share value in each grant-authorising consent.

## Deliverables

- The refresh calendar spreadsheet or table.
- The 1-2-page critical-read memo (Markdown or PDF).
- The 1-page grant-timing decision memo (Markdown or PDF).
- The corporate-record consent language sketches (may be a subsection of the other deliverables).

## Extensions (optional)

- Model a **repricing event.** In a follow-on scenario, the Series-B doesn't close and the company's FMV falls (Month-24 refresh reads $1.10, below the Month-13 refresh of $2.10). The board considers a repricing to reduce outstanding grants' strikes. Author the board memo recommending for or against the repricing, addressing ASC 718 modification accounting and cultural implications.
- Interview a 409A appraiser (or read a published 409A methodology piece from Aranca / Scalar / Preferred Return / a cap-table platform) and compare their methodology to what your critical-read memo asked for.
- Extend the calendar to model the pre-IPO transition: Month 30 the company files an S-1 draft; Month 33 IPO priced. Show how the 409A discipline transitions into '34-Act-reporting FMV.
- Add a **secondary-tender-offer design** exercise: given a proposed tender at 40% above current FMV, design the tender rules (eligibility, cap on participation, pricing methodology, communication) to minimise the 409A impact on future grants while still delivering employee liquidity.
