# The Guidance Stack — Primary Standards, Frameworks, and Practitioner Content

## Why this matters

The judgement calls in this module — is this a distinct performance obligation, am I a principal or an agent, do I have to move to accrual now — are governed by authoritative guidance issued by specific bodies. A CFO who cannot cite the authoritative source for a policy decision cannot defend the decision in an audit and cannot answer a diligence question with confidence. This chapter maps the stack — what is authoritative, what is interpretive, and where startup-specific practitioner content (Kruze, Pilot, Bench, and similar sources) fits alongside the primary sources.

The stack is not just a reading list; it is a hierarchy of authority. When practitioner content and an authoritative standard disagree, the standard wins. When two authoritative sources speak to the same issue (US GAAP and IFRS, for instance), the applicable one for the entity's reporting framework wins. Getting the hierarchy right is what makes the CFO's opinion carry weight.

## Tier 1 — Authoritative US GAAP

**FASB Accounting Standards Codification (ASC).** The Financial Accounting Standards Board's Codification is the single source of authoritative US GAAP for non-governmental entities. It is organised by topic (e.g., Topic 606 for revenue), subtopic, section, and paragraph. Access is via the FASB's public codification viewer (basic view free, professional view subscription-based).

The topics most relevant to this module:

- **ASC 606** — *Revenue from Contracts with Customers*. The five-step model (chapter 2). Governs the recognition, measurement, and disclosure of revenue for every SaaS subscription, professional-services engagement, marketplace transaction, and licence contract.
- **ASC 340-40** — *Other Assets and Deferred Costs — Contracts with Customers*. Governs the capitalisation and amortisation of contract-acquisition costs (sales commissions) and contract-fulfilment costs.
- **ASC 230** — *Statement of Cash Flows*. Governs the presentation of the cash-flow statement.
- **ASC 842** — *Leases*. Governs lessee accounting; brings operating leases onto the balance sheet as right-of-use assets. Out of scope for this module but relevant to the overall balance sheet.
- **ASC 810** — *Consolidation*. Governs when subsidiaries and variable-interest entities are consolidated. Relevant at scale.

FASB also publishes **Accounting Standards Updates (ASUs)** that amend the Codification. Between issuance and the effective date, an ASU is a preview of the amended text; after the effective date, the amendment is in the Codification. Track ASUs for topics you care about — the Codification's "cross-reference" and "amended-by" links show pending changes.

**AICPA Audit and Accounting Guides.** The American Institute of Certified Public Accountants publishes industry-specific and topic-specific guides — including *Revenue Recognition*, *Software Revenue Recognition*, and industry guides for technology companies. These are Category B authoritative under GAAP hierarchy and are the practitioner-level companion to the ASC text. They include worked implementation examples and are the reference an auditor's technical accounting group will cite when reviewing a complex judgement.

**SEC guidance for public companies.** Once a company is public (post-IPO), the SEC's Staff Accounting Bulletins (SABs), Financial Reporting Manual, and comment letters become authoritative-in-practice for public-company reporting. SAB 74 disclosures for pending new accounting standards, SAB 118 disclosures around tax-reform impacts, and the SEC's per-industry XBRL taxonomy all apply. Not directly relevant pre-IPO but a CFO on the pre-IPO track (mod-111) starts building the SEC-facing muscle here.

## Tier 2 — Authoritative tax guidance

**Internal Revenue Code (IRC).** The primary federal-tax statutory law. The provisions relevant to this module:

- **§446** — general rule on methods of accounting for tax purposes.
- **§448** — limitation on the use of cash method (the C-corp / partnership prohibition and the small-business exception).
- **§451** — general rule for taxable year of inclusion of income.
- **§461** — general rule for taxable year of deduction of expenses.
- **§471** — general rule on inventories, with the §471(c) small-business exception.
- **§263A** — uniform capitalisation of costs into inventory (UNICAP), with the small-business exception.
- **§481(a)** — adjustments required when changing a method of accounting.

**Treasury Regulations.** Regulations issued by the Treasury Department under authority of the IRC. Governing detail on the accounting-method-change rules is in Treas. Reg. §1.446-1 and following.

