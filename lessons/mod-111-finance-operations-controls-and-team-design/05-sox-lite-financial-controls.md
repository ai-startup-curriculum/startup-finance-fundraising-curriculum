# SOX-Lite Financial Controls — The Pragmatic Series-B Pattern

## Why this matters

At Series-B a company is too big to run finance-ops on trust and personal relationships and too small to run the full SOX-404 controls program that a public company operates. The specific pattern that fills the gap is what practitioners call **SOX-lite** — the pragmatic subset of formal financial controls a Series-B / Series-C private company installs, chosen to (a) satisfy the auditor and pre-empt material-weakness findings (chapter 4), (b) prevent the specific fraud and error scenarios that scale with headcount and cash, and (c) build the muscle for the eventual full SOX-404 regime the company will operate under as a public company (chapter 8) without spending the two years and multi-million-dollar budget SOX-404 formally requires.

Controls at a startup are not paperwork. Every control has a specific risk it addresses — the accountant approving her own journal entries is the risk that produces expense-fraud stories; the CEO with sole wire-signing authority is the risk that produces the "$800K wire to a fake vendor" news article. Naming the risk, then naming the control that addresses it, then documenting the operating evidence that shows the control worked, is the discipline. The auditor's evaluation, the audit committee's oversight, and the CFO's confidence in the numbers all sit on that discipline.

## The control framework

The reference framework is COSO's *Internal Control — Integrated Framework* (2013 revision). COSO defines five components: control environment, risk assessment, control activities, information and communication, and monitoring. In practice, a private-company SOX-lite program spends most of its energy on **control activities** — the specific policies and procedures that mitigate specific financial-reporting risks — while borrowing the vocabulary of the other four components.

Controls decompose into two types:

- **Preventive controls** — designed to prevent an error or fraud before it occurs. Example: an AP system that will not release a payment above $10K without a second approver. If the second approver is missing, the payment doesn't go out.
- **Detective controls** — designed to detect an error or fraud after it occurs. Example: the monthly bank reconciliation that will surface an unauthorised wire even if the preventive control missed it.

A well-designed control set uses both: preventive controls to keep the error rate low, detective controls as the safety net. Every process should have at least one detective control even if the preventive control is strong, because preventive controls fail (people override them, tooling has bugs, roles change).

## The five categories that matter at Series-B

### 1. Segregation of duties (SoD)

**The risk.** One person who initiates a transaction, approves it, records it, and reconciles it can commit fraud or make an error that no one else catches. Classic SoD violations: the AP clerk who cuts the check, signs the check, records the payment, and reconciles the bank statement.

**The reference separation.** The four functions — *authorise, execute, record, reconcile* — should be split across at least two people, and ideally three, for material transactions. At a small Series-A/B team where headcount does not support four separate people, the pragmatic minimum is *authorise* separated from *execute* separated from *reconcile*.

