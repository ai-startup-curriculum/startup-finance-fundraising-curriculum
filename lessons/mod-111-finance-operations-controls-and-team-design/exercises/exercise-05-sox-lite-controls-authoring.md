# Exercise 05 — SOX-Lite Controls Authoring

**Estimated time:** ~3.5 hours
**Prerequisites:** Chapters 1-5 (stack, hires, close, audit-readiness, SOX-lite controls). Exercise 04 (audit-readiness) is helpful but not required — the controls program is the direct response to the segregation-of-duties finding pattern.

## Problem statement

Author the Series-B financial-controls memo for a specified company. Deliverables: a controls memo the CFO would present to the audit committee, a fully-populated controls matrix (≥ 40 controls), a spend-authority matrix (approvals by threshold and spend type), a vendor-onboarding and wire-transfer control-flow document, an exception-log template with a monthly review cadence, and a scoring of each of the five chapter-5 categories against a "designed / operating / gaps" rubric.

The goal is a memo that (a) satisfies the year-one auditor's control-environment walkthrough (chapter 4), (b) prevents the specific fraud and error scenarios that scale with headcount and cash, and (c) is the seed of the SOX-404 program the company will formalise 12-18 months pre-IPO (chapter 8). SOX-lite as paperwork is a wasted exercise; SOX-lite that names a risk, addresses it with a control, and documents the operating evidence is what carries the company through to IPO without a material-weakness disclosure.

## Scenario — build your own

Construct (or use a real one) a Series-B SaaS company with the following characteristics:

- ~$25M ARR, ~150 employees, ~600 active customer contracts, ~$50M cash on hand from the recent Series-B raise.
- One US HQ entity plus one recently-added UK subsidiary (no employees yet in the UK; a small operating expense footprint).
- GL still on QBO with a planned NetSuite migration in the coming year; corporate cards on Ramp; bill-pay on Ramp; payroll on Rippling; expense-management on Ramp.
- Finance team: CFO, newly-hired Head of Accounting, senior accountant, one FP&A analyst, plus an outsourced accounting firm relationship for tax and technical-accounting support.
- Board decision to commit to first audit in the current fiscal year (see exercise 04). The audit committee has specifically requested a "SOX-lite" controls memo as an input to the year-one audit-readiness workstream.
- Independent audit committee chair (former public-company CFO) as the internal stakeholder driving the controls-memo request.
- No prior formal controls program; the finance team has been operating on trust plus a small number of ad-hoc approval rules encoded in Ramp / bill-pay tooling.

Reasonable variations are welcome; document any assumption changes upfront.

## Requirements

Produce the following artifacts.

### Artifact 1 — The SOX-lite controls memo (4-6 pages)

The memo the CFO delivers to the audit committee. Sections:

- **Executive summary.** One page — the current state, the gaps identified, the proposed program shape, the resourcing required, the timing to "designed and operating" for each category.
- **Framework alignment.** Half-page — the specific COSO components the program aligns to and the private-company / SOX-lite scoping (what is in scope now vs. what is deferred to the SOX-404 formalisation at ~T−18 months pre-IPO).
- **The five categories.** For each of the chapter-5 categories (segregation of duties, spend approval hierarchies, procurement and vendor onboarding, corporate-card and expense-policy enforcement, wire-transfer and disbursement controls), name the specific risks addressed, the specific controls installed (preventive and detective), the owner, the evidence produced, and the review cadence. Cross-reference each control to the controls-matrix line item ID (artifact 2).
- **Compensating controls.** Where headcount does not support full segregation of duties, name the specific compensating control and the reviewer.
- **Exception handling.** How exceptions are logged, reviewed, and remediated. Reference the exception-log template (artifact 5).
- **Program cadence.** Monthly / quarterly / annual review pattern; the CFO's sign-off cadence; the audit-committee reporting cadence.
- **The transition to SOX-404.** A short paragraph naming the specific artifacts and disciplines the SOX-lite program produces that will feed the future SOX-404 program (chapter 8) — process narratives, control matrices, evidence archives.