**IRS Publication 538 — *Accounting Periods and Methods*.** The IRS's plain-English practitioner guide to accounting periods and methods for tax purposes. It walks the cash and accrual methods, the hybrid method, restrictions on cash-method use, the mechanics of changing accounting methods, and Form 3115. It is not authoritative in the way the Code and Regulations are — it is IRS guidance — but it is the go-to first read for a CFO deciding on cash-vs.-accrual for tax.

**Form 3115 (*Application for Change in Accounting Method*)** and its instructions. Filed when a taxpayer changes accounting methods. Instructions include the specific consent procedures — automatic consent (Rev. Proc. 2015-13 as periodically updated) for changes on the DCN list, non-automatic consent for others.

**IRS Revenue Procedures.** Revenue procedures governing accounting-method changes are updated periodically. The CFO should not memorise the specific Rev. Proc. numbers; they should know the tax accountant / CPA will file the correct current procedure and can articulate the type of change being made (from cash to accrual, on all items, etc.).

## Tier 3 — Non-GAAP special-purpose frameworks

**AICPA Financial Reporting Framework for Small- and Medium-Sized Entities (FRF for SMEs).** A special-purpose framework published by the AICPA in 2013 as an alternative to full US GAAP for private companies that do not need GAAP financial statements. It is *not* GAAP — it is an "other comprehensive basis of accounting" (OCBOA). Notable features: modified accrual (a middle ground between pure cash and full accrual), simpler revenue-recognition rules than ASC 606, no deferred-tax computations (deferred taxes optional), simplified pension accounting, no consolidation of variable-interest entities.

For a startup that has crossed the point where cash-basis is inadequate but is not yet ready for a full GAAP audit — often the Series-A window — FRF for SMEs is a legitimate middle ground for internal reporting and for lender/investor packages where GAAP is not contractually required. It is not appropriate for a startup on a Series-B / IPO track because the transition from FRF for SMEs to full GAAP is a second restatement.

**Modified cash basis.** A hybrid where the primary basis is cash but certain accrual concepts are layered in — most commonly, tracking of AR / AP for major customers and vendors, and accrual of payroll and payroll taxes. Modified cash basis is common in outsourced-bookkeeping arrangements at seed stage. It is not a formal framework; the extent of accrual modifications is negotiated between the company and its CPA.

**Tax basis of accounting.** Some private companies produce financial statements on the tax basis — the same basis they file their tax return on — for lender and investor purposes. This is another OCBOA. It has the advantage of eliminating book-tax differences; it has the disadvantage of not being GAAP.

## Tier 4 — Startup-specific practitioner content

Practitioner content — blog posts, guides, template spreadsheets, calculators — from startup-focused outsourced-CPA firms and bookkeeping services is *interpretive*, not authoritative. Its value is in translating the standards and tax provisions into the specific workflows a startup CFO / outsourced accountant runs, and in surfacing the common patterns and pitfalls across many similar companies.

**Kruze Consulting** — a startup-focused outsourced-CPA firm publishing an extensive content library on startup tax, R&D tax credits, delayed 409A refresh, revenue recognition, month-end close, and audit prep. Practical, opinionated, and grounded in the reality of the seed-to-Series-C tax filings they run. Useful for benchmarking practices against the firm's stated methodology.

**Pilot** — outsourced-bookkeeping and outsourced-CFO services with a content library covering month-end close, ASC 606 for SaaS, deferred-revenue treatment, and stack-selection guidance. Pilot's content is aligned with their service offering (accrual bookkeeping, tax filing, R&D credits).

**Bench** — cash-basis-first outsourced bookkeeping targeting small businesses and early-stage startups. Bench's content is useful for the cash-basis pre-seed window; less relevant once accrual is required.

**Zeni, FinvisorAI, Botkeeper, and similar** — newer outsourced-accounting-plus-software offerings. Content varies. Assess the same way — is this consistent with ASC 606 / IRS / AICPA, is it grounded in actual practice, does the firm publish enough detail to be useful without engaging them?

**How to place practitioner content in the stack.** Read practitioner content as *examples of one firm's practice*, not as authoritative rules. When a Kruze blog post says "we recommend X for a Series-A SaaS," that is one firm's opinion informed by many client engagements; it is not the standard. Cross-reference the underlying ASC / IRS / AICPA text before adopting a practice from a blog post, especially for judgement-heavy issues (distinct-PO analysis, gross-vs.-net, capitalisation of commissions).

