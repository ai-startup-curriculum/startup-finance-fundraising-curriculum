# IPO-Readiness and the Dual-Track — The CFO's Choreography Job

## Why this matters

The IPO is the destination the whole finance-ops program has been preparing for. Every prior chapter — the stack (chapter 1), the team (chapter 2), the close (chapter 3), the audit history (chapter 4), the SOX-lite controls (chapter 5), the tax practice (chapter 6), the sales-tax compliance (chapter 7) — feeds a single 18-24 month workstream that ends with an S-1 filing, a roadshow, a pricing meeting, and a first day of trading. The CFO is not the deal-execution owner (the underwriters, the CEO, and outside counsel share that ownership), but the CFO is the *choreographer* — the person whose calendar aligns audit, close, controls, tax, and disclosure into a filing that clears the SEC and prices the deal.

The dual-track — running an IPO process and a private-market process (M&A or continued fundraise) in parallel — is the specific CFO discipline that maximises optionality across the ~18 months of pre-IPO work. Companies that commit to a single track and then need to pivot (market closes, M&A offer materialises, private round becomes more attractive) find themselves with either wasted transaction-side spend or forced timing. Companies that dual-track from ~T-minus-18-months keep both options live until the underwriter-selection / bake-off moment. The tradeoff is meaningful additional prep work; the offset is meaningful optionality.

