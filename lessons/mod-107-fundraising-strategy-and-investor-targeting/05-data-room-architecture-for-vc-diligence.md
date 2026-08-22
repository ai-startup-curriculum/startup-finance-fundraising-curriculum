# Data Room — Architecture for VC Diligence

## Why this matters

A data room is the specific, structured, access-controlled collection of documents a venture fund reads during diligence. It is what the fund's associate is combing through the week before the term sheet is finalised and what the fund's legal counsel is opening in the week after. A well-organised data room compresses the diligence window and reduces the number of "can you send me..." back-and-forth requests. A disorganised data room, or one missing critical documents, extends diligence, introduces doubt, and — in the worst case — kills a deal that had a signed term sheet.

The CFO owns the data room. The founder-CEO owns the story. The two roles run in parallel through the raise, and the data room becomes the CFO's central artifact once the sponsoring partner starts asking for diligence materials — typically after the second or third meeting. This chapter walks the canonical folder structure, the seven canonical sections, the recommended access-tiering pattern, the diligence-request checklist, and the sharing pattern that prevents confidential information from leaking outside the fund.

## The seven canonical sections

Every venture-capital data room contains variations on the same seven sections. The specific names differ by advisor and fund; the substance is stable. The canonical set:

1. **Corporate documents.** Incorporation, bylaws, board minutes, prior financing documents.
2. **Financials.** Financial statements, financial model, KPI dashboard.
3. **Cap table and equity.** Cap table, option-pool documentation, equity-issuance history.
4. **Customer and revenue.** Customer contracts, ACV list, cohort retention, top-customer concentration.
5. **Product and IP.** Product roadmap, IP assignments, patents, trademarks, open-source policy.
6. **Team and organisational.** Team roster, hiring plan, key employment agreements, org chart.
7. **Legal and other.** Employee legal, customer legal, vendor contracts, insurance, litigation history.

The specific documents in each section are enumerated below. A CFO staging a data room for a seed or Series-A round should treat this as a checklist and populate each section with the specific documents the fund's diligence associate will ask for.

## Section 1 — Corporate documents

The corporate-documents section establishes the company's legal existence, ownership, and governance. It is the first section the fund's legal counsel reads and is the foundation for every other section (a cap table only means something if the underlying incorporation and stock-issuance documents establish the shares).

**Documents:**

- **Certificate of Incorporation.** The current, effective certificate as filed with the Delaware Secretary of State (assuming Delaware, which most VC-backed startups are). Include any amendments — for example, a "Restated Certificate" from a prior priced round with then-current preferred-stock terms.
- **Bylaws.** Current bylaws as adopted by the board.
- **Board resolutions and minutes.** Every board meeting since inception (or since the last priced round). At seed / Series-A, this is often a small number of resolutions — incorporation, board-composition changes, prior-round approvals, key hires' equity grants.
- **Prior-round financing documents.** For every prior priced round, the Series-Seed or Series-A Stock Purchase Agreement, Investor Rights Agreement, Voting Agreement, Right of First Refusal and Co-Sale Agreement, and Restated Certificate. For every SAFE, the executed SAFE.
- **Convertible instrument stack.** Every outstanding SAFE, convertible note, or other convertible instrument, with amendments and side letters (mod-105 chapter 5).
- **83(b) elections filed for founders.** Confirmation that each founder filed the 83(b) within 30 days of stock grant (mod-104).
- **Stock-issuance history.** Detailed history of every stock issuance since incorporation with dates, share counts, and consideration.

**CFO note.** The corporate-documents section is where a sloppy company shows up badly. Missing board minutes, incomplete SAFE stack, undocumented stock issuances — all catch the fund's counsel and force the "please confirm and provide" cycle. Getting this section clean before the raise even starts is a specific-preparation step every CFO should do.

## Section 2 — Financials

The financials section is what the fund's diligence associate reads to confirm the numbers on the deck (chapter 4). It is what the sponsoring partner references in the partner meeting when a partner asks "what does the burn look like at the ARR band?"

