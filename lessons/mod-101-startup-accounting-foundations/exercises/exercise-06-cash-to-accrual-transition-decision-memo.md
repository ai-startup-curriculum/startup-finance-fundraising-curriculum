# Exercise 06 — Cash-to-Accrual Transition Decision Memo

**Estimated time:** ~2 hours
**Prerequisites:** Chapter 6 (cash-to-accrual transition) and chapter 7 (guidance stack).

## Problem statement

Author the CFO-authored decision memo that recommends whether — and how — a specific startup should transition from cash to accrual basis accounting. The memo will be delivered to the CEO and lead board investor for concurrence and will drive the engagement of an outsourced-accounting firm or auditor.

The memo is a structured governance artefact, not a research paper. It should be dense, cite specific facts, and end with an unambiguous recommendation and a calendar.

## Scenario — pick one from the profiles below (or supply your own)

**Profile A — early Series-A SaaS, no imminent audit.** SaaS company, ~$3M ARR, 40% annual-prepay concentration, ~$8M cash on balance sheet post-Series-A close six months ago. Series-A term sheet included information-rights language requiring "quarterly financial statements prepared in accordance with US GAAP." Company is currently on cash basis for both management reporting and tax. Board has not formally requested accrual reporting but the lead investor asked "why is your monthly update reporting cash-basis revenue?" at the last board meeting.

**Profile B — Series-B pre-audit prep.** SaaS company, ~$15M ARR, growing 100% YoY, ~$40M cash post-Series-B close nine months ago. Board has resolved to run the first outsourced audit for fiscal year N (starts in six months). Company has been running dual-basis (accrual for management reporting, cash for tax) since Series-A but the accrual books have never been audited, opening balances were an approximation, and the deferred-revenue schedule has never been fully reconstructed contract-by-contract.

**Profile C — approaching §448(c) threshold.** SaaS company, ~$28M current-year revenue, three-year trailing average ~$22M. Currently on cash basis for tax and accrual for management reporting. Company's projections show current-year revenue at $35M and trailing three-year average crossing the §448(c) threshold in fiscal year N+1. No audit engagement pending.

**Profile D — IPO-track Series-C.** SaaS company, ~$60M ARR, Series-C closed, planning dual-track (IPO + strategic sale option) at fiscal year N+2. Currently accrual for management reporting, cash for tax. Has never had an outsourced audit. S-1 filing target is fiscal year N+2 Q3, which will require audited financials for FY N and FY N+1.

## Requirements

Produce a decision memo with the following sections. Target length: 3-5 pages. This is a CFO-to-CEO/board document; write it accordingly.

1. **Executive summary (max 1/2 page).** The recommendation in the first two sentences, the timeline in the third, and the cost estimate in the fourth. A busy CEO should not need to read past the executive summary to get the answer.

2. **Current state.** Where the company is today. Basis of accounting for management reporting and for tax filing. The finance-ops stack. The specific accrual gaps in current reporting (deferred revenue accuracy, opening balance vintage, revenue-recognition policy memo state, etc.).

3. **Triggers assessed.** Walk each of the four triggers from chapter 6:
   - Audit requirement (is one engaged, planned, requested)
   - Tax-code change at scale (§448(c) threshold — current position, projected crossing date, cite the threshold)
   - Board or lead-investor request (contractual clauses in term sheets, informal requests)
   - IPO / dual-track prep (planned filing date, required comparative periods)

   For each, state whether it is fired, approaching, or not applicable, and cite the specific fact.

4. **Options considered.** At least three:
   - Option 1: Status quo (stay on current basis; implications)
   - Option 2: Move management reporting to accrual, keep cash for tax (implications; the most common intermediate step)
   - Option 3: Full transition including tax method change (implications; the endpoint if any trigger has fired)

   For each option, state the pros, cons, cost, and time required.

5. **Recommendation.** One of the options, with the reasoning tied back to the specific triggers assessed. If the recommendation involves multiple phases (e.g., "management reporting now, tax method change on §448(c) crossing in year N+2"), phase them explicitly.

