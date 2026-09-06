# Resources — mod-103 Three-Statement Model & Driver-Based Forecasting

This is the reference stack behind every chapter and exercise in this module. Sources are grouped by tier of authority: read tier-1 primary standards and tier-2 spreadsheet-modelling standards first; treat tier-5 practitioner content and vendor documentation as interpretive, not authoritative. Every benchmark citation and every "convention" claim in the chapters should be verifiable against something in this list.

Because published SaaS benchmark data shifts materially year to year (OpenView, Bessemer, KeyBanc, and Meritech all refresh their surveys annually and the bands for "healthy" burn multiple, "best-in-class" NRR, and Rule-of-40 frontier move with the market), always cite the specific report year when quoting a band in a board pack or a fundraise deck. Similarly, the FP&A-platform landscape (chapter 8) consolidates and re-tiers roughly every 18-24 months; verify the current product positioning of any platform before recommending it. The `<!-- needs-research -->` markers in the chapters flag places where current-year data should be re-verified.

## Tier 1 — Authoritative accounting standards

The three statements are three views of the same underlying transactions under GAAP. The standards define the presentation and reconciliation that every chapter in this module assumes.

- **FASB Accounting Standards Codification** — [asc.fasb.org](https://asc.fasb.org/). Basic view is free; register for access.
  - **ASC Topic 230 — *Statement of Cash Flows*** — presentation and classification of operating, investing, and financing cash flows; indirect method vs. direct method (chapter 1). This is the standard that defines the CFS shape every chapter assumes.
  - **ASC Topic 606 — *Revenue from Contracts with Customers*** — the five-step model governing recognised revenue on the P&L and the deferred-revenue liability on the balance sheet (chapter 1's deferred-revenue walk; chapter 4's cohort revenue schedule). Bookings-vs-billings-vs-revenue-vs-cash mechanics rely on this.
  - **ASC Topic 340-40 — *Other Assets and Deferred Costs — Contracts with Customers*** — capitalisation and amortisation of contract-acquisition costs (sales commissions). Drives chapter 3's deferred-commission asset walk and the SBC schedule's commission piece.
  - **ASC Topic 350-40 — *Internal-Use Software*** — capitalisation of software-development costs during the application-development phase, with amortisation over useful life (chapter 3's capitalised-software line on the balance sheet).
  - **ASC Topic 718 — *Compensation — Stock Compensation*** — recognition and measurement of share-based payment awards; drives the SBC schedule on the hiring plan (chapter 3).
  - **ASC Topic 842 — *Leases*** — right-of-use assets and lease liabilities on the balance sheet; drives the lease-schedule inputs (chapter 1's balance-sheet shape includes ROU assets when in scope).
- **SEC Regulation S-X, Rule 5-03** — [ecfr.gov Title 17 Part 210](https://www.ecfr.gov/current/title-17/chapter-II/part-210). Prescribed public-company income-statement format. Leaves specific definitions of "cost of revenue" to management judgement; the SaaS-metrics canon (below) is the reference for how SaaS COGS is classified in practice.
- **SEC EDGAR** — [sec.gov/edgar](https://www.sec.gov/edgar). Every listed SaaS company's 10-K and 10-Q. Useful for observing how a mature public SaaS company structures its three-statement model at the presentation layer: Snowflake, Datadog, HubSpot, CrowdStrike, MongoDB, ServiceNow, Salesforce, Zoom, Atlassian.
- **IFRS 15 — *Revenue from Contracts with Customers*** — [ifrs.org](https://www.ifrs.org/issued-standards/list-of-standards/ifrs-15-revenue-from-contracts-with-customers/). The IASB standard converged with ASC 606. Relevant for internationally-operating companies whose non-US subsidiaries file under IFRS.
- **IFRS 16 — *Leases*** — [ifrs.org](https://www.ifrs.org/issued-standards/list-of-standards/ifrs-16-leases/). IFRS equivalent of ASC 842.

## Tier 2 — Spreadsheet-modelling standards

These are the industry standards for how spreadsheet financial models are structured, colour-coded, versioned, and reviewed. Chapter 2 (driver / assumption architecture) and chapter 8 (review checklist, failure modes) rely on them directly.

- **FAST Standard** — [fast-standard.org](https://www.fast-standard.org/). The most-cited spreadsheet-modelling standard, originating in project-finance modelling and now widely adopted in corporate FP&A. Covers structure (inputs → drivers → statements → outputs), formula construction (one operation per formula, consistent row-wise formulas across time columns), colour convention (blue for input, black for formula, green for cross-sheet link, red for external link), and review discipline. The FAST Standard document is downloadable at no charge.
- **ICAEW — *Twenty Principles for Good Spreadsheet Practice*** — [icaew.com Twenty Principles](https://www.icaew.com/technical/technology/excel/twenty-principles). Published by the Institute of Chartered Accountants in England and Wales. A concise 20-principle statement that covers model design, control, testing, and documentation. Read alongside the FAST Standard for the wider accountancy-profession view.
- **SSRB — *Spreadsheet Standards Review Board*** — historically maintained the SSRB modelling standards used at bulge-bracket investment banks; still cited in Wall Street modelling training materials. The modern practitioner reference has migrated toward FAST, but the SSRB layout conventions (colour, row-consistency, unit labels) remain widely followed. See practitioner references at [Wall Street Prep](https://www.wallstreetprep.com/) and [Corporate Finance Institute](https://corporatefinanceinstitute.com/).
- **EuSpRIG — *European Spreadsheet Risks Interest Group*** — [eusprig.org](https://eusprig.org/). Academic and practitioner group publishing research on spreadsheet errors, control failures, and mitigation. The EuSpRIG "horror stories" catalogue is a useful reference for chapter 8's failure-mode taxonomy — documented real-world spreadsheet failures with material financial impact.

## Tier 3 — SaaS-metrics canon

The definitional essays that establish the KPI vocabulary in chapters 4, 5, 6, and 7. Every SaaS CFO has read most of these; investors expect familiarity with the terminology. See [`mod-102/resources.md`](../mod-102-unit-economics-and-cohort-financial-modelling/resources.md) for the full canon; the subset most-cited in this module:

- **David Skok — *SaaS Metrics 2.0*** — [forentrepreneurs.com/saas-metrics-2/](https://www.forentrepreneurs.com/saas-metrics-2/). The single most-cited SaaS-metrics essay. Defines bookings vs. billings vs. revenue, MRR / ARR movement, CAC, LTV, LTV:CAC ratio, months-to-recover-CAC, and the magic number. Chapters 4 and 7 sit on this vocabulary.
- **David Sacks — *The Burn Multiple*** — Craft Ventures Substack, [sacks.substack.com](https://sacks.substack.com/). The 2020 essay that formalised burn multiple as a capital-efficiency instrument (referenced in chapter 7's KPI set).
- **a16z — *16 Startup Metrics*** — [a16z.com/16-startup-metrics/](https://a16z.com/16-startup-metrics/). Definitional essay covering first-order metrics.
- **a16z — *16 More Startup Metrics*** — [a16z.com/16-more-metrics-to-watch/](https://a16z.com/16-more-metrics-to-watch/). Second-order metrics (gross vs. net revenue, GMV vs. revenue, bookings vs. billings, cohort-based measures).
- **Brad Feld — *Rule of 40*** — [feld.com](https://feld.com/). The originating post for the Rule of 40 (revenue growth % + EBITDA margin % ≥ 40 for a healthy SaaS trajectory). Referenced in chapter 7's KPI set.
- **Scale Venture Partners — magic number** — [scalevp.com](https://www.scalevp.com/). The originating firm for the magic number ((ΔARR × 4) / prior-quarter S&M spend) as a sales-efficiency instrument.
- **Tomasz Tunguz** — [tomtunguz.com](https://tomtunguz.com/). Long-running blog by the Redpoint partner. Deep archive of essays on cohort analysis, CAC, LTV, sales efficiency, NRR, and stage-specific benchmarks that feed chapters 4-7's forecast-driver benchmarks.
- **Christoph Janz — *Point Nine Capital*** — [pointnine.com/blog](https://www.pointnine.com/blog) and [christophjanz.com](https://christophjanz.com/). Essays on SaaS unit economics, funnel benchmarks, and the "5 ways to build a $100M business" framing that underlies the chapter 5 top-down TAM discussion.

## Tier 4 — Authoritative benchmark providers

The four or five providers a CFO cites when a board pack or a fundraise deck references a benchmark band. Each publishes annually or continuously; check the current year at citation time. See [`mod-102/resources.md`](../mod-102-unit-economics-and-cohort-financial-modelling/resources.md) for detailed treatment; the subset most-relevant to this module:

- **OpenView SaaS Benchmarks Report** — [openviewpartners.com](https://openviewpartners.com/) → Insights → SaaS Benchmarks Report. Annual survey of hundreds of private SaaS companies, segmented by ARR band, motion (PLG vs. sales-led), and industry. Primary reference for driver-forecast bands (S&M / R&D / G&A as percent of revenue, CAC payback, burn multiple) by ARR stage. Chapters 3 and 4 lean on it for the "what does a reasonable non-payroll opex ratio look like at this stage" and "what's a defensible SDR productivity assumption" questions.
- **Bessemer Venture Partners State of the Cloud** — [bvp.com/atlas/state-of-the-cloud](https://www.bvp.com/atlas/state-of-the-cloud). Annual analysis with a strong late-stage and public-SaaS focus. Rule of 40 frontier analysis, cash conversion score, and the "Best Cloud Companies" NRR bands. Chapter 7 cites it.
- **Bessemer Cloud Index (EMCLOUD)** — [cloudindex.bvp.com](https://cloudindex.bvp.com/). Real-time public-SaaS basket with revenue multiples, growth rates, gross margins, and Rule of 40 scores. Continuously updated.
- **Meritech Capital SaaS Comps** — [meritechcapital.com/saas-comps-table](https://www.meritechcapital.com/saas-comps-table). Current-quarter public-SaaS metrics with revenue-multiple correlations to Rule of 40, NRR, and growth rate. Referenced in the top-down analog TAM discussion in chapter 5.
- **KeyBanc Capital Markets Annual SaaS Survey** — cover page and executive summary at [key.com](https://www.key.com/businesses-institutions/industry-expertise/technology.html); the full report is typically distributed to SaaS-industry participants and via partner networks. Detailed unit-economics and expense-ratio benchmarks for private SaaS companies; complements the OpenView dataset.
- **SaaStr Annual State of SaaS** — [saastr.com](https://www.saastr.com/). Practitioner-oriented benchmarks; useful for CAC, sales-efficiency, and stage-transition data that feed the funnel-forecast defaults in chapter 4.
- **Bridge Group — SDR Metrics Report and AE Report** — [bridgegroupinc.com](https://bridgegroupinc.com/). Annual studies of SDR and AE productivity, ramp time, quota attainment, and comp — the reference for defensible SDR / AE productivity assumptions in the funnel and the hiring plan (chapters 3-4 and exercise 04's capacity check).

## Tier 5 — Compensation, hiring, and equity benchmarks

The hiring plan in chapter 3 and exercise 02 relies on salary and burden-rate benchmarks. The SBC schedule relies on 409A / fair-value methodology. These are the reference sources:

- **Pave** — [pave.com](https://www.pave.com/). Real-time compensation benchmarking pulled from partner-company payroll data. The current-market reference for salary bands by role, level, and geography. Free tier available; paid tier for full data access.
- **Carta Total Comp** — [carta.com/blog/carta-total-comp/](https://carta.com/blog/carta-total-comp/). Carta's compensation benchmarking product, sourced from equity and payroll data flowing through Carta's cap-table and payroll systems. Reference for salary + equity combined comp bands.
- **Radford (Aon) — technology compensation surveys** — [aon.com/human-capital-consulting/radford](https://www.aon.com/human-capital-consulting/radford/). Institutional-grade compensation surveys used by public and later-stage private companies for market benchmarking.
- **Option Impact / Advanced-HR** — [advanced-hr.com](https://www.advanced-hr.com/). Venture-industry compensation-benchmark database used by VC firms and their portfolio companies.
- **Levels.fyi** — [levels.fyi](https://www.levels.fyi/). User-submitted total-comp data, strongest coverage for engineering roles at big-tech and later-stage private companies. Directional rather than definitive but useful for reality-checking a benchmark.
- **AICPA / ASA business-valuation resources** — [aicpa.org](https://www.aicpa.org/) and [appraisers.org](https://www.appraisers.org/). Standards and guidance behind 409A valuations that produce the per-employee grant fair value used in the SBC schedule (chapter 3). See also [`mod-104`](../mod-104-cap-tables-and-equity-compensation/) for full 409A methodology.
- **Aranca / Scalar / Carta 409A** — [aranca.com](https://www.aranca.com/), [scalar.io](https://scalar.io/), [carta.com/409a-valuations](https://carta.com/409a-valuations/). Three of the common 409A providers; their published methodology documents are useful as references for how the per-share fair value is derived.

## Tier 6 — TAM / market-sizing sources

Chapter 5 and exercise 04 rely on published industry-research numbers for the top-down TAM view. Standard sources:

- **Gartner** — [gartner.com](https://www.gartner.com/). Industry-analyst research covering enterprise software market sizes, segment growth rates, and Magic Quadrant positioning. Access typically via subscription; some summary numbers appear in press releases and analyst-day disclosures at [gartner.com/en/newsroom](https://www.gartner.com/en/newsroom).
- **IDC** — [idc.com](https://www.idc.com/). Industry-analyst research complement to Gartner; often provides sizing for infrastructure, cloud, and platform categories.
- **Forrester** — [forrester.com](https://www.forrester.com/). Third of the three primary enterprise-tech analyst firms; strong on the buyer-persona and customer-experience dimensions.
- **Statista** — [statista.com](https://www.statista.com/). Aggregator of published market sizes across many industries. Cheaper access than Gartner / IDC / Forrester; sources are usually cited so the underlying provider can be traced.
- **PitchBook** — [pitchbook.com](https://pitchbook.com/). Private-market data provider (deals, funding rounds, valuations). Useful for the analog-based TAM method (chapter 5) — locate a comparable company's ARR at a comparable stage.
- **CB Insights** — [cbinsights.com](https://www.cbinsights.com/). Similar space to PitchBook; strong on emerging-category identification and startup landscape mapping.
- **Crunchbase** — [crunchbase.com](https://www.crunchbase.com/). Free tier and paid tier. Useful for the bottom-up count × price TAM method — identify buyer count in an ICP by industry, size, and geography filters.
- **ZoomInfo** — [zoominfo.com](https://www.zoominfo.com/). Company database with firmographic filters (industry, size, revenue, tech stack). Alternative to Crunchbase for the bottom-up count × price TAM method.
- **LinkedIn Sales Navigator** — [business.linkedin.com/sales-solutions/sales-navigator](https://business.linkedin.com/sales-solutions/sales-navigator). Filter LinkedIn's company and contact data by ICP dimensions; often the most-defensible source for buyer counts because filters are auditable.
- **US Census Bureau — County Business Patterns** — [census.gov/programs-surveys/cbp.html](https://www.census.gov/programs-surveys/cbp.html). Establishment counts by industry (NAICS) and geography. Government-sourced and free. Useful for TAM when the ICP is defined by industry code.
- **Bureau of Labor Statistics — Occupational Employment and Wages** — [bls.gov/oes](https://www.bls.gov/oes/). Employment counts by occupation, industry, and geography. Useful for TAMs sized by "number of workers with role X."

## Tier 7 — Financial-modelling textbooks and courses

For the practitioner who wants to go deeper on modelling technique.

- **Simon Benninga — *Financial Modeling*** — MIT Press, multiple editions (current is the 5th). The canonical academic-and-practitioner reference on financial modelling in Excel. Covers three-statement modelling, valuation, capital-structure modelling, and Monte Carlo simulation. Wider scope than SaaS but the modelling discipline is directly applicable.
- **Danielle Stein Fairhurst — *Using Excel for Business and Financial Modelling*** — Wiley, multiple editions. Practitioner-oriented, focused on operating models rather than trader / valuation models. Strong on the driver-based architecture, scenario / sensitivity workflow, and dashboarding that chapters 2, 6, and 7 cover.
- **Wall Street Prep** — [wallstreetprep.com](https://www.wallstreetprep.com/). Investment-banking modelling training. The three-statement modelling and DCF courses are the widely-used reference for the bulge-bracket layout conventions.
- **Corporate Finance Institute** — [corporatefinanceinstitute.com](https://corporatefinanceinstitute.com/). Broad-catalogue online modelling training with certifications (FMVA). Useful as a self-directed reference for specific modelling techniques.
- **Breaking Into Wall Street** — [breakingintowallstreet.com](https://breakingintowallstreet.com/). Investment-banking / private-equity modelling training with detailed step-by-step three-statement builds for various industries.
- **Aswath Damodaran — *Corporate Finance* and *Applied Corporate Finance*** — Wiley, multiple editions. NYU Stern's Damodaran; the theoretical anchor behind DCF modelling, cost-of-capital construction, and the working-capital / cash-flow reconciliation that chapters 1 and 6 rely on. Online materials free at [pages.stern.nyu.edu/~adamodar/](https://pages.stern.nyu.edu/~adamodar/).

## Tier 8 — FP&A platforms (chapter 8's landscape)

Chapter 8 covers the CFO-level decision on when to move a spreadsheet model to a purpose-built platform. Vendor documentation and independent reviews:

**Native cloud (spreadsheet-successor) — best fit for early- to mid-stage:**

- **Causal** — [causal.app](https://www.causal.app/). Cloud-first, formula-driven, treats time as a first-class dimension. Strong scenario/sensitivity; native Monte Carlo. Docs at [help.causal.app](https://help.causal.app/).
- **Runway** — [runway.com](https://runway.com/). Series-A through Series-B; spreadsheet-successor positioning with strong version control and multi-scenario modelling. Emphasis on operational-model integration.
- **Mosaic** — [mosaic.tech](https://www.mosaic.tech/). Series-B onward; lightweight EPM with integrated dashboarding, workforce planning, actuals-connectors.

**Established mid-market — best fit for growth-stage:**

- **Anaplan** — [anaplan.com](https://www.anaplan.com/). Mid-market to enterprise. Multi-dimensional modelling language (Hyperblock). Docs at [help.anaplan.com](https://help.anaplan.com/).
- **Workday Adaptive Planning** — [workday.com/en-us/products/adaptive-planning](https://www.workday.com/en-us/products/adaptive-planning/overview.html). Formerly Adaptive Insights. Mid-market to enterprise; strong actuals-integration to Workday and other ERPs.
- **Vena** — [venasolutions.com](https://www.venasolutions.com/). Excel-native workflow layer on top of Excel; compromise for teams wanting tooling without leaving Excel.
- **OneStream** — [onestream.com](https://www.onestream.com/). Unified corporate performance management platform; mid-market to enterprise.

**Enterprise / legacy — best fit for very large companies:**

- **Oracle EPM Cloud (Hyperion)** — [oracle.com/performance-management](https://www.oracle.com/performance-management/). Enterprise-scale.
- **SAP BPC / Analytics Cloud** — [sap.com](https://www.sap.com/products/technology-platform/cloud-analytics.html). Enterprise-scale, tight ERP integration for SAP-heavy organisations.
- **IBM Planning Analytics (Cognos TM1)** — [ibm.com/products/planning-analytics](https://www.ibm.com/products/planning-analytics). Enterprise-scale, multi-dimensional modelling.

**Startup-native and adjacent — narrower use cases:**

- **Pry (Brex)** — [pry.co](https://www.pry.co/). Very-early-stage; simple cash-flow forecasting.
- **Finmark** — [finmark.com](https://www.finmark.com/). Seed / Series-A; automated three-statement modelling.
- **Jirav** — [jirav.com](https://www.jirav.com/). SMB / small business; QBO / Xero integration.
- **Abacum** — [abacum.io](https://www.abacum.io/). Series-A through Series-C; collaboration-first FP&A.
- **Cube** — [cubesoftware.com](https://www.cubesoftware.com/). Spreadsheet-native FP&A that layers on top of Excel / Sheets.
- **Aleph** — [getaleph.com](https://www.getaleph.com/). Spreadsheet-native, Excel-first FP&A tool.

**Vendor-independent evaluation and comparison:**

- **Gartner Magic Quadrant for Cloud Financial Planning and Analysis Solutions** — [gartner.com](https://www.gartner.com/) reviews. Subscription-only; the industry-standard vendor-comparison reference.
- **G2 Crowd — FP&A Software category** — [g2.com/categories/corporate-performance-management-cpm](https://www.g2.com/categories/corporate-performance-management-cpm/). User-review-based vendor comparison; free tier.
- **Nucleus Research — CPM Value Matrix** — [nucleusresearch.com](https://nucleusresearch.com/). Independent analyst reports on CPM / FP&A vendors.

## Tier 9 — Big Four and accounting-firm interpretive guides

- **Deloitte — *Roadmap: Statement of Cash Flows*** — [www2.deloitte.com/us/en/pages/audit/articles/a-roadmap-to-the-preparation-of-the-statement-of-cash-flows.html](https://www2.deloitte.com/us/en/pages/audit/articles/a-roadmap-to-the-preparation-of-the-statement-of-cash-flows.html). Detailed interpretive guide to ASC 230 — the reference for CFS classification questions.
- **PwC — *Financial Statement Presentation* guide** — [viewpoint.pwc.com](https://viewpoint.pwc.com/). Comprehensive interpretive guide to statement presentation, cash-flow classification, and disclosure. Requires free registration.
- **EY — *Financial Reporting Developments: Statement of Cash Flows*** — [ey.com](https://www.ey.com/). EY's interpretive guide to ASC 230.
- **KPMG — *Handbooks* series (Revenue, Leases, Financial instruments, Statement of Cash Flows)** — [frv.kpmg.us](https://frv.kpmg.us/). Publicly-available handbooks covering the specific accounting topics that drive the three-statement model.

See [`mod-101` resources](../mod-101-startup-accounting-foundations/resources.md) for the full Big Four revenue-recognition and lease-accounting library referenced by earlier modules; the guides above are the specific ones cited in this module for the statement-shape and CFS-presentation questions.

## Tier 10 — Real broken-model teaching material

Exercise 07 (failure teardown) benefits from working through documented real-world spreadsheet failures.

- **EuSpRIG horror-stories archive** — [eusprig.org/research-info/horror-stories/](https://eusprig.org/research-info/horror-stories/). Documented spreadsheet errors from public disclosures, regulatory filings, and press coverage. Includes the JPMorgan London Whale VaR-model error, the Reinhart-Rogoff growth-vs-debt paper error, the TransAlta $24M copy-paste error, and dozens of others. Each is a real-world example of one or more of chapter 8's seven failure modes.
- **Institute of Chartered Accountants of Scotland — *Spreadsheet Risk Management*** — [icas.com](https://www.icas.com/). Professional guidance on spreadsheet-risk controls; the accountancy-profession complement to EuSpRIG's academic view.
- **Powell, S., Baker, K., & Lawson, B. — *A Critical Review of the Literature on Spreadsheet Errors*** — Decision Support Systems, 2008. Academic literature review of the empirical spreadsheet-error rate; useful context for why the review checklist matters (empirically, ~1-5% of cells in unreviewed models contain errors).

## Cross-references to other modules in this track

- [`mod-101` — Startup Accounting Foundations](../mod-101-startup-accounting-foundations/) — accrual accounting, ASC 606, deferred revenue, bookings-vs-billings-vs-revenue-vs-cash. Prerequisite; the accrual P&L that chapter 1 builds on is defined there.
- [`mod-102` — Unit Economics and Cohort Financial Modelling](../mod-102-unit-economics-and-cohort-financial-modelling/) — cohort retention (feeds chapter 4's cohort revenue schedule), fully-loaded CAC (feeds chapter 4's CAC driver), gross-margin bridge (feeds the gross-margin driver), NRR / GRR / burn multiple / Rule of 40 (feed chapter 7's KPI set).
- [`mod-104` — Cap Tables and Equity Compensation](../mod-104-cap-tables-and-equity-compensation/) — 409A valuation and SBC fair-value methodology consumed by chapter 3's SBC schedule.
- [`mod-106` — Startup Valuation Frameworks](../mod-106-startup-valuation-frameworks/) — the DCF, revenue-multiple, and comparable-company valuations run off the forecast this module produces.
- [`mod-107` — Fundraising Strategy and Investor Targeting](../mod-107-fundraising-strategy-and-investor-targeting/) — the model is a required data-room artefact; round sizing and use-of-proceeds are answered by running the scenarios (chapter 6).
- [`mod-109` — Runway Management and Bridge Financing](../mod-109-runway-management-and-bridge-financing/) — runway management is a live re-forecast of this model as actuals come in.
- [`mod-110` — Board and Investor Governance for the CFO](../mod-110-board-and-investor-governance-for-the-cfo/) — the board-pack dashboard is the artefact chapter 7 builds; the quarterly re-forecast is a versioned rebuild of this model.
- [`mod-111` — Finance Operations, Controls, and Team Design](../mod-111-finance-operations-controls-and-team-design/) — the CFO-level decision on FP&A tooling and platform migration (chapter 8) at Series-B and beyond is developed further there.

## Reading order for this module

If you are new to CFO-grade three-statement modelling, read in this order before working through the exercises:

1. **ASC 230, ASC 606, ASC 340-40** — the accounting substrate. Read at the summary level; deep dives via the Big Four interpretive guides when specific questions arise.
2. **FAST Standard document** — the spreadsheet-modelling architecture that chapter 2 assumes.
3. **ICAEW *Twenty Principles*** — the concise accountancy-profession view of spreadsheet discipline.
4. **David Skok, *SaaS Metrics 2.0*** — the SaaS-metrics vocabulary that chapters 4-7 use throughout.
5. **OpenView SaaS Benchmarks (current year)** — the driver-forecast bands (S&M / R&D / G&A ratios, CAC payback, burn multiple).
6. **Bessemer *State of the Cloud* (current year)** — the Rule-of-40 frontier and public-SaaS trajectory context.
7. **A recent public-SaaS 10-K** (Snowflake, Datadog, HubSpot) — an example of the three-statement presentation this module ultimately supports.
8. **Simon Benninga, *Financial Modeling*** — the deeper modelling-technique reference.
9. **EuSpRIG horror-stories archive** — real-world examples of the failure modes exercise 07 diagnoses.
10. **Vendor documentation for Causal, Runway, or Mosaic** — the modern FP&A-platform reference for chapter 8's graduation decision.

Only after this reading should you rely on secondary practitioner content (Substacks, LinkedIn essays, conference talks). Even then, read them as translations of the canon, not as sources of truth. Every specific benchmark citation in a board pack or a fundraise deck should trace to a tier-1, tier-2, or tier-4 source in this list, with the year and the segment named.
