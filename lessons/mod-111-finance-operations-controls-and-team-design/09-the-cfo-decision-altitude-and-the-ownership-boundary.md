# The CFO Decision Altitude and the Ownership Boundary

## Why this matters

Every chapter in this module has been written at the same altitude. The stack chapter did not teach how to close a month in QuickBooks; it taught which stack the company graduates onto next and when. The close chapter did not teach the specific journal entries for a deferred-revenue subledger; it taught how to design the five-stage close workflow and what sub-ledger owners produce. The audit chapter did not teach how to prepare a workpaper; it taught the PBC list, auditor selection, and the two-year requirement. The controls chapter did not teach the mechanics of running a segregation-of-duties matrix in AuditBoard; it taught the five categories and the compensating-controls pattern. The R&D chapter did not teach how to fill out Form 6765; it taught the four-part test, the payroll-offset election, and the "when it meaningfully extends runway" decision. The sales-tax chapter did not teach how to file a Colorado home-rule return; it taught nexus, the compliance stack, and the exit-diligence exposure. The IPO chapter did not teach the SEC comment-letter response process; it taught the 18-24 month workstream and the CFO's choreography role.

That altitude is deliberate, and it is the module's ownership boundary. This chapter names it explicitly so subsequent modules, subsequent tracks, and the reader's own calendar all get the boundary right.

## The three altitudes of finance work

Finance work in a venture-backed company operates at three distinct altitudes. Each altitude is a different job with a different owner, different skills, and different decisions.

**Altitude 1 — Operator-mechanic.** The individual-contributor work of running the finance function. Booking journal entries, preparing reconciliations, running payroll, filing sales-tax returns, cutting AP checks, preparing 1099s, closing the sub-ledger, preparing the trial balance, drafting the audit workpaper. Roles: bookkeeper, staff accountant, senior accountant, AP clerk, payroll administrator, tax preparer, audit senior. Skill: mechanical accuracy and process discipline. The GAAP and IRC citations are consulted at line-item level; the systems are used at transaction level.

**Altitude 2 — Manager-supervisor.** Owning a specific function within finance and its output quality. Managing a team of operator-mechanics, reviewing their work, owning the sub-ledger integrity, closing the books, running the audit response, drafting the technical-accounting memo, managing the outsourced firm. Roles: controller, senior controller, accounting manager, FP&A manager, tax manager, treasury manager. Skill: technical depth on the specific standard (ASC 606 for revenue, IRC §41 for R&D credit, PCAOB standards for audit response), plus people management. Reads the primary sources in full and translates to the operator layer.

**Altitude 3 — CFO-decision.** Owning the entire finance function's design and its integration with the rest of the company's strategic decisions. Which stack, which vendors, which people, when to hire, when to migrate, when to audit, when to commit to the IPO, what controls to install, what tax positions to take, how the numbers land in the board pack and the fundraise deck. Roles: CFO, Head of Finance, sometimes a very-senior Head of Accounting / VP Finance. Skill: judgement about the tradeoffs — cost vs. optionality, speed vs. discipline, precision vs. defensibility, function-perfect vs. company-appropriate. Reads the primary sources at the section level, defers to the manager-supervisor layer for line-item interpretation, and integrates the finance decision with the CEO's calendar and the board's constraints.

This module is written at altitude 3, with just enough of altitude 2 for the CFO to know when their manager-supervisor layer has interpreted a standard defensibly.

## What this module explicitly does *not* cover

The altitude-1 operator-mechanic work — the how-to of bookkeeping, closing entries, sub-ledger reconciliation preparation, audit-workpaper drafting, tax-return preparation, SOX-control operation, S-1 financial-statement paragraph drafting — is not this module's depth. A CFO who cannot make the graduation call from QuickBooks to NetSuite (chapter 1) has a career-limiting gap; a CFO who cannot themselves post the journal entry to reclassify a prepaid asset into an operating expense is doing the wrong job and should stop. The module's design reflects the second.

The altitude-1 depth belongs in a future **`startup-accounting-controllership`** track that is not yet in the curriculum ladder. That track — when authored — would cover:

- The full ASC 606 mechanics with worked examples across contract shapes and modification patterns.
- The full month-end close operator playbook — every journal entry with its underlying support.
- Sub-ledger design and operation at the transaction level.
- Fixed-asset accounting and capitalised-software mechanics.
- Stock-based-compensation accounting under ASC 718 in operator detail.
- Lease accounting under ASC 842 in operator detail.
- Business-combination accounting under ASC 805 for M&A activity.
- Audit-workpaper preparation and response mechanics at the staff-accountant level.
- Sales-tax return preparation across the major state jurisdictions.
- SOX-404 control operation, testing, and evidence preservation at the operator level.
- Public-company reporting mechanics — 10-Q / 10-K / 8-K / proxy preparation, XBRL tagging, financial-printer workflow.

The controllership track's audience is the assistant controller, staff accountant, senior accountant, and controller-in-training — the people who *operate* the finance function's plant and equipment described in this module. The two tracks would be complementary and inter-reference each other; this module names the graduation calls and the design decisions, and the controllership track shows how the graduated tool is actually run day-to-day.

## What this module defers sideways

Three specific sideways deferrals inside the current curriculum ladder:

**Transaction execution → [`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum).** This module owns the *ongoing-company financial infrastructure* that makes transactions possible — the audit history, the SOX program, the cap table, the diligence-ready financials. The *transaction execution* itself — M&A auction mechanics, SPA drafting, escrow structuring, IPO underwriter selection and pricing, SEC comment-letter response, secondary tender operator mechanics, wind-down and ABC / Chapter-11 operator mechanics — belongs sideways. The chapter 8 IPO-readiness content stops at "the CFO's choreography job" and hands the transaction execution off.

**Corporate governance and equity-comp policy → [`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum).** The chapter 5 controls program covers *financial* controls; the *broader* controls program — data privacy (GDPR, CCPA), employment law compliance, corporate secretary function, entity management, board minutes and consent management operationally, insurance program (D&O, cyber, general liability) — belongs sideways. The equity-comp policy layer (grant guidelines, refresh policy, promotion adjustments) also belongs sideways; this track owns the equity *economics* (mod-104) and the option-pool math, not the HR / people policy that determines who gets what grant.

**Security-and-IT controls → security / trust track (family).** The IT general controls that overlap SOX ITGCs — access management, change management, computer operations — are owned by the security / IT function. The finance function's SOX-404 program consumes those controls as inputs; the security function operates them. A well-designed org has one set of controls that satisfy both audiences.

## What this module defers up

The **founder-numbers slice** — runway, burn, default-alive / default-dead, growth read, first KPI-selection at IDEA-stage — defers *down* to `startup-foundations` (level 10). This is called out in the track's overall CURRICULUM.md; this module never re-teaches those primitives. It layers CFO-grade discipline (the 18-month rolling runway plan, the driver-based model, the audit-ready close, the controls program, the IPO workstream) on top.

## The specific "operator vs. CFO" line in each chapter

To make the boundary usable rather than aspirational, here is the specific altitude-3 vs. altitude-1 line in each of this module's topics:

- **Stack selection (chapter 1).** Altitude 3 owns "when does QBO stop being fit-for-purpose and NetSuite start being fit-for-purpose"; altitude 1 owns "how do I configure the QBO chart of accounts and the NetSuite item master." Both matter; only the first is this module.
- **First-ten hires (chapter 2).** Altitude 3 owns "when to hire the controller, at what comp band, sourcing from which pool, evaluating for which competencies"; altitude 1 owns "how does the controller run the day-to-day close." Both matter; only the first is this module.
- **Month-end close (chapter 3).** Altitude 3 owns "5-day close target, sub-ledger ownership design, cost-of-revenue matching policy, deferred-revenue subledger design"; altitude 1 owns "how do I post the deferred-revenue journal entry when Customer X modifies their contract mid-month." Both matter; only the first is this module.
- **Audit-readiness (chapter 4).** Altitude 3 owns "when to commit to the audit, which auditor to select, how to run the PBC-response project, how to interpret year-one deficiencies against the IPO track"; altitude 1 owns "how do I prepare the workpaper the auditor asked for." Both matter; only the first is this module.
- **SOX-lite controls (chapter 5).** Altitude 3 owns "which controls to install at what stage, how to design the approval hierarchy, how to run the exception log, how to time the SOX-404 formalisation"; altitude 1 owns "how do I operate the wire-approval control day-to-day and preserve the evidence." Both matter; only the first is this module.
- **R&D credit (chapter 6).** Altitude 3 owns "does the credit meaningfully extend runway, which activities qualify at what expense rate, whether to make the payroll-offset election, which specialty firm to engage"; altitude 1 owns "how do I prepare Form 6765 with the specialty firm and reconcile the credit to the tax provision." Both matter; only the first is this module.
- **Sales-tax nexus (chapter 7).** Altitude 3 owns "when to commission the nexus study, which compliance vendor to install, how to address back-exposure per jurisdiction (register / VDA / documented no-action), how to model the exit-diligence exposure"; altitude 1 owns "how do I file the monthly return for California." Both matter; only the first is this module.
- **IPO-readiness (chapter 8).** Altitude 3 owns "the 18-24 month workstream design, the audit / controls / close / tax / disclosure choreography, the dual-track parallelism, the personal calendar shape at each phase, the MD&A drafting"; altitude 1 owns "how do I XBRL-tag the S-1 financial statements." Both matter; only the first is this module.

## The CFO who tries to run altitude 1

The common failure mode: a CFO promoted from controller who continues to run the close, review every journal entry, and hand-check the audit workpapers. Symptoms: the controller under them has nothing to own and quits; the CFO's calendar has no room for capital-allocation or investor work; the board's finance conversations get short-changed. Remedy: the CFO stops running altitude 1, hires the manager-supervisor layer if not already in place, promotes trust downward.

The reverse failure mode: a CFO from a banking / VC background who has never operated altitude 1 or altitude 2 and defers *everything* to the outsourced firm and the controller. Symptoms: the CFO cannot answer specific board questions about the numbers, cannot interpret variances, cannot spot a broken revenue-recognition position before it hits the auditor. Remedy: the CFO builds enough altitude-2 depth in each area to *review* the manager-supervisor work meaningfully, without displacing it.

The functional CFO operates at altitude 3, reviews at altitude 2, and never operates at altitude 1. The whole finance-org design that this module has been building is what enables that pattern.

## Where to go after this module

- **[`project-101-seed-to-series-a-fundraise-pack`](../../projects/project-101-seed-to-series-a-fundraise-pack/)** — the portfolio project that integrates the finance-ops discipline this module installs with the fundraising-track output.
- **[`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum)** — the sideways functional pillar for M&A / IPO / secondary / shutdown transaction *execution* that this module hands off to.
- **Future `startup-accounting-controllership`** — the altitude-1 / altitude-2 track for the operator-mechanic depth this module explicitly does not cover.
- **[`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum)** — the sideways functional pillar for the broader governance / policy / people / legal layer that surrounds the finance function.

## Summary

- Finance work in a venture-backed company operates at three altitudes: operator-mechanic (altitude 1), manager-supervisor (altitude 2), and CFO-decision (altitude 3). This module is written at altitude 3.
- The altitude-1 depth — bookkeeping, close mechanics, sub-ledger operation, audit-workpaper drafting, tax-return preparation, SOX-control operation, S-1 paragraph drafting — belongs in a future `startup-accounting-controllership` track.
- The sideways deferrals in the current ladder: transaction execution → `startup-exit-curriculum`; corporate governance and equity-comp policy → `startup-operations-governance-curriculum`; security / IT controls → security / trust track.
- The founder-numbers slice defers *down* to `startup-foundations`.
- The CFO who operates at altitude 1 leaves no room for their controller and no calendar for capital-allocation work; the CFO who never operates at altitude 1 or 2 cannot review the numbers meaningfully. The functional CFO operates at altitude 3, reviews at altitude 2, and never operates at altitude 1.

This module — and the track it closes — installs the altitude-3 discipline. The finance function's plant, people, close, audit, controls, tax, and IPO-readiness are all now design decisions the CFO owns.