**Sideways deferral note.** This module owns the *ongoing-company financial infrastructure* that makes an IPO possible — the audit history, the SOX program, the public-company close, the S-1 workstream from the operating-side. The *transaction execution* mechanics — underwriter selection, pricing, roadshow choreography, lock-up mechanics, the S-1 / DRS filing process itself, the SEC comment-letter response process, the post-IPO IR calendar — belong sideways to [`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum). This chapter installs enough of the transaction-execution overlay for the CFO to know what the dual-track requires and what the pre-IPO team must produce; the transaction execution itself is out of scope.

## The pre-IPO timeline — the 18-24 month view

Working backward from the intended pricing month, the reference timeline for a first-time IPO issuer:

- **T−24 to T−18 months.** Commit to the two-year audit history if not already in place (chapter 4). Hire the Head of Accounting if not already hired (chapter 2, hire #5). Begin SOX-lite formalisation (chapter 5). If not already on Big Four, consider auditor transition (chapter 4 caveats on switching cost).
- **T−18 to T−12 months.** Auditor selection formalised as PCAOB-registered Big Four or top-tier second-tier. Full SOX-404 program design and implementation begins in earnest. First formal walkthrough of process-flow narratives and control matrices per significant account and disclosure. NetSuite / ERP finalised; close-automation platform (FloQast / Blackline / Numeric) deployed. Head of Investor Relations hired (chapter 2, hire #9). Corporate governance rebuilt for public-company norms — independent directors added to the board, audit / comp / nom-and-gov committees formalised (mod-110 chapter 6), by-laws / certificate reviewed for public-company defaults.
- **T−12 to T−6 months.** Second-year audit completed, giving the two-year audited history the S-1 needs. Public-company close (chapter 3) rehearsed — the finance team runs a "practice" quarter-end close on a public-company timeline to identify gaps. SOX-404 test-of-design and test-of-operating-effectiveness underway on the current period. S-1 drafting begins under the CFO / General Counsel / underwriter-counsel joint workstream. MD&A drafting under the CFO's authorship (see below). Bake-off — the process of interviewing and selecting the lead underwriters and the syndicate. Legal counsel selection (usually a large corporate-finance firm; often the firm that has handled financings to date).
- **T−6 to T−3 months.** Draft S-1 substantially complete. Confidential submission (DRS) to SEC under JOBS Act EGC confidentiality provision if applicable. SEC comment-letter cycle begins (typically 2-4 rounds of comments over 6-12 weeks). Financial-statement update mid-cycle if a quarter closes during the review. Pre-marketing / testing-the-waters conversations with select institutional investors under the JOBS Act EGC allowance.
- **T−3 to T−1 months.** SEC comments substantially cleared. Financial printer engaged. Registration statement declared effective. Roadshow launch — 10-14 days of institutional-investor meetings. Book-building.
- **T−1 to T-day.** Pricing meeting (evening before). Pricing announcement. IPO trades.
- **T+1 to T+90.** Lock-up in effect. First quarterly earnings as a public company (typically the first full quarter that ends after the IPO). Post-IPO analyst-day pattern begins.

The CFO's calendar over this period is roughly: 30% audit / controls / close, 30% S-1 / MD&A / SEC-comment response, 20% investor / roadshow prep, 20% ongoing operating finance work. The CFO does not have a normal quarter during the 18 months pre-IPO.

## The two-year audit requirement — the gating constraint

Reiterating from chapter 4: SEC Regulation S-X requires an S-1 to include audited balance sheets for the two most recent fiscal year-ends and audited statements of operations, cash flows, and stockholders' equity for the three most recent fiscal years — with a JOBS Act EGC reduction to two years of audited operations / cash flow / equity if the issuer qualifies (revenue under the EGC threshold, typically $1.235B as of the last inflation adjustment; verify current threshold before decisioning). <!-- needs-research: verify current EGC revenue threshold under the JOBS Act as most recently indexed -->

The CFO scheduling implication: an IPO in fiscal year N requires FY(N−1) and FY(N−2) audits (for an EGC) both completed and signed before the S-1 can go effective. The **first audit's commit-and-completion date is therefore the earliest binding constraint** on the IPO calendar. A company that commits to its first audit in FY(N−2) has margin; a company that commits in FY(N−1) is running against the wire; a company that commits in FY(N) has already slipped the IPO to FY(N+1).

## PCAOB-registered auditor selection

For SEC registrants, the auditor must be registered with the Public Company Accounting Oversight Board (PCAOB) and must be independent under SEC / PCAOB independence rules. Most Big Four firms are PCAOB-registered; several second-tier firms are as well; verify at the PCAOB's registered-firm directory before decisioning. If the pre-IPO auditor is not PCAOB-registered, the company must switch to a registered firm before filing — a switch that can add 3-6 months to the timeline and cost the incumbent firm's audit-history knowledge.

Independence-rule specifics that trip up first-time filers:

- **Non-audit services.** The auditor cannot provide bookkeeping, financial-statement preparation, actuarial services, valuation services (including business-combination valuations), internal-audit outsourcing, or a range of other services to the audit client. Tax services (in most forms) are still permitted but require audit-committee pre-approval.
- **Employment relationships.** Senior members of the audit team who take employment with the audit client trigger a one-year cooling-off period during which the firm must resign from the engagement.
- **Financial-relationship prohibitions.** Auditors cannot have financial relationships with the audit client (loans, investments, etc.).

The CFO owns the pre-approval workflow for all auditor services and the annual independence letter the auditor delivers to the audit committee.

## Public-company financial-reporting close

The public-company close is a compressed version of the private-company close (chapter 3):

- **Month-end close** — 3-5 business days. Same discipline as private-company Series-C close.
- **Quarter-end close** — 5-7 business days for the accounting close, followed by 2-3 weeks of quarterly-reporting work culminating in the 10-Q filing (typically 40-45 calendar days after quarter-end for large accelerated filers, 45 days for accelerated filers, 45 days for non-accelerated / small-reporting filers). Verify the specific due-date category for the company's expected market cap and float.
- **Year-end close** — 5-10 business days for the accounting close, followed by the 10-K filing (typically 60 days for large accelerated filers, 75 for accelerated, 90 for small-reporting; verify).
- **Earnings release** — typically 30-45 days after quarter-end, preceding the 10-Q filing. Includes GAAP and non-GAAP metrics, earnings-call script, guidance update.

The public-company close is a project each quarter, choreographed by a *close and reporting calendar* that maps every task to owners and dates. The reference cadence: earnings-release drafting starts in week 2 post-quarter-end; auditor review of the 10-Q / 10-K starts in week 3; audit-committee review the day before or the morning of the release; press release and earnings call on release day; 10-Q / 10-K filing 4-14 days later.

## SOX-404 — the full program

The SOX-lite program from chapter 5 becomes the full SOX-404 program 12-18 months pre-IPO. The full program adds:

- **Scoping.** Formal identification of significant accounts and disclosures, in-scope business processes, in-scope entities, in-scope IT systems. The scoping is documented and refreshed annually.
- **Entity-level controls.** Controls that operate at the company level rather than the transaction level — tone-at-the-top, code of conduct, whistleblower program, board oversight, financial-reporting risk-assessment process.
- **Process-level controls.** Documented process-flow narratives (walkthrough documents) for each in-scope process — order-to-cash, procure-to-pay, payroll, financial-close, treasury, tax, stock-based-compensation, IT change-management.
- **IT general controls (ITGCs).** Access controls, change-management, computer-operations, and program-development controls over the financial-reporting systems (typically the ERP, the billing system, the payroll system, the equity system, and adjacent).
- **Application controls.** Controls embedded in the financial-reporting applications — automated reconciliations, edit checks, three-way match, system-enforced approval workflows.
- **Test of design.** Independent evaluation that each control is *designed* effectively to address its risk.
- **Test of operating effectiveness.** Independent evaluation, over a sufficient period (typically 3-6 months of operation), that each control operated as designed. Sampled tests per control.
- **Deficiency evaluation.** Each identified deficiency evaluated on a severity scale: deficiency, significant deficiency, or material weakness. Material weakness triggers specific disclosure and remediation obligations.
- **Management assessment (§404(a)).** Management's annual assessment of internal control over financial reporting, filed with the 10-K.
- **Auditor attestation (§404(b)).** The auditor's independent attestation on internal control effectiveness, filed with the 10-K. **JOBS Act EGCs are exempt from §404(b) for up to five years post-IPO.**

The internal / external staffing pattern: internal audit team (2-6 people at IPO) runs the operating cadence; external SOX advisor (a Big Four or second-tier consulting practice, distinct from the audit firm to preserve independence) supports process narratives, control documentation, deficiency evaluation, and remediation. The CFO owns the program; the Head of Accounting or a dedicated Head of Internal Audit / SOX operates it.

## S-1 drafting — the workstream and the CFO's role

The S-1 is the registration statement filed with the SEC that describes the company, its business, its risk factors, its financials, and the offering. It is typically 250-400 pages. Sections and typical primary authors:

- **Prospectus summary** — CFO, CEO, underwriter counsel joint.
- **Risk factors** — General counsel, outside counsel, CFO joint.
- **Use of proceeds** — CFO.
- **Dividend policy** — CFO.
- **Capitalisation table** — CFO.
- **Dilution** — CFO.
- **Selected financial data** — CFO / Head of Accounting.
- **Management's Discussion and Analysis (MD&A)** — CFO with FP&A support (see below).
- **Business** — CEO, marketing, product, CFO for financial characterisation.
- **Management (bios of officers and directors)** — General counsel, People / HR.
- **Executive compensation** — Comp committee, People / HR, CFO for cost characterisation.
- **Certain relationships and related-party transactions** — General counsel, CFO.
- **Description of capital stock** — General counsel.
- **Shares eligible for future sale** — General counsel.
- **Underwriting** — Underwriter counsel.
- **Legal matters, experts, information incorporated by reference** — Outside counsel.
- **Financial statements** — Head of Accounting, auditor.

The CFO directly authors or reviews substantially all of the financial sections and cross-reviews the risk factors, executive compensation, and related-party sections for consistency with the financials.

Drafting is iterative — 4-6 formal drafts through the pre-filing period, with each draft distributed to the working group (company, underwriters, underwriter counsel, company counsel, auditor) and reviewed at "drafting sessions" (typically weekly, sometimes daily as pricing approaches). The CFO's calendar in the ~T−9 to T−3 month window is dominated by drafting-session prep and follow-up.

## MD&A — the CFO's most-scrutinised writing

Management's Discussion and Analysis (MD&A), governed by SEC Regulation S-K Item 303, is the narrative section where management explains the financial results — the "why" behind the numbers in the statements. It is the section:

- The SEC comments on most heavily in the review cycle.
- Investors read most carefully (both in the S-1 and in each subsequent 10-K / 10-Q).
- The audit committee reviews most rigorously.
- Establishes the company's *disclosure controls and procedures* baseline — every subsequent MD&A revision reflects a period-over-period consistency the market judges the CFO by.

The reference MD&A structure:

- **Overview** — company description, key metrics, key trends.
- **Key financial and operating metrics** — the KPIs the company reports and manages to (ARR, NRR, customer count, gross retention, magic number, etc.). Every metric defined and its calculation explained.
- **Components of results of operations** — revenue, cost of revenue, operating expenses, non-operating items, income taxes; each with a definition and a period-over-period discussion of drivers.
- **Comparison of results** — current period vs. prior period, with dollar and percentage changes, and *quantified drivers* for each variance ("Revenue increased $X primarily due to a $Y increase from expansion in the enterprise segment and a $Z increase from new customer acquisition, partially offset by a $W decrease from customer churn").
- **Liquidity and capital resources** — cash sources and uses, working capital, off-balance-sheet arrangements, contractual obligations.
- **Critical accounting policies and estimates** — the accounting positions where management judgment is most significant (revenue recognition, stock-based comp, income taxes, goodwill / intangibles impairment). Each explained in enough detail for a reader to understand the assumptions and the sensitivity.

The MD&A is the CFO's writing; delegating it to an FP&A analyst or to outside counsel and reviewing only produces a document that reads as legal boilerplate and gets an unfavourable SEC comment. The CFO who cannot personally write a defensible MD&A is not yet ready to be a public-company CFO.

## Dual-track — the parallel-process choreography

The dual-track runs the IPO process and a private-market alternative in parallel through the T−18 to T−3 month window, then converges on one path.

**The parallel private tracks (any one or a mix of the below):**
- **M&A.** Engage a bank on a sell-side mandate; produce a management-presentation deck; run a targeted process of 10-25 strategic and financial buyers; receive indications of interest, then non-binding LOIs, then definitive-agreement diligence. The M&A path can run ~4-6 months from mandate to signing.
- **Late-stage private round.** Continue conversations with growth investors, sovereign-wealth-fund LPs, or strategic-corporate investors interested in a pre-IPO round. Round-shape typically resembles a late-stage priced Series-D/E or a crossover round.
- **Secondary tender or tender-offer / structured secondary.** Provide employee / early-investor liquidity through a formal tender at a set price; can operate in parallel with any of the above.

**The parallel IPO track:** the T−18 to T−3 workstream from the timeline above.

**The convergence.** Somewhere in the T−6 to T−3 window, the CFO / CEO / board choose a path — IPO, sale, private round, or "wait for a better window." The choice reflects: relative valuation (private cap vs. public trading multiple on comparable companies), timing certainty (M&A is typically more certain in the near term, IPO market can close), operating-model fit (public-company operating discipline vs. private-company optionality), stakeholder mix (existing investor liquidity needs, founder / management preferences), and market conditions.

**The choreography cost.** Running both tracks doubles the CFO / General Counsel / CEO calendar for ~9-12 months, adds meaningful outside advisor cost (both banks retained, both counsel retained), and requires the finance team to produce two overlapping-but-distinct diligence packages. The offset is optionality — a well-run dual-track has meaningfully better outcomes than a single-track process on either the IPO or the M&A side when the eventual path is uncertain at the start.

**Confidentiality across tracks.** The IPO track requires standard SEC-compliant disclosure discipline; the M&A track requires standard M&A-process confidentiality. Cross-contamination — a rumour of the M&A process affecting the IPO comparable set, a rumour of the IPO affecting the M&A process bidding — is a specific risk the CFO manages with the CEO, the counsel, and the banks.

## The CFO's post-IPO calendar

Post-IPO, the CFO's calendar shifts:

- **Quarterly-earnings cycle.** ~30% of calendar time — earnings release, earnings call, 10-Q, guidance update, investor follow-ups.
- **Sell-side / buy-side management.** ~20% — analyst-day, ongoing calls, conference attendance (typically 8-12 per year).
- **Board / audit committee.** ~15% — monthly audit-committee, quarterly board, annual meeting, proxy prep.
- **Operating finance.** ~25% — the standing operating CFO work — planning, capital allocation, M&A / bolt-on activity, treasury, tax, controls.
- **Regulatory / compliance.** ~10% — SOX ongoing, SEC filings, insider-trading window management, exchange-listing compliance.

The former private-company CFO's calendar of ~50-60% operating and ~40-50% deals shifts to ~25% operating and ~50% market-facing and ~25% regulatory. This is the specific reason some pre-IPO CFOs step aside for a public-company-experienced CFO at the IPO — the calendar shape is materially different, and the pre-IPO CFO's fit to it varies.

## Summary

- The pre-IPO workstream is 18-24 months of choreographed audit, controls, close, tax, and S-1 work leading to a filing, roadshow, and pricing.
- The two-year audit requirement is the gating constraint — the first audit's commit-and-completion date determines the earliest possible IPO fiscal year.
- PCAOB-registered auditor, SEC / PCAOB independence rules, and audit-committee pre-approval of non-audit services govern the auditor relationship.
- Public-company close compresses to 3-5 days for month-end and 5-7 days for quarter-end, followed by 4-14 days of quarterly-reporting work culminating in the 10-Q.
- SOX-404 is the formalisation of SOX-lite; §404(a) management assessment applies from year 1; §404(b) auditor attestation is deferred up to five years for JOBS Act EGCs.
- S-1 drafting is a multi-workstream project across ~4-6 formal drafts; the CFO owns the financial sections and cross-reviews for consistency.
- MD&A is the CFO's most-scrutinised writing; the CFO must author it personally.
- Dual-track runs IPO and a private-market alternative in parallel to preserve optionality; costs are meaningful advisor spend and CFO calendar burden; offset is materially better outcome distribution.
- The transaction-execution mechanics themselves defer sideways to `startup-exit-curriculum`.

Chapter 9 closes the module with the ownership boundary the whole track has been operating inside.