**Documents:**

- **Historical financial statements.** Monthly P&L, balance sheet, and cash-flow statement for the past 24 months (or since inception, if under 24 months). Reconciled monthly (mod-101, mod-103). If the company is on cash-basis at seed, provide both cash-basis and accrual-basis (mod-101 chapter 6) if accrual is available; the fund will underwrite off accrual.
- **Financial model.** The driver-based three-statement model (mod-103) showing 24-36 month projections against the milestone bar (chapter 1). Include the assumptions tab, driver tab, hiring plan, and KPI dashboard.
- **KPI dashboard.** The reconciled KPI dashboard from mod-103 chapter 8 with monthly historical data and forward projections.
- **ARR waterfall / bridge.** How ARR moved month-over-month for the past 12-24 months: starting ARR, new-ARR, expansion, churn, ending ARR. Compounding the four numbers month-over-month is the reconciliation.
- **Revenue-recognition policy.** For SaaS, the ASC 606 revenue-recognition policy — what is recognised, over what period (mod-101 chapter 2).
- **Bookings-billings-revenue-cash reconciliation.** For SaaS, the four-number reconciliation (mod-101 chapter 3). Fund diligence will ask.
- **Budget vs. actual.** Historical monthly budget-vs-actual for the past 12 months, with variance explanations. Signals the CFO's forecasting discipline.
- **Deferred revenue and DSO.** Deferred-revenue balance and days-sales-outstanding trend. For SaaS companies with annual prepay contracts, the deferred-revenue reconciliation matters.
- **Cash-runway analysis.** Current cash, monthly burn, cash-out date at the current burn rate, and the milestone-bar plan's projected runway (chapter 1).

**CFO note.** The financials section is where the CFO's mod-103 work pays off. A driver-based model that can accept a sensitivity request from the fund ("what happens if you slow hiring by 3 months?") in an hour and return with a rerun is a load-bearing signal of the CFO's competence. A model that requires the CFO to spend three days rebuilding it to answer the question is not.

## Section 3 — Cap table and equity

The cap-table section is what the fund's counsel reconciles to confirm ownership and voting arithmetic. It is also what feeds the pro-forma cap table the term-sheet analysis will produce (mod-108).

**Documents:**

- **Current cap table.** Fully-diluted cap table with every stockholder, every option holder, every warrant holder, every SAFE / note holder, and every reserved-but-unissued option. Formats: Carta / Pulley / Ledgy export, plus an Excel version for downloadable analysis.
- **Pool-shuffle math.** The pool-shuffle arithmetic from mod-104 chapter 2 showing how the option pool is sized and where the ESOP top-up is coming from at the incoming round.
- **Options ledger.** Every option grant since inception with grant date, strike price, vesting schedule, and current vesting status.
- **409A history.** Every 409A valuation since inception with the valuation date, methodology, and resulting strike price (mod-104 chapter 5).
- **Founders' equity documentation.** Restricted stock purchase agreements for each founder, with vesting schedule and any acceleration triggers.
- **Employee stock agreements.** The current form of stock-option agreement used for employees.
- **Waterfall analysis.** For the current cap table, a liquidation-waterfall showing the return to each holder class at several exit-price scenarios (mod-104 chapter 4). Useful for the term-sheet-preference discussion.

**CFO note.** A cap table that does not reconcile is a red flag that fund counsel will not let go. If the Carta export shows 12,345,678 fully-diluted shares and the Excel version shows 12,345,679, someone will spend the next three days finding the missing share. Reconciling before the raise starts is a specific-preparation step.

## Section 4 — Customer and revenue

The customer section is what the fund's associate reads to underwrite the revenue quality — is the revenue real, is it durable, is it concentrated, and does the churn profile match the deck's claim.

**Documents:**

