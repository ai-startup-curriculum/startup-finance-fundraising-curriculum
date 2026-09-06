# Resources — mod-106 Startup Valuation Frameworks

This is the reference stack behind every chapter and exercise in this module. Sources are grouped by tier of authority: read the tier-1 primary and academic sources first; treat tier-5 practitioner content as translation rather than authority. Every "the multiple is X" or "the market compressed by Y" claim in the chapters should trace to a specific report or dataset in this list at a specific vintage.

Public-comp multiples move every trading day. Median pre-moneys, dilution medians, and term-sheet-feature frequencies move every quarter. Whenever a chapter cites a specific number, verify against the current issue of the underlying source before relying on it in a valuation memo or board pack. The `<!-- needs-research -->` markers in the chapters flag places where current-year data should be re-verified.

## Tier 1 — Foundational academic and practitioner works

The load-bearing references behind the valuation frameworks. Read Damodaran first; almost everything downstream traces back to his textbook and NYU Stern datasets.

### Aswath Damodaran (NYU Stern) — the standing valuation reference

- **Aswath Damodaran — *Investment Valuation: Tools and Techniques for Determining the Value of Any Asset*** — Wiley, 3rd ed. (2012, still the current edition). The canonical textbook. The DCF chapters (chapter 5 of this module) are drawn from this. The illiquidity-discount chapters (chapter 3 of this module) are drawn from this.
- **Aswath Damodaran — *The Dark Side of Valuation: Valuing Young, Distressed, and Complex Businesses*** — Pearson FT Press, 2nd ed. (2010). The reference on why early-stage valuation defies standard DCF methodology and what to do about it. Directly relevant to chapters 1 and 5.
- **Aswath Damodaran — NYU Stern page — [pages.stern.nyu.edu/~adamodar](https://pages.stern.nyu.edu/~adamodar/)**. Free companion resources including data downloads updated annually.
  - **Damodaran industry data** — [pages.stern.nyu.edu/~adamodar/New_Home_Page/data.html](https://pages.stern.nyu.edu/~adamodar/New_Home_Page/data.html). Free annual updates of industry-average multiples, cost of capital, growth rates, and margins by sector (US, Global, Emerging Markets, Europe, Japan, China). Cross-reference for the SaaS / software multiples in chapters 3-4.
  - **Damodaran illiquidity / private-company discount analysis** — the specific downloadable spreadsheets and blog posts on illiquidity discounts. Relevant to the private-market discount in chapter 3.
  - **Damodaran blog — *Musings on Markets*** — [aswathdamodaran.blogspot.com](https://aswathdamodaran.blogspot.com/). Continuous commentary on valuation topics including specific writeups on public-comp multiples, market cycles, and individual company valuations.
  - **Damodaran YouTube lectures** — full NYU Stern valuation course lectures available free. The DCF lectures and the multiples lectures cover the mechanics behind chapters 3-5.
- **Aswath Damodaran — *Narrative and Numbers: The Value of Stories in Business*** — Columbia Business School Press, 2017. The reference on binding a valuation to a defensible narrative — directly relevant to chapter 8's negotiation posture.

### Academic textbooks — venture and private-company valuation

- **Andrew Metrick and Ayako Yasuda — *Venture Capital and the Finance of Innovation*** — Wiley, 3rd ed. (2021). The venture-side academic reference. The VC method (chapter 2) and the target-return math are covered rigorously with worked examples. The dilution ladder in chapter 2's back-solve traces to this textbook.
- **Josh Lerner and Ann Leamon — *Venture Capital, Private Equity, and the Financing of Entrepreneurship*** — Wiley, 2nd ed. (2023). Harvard Business School textbook covering the broader venture-financing landscape; the chapters on staging, deal structuring, and exit valuation are the academic backbone for how VCs price a round.
- **Bob Zider — "*How Venture Capital Works*"** — Harvard Business Review, 1998. Classic HBR article; still the clearest short exposition of venture partnership economics and how the fund-level return math shapes deal-level pricing. Cross-reference chapter 2.
- **Ronald Gilson — "Engineering a Venture Capital Market: Lessons from the American Experience"** — Stanford Law Review, 2003. Academic reference on how the US venture legal-financial infrastructure evolved; useful context on the comp-set and market-conditions data.
- **Steven Kaplan and Per Strömberg — "Financial Contracting Theory Meets the Real World: An Empirical Analysis of Venture Capital Contracts"** — Review of Economic Studies, 2003. The classic academic paper on how VCs structure priced-round terms; the source data on liquidation-preference and anti-dilution incidence is a decade-plus old but still cited.
- **AICPA — *Valuation of Privately-Held-Company Equity Securities Issued as Compensation* (Practice Aid)** — AICPA (American Institute of Certified Public Accountants), most recent revision 2013 with subsequent supplements. Practitioner-facing guide to private-company valuation methodology, including calibration to public comps and the illiquidity-discount discussion. Also the reference behind 409A common-stock valuation methodology (crossref [mod-104](../mod-104-cap-tables-and-equity-compensation/) chapter 5).

## Tier 2 — Public-comp datasets

The specific publicly-published comp tables and indexes that anchor Series-A / B / C / later valuation. All of these publish free public data at the URLs below; the constituent lists and per-constituent multiples are the source data behind chapters 3-4.

### Meritech and Bessemer — the SaaS-comp anchors

- **Meritech Capital Partners — *Enterprise SaaS Comparables*** — [meritechcapital.com/public-comparables/enterprise-saas](https://www.meritechcapital.com/public-comparables/enterprise-saas). Live table of publicly-traded enterprise SaaS companies with EV, LTM revenue, NTM revenue, EV/LTM, EV/NTM, NTM growth, gross margin, FCF margin, Rule of 40. Updated regularly. Includes high-growth and cloud subsets. Chapters 3-4 anchor to this table.
- **Meritech — related public tables** — same landing page includes public comparables for other software subsectors and periodic memos on SaaS valuation dynamics.
- **Bessemer Venture Partners — *BVP Nasdaq Emerging Cloud Index*** — [cloudindex.bvp.com](https://cloudindex.bvp.com/). Live market-cap-weighted index of publicly-traded cloud companies with historical time series, median EV/NTM revenue for the full index and high-growth subsets, and constituent-level data. Chapter 3's Bessemer discussion anchors here. The historical time series is essential for the market-cycle placement in chapter 4.
- **Bessemer Venture Partners — *State of the Cloud* annual report** — [bvp.com/atlas/state-of-the-cloud](https://www.bvp.com/atlas/state-of-the-cloud). Bessemer's annual synthesis of cloud-market data, including per-year median multiples, growth rates, and market-cycle commentary.
- **Bessemer — *Cloud 100* list (with Forbes)** — annual ranking of top private cloud companies with commentary on valuation, growth, and market position. Useful as a private-market comp reference alongside the public comps.

### Public-market databases — subscription and open

- **S&P Capital IQ** — [capitaliq.spglobal.com](https://www.capitaliq.spglobal.com/). Subscription. The industry-standard equity-research database for public-comp data with the full set of multiples, financial-statement history, and consensus-forecast data. Most CFOs at growth-stage companies have access via a banking / advisor relationship.
- **FactSet** — [factset.com](https://www.factset.com/). Subscription. Competitor to S&P Capital IQ with equivalent public-comp data.
- **Refinitiv (LSEG Eikon)** — [lseg.com/en/data-analytics](https://www.lseg.com/en/data-analytics). Subscription.
- **PitchBook — Software Analytics** — [pitchbook.com](https://pitchbook.com/). Subscription. Covers both public and private software analytics; the private-round comp data is unique to PitchBook.
- **Damodaran industry-average data** — [pages.stern.nyu.edu/~adamodar/New_Home_Page/data.html](https://pages.stern.nyu.edu/~adamodar/New_Home_Page/data.html). Free annual updates. Broader industry coverage than Meritech / Bessemer but less software-specific detail.
- **Damodaran archived data** — [pages.stern.nyu.edu/~adamodar/New_Home_Page/dataarchived.html](https://pages.stern.nyu.edu/~adamodar/New_Home_Page/dataarchived.html). Prior-year snapshots; useful for market-cycle placement work.
- **Yahoo Finance** — [finance.yahoo.com](https://finance.yahoo.com/). Free. Point-in-time market data and consensus estimates for individual constituents; adequate for building a small hand-picked comp set if the Meritech / Bessemer universe doesn't cover the target's subsector.
- **SEC EDGAR** — [sec.gov/edgar](https://www.sec.gov/edgar). Free. 10-K, 10-Q, S-1, and 8-K filings for public-comp constituents. Primary source for the underlying financial-statement data and disclosed metrics (ARR, NRR, sales efficiency) not always in the aggregated databases.

### Illiquidity-discount and private-company discount references

- **Kroll (formerly Duff & Phelps) — *Valuation Handbook — U.S. Guide to Cost of Capital*** — Kroll, updated annually. Subscription. The industry-standard reference for cost-of-capital data, including size premiums and industry premiums used in DCF work (chapter 5). Also covers illiquidity-discount methodology.
- **Kroll (formerly Duff & Phelps) — *Valuation Handbook — International Guide to Cost of Capital*** — non-US analogue.
- **Business Valuation Resources (BVR) — *Discount for Lack of Marketability (DLOM) Study*** — [bvresources.com](https://www.bvresources.com/). Periodic empirical studies of illiquidity discounts observed in restricted-stock transactions.
- **Pluris DLOM Database** — [pluris.com](https://www.pluris.com/). Subscription database of DLOM studies drawn from private-company transactions.
- **AICPA Practice Aid** (see tier 1). Includes the illiquidity discussion in the private-company valuation context.

## Tier 3 — Quarterly deal-terms and market-conditions reports

The current-market context for a specific fundraise. Read all four (Fenwick, Wilson Sonsini, PitchBook-NVCA, Carta) every quarter during an active raise; read at least four trailing quarters for trend context. Each has a specific sample bias — triangulation is required.

### The four quarterly reports

- **Fenwick & West — *Silicon Valley Venture Survey*** — [fenwick.com/insights](https://www.fenwick.com/insights) (search "Silicon Valley Venture Survey" if the URL structure changes). Quarterly since 2002. Silicon Valley scope. Strongest on term-sheet-feature frequencies (participating preferred, anti-dilution, pay-to-play, redemption) and the Fenwick Barometer (a single-number quarterly direction indicator). Chapter 6 anchor.
- **Wilson Sonsini Goodrich & Rosati — *Entrepreneurs Report*** — [wsgr.com/en/insights](https://www.wsgr.com/en/insights.html) (search "Entrepreneurs Report"). Quarterly. National US scope. Strongest on seed / pre-seed detail, bridge-round tracking, convertible-instrument cuts (SAFE and note cap-and-discount ranges), and term-sheet features complementing Fenwick. Note that WSGR is the historical brand ("Wilson Sonsini Goodrich & Rosati"); current branding is "Wilson Sonsini."
- **PitchBook-NVCA — *Venture Monitor*** — [nvca.org/research/pitchbook-nvca-venture-monitor](https://nvca.org/research/pitchbook-nvca-venture-monitor/). Quarterly and annual, jointly published by PitchBook and NVCA. National US scope with regional and sector cuts. Strongest on macro market data (deal count, capital deployed, LP-side fundraising), median deal size and pre-money by stage, time between rounds, and exit activity. Full report requires PitchBook access; the summary release and top-level charts are free.
- **Carta — *State of Private Markets*** — [carta.com/data](https://carta.com/data). Periodic (typically quarterly with retrospective annual reviews). Drawn from Carta's platform data (tens of thousands of US venture-backed cap tables). Strongest on cap-table mechanics — median dilution per round, ESOP sizing, secondary-transaction volume, down-round frequency, bridge-round frequency, founder ownership evolution. Chapter 7 anchor.

### Complementary quarterly reports

- **Cooley GO — *Venture Financing Report*** — [cooleygo.com/venture-financing-report](https://www.cooleygo.com/venture-financing-report/). Quarterly practitioner report similar to Fenwick / Wilson Sonsini with a Cooley-representation-based sample. Useful as a fifth cross-check.
- **Aumni (JPMorgan) — *Venture Beacon*** — [aumni.fund](https://www.aumni.fund/). Data-driven venture-terms reporting with strong term-sheet-feature coverage.
- **AngelList — *State of Startups* and periodic data essays** — [angellist.com/blog](https://www.angellist.com/blog/). Periodic data updates from AngelList's platform data. Complements Carta for early-stage / SAFE-heavy data.
- **CB Insights — *State of Venture*** — [cbinsights.com/research](https://www.cbinsights.com/research). Quarterly and annual. Subscription (some free excerpts). Global scope, competitor to PitchBook.
- **Silicon Valley Bank (SVB) — *State of the Markets*** — [svb.com/trends-insights](https://www.svb.com/trends-insights/). Periodic reports on venture-market activity from SVB's client dataset.
- **First Republic (now JPMorgan) — periodic venture-market reports** — historically SVB-alternative source; verify current availability.

### Regional and international market data

- **Angel Capital Association (ACA) — *HALO Report*** — [angelcapitalassociation.org](https://www.angelcapitalassociation.org/). Periodic report on US angel-investment activity, including regional pre-money medians for angel and pre-seed rounds. Directly relevant to the Payne Scorecard baseline in chapter 1 / exercise 1.
- **European venture reports** — Atomico *State of European Tech* ([stateofeuropeantech.com](https://www.stateofeuropeantech.com/)) and Dealroom *European Venture Capital* ([dealroom.co](https://dealroom.co/)) for European fundraising context. Note that the module's frameworks are US-anchored; European market conventions differ.
- **PitchBook NVCA regional cuts** — the PitchBook-NVCA report includes regional cuts for California / Northeast / South / Midwest.
- **PitchBook Global Venture Monitor** — separate non-US report.

## Tier 4 — Anchor-method primary sources

The specific documentation behind the Berkus, Payne, and risk-factor methods in chapter 1.

- **Dave Berkus — *Berkonomics*** — [berkonomics.com](https://berkonomics.com/). Dave Berkus's own blog. The primary source for the Berkus Method, its origin, subsequent inflation-adjustments, and Berkus's own commentary on how the method should be applied.
- **Dave Berkus — *Basic Berkus Method*** posts — search berkonomics.com for the "Berkus Method" tag. Includes the classic $500K-per-component / $2.5M-ceiling formulation and the later inflation-adjusted variants.
- **Bill Payne — *billpayne.com*** — [billpayne.com](http://billpayne.com/). Bill Payne's own site with his writings on the Scorecard Method, the Payne factor weights, and companion methods.
- **Bill Payne — *The Definitive Guide to Raising Money from Angels*** — Bill Payne, 2011. The primary printed source for the Payne Scorecard Method, the risk-factor summation method (attributed to the Ohio TechAngel Fund), and other angel-round valuation methods.
- **Angel Capital Association (ACA) — practitioner materials** — [angelcapitalassociation.org](https://www.angelcapitalassociation.org/). Educational materials for angel groups including the Kauffman Foundation-supported curriculum that incorporated the Payne Scorecard.
- **Ohio TechAngel Fund materials** — the historical origin of the 12-factor risk-factor summation method as cited by Payne. Detail is primarily available through Payne's writing rather than directly from OTAF.
- **Kauffman Foundation — angel-investor educational materials** — [kauffman.org](https://www.kauffman.org/). Foundation-funded materials that codified the Payne Scorecard as part of the angel-group training curriculum in the mid-2000s.

## Tier 5 — Practitioner canon

The essays, blogs, guides, and books that translate the tier-1 to tier-3 references into founder- and CFO-actionable frameworks.

### VC-side canon

- **Brad Feld — *Feld Thoughts*** — [feld.com](https://feld.com/). Foundry Group partner. The *Term Sheet Series* (2005-2007, still linked from the site) is the founder's-side canonical reference on term-sheet mechanics; the valuation-related essays anchor to Rule of 40 (which Feld helped popularise).
- **Brad Feld — *Ask the VC*** — [askthevc.com](https://askthevc.com/). Q&A-style companion site. Historical archive relevant to valuation and term-sheet questions.
- **Mark Suster — *Both Sides of the Table*** — [bothsidesofthetable.com](https://bothsidesofthetable.com/). Upfront Ventures partner. Regular commentary on fund math, portfolio construction, and how VCs think about valuation at seed and Series-A.
- **Fred Wilson — *AVC*** — [avc.com](https://avc.com/). Union Square Ventures partner. Deep archive on venture-round pricing dynamics, exit expectations, and market cycles.
- **Bill Gurley — *Above the Crowd*** — [abovethecrowd.com](https://abovethecrowd.com/). Benchmark partner. Long-form essays on public-market valuation dynamics and their effect on private-round pricing. The 2015 essay *Investors Beware: Today's $100M+ Late-Stage Private Rounds Are Very Different from an IPO* is the reference on how private-round pricing can decouple from market discipline.
- **Scott Kupor — *Secrets of Sand Hill Road: Venture Capital and How to Get It*** — Portfolio, 2019. Andreessen Horowitz managing partner. Covers fund economics, VC decision frameworks, and term-sheet negotiation.
- **Chris Sacca and other early-stage investor essays** — Lowercase Capital and successor commentary on seed-round pricing.

### SaaS-community canon

- **Bessemer Venture Partners — *State of the Cloud* and *Bessemer's Ten Laws of Cloud Computing*** — [bvp.com/atlas](https://www.bvp.com/atlas). Bessemer's practitioner-oriented essays on SaaS metrics, Rule of 40, growth-adjusted multiples, and market-cycle commentary. The "Cloud 100" annual list and companion essays are directly relevant to chapters 3-4.
- **SaaStr (Jason Lemkin) — *SaaStr Blog* and podcast** — [saastr.com](https://www.saastr.com/). SaaS-community reference. Frequent posts on SaaS metrics, benchmarks, and Rule of 40.
- **OpenView Venture Partners — *SaaS Benchmarks Report*** — [openviewpartners.com](https://openviewpartners.com/). Periodic report on SaaS metrics benchmarks including Rule of 40, sales efficiency, and CAC payback. Companion to Meritech / Bessemer for the private-company benchmark side.
- **ChartMogul — *SaaS Metrics Reports*** — [chartmogul.com](https://chartmogul.com/). Periodic reports drawn from ChartMogul's subscription-analytics platform data on SaaS growth and retention benchmarks.
- **Redpoint Ventures — *Tomasz Tunguz's blog*** — [tomtunguz.com](https://tomtunguz.com/). Tunguz's essays on SaaS growth, market cycles, and valuation multiples.
- **David Skok — *For Entrepreneurs*** — [forentrepreneurs.com](https://www.forentrepreneurs.com/). Matrix Partners MD. Classic reference on SaaS metrics (LTV/CAC, months-to-recover-CAC, cohort analysis) that underpin growth-adjusted multiple work in chapter 4.

### Books

- **Brad Feld and Jason Mendelson — *Venture Deals: Be Smarter Than Your Lawyer and Venture Capitalist*** — Wiley, 5th ed. (2023). Chapter on valuation and pre-money mechanics is the founder-side canonical framing.
- **Alexander Osterwalder et al. — *Business Model Generation*** — Wiley, 2010. Referenced across the track for business-model framing; not directly a valuation text but useful context.
- **Chris Mercer — *Business Valuation: An Integrated Theory*** — Wiley, 3rd ed. Reference on private-company valuation methodology including illiquidity-discount theory and control-premium mechanics.
- **Shannon Pratt — *Valuing a Business: The Analysis and Appraisal of Closely Held Companies*** — McGraw-Hill, 6th ed. The private-company-valuation reference used by professional appraisers; substantial coverage of the DLOM literature relevant to the chapter 3 private-market discount.

### Podcasts and video

- **20VC with Harry Stebbings** — [20vc.com](https://www.20vc.com/). Venture-industry interviews; frequent deep-dives on fund economics and portfolio construction relevant to the VC method in chapter 2.
- **This Week in Startups (Jason Calacanis)** — [thisweekinstartups.com](https://thisweekinstartups.com/). Founder- and investor-facing interviews.
- **The Twenty Minute VC** — Harry Stebbings's original podcast (now folded into 20VC).
- **Acquired** — [acquired.fm](https://www.acquired.fm/). Deep-dive company narratives including fundraise-and-exit history for named companies.
- **Aswath Damodaran — YouTube lectures** — full NYU Stern valuation course lectures free on YouTube.

## Tier 6 — Cap-table platforms and modelling tools

The systems of record and modelling tools that operationalise the valuation frameworks in a live cap-table context.

- **Carta** — [carta.com](https://carta.com/). Cap-table platform with built-in round-modelling, priced-round conversion, and valuation-scenario tools. The State of Private Markets report data comes from this platform.
- **Pulley** — [pulley.com](https://pulley.com/). Cap-table and round-modelling platform with focus on early-stage.
- **LTSE Equity** — [ltse.com/equity](https://ltse.com/equity). Cap-table and scenario-modelling platform.
- **Foundersuite / Founders Circle — DIY cap-table and valuation-modelling templates** — [foundersuite.com](https://foundersuite.com/) / [founderscircle.com](https://founderscircle.com/).
- **Cooley GO — *Convertible Note and SAFE Calculators*** — [cooleygo.com](https://www.cooleygo.com/). Web calculators for SAFE and note conversion; useful when checking the pre-money / post-money arithmetic in a valuation model.
- **Kruze Consulting — SaaS financial models and valuation calculators** — [kruzeconsulting.com](https://kruzeconsulting.com/). Free downloadable models for early-stage financial planning and SAFE / priced-round modelling.

## Tier 7 — Cross-references to other modules in this track

- [`mod-101` — Startup Accounting Foundations](../mod-101-startup-accounting-foundations/) — the GAAP revenue-recognition base that determines the specific "revenue" the multiplier is applied to (chapter 3's ARR-vs.-revenue-vs.-bookings-vs.-billings distinction).
- [`mod-102` — Unit Economics and Cohort Financial Modelling](../mod-102-unit-economics-and-cohort-financial-modelling/) — the cohort model that supports the NTM revenue projection and NRR / GRR anchor for the multiples framework (chapter 3).
- [`mod-103` — Three-Statement Model and Driver-Based Forecasting](../mod-103-three-statement-model-and-driver-based-forecasting/) — the driver-based model that produces the NTM revenue, FCF margin, and Rule of 40 inputs for chapters 3-5.
- [`mod-104` — Cap Tables and Equity Compensation](../mod-104-cap-tables-and-equity-compensation/) — the pre-money / post-money / option-pool arithmetic every valuation resolves into (mod-104 chapter 2). Chapter 5 (409A methodology) is adjacent to but distinct from this module's fundraising-valuation work.
- [`mod-105` — Convertible Instruments](../mod-105-convertible-instruments/) — the valuation cap on outstanding SAFEs is a de facto ceiling on the priced-round pre-money; the SAFE-overhang mechanic (mod-105 chapter 7) affects the priced-round dilution calculation in chapter 2.
- [`mod-107` — Fundraising Strategy and Investor Targeting](../mod-107-fundraising-strategy-and-investor-targeting/) — the target-investor-list construction that consumes the VC-method calculation in chapter 2 and the market-conditions memo in chapters 6-7.
- [`mod-108` — Term Sheets and Preferred Stock Economics](../mod-108-term-sheets-and-preferred-stock-economics/) — the term-sheet economics that follow the pre-money the valuation frameworks price. The boundary in chapter 8 handoff.
- [`mod-109` — Runway Management and Bridge Financing](../mod-109-runway-management-and-bridge-financing/) — down-round and bridge-round mechanics that follow from a market-clearing pre-money below the founder's target.
- [`mod-110` — Board and Investor Governance for the CFO](../mod-110-board-and-investor-governance-for-the-cfo/) — the board-consent mechanics on priced-round issuance and the reporting cadence on valuation and market-conditions memos.
- [`mod-111` — Finance Operations, Controls, and Team Design](../mod-111-finance-operations-controls-and-team-design/) — the valuation-memo audit trail and the pre-negotiation checklist discipline as a controls artefact.
- [`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum) — transaction valuation for M&A / IPO / secondary sale, with earn-out, escrow, and structuring mechanics. The boundary in chapter 8.

## Reading order for this module

If you are new to CFO-grade valuation work, read in this order before working through the exercises:

1. **Aswath Damodaran — *Investment Valuation* (chapters on multiples and on early-stage / private-company valuation)** — the foundational reference. Read the DCF chapters even if the DCF will not be your primary framework (chapter 5).
2. **Aswath Damodaran — *The Dark Side of Valuation* (chapters on young / distressed companies)** — the early-stage-specific reference. Directly relevant to chapters 1 and 5.
3. **Bill Payne — *The Definitive Guide to Raising Money from Angels*** — the primary source for the Payne Scorecard and risk-factor summation methods (chapter 1).
4. **Dave Berkus's *Berkonomics* posts on the Berkus Method** — the primary source for the Berkus Method (chapter 1).
5. **Andrew Metrick and Ayako Yasuda — *Venture Capital and the Finance of Innovation* (chapters on the VC method and portfolio construction)** — the academic reference for chapter 2.
6. **Meritech Capital — *Enterprise SaaS Comparables* (the current-day table)** and **Bessemer Cloud Index (the current-day dashboard and constituent list)** — read the constituent-level data end-to-end. These are the anchor references for chapters 3-4.
7. **Bessemer *State of the Cloud* annual report** — synthesis of the current-year cloud-market data.
8. **The current-quarter Fenwick Silicon Valley Venture Survey, Wilson Sonsini Entrepreneurs Report, PitchBook-NVCA Venture Monitor, and Carta State of Private Markets** — the current-market context. Read all four before starting any priced-round fundraise process.
9. **Brad Feld and Jason Mendelson — *Venture Deals* (the pre-money / post-money and term-sheet chapters)** — the founder-side canonical framing.
10. **Bill Gurley — *Above the Crowd* essays on public-vs.-private-round pricing dynamics** — the practitioner reference on how public and private multiples decouple in certain market cycles.

Only after this reading should you rely on secondary practitioner content (Substacks, LinkedIn essays, conference talks). Even then, read them as translations of the canon, not as sources of truth. Every specific multiple, discount, or benchmark cited in a valuation memo should trace to a tier-1 to tier-3 source in this list, with the specific issue, timestamp, or page number named.
