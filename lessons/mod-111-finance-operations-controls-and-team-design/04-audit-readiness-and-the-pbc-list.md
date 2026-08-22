# Audit-Readiness and the PBC List — The First Outsourced Audit and the Two-Year Requirement

## Why this matters

At some point — usually at Series-B, sometimes earlier if a lead investor demands it, sometimes later if the company delays it — the finance function commits to its first outsourced audit. The audit is a GAAP-basis, independent-CPA-firm examination of the company's financial statements, issued as an audit opinion (unqualified, qualified, adverse, or disclaimer) that the board, the lead investor, and eventually the SEC can rely on. It is the moment the company's finance function is graded by someone outside the company for the first time.

The audit is also the beginning of a rolling annual project. Once the first audit is committed, every subsequent year needs a *comparative* audit — meaning the trailing twelve months as well as the prior year both audited — and any subsequent fundraise or IPO will ask for the audit history as a baseline diligence item. The IPO S-1 specifically requires **two years of audited financial statements** for an EGC (emerging-growth company, most venture-backed IPOs) or three years for a non-EGC. If the first audit is committed the year of the IPO, the CFO cannot deliver the two-year history in time and the IPO slips a year. This is the specific reason "when to commit to the first audit" is a high-stakes CFO decision, not an operational one.

The audit itself is 80% audit-prep and 20% audit. The prep work — assembling the PBC (prepared-by-client) list, reconciling the twelve months of closes to auditor-grade, documenting the accounting policies, walking the auditor through the systems — is the finance-ops team's project. The audit fieldwork the CPA firm runs is the last chapter of that project. A company that does its year-round work well runs a six-to-eight-week audit; a company that treats audit as a January-through-May scramble runs a five-month audit and hires 30% more temporary help to survive it.

## What the auditor is doing

The auditor's job — per PCAOB and AICPA auditing standards — is to gather sufficient appropriate evidence to opine on whether the financial statements present fairly in all material respects the financial position of the company (balance sheet), the results of its operations (P&L), and its cash flows (cash-flow statement), in conformity with GAAP.

Practically that decomposes into:

- **Understand the entity and its environment** — how the company makes money, what its risks are, what its control environment looks like.
- **Understand the accounting policies** — revenue recognition (ASC 606), stock-based compensation (ASC 718), leases (ASC 842), income taxes (ASC 740), business combinations (ASC 805) if applicable, and any industry-specific standards.
- **Test balances** — verify balance-sheet accounts by testing samples of transactions, agreeing sub-ledger totals to the GL, confirming AR balances directly with customers, confirming cash balances directly with banks, testing revenue recognition against contracts.
- **Test transactions** — verify P&L accounts by testing a sample of transactions to source documents.
- **Test controls (if reliance planned)** — if the auditor plans to reduce substantive testing by relying on the company's controls, they test the operating effectiveness of those controls.
- **Perform analytical procedures** — trend analysis, ratio analysis, unexpected-relationship investigation.
- **Evaluate management estimates** — deferred-revenue schedule, allowance for doubtful accounts, useful lives of fixed assets, stock-based-comp forfeiture rate, income-tax valuation allowance.
- **Concluding procedures** — subsequent events review, management representation letter, engagement quality review, issuance of the audit opinion.

The finance team's job during audit is to give the auditor everything they need to do the above, quickly and accurately, in a well-organised trail.

## The PBC list — prepared-by-client

The PBC (prepared-by-client) list is the auditor's inventory of every document, schedule, and reconciliation they need from the company to run the audit. For a first-time Series-B audit, the PBC list typically contains 150-400 line items. The CFO / Head of Accounting owns the response.

The PBC list groups roughly into:

- **Corporate documents.** Certificate of incorporation, bylaws, board minutes for the audit period, board consents, stockholder consents, cap table, stock purchase agreements, convertible-note / SAFE documents, option-grant approvals, subsidiary formation documents, related-party disclosures.
- **Financial statements and trial balance.** Draft consolidated financial statements, trial balance per legal entity, consolidating worksheets, closing entries, journal-entry population for testing.
- **Cash.** Bank confirmations, bank statements for every account for every month, bank reconciliations, wire logs, treasury investment statements.
- **AR and revenue.** AR aging, customer confirmation letters (send-out), contract population for revenue testing, contract copies for selected customers, revenue-recognition subledger, deferred-revenue roll-forward, ARR / ACV walk, customer credit-memo log.
- **Fixed assets and intangibles.** Fixed-asset roll-forward, capex additions with support (POs, invoices), depreciation calculation, capitalised-software policy and calculations, intangible-asset amortisation schedule.
- **Accounts payable and accrued liabilities.** AP aging, accrued-liability schedule with support, un-recorded-liability search evidence, subsequent-payment log for cutoff testing.
- **Debt.** Loan agreements, amortisation schedules, debt-covenant compliance certificates, warrant schedules.
- **Equity.** Cap table, stock-issuance log, stock-option grant support (board approval, grant agreements, 409A valuations), stock-based-comp expense calculation, ASC 718 Black-Scholes support, ESPP support if applicable.
- **Revenue recognition detail.** Signed contract copies for revenue-testing sample, executed order forms, delivery / go-live confirmations, credit memos and refunds, gross-vs.-net analysis (mod-101 chapter 5), performance-obligation identification and allocation memos, standalone selling price analysis.
- **Payroll and stock-based comp.** Payroll registers, payroll-tax filings (941s, W-3s, state), Carta / Shareworks reports, ESPP participation reports, executive compensation summary.
- **Income tax.** Tax provision calculation, deferred-tax roll-forward, uncertain-tax-position analysis, R&D-credit calculations (chapter 6), state / local tax filings, international tax filings.
- **Sales tax.** Nexus study (chapter 7), sales-tax filings by state, marketplace-facilitator schedules, Anrok / Avalara / TaxJar reports.
- **Legal and contingencies.** Attorney letter (the "audit inquiry letter" — a formal auditor request to outside counsel for a list of pending or threatened litigation), contract commitments (leases, purchase commitments, minimum-guarantees), indemnification exposures.
- **Related-party transactions.** Director / officer transactions with the company, sister-company transactions, founder loans, related-party service agreements.
- **Subsequent events.** Events between the balance-sheet date and audit-issuance date that require disclosure or adjustment.

PBC-list management is a project-management discipline. Tag every line item with owner, target-due-date, status, and location (link to the reconciliation, the schedule, or the document in a well-organised audit-workpaper folder). FloQast, Blackline, AuditBoard, and Workiva all offer PBC-list workflow; a well-run Google Sheet with the same discipline works at Series-B scale.

## Auditor selection — Big Four vs. mid-market vs. boutique

The auditor pool for venture-backed startups splits roughly:

- **Big Four (Deloitte, PwC, EY, KPMG).** The default for companies on the pre-IPO track, for companies where the lead investor's LPs expect a Big Four audit, and for companies large enough that the audit fee is not prohibitive. Fees typically start at $150K-$400K for a first-year Series-B audit and scale up. The advantage: institutional knowledge, deep industry teams, seamless SEC reviewer familiarity when the IPO comes. The disadvantage: cost, and less senior-team attention on a mid-market client.
- **Second-tier national firms (BDO, Grant Thornton, RSM, CBIZ, Baker Tilly).** The middle segment. Fees typically $75K-$250K. Advantage: better ratio of partner attention, competitive on price, most are PCAOB-registered (verify for the specific firm — required if IPO is on horizon). Disadvantage: less SEC-review reps for the eventual S-1, though this is often overstated.
- **Startup-specialist boutiques (Frank Rimerman, WithumSmith+Brown, Armanino, PKF O'Connor Davies, and regional firms).** The smaller end. Fees typically $50K-$150K for a first-year Series-B audit. Advantage: hands-on partner-led work, deep startup fluency, pragmatic on emerging-company issues. Disadvantage: for the IPO track, most companies switch to Big Four in the year of or the year before the S-1 filing, which means transferring the audit history.

The CFO decision matrix:

- **If the IPO track is committed within 2-3 years** — hire Big Four now, avoid the switch. The switch itself is expensive (transferring workpapers, re-orienting the audit team, sometimes re-performing prior-year procedures) and can slip the S-1 timeline.
- **If the IPO track is a possible-not-committed** — a PCAOB-registered second-tier firm is often the right choice; can switch to Big Four later if needed with a manageable transition cost.
- **If the IPO track is deferred or the exit is likely M&A** — a startup-specialist boutique is usually the best value.

Independence is the constraint that overrides all of the above. The auditor cannot provide bookkeeping, financial-statement preparation, valuation services, or tax-provision preparation for the audit client — SEC and PCAOB independence rules. The company's outsourced tax firm (chapter 6 on R&D credit; chapter 7 on sales tax) must be a *different firm* from the auditor. If the auditor's tax practice would otherwise be the natural fit, either use their firm's tax practice for advisory only (not preparation) or pick a different tax firm.

## The year-one deficiencies that recur

Every first-year Series-B audit surfaces a similar set of findings. Naming them in advance shortens the audit and reduces the "material weakness" or "significant deficiency" flags that would otherwise appear in the audit's communications-with-those-charged-with-governance letter (the "management letter"):

- **Segregation of duties.** At small headcount the same person books the entry, approves the entry, and reconciles the account. The auditor documents this as a deficiency; the response is chapter 5's compensating controls.
- **Stock-based compensation.** Missing board approvals, grant-date confusion (approval date vs. offer date vs. accepted date), 409A valuations that don't cover the grant date, Black-Scholes inputs (volatility, risk-free rate, expected term) not documented.
- **Revenue recognition.** Contracts without signed order forms, performance obligations bundled where they should be separate, standalone-selling-price methodology undocumented, revenue booked before delivery, credit memos issued outside a control process.
- **Cutoff.** Invoices dated wrong (year-end scramble to hit a bookings number), un-invoiced services delivered in the audited year but revenue not accrued (or vice versa), vendor invoices for services in the audited period not booked in the correct period.
- **Cash controls.** Wire transfers without dual approval, corporate card charges without documented business purpose, expense-report backup missing, per-diem or founder-reimbursement without policy.
- **Fixed assets and capitalised software.** Capitalised-software costs including ineligible activities (research, planning, post-implementation), fixed-asset additions without approval trail, depreciation started before asset placed in service.
- **Related-party transactions.** Founder loans, sister-entity revenue, board-member contracts without independent-director approval or disclosure.
- **Income tax.** Tax provision as a Q4 exercise instead of a year-round accrual, deferred-tax roll-forward with unexplained variances, R&D-credit position without contemporaneous documentation (chapter 6).

The Head of Accounting owns the year-round work to prevent these findings from recurring. The CFO owns the response to any material-weakness finding — including the disclosure implications if the company is on the IPO track (a material weakness in the last-year audited financials creates a specific disclosure obligation in the S-1 and can delay the offering).

## The two-year IPO requirement

The specific mechanic that dictates the audit-commit timing: SEC Regulation S-X requires an IPO S-1 to include audited balance sheets for the two most recent fiscal year-ends and audited income statements, cash-flow statements, and statements of stockholders' equity for the three most recent fiscal years (or two for an EGC under the JOBS Act, which covers most venture-backed IPOs). The audited comparative period cannot be produced retroactively unless the company has run through the reconciliations, controls, and documentation of a full audit for each period.

Practical implication: **if the company wants to file an S-1 in fiscal year N, the first audit must cover fiscal year N-2 or earlier.** For a company planning a 2028 IPO, the FY2026 audit is the minimum-viable first audit; a FY2025 first audit gives more margin. Committing later than that means the IPO slips or the company files as an "emerging growth company" with reduced disclosure, but even that still requires two years of audited financials.

The corollary: the CFO's IPO-timing conversation with the board (chapter 8) is inextricable from the audit-commit conversation. A board that wants an IPO on a two-year horizon has already committed to the audit history whether or not it has been formally decided.

## The audit committee

The audit itself is signed off by the audit committee of the board (mod-110 chapter 6). The CFO reports the audit progress to the audit committee at quarterly cadence during the year, ramps to monthly during audit fieldwork, and presents the year-end audit results to the audit committee for approval before the audit is finalised. The audit committee formally engages the auditor, formally approves auditor fees, and formally reviews the auditor's independence letter each year.

Committee-formation timing matters: pre-audit-commit, the CFO reports audit-related items to the full board; post-audit-commit and certainly by IPO, the audit committee is a standing independent-director-majority committee. mod-110 chapter 6 covers charter, cadence, and independent-director requirements.

## The auditor as a diligence artifact

Post-audit, the audit opinion and the audited financial statements become a diligence artifact used in every subsequent capital-markets transaction:

- **The next fundraise.** Lead investors expect the audited financials as a baseline diligence input; a Series-C without them is possible but signals that the finance-ops program is behind schedule.
- **The debt facility.** Venture debt and growth debt underwriters (mod-109) require audited financials at closing and for periodic covenant certification.
- **The M&A process.** An acquirer's diligence team starts with the audited financials; unaudited financials trigger a longer, more expensive diligence process and typically an escrow adjustment for uncertainty.
- **The IPO.** As above, the two- or three-year history is the entry price.

The audit is not a compliance exercise; it is the CFO's ongoing certification to the capital markets that the finance function is operating at the standard the next transaction will require.

## Summary

- The audit is an independent-CPA-firm examination of GAAP-basis financial statements, issued as an audit opinion; typically committed at Series-B, sometimes earlier.
- The PBC list is the auditor's inventory of documents and schedules needed from the company; well-run PBC-list project-management is the difference between a six-week audit and a five-month audit.
- Auditor selection splits Big Four / second-tier / startup-boutique, driven mostly by IPO trajectory and independence constraints.
- Year-one deficiencies recur across companies (segregation of duties, stock-based comp, revenue recognition, cutoff, cash controls); pre-empting them is the year-round work.
- The IPO S-1 requires two years of audited financials for an EGC; the first audit's commit date must precede the planned S-1 by at least two full fiscal years.
- The audit opinion becomes a diligence artifact used in every subsequent transaction.

Chapter 5 turns to the controls the auditor will test.
