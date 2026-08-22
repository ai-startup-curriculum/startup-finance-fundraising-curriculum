# The Quarterly Board Pack — Architecture, Reconciliation, and the 72-Hour Rule

## Why this matters

The board pack is the single most consequential document the CFO produces in the ordinary quarterly cycle. It is the artifact the board reads to form its view of the company between meetings, the record the next lead investor will read during Series-B or Series-C diligence, the reference the audit committee (once formed) works from, and — in the moments that matter — the document a litigant, an acquirer, or an SEC examiner reads to assess whether the board was governing on real information or on aspirational marketing.

A board pack that reconciles cleanly to the general ledger, presents the KPI dashboard in the same numbers the operating team uses internally, frames financials in an actuals-vs.-budget-vs.-prior-quarter frame that a professional reader can process in ten minutes, calls out risks and decisions clearly, and lands 72 hours before the meeting is one of the strongest signals a CFO can send about the operating discipline of the company. A pack that arrives the morning of the meeting, drifts on KPI definitions from quarter to quarter, and buries the miss in a footnote is one of the strongest signals against.

This chapter installs the architecture, the reconciliation discipline, the 72-hour rule, and the failure modes that separate the two.

## The five-section architecture

A working reference board pack has five sections. Different companies rearrange the order, and some add or split sections, but the five below are the canonical set for a Series-A/B/C operating company.

**1. CEO letter (1-3 pages).** The CEO's narrative for the quarter. What happened, what the CEO's read on it is, what the next quarter's focus is, and what the CEO specifically wants from the board this meeting. Written by the CEO, edited by the CFO for consistency with the numbers. Sets the tone for the rest of the pack. If the CEO letter and the KPI dashboard tell different stories, the pack is broken and the meeting will surface it painfully.

**2. KPI dashboard (2-4 pages).** The 8-15 key operating metrics the board tracks. Every metric shows: current-quarter actual, current-quarter plan, prior-quarter actual, year-to-date actual, year-to-date plan, and (for the top few) a trailing-12-month chart. Every KPI must reconcile to a specific line or calculation in the financial model — the same actuals that produce the P&L produce the KPI dashboard. Definitional footnotes for every non-obvious metric.

**3. Financials — actuals vs. budget vs. prior quarter (4-8 pages).** The full P&L, balance sheet, and cash flow. Formatted as: current-quarter actual | current-quarter budget | variance | prior-quarter actual | quarter-over-quarter delta | full-year budget | full-year forecast. Variance callouts for anything above a materiality threshold. The CFO's narrative in a paragraph or two calling out the top three-to-five drivers of variance and the top one-or-two drivers of the forecast update.