## Tier 5 — Adjacent references useful for context

**IFRS 15 — *Revenue from Contracts with Customers*.** The IASB standard converged with ASC 606 by the FASB / IASB joint revenue project. For a startup with international operations reporting under IFRS in some subsidiary jurisdictions, IFRS 15 is the equivalent standard. The five-step model is substantively identical; there are minor differences in specific implementation guidance and disclosures. Meritech / Bessemer comps that include IFRS-reporting European companies are cross-comparable at the revenue-recognition level.

**Big Four and second-tier accounting-firm technical publications.** Deloitte's *Revenue from Contracts with Customers — A Guide to IFRS 15 and ASC 606*, PwC's revenue guide, EY's revenue guide, KPMG's revenue guide. Non-authoritative but heavily-cited practitioner interpretation. When a specific fact pattern needs research beyond the ASC text and the AICPA guide, the Big Four guides are the next stop.

**FASB Emerging Issues Task Force (EITF) archive.** Historical positions on emerging accounting issues, largely subsumed into the Codification but occasionally the only source for a narrow legacy issue.

**Peer-company 10-K / S-1 disclosures.** Reading the revenue-recognition footnote in a peer company's 10-K (any public SaaS company's most recent Form 10-K, Note 2 or 3, "Revenue") is the fastest way to see how a mature company describes its ASC 606 policy for a specific SaaS pattern. Access via SEC EDGAR. Copy the *structure* of the disclosure, not the specific accounting treatment.

## The CFO's practical stack — how to actually use this

For any policy decision:

1. **Start with the objective and the specific fact pattern.** "We have a hybrid SaaS + implementation contract with a large distinct implementation fee — how do we recognise it?"
2. **Read the relevant ASC text directly.** In this case, ASC 606-10-25-14 through 25-22 (identifying performance obligations) and 606-10-25-19 (distinct within the context of the contract).
3. **Read the corresponding AICPA guide section.** Working examples of implementation-fee analysis.
4. **Cross-reference to a Big Four guide** if the ASC text is ambiguous for the specific fact pattern.
5. **Check practitioner content for common patterns.** Kruze or a Big Four blog on SaaS implementation fees may surface market practice.
6. **Document the analysis in the revenue-recognition policy memo.** Cite the ASC references. Show the reasoning. Have the CPA / auditor review.
7. **Apply consistently.** Every contract with the same fact pattern gets the same treatment.

Steps 1-3 are non-negotiable. Steps 4-6 are how a CFO builds a defensible policy. Skipping directly to a practitioner blog post — as founders often do — produces a policy that will not survive an audit.

## What is NOT in the guidance stack

- **Twitter / X threads** on ASC 606. Occasionally useful as a pointer; never authoritative.
- **AI-model output** on revenue recognition. Useful for orientation; not a substitute for reading the ASC text.
- **Analogies from other industries** ("we're basically like Netflix, so we do it their way"). Every specific fact pattern needs its own analysis. Netflix's ASC 606 disclosures may or may not apply to your subscription streaming; read the text, not the analogy.

## Summary

- Authoritative US GAAP is the FASB ASC (Codification). ASC 606 governs SaaS revenue recognition; ASC 340-40 governs commissions; ASC 230 governs the cash-flow statement.
- Authoritative tax guidance is the IRC and Treasury Regulations. IRS Publication 538 is the practitioner-level plain-English companion for accounting-method issues. Form 3115 is the accounting-method-change filing.
- AICPA FRF for SMEs is a non-GAAP special-purpose framework, useful as a middle ground between cash and full GAAP at Series-A but not a path to a Series-B audit.
- Startup-specific practitioner content (Kruze, Pilot, Bench, and similar) is interpretive, useful for benchmarking practices, and not a substitute for the authoritative source.
- The CFO's practical stack: fact pattern → ASC / IRC direct → AICPA guide → Big Four guide → practitioner blog → policy memo → apply consistently.
- Peer-company 10-K disclosures are the fastest way to see how a mature SaaS company frames its revenue-recognition policy.

With the seven chapters complete, the exercises in the `exercises/` folder walk hands-on drills on each of the chapter's objectives against a real (or realistic hypothetical) startup's contracts and financials.
