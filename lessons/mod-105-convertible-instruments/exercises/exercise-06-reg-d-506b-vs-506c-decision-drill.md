# Exercise 06 — Reg D 506(b) vs. 506(c) Decision Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 6 (Reg D exemptions 504, 506(b), 506(c), and Form D). Also references chapter 5 (side letters — the subscription agreement lives alongside the SAFE).

## Problem statement

Six hypothetical seed-stage raise scenarios are described below. For each, pick the correct Reg D exemption (Rule 504, 506(b), or 506(c)), justify the choice against the specific rule text, walk the Form D filing and state notice-filing obligations, and write a one-page compliance memo the founder can hand to counsel or to an incoming investor. Then produce a single consolidated compliance-checklist template the founder can use for every future closing.

The drill's purpose is not to make anyone a securities lawyer — every real raise still goes through counsel — but to install the CFO-level pattern recognition: which exemption fits which fact pattern, which facts push a raise across an exemption boundary, and which compliance step comes at which point in the closing timeline.

## The six scenarios

For each scenario, produce the decision memo described in the requirements. Assume the company in each scenario is a Delaware C-corp incorporated less than three years ago with no prior SEC-reporting history and no disqualifying bad-actor events among covered persons unless the scenario says otherwise.

- **Scenario A — Friends-and-family SAFEs.** The founder is closing $500,000 of post-money SAFEs at a $6,000,000 cap from six angel investors — a college roommate, a former manager, two neighbours, and two family friends. Two of the six are personally accredited (income test); four are not accredited but are "sophisticated" in the founder's assessment (all hold advanced degrees; one is a CPA). The founder has not tweeted, posted, or otherwise publicised the raise; all six investors were approached one-on-one through the founder's personal network.

- **Scenario B — YC batch demo-day-plus-DMs.** The founder just came out of a YC batch. During Demo Day, YC live-streamed the founder's two-minute pitch to a public audience of thousands. Following Demo Day the founder is fielding inbound DMs from unknown investors and is closing $2,000,000 of post-money SAFEs at a $15,000,000 cap. All prospective investors self-represent as accredited via a Google Form the founder built; the founder has done no independent verification. Investors include institutional seed funds, angel networks, and several individuals the founder has never met.

- **Scenario C — AngelList Syndicate raise.** The founder is running a $1,500,000 raise through an AngelList Syndicate. AngelList's platform posts the deal to Syndicate members (LPs who have signed up with the platform, some of whom the founder has no pre-existing relationship with). AngelList's verification service confirms accreditation of all Syndicate participants. The founder is not otherwise publicising the raise outside AngelList.

- **Scenario D — Rolling seed at a boutique-fund lead.** The founder has a boutique institutional seed fund as lead ($1,000,000 on a $12,000,000 post-money cap) and is filling the remaining $500,000 of a $1,500,000 target from the lead's investor network. The lead's General Partner is personally introducing each additional investor to the founder; all additional investors are institutional funds or personally accredited high-net-worth individuals. There is no public announcement of the raise.

- **Scenario E — Crowdfunding-plus-506 stacked round.** The founder ran a $500,000 Regulation Crowdfunding (Reg CF) campaign via a SEC-registered funding portal three months ago that closed with 400+ small-dollar non-accredited investors. The founder is now closing an additional $1,500,000 of post-money SAFEs at a $10,000,000 cap. The current raise is being filled by a lead institutional seed fund plus a handful of accredited angels from the founder's network; no public solicitation for this second raise. Question: what does the earlier Reg CF campaign do to the exemption analysis for the current raise (integration, if any), and what exemption does the current raise fit under?

- **Scenario F — Ambiguous solicitation.** The founder has appeared on two well-known founder-focused podcasts in the last two months. On the first, the founder discussed the business generally and did not mention a specific raise. On the second, the founder said "we're actively raising a seed round right now and looking for investors who have deep expertise in vertical X" but did not name a specific dollar amount, cap, or terms. Following the podcast appearances, the founder has taken inbound interest and is closing $1,000,000 of SAFEs at a $10,000,000 cap. Roughly half of the interested investors were introduced through the founder's pre-existing network; the other half heard about the raise from the second podcast. All are self-represented accredited.

## Requirements

For each of the six scenarios (A-F), produce the following in a single workbook with per-scenario tabs plus a final consolidated checklist:

1. **Exemption decision.** Pick one of {Rule 504, Rule 506(b), Rule 506(c), or "does not fit inside Reg D — see counsel"}. Justify the choice by:
   - Quoting the specific sub-rule (e.g., "Rule 506(c)(2)(i) prohibits sales to non-accredited investors under this rule").
   - Explaining why the alternative exemptions don't fit.
   - Flagging any specific fact in the scenario that pushes the analysis toward or away from the chosen exemption.
2. **Accredited-investor analysis.** For each investor category in the scenario, identify:
   - Which limb of Rule 501(a) they qualify under (income test, net-worth test, professional certification, entity limb, etc.).
   - Whether the exemption chosen permits their participation (some limit non-accredited; some prohibit).
   - The verification approach: self-certification (permitted under 506(b) for accredited investors) vs. reasonable-steps verification (required under 506(c)).