**4. Strategic topic deep-dive (5-10 pages).** One topic per meeting. Selected in advance (typically at the last meeting's action-item review). Depth is real — the deep-dive is the section the board is expected to *spend actual time on* during the meeting. Common topics: the annual plan (usually the Q4 meeting), the go-to-market strategy update (once per year), a specific product-line or geographic-expansion memo, a major-hire memo, a competitive-landscape memo, an M&A opportunity memo, a fundraise-strategy memo, a customer-concentration memo. The deep-dive is what makes the board meeting worth the board's time; a pack without one is a pack that will produce a walk-through meeting.

**5. Risks / decisions / consents (2-4 pages).** The three-part governance list. Risks: the top three-to-five risks the board should be aware of, with the operating team's mitigation plan for each. Decisions: the specific decisions the board is being asked to make at this meeting (with reference to the underlying decision memo — see chapter 5). Consents: the specific written consents being requested for board sign-off (with reference to the underlying resolution — see chapter 4). No consent without a memo; no decision without an option set.

Some companies add:

- **Appendices** (cohort tables, hiring plan, functional-team updates, market data, competitor filings). Should be short and skimmable; the pack should be readable without them.
- **Prior-meeting action-item status** (the running register — see chapter 4). Sometimes a section, sometimes an appendix; either way the board reads it first to check what has happened since the last meeting.

The full reference pack is 20-40 pages for a Series-A company, 30-60 for a Series-B, 40-80 for a Series-C+. Longer than that and the 72-hour pre-read rule stops functioning; the board reads the first half and skims the second.

## The KPI dashboard — reconciliation is the discipline

The KPI dashboard is the section that most often breaks. The failure mode: the operating KPIs (as tracked by the go-to-market team, the product team, the marketing team) drift from the finance-team's numbers as reported in the financials, and the board pack contains two versions of the same underlying reality.

Examples of the drift:

- **ARR definition drift.** The GTM team defines ARR as booked contracts (including next-year commits); the finance team defines ARR as active-in-the-month recurring revenue extrapolated to annual; the board pack uses one number in the KPI dashboard and reports a different number in the P&L narrative.
- **Bookings vs. billings vs. revenue drift.** The pipeline dashboard says $2M closed-won in Q3; the financials show $1.4M of Q3 revenue; the CFO explains the difference verbally at the meeting because the pack does not.
- **Headcount drift.** The people team reports headcount as "62 as of quarter-end" using one definition (all W-2 employees, plus signed-not-started); the financial model computes headcount as "58" using a different definition (all salaried employees in payroll as of quarter-end); the pack cannot tell the reader which number is real.
- **Gross margin drift.** GTM reports "78% gross margin" as (Revenue - Direct COGS) / Revenue; finance reports "72% gross margin" as (Revenue - Direct COGS - Customer Support - Hosting) / Revenue; both are defensible; neither is the board's reference until the CFO installs one.
- **Cohort NRR drift.** Product analytics reports one NRR curve; the finance model computes a different NRR curve; the board pack picks one without explaining the choice.

The mechanic that closes the drift is the **KPI definition table**. Once, at the start of the year, the CFO publishes the definitional table: for every board-tracked KPI, the exact calculation, the source of the underlying data, the update cadence, and the responsible owner. That table is republished in the appendix of every board pack for the year. Definitional changes require a memo (see chapter 5) and are approved at a board meeting before they take effect.

The second mechanic is the **month-end close reconciliation**. Every KPI in the board pack reconciles to the same actuals used for the financials, which reconcile to the same actuals used for the general ledger, which are the actuals the auditor (once engaged) will confirm. One set of numbers. The finance team's close protocol (from mod-101 and mod-111) is what makes that one set possible. A CFO who cannot answer "does the ARR on this KPI slide reconcile to the deferred-revenue balance on the balance sheet" is a CFO whose pack will lose credibility the first time a board member asks that question.

## Financials — the actuals-vs.-budget-vs.-prior-quarter format

The financials section is boring by design. It presents the three statements (P&L, balance sheet, cash flow) in a format the reader can scan for variance and trend, and it lets the strategic deep-dive be the section that consumes actual attention.

**The columns.** For each line, the pack presents: current-quarter actual, current-quarter budget, variance (dollar and percent), prior-quarter actual, quarter-over-quarter delta (dollar and percent), full-year actual-to-date, full-year budget, full-year updated forecast. That is eight columns; some packs collapse it to six by dropping the QoQ deltas. Eight is the reference; fewer is acceptable if the pack is readable.

**Variance callouts.** Every line with variance above a materiality threshold (a common heuristic is ±10% of the budget line or ±$100K absolute, whichever is greater) gets a callout — a footnote number tied to a narrative paragraph. The reader can trace every material variance from the number to the cause without asking the CFO at the meeting.

**The forecast update.** The full-year forecast column is updated at every quarterly pack. If the current-quarter miss propagates to a full-year miss, the forecast column shows it, and the CFO's narrative section addresses it. A forecast that never updates from the original budget is a forecast the board cannot trust.

**The narrative section.** One paragraph per statement (P&L, balance sheet, cash flow), naming the top three-to-five drivers of variance and the top one-or-two drivers of the forecast update. Not a walkthrough of every line — a synthesis. The narrative earns its space by being interpretive; the tables carry the data.

**Cash and runway.** The cash-flow statement and the runway model get their own page or half-page callout. Current cash, monthly burn (trailing three-month average), forward-looking runway on the current forecast, and (per mod-109 chapter 1) the distance from each of the 12 / 9 / 6-month triggers. This is the page the board opens first if the runway is short; make it easy to find.

**Balance sheet — the section boards under-read.** The balance sheet section is the section most often skipped by board members who are not CFOs by background. The CFO's job is to call out the two-to-three balance-sheet items that matter: AR aging (if there is customer-concentration or collection risk), deferred revenue (which reconciles to the ARR calculation), inventory (if there is any), and the debt / warrant / preference balances (if there is venture debt or a bridge outstanding). Everything else in the balance sheet can be skimmed.

## The strategic deep-dive

The strategic deep-dive is the section that most differentiates a governance-grade pack from a walk-through pack. It is one topic. It is prepared in advance. It is real.

**Selection.** The deep-dive topic for the meeting is agreed at the *prior* board meeting, typically in the last 10 minutes when the CFO reviews the calendar for the next quarter. That gives the CFO 90 days to prepare the memo — which is what makes the deep-dive real rather than a rushed appendix. Common topic rotation for a Series-B company:

- **Q1 meeting** (annual plan quarter) — the annual plan itself. The deep-dive is the plan memo: the milestone bar, the target-KPI trajectory, the hiring plan, the cash plan, the sensitivity heatmap, the fundraise-readiness projection.
- **Q2 meeting** — go-to-market strategy update. Segment focus, pricing, sales-team design, marketing mix.
- **Q3 meeting** — product / roadmap deep-dive. What is being built, what customer signal drives it, what the competitive frame is.
- **Q4 meeting** — one of: fundraise-strategy memo (if raising in the next six months), an M&A opportunity, a specific geographic or product-line expansion memo, or a talent / org-design memo.

Other patterns exist; the point is that the CFO owns the calendar and the topic rotation, and the topic is selected far enough in advance to be prepared properly.

**Structure.** The deep-dive is typically 5-10 pages: an executive summary (one page), the context (one to two pages), the specific analysis or option set (two to four pages), the recommendation (one page), and the risks and open questions (one page). If the deep-dive is a decision item (see chapter 5), the same memo also serves as the board decision memo.

**Presentation.** Because the pack lands 72 hours before the meeting, the deep-dive is *read* before the meeting. The 60-minute deep-dive slot in the meeting is not a presentation of the memo; it is a discussion of the memo. The CFO or CEO opens with a two-to-three-minute framing ("what has changed in your understanding since the pack landed, and what are the two-or-three specific questions we should spend the hour on"), and the discussion proceeds from there.

**One deep-dive, not three.** The failure mode is to attempt three deep-dives in one meeting. The board attention budget for a real deep-dive is one topic per meeting. Attempting three produces a superficial pass on all three and no decision on any of them.

## Risks, decisions, and consents

The three-part governance list is a specific, formal section, not a "any other business" grab-bag.

**Risks.** Three-to-five bulleted risks, each with: the specific risk, the operating team's current assessment (probability × impact, or qualitative equivalent), the mitigation plan, and the trigger that would escalate the risk to a decision item. Risks that have been on the list for three consecutive meetings without escalation should be either escalated or removed; a chronic-risk item that never moves is a signal the risk list is being used as a hedge, not a governance tool.

**Decisions.** Each decision item cross-references a decision memo (chapter 5). The pack does not embed the memo in this section — the memo is a separate section or an appendix — but the risks / decisions / consents section names the decision, the memo reference, and the specific ask ("we are seeking board approval for the recommended option in the [Series-B fundraise decision memo, appendix C]"). If the pack contains a decision item without a memo, the pack is not ready to ship. Send the decision-required memo late (with an addendum to the pack) rather than embedding an unstructured decision request in the risks list.

**Consents.** Each consent item cross-references the specific resolution (chapter 4). The pack names the consent, the specific corporate action being authorised, and the standard-vs.-non-standard status (the ordinary quarterly consents — 409A refresh approval, option grant approvals, prior-quarter minutes approval — are labelled as ordinary; a non-standard consent like a debt-facility authorisation is called out).

The mechanic here is that **every consent is preceded by a decision memo or a resolution draft in the same pack**. The board does not vote in the meeting on a consent it has not seen in writing 72 hours before the meeting. Exception: at the meeting a specific consent-required item can emerge from the discussion, and the board can vote to authorise a written consent to circulate after the meeting once the CFO has drafted the resolution. That is a documented pattern; a "surprise consent" at the meeting is not.

## The 72-hour rule

The pack lands in the board's inbox 72 hours before the meeting starts. Not 24. Not 4. Not "the morning of." 72 hours (three calendar days) is the industry-standard pre-read window and is the mechanic that lets the meeting spend its time on discussion rather than presentation.

**Why 72 hours specifically.** Board members read the pack over a two-to-four hour window, and they read it either the night before the meeting or over the morning of. 72 hours gives them a weekend day, or a full workday plus a night, to read the pack, form questions, and send those questions to the CFO / CEO in advance. Shorter than 72 hours and they read while the meeting is starting — which converts the meeting into a walk-through. Longer than 72 hours and the numbers get stale between pack send and meeting.

**What "landing" means.** The pack lands in every board member's inbox at the same time, with a subject line that identifies the meeting date, and with the pack attached (or with a direct link to the pack in a specific data-room location). It does not land as "the KPI slides are in this file, the financials are in this file, the CEO letter is in this email body." Assembly is a job the CFO does before send, not the board members' job on receipt.

**The pre-read conversation.** Between pack send and meeting, a common pattern is a 15-30 minute pre-read call with each of the two-or-three most senior board members (typically the lead investor, the founder-CEO-adjacent independent, and the audit-committee chair once formed). The purpose: surface the board member's questions in advance so the meeting agenda can be adjusted, and give the board member a chance to raise a concern in a private conversation before doing so in the meeting. Not required, and not universally practiced, but common enough that a CFO who does *not* run pre-read calls should have a specific reason not to.

**The 72-hour rule interacts with the finance-team close.** For a quarterly pack, the finance team has to close the quarter, produce the actuals, reconcile the KPIs to the actuals, update the forecast, draft the narrative, and package the pack — all before the 72-hour mark. Working backward from a typical Q3 meeting on October 25, the pack sends October 22, which means the pack is package-ready October 21, which means the quarter's actuals are close-ready by October 15-18, which means the finance team's close protocol is a 12-15 business-day cycle at minimum for the quarter-end. A slower close pushes the meeting later or breaks the 72-hour rule; either way, the close protocol (mod-111) is the upstream constraint.

**Exceptions.** Emergency board meetings (a specific incident, a term-sheet response) run on a compressed timeline and the 72-hour rule may not apply. Everyone treats those as exceptions and adjusts expectations accordingly.

## Preparation timeline

Working backward from the meeting, the reference preparation timeline for a quarterly pack:

- **Day M-7 to M-90 (from prior meeting):** the strategic deep-dive topic is agreed at the prior meeting. The CFO / CEO develop the memo over the quarter.
- **Day M-30:** finance team confirms close-cycle timing; identifies material variances likely to be in the pack; the CFO drafts the KPI-definition addendum if any definitions have changed.
- **Day M-20:** the CEO drafts the CEO letter outline.
- **Day M-15 to M-10:** the finance team closes the quarter. Actuals reconcile to GL. Variance callouts drafted. KPIs recompute.
- **Day M-10 to M-7:** the pack is assembled. Deep-dive memo finalises. Decision memos and consent resolutions are drafted. Risks list is refreshed.
- **Day M-7 to M-4:** CEO and CFO review; the CEO letter is finalised; the pack is polished.
- **Day M-4 to M-3:** pack lands in board inboxes. 72-hour window opens.
- **Day M-3 to M-1:** pre-read calls with senior board members. Agenda adjusted based on questions raised.
- **Day M:** meeting.
- **Day M+2 to M+5:** minutes drafted; action-item register updated; consent resolutions circulated for signature; strategic-topic memo for next meeting agreed.

The CFO owns this calendar. A CFO who cannot produce a pack on this timeline needs to fix the upstream close cycle before the meeting cadence can improve.

## Pack format

Traditional format is a PDF assembled from a slide deck (Google Slides or PowerPoint) with embedded tables for the financials. Some companies have migrated to Notion pages, Docsend links, or dedicated board-portal software (BoardEffect, Diligent, OnBoard). The format matters less than the discipline; two guardrails:

- **The pack is downloadable and printable.** Some board members read on paper. Some read on tablets while offline (an airplane, a train). A pack that requires live internet to view is a pack a fraction of the board cannot read.
- **The pack is version-controlled.** Once sent, the pack does not change without a version note. If a material error is found after send, an addendum email documents the change; the pack itself is not silently re-uploaded.

## Reconciliation — the CFO's discipline

The single technical discipline that separates a governance-grade pack from a marketing pack is **reconciliation**. Every number in the pack traces to a specific source:

- **ARR** → the finance team's ARR calculation → deferred revenue on the balance sheet + current-period recognised revenue for annual contracts.
- **Gross margin** → COGS in the P&L (using the definition in the KPI-definition table).
- **Cash** → the bank statement, tied to the balance sheet cash line.
- **Runway** → the driver-based model, using the current-quarter actuals as the starting point.
- **Headcount** → the payroll system as of quarter-end, using the definition in the KPI-definition table.
- **CAC / payback** → the S&M spend divided by net-new-customers or net-new-ARR, per the definition in the KPI-definition table.
- **NRR** → the cohort calculation using the finance-team's customer master, not the go-to-market team's separate CRM view.

Reconciliation gets tested every time a board member asks "where does that number come from" — a question that comes up in most board meetings at some point. A CFO who can answer immediately and precisely earns a level of trust that a CFO who has to check and come back with the number simply does not.

## Common CFO-side failure modes

- **KPI drift across quarters.** The GTM team's number and the finance team's number diverge, and the board pack presents both without noting the difference.
- **Definitional changes without notice.** ARR definition changes between Q2 and Q3, and the Q3 pack shows a "step" the reader assumes is real performance.
- **Missing the 72-hour rule.** Pack lands the morning of the meeting; meeting becomes a walk-through.
- **Three deep-dives in one meeting.** All three superficial; none decided.
- **No decision memo for a decision item.** The board is asked to vote on a decision they have not seen in writing before the meeting.
- **Chronic risks that never escalate.** The risk list becomes a hedge, not a governance tool.
- **No pre-read calls with senior board members.** The meeting surprises the CFO with a question that could have been surfaced in advance.
- **The pack is not version-controlled.** A silent re-upload after send erodes trust.
- **The finance-team close cycle is too slow to support the 72-hour rule.** The pack is late every quarter; the underlying operational fix (mod-111) is deferred.
- **The pack is beautifully designed but not reconcilable.** Beautiful is a bonus; reconcilable is the requirement.

## What good looks like

A CFO who has this material installed:

- Ships a five-section pack (CEO letter, KPI dashboard, financials, strategic deep-dive, risks / decisions / consents) at every quarterly meeting.
- Maintains a KPI-definition table published at the start of the year and re-referenced in every pack.
- Reconciles every KPI to the general-ledger actuals; can answer "where does this number come from" instantly.
- Lands the pack 72 hours before the meeting, without exception.
- Runs pre-read calls with the two-or-three most senior board members between pack send and meeting.
- Rotates the strategic deep-dive topic on an annual cycle agreed at the prior meeting.
- Cross-references every decision item to a specific decision memo (chapter 5), and every consent item to a specific resolution (chapter 4).
- Runs an actuals-vs.-budget-vs.-prior-quarter financials section with a materiality-threshold variance callout convention.
- Refreshes the full-year forecast at every quarter, and calls out the drivers of the update.
- Owns the pack-preparation calendar working backward from the meeting date.

## Summary

- The board pack is the highest-consequence quarterly artifact the CFO produces. Its five sections are CEO letter, KPI dashboard, financials, strategic deep-dive, and risks / decisions / consents.
- The KPI dashboard reconciles to the same actuals as the financials, which reconcile to the general ledger. Definitional drift and unreconciled KPIs destroy the pack's credibility.
- The financials section is boring by design: actuals vs. budget vs. prior quarter, with variance callouts above a materiality threshold and a narrative paragraph per statement.
- The strategic deep-dive is one topic per meeting, agreed at the prior meeting, prepared over 90 days, and *discussed* rather than presented at the meeting.
- The risks / decisions / consents section names the three-part governance list. Every decision cross-references a memo; every consent cross-references a resolution.
- The 72-hour pre-read rule lets the meeting spend its time on discussion rather than presentation. Missing it is the fastest way to convert the meeting into a walk-through.
- The finance-team close cycle is the upstream constraint on the 72-hour rule. A slow close breaks the whole cadence.
- Reconciliation is the technical discipline that separates a governance-grade pack from a marketing pack. Every number traces to a specific source.

Chapter 3 turns from the pack itself to the meeting the pack enables — the pre-read → 30 / 60 / 30 → executive session structure, and the reasons the "walk through the pack" meeting is a governance-failure pattern.
