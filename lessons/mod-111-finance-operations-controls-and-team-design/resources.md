# Resources — mod-111 Finance Operations, Controls & Team Design

This is the reference stack that sits behind every chapter and exercise in this module. Sources are grouped by tier of authority. The primary-source tier is US federal statutory and regulatory material — IRC §41 and §174, Treas. Reg. §1.41, the Sarbanes-Oxley Act §302 / §404, SEC Regulations S-K and S-X, PCAOB auditing standards, and the *South Dakota v. Wayfair, Inc.* decision. The vendor-documentation tier — NetSuite, Workday Adaptive, Coupa, Blackline, Ramp, Brex, Mercury, Rippling, Gusto, Airbase, Avalara, Anrok, TaxJar — is second-tier and volatile; verify pricing, coverage, and feature claims against current vendor docs. The practitioner-canon tier (Kruze, Pilot, Bench, Zeni, Carta State of Startup Compensation, Pave benchmarks, David Sacks and Fred Wilson on CFO operating discipline) is third-tier and useful for pattern reading; every quantitative claim should trace back to a tier-1 source or be flagged `[assumption]` / `<!-- needs-research: ... -->`.

Because tax rates, sales-tax thresholds, EGC thresholds, payroll-offset caps, vendor pricing, and comp benchmarks all move, verify the specific citation against the current-vintage primary source before decisioning. The `<!-- needs-research -->` markers in the chapters flag the specific places where current-vintage data must be re-checked.

## Tier 1 — Primary legal, regulatory, and standard-setting sources

The load-bearing tier. Read these first.

### Tax — Internal Revenue Code and Treasury Regulations