### Artifact 2 — The controls matrix (≥ 40 controls)

A spreadsheet with columns per chapter 5:

- Control ID (e.g., FIN-005)
- Control description (one sentence, actionable)
- Category (1 SoD / 2 spend / 3 procurement / 4 card-and-expense / 5 wire)
- Preventive / detective
- Risk addressed (one sentence, specific — "unauthorised wire to attacker-controlled account", not "wire fraud")
- Owner (name / role)
- Frequency (each transaction / daily / weekly / monthly / quarterly)
- Evidence produced (specific artifact — "signed wire log", "Ramp approval trail", "monthly bank reconciliation with reviewer signature")
- Reviewer (name / role, different from owner)
- Tool-enforced or policy-only? (name the tool if tool-enforced — Ramp / Brex / bill-pay / bank ACH filter / NetSuite / etc.)
- Status (designed / operating / gap)
- Design date, last-operated date, next-review date

Target: ≥ 40 controls, distributed roughly 6-10 SoD, 8-12 spend, 6-10 procurement, 8-10 card / expense, 6-8 wire.

### Artifact 3 — The spend-authority matrix

A table (chapter 5 shows the shape) filled in for the specific company's revenue and cost base. Rows per spend type (vendor invoice, purchase order, contract commitment, capex, salary offer, severance, marketing spend, professional-services engagement, at minimum); columns per threshold band (recommend at least five bands: ≤$5K / $5K-$25K / $25K-$100K / $100K-$500K / >$500K). Each cell names the specific approver(s) and any additional escalation (legal review, board notification, board approval).

The matrix must be **tool-enforceable**: each threshold must map to a rule the AP / spend tool (Ramp / Brex / bill-pay / NetSuite AP) can enforce in-workflow, not a policy document that only exists on paper. Name the specific tool workflow for each rule.

Include a one-page appendix — the rationale for the specific threshold values against the company's revenue and cost base, and the specific process for annual re-tuning of the thresholds.

### Artifact 4 — The vendor-onboarding and wire-transfer control-flow document (2-3 pages)

Two process-flow narratives:

- **Vendor onboarding.** From requisition through W-9 / W-8 collection, OFAC screen, bank-detail verification (with the specific second-channel confirmation script), approval routing, and system activation. Name each hand-off point and the evidence captured at each step.
- **Wire transfer.** From wire request through dual approval, call-back verification for new payees, positive-pay / ACH-filter interaction with the bank, disbursement, and next-day cash-log reconciliation. Include the specific escalation path for a BEC-attempt indicator.

Each narrative should include a simple swim-lane diagram (Mermaid / draw.io / spreadsheet grid) showing the owner at each step and the evidence captured.

Bonus: name at least three specific BEC (business email compromise) attack patterns and the specific control that blocks each — CEO-impersonation urgency requests, vendor-banking-detail-change emails, wire-to-crypto-exchange requests, or others from current threat-intelligence reporting.

### Artifact 5 — The exception-log template and monthly review cadence (1-2 pages)

A spreadsheet template with columns:

- Exception ID
- Date logged
- Control bypassed (control ID and description)
- Reason for exception
- Approver (name and role)
- Compensating action taken (e.g., "verbal approval documented after the fact, invoice attached")
- Remediation (any process fix committed to prevent recurrence)
- Reviewer and review date (CFO / Head of Accounting)
- Status (open / closed / escalated to audit committee)

Plus a short (1 page) description of the monthly exception-review meeting — attendees, agenda, escalation criteria to the audit committee, and the annual roll-up to the year-end SOX-lite program report.

### Artifact 6 — The category-by-category scoring (1-2 pages)

For each of the five chapter-5 categories, score the *current-state* program on a three-point rubric:

- **Designed** — the specific controls exist and are documented.
- **Operating** — the controls have been operating over the past ≥ 3 months with evidence retained.
- **Gap** — the control is either not designed, not operating, or operating without adequate evidence.