- **Customer list.** Every current customer with ACV, contract start date, contract end date, product tier, and payment terms. Anonymised if necessary (Customer A / Customer B), with the mapping preserved for reference calls under NDA.
- **Top-10 customers concentration.** Percentage of ARR contributed by the top 10 customers. Fund will flag if concentration is >50% at seed or >30% at Series-A.
- **Cohort retention curves.** Monthly cohorts showing revenue retention over time (mod-102). Both gross retention and net retention.
- **Churn analysis.** Reason-coded churn for the past 12-24 months. What percentage churned for what reason.
- **Standard customer contract.** The standard MSA (master services agreement) and standard order form. Fund counsel will read for auto-renewal terms, uncapped liability, unusual assignment restrictions.
- **Customer references.** A list of 5-10 customers who are willing to take reference calls. The CFO manages the reference list and works with customers to prepare them for the fund's calls (typically the fund calls two to four references).
- **Pipeline detail.** Current pipeline by stage and expected close date. Some funds ask for pipeline; others do not.

**CFO note.** The customer section is the section where the deck's claims about traction get validated or invalidated. A deck that claims 130% NRR and a cohort table that shows 110% NRR is a deck whose claim will be corrected in diligence — better to have the deck be honest.

## Section 5 — Product and IP

**Documents:**

- **Product roadmap.** 12-24 month product plan with milestones.
- **Product architecture overview.** A brief technical description of the product architecture. Useful for the fund's technical diligence.
- **IP assignments.** Every founder and every employee has signed an IP-assignment agreement (Proprietary Information and Inventions Assignment, or "PIIA"). Contractors who have contributed code have signed the equivalent for their work. Fund counsel will confirm this coverage — a company where a former contractor still holds IP rights to material code is a company with an IP problem.
- **Patents and trademarks.** Any filed patents, trademarks, or copyright registrations, with the current status.
- **Open-source policy.** How the company uses open-source software. Any GPL-family dependencies (which can carry viral licensing implications).
- **Product security.** SOC 2 status (in-progress, Type I, Type II). Penetration test results, if available. Data-encryption and key-management policy.
- **Product demo access.** Access to a product demo environment or a walkthrough video for the fund's technical diligence.

**CFO note.** The IP section is one place where fund counsel can find surprises that end a deal. If a founder's prior employer has a plausible IP claim on the target company's core technology, the fund will require an indemnification or the deal will not close. The CFO's job is to know these risks before the fund's counsel does.

## Section 6 — Team and organisational

**Documents:**

- **Team roster.** Every employee and contractor with title, start date, cash compensation, equity, and reporting line.
- **Org chart.** Current org chart plus a 6- and 12-month planned org chart.
- **Hiring plan.** Detailed hiring plan aligned to the milestone-bar operating plan (chapter 1).
- **Key employment agreements.** Founders' and executives' employment agreements, offer letters, and any equity acceleration terms.
- **Consultants and contractors.** List of consultants and contractors with material work relationships.
- **Compensation benchmarking.** Compensation benchmarks used to set current pay (Carta Comp, Pave, Option Impact). Signals the CFO's discipline on comp.
- **Advisory board.** Advisors and advisory-board members with their equity.

## Section 7 — Legal and other

**Documents:**

- **Employment law.** Employee handbook, PTO policy, standard offer letter template, standard NDA and IP-assignment templates.
- **Litigation history.** Any past, present, or threatened litigation. Even a threatened claim goes here; fund counsel will find out later if it is not disclosed and the deal will be at risk.
- **Insurance.** Current insurance policies — general liability, D&O, cyber, professional. Coverage limits and expiration dates.
- **Vendor contracts.** Material vendor contracts (>$50K/year, or specific to the business — e.g., a hosting-provider contract).
- **Real estate.** Lease agreements for office space (if any).
- **Tax.** Federal, state, and local tax filings. R&D tax-credit history (if applicable). Sales-tax nexus footprint.
- **Regulatory.** Any industry-specific regulatory approvals or licences (healthcare, fintech, defence — the specific regime).
- **Prior diligence memos.** If the company has been through diligence before (a prior round, an acquisition offer), a scrubbed version of the prior diligence process's request list is a useful reference.