3. **General-solicitation analysis.** Identify whether any general solicitation has occurred in the scenario's fact pattern. Cite the SEC's guidance (Rule 502(c), the C&DIs on general solicitation, and the JOBS Act clarifications). Flag any facts that are ambiguous (Scenario F is deliberately ambiguous) and explain the reasoning.
4. **Form D filing plan.** Specify:
   - The Form D deadline (15 calendar days after first sale — chapter 6, Rule 503).
   - Whether EDGAR filer credentials (CIK) need to be obtained (assume no if the company has previously filed).
   - The specific fields on Form D that need particular attention for the scenario (e.g., the accredited/non-accredited investor count field, the exemption-relied-upon field, the aggregate offering size field).
   - The Form D amendment plan (when the offering closes above the initial amount, when the offering stays open more than a year).
5. **State notice-filing plan.** Identify which states' notice-filing obligations apply based on where the investors reside. For the drill, assume investors reside as follows (choose specific states based on scenario plausibility):
   - Scenarios A, D, F: California and New York investors only.
   - Scenario B: California, New York, Massachusetts, and Illinois investors.
   - Scenario C: California, New York, Texas, Florida, and Massachusetts investors (Syndicate members).
   - Scenario E: California, New York, and 400+ Reg CF investors spread across all 50 states.
   Cite the relevant NSMIA preemption of substantive state-law qualification for 506 offerings, then identify the state notice-filing and fee obligations that remain.
6. **Bad-actor screening.** Specify the covered-person set for the scenario (directors, executive officers, 20%-plus stockholders, promoters, compensated solicitors). List the questionnaire questions that need to be run (SEC or state injunctions, court orders, criminal convictions relating to securities, etc.). For scenario D, additionally consider whether the lead fund's GP counts as a covered person.
7. **Integration analysis.** For every scenario, briefly consider whether any prior or contemporaneous offering could be integrated with the current raise (Rule 152 as reformed in 2020). Scenario E is the primary integration test (Reg CF followed by a 506 offering); for the others, flag the analysis as low-risk with a one-line justification.
8. **One-page compliance memo.** Written to the founder for each scenario, covering:
   - The exemption chosen and the one-line reason.
   - The three or four most important compliance dates on the timeline (first sale, Form D deadline, state notice deadlines, any amendment triggers).
   - The specific verification approach for accredited status (self-cert vs. reasonable-steps).
   - Any facts in the scenario that need to be re-checked with counsel before proceeding (e.g., ambiguous general-solicitation facts in Scenario F).
   - A "do not do" list — the specific actions the founder should avoid to preserve the exemption (e.g., "do not accept non-accredited investors under 506(b) without the S-1-style disclosure package"; "do not tweet the specific terms of the raise if relying on 506(b)").