For each gap, name the specific remediation, the owner, and the target date. Total gap count and the target-close date drive the memo's executive-summary "when will we be ready for the auditor" statement.

## Starter guidance

- Start with the risks, not the controls. For each category name the specific fraud or error the control prevents; then name the control. The auditor evaluates the risk-to-control mapping, not the control count.
- The controls matrix is the *load-bearing* artifact. Every other artifact references it by control ID. Do not skip the matrix.
- The spend-authority thresholds are tuned to the company's revenue and cost base, not copied from a peer. A $25K threshold is meaningful at $25M ARR and meaningless at $200M ARR.
- For every SoD violation you cannot fully resolve (small headcount), name the specific *compensating control* and the reviewer. "We're too small to fully split" without a documented compensating control is a material-weakness precursor.
- Cross-reference chapter 4's year-one deficiency-anticipation categories — the SoD, revenue-recognition, cash-controls, and cutoff deficiency categories all map directly to specific SOX-lite controls. If your controls matrix does not address them, the year-one audit will flag the gap.
- Use exercise 04's deficiency memo (if you completed it) as an input — the deficiency-memo remediation plan is the direct source of many of the controls-matrix entries.
- The BEC threat pattern evolves — cite current-year FBI IC3 or specific industry-report language for the specific attack patterns. If you cannot verify a claim, mark it `[assumption]` or `<!-- needs-research: ... -->` per the module convention.

## Acceptance criteria

- **The memo names all five chapter-5 categories** with a specific risk-to-control mapping for each.
- **The controls matrix has ≥ 40 controls** with owner, reviewer, evidence, frequency, and tool.
- **Every control has a *distinct* owner and reviewer** (or a documented compensating-control note where the same person appears in both slots).
- **The spend-authority matrix has ≥ 5 spend types × ≥ 5 threshold bands filled in** with specific approvers and specific tool-enforcement mappings.
- **The wire-transfer flow includes call-back verification and dual approval** with specific thresholds.
- **The exception-log template is usable** — a CFO / Head of Accounting could open it, log an exception, and route it through the monthly review.
- **The category scoring names specific gaps** with a specific remediation, owner, and date — not "we'll clean this up over time."
- **Any unverified claim** (specific FBI IC3 statistics, specific vendor tool capabilities) is tagged `[assumption]` or `<!-- needs-research: ... -->`.

## Deliverables

- The SOX-lite controls memo (Markdown or PDF, 4-6 pages).
- The controls matrix (spreadsheet, ≥ 40 rows).
- The spend-authority matrix (spreadsheet or Markdown table).
- The vendor-onboarding and wire-transfer control-flow document (Markdown or PDF, 2-3 pages, with swim-lane diagrams).
- The exception-log template and cadence memo (spreadsheet + short Markdown).
- The category-by-category scoring (Markdown or spreadsheet, 1-2 pages).

## Extensions (optional)

- **Model the SOX-404 transition memo.** Add a section describing the 12-18 month path from the current SOX-lite program to a full SOX-404 program at ~T−18 months pre-IPO — the additional entity-level controls, IT general controls, application controls, test-of-design, and test-of-operating-effectiveness workstreams that layer onto the existing matrix.
- **Model a material-weakness scenario.** The year-one audit surfaces a material weakness in a specific area (revenue recognition, IT access controls, related-party transactions — pick one). Author the remediation plan, the disclosure memo to the audit committee, and the specific controls the SOX-lite program adds to prevent recurrence.
- **Cross-reference to SOC 2.** For a company that must maintain both SOX-lite (finance controls) and SOC 2 (security / trust controls), map the shared evidence (change-management, access-management, backup-and-recovery) and the distinct scopes. Name where the controls program overlaps with the security team's ownership and how the two programs coordinate to avoid duplicated testing.
- **Model an M&A wrinkle.** A bolt-on acquisition closes mid-year, adding a small target with its own AP process and its own corporate cards. Author the 90-day controls-integration plan — mapping the target onto the acquirer's controls matrix, retiring the target's redundant controls, and running the interim compensating-control set until integration completes.
