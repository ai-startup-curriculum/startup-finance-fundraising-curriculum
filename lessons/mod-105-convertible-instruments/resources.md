# Resources — mod-105 Convertible Instruments

This is the reference stack behind every chapter and exercise in this module. Sources are grouped by tier of authority: read tier-1 statutory and regulatory sources first; treat tier-6 practitioner content and vendor documentation as interpretive, not authoritative. Every "the rule is X" claim in the chapters should be verifiable against something in this list, and every reference to a SAFE variant, a Reg D exemption, or an NVCA model clause should trace to a specific document in this list at a specific vintage.

Convertible-instrument templates, securities-law rules, and market convention all move. The YC SAFE form was overhauled in 2018 (from pre-money to post-money) and further updated since; the SEC amended the accredited-investor definition in 2020, reformed Reg D integration in the same rulemaking (Rule 152), and periodically issues Compliance and Disclosure Interpretations (C&DIs) that reshape the practical boundary between 506(b) and 506(c); state Blue Sky notice-filing fees and forms change without notice. Cite the specific version and effective date whenever quoting a rule or a template clause. The `<!-- needs-research -->` markers in the chapters flag places where current-year data should be re-verified.

## Tier 1 — Statutory and regulatory primary sources

The federal securities-law regime that governs every SAFE, note, and preferred-round closing in the United States. Read the statute and the regulation, not just a practitioner summary — the practitioners are all interpreting these primary texts.

### Federal securities law — the Securities Act of 1933 and Reg D