9. **Consolidated compliance checklist.** A single checklist the founder can print and use for every future closing, aggregating the common steps across the six scenarios. Include:
   - The exemption-choice decision tree (chapter 6's "choose 506(b) when / choose 506(c) when" logic).
   - The accredited-investor questionnaire template (or a reference to a specific template such as the ones in the resources.md file).
   - The subscription-agreement fields that need to be completed at each closing.
   - The bad-actor questionnaire template.
   - The Form D pre-filing checklist (CIK obtained, exemption identified, offering-size field prepared).
   - The state-notice-filing tracker (a table with columns for state, deadline, fee, filed date, confirmation number).
   - The document-retention list (SAFE / note, subscription agreement, investor questionnaire, Form D acknowledgment, state notice confirmations, bad-actor questionnaires, verification evidence for 506(c)).

## Starter guidance

- **Read Rule 501(a), Rule 502, Rule 503, Rule 504, and Rule 506 before starting.** Every answer in the drill traces to one of these rules. The rule text is short and precise; the practitioner summaries are approximations.
- **The SEC C&DIs on general solicitation are the definitive source** for the boundary between "talking about the business" and "soliciting a specific offering." Section 256 of the C&DIs (Rule 502 - General Solicitation) covers most of the fact patterns in the drill.
- **The 15-day Form D deadline runs from first sale, not from first offer.** "First sale" is the first date an investor is irrevocably committed and payment has been made. Get this date right in the scenario timeline.
- **NSMIA (National Securities Markets Improvement Act, 1996, codified at 15 USC § 77r) preempts state substantive qualification of 506 offerings** but does not preempt state notice filings and fees. State notice filing deadlines vary — many are the same 15-day window as federal Form D, but some are different. Consult the specific state's Blue Sky code (or a service like COGENCY Global) for each state.
- **For scenario B**, the YC Demo Day is a widely-known industry practice; the SEC has not issued specific guidance blessing (or condemning) Demo Day-triggered raises. Consider whether the specific fact of a public livestream converts the follow-up SAFE closings into 506(c) territory. Some practitioners argue that if the founder has been pitching investors before Demo Day under 506(b) and Demo Day is a continuation of that relationship-building, 506(b) can still apply; others argue the livestream is a general solicitation that pushes the round onto 506(c). The right answer for a real deal is "ask counsel"; for the drill, produce a defensible analysis with cited authority.
- **For scenario C**, AngelList Syndicates operate as a 506(c) platform because the deal is exposed to Syndicate members who are not necessarily in a pre-existing relationship with the company. AngelList itself provides verification services to satisfy 506(c)'s reasonable-steps requirement.
- **For scenario D**, the boutique fund lead's introduction of additional investors is a common seed-round pattern. The pre-existing relationship required for 506(b) can extend to the lead's network via the lead's substantive relationship with each investor, provided the lead is not acting as an unregistered broker. Consider whether the lead's role creates any specific issue.
- **For scenario E**, integration between a Reg CF campaign and a 506 offering is specifically addressed by the SEC's 2020 integration reforms (Rule 152). Reg CF and a subsequent 506 offering more than 30 days apart are generally not integrated. Verify the timing in the scenario.
- **For scenario F**, apply the SEC's "reasonable-belief" test: a specific mention of an active raise on a public podcast is a general solicitation of that offering, even without dollar amounts. The founder has probably pushed the round onto 506(c) territory with the second podcast. Model the remediation: either (a) run the round as 506(c) with verification, or (b) rely on 506(b) only for investors with a demonstrable pre-existing substantive relationship and use 506(c) for the podcast-inbound investors, with an integration analysis to keep the two closings separate.
- **Cite the specific rule and the specific SEC release** for each decision. Do not paraphrase without citing. Cited authority is what makes the memo useful to counsel; unattributed reasoning is what makes it a homework exercise.

## Acceptance criteria

- **Each of the six scenarios has an exemption pick** (or an explicit "does not fit — see counsel") with the specific rule text cited.
- **Scenario A**: 506(b) with accredited-only-in-practice guidance (the four non-accredited-but-sophisticated investors trigger the S-1-style disclosure obligation, which is prohibitive; the memo recommends declining those four or restructuring).
- **Scenario B**: 506(c) with verification, because Demo Day is a general solicitation and the follow-up round has to be handled as a 506(c) raise. (An alternative defensible answer accepts 506(b) for a narrow subset of investors with pre-existing substantive relationships and 506(c) for the rest, with the integration analysis in step 7 held above zero risk.)
- **Scenario C**: 506(c) — AngelList Syndicate structure.
- **Scenario D**: 506(b) — private, network-based, no general solicitation.
- **Scenario E**: 506(b) or 506(c) for the current raise, with an integration analysis showing that the Reg CF campaign three months ago does not integrate with the current raise (Rule 152, safe-harbor of 30-day separation exceeded).
- **Scenario F**: 506(c), with a memo that specifically flags the second podcast appearance as the crossing of the general-solicitation line and prescribes verification for all investors going forward.
- **Every memo identifies the Form D 15-day deadline** and the state notice-filing obligations for the specified states.
- **Every memo runs the bad-actor questionnaire** on the covered-person set.
- **The consolidated compliance checklist covers all common steps** across the six scenarios and is usable as a template for future closings.
- **Every rule citation is to a specific sub-rule** (e.g., "Rule 506(c)(2)(ii)(A)" not "Rule 506(c)"), and every state-notice claim cites the specific state's Blue Sky code section or a specific service resource.

## Deliverables

- The workbook with six per-scenario tabs plus the consolidated compliance-checklist tab.
- Six one-page compliance memos (Markdown or PDF, one per scenario).
- A one-page cover memo summarising the drill's teaching points ("Demo Day pushes the round onto 506(c) unless carefully handled; AngelList Syndicates are 506(c); podcasts that name a specific raise are general solicitation; the 15-day Form D clock always runs from first sale") for the founder's reference.

## Extensions (optional)

- **Add a seventh scenario** — a fundraise partly funded by a foreign investor (a UK-resident angel accredited under the UK Financial Conduct Authority's equivalent test but not a US "accredited investor" under Rule 501(a)). Analyse whether Reg D applies at all, whether Regulation S (offshore-offering safe harbour) is relevant, and how the analysis changes.
- **Model a bad-actor scenario** — one of the directors of the company in Scenario A was subject to an SEC administrative order five years ago that meets a Rule 506(d)(1) disqualifying-event definition. Walk the three remediation options (reasonable-care defence, SEC waiver application, restructure to remove the covered person) and recommend one for the specific facts.
- **Author the Form D filing itself** for Scenario A. Draft each field of the Form D as it would be submitted to EDGAR. Cross-check against the current Form D on the SEC website.
- **Trace a specific state's Blue Sky notice-filing process** — pick California (its Section 25102(f) filing) or New York (its M-11 filing) and produce the actual filing document and the fee-schedule reference. Compare the two states' processes.
- **Interview a startup securities lawyer** (or read the Cooley GO / Wilson Sonsini Alerts on current-year Reg D guidance) and add any recently-issued C&DIs or interpretive letters that would change the analysis of any scenario. Cite specifically.
