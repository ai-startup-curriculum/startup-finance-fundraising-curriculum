# Resources — mod-104 Cap Tables & Equity Compensation

This is the reference stack behind every chapter and exercise in this module. Sources are grouped by tier of authority: read tier-1 statutory and regulatory sources first; treat tier-6 practitioner content and vendor documentation as interpretive, not authoritative. Every "the rule is X" claim in the chapters should be verifiable against something in this list; every benchmark citation should name the specific quarterly report and edition.

Because equity-comp regulation, benchmark data, and market convention all move — the SEC amended Rule 701's disclosure threshold from $5M to $10M in 2018, the Section 1202 QSBS parameters have periodic legislative proposals, the AICPA Practice Aid has been updated several times, Carta's and Pave's benchmark bands shift each quarter — always cite the specific edition or effective date when quoting a rule or a band. The `<!-- needs-research -->` markers in the chapters flag places where current-year data should be re-verified.

## Tier 1 — Statutory and regulatory primary sources

The federal tax and securities-law regimes that govern every mechanic in this module. Read the statute and the regulation, not just a practitioner summary — the practitioners are all interpreting these primary texts.

### Federal tax — the equity-comp regime

- **Internal Revenue Code (Title 26, US Code)** — [uscode.house.gov](https://uscode.house.gov/browse/prelim@title26&edition=prelim). The statute itself. Read alongside the Treasury Regulations for the operative rules.
  - **IRC §83 — *Property Transferred in Connection with Performance of Services*** — the governing statute for restricted stock, early-exercised options, and the 83(b) election (chapter 7). Section 83(b) is the specific election-to-be-taxed-at-grant sub-section.
  - **IRC §421-424 — *Statutory Options*** — the incentive-stock-option (ISO) regime. §422 defines the ISO itself; §421 covers the timing-of-income-recognition rule; §423 covers Employee Stock Purchase Plans (ESPPs); §424 covers modifications and disqualifying dispositions.
  - **IRC §409A — *Inclusion in Gross Income of Deferred Compensation Under Nonqualified Deferred Compensation Plans*** — the deferred-compensation regime that governs option strike-price setting (chapter 5). Enacted as part of the American Jobs Creation Act of 2004.
  - **IRC §1202 — *Partial Exclusion for Gain from Certain Small Business Stock*** — the QSBS exclusion (chapter 7). Read §1202(a) (the exclusion), §1202(b) (the per-issuer limitation of the greater of $10M or 10x adjusted basis), §1202(c) (the definition of qualified small business stock), §1202(d) (the $50M aggregate gross assets test), and §1202(e) (the active-business requirement and the list of excluded industries).
  - **IRC §280G — *Golden Parachute Payments*** — the change-of-control-payment excise-tax regime that intersects with acceleration provisions (chapter 7's acceleration section; chapter 4's waterfall on the executive line).
- **Treasury Regulations (Title 26 CFR)** — [ecfr.gov Title 26](https://www.ecfr.gov/current/title-26). The operative interpretation of the statute.
  - **Treas. Reg. §§1.83-1 through 1.83-7** — the §83 regulations. §1.83-2 is the 83(b) election-mechanics regulation (form, timing, filing).
  - **Treas. Reg. §§1.409A-1 through 1.409A-6** — the §409A regulations, finalised in 2007. §1.409A-1(b)(5) is the stock-rights-exemption regulation; §1.409A-1(b)(5)(iv)(B) is the FMV-safe-harbor regulation (chapter 5's three safe harbors). §1.409A-3 covers the timing-of-payment rules; §1.409A-6 covers the immediate-income-inclusion consequences.
  - **Treas. Reg. §§1.421 through 1.424** — the statutory-options regulations. §1.422-2 defines ISO qualification; §1.422-4 defines the $100K first-time-exercisable limit (chapter 7).
  - **Treas. Reg. §1.1202** — the QSBS regulations (largely proposed / partial; substantial reliance on the statute itself).
- **IRS Notices, Revenue Rulings, and Revenue Procedures** — [irs.gov/tax-professionals/tax-code-regulations-and-official-guidance](https://www.irs.gov/tax-professionals/tax-code-regulations-and-official-guidance).
  - **IRS Notice 2005-1** — the initial 409A transition guidance.
  - **Rev. Proc. 2002-50** — safe-harbor guidance on ISO substantial-risk-of-forfeiture.
  - **Rev. Rul. 68-153** — the classic 83(b) election-vs.-no-election revenue ruling still cited by practitioners.
- **IRS Publication 525 — *Taxable and Nontaxable Income*** — [irs.gov/publications/p525](https://www.irs.gov/publications/p525). Taxpayer-facing summary of ISO / NSO / RSU / restricted-stock treatment; useful as a plain-English cross-check on the regs.
- **IRS Form 3921 (ISO exercise reporting) and Form 3922 (ESPP purchase reporting)** — [irs.gov/forms-instructions](https://www.irs.gov/forms-instructions). The information returns companies file for each ISO exercise and ESPP purchase; a diligence firm cross-references these to the option ledger and the cap table.

### Federal securities law — Rule 701 and beyond

- **Securities Act of 1933** — [sec.gov/about/laws/sa33.pdf](https://www.sec.gov/about/laws/sa33.pdf). §5 is the registration requirement; every exemption chapter 6 discusses is an exemption *from* §5.
- **Securities Exchange Act of 1934** — [sec.gov/about/laws/sea34.pdf](https://www.sec.gov/about/laws/sea34.pdf). §14(e) (tender-offer anti-fraud) and Rule 14e-1 (tender-offer minimum-open-period) govern secondary-tender programme design (chapter 7's secondary section).
- **17 CFR §230.701 — Rule 701, *Exemption for Offers and Sales of Securities Pursuant to Certain Compensatory Benefit Plans and Contracts Relating to Compensation*** — [ecfr.gov Rule 701](https://www.ecfr.gov/current/title-17/chapter-II/part-230/subject-group-ECFRc41f7fb42c3f0d0/section-230.701). The rule itself. Chapter 6's aggregate-cap and per-grantee disclosure mechanics are §230.701(d) and §230.701(e). The 2018 amendment raising the disclosure threshold from $5M to $10M is documented in [SEC Release No. 33-10521](https://www.sec.gov/rules/final/2018/33-10521.pdf).
- **SEC Concept Release on Compensatory Securities Offerings and Sales (2018)** — [sec.gov/rules/concept/2018/33-10521](https://www.sec.gov/rules/concept/2018/33-10521). The rulemaking release for the 2018 amendment; useful for understanding SEC intent behind the higher threshold and the additional disclosure guidance.
- **Form S-8** — [sec.gov/files/forms-8.pdf](https://www.sec.gov/files/forms-8.pdf). The short-form registration statement post-IPO companies file to register equity-incentive-plan shares (chapter 6's graduation path). One-page substantive filing; the operative content is the plan document filed as an exhibit.
- **Regulation D** — [ecfr.gov Regulation D](https://www.ecfr.gov/current/title-17/chapter-II/part-230/subject-group-ECFR1c9007c9df97e56). The private-placement exemption regime; Reg D 506(b) and 506(c) are the exemptions used for grants to non-eligible-under-701 recipients (chapter 6's consultant-LLC failure mode).
- **Rule 144** — [ecfr.gov Rule 144](https://www.ecfr.gov/current/title-17/chapter-II/part-230/subject-group-ECFR3d19b6e02f2a72c/section-230.144). The resale-exemption regime for restricted / control securities post-liquidity-event.
- **Rule 12b-2** — [ecfr.gov Rule 12b-2](https://www.ecfr.gov/current/title-17/chapter-II/part-240/subpart-A/section-240.12b-2). The definitions section for '34-Act reporting terms including "affiliate" — relevant for tender-offer and secondary-market mechanics.

### State law — Delaware GCL

The overwhelming majority of venture-backed startups are Delaware C-corps. The Delaware General Corporation Law governs the corporate mechanics that every cap-table entry references.

- **Delaware General Corporation Law (Title 8, Delaware Code)** — [delcode.delaware.gov/title8/c001](https://delcode.delaware.gov/title8/c001/). The statute itself.
  - **§102 — Contents of the certificate of incorporation.** The classes-and-series authorisation that governs the "authorised shares" line on the cap table (chapter 1).
  - **§141 — Board of directors: powers.** The board-consent authorising mechanic behind every stock issuance and every option grant.
  - **§151 — Classes and series of stock; rights, etc.** The certificate-of-designation mechanic behind each preferred series' terms (chapter 4's preference-stack setup).
  - **§152 — Issuance of stock; lawful consideration.** The consideration requirement for share issuance.
  - **§157 — Rights and options respecting stock.** The statutory authority for the option pool.
  - **§211 — Meetings of stockholders.** Annual and special meetings; the stockholder-consent mechanic (chapter 3's pool-amendment path).
  - **§228 — Consent of stockholders or members in lieu of meeting.** The written-consent-in-lieu-of-meeting mechanic used for most private-company stockholder actions.
  - **§242 — Amendment of certificate of incorporation.** The mechanic for amending the charter at each priced round.
  - **§251 — Merger or consolidation of domestic corporations.** The merger statute; combined with the certificate's deemed-liquidation-event definition, governs the waterfall trigger (chapter 4).
  - **§262 — Appraisal rights.** The dissenter-appraisal mechanic at merger; a rare but real waterfall consideration when common holders object to the sale.
- **Delaware Franchise Tax** — [corp.delaware.gov/franchisetax](https://corp.delaware.gov/franchisetax/). The two calculation methods — authorised-share method and assumed-par-value-capital method — that govern the annual tax cost of high authorised-share counts (chapter 1's authorised-vs.-issued note).

### Accounting — ASC 718

- **FASB ASC Topic 718 — *Compensation — Stock Compensation*** — [asc.fasb.org](https://asc.fasb.org/). The GAAP standard for recognising the fair-value expense of stock-based compensation on the P&L. Cross-referenced from chapter 7 (equity-comp instrument choice affects the ASC 718 expense profile) and mod-101 (which owns the accrual-accounting substrate).
- **AICPA Accounting and Valuation Guide — *Valuation of Privately-Held-Company Equity Securities Issued as Compensation*** ("the AICPA Practice Aid") — [aicpa-cima.com](https://www.aicpa-cima.com/) and via AICPA Store. First published 2004, updated 2013, and updated further in the mid-to-late 2010s and 2020s. The definitive methodology reference behind every independent 409A appraisal (chapter 5's methodology section). Chapters covering backsolve from priced round, option-pricing-model allocation between preferred and common, DLOM justification, and secondary-tender treatment.

## Tier 2 — Model financing and legal-form documents

The reference templates that most term sheets, charters, and equity-plan documents are drafted against with red-line variations. Every clause chapter 2, 4, or 8 (mod-108) discusses can be traced back to one of these.

- **NVCA — National Venture Capital Association Model Legal Documents** — [nvca.org/model-legal-documents](https://nvca.org/model-legal-documents/). Free download; the industry-standard reference set. Includes:
  - **Model Certificate of Incorporation** — the certificate template with the certificate-of-designation blocks for each preferred series (chapter 4's preference structures).
  - **Model Term Sheet** — the term-sheet template with the option-pool clause chapter 2 quotes.
  - **Model Stock Purchase Agreement** — the preferred-stock issuance template.
  - **Model Investor Rights Agreement** — information rights, registration rights, pre-emptive rights (mod-108 territory but referenced by cap-table reconciliation).
  - **Model Voting Agreement** — drag-along, board composition, waterfall-execution-cooperation covenants.
  - **Model Right of First Refusal and Co-Sale Agreement** — the transfer-restriction and tag-along mechanics.
  - **Model Management Rights Letter** — the VC's ERISA-compliant management-rights template.
  - **Model Legal Opinion** — the closing-opinion template.
  - Model Certificate of Amendment — the charter-amendment template used at each round.
- **Y Combinator SAFE library** — [ycombinator.com/documents](https://www.ycombinator.com/documents). The Simple Agreement for Future Equity templates. Post-Money SAFE (2018 vintage, current standard), Pre-Money SAFE (2013 vintage, legacy), Discount-only, Valuation-Cap-only, and MFN variants. Chapter 1's as-converted view and chapter 2's SAFE-conversion math depend on these. Full treatment in [`mod-105`](../mod-105-convertible-instruments/).
- **Cooley GO Docs** — [cooleygo.com/documents](https://www.cooleygo.com/documents/). Cooley's free document library. Includes equity-incentive-plan templates, restricted-stock-purchase agreements, option-grant agreements, 83(b) election forms, and warrant templates. The templates that most seed and Series-A-stage companies use at formation.
- **Cooley GO Term Sheet Generator** — [cooleygo.com](https://www.cooleygo.com/). Configurable term-sheet builder with the option-pool clause, preference structure, and other levers exposed.
- **Wilson Sonsini Term Sheet Generator** — [wsgr.com](https://www.wsgr.com/) via the firm's resources. Similar tool with a slightly different clause library.
- **Orrick Startup Forms Library** — [orrick.com/en/Total-Access/Tool/Orrick-Startup-Forms-Library](https://www.orrick.com/en/Total-Access/Tool/Orrick-Startup-Forms-Library). Another practitioner-firm free-download library.
- **Gunderson Dettmer Deal Central** — [gunder.com](https://www.gunder.com/). Similar; especially strong on convertible-instrument templates.

## Tier 3 — Cap-table and equity-management platforms

The systems of record that most modern venture-backed startups use for the cap table, the option ledger, the 409A workflow, and (increasingly) the Rule 701 monitoring. The CFO's job is to check the platform's calculation, not to compute the cap table by hand — but the CFO must understand what the platform is doing.

- **Carta** — [carta.com](https://carta.com/). The dominant cap-table platform in the US venture market. Cap-table, option ledger, 409A (Carta Valuations), Rule 701 tracking, secondary-tender workflow. Documentation at [support.carta.com](https://support.carta.com/).
- **Pulley** — [pulley.com](https://pulley.com/). Cap-table and equity-management competitor to Carta with a focus on early-stage companies. Documentation at [support.pulley.com](https://support.pulley.com/).
- **LTSE Equity** — [ltse.com/equity](https://ltse.com/equity). Cap-table platform associated with the Long-Term Stock Exchange.
- **AngelList Stack** — [angellist.com/stack](https://www.angellist.com/stack). Bundled cap-table + banking + payroll product aimed at YC-vintage seed-stage companies.
- **Shareworks (Morgan Stanley at Work)** — [shareworks.com](https://shareworks.com/) / [morganstanley.com/atwork](https://www.morganstanley.com/atwork/). Enterprise-grade equity administration used by larger private and public companies.
- **Global Shares (J.P. Morgan)** — [globalshares.com](https://www.globalshares.com/). Similar mid- to large-company equity admin platform.

### 409A appraisal providers

- **Aranca** — [aranca.com](https://www.aranca.com/) → Valuation Advisory → 409A Valuations. Full-service independent appraiser widely used at Series-A through Series-D.
- **Scalar** — [scalar.io](https://scalar.io/). Formerly ValuatePro; independent appraiser.
- **Preferred Return** — [preferredreturn.com](https://preferredreturn.com/). Boutique 409A firm.
- **VRC (Valuation Research Corporation)** — [valuationresearch.com](https://valuationresearch.com/). Full-service valuation firm.
- **Kroll (formerly Duff & Phelps)** — [kroll.com](https://www.kroll.com/en/services/valuation-services). Enterprise-grade valuation practice with a strong 409A book.
- **Marcum** — [marcumllp.com](https://www.marcumllp.com/services/consulting/valuation). Accounting firm's valuation practice.
- **Andersen** — [andersen.com](https://andersen.com/). Accounting-and-advisory firm's valuation-services practice.
- **Carta Valuations, Pulley 409A, LTSE Equity 409A** — cap-table-platform embedded 409A products bundled with the platform (see Tier 3).

## Tier 4 — Compensation and equity-benchmark data

The benchmark reference sources chapter 3 uses for pool sizing and chapter 7 uses for grant-size defaults. Each publishes on its own cadence; verify the current edition and segment when citing.

- **Carta State of Private Markets** — [carta.com/data](https://carta.com/data/) and [carta.com/blog/state-of-private-markets](https://carta.com/blog/state-of-private-markets/). Quarterly report drawn from Carta's cap-table dataset. Covers pool sizes by stage, grant sizes by role and level, secondary-tender volume, dilution per round, valuation trends, and vesting norms. The most-cited benchmark for pool-sizing conversations at Series-A and Series-B (chapter 3).
- **Carta Total Comp** — [carta.com/blog/carta-total-comp/](https://carta.com/blog/carta-total-comp/). Salary + equity total-compensation benchmark bundling Carta cap-table and payroll data.
- **Pave** — [pave.com](https://pave.com/) and [pave.com/data](https://pave.com/data). Real-time compensation benchmark from partner-company payroll data. Salary and equity bands by role, level, geography, and stage. Chapter 3's per-hire grant-size defaults reference this.
- **Peter Walker — Carta Head of Insights on LinkedIn** — [linkedin.com/in/peterjameswalker](https://www.linkedin.com/in/peterjameswalker/). Continuously updated posts on cap-table trends drawn from the Carta dataset; useful for interim data between quarterly reports.
- **Compensia** — [compensia.com](https://www.compensia.com/). Compensation consulting firm serving late-stage private and public companies; publishes periodic equity-comp survey data.
- **Radford (Aon)** — [aon.com/human-capital-consulting/radford](https://www.aon.com/human-capital-consulting/radford/). Institutional compensation survey used by later-stage private and public technology companies.
- **Option Impact / Advanced-HR** — [advanced-hr.com](https://www.advanced-hr.com/). Venture-industry compensation benchmark database used by VC firms and their portfolio companies.
- **AngelList Talent — Startup Salary and Equity Data** — [angellist.com/talent](https://angellist.com/talent). Startup-specific benchmarks.
- **Levels.fyi** — [levels.fyi](https://www.levels.fyi/). User-submitted comp data; strongest coverage for engineering roles at big-tech and later-stage private companies. Directional rather than definitive.

## Tier 5 — Terms-of-financing surveys

The quarterly and annual surveys that measure the current-market incidence of specific term-sheet clauses — 1x vs. participating preferred, liquidation-preference multiples, anti-dilution provisions, redemption rights, pay-to-play. Chapter 4's "most rounds default to 1x non-participating" and similar claims should be verified against the current-quarter data.

- **Fenwick & West — Silicon Valley Venture Capital Survey** — [fenwick.com](https://www.fenwick.com/) → Insights → publications archive. Quarterly survey of Silicon Valley venture rounds covering pre-money valuations, up/flat/down-round distribution, liquidation-preference multiples, participation-rights incidence, anti-dilution provisions, and pay-to-play. Widely cited by practitioners.
- **Wilson Sonsini Goodrich & Rosati (WSGR) — Entrepreneurs Report and Terms Survey** — [wsgr.com](https://www.wsgr.com/). Quarterly survey with similar coverage; often used as a cross-check on the Fenwick data.
- **Cooley — Cooley GO Venture Financing Report** — [cooleygo.com/venture-financing-report](https://www.cooleygo.com/venture-financing-report/). Quarterly deal-terms report from Cooley's deal book.
- **Aumni (JP Morgan) — Venture Beacon** — [aumni.fund](https://www.aumni.fund/). Data-driven venture terms reporting; strong on preference-stack and participation-rights trends.
- **PitchBook — Venture Monitor** — [pitchbook.com](https://pitchbook.com/) → News & Analysis → Venture Monitor. Quarterly venture market report; complements the law-firm surveys with deal-volume and valuation-trend context.
- **NVCA — Venture Monitor** — [nvca.org](https://nvca.org/) with PitchBook. Same report, association imprint.

## Tier 6 — Practitioner canon

The essays, blogs, and books that translate the statute, regulation, and model documents into founder- and CFO-actionable frameworks. Read tier-6 last, as translation; when there's a conflict with tier-1, tier-1 wins.

### Blogs and essays

- **Brad Feld — *Feld Thoughts*** — [feld.com](https://feld.com/). Long-running blog by the Foundry Group partner. Deep archive on term-sheet mechanics, preference structures, board dynamics, cap-table cleanliness, and founder-side negotiation. The *Term Sheet Series* (2005-2007, still linked from the site) is the founder's-side canon on term-sheet mechanics.
- **Mark Suster — *Both Sides of the Table*** — [bothsidesofthetable.com](https://bothsidesofthetable.com/). Upfront Ventures partner. Founder-facing and investor-facing perspective on venture financing, pool math, and preference stack.
- **Fred Wilson — *AVC*** — [avc.com](https://avc.com/). Union Square Ventures partner. Long-running daily blog with a strong series on venture math and mechanics.
- **Bill Gurley — *Above the Crowd*** — [abovethecrowd.com](https://abovethecrowd.com/). Benchmark partner. Deep-dive essays on late-stage venture dynamics, IPO structuring, and dual-class share structures.
- **Y Combinator SAFE User Guide** — [ycombinator.com/documents](https://www.ycombinator.com/documents). The founder-facing explainer that ships alongside the SAFE templates; covers pre-money vs. post-money SAFE conversion mechanics.
- **Founder Institute — Cap Table Bootcamp** — [fi.co](https://fi.co/). Free founder-education resources on cap-table basics.
- **Holloway — *Guide to Equity Compensation*** — [holloway.com/g/equity-compensation](https://www.holloway.com/g/equity-compensation). A book-length practitioner guide to employee-side equity comp; covers ISO / NSO / RSU / restricted stock mechanics, 83(b), early exercise, QSBS. Employee-facing rather than CFO-facing but useful for the grant-explanation-memo perspective (exercise 07).
- **Andreessen Horowitz — *Equity 101* series** — [a16z.com](https://a16z.com/). Multi-part explainer on equity for founders and employees.
- **First Round Capital — *First Round Review*** — [review.firstround.com](https://review.firstround.com/). Occasional deep-dive articles on cap-table mechanics, hiring, and equity strategy.

### Books

- **Brad Feld and Jason Mendelson — *Venture Deals: Be Smarter Than Your Lawyer and Venture Capitalist*** — Wiley, multiple editions (current is 5th, 2023). The founder-facing canonical text on term sheets, preference structures, and negotiation dynamics. Every founder-CFO should have read this before their first Series-A. Chapter 2's shuffle discussion and chapter 4's waterfall discussion sit on this text's framework.
- **Noam Wasserman — *The Founder's Dilemmas*** — Princeton University Press, 2012. Academic treatment of founder equity splits, co-founder dynamics, and the cap-table decisions that get made (or not made) at formation. Chapter 1's "founder common" section touches this material.
- **Alexander Osterwalder et al. — *Business Model Generation*** — Wiley, 2010. Referenced from mod-102; not directly a cap-table text but relevant framing for founder economics.
- **Andrew Metrick and Ayako Yasuda — *Venture Capital and the Finance of Innovation*** — Wiley, 3rd ed. Academic textbook on venture finance covering pre-money vs. post-money math, term-sheet terms, and preference-stack economics with worked examples. Denser than *Venture Deals* but more mechanically rigorous.
- **Josh Lerner and Ann Leamon — *Venture Capital, Private Equity, and the Financing of Entrepreneurship*** — Wiley, 2nd ed. Harvard Business School textbook covering the broader financing landscape; chapters on term sheets and equity structure directly relevant.
- **Constance Bagley and Craig Dauchy — *The Entrepreneur's Guide to Business Law*** — Cengage, multiple editions. Legal reference for the corporate-formation and equity-issuance mechanics; the Delaware GCL sections referenced in chapter 1 have practitioner treatment here.
- **Frank K. Reilly and Keith C. Brown — *Investment Analysis and Portfolio Management*** — Cengage. The academic reference behind the discount-for-lack-of-marketability (DLOM) methodology chapter 5 discusses.

### Podcasts and video

- **20VC with Harry Stebbings** — [20vc.com](https://www.20vc.com/). Venture-industry interviews with GPs and founders; occasional deep-dives on term sheets and preference-stack mechanics.
- **Acquired podcast** — [acquired.fm](https://www.acquired.fm/). Deep-dive company narratives that often include the cap-table and financing history.
- **This Week in Startups (Jason Calacanis)** — [thisweekinstartups.com](https://thisweekinstartups.com/). Practitioner interviews.
- **YC How to Start a Startup video lectures** — [startupclass.samaltman.com](http://startupclass.samaltman.com/). Free video course from YC's Stanford CS183B iteration; several lectures cover cap-table and equity-comp material.

## Tier 7 — Big Four and law-firm interpretive guides

The audit-firm and law-firm publications that interpret the primary statute and regulation for practitioners. Useful when a specific question — "does this event count as a material event under 409A?", "what disclosures does Rule 701 require above $10M?", "how is a modification accounted for under ASC 718?" — needs a definitive answer beyond the statute itself.

- **PwC — *Viewpoint*** — [viewpoint.pwc.com](https://viewpoint.pwc.com/). Comprehensive interpretive-guide library; requires free registration. Guides on ASC 718 (stock compensation), IRC §409A, Rule 701 disclosure, and NVCA-model interpretation.
- **Deloitte — *Roadmap* series** — [deloitte.com/us/en/pages/audit/topics/roadmap-series](https://www.deloitte.com/us/en/pages/audit/topics/roadmap-series.html). Publicly-available interpretive roadmaps including *Share-Based Payment Awards* (the ASC 718 handbook) and *Compensation — Stock Compensation*.
- **EY — *Financial Reporting Developments*** — [ey.com](https://www.ey.com/). ASC 718 and 409A interpretive coverage.
- **KPMG — *Handbooks* series (Share-based Payment, Compensation)** — [frv.kpmg.us](https://frv.kpmg.us/). Publicly-available handbooks.
- **Cooley — *Cooley Alert* and *Cooley PubCo*** — [cooley.com/news/insight](https://www.cooley.com/news/insight). Regular practitioner alerts on venture financing, SEC rulemaking, and equity-comp legal developments.
- **Wilson Sonsini — *WSGR Alerts*** — [wsgr.com/en/insights](https://www.wsgr.com/en/insights.html). Similar; WSGR is the other dominant venture-side firm.
- **Latham & Watkins — *Client Alerts*** — [lw.com](https://www.lw.com/). Cross-practice alerts including venture and equity-comp.
- **Fenwick — *Publications and Insights*** — [fenwick.com/insights](https://www.fenwick.com/insights). The quarterly financing survey (Tier 5) plus alerts on venture legal developments.
- **Wilson Sonsini — *SEC Reporting Handbook*** — helpful reference for post-IPO Form S-8 mechanics.
- **NVCA Legal Documents Users' Guide** — accompanies the NVCA Model Documents at [nvca.org/model-legal-documents](https://nvca.org/model-legal-documents/). Section-by-section commentary on the model documents.

## Tier 8 — Waterfall and preference-stack tools

Software that runs the waterfall calculation exercise 04 asks the student to build. Useful as a reference and as a sanity-check for the exercise's outputs.

- **Carta — Waterfall Modeling** — [carta.com](https://carta.com/). Built-in waterfall-analysis tool inside Carta for cap tables hosted on the platform.
- **Pulley — Exit Modeling** — [pulley.com](https://pulley.com/). Built-in exit-scenario tool.
- **LTSE Equity — Scenario Modeling** — [ltse.com/equity](https://ltse.com/equity). Similar built-in tool.
- **Capshare (now part of Solium / Morgan Stanley at Work)** — legacy cap-table tool; waterfall analysis remains a documented mechanic in the Solium platform.
- **Excel/Google Sheets — DIY waterfall templates** — the [Cooley GO](https://www.cooleygo.com/) and [Founders Circle](https://founderscircle.com/) resource libraries include downloadable Excel waterfall templates that exercise 04's build can be sanity-checked against.

## Tier 9 — Diligence and reconciliation references

Chapter 1's reconciliation-to-corporate-record discipline is the specific defence against the diligence-firm findings that most late-stage rounds surface. These are the reference documents behind the diligence process itself.

- **NVCA — *Model Diligence Request List*** — an appendix to the NVCA Model Documents. The reference for what a Series-A / Series-B diligence firm will ask for.
- **SharesPost / Nasdaq Private Market — Diligence Playbooks** — [nasdaqprivatemarket.com](https://www.nasdaqprivatemarket.com/). Diligence protocol references used in secondary-tender contexts.
- **AICPA — *Practice Aid on Auditing Equity Instruments*** — [aicpa-cima.com](https://www.aicpa-cima.com/). The auditor-side counterpart to the diligence-firm view; useful for understanding how the annual audit tests cap-table integrity.

## Cross-references to other modules in this track

- [`mod-101` — Startup Accounting Foundations](../mod-101-startup-accounting-foundations/) — the accrual-basis financial vocabulary and the ASC 718 stock-based-compensation expense line the equity-comp mechanics feed. Prerequisite for chapter 7's ASC 718 discussion.
- [`mod-103` — Three-Statement Model and Driver-Based Forecasting](../mod-103-three-statement-model-and-driver-based-forecasting/) — the hiring plan whose grant-per-hire assumptions size the pool this module tops up. The chapter 3 bottom-up pool-sizing depends on the hiring plan built in mod-103's chapter 3.
- [`mod-105` — Convertible Instruments](../mod-105-convertible-instruments/) — SAFEs and convertible notes are represented on the cap table here as as-converted lines; mod-105 covers the mechanics of the instruments themselves and the priced-round conversion that rebuilds the cap table this module's anatomy defines.
- [`mod-106` — Startup Valuation Frameworks](../mod-106-startup-valuation-frameworks/) — the DCF and comparable-company valuations that feed both fundraising and 409A methodology (chapter 5's DCF and comparable-companies methods).
- [`mod-108` — Term Sheets and Preferred Stock Economics](../mod-108-term-sheets-and-preferred-stock-economics/) — the term-sheet negotiation of the preference structures whose waterfall math this module installs. Chapter 4's structures (participating, capped-participation, seniority) are the mechanics; mod-108 owns the negotiation.
- [`mod-109` — Runway Management and Bridge Financing](../mod-109-runway-management-and-bridge-financing/) — down-round mechanics, pay-to-play, and the recapitalisation waterfall against an existing preference stack.
- [`mod-110` — Board and Investor Governance for the CFO](../mod-110-board-and-investor-governance-for-the-cfo/) — the board-consent and stockholder-consent mechanics chapter 3's pool amendments and chapter 5's 409A adoption depend on.
- [`mod-111` — Finance Operations, Controls, and Team Design](../mod-111-finance-operations-controls-and-team-design/) — the audit-readiness workstream that unlocks the Rule 701 disclosure threshold (chapter 6) and the pre-IPO S-8 preparation.
- [`project-102` — Cap-Table and Priced-Round Simulation](../../projects/project-102-cap-table-and-priced-round-simulation/) — the multi-round simulation that exercises every mechanic in this module against stacked SAFEs and priced rounds.
- [`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum) — the sister track that owns equity-comp *policy* (grant guidelines, refresh cadence, IC-plan structure). Chapter-and-module boundary noted in the module README and in each chapter's ownership-boundary section.

## Reading order for this module

If you are new to CFO-grade cap-table and equity-comp work, read in this order before working through the exercises:

1. **NVCA Model Certificate of Incorporation and Model Term Sheet** — the reference against which every priced round is drafted. Read the certificate-of-designation blocks for each series to see the specific preference language chapter 4 discusses.
2. **YC SAFE templates (post-money and pre-money) and the YC SAFE User Guide** — the two SAFE variants and how each converts. Chapters 1 and 2 assume familiarity.
3. **Brad Feld and Jason Mendelson, *Venture Deals*** — the founder-side canonical text. Read cover-to-cover before attempting exercise 02 or 04.
4. **17 CFR §230.701 (Rule 701) and the 2018 SEC amending release** — the securities-law regime chapter 6 covers. Short read; foundational.
5. **IRC §409A and Treas. Reg. §1.409A-1(b)(5)(iv)(B) (the FMV safe-harbor regulation)** — the 409A regime chapter 5 covers. The regulation is more readable than the statute; start there.
6. **IRC §422 and Treas. Reg. §1.422 (the ISO regime); IRC §83 and Treas. Reg. §1.83 (restricted stock and 83(b))** — the tax code that governs chapter 7's instrument choice.
7. **IRC §1202 and IRS guidance on QSBS** — the pot of gold that makes chapter 7's early-exercise recommendation valuable. Read the statute; there are relatively few regulations.
8. **AICPA Practice Aid — *Valuation of Privately-Held-Company Equity Securities Issued as Compensation*** — the methodology behind every 409A report. Required for reading a 409A report critically (chapter 5's critical-read section).
9. **Current-quarter Fenwick / WSGR / Cooley venture-terms surveys** — the current market for preference structures, participation rights, and anti-dilution provisions.
10. **Current-quarter Carta State of Private Markets** — the current market for pool sizes, grant sizes, secondary-tender volume, and valuation trends.
11. **Delaware GCL §§102, 141, 151, 152, 157, 242, 251, 262** — the corporate mechanics behind every cap-table line and the waterfall trigger.
12. **Holloway *Guide to Equity Compensation*** — the employee-facing view; useful when authoring the grant-explanation memo in exercise 07.

Only after this reading should you rely on secondary practitioner content (Substacks, LinkedIn essays, conference talks). Even then, read them as translations of the canon, not as sources of truth. Every specific mechanic cited in a term-sheet negotiation, a board memo, or a diligence response should trace to a tier-1, tier-2, tier-3, or tier-4 source in this list, with the specific section, edition, or vintage named.