- **Securities Act of 1933** — [sec.gov/about/laws/sa33.pdf](https://www.sec.gov/about/laws/sa33.pdf). §5 is the registration requirement that every exemption in chapter 6 exempts *from*. §4(a)(2) is the statutory private-placement exemption that Reg D operationalises as a safe harbour.
- **Regulation D — 17 CFR §§ 230.500-230.508** — [ecfr.gov Regulation D](https://www.ecfr.gov/current/title-17/chapter-II/part-230/subject-group-ECFR1c9007c9df97e56). The private-placement exemption regime.
  - **17 CFR § 230.501 — *Definitions and Terms Used in Regulation D*** — the accredited-investor definition (Rule 501(a)) that chapter 6 catalogues. The definition was materially expanded by [SEC Release No. 33-10824](https://www.sec.gov/rules/final/2020/33-10824.pdf) (effective December 2020) to add professional-certification limbs, knowledgeable-employees, and additional entity limbs.
  - **17 CFR § 230.502 — *General Conditions to be Met*** — Rule 502(a) covers integration; Rule 502(b) covers information requirements when non-accredited investors participate; Rule 502(c) is the general-solicitation prohibition; Rule 502(d) covers resale restrictions.
  - **17 CFR § 230.503 — *Filing of Notice of Sales*** — the Form D filing obligation, 15 calendar days after first sale.
  - **17 CFR § 230.504 — *Exemption for Limited Offerings*** — the small-offering exemption, $10M aggregate in any 12-month period following the 2021 amendment. Rarely used at seed.
  - **17 CFR § 230.506 — *Exemptions for Limited Offers and Sales Without Regard to Dollar Amount of Offering*** — the workhorse exemption. Rule 506(b) is the no-general-solicitation safe harbour used by most private venture rounds. Rule 506(c) is the general-solicitation-permitted safe harbour that requires verified accreditation. Rule 506(d) is the bad-actor disqualification. Rule 506(e) is the bad-actor-disclosure-obligation clause.
  - **17 CFR § 230.507 — *Disqualifying Provision Relating to Exemptions Under §§ 230.504 and 230.506*** — the SEC's disqualification mechanic for failures to file Form D (requires a court injunction against the specific failure).
  - **17 CFR § 230.508 — *Insignificant Deviations from a Term, Condition or Requirement of Regulation D*** — the safe-harbour-preservation provision for de-minimis compliance failures.
- **17 CFR § 230.152 — *Integration Framework for Registered and Exempt Offerings*** — [ecfr.gov Rule 152](https://www.ecfr.gov/current/title-17/chapter-II/part-230/subject-group-ECFRcda1e70bfbadf75/section-230.152). The 2020 integration reform that established the 30-day safe harbour between offerings and reshaped the analysis in chapter 6's Scenario E territory. Rulemaking release [33-10884](https://www.sec.gov/rules/final/2020/33-10884.pdf).
- **17 CFR § 230.144 — *Persons Deemed Not to Be Engaged in a Distribution and Therefore Not Underwriters*** — the resale-exemption regime for restricted / control securities post-liquidity-event. Adjacent to Reg D; relevant when a SAFE holder ultimately resells post-priced-round shares.
- **17 CFR § 230.155 — *Integration of Abandoned Offerings*** — the abandoned-offering integration safe harbour.
- **JOBS Act of 2012** — [sec.gov/spotlight/jobs-act.shtml](https://www.sec.gov/spotlight/jobs-act.shtml). The statute that added Rule 506(c) (Title II of the Act) and Regulation Crowdfunding (Title III). Chapter 6's 506(c) discussion is downstream of Title II.
- **National Securities Markets Improvement Act (NSMIA), 1996** — codified at 15 USC § 77r. The preemption of state substantive qualification of 506 offerings that chapter 6 references. State notice filings and fees are not preempted; substantive registration is.
- **Regulation Crowdfunding (Reg CF) — 17 CFR §§ 227.100-227.503** — [ecfr.gov Regulation Crowdfunding](https://www.ecfr.gov/current/title-17/chapter-II/part-227). The small-non-accredited-investor exemption via SEC-registered funding portals; relevant to chapter 6's integration analysis (Scenario E in exercise 06).
- **Regulation A / Regulation A+ — 17 CFR §§ 230.251-230.263** — [ecfr.gov Regulation A](https://www.ecfr.gov/current/title-17/chapter-II/part-230/subject-group-ECFRe17baec3f057ff4). The "mini-IPO" regime for offerings up to $75M with qualified offering statement. Rarely used at seed; noted for completeness.

### SEC guidance — releases, C&DIs, no-action letters

- **SEC Compliance and Disclosure Interpretations — *Securities Act Rules*** — [sec.gov/divisions/corpfin/guidance/securitiesactrules-interps.htm](https://www.sec.gov/divisions/corpfin/guidance/securitiesactrules-interps.htm). The SEC Division of Corporation Finance's running interpretive guidance on the Securities Act rules including Reg D. Section 256 addresses Rule 502 general-solicitation questions in detail; section 260 addresses Rule 506(c) verification questions; section 261 addresses integration. Consult the current version whenever a fact pattern is close to a boundary.
- **SEC Release No. 33-9415 — *Eliminating the Prohibition Against General Solicitation and General Advertising in Rule 506 and Rule 144A Offerings*** (July 2013) — [sec.gov/rules/final/2013/33-9415.pdf](https://www.sec.gov/rules/final/2013/33-9415.pdf). The rulemaking release adopting Rule 506(c). Chapter 6's history of 506(c) traces here.
- **SEC Release No. 33-10824 — *Accredited Investor Definition*** (August 2020, effective December 2020) — [sec.gov/rules/final/2020/33-10824.pdf](https://www.sec.gov/rules/final/2020/33-10824.pdf). The rulemaking release for the expanded accredited-investor definition. Chapter 6's Rule 501 catalogue depends on this.
- **SEC Release No. 33-10884 — *Facilitating Capital Formation and Expanding Investment Opportunities by Improving Access to Capital in Private Markets*** (November 2020) — [sec.gov/rules/final/2020/33-10884.pdf](https://www.sec.gov/rules/final/2020/33-10884.pdf). The rulemaking release that reformed integration (Rule 152), raised the Rule 504 cap to $10M, and adjusted several Reg CF parameters. The current market-standard integration analysis follows from this release.
- **SEC Release No. 33-9974 — *Amendments for Small and Additional Issues Exemptions Under the Securities Act (Regulation A)*** — the Reg A+ rulemaking release; noted for completeness.
- **SEC Small Entity Compliance Guides** — [sec.gov/info/smallbus/secg.shtml](https://www.sec.gov/info/smallbus/secg.shtml). Plain-English guides to Reg D and Reg CF written for small-issuer counsel; useful cross-check on the rule text.
- **SEC no-action letters on general solicitation** — search the [SEC No-Action Letters database](https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&type=NOACT). The Citizen VC no-action letter (2015) is the load-bearing authority on what constitutes a "substantive relationship" for 506(b) purposes; several follow-on letters refine it.

### Form D and EDGAR

- **SEC Form D and Instructions** — [sec.gov/about/forms/formd.pdf](https://www.sec.gov/about/forms/formd.pdf) and [sec.gov/forms](https://www.sec.gov/forms). The notice-filing form itself, the 15-day-after-first-sale filing obligation of Rule 503.
- **EDGAR Filer Manual** — [sec.gov/info/edgar/edmanuals.htm](https://www.sec.gov/info/edgar/edmanuals.htm). The technical reference for filing on EDGAR including obtaining CIK / access codes.
- **EDGAR Filing Guide** — [sec.gov/edgar](https://www.sec.gov/edgar). Landing page for EDGAR filer resources. First-time Form D filers should obtain CIK / EDGAR access codes several days before the 15-day filing clock starts to avoid a last-minute filing scramble.
- **SEC Investor Alert — *Updated Investor Bulletin: Accredited Investors*** — [sec.gov/oiea/investor-alerts-and-bulletins](https://www.sec.gov/oiea/investor-alerts-and-bulletins). Plain-English accredited-investor primer useful for the investor-facing side of the questionnaire.

### State Blue Sky — notice-filing regimes

Every 506 offering that involves an investor in a specific state requires a state-level notice filing under the state's Blue Sky code, notwithstanding NSMIA preemption of substantive qualification. Each state has its own form, deadline, and fee. Common state references:

- **California Department of Financial Protection and Innovation — §25102(f) Notice Filing** — [dfpi.ca.gov](https://dfpi.ca.gov/). California's notice-filing form for 506 offerings.
- **New York State Department of Law (Attorney General) — Investor Protection Bureau** — [ag.ny.gov/investor-protection](https://ag.ny.gov/investor-protection). New York's Form M-11 (state notice filing) and related requirements.
- **Massachusetts Securities Division — *Regulation of the Sale of Securities*** — [sec.state.ma.us/sct](https://www.sec.state.ma.us/sct/). Massachusetts's notice-filing regime.
- **Texas State Securities Board** — [ssb.texas.gov](https://www.ssb.texas.gov/). Texas's notice-filing regime.
- **NASAA — North American Securities Administrators Association** — [nasaa.org](https://www.nasaa.org/). The organisation of state securities regulators; publishes model uniform notice-filing forms and coordinated filing programmes.
- **NASAA Electronic Filing Depository (EFD)** — [efdnasaa.org](https://www.efdnasaa.org/). The multi-state electronic filing depository for Reg D notice filings; most states accept EFD as the state-level filing channel.

### Federal tax — the note-specific pieces

Chapter 3's convertible-note interest and OID discussion touches these; chapter 6 does not.

- **Internal Revenue Code §§ 1272-1275 — *Original Issue Discount (OID)*** — [uscode.house.gov](https://uscode.house.gov/browse/prelim@title26). The OID regime that governs the imputed-interest treatment of convertible notes issued below face value or with embedded conversion features. Not the everyday concern of a seed-stage note but occasionally load-bearing.
- **Treas. Reg. §§ 1.1272-1 through 1.1275-6** — [ecfr.gov Title 26](https://www.ecfr.gov/current/title-26). The operative OID regulations.
- **IRS Publication 1212 — *Guide to Original Issue Discount (OID) Instruments*** — [irs.gov/publications/p1212](https://www.irs.gov/publications/p1212). Practitioner-facing OID guide.

### State corporate law — Delaware

- **Delaware General Corporation Law (Title 8, Delaware Code)** — [delcode.delaware.gov/title8/c001](https://delcode.delaware.gov/title8/c001/). The statute that governs the corporate authority to issue SAFEs, notes, and preferred stock.
  - **§ 151 — Classes and series of stock; rights, etc.** — the certificate-of-designation mechanic that receives SAFE / note conversions when they become preferred.
  - **§ 152 — Issuance of stock; lawful consideration.** — the consideration requirement for share issuance.
  - **§ 157 — Rights and options respecting stock.** — the statutory authority for the SAFE and the note as contracts entitling the holder to future shares.
  - **§ 242 — Amendment of certificate of incorporation.** — the mechanic for amending the charter at each priced round when the SAFEs and notes convert into a new preferred series.

## Tier 2 — Model financing and legal-form documents

The template documents that every SAFE, note, side letter, subscription agreement, and preferred-round instrument in the module is drafted against with red-line variations.

### YC SAFE templates

- **Y Combinator — *SAFE Financing Documents*** — [ycombinator.com/documents](https://www.ycombinator.com/documents). The Simple Agreement for Future Equity library. The current standard is the **post-money SAFE (2018 vintage)** in the four variants chapter 1 catalogues:
  - **SAFE — Valuation Cap, No Discount** (variant 1).
  - **SAFE — Discount, No Valuation Cap** (variant 2).
  - **SAFE — MFN, No Valuation Cap, No Discount** (variant 3).
  - **SAFE — Valuation Cap and Discount** (variant 4).
  Also available at the same URL: the **pre-money legacy SAFE (2013 vintage)** in the same four variants for reference. The Pro-Rata Side Letter template lives here too. Chapters 1, 2, and 5 all depend on these forms verbatim.
- **Y Combinator — *SAFE User Guide*** — [ycombinator.com/documents](https://www.ycombinator.com/documents). The founder-facing explainer that ships alongside the SAFE templates. Covers the pre-vs.-post-money conversion mechanic in narrative form.
- **Y Combinator — *SAFE Primer*** — [ycombinator.com/library](https://www.ycombinator.com/library/). YC's library of related material including the primer on how SAFEs convert.

### Convertible note templates

- **Cooley GO — Convertible Note Templates** — [cooleygo.com/documents](https://www.cooleygo.com/documents/). Cooley's free convertible-note templates including the standard convertible note, the noteholder consent forms, and related side-letter templates. Chapter 3's note anatomy tracks these forms.
- **Y Combinator — Convertible Note templates (archival)** — [ycombinator.com/documents](https://www.ycombinator.com/documents). YC no longer defaults to convertible notes but has historically published note templates; useful for reading the alternative structure the SAFE was designed to replace.
- **500 Startups KISS (Keep It Simple Security) — Convertible Debt and Convertible Equity versions** — legacy templates from 500 Startups from the 2010s. Occasionally still on cap tables. Not currently maintained but findable via web archive.
- **Gunderson Dettmer — convertible-note forms** — [gunder.com](https://www.gunder.com/). Practitioner-firm templates often used for institutional-lead-driven note rounds.

### Preferred-round model documents

- **NVCA — National Venture Capital Association Model Legal Documents** — [nvca.org/model-legal-documents](https://nvca.org/model-legal-documents/). Free download; the industry-standard reference set for the priced round that a SAFE or note converts *into*. Chapter 4's pro-forma bakes into an NVCA-model Series-A close. Includes:
  - **Model Certificate of Incorporation** — the amended-and-restated charter that adds the new preferred series (and rewrites the SAFE / note conversion by amending the certificate-of-designation).
  - **Model Term Sheet** — the term-sheet template with the option-pool clause and the preferred-stock terms.
  - **Model Stock Purchase Agreement** — the preferred-stock issuance template used at the priced round.
  - **Model Investor Rights Agreement** — information rights, registration rights, pre-emptive (pro-rata) rights that survive the SAFE side letters into the priced-round docs.
  - **Model Voting Agreement**, **Model Right of First Refusal and Co-Sale Agreement**, **Model Management Rights Letter**.
- **NVCA Legal Documents Users' Guide** — companion to the model documents. Section-by-section commentary; the reference for interpreting a specific clause in context.

### Side-letter templates

- **Y Combinator — Pro-Rata Side Letter** — [ycombinator.com/documents](https://www.ycombinator.com/documents). YC's standard pro-rata side letter that accompanies the post-money SAFE.
- **NVCA — Model Right of First Refusal and Co-Sale Agreement** — [nvca.org/model-legal-documents](https://nvca.org/model-legal-documents/). The pre-emptive-rights portion of this document is the priced-round analogue of the seed-stage pro-rata side letter; useful cross-reference when authoring a pro-rata side letter that dovetails with the eventual priced-round rights.
- **Cooley GO — MFN Side Letter Template** — [cooleygo.com/documents](https://www.cooleygo.com/documents/). Cooley's standard MFN side letter.
- **Wilson Sonsini Term Sheet Generator** — [wsgr.com](https://www.wsgr.com/). Configurable term-sheet builder with the side-letter clause library exposed for red-line.
- **Orrick Startup Forms Library** — [orrick.com/en/Total-Access/Tool/Orrick-Startup-Forms-Library](https://www.orrick.com/en/Total-Access/Tool/Orrick-Startup-Forms-Library). Another practitioner-firm free-download library including subscription-agreement templates and standard side letters.

### Subscription agreements and investor questionnaires

- **NVCA — Model Stock Purchase Agreement (representations and warranties sections)** — the accredited-investor representations, bad-actor representations, and jurisdiction-consent language most subscription-agreement templates lift.
- **AngelList — Investor Questionnaire (public sample)** — [angellist.com](https://angellist.com/). AngelList's accredited-investor questionnaire used across their platform; useful reference for what a 506(c)-verification questionnaire looks like.
- **VerifyInvestor.com — verification service** — [verifyinvestor.com](https://verifyinvestor.com/). One of the third-party accreditation-verification services referenced in the SEC's Rule 506(c)(2)(ii) non-exclusive verification methods.
- **Parallel Markets — verification service** — [parallelmarkets.com](https://parallelmarkets.com/). Another 506(c)-verification service used by AngelList, Republic, and similar platforms.

## Tier 3 — Cap-table and equity-management platforms

The systems of record most venture-backed startups use for tracking SAFEs, notes, and the priced-round conversion. Every platform has its own convention for representing an unconverted SAFE and for running the conversion when the priced round is priced. The CFO's job is to verify what the platform is doing against the rules in the module, not to trust the platform's default.

- **Carta** — [carta.com](https://carta.com/). The dominant cap-table platform in the US venture market. Represents SAFEs as on-cap-table instruments; runs the priced-round conversion via a workflow. Documentation at [support.carta.com](https://support.carta.com/). Cross-reference chapter 4's stacked-conversion arithmetic against Carta's output for the same stack.
- **Pulley** — [pulley.com](https://pulley.com/). Cap-table and equity-management competitor to Carta with a focus on early-stage companies. Documentation at [support.pulley.com](https://support.pulley.com/).
- **LTSE Equity** — [ltse.com/equity](https://ltse.com/equity). Cap-table platform associated with the Long-Term Stock Exchange.
- **AngelList Stack** — [angellist.com/stack](https://www.angellist.com/stack). Bundled cap-table + banking + payroll product aimed at YC-vintage seed-stage companies; includes a SAFE-issuance and Form D filing workflow.
- **Clerky** — [clerky.com](https://www.clerky.com/). Automated startup legal formation and issuance platform that handles SAFE issuance, subscription agreements, and Form D filing end-to-end; widely used by YC and other seed-stage companies for lightweight SAFE closings.
- **Stripe Atlas** — [stripe.com/atlas](https://stripe.com/atlas). Incorporation-plus-post-formation product that includes SAFE templates and initial fundraise workflow.
- **Republic** — [republic.co](https://republic.co/). Retail-oriented investment platform that runs offerings under Reg CF and Reg A+; occasionally 506(c) for accredited-only tranches.

### AngelList Syndicates and RUV vehicles

- **AngelList Syndicates** — [angellist.com/syndicates](https://www.angellist.com/syndicates/). SPV-based investment vehicles that pool accredited investors into a single line on the cap table. Chapter 6's Scenario C references this; the deals are structured under 506(c) because the deal is exposed to Syndicate members beyond the pre-existing-relationship boundary.
- **AngelList — Roll-Up Vehicle (RUV)** — [angellist.com/ruv](https://www.angellist.com/ruv/). AngelList's lightweight SPV for consolidating many small investors into a single line; used to keep the SAFE / note ledger clean when many small angels commit.

## Tier 4 — Fundraising-market benchmark data

The current-market pattern-of-terms data for SAFEs, notes, and seed-round structures. Each publishes on its own cadence; verify the current edition when citing.

- **Carta — *State of Private Markets* / *State of the Startup Ecosystem*** — [carta.com/data](https://carta.com/data/). Quarterly reports drawn from the Carta cap-table dataset. Covers current-market SAFE / note prevalence by stage, valuation-cap distributions, discount-rate distributions, priced-round conversion patterns, and dilution per round.
- **AngelList — *State of Startups*** — [angellist.com/blog](https://www.angellist.com/blog/). Periodic data updates on seed-market activity from AngelList's platform data.
- **Peter Walker (Carta Head of Insights) on LinkedIn** — [linkedin.com/in/peterjameswalker](https://www.linkedin.com/in/peterjameswalker/). Continuously updated posts on cap-table and fundraising trends from the Carta dataset.
- **PitchBook — *Venture Monitor*** — [pitchbook.com](https://pitchbook.com/). Quarterly venture-market report with deal-volume and valuation-trend context.
- **NVCA — *Venture Monitor*** — [nvca.org](https://nvca.org/) with PitchBook. Same report, association imprint.
- **Fenwick & West — Silicon Valley Venture Capital Survey** — [fenwick.com](https://www.fenwick.com/). Quarterly survey more focused on priced rounds than on seed convertibles but useful for the priced-round-side of the conversion arithmetic.
- **Wilson Sonsini — Entrepreneurs Report and Terms Survey** — [wsgr.com](https://www.wsgr.com/). Quarterly survey covering priced-round terms.
- **Cooley GO — Venture Financing Report** — [cooleygo.com/venture-financing-report](https://www.cooleygo.com/venture-financing-report/). Quarterly deal-terms report.
- **Aumni (JP Morgan) — Venture Beacon** — [aumni.fund](https://www.aumni.fund/). Data-driven venture-terms reporting; strong on the SAFE-to-priced-round transition.

## Tier 5 — Practitioner canon

The essays, blogs, guides, and books that translate the statute, regulation, and templates into founder- and CFO-actionable frameworks. Read tier-5 last, as translation; when there's a conflict with tier-1, tier-1 wins.

### YC and seed-community canon

- **Y Combinator — *SAFE User Guide*** — [ycombinator.com/documents](https://www.ycombinator.com/documents). Already cited in tier 2; the founder-facing explainer is the closest thing to authoritative on how YC intends the current post-money SAFE to be read.
- **Y Combinator — *Startup School Library — Fundraising*** — [ycombinator.com/library](https://www.ycombinator.com/library/). Free library of essays and video lectures on seed-stage fundraising.
- **Paul Graham — *Fundraising Rounds*** and related essays — [paulgraham.com](http://www.paulgraham.com/). The seed-round conceptual framing that YC's SAFE mechanic is built on.
- **Jared Friedman (YC) — SAFE conversion explainers** — periodic posts on the YC blog and on Twitter/X. Useful current commentary on how the current SAFE form is being interpreted at YC batches.
- **Sam Altman — *Startup Playbook*** — [playbook.samaltman.com](https://playbook.samaltman.com/). Founder-facing playbook that covers seed fundraising mechanics at high altitude.

### Blogs and essays — founder- and investor-side

- **Brad Feld — *Feld Thoughts*** — [feld.com](https://feld.com/). Long-running blog by the Foundry Group partner. Deep archive on term-sheet mechanics, preference structures, board dynamics, and cap-table cleanliness. The *Term Sheet Series* (2005-2007, still linked from the site) is the founder's-side canon on term-sheet mechanics.
- **Mark Suster — *Both Sides of the Table*** — [bothsidesofthetable.com](https://bothsidesofthetable.com/). Upfront Ventures partner. Founder-facing and investor-facing perspective on convertible-note pitfalls, MFN mechanics, and seed-programme structure.
- **Fred Wilson — *AVC*** — [avc.com](https://avc.com/). Union Square Ventures partner. Regular commentary on SAFE-vs.-note trade-offs and seed-round dynamics.
- **Bill Gurley — *Above the Crowd*** — [abovethecrowd.com](https://abovethecrowd.com/). Benchmark partner. Deeper essays on convertible-instrument distortions in the seed market.
- **Elad Gil — *High Growth Handbook* (blog and book)** — [eladgil.com](https://eladgil.com/). Practitioner-oriented essays on fundraising and cap-table management.
- **Naval Ravikant / AngelList — essays on SAFE mechanics** — [angellist.com/blog](https://www.angellist.com/blog/). Historical essays on why AngelList Syndicates converged on 506(c) and how the SAFE fits their model.
- **Founder Institute — Convertible Note Bootcamp** — [fi.co](https://fi.co/). Free founder-education resources on convertible-instrument basics.

### Books

- **Brad Feld and Jason Mendelson — *Venture Deals: Be Smarter Than Your Lawyer and Venture Capitalist*** — Wiley, multiple editions (current is 5th, 2023). The founder-facing canonical text on term sheets, preference structures, and negotiation dynamics. Chapters on convertible debt and SAFEs are the practitioner-standard framing.
- **Andrew Metrick and Ayako Yasuda — *Venture Capital and the Finance of Innovation*** — Wiley, 3rd ed. Academic textbook covering pre-money vs. post-money math, convertible-instrument mechanics, and preference-stack economics with worked examples. Denser than *Venture Deals* but more mechanically rigorous.
- **Josh Lerner and Ann Leamon — *Venture Capital, Private Equity, and the Financing of Entrepreneurship*** — Wiley, 2nd ed. Harvard Business School textbook on the broader financing landscape; chapters on convertible debt and seed structures are directly relevant.
- **Constance Bagley and Craig Dauchy — *The Entrepreneur's Guide to Business Law*** — Cengage, multiple editions. Legal reference for the securities-law regime that governs every SAFE and note closing.
- **Alexander Osterwalder et al. — *Business Model Generation*** — Wiley, 2010. Referenced from mod-102; not a fundraising text directly but framing for founder economics.

### Podcasts and video

- **20VC with Harry Stebbings** — [20vc.com](https://www.20vc.com/). Venture-industry interviews; occasional deep-dives on convertible-instrument market convention.
- **This Week in Startups (Jason Calacanis)** — [thisweekinstartups.com](https://thisweekinstartups.com/). Practitioner interviews including seed-stage fundraise mechanics.
- **YC How to Start a Startup video lectures** — [startupclass.samaltman.com](http://startupclass.samaltman.com/). Free video course from YC's Stanford CS183B iteration; several lectures cover fundraising mechanics.
- **Acquired podcast** — [acquired.fm](https://www.acquired.fm/). Deep-dive company narratives that often include the seed-programme and priced-round history.

## Tier 6 — Law-firm and Big Four interpretive guides

The audit-firm and law-firm publications that interpret the primary statute and regulation for practitioners. Useful when a specific question — "does this fact pattern count as general solicitation?", "does a Reg CF campaign integrate with a subsequent 506(b) round?", "is this MFN drafting elective or automatic?" — needs a definitive answer beyond the statute itself.

### Law-firm alerts and guides

- **Cooley — *Cooley Alert* and *Cooley PubCo*** — [cooley.com/news/insight](https://www.cooley.com/news/insight). Regular practitioner alerts on venture financing, SEC rulemaking, and equity-comp developments. Cooley's *SAFE User Guide* and *Convertible Note Playbook* are cited by many seed-stage founders.
- **Wilson Sonsini — *WSGR Alerts*** — [wsgr.com/en/insights](https://www.wsgr.com/en/insights.html). Similar; WSGR is the other dominant venture-side firm. Their coverage of Rule 506(c) verification methodologies is thorough.
- **Gunderson Dettmer — Deal Central and *Gunder Alerts*** — [gunder.com](https://www.gunder.com/). Alerts on venture financing developments; especially strong on convertible-note market convention.
- **Fenwick & West — *Publications and Insights*** — [fenwick.com/insights](https://www.fenwick.com/insights). The quarterly financing survey plus alerts on venture legal developments.
- **Orrick — *Startup Group Insights*** — [orrick.com/en/insights](https://www.orrick.com/en/insights). Alerts and practitioner guides on seed-stage fundraising and Reg D compliance.
- **Latham & Watkins — *Client Alerts*** — [lw.com](https://www.lw.com/). Cross-practice alerts including venture financing.
- **Perkins Coie — *Startup Percolator*** — [perkinscoie.com/en/news-insights.html](https://www.perkinscoie.com/en/news-insights.html). Alerts on venture and seed financing.
- **Foley Hoag — *Emerging Enterprise Center*** — [foleyhoag.com](https://www.foleyhoag.com/). Boston-market alerts on venture financing and SEC rulemaking.
- **Morrison & Foerster — *Client Alerts*** — [mofo.com](https://www.mofo.com/). Cross-practice alerts including venture financing.

### Big Four interpretive libraries

- **PwC — *Viewpoint*** — [viewpoint.pwc.com](https://viewpoint.pwc.com/). Interpretive-guide library; requires free registration. Guides on ASC 480 / 815 (financial-instrument classification of convertible debt), Reg D compliance, and NVCA-model interpretation.
- **Deloitte — *Roadmap* series** — [deloitte.com/us/en/pages/audit/topics/roadmap-series](https://www.deloitte.com/us/en/pages/audit/topics/roadmap-series.html). Publicly-available interpretive roadmaps including *Contracts on an Entity's Own Equity* (the accounting for convertible instruments).
- **EY — *Financial Reporting Developments*** — [ey.com](https://www.ey.com/). Interpretive coverage of ASC 480 / 815 and related standards.
- **KPMG — *Handbooks* series (Financing Transactions, Debt and Equity Financings)** — [frv.kpmg.us](https://frv.kpmg.us/). Publicly-available handbooks on convertible-instrument accounting classification.

## Tier 7 — Convertible-instrument modelling tools

Tooling and templates that automate parts of the chapter 4 stacked-conversion arithmetic. Useful as reference and as sanity checks against a hand-built pro-forma.

- **Carta — Priced Round Modeling / Waterfall Modeling** — [carta.com](https://carta.com/). Built-in priced-round and exit-scenario tools inside Carta for cap tables hosted on the platform.
- **Pulley — Round Modeling** — [pulley.com](https://pulley.com/). Built-in round-modelling tool for pre-priced-round SAFE conversion planning.
- **LTSE Equity — Scenario Modeling** — [ltse.com/equity](https://ltse.com/equity). Similar built-in tool.
- **Clerky — SAFE and Priced Round Workflows** — [clerky.com](https://www.clerky.com/). Automates SAFE issuance and the mechanical portions of the priced-round conversion.
- **Cooley GO — Convertible Note and SAFE Calculators** — [cooleygo.com](https://www.cooleygo.com/). Free web calculators for basic SAFE and note conversions.
- **Foundersuite / Founders Circle — Downloadable Cap-Table Templates** — [foundersuite.com](https://foundersuite.com/) / [founderscircle.com](https://founderscircle.com/). DIY-spreadsheet templates for founders modelling their own stacks.

## Tier 8 — Diligence references

Chapter 4's pro-forma is directly the artefact a diligence firm will produce at Series-A close from the SAFE / note register and the priced-round terms. These are the reference documents behind that process.

- **NVCA — *Model Diligence Request List*** — an appendix to the NVCA Model Documents. The reference for what a Series-A / Series-B diligence firm will ask for on the SAFE / note side.
- **Cooley GO — Diligence Room Checklist** — [cooleygo.com](https://www.cooleygo.com/). Practitioner checklist for the seed-to-Series-A transition; covers what SAFE, note, side-letter, and Form D artefacts the diligence firm will demand.
- **Wilson Sonsini — Series A Preparedness Guide** — [wsgr.com](https://www.wsgr.com/). Similar practitioner guide.
- **Aumni (JP Morgan) — Convertible Instrument Analytics** — [aumni.fund](https://www.aumni.fund/). Data-driven analysis of convertible-instrument patterns in venture deals.

## Cross-references to other modules in this track

- [`mod-101` — Startup Accounting Foundations](../mod-101-startup-accounting-foundations/) — the accrual-basis framework in which convertible-note interest accrues and convertible-instrument fair-value classification lives on the balance sheet.
- [`mod-102` — Unit Economics and Cohort Financial Modelling](../mod-102-unit-economics-and-cohort-financial-modelling/) — the unit-economics case the SAFE proceeds are being deployed against.
- [`mod-103` — Three-Statement Model and Driver-Based Forecasting](../mod-103-three-statement-model-and-driver-based-forecasting/) — the forecast that justifies the raise size and the runway; the note's maturity clock ticks against this forecast's runway line.
- [`mod-104` — Cap Tables and Equity Compensation](../mod-104-cap-tables-and-equity-compensation/) — the cap-table anatomy, four share-count conventions, and pre-vs.-post-money math this module extends. Prerequisite for chapters 1, 2, and 4.
- [`mod-106` — Startup Valuation Frameworks](../mod-106-startup-valuation-frameworks/) — the valuation methods that set the SAFE / note cap and the priced-round pre-money.
- [`mod-107` — Fundraising Strategy and Investor Targeting](../mod-107-fundraising-strategy-and-investor-targeting/) — the strategy and investor-targeting that produces the SAFE, note, and priced-round closings this module structures.
- [`mod-108` — Term Sheets and Preferred Stock Economics](../mod-108-term-sheets-and-preferred-stock-economics/) — the priced-round preferred-stock terms that all the convertible instruments in this module ultimately convert into.
- [`mod-109` — Runway Management and Bridge Financing](../mod-109-runway-management-and-bridge-financing/) — bridge notes as a specific runway-management instrument; chapter 3's note anatomy is the substrate for bridge-note structuring.
- [`mod-110` — Board and Investor Governance for the CFO](../mod-110-board-and-investor-governance-for-the-cfo/) — the board-consent and stockholder-consent mechanics behind every SAFE, note, and priced-round issuance.
- [`mod-111` — Finance Operations, Controls, and Team Design](../mod-111-finance-operations-controls-and-team-design/) — the audit-readiness and compliance-log workstreams that keep the Form D and state-notice-filing trail defensible.
- [`project-102` — Cap-Table and Priced-Round Simulation](../../projects/project-102-cap-table-and-priced-round-simulation/) — the multi-round simulation that exercises every mechanic in this module against stacked SAFEs and priced rounds.

## Reading order for this module

If you are new to CFO-grade convertible-instrument work, read in this order before working through the exercises:

1. **Y Combinator SAFE User Guide and the four current post-money SAFE templates** — the operative forms behind chapters 1, 2, 4, and 5. Read every clause of one variant end-to-end.
2. **YC pre-money legacy SAFE (2013 vintage)** — read alongside the post-money form to see the specific "SAFE Price" definition change that drives chapter 2's different mechanic.
3. **A Cooley GO or Gunderson Dettmer convertible-note template** — the standard note form behind chapter 3. Read the principal / interest / maturity / conversion clauses in the order chapter 3 catalogues them.
4. **NVCA Model Certificate of Incorporation and Model Term Sheet** — the priced-round documents that receive the SAFE / note conversion in chapter 4.
5. **17 CFR §§ 230.500-230.508 (Regulation D) and 17 CFR § 230.152 (Integration Framework)** — the operative rules behind chapter 6. Short read; foundational.
6. **SEC Release No. 33-10824 (2020 accredited-investor definition amendments)** — the current Rule 501 definition. Read the release and cross-reference to Rule 501(a).
7. **SEC C&DIs on Regulation D (Sections 256, 260, 261)** — the interpretive guidance on general solicitation, 506(c) verification, and integration. Consult before writing any 506(b)-vs.-506(c) memo.
8. **Brad Feld and Jason Mendelson, *Venture Deals*** — the founder-side canonical text. Read the SAFE / note chapters before attempting exercise 04.
9. **Current-quarter Carta *State of Private Markets*** — the current market for SAFE / note valuation caps, discount rates, and priced-round conversion patterns.
10. **A YC batch's post-Demo-Day disclosure playbook** (available through YC's internal batch resources; approximated by public YC blog posts on Demo Day compliance) — the practitioner framing of the specific general-solicitation problem chapter 6 Scenario B covers.
11. **A boutique startup-securities lawyer's most-recent Reg D compliance alert** (Cooley, Wilson Sonsini, Gunderson, Orrick, or Perkins Coie) — the current-year interpretive answers to the Rule 506 questions that come up on every raise.

Only after this reading should you rely on secondary practitioner content (Substacks, LinkedIn essays, conference talks). Even then, read them as translations of the canon, not as sources of truth. Every specific mechanic cited in a SAFE, a side letter, a note, or a Reg D memo should trace to a tier-1 or tier-2 source in this list, with the specific section or vintage named.