**Compensating controls at small headcount.** When true SoD is not possible because the team is too small, the auditor accepts *compensating* controls — typically a review by someone outside the specific process (the CFO reviews the CFO's expense report; the CEO's expenses are approved by the audit committee chair; the accountant's journal entries are reviewed by the outsourced accountant or the CFO). These compensating controls must be *documented* with a reviewer signature (or e-signature) each period.

**Common SoD violations to fix by Series-B.**
- The accountant who books their own journal entries without reviewer sign-off.
- The AP clerk who both processes vendor onboarding and processes vendor payments.
- The CFO who both initiates wire transfers and reconciles the bank statement.
- The controller who both books stock-option grants and administers the option-grant approvals.

### 2. Approval hierarchies for spend

**The risk.** Uncontrolled spend at any level: an employee books a $50K vendor without approval, a manager signs a $200K contract without CFO involvement, an executive commits the company to a multi-year lease.

**The reference structure — the spend authority matrix.** A single document, approved by the CFO and the audit committee, that specifies for each spend type (vendor invoice, purchase order, contract commitment, capex, hiring req, salary offer) the approval threshold and the required approver at each threshold. Typical shape for a Series-B SaaS company:

| Spend type | ≤$5K | $5K-$25K | $25K-$100K | $100K-$500K | >$500K |
|---|---|---|---|---|---|
| Vendor invoice | Manager | Dept head | CFO | CFO+CEO | CFO+CEO+board notify |
| Purchase order | Manager | Dept head | CFO | CFO+CEO | CFO+CEO+board notify |
| Contract commitment (multi-year) | Dept head | Dept head+legal | CFO+legal | CFO+CEO+legal | Board approval |
| Capex | Dept head | CFO | CFO | CFO+CEO | Board approval |
| Salary offer | Hiring manager | Hiring manager+HR | CFO | CFO+CEO | Board / comp cmte |
| Severance | Manager+HR | Manager+HR+legal | CFO+CEO+legal | CFO+CEO+legal | Board+legal |

Thresholds should be tuned to the company's revenue and cost base. The specific numbers matter less than the *documented gradient* and the *tool-enforced* thresholds (Ramp / Brex / Airbase / Coupa / Zip should enforce the matrix in-workflow, not as a policy document).

**The board-approval line.** Any spend that crosses the board-approval threshold — typically material capital commitments, executive severance, or transactions with a related party — is documented in the board consent register (mod-110 chapter 4). The CFO owns the trigger identification; the board owns the approval.

### 3. Procurement and vendor onboarding

**The risk.** Vendors added to the system without diligence become the vector for fake-vendor fraud, non-compliant vendors, or vendors that expose the company to OFAC / sanctions liability.

**The reference process — the vendor-onboarding checklist.** Every new vendor is onboarded through:
- **Requisition.** A requestor identifies the need and the specific vendor; a purchase order is created.
- **Vendor form.** The vendor completes a W-9 (US) or W-8 series (foreign), provides banking details, provides certificate of good standing or business registration.
- **OFAC / sanctions screen.** The vendor is screened against the OFAC Specially Designated Nationals list (US Treasury) and against any additional company-required lists.
- **Approval.** AP owner approves the vendor for onboarding; CFO approval required if the initial engagement crosses a spend threshold.
- **Bank verification.** For any vendor being paid via ACH or wire, the banking details are verified via a *second-channel confirmation* — a phone call to a known number at the vendor, not a reply to the email that supplied the details. This is the specific control that prevents the "vendor email compromised, fake wire instructions supplied" attack.

**Three-way match.** For invoiced spend against a purchase order, the payment cannot release until the invoice matches the PO and the receipt (evidence that the goods / services were received). Coupa, Zip, and NetSuite AP all enforce three-way match natively.

### 4. Corporate-card and expense-policy enforcement

**The risk.** Employees using corporate cards for personal expenses, cardholders spending outside the policy limits, missing receipts that make the expense unsubstantiated for tax purposes.

**The reference controls.**
- **Policy document.** A written expense policy — approved by the CFO, distributed to every cardholder, refreshed annually — covering allowed categories, per-diem limits, meal-per-person limits, travel-class rules, and receipt requirements.
- **Tool-enforced merchant restrictions.** Ramp, Brex, and Airbase allow per-card merchant-category-code restrictions (block gambling, block cash advances, block adult entertainment); the CFO turns these on by default and adjusts by role.
- **Real-time expense-report matching.** Each corporate-card charge is matched to a receipt and a business-purpose note within N days (typical: 7-14 days). Missing receipts past the deadline auto-suspend the card.
- **Executive expense review.** Executives' expenses are reviewed by someone outside their reporting line — typically the CFO reviews the CEO, and the audit committee chair reviews the CFO on an annual sample basis.
- **Reimbursement policy.** Non-corporate-card expenses reimbursed only against receipt, coded in the same categories as corporate-card expenses, and subject to the same policy.

**IRS accountable-plan requirement.** Under IRS regulations, a reimbursement plan is an "accountable plan" (non-taxable to the employee) only if reimbursements are for business expenses substantiated within a reasonable time and any excess advance is returned. A messy expense-reimbursement process creates a *taxable-income* problem for employees on top of the control problem.

### 5. Wire-transfer and disbursement controls

**The risk.** Fraudulent wire transfers — either external (business-email-compromise attacks that trick finance staff into sending wires to attacker-controlled accounts) or internal (a finance employee wiring funds to their own account). Wire fraud is the single largest financial fraud category by dollar loss for mid-market companies <!-- needs-research: cite current FBI IC3 report on business email compromise losses for the current year -->.

**The reference controls.**
- **Dual approval for every wire.** Every outbound wire above a threshold (typical: $10K, sometimes lower) requires two approvers — the initiator plus a second signer at the CFO or Head of Accounting level.
- **Call-back verification for new payees.** Any wire to a new payee, or to an existing payee with changed banking details, requires call-back verification at a known phone number before release. The call-back is documented.
- **Positive-pay and reverse-positive-pay at the bank.** For ACH and check disbursements, positive-pay (the bank matches outbound payments against a pre-authorised file) and ACH filters (only pre-authorised counterparties can debit the account) block unauthorised debits.
- **Daily cash review.** The treasury owner reconciles yesterday's activity against the disbursement log every morning; any unauthorised movement is caught in one business day.
- **BEC-specific training.** Finance staff trained specifically on business-email-compromise patterns — CEO-impersonation urgency requests, vendor-banking-detail-change emails, wire-to-crypto-exchange requests. The training is documented; the auditor asks for it.

## The controls matrix — the document

The five categories above are documented in a **controls matrix** — a single spreadsheet or workflow tool listing every control, the risk it addresses, the owner, the frequency, the evidence produced, and the reviewer. Typical columns:

- Control ID (e.g., FIN-005)
- Control description (e.g., "Every wire above $10K requires two approvers")
- Risk addressed (e.g., "Fraudulent or erroneous wire transfer")
- Preventive / detective
- Owner (name / role)
- Frequency (each transaction / daily / monthly / quarterly)
- Evidence produced (e.g., "Wire log with two approver signatures")
- Reviewer (name / role)
- Last review date, next review date

At Series-B the matrix might contain 40-80 controls; at pre-IPO with SOX-404 preparation (chapter 8) it grows to 200-500. AuditBoard, Workiva, and larger GRC platforms manage this at scale; a well-run spreadsheet works at Series-B.

## Tone and enforcement

The controls are not the auditor's controls; they are the *CFO's* controls. Two enforcement patterns to install early:

- **The CFO owns the controls program.** Not the outsourced auditor, not the outside counsel, not the Head of Compliance. The CFO signs each policy, sits in the audit-committee readouts on controls, and is the escalation for exceptions.
- **The exception is documented.** Every time a control is bypassed — a wire released without dual approval because the second approver was travelling, a purchase over threshold approved verbally with paperwork after the fact — the exception is logged with reason, approver, and remediation. Exception logs are reviewed monthly by the CFO / Head of Accounting; the auditor will ask for the log.

Controls that everyone follows are not the useful discovery. Controls that were bypassed for a reason — and how the company responded — are.

## What SOX-lite is *not*

- **Not SOX-404.** SOX Section 404, applicable to public companies, requires (a) management assessment of internal controls over financial reporting (§404(a)) and (b) auditor attestation on those controls (§404(b), with a small-reporting-company deferral under the JOBS Act). SOX-404 is a formal program with independent testing, documentation of process-flow narratives, entity-level controls, IT-general-controls, and application controls. Chapter 8 covers the transition from SOX-lite to full SOX-404 pre-IPO.
- **Not SOC 2 / ISO 27001.** SOC 2 is a controls report focused on the *service organisation's* systems and data (typically the trust-services criteria of security, availability, processing integrity, confidentiality, and privacy). ISO 27001 is an information-security management-system standard. Both cover controls the *engineering / security* function operates, not the *finance* function. They may share underlying evidence (change-management, access-management) but they are separate programs with separate reports.
- **Not a compliance-team-owned program.** At mid-market scale there is no separate compliance team; the CFO owns financial controls, the security-and-IT function owns security controls, and the general counsel owns legal-and-regulatory compliance. The CFO's job is the financial-controls slice.

## The transition to full SOX-404

Once the IPO is on the two-year horizon, the SOX-lite program formalises into a full SOX-404 program (chapter 8 details this). The transition steps:

- **Scoping.** Identify the significant accounts and disclosures, the relevant business processes, and the in-scope entities.
- **Process narratives and control matrices.** Formal process-flow documentation and control-matrix documentation for each in-scope process.
- **Test of design.** Independent evaluation that each control is *designed* effectively.
- **Test of operating effectiveness.** Independent evaluation, over a sufficient period, that each control is *operating* effectively.
- **Deficiency evaluation.** Any deficiency evaluated for severity — control deficiency / significant deficiency / material weakness.
- **Remediation and re-testing.** Any significant deficiency or material weakness remediated and re-tested.
- **Management assessment and auditor attestation.** Management issues its §404(a) assessment; the auditor issues its §404(b) attestation (deferred for EGCs under JOBS Act).

The company that runs a rigorous SOX-lite program at Series-B/C spends 12-18 months on the SOX-404 transition. The company that runs SOX-lite as paperwork spends 18-30 months and stumbles into a material-weakness disclosure that delays the IPO.

## Summary

- SOX-lite is the pragmatic pattern of financial controls a Series-B / C private company installs — enough to satisfy the auditor, address the specific risks, and build the muscle for full SOX-404 without the full program.
- Controls decompose into preventive (prevent errors before they occur) and detective (catch errors after they occur); a well-designed program uses both.
- The five categories at Series-B: segregation of duties, spend approval hierarchies, procurement / vendor onboarding, corporate-card / expense-policy enforcement, wire-transfer controls.
- Every control is documented in a controls matrix with owner, frequency, evidence, and reviewer; exceptions are logged and reviewed.
- SOX-lite is *not* full SOX-404, *not* SOC 2 / ISO 27001, and *not* a compliance-team-owned program; the CFO owns it.
- The transition to full SOX-404 begins ~18 months pre-IPO (chapter 8).

Chapter 6 turns to the tax practice that funds part of the finance-ops budget — the R&D credit.