## The recommended read order

The fund's diligence process typically reads the data room in the following order (though every fund is slightly different):

1. **Financials** — is the traction real, and is the burn sustainable through to the next milestone?
2. **Customer and revenue** — is the revenue quality durable?
3. **Cap table** — what is the ownership structure, and what does the pro-forma cap table look like post-round?
4. **Corporate documents** — is the corporate structure clean, and are the prior-financing documents standard?
5. **Team** — who are the people, and are they the right people?
6. **Product and IP** — is the technology defensible, and is the IP clear?
7. **Legal and other** — any surprises?

The CFO's job is to lay out the read order in the data room's landing README (a top-level document that says "start here"). Even something as simple as "we recommend reading in the following order: /financials → /customers → /cap-table → ..." accelerates the fund's diligence and signals professionalism.

## Access tiering — the sharing pattern

Not every fund gets access to every document at every stage. A well-designed data room uses **access tiers** to stage what a fund sees at each funnel stage. The specific pattern:

**Tier 1 — Public (deck only).** The pitch deck (chapter 4) is shared with any warm-intro fund pre-first-meeting. No access to the data room. DocSend or similar link with view-only access.

**Tier 2 — First-meeting supplement.** After a productive first meeting, a small subset of the data room may be shared: high-level financial highlights (revenue-per-quarter chart), top-line cap table, product overview, team bios. Still no access to the primary data room.

**Tier 3 — Serious-diligence access.** After the sponsoring partner commits to bringing the deal to a partner meeting, the fund gets access to the primary data room. Restricted view — watermarked documents, download disabled on the most sensitive documents (customer contracts, employment agreements). NDA typically signed before Tier 3 access.

**Tier 4 — Post-term-sheet full access.** Once the term sheet is signed and the exclusivity / no-shop period is in effect, the fund gets full access — download-enabled, complete document set, direct access to customer references. This is the "confirmatory diligence" period.

**The tools that support tiering.** Common data-room platforms: DocSend, Google Drive (with careful permission management), Dropbox, Notion, dedicated VDR products (Firmex, Datasite, Intralinks). For a seed / Series-A round, a well-organised Google Drive or DocSend is usually enough. For a Series-B / C or a public-company-adjacent round, a dedicated VDR provides better audit-trail and permission controls.

## The diligence-request checklist

Every fund's diligence process sends the target company a "diligence request list" — the specific documents the fund wants. A well-prepared CFO can respond to most of the list from the existing data room, with minimal ad-hoc collection needed.

