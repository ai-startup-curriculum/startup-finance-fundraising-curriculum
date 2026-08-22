# Sales Tax, VAT, and the Compliance Stack — Nexus, Registration, and the Vendor Layer

## Why this matters

Sales tax is the CFO's most-underestimated compliance risk. Unlike income tax — one federal filing, a handful of state filings, all through one tax practice — sales tax fragments across 45 US states with sales tax, ~11,000 local taxing jurisdictions, the EU's 27 member states plus the UK, and a growing list of other international VAT / GST regimes. Every one of those jurisdictions has its own rules on what triggers a filing obligation (nexus), what is taxable, at what rate, on what cadence, with what registration process, and with what penalty regime for non-compliance.

The 2018 Supreme Court decision in *South Dakota v. Wayfair, Inc.* eliminated the physical-presence rule that had governed sales-tax nexus since *Quill v. North Dakota* (1992). Post-*Wayfair*, any state may impose a filing obligation on a remote seller based on **economic nexus** — typically a threshold like $100K in sales or 200 transactions into the state per year, though thresholds vary. This transformed sales-tax compliance for SaaS / e-commerce companies overnight: a company selling $50M ARR into all 50 states with no physical presence went from filing in 1-2 states pre-*Wayfair* to potentially filing in 30-45 states post-*Wayfair*, on top of any local jurisdictions and marketplace-facilitator overlays.

For a Series-A/B SaaS company, sales-tax exposure is the single biggest tax-related M&A / IPO diligence surprise. An acquirer's diligence team runs a nexus study, discovers the target has been under-collecting sales tax across 20+ states for three years, and the *cumulative back-tax liability plus penalties and interest* becomes an escrow adjustment (or a purchase-price haircut) that dwarfs the annual compliance cost the company avoided. Every CFO has read a horror story where a $5M-ARR company took a $2M sales-tax reserve at exit; the horror is entirely avoidable if the CFO installs the compliance discipline while it is still cheap.

## The specific mechanics — US sales tax post-*Wayfair*

Sales tax in the US is a **state (and local) tax** — there is no federal sales tax. Each state that imposes a sales tax defines:

- **Taxability of the good or service.** Physical goods are almost universally taxable. Digital goods and SaaS are taxable in some states and not others; the map has been in motion for a decade. As of the current tax year, roughly 25-30 US states impose sales tax on SaaS in some form, though the specific characterisation (SaaS as a data-processing service, as a taxable service, as tangible personal property in digital form) and the exemptions vary widely. <!-- needs-research: pull the current state-by-state SaaS-taxability map from a specialty source (Anrok / Avalara / Bloomberg Tax) -->
- **Nexus.** The connection between the seller and the state that triggers a filing obligation.
- **Rate.** State rate plus any local (county / city / district) rates. Some states have a single state-wide rate; others (Colorado, Louisiana, Alabama) have per-jurisdiction rates that can vary by street address.
- **Filing cadence.** Monthly, quarterly, or annual depending on volume.
- **Sourcing rule.** Origin-based (rate at the seller's location) or destination-based (rate at the buyer's location). Most states are destination-based for SaaS; the exceptions are historically documented.

### Nexus types after *Wayfair*