6. **Implementation plan.** A calendar for each step:
   - Opening-balance-sheet restatement (with date)
   - Comparative-period restatement (if audit-driven — with the periods and the completion date)
   - First accrual close cycle (with date)
   - Revenue-recognition policy memo (draft date, review by CPA, board acknowledgment)
   - Auditor / CPA firm engagement (RFP / selection, engagement letter, pre-audit fieldwork)
   - Form 3115 filing (if applicable, with target filing date)
   - Communication plan (board notification, investor-update disclosure, employee-facing changes to financial reporting)

7. **Cost estimate.** Rough estimates in dollars (or as a percentage of current finance-team run-rate) for:
   - Outsourced-accounting firm time to restate opening balances and comparative periods
   - Auditor pre-audit engagement (if audit-driven)
   - Tax-return work if changing methods
   - Software / tooling changes (e.g., NetSuite adoption if driven by the same trigger)

   Cite ranges rather than point estimates; note the ranges are drawn from practitioner content and should be validated with the specific firms shortlisted.

8. **Risks and mitigations.** Named risks:
   - Opening-balance error (mitigation: engage auditor early)
   - Deferred-revenue misstatement (mitigation: reconstruct contract-by-contract; do not estimate)
   - Auditor rejection of the policy memo (mitigation: pre-review policy with CPA)
   - Tax-filing timing missed (mitigation: coordinate Form 3115 with year-end close)
   - Board / investor disclosure friction (mitigation: proactive communication)

9. **Ask.** The specific decision or approval requested from the CEO / board and the date needed by. Not "please review" — "approve the recommendation and the implementation calendar by [date] so we can send the auditor RFP on [date]".

## Starter guidance

- Read chapter 6 and chapter 7 first. The memo's authority comes from citing the specific ASC, IRC, and IRS-publication sources for each judgement.
- Do not invent facts about the profile you pick. If the profile does not tell you the answer to a question (e.g., "is there a state-tax nexus complication?"), state the assumption you are making and flag it as "verify with tax counsel."
- The recommendation is the point of the memo. Every other section supports the recommendation. If the CEO reads only the executive summary and the recommendation, they should have the answer.
- Cost estimates should be honest. If you do not know the range, say so and cite a source you would use to validate it (e.g., "cost estimate to be finalised on receipt of proposals from [Kruze / Pilot / a Big Four firm]"). Do not invent a number.
- If the profile fires a required trigger (audit, §448(c), IPO), the recommendation is *when* to move, not *whether* to move. Do not spend paragraphs debating "whether" when the trigger has fired.

## Acceptance criteria

- **All four triggers explicitly assessed.** For the chosen profile, each of audit / §448(c) / board / IPO is called out and classified as fired / approaching / not applicable.
- **Recommendation is unambiguous.** One option, not "some combination of."
- **Implementation plan is dated.** Every step has a target date, even if approximate. "Q2 FY26" is acceptable; "later this year" is not.
- **Costs are rangebounded and sourced.** Point estimates without source are not acceptable.
- **Authoritative citations for judgements.** ASC 606, IRC §448, IRS Publication 538 cited where they drive a conclusion.
- **The memo would survive board reading.** A board member with no context should understand the recommendation and the rationale in one read.
- **Ask is specific.** A named decision, a named decider, a named date.

## Deliverables

- The decision memo (Markdown or PDF), 3-5 pages, following the section structure above.
- A one-slide summary version suitable for inclusion in a board pack (title, current state, recommendation, timeline, cost, ask).

## Extensions (optional)

- After finishing the memo, produce a shadow memo for a different profile from the list. Note which sections change materially and which are stable — the pattern-transferable content vs. the profile-specific content.
- Draft the board consent language that would formally record the board's approval of the transition.
- Draft the investor-update paragraph that would disclose the change of method to existing investors (or the deck slide that would disclose it in the next investor materials).