- **Internal Revenue Code §41 — Credit for increasing research activities** — [uscode.house.gov](https://uscode.house.gov/) → 26 USC §41. The statutory basis for the federal R&D tax credit. Directly referenced in chapter 6 and exercise 06. Sub-sections most cited:
  - **§41(a)** — computation of the regular research credit.
  - **§41(b)** — definition of qualified research expenditures (wages, supplies, contract research, computer time / rental — the four QRE categories).
  - **§41(c)(4)** — Alternative Simplified Credit (ASC) method.
  - **§41(d)** — definition of qualified research (the four-part test).
  - **§41(h)** — the qualified small business election for payroll-tax offset.
- **Internal Revenue Code §174 — Research and experimental expenditures** — 26 USC §174. Post-2017 TCJA, §174 expenditures must be capitalised and amortised over 5 years for domestic research and 15 years for foreign research. Referenced in chapter 6 for the credit-vs.-capitalisation distinction and in exercise 06's optional extension.
- **Treasury Regulations §1.41-0 through §1.41-9** — [ecfr.gov](https://www.ecfr.gov/current/title-26/chapter-I/subchapter-A/part-1/subject-group-ECFR9c17f6cf5a1e69a) → 26 CFR §1.41-*. The specific Treasury guidance implementing §41. Most cited:
  - **§1.41-2** — qualified research expenses (wage / supply / contract-research definitions).
  - **§1.41-4** — the four-part test detailed regulation.
  - **§1.41-4(c)(6)** — internal-use software; the three-prong high-threshold-of-innovation test. Directly referenced in chapter 6 and exercise 06.
  - **§1.41-6** — aggregation of expenditures for related taxpayers.
- **IRS Form 6765 — Credit for Increasing Research Activities** — [irs.gov/forms-pubs/about-form-6765](https://www.irs.gov/forms-pubs/about-form-6765). The specific form on which the credit is claimed and the §41(h) election is made. The 2024 revisions materially expanded documentation on the return itself; verify current-year revisions.
- **IRS Form 8974 — Qualified Small Business Payroll Tax Credit for Increasing Research Activities** — [irs.gov/forms-pubs/about-form-8974](https://www.irs.gov/forms-pubs/about-form-8974). The specific form on which the payroll-tax-offset is claimed each quarter against Form 941.
- **IRS Chief Counsel Advice 20214101F (January 2022 IRS memorandum on §41 refund claims)** — imposed the specific "5 items of information" documentation requirement for §41 refund claims. Referenced in chapter 6 for the documentation-practice discipline.
- **Protecting Americans from Tax Hikes (PATH) Act of 2015** — the statute that made the R&D credit permanent and introduced the $250K payroll-tax offset for qualified small businesses.
- **Inflation Reduction Act of 2022 (Pub. L. 117-169)** — increased the payroll-offset cap to $500K starting in the 2023 tax year, split between Social Security ($250K max) and Medicare ($250K max) portions. Verify current cap at time of decisioning.

### Tax — sales tax and VAT

- ***South Dakota v. Wayfair, Inc.*, 585 U.S. 162 (2018)** — [supremecourt.gov](https://www.supremecourt.gov/opinions/17pdf/17-494_j4el.pdf). The Supreme Court decision eliminating the physical-presence rule for state sales-tax nexus and enabling economic-nexus regimes. The specific foundation for chapter 7 and exercise 07.
- ***Quill Corp. v. North Dakota*, 504 U.S. 298 (1992)** — the earlier decision *Wayfair* overturned; still relevant for pre-*Wayfair* historical context.
- **State Departments of Revenue** — each of the 45 US sales-tax states publishes economic-nexus thresholds, SaaS-taxability rulings, and registration mechanics. Directly referenced in exercise 07. Verify current thresholds and taxability rulings by state; the map moves. Reference state DOR pages by state — California CDTFA, New York DTF, Texas Comptroller, Illinois DOR, Massachusetts DOR, etc.
- **Streamlined Sales Tax Governing Board** — [streamlinedsalestax.org](https://www.streamlinedsalestax.org/). The multi-state agreement simplifying tax administration for participating states. Provides a single registration mechanism (SSUTA) for its ~24 member states.
- **EU VAT Directive (Council Directive 2006/112/EC, as amended)** — [eur-lex.europa.eu](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:02006L0112-20240101). The statutory basis for EU VAT. Sections relevant to chapter 7:
  - Articles 44-59a — place of supply of services.
  - Articles 358-369x — the One-Stop Shop (OSS), Import One-Stop Shop (IOSS), and Non-Union OSS special schemes.
  - The 2015 changes to place-of-supply for electronically-supplied services.
  - The 2021 changes introducing the €10K distance-sales threshold and expanding the OSS.
- **VIES (VAT Information Exchange System)** — [ec.europa.eu/taxation_customs/vies/](https://ec.europa.eu/taxation_customs/vies/). The EU-wide VAT-number validation system referenced in chapter 7 for the reverse-charge mechanism.
- **UK HMRC — VAT (Notice 700 et al.)** — [gov.uk/government/collections/vat-notices](https://www.gov.uk/government/collections/vat-notices). Post-Brexit UK VAT regime. Referenced in chapter 7 and exercise 07 for the £85K threshold and post-Brexit registration mechanics.
- **Other international VAT / GST references** — the specific country-authority pages for each in-scope market (Australian Tax Office GST guidance, Canada Revenue Agency GST / HST guidance, India GST Council OIDAR guidance, National Tax Agency Japan on Consumption Tax and JCT invoicing). Verify at the source before drafting a registration plan.

### Audit and financial-reporting standards

- **Sarbanes-Oxley Act of 2002 (Pub. L. 107-204)** — [sec.gov/about/laws/soa2002](https://www.sec.gov/about/laws/soa2002.pdf). The statutory basis for public-company financial-reporting-control standards. Sections cited:
  - **§302 — Corporate responsibility for financial reports.** CEO / CFO certification of financial statements and disclosure controls and procedures.
  - **§404 — Management assessment of internal controls.** §404(a) management assessment; §404(b) auditor attestation.
  - **§906 — Corporate responsibility for financial reports.** Separate CEO / CFO certification with criminal penalties.
- **Public Company Accounting Oversight Board (PCAOB)** — [pcaobus.org](https://pcaobus.org/). Standard-setter and regulator for auditors of SEC registrants. Directly relevant:
  - **PCAOB registered-firm directory** — [pcaobus.org/oversight/registration](https://pcaobus.org/oversight/registration). Confirm PCAOB registration before auditor selection (chapter 8 and exercise 08).
  - **PCAOB auditing standards** — the AS series. AS 2201 covers audits of internal control over financial reporting integrated with an audit of financial statements — the specific standard for SOX-404 audits. Referenced in chapter 8.
  - **PCAOB independence rules** — Rule 3520 and adjacent. Referenced in chapter 8 for the pre-approval workflow.
- **SEC Regulation S-K** — [ecfr.gov](https://www.ecfr.gov/current/title-17/chapter-II/part-229) → 17 CFR Part 229. Non-financial disclosure requirements for SEC filings. Sections cited:
  - **Item 303 — Management's Discussion and Analysis of Financial Condition and Results of Operations.** The specific MD&A regulation. Directly referenced in chapter 8 and exercise 08.
  - **Item 407 — Corporate governance.** Includes 407(d)(5) audit committee financial expert; cross-referenced with mod-110 chapter 6.
  - **Item 512 — Undertakings.** The specific undertakings a registrant makes with an S-1 filing.
- **SEC Regulation S-X** — [ecfr.gov](https://www.ecfr.gov/current/title-17/chapter-II/part-210) → 17 CFR Part 210. Financial-statement form and content requirements. Sections cited:
  - **Rule 3-01 — Consolidated balance sheets** (2 years for a registrant).
  - **Rule 3-02 — Consolidated statements of comprehensive income, cash flows, and changes in stockholders' equity** (3 years, or 2 years for EGCs under JOBS Act).
  - **Rule 3-10 — Financial statements of guarantors and issuers of guaranteed securities registered or being registered.**
  - **Article 11 — Pro forma financial information.**
- **Jumpstart Our Business Startups (JOBS) Act of 2012 (Pub. L. 112-106)** — [sec.gov/about/laws/jobsact.htm](https://www.sec.gov/about/laws/jobsact.htm). Introduced the Emerging Growth Company (EGC) status. Key EGC accommodations for chapter 8:
  - Confidential DRS (draft registration statement) submission.
  - Two years of audited financials (rather than three) in the S-1.
  - Testing-the-waters communications with QIBs and institutional accredited investors.
  - Deferred §404(b) auditor attestation for up to 5 years post-IPO.
  - Revenue threshold indexed for inflation (current threshold to be verified at decisioning; recent-cycle indexed value ~$1.235B — confirm at time of use).

### Standards and framework references

- **COSO (Committee of Sponsoring Organizations of the Treadway Commission) — Internal Control – Integrated Framework (2013 Revision)** — [coso.org](https://www.coso.org/guidance-on-ic). The reference internal-controls framework. Directly referenced in chapter 5. The five components (control environment, risk assessment, control activities, information and communication, monitoring) are the vocabulary the SOX-lite and SOX-404 programs use.
- **COSO — Enterprise Risk Management (ERM) 2017 Framework** — [coso.org/enterprise-risk-management](https://www.coso.org/enterprise-risk-management). Adjacent-relevant for the enterprise-risk overlay chapter 5's compensating-control discussion assumes.
- **FASB Accounting Standards Codification (ASC)** — [asc.fasb.org](https://asc.fasb.org/). US GAAP source. The specific ASC references chapter 3 (close design), chapter 4 (audit), and chapter 8 (S-1 and MD&A) traverse:
  - **ASC 606 — Revenue from Contracts with Customers.** The revenue-recognition standard the close, deferred-revenue subledger, and MD&A revenue-driver analysis run against.
  - **ASC 842 — Leases.** Right-of-use asset and lease liability recognition; relevant to the close discipline post-2019.
  - **ASC 718 — Compensation—Stock Compensation.** Stock-based comp; cross-referenced with mod-104.
  - **ASC 740 — Income Taxes.** The tax-provision discipline the audit reviews.
  - **ASC 805 — Business Combinations.** Referenced in exercise 04's M&A extension.
- **AICPA (American Institute of Certified Public Accountants)** — [aicpa-cima.com](https://www.aicpa-cima.com/). Standard-setter for private-company audits (via auditing standards for engagements not subject to PCAOB) and for adjacent practices. Directly relevant:
  - AICPA Statements on Auditing Standards (SAS) series — the private-company audit-standard analog to PCAOB standards.
  - AICPA Audit and Accounting Guide — Not-for-Profit Entities (for adjacent org types).
  - AICPA guidance on start-up entity accounting.

## Tier 2 — Vendor documentation

The finance-ops stack layer. Volatile — verify current pricing, coverage, and feature availability at the vendor's current-vintage documentation.

### Banking and ops

- **Mercury** — [mercury.com](https://mercury.com/). Referenced in chapter 1 for the founder-bookkeeping tier and in chapter 5 for wire-transfer controls (dual approval, ACH filters).
- **Brex** — [brex.com](https://brex.com/). Referenced in chapter 1 for banking + card + bill-pay integration at the seed / Series-A stage.
- **Ramp** — [ramp.com](https://ramp.com/). Referenced in chapter 1 (spend layer), chapter 3 (close automation touch-points), and chapter 5 (spend-authority matrix enforcement).
- **First Citizens Bank (post-SVB-acquisition)** — [firstcitizens.com](https://www.firstcitizens.com/). Referenced in chapter 1 for post-2023 SVB-legacy banking.
- **JPMorgan Chase, Wells Fargo — commercial banking pages** — the traditional-bank alternatives.
- **Meow, Arc, Treasure** — [meow.com](https://meow.com/), [arc.tech](https://arc.tech/), [treasure.tech](https://www.treasure.tech/). Treasury / MMF products referenced in chapter 1.
- **Wise, Airwallex, Nium** — [wise.com](https://wise.com/), [airwallex.com](https://www.airwallex.com/), [nium.com](https://www.nium.com/). International / FX providers referenced in chapter 1's Series-B section.

### General ledger and accounting

- **QuickBooks Online (Intuit)** — [quickbooks.intuit.com](https://quickbooks.intuit.com/). The reference founder-tier GL. Chapter 1 references the QBO → NetSuite migration path.
- **Xero** — [xero.com](https://www.xero.com/). Alternative founder-tier GL, stronger multi-currency handling.
- **NetSuite (Oracle)** — [netsuite.com](https://www.netsuite.com/). The reference Series-B GL migration target. Chapter 1 references NetSuite implementation planning; chapter 3 references NetSuite for the close discipline; chapter 5 for the AP three-way match.
- **Sage Intacct** — [sage.com/en-us/sage-business-cloud/intacct/](https://www.sage.com/en-us/sage-business-cloud/intacct/). Alternative to NetSuite; stronger in services-heavy verticals.

### Payroll and HRIS

- **Gusto** — [gusto.com](https://gusto.com/). Simpler / cheaper payroll for pre-seed / seed. Chapter 1 reference.
- **Rippling** — [rippling.com](https://www.rippling.com/). Combined payroll + HRIS + IT device management. Chapter 1 references the Rippling headcount-cap graduation event.
- **Justworks, TriNet** — [justworks.com](https://www.justworks.com/), [trinet.com](https://www.trinet.com/). PEO alternatives with better benefits pricing but restricted entity-structuring flexibility.
- **Deel, Remote** — [deel.com](https://www.deel.com/), [remote.com](https://remote.com/). International employer-of-record providers for cross-border payroll.
- **Workday HCM** — [workday.com](https://www.workday.com/en-us/products/human-capital-management/overview.html). The enterprise HRIS / payroll / talent target for Series-C+ companies.

### AP / spend / procurement

- **Bill.com** — [bill.com](https://www.bill.com/). Bill-pay for vendor-heavy workflows.
- **Airbase** — [airbase.com](https://www.airbase.com/). Combined spend management; chapter 1 reference.
- **Coupa** — [coupa.com](https://www.coupa.com/). Enterprise procurement reference. Chapter 1 (procurement graduation), chapter 5 (three-way match).
- **Zip** — [ziphq.com](https://ziphq.com/). Modern lightweight procurement alternative with SaaS-vendor focus.
- **SAP Ariba** — [sap.com/products/spend-management/ariba.html](https://www.sap.com/products/spend-management/ariba.html). Enterprise procurement in supplier-heavy industries.
- **SAP Concur** — [concur.com](https://www.concur.com/). Enterprise expense-management reference (over-buying at Series-B).

### FP&A / planning / close

- **Workday Adaptive Planning** — [workday.com/en-us/products/adaptive-planning/overview.html](https://www.workday.com/en-us/products/adaptive-planning/overview.html). The Series-B / C+ FP&A platform reference. Chapter 1 reference.
- **Anaplan** — [anaplan.com](https://www.anaplan.com/). Alternative Series-B / C+ FP&A / planning platform.
- **Vena, Mosaic, Causal, Cube, Pry, Runway** — [venasolutions.com](https://www.venasolutions.com/), [mosaic.tech](https://www.mosaic.tech/), [causal.app](https://www.causal.app/), [cube.dev](https://www.cube.dev/), [pry.co](https://pry.co/), [runway.com](https://www.runway.com/). Alternative FP&A / planning platforms with distinct feature emphasis.
- **OneStream, Fluence, Prophix** — enterprise consolidation platforms referenced in chapter 1's Series-C+ section.
- **FloQast, Blackline, Numeric** — [floqast.com](https://floqast.com/), [blackline.com](https://www.blackline.com/), [numeric.io](https://www.numeric.io/). Close-management and account-reconciliation platforms referenced in chapters 1, 3, and 8.

### Billing / revenue-recognition

- **Stripe (Stripe Billing)** — [stripe.com/billing](https://stripe.com/billing). The default SaaS billing reference.
- **Chargebee, Maxio, Recurly** — [chargebee.com](https://www.chargebee.com/), [maxio.com](https://www.maxio.com/), [recurly.com](https://recurly.com/). Alternative subscription-billing platforms.
- **Metronome, Orb, m3ter** — [metronome.com](https://metronome.com/), [withorb.com](https://www.withorb.com/), [m3ter.com](https://m3ter.com/). Usage-based / consumption billing platforms.
- **RightRev, Ordway** — [rightrev.com](https://rightrev.com/), [ordwaylabs.com](https://ordwaylabs.com/). ASC 606 revenue-recognition automation.
- **Zuora** — [zuora.com](https://www.zuora.com/). Enterprise subscription billing.

### Sales tax / VAT

- **Avalara (AvaTax and Avalara Returns)** — [avalara.com](https://www.avalara.com/). The enterprise sales-tax reference. Chapter 7 and exercise 07.
- **Anrok** — [anrok.com](https://www.anrok.com/). SaaS-native sales tax and VAT. Chapter 7 and exercise 07.
- **TaxJar (Stripe)** — [taxjar.com](https://www.taxjar.com/). SMB / e-commerce sales-tax. Chapter 7.
- **Vertex** — [vertexinc.com](https://www.vertexinc.com/). Enterprise tax engine.
- **Sovos** — [sovos.com](https://sovos.com/). Global VAT / GST compliance.
- **Kintsugi, Numeral** — [trykintsugi.com](https://www.trykintsugi.com/), [numeralhq.com](https://www.numeralhq.com/). Newer entrants targeting the SaaS-native / API-first end.

### Audit / controls / GRC tooling

- **AuditBoard** — [auditboard.com](https://www.auditboard.com/). SOX / audit-workflow platform. Chapter 5 and chapter 8.
- **Workiva** — [workiva.com](https://www.workiva.com/). Financial reporting, SOX, and disclosure-management platform. Chapter 8 for the S-1 workflow.

### Treasury and cash management

- **Kyriba, GTreasury, Trovata** — [kyriba.com](https://www.kyriba.com/), [gtreasury.com](https://www.gtreasury.com/), [trovata.io](https://trovata.io/). Enterprise treasury / cash-visibility platforms referenced in chapter 1's Series-C+ section.

### Equity administration and cap-table

- **Carta** — [carta.com](https://carta.com/). Cap-table platform; also the source of the *State of Startup Compensation* and cap-table / market-benchmark data referenced in chapter 2 and exercise 02.
- **Pulley, Shareworks (Morgan Stanley), AngelList Stack** — alternative equity-administration platforms.

### R&D-credit specialty firms

- **alliantgroup, KBKG, Endeavor Advisors** — [alliantgroup.com](https://alliantgroup.com/), [kbkg.com](https://www.kbkg.com/), [endeavoradvisors.com](https://endeavoradvisors.com/). Independent R&D-credit specialty practices. Chapter 6 and exercise 06.
- **Big Four practices** — Deloitte, PwC, EY, KPMG each have R&D-credit practices; verify current pricing and engagement models.

## Tier 3 — Practitioner canon and startup-CFO reference

The books, blog archives, and specialty publications that populate the pattern library.

### Startup-CFO / finance-ops blogs and firms

- **Kruze Consulting** — [kruzeconsulting.com](https://kruzeconsulting.com/). Outsourced CFO / accounting firm serving venture-backed startups. Public content on: R&D-credit qualification, close-cycle practice, sales-tax nexus, audit-prep, benchmarks. Referenced across chapters 3, 4, 6, and 7.
- **Pilot** — [pilot.com](https://pilot.com/). Outsourced bookkeeping / CFO firm. Publishes practitioner content on close, audit-prep, and R&D-credit.
- **Bench, Zeni** — [bench.co](https://bench.co/), [zeni.ai](https://zeni.ai/). Alternative outsourced-bookkeeping providers.
- **Burkland Associates** — [burklandassociates.com](https://burklandassociates.com/). Fractional-CFO firm; publishes on startup-CFO practice.
- **Propeller Industries** — [propellerindustries.com](https://www.propellerindustries.com/). Fractional-CFO / outsourced-finance firm.
- **The CFO Perspective (Steve Rosvold)** — practitioner blog / podcast on the CFO role.

### Comp benchmarks

- **Carta — *State of Startup Compensation* (annual)** — [carta.com/blog/state-of-startup-compensation](https://carta.com/blog/state-of-startup-compensation/) or the current-year URL. The annual reference for cash and equity benchmarks at venture-backed private companies. Chapter 2 and exercise 02.
- **Pave** — [pave.com](https://www.pave.com/). Real-time comp benchmark data; used by high-growth startups for offer benchmarking. Chapter 2.
- **Option Impact (Advanced-HR)** — the historical venture-backed-comp benchmark tool.
- **Radford (Aon)** — [aon.com/human-capital-consulting/radford](https://www.aon.com/human-capital-consulting/radford/). Enterprise executive-comp benchmark; used at the growth-stage and public-company end.
- **Compensia** — [compensia.com](https://www.compensia.com/). Executive comp advisory serving both private and public companies. Referenced in mod-110 chapter 6 for the comp-committee cadence.

### Board and CFO-adjacent canon

- **Brad Feld and Mahendra Ramsinghani — *Startup Boards*** — Wiley, 2nd edition. Cross-referenced from mod-110 as the reference board-craft canon; relevant to chapter 2 for the audit-committee cadence and chapter 8 for the pre-IPO governance rebuild.
- **Fred Wilson — *AVC*** — [avc.com](https://avc.com/). Referenced across the module for CFO-role and pre-IPO discipline.
- **David Sacks — essays on operating discipline and the CFO role** — [sacks.substack.com](https://sacks.substack.com/). Referenced for the CFO-operating-cadence pattern.
- **Bill Gurley — *Above the Crowd*** — [abovethecrowd.com](http://abovethecrowd.com/). Referenced for governance-failure-mode and pre-IPO discipline.
- **Scott Kupor — *Secrets of Sand Hill Road*** — Portfolio, 2019. The a16z inside view of how investor-side diligence and pre-IPO conversations run.
- **Ben Horowitz — *The Hard Thing About Hard Things*** — HarperBusiness, 2014. Chapter on the CFO role in difficult periods.

### CFO-specific books and reference

- **Jack McCullough — *Secrets of Rockstar CFOs*** and adjacent CFO-Leadership Council content — [cfoleadership.com](https://cfoleadership.com/). Practitioner-community content on the CFO-role transition from operator to strategist.
- **Larry Reinharz and Steven Bragg — *The New CFO Financial Leadership Manual*** — Wiley. Reference for CFO operating discipline.
- **The CFO Yearbook (annual publisher content)** and specialty-CFO practitioner books — verify current-vintage editions.

### Sales-tax / VAT practitioner content

- **TaxOps, TaxConnex, Peisner Johnson** — [taxops.com](https://www.taxops.com/), [taxconnex.com](https://www.taxconnex.com/), [peisnerjohnson.com](https://peisnerjohnson.com/). Specialty sales-tax firms that run nexus studies and VDAs for the mid-market. Referenced in chapter 7.
- **Bloomberg Tax — sales-tax reference** — [pro.bloombergtax.com](https://pro.bloombergtax.com/). Practitioner reference for state-by-state SaaS-taxability updates.
- **Sales Tax Institute** — [salestaxinstitute.com](https://www.salestaxinstitute.com/). Practitioner reference from Diane Yetter and colleagues.

### R&D-credit practitioner content

- **Journal of Accountancy, Tax Adviser (AICPA journals)** — periodic articles on §41 practice.
- **BDO — R&D Tax Credit practitioner content**, **RSM — R&D-credit practitioner content** — the second-tier practices publish accessible guidance.

## Tier 4 — Adjacent-track cross-references

Modules within the Startup Finance & Fundraising track that intersect with mod-111.

- [`mod-101 — Startup Accounting Foundations`](../mod-101-startup-accounting-foundations/) — the accrual mechanics the close and audit sit on top of; ASC 606 revenue-recognition foundation the deferred-revenue subledger in chapter 3 encodes.
- [`mod-102 — Unit Economics and Cohort Financial Modelling`](../mod-102-unit-economics-and-cohort-financial-modelling/) — the KPI definitions the FP&A team maintains against the close; the cohort-NRR / CAC / LTV metrics that must reconcile to the ledger.
- [`mod-103 — Three-Statement Model and Driver-Based Forecasting`](../mod-103-three-statement-model-and-driver-based-forecasting/) — the operating model the FP&A team maintains and reconciles to actuals; the driver-based forecast that anchors the MD&A comparison of results (chapter 8).
- [`mod-104 — Cap Tables and Equity Compensation`](../mod-104-cap-tables-and-equity-compensation/) — the stock-based-comp accounting and disclosures referenced in chapter 4's year-one deficiency-anticipation memo and chapter 8's S-1 executive-compensation section.
- [`mod-105 — Convertible Instruments`](../mod-105-convertible-instruments/) — the SAFE / note accounting the close and audit must handle at pre-priced-round stages.
- [`mod-106 — Startup Valuation Frameworks`](../mod-106-startup-valuation-frameworks/) — the valuation framework the pre-IPO S-1 comparable analysis draws on (chapter 8's dual-track convergence memo).
- [`mod-107 — Fundraising Strategy and Investor Targeting`](../mod-107-fundraising-strategy-and-investor-targeting/) — the CFO-in-the-raise workstream that the pre-IPO dual-track's private-path runs against; the diligence-ready-actuals discipline chapter 4 supports.
- [`mod-108 — Term Sheets and Preferred-Stock Economics`](../mod-108-term-sheets-and-preferred-stock-economics/) — the preferred-stock economics the CFO tracks through the pre-IPO cap-table lens (chapter 8).
- [`mod-109 — Runway Management and Bridge Financing`](../mod-109-runway-management-and-bridge-financing/) — the runway math that decides when a hire is affordable, when a migration is on the critical path, and the specific "when must we price / close" backstop against the dual-track (chapter 8, exercise 08).
- [`mod-110 — Board and Investor Governance for the CFO`](../mod-110-board-and-investor-governance-for-the-cfo/) — the board channel the audit-committee-ownership of the audit-readiness workstream and controls program reports into; the pre-IPO governance rebuild (mod-110 chapter 6) that chapter 8 sits on top of.

Cross-track:

- [`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum) — the transaction-execution mechanics (underwriter selection, pricing mechanics, roadshow, SEC comment-letter response process at the specific-tactical level, syndicate structure, lock-up mechanics, M&A definitive-agreement negotiation) that this module hands off to. Explicitly deferred sideways in chapters 8 and 9 and in exercise 08.
- **`startup-accounting-controllership` (planned, not yet authored)** — the future track that would own the operator-mechanic depth (bookkeeping mechanics, staff-accountant close mechanics, technical-accounting position-authoring) this module explicitly does *not* teach at the operator level. Referenced in chapter 9 as the ownership-boundary partner track.
- [`founder-ceo-curriculum`](https://github.com/ai-startup-curriculum/founder-ceo-curriculum) — the CEO-side of the CFO / CEO partnership, especially through the pre-IPO period.
- [`legal-founders-curriculum`](https://github.com/ai-startup-curriculum/legal-founders-curriculum) — the outside-counsel-side of the S-1, corporate-governance, and audit-committee work.

## Reading order for this module

If you are new to the finance-ops / controls / pre-IPO canon, this is the order to read:

1. **IRC §41 and Treas. Reg. §1.41.** The statutory reference for R&D credit; short and specific. Read before decisioning any credit position.
2. **SEC Regulation S-K Item 303 (MD&A) and Regulation S-X Rule 3-01 / 3-02 (financial-statement forms).** The specific reference for the S-1 / MD&A drafting workstream (chapter 8).
3. **Sarbanes-Oxley §302 and §404.** The statutory basis for public-company internal-control obligations.
4. **COSO Internal Control – Integrated Framework (2013).** The reference internal-controls framework. Read before drafting any controls matrix.
5. ***South Dakota v. Wayfair, Inc.*** — the specific Supreme Court decision underlying post-2018 sales-tax exposure.
6. **JOBS Act of 2012.** The specific accommodations for Emerging Growth Companies that reshape the pre-IPO S-1 and SOX-404 timelines.
7. **PCAOB registered-firm directory** and current PCAOB independence rules. Read before auditor selection.
8. **NetSuite and Workday Adaptive implementation guides.** For any CFO on the specific Series-B / C migration path.
9. **The current *Carta State of Startup Compensation* (or Pave benchmark).** For any comp-benchmark decisioning (chapter 2, exercise 02).
10. **Kruze Consulting and Pilot public content on R&D-credit, sales-tax, and close-discipline.** The practitioner-canon reference for the operating-side patterns.
11. **Feld & Ramsinghani, *Startup Boards*** — the board-craft reference (cross-referenced from mod-110); relevant for the audit-committee ownership of the audit-readiness workstream.
12. **Current-vintage state DOR sales-tax pages** for any state the company has nexus in.

Only after that canon should you rely on secondary practitioner content (LinkedIn essays, Substacks, conference talks). Every quantitative claim in a memo, controls matrix, or plan should trace to a tier-1 through tier-3 source; every unverified claim should be flagged `[assumption]` or `<!-- needs-research: ... -->`. The pre-IPO CFO's writing is the most-scrutinised writing a private-company operator produces; the discipline of citing to source is the discipline that carries the writing through SEC comment.
