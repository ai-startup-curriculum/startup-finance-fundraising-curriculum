# Exercise 07 — Sales-Tax Nexus and Registration Drill

**Estimated time:** ~3.5 hours
**Prerequisites:** Chapter 7 (sales tax, VAT, and the compliance stack). Basic familiarity with the company's billing system and customer geography is assumed.

## Problem statement

For a specified Series-A / Series-B SaaS company, run the year-one sales-tax nexus study end-to-end and produce the registration plan. Deliverables: a US-state nexus study across a four-year review period, an EU / UK / international VAT / GST nexus review, a per-jurisdiction action plan (register-and-file-forward / voluntary-disclosure-agreement / documented-no-action), a compliance-vendor selection memo, a back-exposure reserve calculation, and an M&A / IPO diligence-defense memo demonstrating that the year-one program is defensible.

The goal is to demonstrate the specific CFO discipline that keeps sales-tax exposure from becoming the horror-story reserve at exit. Sales-tax compliance is cheap to install ($20K-$60K/year in vendor cost plus specialty-firm study fee at Series-A) and expensive to unwind ($500K-$5M reserve at Series-C M&A / IPO diligence). The exercise trains the discipline that the CFO must own even when the day-to-day filing is fully outsourced.

## Scenario — build your own

Construct (or use a real one) a Series-A / Series-B SaaS company with the following characteristics:

- ~$8M-$25M ARR (pick a specific number), ~50-150 employees.
- Product: SaaS with a mix of subscription and (optionally) usage-based revenue. Choose a specific product category (developer tools, data platform, workflow SaaS, consumer-adjacent prosumer tool) that pattern-matches to a specific US-state SaaS-taxability position.
- Customer mix: pick a specific mix — e.g., 70% US enterprise B2B, 20% US SMB B2B, 10% US SMB / prosumer / small-business B2C. Optional international layer: ~15% of revenue from EU customers (mixed B2B / B2C) plus a UK customer base.
- Billing on Stripe (or Chargebee), with sales-tax calculation *currently not integrated* into the invoicing workflow — sales tax has not been collected on any invoices to date.
- Sales history: state-by-state and country-by-country revenue for the current calendar year plus the prior three calendar years. Reasonable defaults: 25-35 US states with any sales, 10-20 US states with sales above the $100K threshold; 3-8 EU countries with sales; UK with sales above the £85K threshold.
- Physical presence: HQ in one US state (choose one), one remote-employee footprint of ~30 employees distributed across ~15 other states (each creating physical nexus in that state), one recently-added UK subsidiary with one employee, and periodic trade-show / customer-visit travel to a handful of additional states.
- Board decision: the audit committee (or a Series-B lead investor's LP-reporting requirement) has asked the CFO to install sales-tax compliance in the current year.
- Fiscal year: calendar year.

Reasonable variations are welcome; document any assumption changes upfront.

## Requirements

Produce the following artifacts.

### Artifact 1 — US-state nexus study (spreadsheet + 3-4 page memo)

The specific nexus-study artifact chapter 7 describes. Spreadsheet columns:

- State
- Physical presence? (Y / N + specific presence — employee, office, inventory, trade-show)
- Physical-nexus date (day 1 of the presence)
- Economic-nexus threshold (state-specific — $100K / 200 transactions is common; some states diverge). Cite the specific state statute or DOR guidance for each state.
- Current-year revenue into the state
- Current-year transaction count into the state
- Economic-nexus triggered? (Y / N)
- Economic-nexus trigger date (specific month the threshold was crossed)
- Prior-year revenue and transaction count (each of the prior three years)
- Prior-year economic-nexus trigger dates
- SaaS taxability in the state (taxable / not-taxable / partially-taxable — cite the specific state rule; note that this is a moving target — mark with `[assumption]` and cite date-of-check)
- Rate (state rate; note local-rate variability if applicable)
- Sourcing rule (origin / destination)
- Filing cadence expected (monthly / quarterly / annual)
- Nexus type conclusion (physical / economic / affiliate / marketplace / none)
- Nexus date (earliest of the applicable types)
- Cumulative exposure since nexus date (revenue × rate)
- Recommended action (register-and-file-forward / VDA / documented no-action)

Target: all 45 US sales-tax states, plus DC. Companion memo (3-4 pages) walks the reader through: the state selection, the specific thresholds cited by state, the SaaS-taxability map used (with source and date), the states with the largest exposure, and the states with the trickiest analysis (Colorado / Louisiana / Alabama local rates, Illinois / Texas / New York SaaS-taxability history).

### Artifact 2 — EU / UK / international VAT / GST nexus review (2-3 page memo)

For the EU / UK / and any other international markets in scope:

- **EU B2C sales.** Country-by-country sales table. Confirm whether the company has crossed the €10K place-of-supply threshold (below which the seller's home country VAT applies for EU distance sales). If above, the OSS registration analysis applies. Determine which member state to use as the OSS registration home base and the specific Non-Union OSS registration mechanics for a non-EU seller of digital services.
- **EU B2B sales.** Confirm the reverse-charge mechanism can be used (customer's EU VAT ID captured and validated via VIES). Name the specific control the company installs at contract signing to capture the VAT ID.
- **UK sales.** Confirm whether the company has crossed the £85K UK VAT registration threshold. Name the specific registration mechanic post-Brexit and the impact of the recently-added UK subsidiary on registration.
- **Other international.** For each of Australia (GST at 10%), Canada (GST + provincial), India (GST / OIDAR), Japan (Consumption Tax / JCT), if the company has any customer sales, name whether registration is required and the specific mechanics. If not required (below threshold), state the threshold and the monitoring cadence.

For each jurisdiction, state a recommended action: register (with specific mechanic) / monitor (with monitoring cadence and specific threshold to watch) / not-required (with rationale).

### Artifact 3 — Per-jurisdiction action plan (spreadsheet)

Roll up the US and international studies into a single action-plan spreadsheet:

- Jurisdiction
- Action (register-and-file-forward / VDA / documented no-action / monitor / not-required)
- Target action date (month)
- Owner (name / role — tax lead, specialty firm, compliance-vendor's managed-services team, CFO for documented no-action decisions)
- Estimated back-exposure (revenue × rate × months since nexus)
- Estimated back-exposure with penalties and interest (add estimated 20-40% based on state; cite the specific state's penalty regime where you can)
- VDA look-back offer expected (typically 3-4 years; state-specific)
- Estimated first-year prospective compliance cost (registration fee + vendor cost + specialty-firm fee allocation)

Include a summary section: total back-exposure gross, total back-exposure net-of-VDA-benefits, total prospective annual compliance cost, and a total-year-one budget the CFO would present to the board.

### Artifact 4 — Compliance-vendor selection memo (2-3 pages)

The RFP-style memo the CFO uses to select the compliance vendor. Compare at least three vendors from chapter 7 (Anrok, Avalara, TaxJar, Sovos, Vertex — pick three appropriate for the company's stage and product profile):

- **Fit criteria.** Rate calculation depth in the specific states of nexus; SaaS-taxability handling; billing-system integration (Stripe / Chargebee); international VAT / GST coverage if in scope; managed-filing services vs. self-service filing; VDA support; nexus-monitoring alerts; API-first vs. batch reconciliation.
- **Cost.** Annual subscription fee, per-transaction fees if applicable, managed-services fees, filing fees per jurisdiction. Model the total-cost-of-ownership over three years.
- **Integration effort.** Real-time rate calculation at the billing-transaction level — chapter 7's specific installation-discipline claim. State the specific engineering effort required to integrate and the timeline.
- **Recommendation.** With an explicit trade-off statement — "recommend Vendor X because [rationale]; accept the fee premium of $Y because [rationale]; alternative would be Vendor Z if [condition]."

### Artifact 5 — Back-exposure reserve calculation (1-2 pages)

The specific back-exposure number that will show up on the balance sheet as a *sales-tax payable* reserve until it is resolved. Calculation:

- Per-jurisdiction back-tax exposure (from artifact 1 / 2).
- Penalties and interest by jurisdiction (state-specific; cite where possible, tag `[assumption]` otherwise).
- VDA look-back haircut where a VDA is planned (limits the look-back and often waives penalties).
- Documented no-action haircut where applicable (with the specific rationale for each).
- Net reserve = sum of the per-jurisdiction net exposure.

Show the calculation methodology, the specific accounting entry (Dr. sales-tax expense / Cr. sales-tax payable), the disclosure that will appear in the notes to the financials, and the auditor conversation that will accompany the reserve at the year-one audit (chapter 4).

### Artifact 6 — M&A / IPO diligence-defense memo (2 pages)

The memo the CFO would hand to a diligence team (M&A acquirer's tax practice or IPO underwriter's tax counsel) demonstrating that sales-tax compliance is under control. Sections:

- **The nexus-study methodology.** How the study was scoped, what period was reviewed, what specialty firm was engaged (if any).
- **The registration-and-VDA program.** Which jurisdictions were registered, which VDAs were completed, which had documented no-action decisions, and the current-year filing cadence.
- **The compliance vendor and integration.** Which vendor is installed, which billing-system integration is live, and the specific evidence (transaction-level tax calculation on every invoice).
- **The nexus-monitoring cadence.** How future threshold crossings are detected and acted on.
- **The reserve.** The current sales-tax reserve on the balance sheet, why it is at the specific level, and the path to zero.

The memo is defensive artifact — a well-run compliance program produces a memo the diligence team accepts with minimal follow-up. A poorly-run program produces a diligence request list of hundreds of items and a purchase-price adjustment. The CFO who can produce this memo has done the job.

## Starter guidance

- The state-specific SaaS-taxability map is the specific place to mark `[assumption]` and cite date-of-check. Rules change; the exercise is about the *reading discipline*, not producing a mechanically-correct current map.
- Cite the specific state statute or DOR guidance for each state's economic-nexus threshold. "Around $100K" is not defensible; "Cal. Rev. & Tax Code §6203(c) — $500K threshold, no transaction count" is.
- The remote-employee physical-presence layer is the specific place year-one filers under-analyse. Every state with a remote employee creates physical nexus in that state from the employee's first day; the economic-nexus analysis does not override the physical-nexus analysis, it layers on top.
- The Colorado / Louisiana / Alabama local-rate wrinkle is real; do not skip it. If your company has any presence or nexus in one of these states, name the specific mechanic and the vendor capability that handles it.
- Use chapter 7's practitioner playbook sequence (nexus study → vendor selection → integration → back-exposure → monthly workflow → nexus monitoring) as the memo's organising narrative.
- Cross-reference exercise 04 (audit-readiness) — the sales-tax reserve appears on the balance sheet the auditor reviews and the reserve calculation is a specific PBC-list item.
- Cross-reference exercise 06 (R&D credit) — the tax lead who owns the R&D credit typically also owns sales-tax nexus; the exercise scope is the "tax-lead workstream" as an integrated whole.
- The compliance-vendor claims (feature coverage, price, integration depth) evolve; every specific claim you cannot verify should be tagged `[assumption]` per the module convention.

## Acceptance criteria

- **The US nexus study covers all 45 sales-tax states + DC** with per-state thresholds cited.
- **Every state with physical presence is analysed** for physical-nexus date first, then economic-nexus overlay.
- **The SaaS-taxability map is dated and sourced.** Any state where the taxability is a moving target is flagged.
- **The EU / UK / international review names the specific registration mechanic** (OSS vs. Non-Union OSS vs. per-country) with the specific threshold cited.
- **The per-jurisdiction action plan has a specific action, date, owner, and estimated cost for every jurisdiction with any exposure.**
- **The compliance-vendor memo compares ≥ 3 vendors** on the fit / cost / integration criteria.
- **The back-exposure reserve calculation is walked cell-by-cell** with source citations and `[assumption]` tags on any unverified rates.
- **The diligence-defense memo is a stand-alone artifact** — a diligence team could read it and accept the compliance-program story.
- **Every unverified taxability, threshold, or rate claim is tagged** `[assumption]` or `<!-- needs-research: ... -->`.

## Deliverables

- The US-state nexus study (spreadsheet + Markdown memo, 3-4 pages).
- The EU / UK / international VAT / GST nexus review (Markdown, 2-3 pages).
- The per-jurisdiction action plan (spreadsheet).
- The compliance-vendor selection memo (Markdown or PDF, 2-3 pages).
- The back-exposure reserve calculation (spreadsheet + short Markdown, 1-2 pages).
- The M&A / IPO diligence-defense memo (Markdown or PDF, 2 pages).

## Extensions (optional)

- **Model an M&A-diligence scenario.** Assume an acquirer's tax-diligence team arrives at Q3 with a specific request list of ~50 sales-tax items. Author the response playbook — which items are already in the artifacts above, which are new, which are addressed by the VDA program, and which trigger a purchase-price adjustment.
- **Add the marketplace-facilitator overlay.** Assume the company also sells through a marketplace (a partner reseller, an app-store integration, an embedded-billing partner). Show how the marketplace-facilitator regime shifts the collection-and-remittance responsibility and where the company's residual responsibility remains.
- **Extend to a US B2C consumer SaaS company.** For a much higher-transaction-count / lower-per-transaction consumer product, walk how the analysis shifts — more states above the transaction-count threshold, more emphasis on real-time tax calculation at checkout, more emphasis on the customer-experience impact of adding sales tax at checkout.
- **Extend to hardware.** For a company selling physical goods across the US, show where the analysis diverges from SaaS (universal taxability, physical presence at any inventory location, resale-certificate management, drop-shipper mechanics).
- **Model a state examination.** Assume one state (pick a specific state) opens an examination of the company's post-*Wayfair* compliance. Author the response plan — the initial notice-response letter, the document production list, the CFO's target settlement position, and the specialty-firm engagement decision.
