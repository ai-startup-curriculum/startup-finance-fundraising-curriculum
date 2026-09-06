# Exercise 06 — R&D Tax Credit Qualification Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 6 (R&D tax credit — Section 41 and the payroll offset). Familiarity with the company's engineering roadmap and payroll base is assumed.

## Problem statement

For a specified Series-A / Series-B SaaS company, run the year-one R&D credit qualification exercise end-to-end. Deliverables: a project-by-project four-part test memo covering the engineering roadmap, a qualified-research-expenditure (QRE) computation across the four expense categories, an Alternative Simplified Credit (ASC) calculation, a payroll-tax-offset election decision memo, a documentation-practice memo, and a specialty-firm-vs.-in-house engagement decision with a net-of-fee credit estimate.

The goal is muscle memory on the qualification / election / documentation practice — after this drill you should be able to look at any engineering roadmap and, within an hour, identify the qualifying projects, the QRE base, and the approximate credit and payroll-offset value. The credit is the CFO's most-underestimated cash lever at Series-A / Series-B; the CFO who cannot personally scope the qualification is over-relying on a specialty firm.

## Scenario — build your own

Construct (or use a real one) a company with the following minimum shape:

- ~$4M-$8M ARR (or pre-revenue with material engineering payroll), ~$8M in total qualified wages, ~40 engineers and applied-research staff.
- Gross receipts under $5M in the current tax year and no gross receipts in any of the prior five years (so the company qualifies for the payroll-offset election under §41(h)).
- Product: a customer-facing SaaS product (choose a specific product category — data platform, developer tools, applied ML / AI, workflow automation, security, fintech infrastructure — that pattern-matches to the specific §41(d) permitted-purpose analysis).
- Engineering roadmap for the tax year with at least eight discrete named projects across a mix of product features, platform work, applied-ML / research work, security / reliability, and internal-tooling work. At least two of the eight should be *internal-use* software so the drill covers the Treas. Reg. §1.41-4(c)(6) high-threshold-of-innovation analysis.
- Cloud spend: ~$500K annually across AWS / GCP / Azure with a rough split between production (customer-serving), development / staging / experimental, and internal-tooling workloads.
- One contract-research engagement of ~$300K with an external ML-research consultancy where the company retains rights to the results and bears economic risk.
- Payroll runs on Rippling or Gusto; GL is QBO or Xero; the company has an outsourced tax firm relationship and is considering engaging a specialty R&D-credit firm for the year-one study.
- Fiscal year: calendar year.

Reasonable variations are welcome; document any assumption changes upfront.

## Requirements

Produce the following artifacts.

### Artifact 1 — Project-by-project four-part test memo (5-8 pages)

For each of the ≥ 8 named projects, a one-paragraph analysis of qualification under the four-part test:

- **Part 1 (§174 expenditure).** Yes / no with a one-sentence rationale.
- **Part 2 (permitted purpose).** Yes / no; if the project is *internal-use* software, apply the Treas. Reg. §1.41-4(c)(6) high-threshold-of-innovation test explicitly (innovation, significant economic risk, commercial-availability test), and state whether all three prongs are met. Do not skip the internal-use analysis for the internal-tooling projects.
- **Part 3 (technological in nature).** Yes / no with the specific hard-science principle in play (computer science, engineering, applied statistics / ML, cryptography, etc.).
- **Part 4 (process of experimentation).** Yes / no with the specific (a) uncertainty identified, (b) alternatives evaluated, (c) evaluation methodology. Cite the specific engineering tickets / experiments / A-B tests / benchmarks / model comparisons where possible.

Conclude each project with: **QRA / not QRA**, and if partial (some sprints qualify, some do not), state the estimated qualifying percentage of the project's spend.

Include a summary table at the top: project → QRA yes/no → estimated qualifying % of associated wages and cloud spend.

### Artifact 2 — Qualified-research-expenditure (QRE) computation (spreadsheet)

A worksheet with the following sections:

- **Qualified wages.** Per-employee table with: employee ID (redacted), role, total wages for the year, estimated % time on qualifying projects, allocation methodology (project-tag distribution / sprint allocation / sub-team dedication), qualified wages. Highlight the ≥ 80% cases where the full wage is included.
- **Qualified supplies.** Line items for any tangible property used in qualifying research. Likely small for a SaaS company; still enumerate.
- **Qualified contract research.** The $300K external ML-research engagement, with the 65% qualified-contract-research factor applied ($195K included in QRE), plus documentation of the rights-retention and economic-risk analysis.
- **Qualified cloud-computing / rental costs.** AWS / GCP / Azure allocation across production, development / staging / experimental, and internal-tooling workloads. Only the qualifying portion (dev / staging / experimental workloads on qualifying projects) is included. Show the allocation methodology.
- **Total QREs** — sum of the four categories.

Produce two computations: one using the "generous but defensible" allocations (higher %-time estimates, higher cloud allocation), one using the "conservative" allocations (lower %-time, lower cloud allocation). The credit range across the two is the CFO's expected credit range for the year.

### Artifact 3 — Alternative Simplified Credit (ASC) calculation

Compute the federal credit under the ASC method for both the generous and the conservative QRE numbers:

- Year-1 first-time-filer case: credit = 6% of current-year QREs.
- Steady-state case (assume prior-3-year QRE average of $5M as an illustrative figure — document your assumption): credit = 14% × (current-year QREs − 0.5 × prior-3-year average).

Present both years so the reader sees the year-1 discount vs. the steady-state result.

Optional bonus: pull the **state credit** for the company's principal state of operation (California, Massachusetts, New York, or Texas are the most common — pick one), state the specific state-credit rate and any material qualification differences, and estimate the state credit under the same QRE base.

### Artifact 4 — Payroll-tax-offset election decision memo (2-3 pages)

The memo the CFO would present to the CEO / board explaining:

- **Qualification.** Whether the company meets the §41(h) qualified-small-business criteria (gross receipts under $5M in current year; no gross receipts in any of the prior five years). Cite the specific gross-receipts numbers.
- **Election mechanics.** The Form 6765 election on the timely-filed return; the Form 8974 quarterly claim against Form 941 payroll-tax filings; the specific cap ($500K post-IRA-2022, split between the Social Security and Medicare portions — verify current cap).
- **Cash-flow timing.** The specific quarters the offset lands in — if the return is filed in Q1 of the following year, the offset applies against payroll-tax remittance starting in Q2, over the four subsequent quarters. Model the specific dollar amount per quarter against the current payroll-tax liability.
- **Runway impact.** The credit at the cap (~$500K) against the company's current monthly burn — how many additional months of runway does the credit generate? Cross-reference to mod-109's runway framework.
- **Five-year limit.** How many years of the five-year election window the company will use, and the specific graduation event (revenue crossing $5M) that will end eligibility.
- **Recommendation.** Elect / do-not-elect with a specific rationale and any dependencies (the return must be filed on time — do not sabotage the election with a late filing).

### Artifact 5 — Documentation-practice memo (2-3 pages)

The year-round documentation practice memo — the CFO's operating instructions to the engineering and finance teams:

- **Project-level identification.** Which system captures which project (Linear / Jira / Notion / Github Projects), the naming convention, the tax-owner's mirror-to-tax-file cadence at close.
- **Four-part test memos.** The template and cadence for the per-project four-part-test memo (typically written by the engineering lead in collaboration with the tax-owner at project inception; refreshed at project close).
- **Time allocation.** The methodology — formal time-tracking, sprint-team-allocation, project-tag distribution, or a defensible mix. The methodology chosen is documented and applied consistently; changing methodologies mid-year invites IRS-examination scrutiny.
- **Cloud-computing allocation.** The tagging discipline in AWS / GCP / Azure that distinguishes production from dev / staging / experimental. Name the specific tags and the finance-team's monthly review process.
- **Contract-research documentation.** The specific artifacts the CFO retains — the contract, the statement of work, the invoices, evidence of retained rights and economic risk (indemnity provisions, IP-assignment clauses, ownership terms).
- **Retention and IRS response.** The retention policy for all supporting documentation (typically the return period plus 3-6 years); the CFO-owned IRS-examination response playbook if the return is examined.

### Artifact 6 — Specialty-firm engagement decision (1-2 pages)

The decision memo on whether to engage a specialty R&D-credit firm (alliantgroup, KBKG, Endeavor, Kruze, or a Big Four practice) for the year-one study:

- **Fee structure.** Model the specialty-firm fee — commonly 15%-25% of credit generated, or a fixed engagement fee for larger companies. State the fee-structure assumption.
- **Net-of-fee credit.** Gross credit − specialty fee = net credit. Compare against the "in-house study by the outsourced tax firm" alternative (typically a fixed fee of $10K-$50K).
- **Study depth.** The specialty-firm study typically produces a defensible qualification study, engineering-lead interviews, formal four-part-test memos per project, and IRS-examination response support. Compare to the in-house alternative's depth.
- **Recommendation.** Engage / do-not-engage with the specific rationale.

## Starter guidance

- Start with the roadmap. Every project's four-part-test analysis begins with the specific engineering work, not the tax rules. The tax rules apply *to* the engineering work; the engineering work is not written to fit the tax rules.
- The internal-use software analysis is the specific place year-one filers over-claim. Apply Treas. Reg. §1.41-4(c)(6) explicitly for internal-use projects; if the three-prong high-threshold-of-innovation test is not clearly met, exclude the project rather than including it with a shaky analysis.
- The cloud-allocation methodology is the specific place year-one filers under-document. Set up the AWS / GCP / Azure tagging *before* the year begins; retroactive tagging is defensible but harder.
- Use chapter-6's illustrative example (a Series-B SaaS company with $8M in qualified wages, ~$500K in qualified cloud) as a sanity check — your QRE totals should be in the same order of magnitude.
- For any tax-code claim you cannot verify to the specific current-year citation, mark it `[assumption]` or `<!-- needs-research: ... -->` per the module convention. IRC §41 has been amended multiple times; the Treas. Reg. references have been updated; the payroll-offset cap changed under the IRA 2022. Verify against current sources.
- Cross-reference with exercise 07 (sales tax) and exercise 05 (controls) — the tax lead who owns the R&D credit typically also owns sales-tax nexus and coordinates with the controls program on the vendor-and-contract documentation.

## Acceptance criteria

- **Each of the ≥ 8 projects has a complete four-part test analysis.** No skipped parts.
- **The internal-use software analysis is applied explicitly** to each internal-use project with the three-prong test.
- **The QRE computation covers all four expense categories** — wages, supplies, contract research (at 65%), cloud-computing — with the specific allocation methodology.
- **Two QRE scenarios (generous and conservative) are computed.**
- **The ASC calculation is shown for both the year-1 first-time-filer case and the steady-state case.**
- **The payroll-offset election memo confirms qualification** against the specific §41(h) criteria and quantifies the cash-flow timing and runway impact.
- **The documentation-practice memo names specific tools, tags, cadences, and owners** — not generic "we'll document as we go."
- **The specialty-firm decision includes a net-of-fee credit estimate.**
- **Every unverified tax citation is tagged** `[assumption]` or `<!-- needs-research: ... -->`.

## Deliverables

- The project-by-project four-part test memo (Markdown or PDF, 5-8 pages).
- The QRE computation (spreadsheet).
- The ASC calculation (spreadsheet or Markdown table).
- The payroll-tax-offset election decision memo (Markdown or PDF, 2-3 pages).
- The documentation-practice memo (Markdown or PDF, 2-3 pages).
- The specialty-firm engagement decision memo (Markdown or PDF, 1-2 pages).

## Extensions (optional)

- **Model the §174 capitalisation interaction.** Compute the current-year taxable-income effect of the TCJA 2017 §174 capitalisation-and-amortisation requirement (five-year domestic amortisation, fifteen-year foreign) against the same QRE base. Show how the taxable-income effect and the credit are computed independently.
- **Add a state-credit filing.** Fully compute the California R&D credit (or another chosen state's credit) alongside the federal credit. Note where the state's qualification test diverges from §41 (e.g., California's separate base-amount calculation, or the "in-state" QRE definition).
- **Model an IRS examination scenario.** Assume the return is examined 18 months post-filing. Author the specific documentation package the CFO delivers, the specific positions likely to be challenged (contract-research rights retention, internal-use software qualification, %-time allocation methodology), and the response playbook.
- **Extend to Series-C+.** Add a scenario where the company has grown past the payroll-offset qualifying window (revenue > $5M for two years). Show how the credit computation and use change — direct income-tax offset vs. deferred tax asset — and how the CFO decision-framework shifts.