- **Physical nexus.** The classic pre-*Wayfair* rule: an office, an employee, an inventory location, a warehouse, or in some states even an occasional presence (a trade show, a customer visit) can create nexus. Physical nexus is triggered on day 1.
- **Economic nexus.** Post-*Wayfair* rule: crossing a state's sales or transaction threshold in the current or prior calendar year (or, in some states, a rolling 12-month period). Common threshold is $100K in sales or 200 transactions; some states use $500K in sales with no transaction count; some use $250K. The thresholds and mechanics vary.
- **Affiliate nexus / click-through nexus.** Older pre-*Wayfair* rules that some states retain — a related entity's presence, or a marketing-affiliate relationship above a threshold, can create nexus even without physical presence.
- **Marketplace-facilitator nexus.** For sellers using a marketplace platform (Amazon, Etsy, Uber, Airbnb, Doordash, Shopify's marketplace features), the *marketplace* typically collects and remits sales tax on behalf of the seller for marketplace transactions in states with marketplace-facilitator laws (nearly all US states as of ~2020 onward). The marketplace-facilitator regime does not eliminate the seller's non-marketplace obligations.

### The nexus study

The reference process — a **nexus study** — is the first output of a competent sales-tax compliance program. Every CFO commissions one at Series-A (or earlier if the company is high-volume from day 1). The study:

- Inventories every state / jurisdiction the company has sold into over the review period (usually the current year plus prior 3-4 years).
- Applies each jurisdiction's economic-nexus threshold to the sales volume and transaction count into that jurisdiction.
- Flags where physical presence (employees, offices, in-person events) created nexus.
- Identifies which of those jurisdictions treat the company's specific offering (SaaS, digital goods, physical goods, mixed) as taxable.
- Produces a table: jurisdiction / nexus type / nexus date / taxable-or-not / recommended action (register-and-file-forward, register-and-voluntary-disclosure-back, monitor, not-required).

The study is typically run by the outsourced tax firm, by a specialty sales-tax firm (TaxOps, TaxConnex, MyLodgeTax for lodging, Peisner Johnson, etc.), or by Anrok / Avalara's / TaxJar's compliance-consulting arm.

### Registration and voluntary disclosure

Once the nexus study identifies exposure, the CFO decides how to address each state:

- **Register and file forward.** For states where nexus was triggered recently and the back-tax exposure is small, register in the state and begin collecting and remitting prospectively. Accept any small back-tax liability as a current-year expense.
- **Voluntary Disclosure Agreement (VDA).** For states where back-tax exposure is material, enter a VDA — a formal agreement with the state's Department of Revenue that limits look-back (typically 3-4 years, sometimes 3 years even for longer under-collection), waives penalties, and requires payment of back-tax and interest. VDAs are typically negotiated on the company's behalf by a specialty firm and are anonymous until the state agrees to the terms.
- **Amnesty programs.** States periodically run amnesty programs with reduced-penalty terms; the CFO's tax firm should track these.
- **Do-nothing (documented decision).** For jurisdictions with de minimis exposure or where the company has evaluated and decided the risk-adjusted cost of registration exceeds the exposure, document the decision with a memo signed by the CFO. This is defensible; unwritten "we thought about it and decided no" is not.

### Ongoing compliance

Post-registration, sales tax becomes a monthly workflow:

- Sales-tax collection at checkout (or at invoicing) at the correct rate for the buyer's jurisdiction.
- Monthly / quarterly return preparation per jurisdiction.
- Remittance per jurisdiction on the required cadence.
- Reconciliation of collected-vs.-remitted per jurisdiction, with the balance on the balance sheet as a *sales-tax payable*.
- Exemption-certificate management (customers claiming exemption for resale, non-profit status, or government purchase).

The workload at scale is entirely automatable. Doing it by hand across 40 states is not viable past ~$5M ARR.

## The compliance stack — Avalara, TaxJar, Anrok, and adjacent

The vendor layer that automates the above:

- **Avalara AvaTax.** The enterprise reference. Real-time tax calculation via API integrated into the billing system (Stripe, Chargebee, NetSuite, Salesforce CPQ). Return preparation and filing via Avalara Returns. Full jurisdiction coverage in the US, plus international VAT / GST modules. High cost ($10K-$100K+ per year depending on transaction volume and jurisdiction count), high depth.
- **TaxJar (now owned by Stripe).** SMB-focused. Real-time rate calculation, automated filing in many states, strong e-commerce (Shopify, Amazon, WooCommerce, BigCommerce) integrations. Lower cost, less international coverage.
- **Anrok.** SaaS-native (founded specifically for the post-*Wayfair* SaaS use case). Native handling of SaaS-specific taxability rules, subscription-billing integration, nexus monitoring, VDA management. Rapidly-growing footprint in the SaaS mid-market.
- **Vertex.** Enterprise tax engine with deep configuration; typically used at large enterprise / Global 2000 scale.
- **Sovos.** Global tax compliance; strong at VAT / GST in Europe and Latin America.
- **Kintsugi, Numeral, and other emerging vendors** — newer entrants targeting the SaaS-native / API-first end.

The CFO decision: at Series-A pre-*Wayfair*-exposure, Anrok or TaxJar is typically enough. At Series-B with 30+ states of nexus and international operations, Avalara or Anrok (both scale) is typical. At Series-C+ with heavy international footprint, Avalara / Sovos / Vertex compete.

The vendor selection matters less than the *installation discipline*: the tax engine must be integrated into billing at the transaction level, not applied retroactively as a monthly reconciliation. Retroactive tax calculation on already-invoiced revenue leads to under-collected sales tax that the company must remit out of its own pocket — a direct margin hit.

## EU / UK VAT — the international layer

Once the company sells to customers in the EU or UK, a second compliance regime applies.

### EU VAT (post-2015 place-of-supply-of-services)

Under the EU's 2015 changes for electronically-supplied services (ESS), digital services (SaaS, streaming media, e-books, online courses) sold to **EU consumers (B2C)** are taxed at the **customer's** country's VAT rate, not the seller's country's rate. A US SaaS company selling to a consumer in Germany applies the German VAT rate; a sale to a consumer in France applies the French rate.

For B2C sales into the EU, the seller has two compliance options:
- Register for VAT in each EU country they sell into (expensive, complex).
- Register for the **One-Stop Shop (OSS)** — a single VAT registration in one EU member state that handles the seller's obligations across all EU member states. Non-EU sellers use the **Import One-Stop Shop (IOSS)** for goods or the **Non-Union OSS** for digital services.

For **B2B sales** into the EU (customer is a VAT-registered business), the *reverse-charge mechanism* typically applies — the customer accounts for the VAT under their own registration and the seller does not charge VAT, provided the seller collects and validates the customer's EU VAT ID. VIES (VAT Information Exchange System) provides the validation API.

### UK VAT (post-Brexit)

Since 2021, the UK operates its own VAT regime separate from the EU. A non-UK seller with UK B2C sales above the £85K threshold registers for UK VAT directly; the OSS does not cover UK sales. B2B sales use reverse-charge similar to the EU model.

### Other international VAT / GST

- **Australia** — GST at 10%, non-resident sellers of digital services above the threshold register for Australian GST.
- **Canada** — federal GST plus provincial PST / HST / QST; non-resident sellers may need to register depending on province and volume.
- **India** — GST regime with specific rules for OIDAR (Online Information and Database Access or Retrieval) services provided by non-residents.
- **Japan** — Consumption Tax with a JCT invoice regime.
- Many other jurisdictions with similar patterns; the compliance stack (Avalara / Sovos) typically handles the mainline countries.

### The B2B vs. B2C mix — the key sales-tax / VAT design decision

For SaaS companies, the customer mix largely dictates the international VAT compliance burden. A pure enterprise-B2B seller can validate customer VAT IDs at contract signing and rely on reverse-charge across most of the EU with minimal VAT-specific compliance. A B2C or prosumer seller (developer tools sold to individual developers, media / entertainment / consumer SaaS) has the full OSS compliance load. This is a specific reason CFOs of B2C-focused companies invest in the tax-compliance stack earlier and more heavily than B2B-only peers.

## The audit / diligence exposure

The specific reason to install this discipline early:

- **M&A diligence.** The acquirer's tax diligence team runs a nexus study on the target and calculates the historical unremitted-sales-tax exposure. This becomes an *escrow*, an indemnity, or a purchase-price adjustment. On a Series-B / C-stage target, this can easily be $500K-$5M+.
- **IPO diligence.** The S-1 process requires the company to disclose material tax exposures. A sales-tax reserve that materialises during the S-1 draft can delay the offering or become an S-1 risk-factor disclosure.
- **Audit disclosure.** The annual audit's tax-provision review will surface material sales-tax exposure and require either payment / voluntary disclosure or a reserve on the balance sheet. A first-year audit that discovers a $1M sales-tax reserve is a material-weakness precursor.
- **State examination.** States are actively examining SaaS companies for post-*Wayfair* compliance; the notice can arrive years after the nexus was triggered, with interest and penalty accrual on the whole period.

The through-line: the sales-tax program is cheap when installed at Series-A (~$20K-$60K in first-year vendor cost plus specialty-firm study) and expensive when unwound at exit (~$500K-$5M reserve). The CFO decision is not "when do we start collecting" — it is "how quickly can we get compliant across our current exposure and stay compliant going forward."

## Practitioner playbook — the pragmatic Series-A / Series-B sequence

1. **Commission a nexus study** (Series-A or immediately upon hire of the first controller). Include the current year plus prior three to four years.
2. **Select a compliance vendor** (Anrok for SaaS-native, Avalara for multi-modal / international, TaxJar for e-commerce heavy).
3. **Integrate the vendor into billing** — real-time rate calculation at invoice / checkout, not retroactive.
4. **Address back exposure** — register-and-file-forward for de-minimis states, VDA for material back exposure, documented decision for the rest.
5. **Install the monthly workflow** — collected-vs.-remitted reconciliation, exemption-certificate management, monthly / quarterly returns per jurisdiction.
6. **Establish the ongoing nexus-monitoring cadence** — the vendor tracks sales volume per state and alerts when a threshold is crossed; the CFO or tax owner reviews monthly.
7. **Track international expansion** — VAT / GST registration on the same rolling monitoring; usually piggy-backing on the same compliance vendor.

## Summary

- Sales tax is the CFO's most-underestimated compliance risk; *South Dakota v. Wayfair, Inc.* (2018) replaced the physical-presence rule with economic nexus and expanded exposure from 1-2 states to potentially 45+ for SaaS / e-commerce companies.
- Nexus triggers: physical presence (day 1), economic nexus (state-specific thresholds, typically $100K / 200 transactions), affiliate / click-through nexus, marketplace-facilitator nexus.
- The reference process is the nexus study, followed by register-and-file-forward, VDA, or documented no-action per jurisdiction.
- The compliance stack — Avalara, Anrok, TaxJar, Sovos, Vertex — automates rate calculation, filing, and remittance; installation must integrate at the billing-transaction level.
- EU / UK VAT layers on top of US sales tax once international B2C sales begin; the OSS / IOSS regimes simplify multi-country compliance for digital services.
- The M&A / IPO / audit diligence exposure is the specific reason to install this discipline at Series-A; cheap at $20K-$60K/year to run, expensive at $500K-$5M reserve to unwind at exit.

Chapter 8 turns to the destination the whole finance-ops program is preparing for: the IPO.
