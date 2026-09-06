# Resources — mod-102 Unit Economics & Cohort Financial Modeling

This is the reference stack behind every chapter and exercise in this module. Sources are grouped by tier of authority: read tier-1 primary sources and tier-2 authoritative benchmark providers first; treat tier-4 practitioner content as interpretive, not authoritative. Every benchmark citation in the chapters should be verifiable against something in this list.

Because published benchmark data shifts materially year to year (OpenView, Bessemer, and KeyBanc all refresh their surveys annually and the bands for a "healthy" burn multiple or "best-in-class" NRR move with the market), always cite the specific report year when quoting a band in a board pack or a fundraise deck. The `<!-- needs-research -->` markers in the chapters flag places where the current-year data should be re-verified.

## Tier 1 — Authoritative standards (GAAP, SEC)

The SaaS-metrics canon is a set of *industry practices layered on top of* the accounting standards; the standards themselves are the substrate against which every metric ultimately reconciles.

- **FASB Accounting Standards Codification** — [asc.fasb.org](https://asc.fasb.org/). Basic view is free; register for access.
  - **ASC Topic 606 — *Revenue from Contracts with Customers*** — the five-step model that governs the recognised-revenue numerator in the cohort table (chapter 4) and the P&L revenue line the gross-margin bridge (chapter 3) walks down from. The principal-vs.-agent guidance (ASC 606-10-55-36 to 55-40) governs whether a marketplace reports GMV or net take-rate as revenue (chapter 3).
  - **ASC Topic 340-40 — *Other Assets and Deferred Costs — Contracts with Customers*** — capitalisation and amortisation of contract-acquisition costs (sales commissions). Relevant to the "cash vs. amortised" CAC-loading choice discussed in chapter 1.
  - **ASC Topic 230 — *Statement of Cash Flows*** — presentation and classification of operating, investing, and financing cash flows. Relevant to the burn-multiple net-burn definition (chapter 6).
- **SEC Regulation S-X, Rule 5-03** — [ecfr.gov Title 17 Part 210](https://www.ecfr.gov/current/title-17/chapter-II/part-210). Prescribed public-company income-statement format. The regulation leaves the specific definition of "cost of revenue" to management judgement, which is why the SaaS-metrics canon and public-SaaS 10-K disclosure practice (below) become the reference for gross-margin decomposition.
- **SEC EDGAR** — [sec.gov/edgar](https://www.sec.gov/edgar). Every listed SaaS company's 10-K and 10-Q. The "Cost of revenue" footnote and the "Revenue" footnote in a 10-K are the primary sources for observing convergent industry practice on COGS classification, gross-margin decomposition, and NRR / GRR disclosure. Useful reference filings for gross-margin bridges: Snowflake, Datadog, CrowdStrike, HubSpot, Zoom, ServiceNow, Salesforce, MongoDB.

## Tier 2 — Authoritative benchmark providers

These are the four or five providers a CFO cites when a board pack or a fundraise deck references a benchmark band. Each publishes annually or continuously; check the current year at citation time.

- **OpenView SaaS Benchmarks** — [openviewpartners.com](https://openviewpartners.com/) → Insights → SaaS Benchmarks Report. Annual survey of hundreds of private SaaS companies, segmented by ARR band, motion (PLG vs. sales-led), and industry. Primary reference for CAC payback, burn multiple, and function-mix benchmarks (S&M / R&D / G&A as percent of revenue) by ARR stage. Chapters 1, 3, 5, 6 all cite it.
- **Bessemer Venture Partners State of the Cloud** — [bvp.com/atlas/state-of-the-cloud](https://www.bvp.com/atlas/state-of-the-cloud). Annual analysis with a strong late-stage and public-SaaS focus. Cash conversion score, "Best Cloud Companies" NRR data, and the Rule of 40 frontier analysis live here. Chapters 5 and 6 lean on it.
- **Bessemer Cloud Index (EMCLOUD)** — [cloudindex.bvp.com](https://cloudindex.bvp.com/). Real-time public-SaaS basket with revenue multiples, growth rates, gross margins, and Rule of 40 scores. Continuously updated. Use for the "what multiple does a Rule-of-40-of-X company trade at" reference in the valuation-narrative work of chapter 7 and [`mod-106`](../mod-106-startup-valuation-frameworks/).
- **Meritech Capital SaaS Comps** — [meritechcapital.com/saas-comps-table](https://www.meritechcapital.com/saas-comps-table). Current-quarter public-SaaS metrics with revenue-multiple correlations to Rule of 40, NRR, and growth rate. The reference table for revenue-multiple-based benchmarking against comparable public companies. Chapter 7 cites it directly.
- **KeyBanc Capital Markets Annual SaaS Survey** — Cover page and executive summary distributed via [key.com](https://www.key.com/businesses-institutions/industry-expertise/technology.html); the full report is typically distributed to SaaS-industry participants and via partner networks. Detailed unit-economics and expense-ratio benchmarks for private SaaS companies; complements the OpenView dataset with a somewhat different sample. Chapter 6 and exercise 06 reference it.
- **SaaStr Annual State of SaaS** — [saastr.com](https://www.saastr.com/). Practitioner-oriented benchmarks focused on the operator community; useful for CAC, sales-efficiency, and stage-transition data. Less rigorous than OpenView / Bessemer / KeyBanc but often the fastest-published take on emerging trends.

## Tier 3 — The SaaS-metrics canon

The essays and long-form pieces that established the conventional definitions of ARR, MRR, CAC, LTV, payback, magic number, NRR / GRR, and the associated benchmark ranges. Every practising SaaS CFO has read most of these; investors expect familiarity with the terminology.

- **David Skok — *SaaS Metrics 2.0*** — [forentrepreneurs.com/saas-metrics-2/](https://www.forentrepreneurs.com/saas-metrics-2/). The single most-cited SaaS-metrics essay. Defines bookings vs. billings vs. revenue, MRR / ARR movement, CAC, LTV, LTV:CAC ratio, months-to-recover-CAC (the payback formulation), and the magic number. Chapters 1, 2, 3, and 6 all sit on top of this vocabulary.
- **David Skok — *SaaS Metrics 2.0 — A Guide to Measuring and Improving What Matters*** — the same series, with several companion essays on churn, unit economics, and the cash-flow trough. All linked from the primary essay.
- **David Sacks — *The Burn Multiple*** — Craft Ventures Substack, [sacks.substack.com](https://sacks.substack.com/). The 2020 essay that formalised burn multiple as an efficiency metric. Chapter 6 cites the definition and the interpretive bands. The bands quoted in industry commentary derive from this essay; verify against the current version.
- **a16z — *16 Startup Metrics*** — [a16z.com/16-startup-metrics/](https://a16z.com/16-startup-metrics/). Definitional essay covering the first-order metrics.
- **a16z — *16 More Startup Metrics*** — [a16z.com/16-more-metrics-to-watch/](https://a16z.com/16-more-metrics-to-watch/). Companion essay covering the second-order metrics (gross vs. net revenue, GMV vs. revenue, bookings vs. billings, cohort-based measures).
- **a16z marketplace essays** — [a16z.com/marketplace-100/](https://a16z.com/marketplace-100/) and the *Marketplace 100* series. Reference for marketplace take-rate bands and GMV-vs.-revenue framing (chapter 3).
- **Bill Gurley — *A Rake Too Far — Optimal Platform Pricing Strategy*** — [abovethecrowd.com](https://abovethecrowd.com/2013/04/18/a-rake-too-far-optimal-platformpricing-strategy/). The canonical essay on marketplace take-rate economics and the trade-off between take-rate and platform growth. Chapter 3 cites the 20% take-rate threshold discussion.
- **Tomasz Tunguz** — [tomtunguz.com](https://tomtunguz.com/). Long-running blog by the Redpoint partner. Deep archive of essays on cohort analysis, CAC, LTV, sales efficiency, NRR, and stage-specific benchmarks.

## Tier 4 — Venture-return and cost-of-capital references

For chapter 2's discount-rate defence and for the general venture-required-return framing throughout the module.

- **Aswath Damodaran — private-company valuation resources** — [pages.stern.nyu.edu/~adamodar/](https://pages.stern.nyu.edu/~adamodar/). NYU Stern's Damodaran maintains the most comprehensive academic-and-practitioner reference on cost of equity, cost of capital, and the illiquidity, size, and stage discounts that apply to private-company valuations. Read *Investment Valuation* (the textbook) for the theoretical grounding; the online datasets for current-year risk premia, industry betas, and country-risk premia.
  - **Damodaran — *Valuing Young, Start-up and Growth Companies*** — a specific working paper on the venture-stage adjustments. Available on the pages.stern site under "Papers."
  - **Damodaran — annual updates to the equity risk premium and industry betas** — refreshed each January; the current-year numbers feed any DCF-anchored LTV computation.
- **Scott Kupor — *Secrets of Sand Hill Road: Venture Capital and How to Get It*** — Portfolio, 2019. Written by a16z's managing partner. The inside-the-VC-firm view of how required returns are constructed from LP-return expectations, fund-life mechanics, and the venture-portfolio failure-rate math. Chapter 2 cites the required-IRR ranges by stage.
- **Brad Feld and Jason Mendelson — *Venture Deals: Be Smarter Than Your Lawyer and Venture Capitalist*** — Wiley, multiple editions (current is the 5th or later). The standard practitioner reference for venture-deal mechanics; the venture-return-distribution framing in chapter 2 draws on the "how VCs think about returns" chapters.
- **CFA Institute — *Private Equity and Venture Capital* readings** — part of the CFA Program curriculum, level II and III. Publicly available summaries at [cfainstitute.org](https://www.cfainstitute.org/). Rigorous treatment of private-equity return distributions, IRR construction, and the relationship between fund-level target IRRs and portfolio-company hurdle rates.
- **Cambridge Associates — Private Investment Benchmarks** — [cambridgeassociates.com](https://www.cambridgeassociates.com/) → Insights → Benchmarks. Quarterly published benchmark returns for venture, growth-equity, and private-equity funds. Reference for what actual venture returns have been in recent vintages, which is the empirical anchor for the required-IRR bands used in LTV discounting.
- **Preqin — Private Capital reports** — [preqin.com](https://www.preqin.com/). Subscription data provider covering private-capital fund performance, deal flow, and LP allocations. Used by CFOs and investors as a second source alongside Cambridge Associates for return-benchmark verification.

## Tier 5 — Cohort-analysis and BI tools

Referenced in chapter 4 for the cohort-table build. All are alternatives to a well-structured spreadsheet once cohort volume exceeds spreadsheet-manageable size.

- **ChartMogul** — [chartmogul.com](https://chartmogul.com/). Purpose-built SaaS-analytics tool with cohort, MRR-movement, and retention primitives. Integrates directly with common billing systems (Stripe, Chargebee, Recurly, Zuora).
- **Baremetrics** — [baremetrics.com](https://baremetrics.com/). Similar space to ChartMogul; SaaS-metrics focused with cohort and retention analysis.
- **Mixpanel** — [mixpanel.com](https://mixpanel.com/). Product-analytics tool with cohort primitives that extend to funnel and behavioural cohorts, not just billing cohorts.
- **Amplitude** — [amplitude.com](https://amplitude.com/). Product-analytics competitor to Mixpanel with equivalent cohort primitives.
- **Cube** — [cube.dev](https://cube.dev/). Open-source headless BI / semantic-layer tool useful for cohort tables built on top of a data warehouse.
- **Looker** — [cloud.google.com/looker](https://cloud.google.com/looker). BI tool (owned by Google Cloud) with LookML modelling; supports cohort tables via period-over-period and cohort-relative dimensions.
- **ThoughtSpot** — [thoughtspot.com](https://thoughtspot.com/). Search-driven BI tool with cohort and retention templates.

## Tier 6 — Related standards and cross-track references

Context references that intersect with this module but are not primary citations for it.

- **IFRS 15 — *Revenue from Contracts with Customers*** — the IASB standard converged with ASC 606. Summary at [ifrs.org](https://www.ifrs.org/issued-standards/list-of-standards/ifrs-15-revenue-from-contracts-with-customers/). Relevant for internationally-operating companies whose non-US subsidiaries file under IFRS.
- **Big Four revenue-recognition guides** — Deloitte, PwC, EY, KPMG each publish interpretive guides on ASC 606 / IFRS 15. Full list at [`mod-101` resources](../mod-101-startup-accounting-foundations/resources.md). Referenced here for the gross-margin bridge's revenue starting point (chapter 3).
- **Sequoia Capital — pitch-deck templates and guidance** — [sequoiacap.com](https://www.sequoiacap.com/article/writing-a-business-plan/) → *Writing a Business Plan*. The Sequoia deck template is one of the two canonical patterns; the "unit economics" slide format in chapter 7 follows this convention.
- **Y Combinator — startup essays and pitch guidance** — [ycombinator.com/library](https://www.ycombinator.com/library). The YC deck pattern is the second canonical convention; the compressed early-stage version of the unit-economics slide.
- **DocSend — *Startup Pitch Deck Benchmarks*** — [docsend.com](https://www.docsend.com/) publishes annual analysis of investor engagement with pitch decks: which slides investors spend the most time on, which slides get skipped, and how decks that raise successfully differ from ones that don't. Chapter 7 references DocSend tracking for deck-iteration methodology.

## Cross-references to other modules in this track

The module's outputs feed forward through the CFO track. Where the outputs land:

- [`mod-101 — Startup Accounting Foundations`](../mod-101-startup-accounting-foundations/) — accrual accounting, ASC 606, deferred revenue. Prerequisite; the accrual P&L that chapter 3's gross-margin bridge starts from is defined there.
- [`mod-103 — Three-Statement Model and Driver-Based Forecasting`](../mod-103-three-statement-model-and-driver-based-forecasting/) — the cohort retention curve from chapter 4 becomes a driver in the forecast model.
- [`mod-106 — Startup Valuation Frameworks`](../mod-106-startup-valuation-frameworks/) — the Rule of 40 and NRR values from chapters 5 and 6, cross-referenced against the Bessemer / Meritech public-comp data, bound the revenue multiple the company can support.
- [`mod-107 — Fundraising Strategy and Investor Targeting`](../mod-107-fundraising-strategy-and-investor-targeting/) — the unit-economics pack this module produces becomes the data-room artefact and the unit-economics slide sequence of the fundraise deck.
- [`mod-108 — Term Sheets and Preferred Stock Economics`](../mod-108-term-sheets-and-preferred-stock-economics/) — the valuation range implied by the pack is the anchor for term-sheet negotiation.
- [`mod-109 — Runway Management and Bridge Financing`](../mod-109-runway-management-and-bridge-financing/) — the burn-multiple diagnostic from chapter 6 is one input to the runway-and-bridge decision framework.
- [`mod-110 — Board and Investor Governance for the CFO`](../mod-110-board-and-investor-governance-for-the-cfo/) — the KPI dashboard in a board pack is sourced from the pack this module authors.

Cross-track references:

- [`startup-product-gtm-curriculum`](https://github.com/ai-startup-curriculum/startup-product-gtm-curriculum) — the GTM-operator view of the same CAC / LTV / payback / magic-number metrics. Chapter 7 draws the ownership boundary.
- [`startup-foundations`](https://github.com/ai-startup-curriculum/startup-foundations) — the level-10 founder-numbers layer (runway, burn, growth rate, default-alive vs. default-dead, North-Star metric). Chapter 7 places this module above it.

## Reading order for this module

If you are new to the SaaS-metrics canon, read in this order before working through the exercises:

1. Skok, *SaaS Metrics 2.0* — the vocabulary.
2. a16z, *16 Startup Metrics* and *16 More Startup Metrics* — the definitional companion pieces.
3. Sacks, *The Burn Multiple* — the capital-efficiency framing.
4. Bessemer, *State of the Cloud* (current-year) — the benchmark bands.
5. OpenView, *SaaS Benchmarks* (current-year) — the private-company benchmark bands segmented by ARR stage.
6. Meritech, *SaaS Comps* — the public-comp reference against which the pack ultimately maps to a valuation.
7. One recent public-SaaS 10-K (e.g., Snowflake, Datadog, HubSpot) — the "Cost of revenue" and "Revenue" footnotes as an example of the disclosure this module's pack ultimately supports.
8. Damodaran, *Valuing Young, Start-up and Growth Companies* — the discount-rate defence for cohort LTV.
9. Kupor, *Secrets of Sand Hill Road* and Feld & Mendelson, *Venture Deals* — the venture-return context.

Only after this canon should you rely on secondary practitioner content (Substacks, LinkedIn essays, conference talks). Even then, read them as translations of the canon, not as sources of truth. Every specific benchmark citation in a board pack or a fundraise deck should trace to a tier-1 or tier-2 source in this list, with the year and the segment named.
