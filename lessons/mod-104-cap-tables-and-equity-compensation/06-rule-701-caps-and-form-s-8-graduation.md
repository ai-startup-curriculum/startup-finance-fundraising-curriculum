# Rule 701 Caps and Form S-8 Graduation

## Why this matters

The default rule under the federal securities laws — Section 5 of the Securities Act of 1933 — is that every offer or sale of a security must either be registered with the SEC or fit inside a specific exemption. Employee options are securities. A private company that grants options to its employees is offering securities to those employees.

Registering a stock offering is expensive and public — S-1 territory. Private companies rely on **exemptions**. For employee equity compensation, the exemption is **Rule 701** under the Securities Act, which exempts offers and sales of securities "pursuant to a written compensatory benefit plan" from registration, subject to two caps: an **aggregate annual limit** on the value of securities the company can issue under the rule (with three alternative formulations, whichever is largest) and a **per-grantee disclosure obligation** that kicks in above another threshold.

Exceed the aggregate limit and the option grants above the cap lose their exemption — they are unregistered offerings that violated Section 5, which is a serious problem. The remedy is a rescission offer, plus potential SEC enforcement action, plus a diligence problem at every subsequent round. Miss the disclosure trigger and every grantee above the disclosure threshold has a **rescission right** to unwind their exercise, plus the company has a securities-law compliance failure to disclose in every future financing.

Rule 701 is the securities regime that governs the size of the option pool a private company can actually deploy in a 12-month period. This chapter installs the mechanic, the alternative caps, the disclosure trigger, and the graduation path to Form S-8 (which registers the plan and removes the caps entirely, but is only available after IPO).

## The Rule 701 exemption in one paragraph

Rule 701 (17 CFR §230.701) exempts from Section 5 registration the offer and sale of securities by a company not subject to the '34 Act reporting requirements, pursuant to a written compensatory benefit plan, to natural persons who are the company's employees, directors, general partners, trustees, officers, consultants, or advisors (and specific family members of those persons under permissible transfers), subject to aggregate size and per-grantee disclosure limits. That's it. The rule is short, the cases are few, and the mechanic is well-settled — the operational challenge is not interpretation but *tracking*.

## Who counts as a Rule 701 recipient

Rule 701 is available only for natural persons, and only for a defined set of relationships:

- **Employees** — including part-time employees.
- **Directors** — of the company or its consolidated subsidiaries.
- **General partners, trustees, officers.**
- **Consultants and advisors** — but only if they are natural persons providing bona fide services (not to promote or maintain a market for the company's securities), and only if the services rendered are not in connection with the offer and sale of securities in a capital-raising transaction. This carve-out is what stops the company from using Rule 701 to compensate a fundraising advisor.
- **Family members** who acquire the securities from an eligible recipient through gifts or domestic-relations orders.

Grants to entities (an advisor's LLC, a portfolio company's fund) do not qualify under 701. Grants to non-natural-person consultants have to fit a different exemption (usually Reg D 506(b) or 506(c)).

## The aggregate cap — take the largest of three

The heart of Rule 701 is the aggregate cap. The company may sell, under Rule 701, securities during any consecutive 12-month period with an aggregate sales price or amount not exceeding **the greatest of**:

1. **$1,000,000**, or
2. **15% of the total assets** of the company (or of the parent, if the plan is at the subsidiary level), measured at the company's most recent balance-sheet date, or
3. **15% of the outstanding amount of the class of securities being offered** (typically common stock), measured at the same date.

The rule takes the *largest* of the three, not the smallest, and the company chooses the alternative that produces the largest headroom for the period.

**Which alternative is largest at each stage.**

- **Pre-seed / seed.** The $1M dollar floor is usually the largest for a company with under $6.7M in assets and few outstanding common shares. The dollar floor gives seed-stage companies a working budget of $1M / year for option grants (measured at FMV, i.e., 409A per-share value × shares granted), which is roughly the pool consumption for a small team.
- **Series-A.** 15% of common outstanding usually exceeds the $1M floor once the company has enough founder + exercised common on its books. If the company has 8M common outstanding × current 409A of $1.20 = $9.6M common-equity base, 15% is $1.44M. Add: has the round proceeds hit the balance sheet? If yes, 15% of assets is likely the largest — a $10M raise with $8M cash left on the balance sheet is $8M × 15% = $1.2M plus any other assets; often the 15%-of-assets alternative is roughly in line with the 15%-of-common alternative at Series-A.
- **Series-B+.** 15% of assets usually dominates — assets include cash from the last round plus AR plus fixed assets plus intangibles, all growing with the company. A Series-B company with $30M cash + $10M other assets = $40M in total assets has a 15% cap of $6M per rolling 12 months. This is usually enough for the pool consumption of a company that size.
- **Late-stage pre-IPO.** 15% of common outstanding might reassert as largest once the fully-diluted count is very high. The 15%-of-assets alternative continues to grow with the balance sheet.

The CFO's job is to compute all three alternatives at the start of each rolling 12-month period, pick the largest, and monitor consumption against it.

## What counts as consumption

Consumption is measured at the **date of grant** (for options) at the **exercise price** *plus* the FMV of the shares at grant (i.e., the total consideration if exercised immediately at the current FMV). More precisely, per Rule 701(d)(3): the aggregate sales price for an option is the exercise price multiplied by the number of shares underlying the option.

- **Options granted (at FMV strike):** the exercise price × shares underlying = the consumption at grant. For a company where FMV = strike, this is roughly the grant's "in the money" value would be zero at grant, but the *aggregate sales price* is still counted at strike × shares.
- **Options exercised:** exercise price × shares actually exercised, counted at exercise if it occurs during a different rolling window than the grant. In practice, most companies count at grant, not at exercise, and confirm that consumption tracks accordingly.
- **RSUs settled:** FMV × shares delivered at settlement. RSU grants themselves are counted when they settle (i.e., convert to actual shares) rather than at grant date, because the rule measures at the point of security issuance.
- **Restricted stock purchased:** purchase price × shares.

Different startup-CFO / GC practitioners weight the "measured at grant vs. exercise" question slightly differently. The conservative practice is to track *both* — the total grants during the period, and the total actual issuances (exercises / vestings) during the period — and stay under the cap on the higher of the two.

## The per-grantee disclosure obligation

Beyond the aggregate cap, Rule 701 has a **disclosure trigger** that kicks in when the aggregate sales price or amount of securities sold under Rule 701 during any consecutive 12-month period **exceeds $10 million** (raised from $5M by an SEC amendment in 2018).

Above the $10M threshold, the company must provide each investor, a reasonable period of time before the date of sale, a specific set of disclosures:

- **A copy of the compensatory benefit plan** (the equity incentive plan document).
- **A description of the risks** associated with the investment (specific risk factors, like an S-1 short-form).
- **The company's financial statements** — not audited under Rule 701 as written, but the more recent AICPA and SEC guidance drives most late-stage private companies to provide either the most recent audited financials or, if not audited, the balance sheet not more than 180 days old plus the income statement and CFS for the period since.

The financial statements requirement is the operational hurdle. A late-stage private company crossing the $10M / 12 months threshold usually already has audited financials (Series-B or later companies typically get their first audit as a Series-B closing condition, or shortly after). But if not, crossing the threshold forces the audit-financials workstream.

**Failure to disclose creates a rescission right.** Each grantee who received securities without the required disclosures has the right to unwind the transaction — return the shares to the company and get their exercise price back. Rescission rights are typically 1-2 years long (state statutes of limitation vary). Rescission rights are also a diligence-flagged material item that has to be disclosed at every subsequent financing and IPO.

## Rolling 12-month monitoring

The cap is a **rolling 12-month** measurement, not a calendar year or fiscal year. Every month, the CFO computes:

- Total consumption over the trailing 12 months (grants × strike + settled RSUs × FMV + restricted stock × purchase price).
- Current cap (largest of $1M, 15% of assets, 15% of outstanding common) as of the most recent quarterly balance sheet.
- Headroom = cap − consumption.

If headroom shrinks below, say, 20%, planning discussions begin: is the next quarter's expected grant activity going to blow the cap? Is a large annual refresh cycle coming up? Is there a pending large grant (VP-level hire) that would tip it?

The reality at most late-stage private companies is that the cap does not bind — 15% of a $200M-asset company is $30M / year, which is more than the annual grant activity. The cap becomes binding when a company is:

- **Late-stage but not yet audited**, and about to cross $10M / 12 months and hit the disclosure obligation without the financial statements ready.
- **Doing a large one-time grant**, e.g., a founder-refresh grant, a large key-executive hire, or an aggressive tender-offer participation grant.
- **Doing an option-exchange / repricing** where the newly-issued (or newly-modified) options count for a fresh Rule 701 measurement.

## Failure modes and remedies

**Exceeded the aggregate cap.** The grants above the cap are unregistered offerings in violation of Section 5. The remedy is a **rescission offer** — the company offers to buy back the securities at the original purchase price plus interest. The rescission offer itself needs to fit under a different exemption (typically Regulation D or a state exemption), which adds complexity. SEC enforcement action is possible but unusual for good-faith cases. Diligence firms will insist on complete disclosure at every subsequent round.

**Exceeded the $10M disclosure threshold without providing the disclosures.** Each grantee above the threshold has a **rescission right**. The company should promptly provide the missing disclosures and consider offering the grantees a formal rescission opportunity. Every subsequent financing round will include disclosure of the rescission right as a material item.

**Consultant / advisor grant to a non-natural-person.** Grant doesn't qualify under Rule 701; must be qualified under a different exemption. If the grant was intended to sit under 701 and doesn't, the company has an unregistered offering. Fix: shift the grant to a personal-name recipient or rescind and re-issue under Reg D 506(b).

**Grant during a "gun jumping" window before an IPO S-1 filing.** Complicated interaction between Rule 701 and the '33 Act quiet-period rules. Speak to counsel; there are specific carve-outs for equity compensation grants that continue during the pre-IPO window.

## Graduation to Form S-8

Once a company becomes SEC-reporting (typically post-IPO under the '34 Act), Rule 701 stops being the operative regime. The company files a **Form S-8** — a short-form registration statement — that registers the shares underlying the equity incentive plan. Post-S-8:

- No aggregate cap on the value of options / RSUs the company can issue.
- No per-grantee disclosure obligation (the '34 Act filings substitute).
- Employees can exercise and immediately sell without a resale exemption (the Form S-8-registered shares are freely tradable, subject to short-swing profits rules for insiders and the Rule 144 volume limits for affiliates).

Form S-8 is short and cheap to file — it's a mostly ministerial filing. The company files an initial S-8 at IPO covering existing plan shares, then files additional S-8s as new share reserves are added.

**Between the SEC-reporting trigger and the S-8 filing** there is a window (usually days) where the company is subject to the '34 Act but hasn't yet registered the plan. Grants during this window need special handling — usually the company just doesn't grant during the window, or the counsel writes a specific carve-out.

## Pre-IPO planning

The Rule 701 discipline builds naturally toward IPO-readiness:

- **Audit-readiness** (typically at Series-B for other reasons — mod-111) also unlocks the $10M / 12 months disclosure threshold with financial statements in hand.
- **Cap-table platform** (Carta, Pulley, LTSE Equity) that automates the Rule 701 consumption calculation is now standard; the CFO's job is to check the calculation, not to compute it by hand.
- **The IPO cap** — the fully-diluted count at IPO includes every grant that has been made, and the S-1 discloses the historical grant activity, so any Rule 701 issue in the prior 3-5 years surfaces.
- **The dual-track** (IPO or acquisition) approach makes the Rule 701 discipline extra important because an acquisition diligence process finds Rule 701 problems as fast as an IPO diligence process.

The pre-IPO CFO's typical workstream (relevant to mod-111 finance-ops) includes:

- Reviewing 3+ years of Rule 701 consumption for any missed disclosures or cap overages.
- Fixing any historical issues (rescission offers, disclosure supplements) *before* filing the S-1.
- Ensuring the equity incentive plan documents are S-8-ready and the shares reserved under the plan are stated as a fully-diluted share count.

## Interaction with the option pool

Rule 701 is a *separate* constraint from the option pool. The option pool is the internal share reserve that governs how many options the company *can* grant based on stockholder-approved authorisation. Rule 701 is the external securities-law constraint that governs how much can be issued under the rule in a rolling 12-month window.

The pool can be much larger than the Rule 701 12-month cap. A 15%-post-close pool at a Series-B might be, e.g., 3M shares of a 20M FD company = 3M shares × $10 FMV = $30M of nominal value — well above the $10M disclosure threshold and possibly above the 15%-of-assets cap. The pool is the multi-year reserve; Rule 701 gates the annual burn rate.

Practically this means: at late stages, the CFO's grant-scheduling decisions might have to be paced to fit inside Rule 701's rolling window, even if the pool has capacity. A VP-level hire whose grant would blow the cap either gets a smaller grant (bad for recruiting), a phased grant (some now, some at the anniversary), or the CFO accepts triggering the $10M disclosure obligation and provides the financials.

## Summary

- Rule 701 is the '33 Act exemption private companies rely on for employee equity grants. The alternative is registration (impractical) or fitting each grant under a different exemption (also usually impractical).
- The aggregate cap is the greatest of $1M, 15% of total assets, or 15% of outstanding class-common in any rolling 12-month period. The CFO computes all three and picks the largest.
- Consumption is measured at the exercise price × shares underlying for options, at FMV × shares delivered for RSU settlements, and at purchase price × shares for restricted stock. The measurement is on a rolling 12-month basis.
- Above $10M / 12 months, the disclosure obligation triggers: a copy of the plan, risk factors, and financial statements (increasingly, audited) provided to each grantee before the grant.
- Failure modes — cap exceedance, missed disclosures, non-eligible grantees — create rescission rights and diligence problems. Fix by rescission offers, disclosure supplements, and re-issuing under other exemptions where applicable.
- Post-IPO, the company files a Form S-8 registering the equity plan and Rule 701 becomes irrelevant. Between the SEC-reporting trigger and the S-8 filing, there's a small dark window that requires special handling.
- The option pool is an internal share-authorisation constraint; Rule 701 is an external annual-burn-rate constraint. Both must be respected. Late-stage grants sometimes have to be paced to fit inside Rule 701 even when the pool has capacity.

Chapter 7 turns to the equity-compensation toolkit — ISOs, NSOs, RSUs, restricted stock, 83(b) elections, early-exercise programs, QSBS planning, and secondary-tender mechanics — the instruments that the pool, the 409A, and Rule 701 machinery ultimately serve.