**A canonical VC diligence request list contains** (approximately — every fund's list is slightly different):

- Financial statements (past 24 months, current, projected).
- Financial model with sensitivity.
- Bookings-billings-revenue-cash reconciliation.
- Cash runway and burn analysis.
- KPI dashboard with historical and projected data.
- Cohort retention curves and churn analysis.
- Top-10 customer concentration and current MRR/ARR contribution by customer.
- Standard customer contract and material customer contracts (e.g., >$100K ACV).
- Cap table and options ledger.
- 409A history.
- All prior financing documents (SAFEs, notes, priced-round docs).
- Board consent history / minutes.
- IP assignments for all founders / employees.
- Litigation history.
- Insurance policies.
- Team roster and compensation.
- Hiring plan.
- Product roadmap.
- SOC 2 / security materials.
- Vendor contracts (material).
- Real-estate contracts.

**The CFO's pre-raise preparation.** Build the data room *before* the raise starts. Not the week after the sponsoring partner requests diligence access. A CFO who has the data room ready on day 1 of the raise is a CFO who compresses the diligence window and produces a better close outcome.

## Audit trail and access management

**Every access grant should be logged.** Which fund got Tier 3 access on what date, which specific documents they viewed, which they downloaded (if downloads were enabled), and which are still under review. A specific-fund access history is useful for the funnel management (chapter 3) and, in the worst case, for a subsequent dispute.

**Every access grant should be revocable.** When a fund passes, the CFO revokes Tier 3 access (and Tier 4 if it was granted). Passed funds should not retain access to the primary data room.

**Sensitive documents should be watermarked.** Every downloaded PDF from the data room should have a per-fund watermark ("Confidential — shared with [Fund Name] on [Date]"). If a document later shows up outside the recipient fund, the leak source is identifiable.

**No customer-identifiable information without customer consent.** Customer contracts, customer names on cohort tables, and customer references should be either anonymised or explicitly cleared with the customer. Some customers will not allow their name to be shared with third parties without a specific NDA; respect that.

## Common data-room traps

- **Building the data room during the raise.** A raise where the CFO is scrambling to assemble documents at 11pm on the day the fund's diligence associate has requested them is a raise that reads as disorganised.
- **Missing documents.** Every gap in the data room becomes a "please provide" request from fund counsel, extending diligence. Filling the gaps before the raise starts is cheaper.
- **Un-reconciled cap table.** The Carta cap table and the Excel cap table disagreeing by a share is a red flag. Reconcile before the raise.
- **Undisclosed litigation or IP claims.** If the fund's counsel finds it and the target company did not disclose it, the deal breaks. Disclose everything material.
- **Poor access management.** Every fund on the raise's target list getting Tier 3 access to the data room from day 1 is a data-room-security failure. Stage access carefully.
- **Un-watermarked sensitive documents.** Downloaded customer contracts that show up in a competitor's inbox six months later are a serious risk. Watermark.
- **No landing README.** A data room without a "start here" document forces the fund to figure out where to start, which extends diligence.
- **Documents in inconsistent formats.** Mixing PDF, Excel, Google Doc, and Word for the same document type reads as unprofessional. Pick a format per section and stick to it.
- **Historical documents missing.** Board minutes for the past 24 months missing three specific meetings is a red flag. Complete the record.

## What good looks like

A well-organised data room:

- Has all seven canonical sections populated before the raise starts.
- Has a top-level README that recommends a read order for the diligence process.
- Uses access tiering to stage what each fund sees at each funnel stage.
- Has a per-fund audit trail of who accessed what and when.
- Uses watermarks on downloaded sensitive documents.
- Has customer-identifiable information anonymised or under explicit NDA.
- Has the cap table reconciled across sources (Carta, Excel, prior-round documents).
- Has the financial model in a state that supports live sensitivity requests from fund diligence.
- Has the diligence-request checklist pre-mapped to the data-room folders so the CFO can respond to any fund's request list in hours, not days.
- Is maintained through the raise — updated as new financial months close, updated as new customer contracts are signed, updated as new employees join.

## Summary

- The data room is the central artifact of VC diligence and is CFO-owned. It stages the specific documents a fund's diligence process reads to confirm the deck's claims and underwrite the deal.
- Seven canonical sections: corporate documents, financials, cap table, customer and revenue, product and IP, team and organisational, legal and other.
- The recommended read order (financials → customer → cap table → corporate → team → product → legal) accelerates the fund's diligence and signals CFO professionalism.
- Access tiering (public deck → first-meeting supplement → serious-diligence access → post-term-sheet full access) stages what each fund sees at each funnel stage; NDAs, watermarks, and per-fund audit trails support the tiering.
- The diligence-request checklist is largely predictable across funds; a CFO who has the data room prepared before the raise starts responds to any fund's request in hours rather than days.
- Common traps: building the data room during the raise, missing documents, un-reconciled cap table, undisclosed litigation or IP claims, poor access management, and un-watermarked sensitive documents.

Chapter 6 turns to DocSend engagement benchmarks — how to read the specific signal the deck itself produces (time-per-slide, drop-off, forward count) and iterate the deck against that signal.
