# The Cash-to-Accrual Transition — Required vs. Elective Triggers

## Why this matters

Most startups begin on cash basis. It is simple, it is permitted for federal tax purposes for small taxpayers, and QBO / Xero can be configured for cash-basis bookkeeping in a few clicks. At some point, every startup that is going to raise institutional capital or clear an audit has to move to accrual. The move is *not* mechanical — it is a governance decision with tax consequences, retroactive-restatement implications, an auditor letter, and, at scale, an IRS Form 3115 filing to change accounting methods.

This chapter's job is to make explicit *when* the move is required (not the CFO's option to defer) and *when* it is elective (the CFO's judgement, usually driven by an investor or board request ahead of the requirement). It is not a tax opinion; the specifics of any single company's tax and financial-reporting posture should be verified with the company's CPA or tax counsel. This chapter installs the decision framework.

## The four canonical triggers

### 1. Audit requirement

An audit conducted under US Generally Accepted Auditing Standards (GAAS) by a CPA firm produces an opinion on financial statements prepared in accordance with US GAAP. US GAAP presumes accrual accounting. The moment a startup contracts for its first outsourced audit — typically Series-B triggered by a board request or as pre-IPO preparation (see mod-111) — the audited financials must be accrual-basis GAAP.

Two nuances:

- A **review** or **compilation** engagement (not an audit) may be issued on a special-purpose framework such as the AICPA's *Financial Reporting Framework for Small- and Medium-Sized Entities* (FRF for SMEs) or on cash-basis / modified-cash-basis. These are useful intermediate options at Series-A when a lender or investor wants CPA involvement but the full audit is not warranted. Reviews / compilations are *not* substitutes for a GAAP audit in a Series-B or pre-IPO context.
- The **two-year comparative** requirement — an IPO S-1 filing requires audited financial statements for the two most recent fiscal years (three for larger accelerated filers, subject to specific SEC rules and current-year JOBS-Act EGC accommodations). This means audit-readiness in year N requires accrual-basis GAAP financials for year N-1 and year N-2. The clock starts earlier than the audit itself. <!-- needs-research: verify current SEC S-1 audited-period requirement and any EGC accommodations under current JOBS Act rules -->

**Trigger classification:** Required at the moment the audit engagement letter is signed. In practice, the move should be completed at least one full fiscal quarter before the audit begins so the auditors have clean accrual books to work with from the start.

### 2. Tax-code change at scale

The Internal Revenue Code permits certain small taxpayers to use cash-basis accounting for federal income-tax purposes. The primary provision is IRC §448, which prohibits C corporations, partnerships with C-corporation partners, and tax shelters from using cash-basis, subject to specified exceptions. The most important exception for startups is the **small-business exception** under §448(c) — taxpayers whose average annual gross receipts over the prior three tax years do not exceed a specified threshold may use cash-basis regardless of entity type.

The threshold was $25 million at the time of the Tax Cuts and Jobs Act (TCJA, effective 2018) and is adjusted annually for inflation. <!-- needs-research: cite current-year inflation-adjusted §448(c) gross-receipts threshold and the effective year -->

When a taxpayer crosses the threshold — a growing SaaS startup with $30M+ trailing three-year average gross receipts — cash-basis is no longer permitted for federal tax purposes. The taxpayer must change accounting methods, typically by filing Form 3115 (*Application for Change in Accounting Method*) and applying a §481(a) adjustment that spreads the cumulative catch-up (the amount that would have been recognised under accrual but was not under cash) over four years for positive adjustments.

Two related provisions matter:

- **IRC §471(c)** — the small-business exception to the inventory-accounting rules. Small taxpayers under the §448(c) threshold can elect not to account for inventory under §471. This is less relevant for pure SaaS but matters for hardware / marketplace / physical-goods startups.
- **IRC §263A** — the uniform capitalisation rules (UNICAP) require certain costs to be capitalised into inventory. Same §448(c) small-business exception applies.

**Trigger classification:** Required once the §448(c) gross-receipts threshold is crossed. The company has until the due date of the tax return for the year of the change to file Form 3115.

### 3. Board or lead-investor request

A term sheet or investor rights agreement (IRA) at Series-A or Series-B commonly includes an information rights clause requiring monthly or quarterly financial statements prepared in accordance with US GAAP. The moment such a clause is agreed, the company is contractually committed to accrual reporting on the specified cadence.

Even without a contractual clause, a lead investor or independent board member can request GAAP-basis reporting starting at any point after the round closes. The request is almost universally granted; the political cost of refusing accrual reporting after taking institutional capital is severe.

**Trigger classification:** Elective in the sense that the company chose to accept the term / grant the request — but non-negotiable once accepted. In practice, most institutional Series-A term sheets carry information rights that require accrual GAAP.

### 4. IPO prep / dual-track

An IPO on a US exchange requires audited GAAP financial statements for the periods specified by SEC S-1 requirements. A dual-track process (IPO + strategic sale in parallel) requires the same. The financial-close discipline required to hit a public-company reporting timeline (10-Q within 40-45 days of quarter-end for accelerated filers, 10-K within 60-75 days of year-end) is materially higher than the accrual-basis close a Series-B private company runs.

For a company on cash basis at the start of IPO prep, the move to accrual should be complete two to three fiscal years before the S-1 filing so that the required comparative audited periods are all accrual and there is no accounting-method-change disclosure to explain in the MD&A.

**Trigger classification:** Required once IPO or dual-track process is planned. Realistically, if the move has not happened by Series-B, the audit + IPO-prep sequence forces it at that point.

## When the move is elective — and why to do it anyway

Even before any of the four triggers fires, most CFOs run parallel accrual books from the moment the company has its first material deferred-revenue balance (typically the first annual-prepay customer). The reasons:

- **The board / investors will ask.** A monthly update at Series-A that quotes accrual revenue vs. one that quotes cash-basis revenue tells a very different story about growth trajectory. Being consistent from month one avoids restatement conversations later.
- **Internal-decision quality.** Cash-basis P&L in a subscription business misrepresents the unit economics. CAC payback, LTV, and gross margin computed on cash-basis revenue are wrong. mod-102 assumes accrual revenue as input.
- **Model reconciliation.** The three-statement model (mod-103) is fundamentally an accrual construction. A cash-basis P&L cannot be reconciled to a balance sheet and cash-flow statement in a meaningful way; there is no working-capital section to reconcile.
- **Preparing for audit.** The first-time audit is materially harder if the two comparative periods have to be reconstructed from cash-basis records. Auditors will charge for the extra work.

The typical pattern for a well-run startup: cash-basis for tax filing (until §448(c) forces the change), accrual-basis for management reporting and investor reporting from the first annual-prepay contract. QBO and Xero support this dual-basis reporting; NetSuite (typically adopted at Series-B) is accrual-native.

## The mechanics of the transition

The transition from cash to accrual involves several concrete steps:

1. **Restate opening balance sheet.** The opening equity is adjusted for the cumulative effect of moving from cash to accrual — cumulative AR added (revenue earned but not collected under cash), cumulative deferred revenue added (cash collected in advance of delivery), cumulative AP added (expenses incurred but not paid), cumulative prepaid expenses added. The net adjustment hits retained earnings / accumulated deficit as of the transition date.
2. **Restate comparative periods.** If the audit requires two comparative years, both prior years must be restated to accrual. This is where the audit prep cost gets real; every customer contract, every invoice, and every vendor invoice for the prior periods needs the accrual entries reconstructed.
3. **Book ongoing accrual entries.** Every new customer invoice creates AR and deferred revenue; every new vendor invoice creates AP; every payroll cycle creates accrued wages. Month-end close now includes accrual adjustments for the last few days of the month.
4. **File Form 3115 (if required).** For a tax-driven change of method (§448(c) threshold crossing), the IRS filing spreads the §481(a) adjustment. Companies making the change primarily for financial-reporting purposes and remaining on cash-basis for tax can defer the tax filing until later.
5. **Update the revenue-recognition policy memo.** The written policy documenting the company's application of ASC 606 (see chapter 2) becomes formal at this point. The policy memo is the artefact the auditors ask for first.
6. **Coordinate with the auditor.** The auditor should be engaged early on the opening-balance-sheet restatement so their opinion covers it. Restating a prior period without the auditor's review creates a re-audit engagement later.

## The decision memo pattern

The CFO's cash-to-accrual transition decision memo should structure the recommendation as follows (this is also the pattern for exercise-06):

- **Context.** Where the company is today (cash basis, no audit, ARR / burn / stage).
- **Triggers assessed.** Which of the four triggers is fired or approaching (audit request, §448(c), investor request, IPO prep). Cite the specific fact — the term-sheet clause, the projected gross-receipts crossing date, the audit RFP.
- **Options.** Stay on cash basis (implications); dual-book accrual for management reporting only (implications); full transition with tax filing (implications).
- **Recommendation.** One option, with the reasoning.
- **Timeline.** The specific calendar for each transition step (restatement, opening-balance adjustment, first accrual close, auditor coordination, tax filing if applicable).
- **Cost estimate.** Fractional-CFO / outsourced-accounting time, auditor pre-audit engagement, potential tax-return amendment cost.
- **Risks and mitigations.** What could go wrong (opening-balance error, deferred-revenue misstatement, auditor rejection of the policy memo) and how to mitigate.

The memo is a board-level artefact if the transition is investor-driven and typically a CEO-approval artefact if internally driven. Either way, it should be documented; a cash-to-accrual transition made informally will not stand up in the first audit.

## Common transition failure modes

- **Retroactive restatement without the auditor.** The auditor rejects the restatement because they were not engaged to opine on it; the company pays for a re-audit.
- **Missing the opening deferred-revenue balance.** Cash-basis records do not track deferred revenue, so the opening balance has to be reconstructed contract-by-contract. This is where most restatement errors occur.
- **Filing Form 3115 late.** The §448(c) threshold crossing triggers a tax-filing deadline; missing it exposes the company to penalties.
- **Inconsistent policy application.** The policy memo is drafted but not consistently applied to new contracts; every audit sample turns up an exception.
- **Not disclosing the change of method.** In investor materials, a change from cash-basis reported revenue to accrual-basis reported revenue for the same period is a required disclosure. Presenting the two side-by-side without explaining the reconciliation confuses investors and looks like manipulation.

## Summary

- Four triggers drive the cash-to-accrual transition: an audit engagement (required), an IRC §448 threshold crossing (required for tax), a board or lead-investor request (contractually required once accepted), and IPO / dual-track prep (required for the S-1 audit periods).
- Well-run startups move to accrual for management reporting from the first annual-prepay contract, well ahead of the required triggers, and often stay on cash-basis for tax until the §448(c) threshold forces the tax change.
- The mechanical transition involves opening-balance-sheet restatement, comparative-period restatement, ongoing accrual entries, Form 3115 (if tax-driven), the revenue-recognition policy memo, and coordinated auditor engagement.
- A written decision memo — context, triggers, options, recommendation, timeline, cost, risks — is the artefact that documents the CFO's choice and defends it in the audit.

Chapter 7 walks the authoritative guidance stack behind every judgement call in this module — FASB ASC 606, IRS Publication 538, AICPA FRF for SMEs — and where startup-specific practitioner content fits alongside the primary sources.
