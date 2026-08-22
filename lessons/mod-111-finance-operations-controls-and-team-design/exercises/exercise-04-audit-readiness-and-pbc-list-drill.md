# Exercise 04 — Audit-Readiness and PBC List Drill

**Estimated time:** ~3.5 hours
**Prerequisites:** Chapters 1-4 (stack, hires, close, audit-readiness).

## Problem statement

For a specified Series-B SaaS company committing to its first outsourced audit, produce the full audit-readiness plan. Deliverables: an auditor-selection memo (three firms bidded), a PBC (prepared-by-client) list of ≥ 150 line items organised by section, a year-one deficiency-anticipation memo, and a 12-month audit-prep project plan that carries the finance team from audit engagement letter through audit-opinion issuance.

The goal is the specific project-management discipline the CFO / Head of Accounting runs during the first audit. Everyone survives the first audit; the difference is whether it takes six weeks with 20% overtime or five months with 60% overtime and a re-hire cycle at the end.

## Scenario — build your own

Construct (or use a real one) a Series-B SaaS company with the following characteristics:

- ~$25M ARR, ~150 employees, ~600 active customer contracts, ~$50M cash on hand from the recent Series-B raise.
- GL on QBO for the audit year, migrating to NetSuite in the following year (audit will need to handle the transition disclosure).
- Deferred-revenue subledger ~4,500 active contract-months tracked; recent hire of Head of Accounting.
- One international customer entity (a UK subsidiary), added mid-audit-year.
- No prior audit history.
- Board decision to commit to first audit: driven by the Series-B lead investor's LP-side reporting requirements and by the audit-committee's expressed intent to have the two-year audit history in place by the third year post-B to enable an IPO in year four or five.
- Fiscal year: calendar year. Audit period: the just-closed calendar year.

## Requirements

Produce the following artifacts.

### Artifact 1 — Auditor selection memo (2-4 pages)

A memo to the audit committee recommending an auditor. Include:

- **The RFP shape.** Which three firms were RFP'd, why those three, how the RFP was scoped (audit-only vs. audit + tax + advisory; multi-year commitment vs. year-by-year; on-site fieldwork vs. remote-first).
- **Comparison matrix.** For each of the three firms, a row per criterion — (1) PCAOB registration status, (2) SaaS / technology practice depth, (3) partner-on-engagement continuity, (4) proposed fee (with any assumptions about scope), (5) audit-committee references (2-3 companies of similar profile), (6) transition-cost estimate if the company later switches, (7) any independence concerns (e.g., existing tax-practice relationship that would conflict).
- **The recommendation** with an explicit trade-off statement — "recommend Firm X because [rationale]; accept the fee premium of $Y because [rationale]; alternative would be Firm Z if [condition]."
- **The pre-approval workflow** the audit committee will run for the recommended firm's non-audit services.

Assume for the exercise that the three firms are one Big Four, one second-tier national (e.g., BDO, Grant Thornton, RSM), and one startup-boutique (e.g., Frank Rimerman, Withum, Armanino). Fill in the specific choice pattern based on the company's IPO trajectory.

### Artifact 2 — PBC (prepared-by-client) list (≥150 line items)

A spreadsheet with columns:

- Line item ID (PBC-XXX)
- Category (corporate documents, cash, AR / revenue, AP / accrued, fixed assets, equity, debt, tax, sales tax, legal, related-party, subsequent events, etc.)
- Description
- Source (specific system / person / document location)
- Owner (name / role)
- Preparer target completion date
- Reviewer target completion date
- Auditor deadline
- Status (not-started / in-progress / delivered / auditor-reviewed / cleared)
- Notes (auditor questions, follow-ups)

Target minimum: 150 line items covering all 15 chapter-4 PBC-list categories.

### Artifact 3 — Year-one deficiency-anticipation memo (3-4 pages)

For each of the year-one deficiency categories from chapter 4 (segregation of duties, stock-based comp, revenue recognition, cutoff, cash controls, fixed assets, related-party, income tax), identify:

- Whether the company is expected to be flagged on this category.
- The specific evidence gap that would trigger the flag.
- The remediation plan (compensating control, process fix, documentation upgrade) that avoids the flag or minimises its severity.
- The disclosure implication if the flag becomes a *material weakness* rather than a *significant deficiency* — including any impact on the future S-1 disclosure (chapter 8).

### Artifact 4 — 12-month audit-prep project plan (Gantt-style)

A visual project plan showing the audit-prep workstream from Q1 (planning and PBC-list drafting) through Q4 (audit-fieldwork wrap and opinion issuance). Milestones:

- Engagement letter signed (Q1).
- Kickoff meeting (Q1).
- Interim procedures — internal-control walkthrough, initial control testing (Q2-Q3).
- Year-end preparation — reconciliations frozen, PBC-list delivered (Q4 or Q1-following).
- Fieldwork on-site or remote (Q1-Q2 following year-end).
- Draft opinion (Q2 following year-end).
- Audit-committee sign-off (Q2 following year-end).
- Opinion issuance (Q2 following year-end).

Overlay the finance-team internal workstream (close cycles, sub-ledger reconciliations, technical-accounting memos) to show the load pattern on the team across the year.

### Artifact 5 — The audit-committee readout template (1-2 pages)

The reference template the CFO / Head of Accounting will use for the quarterly audit-committee update through the audit-prep year. Sections:

- PBC-list status (delivered / outstanding / at risk).
- Auditor interactions this quarter (topics discussed, positions taken, open items).
- Deficiency-anticipation status (any newly-identified risks; remediation progress).
- Technical-accounting positions being taken (revenue recognition edge cases, stock-based-comp inputs, business-combination if any M&A, income-tax provision progress).
- Auditor independence check (any new relationships to review; any pre-approval requests).
- Next-quarter focus.

## Starter guidance

- Draft the PBC list against the chapter-4 category list; do not invent categories. If a category doesn't apply (e.g., no debt), state "N/A — no debt outstanding" rather than skipping the section entirely.
- For the auditor-selection memo, choose the recommendation *first* based on the company's characteristics, then write the rationale — do not run the comparison as a scoring matrix and pick the winner mechanically. The CFO decision is a judgement call informed by the matrix.
- The year-one deficiency memo is where a CFO earns their salary — thinking through what the auditor will find *before* they find it and either fixing it or preparing the compensating story.
- Use chapter 5's SOX-lite controls memo (exercise 05) as an input to the deficiency memo — the controls program is the direct response to the segregation-of-duties finding pattern.
- Cross-reference the ownership scope with mod-110's audit-committee chapter — the audit committee is the board audience for this workstream.

## Acceptance criteria

- **Auditor-selection memo names three specific firms** (real or clearly-labelled composite) with a defensible recommendation and trade-off statement.
- **PBC list has ≥ 150 line items** across all 15 chapter-4 categories.
- **Every PBC line item has an owner and a due date.**
- **Deficiency memo addresses all 8 chapter-4 deficiency categories** with a company-specific assessment and remediation plan for each.
- **Project plan spans 12 months** with named milestones and the finance-team load overlay.
- **Audit-committee readout template is usable** — a CFO could open it, fill it in, and hand to the audit-committee chair.

## Deliverables

- Auditor-selection memo (Markdown or PDF, 2-4 pages).
- PBC list (spreadsheet).
- Deficiency-anticipation memo (Markdown or PDF, 3-4 pages).
- 12-month project plan (spreadsheet or visual).
- Audit-committee readout template (Markdown or Google Doc).

## Extensions (optional)

- Model a company on a *tighter* IPO trajectory (IPO in year 3 post-Series-B rather than year 4-5): what changes in the auditor selection, the PBC-list depth, the deficiency-anticipation priorities, the audit-committee cadence?
- Model an *M&A-heavy* company (three bolt-on acquisitions in the audit year): add the business-combination-accounting workstream, the opening-balance-sheet valuation process, and the ASC 805 disclosure additions.
- Model a *material weakness* finding scenario: the year-one audit surfaces a material weakness in revenue recognition; author the remediation plan, the disclosure to the board, and the audit-committee response.
