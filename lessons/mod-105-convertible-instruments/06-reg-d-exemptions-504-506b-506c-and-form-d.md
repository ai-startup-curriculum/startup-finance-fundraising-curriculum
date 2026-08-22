# Regulation D — Rules 504, 506(b), 506(c), and the Form D Filing

## Why this matters

Every SAFE, note, and preferred-round closing in the United States is an **offer and sale of securities** under the Securities Act of 1933. The default rule under Section 5 of the Securities Act is that any offer or sale must be registered with the SEC — a public-offering process that takes months and costs millions and that no seed-stage startup runs. Instead, every real seed closing relies on a **private-placement exemption** that lets the offering happen without SEC registration.

The dominant exemption regime is **Regulation D** (17 CFR §§ 230.500-230.508), a set of rules the SEC issued to give startups a safe harbour with specific compliance obligations. Under Reg D, a company can sell securities to accredited investors (and in some cases a limited number of non-accredited investors) without registration, subject to conditions on the offering and a Form D notice filing with the SEC.

A CFO who doesn't get Reg D right can:

- **Blow the exemption** — the offering falls outside the safe harbour and defaults to the Section 5 registration requirement it violated. Consequence: investors get a right of rescission (the right to force the company to buy back the securities for the money paid), the company faces potential SEC enforcement, and the founder loses substantial time and reputation cleaning up.
- **Miss the Form D deadline** — the notice filing is late (15 days after first sale), potentially costing the company a compliance certification the offering-safe-harbour depends on and triggering state-level notice failures too.
- **Verify accreditation wrong** — under Rule 506(c), the company must take "reasonable steps to verify" accredited status, not just accept an investor's self-certification. Getting this wrong under 506(c) blows the exemption.
- **Solicit generally when they can't** — Rule 506(b) prohibits "general solicitation and advertising" of the offering. Posting the fundraise on Twitter or on a public pitch deck can blow 506(b).

This chapter installs the three exemptions, the accredited-investor definition, the Form D filing mechanic, and the specific-choice decision tree the CFO uses at each raise.

## The three Rules — 504, 506(b), 506(c)

Reg D contains three exemption safe harbours a seed-stage company might use. (Rule 505 was repealed in 2016.)

### Rule 504 (17 CFR § 230.504)

Small-offering exemption. Currently caps aggregate offering size at **$10,000,000 in any 12-month period** (raised from $5M in 2021).

- Accredited-investor status not required — investors can be non-accredited.
- No specific general-solicitation prohibition in Rule 504 itself, but state "blue sky" laws typically still apply (see below) and often restrict general solicitation.
- Cannot be used by SEC-reporting companies, investment companies, or "blank-check" companies.
- Not integrated with Rule 506 offerings (see integration below).
- Rarely used in practice for seed rounds because state Blue Sky compliance is onerous compared to 506(b), which pre-empts state regulation for accredited-investor sales.

Most seed startups do not use Rule 504. The default choice is between 506(b) and 506(c).

### Rule 506(b) (17 CFR § 230.506(b))

The workhorse exemption. Used for the overwhelming majority of seed-stage raises, and specifically the default for most YC-style SAFE closings.

- **Unlimited raise size.** No cap on aggregate offering.
- **Unlimited accredited investors.**
- **Up to 35 non-accredited but "sophisticated" investors** allowed per offering. In practice, most startups avoid selling to non-accredited investors under 506(b) because the additional disclosure requirements are onerous. If a startup takes any non-accredited investors, it must deliver specific written disclosures — audited financials for the last two fiscal years, an offering memorandum with narrative, and other detail modelled on the S-1 registration statement. This is prohibitively expensive at seed. The practical rule: **only sell to accredited investors under 506(b)**.
- **No general solicitation or advertising.** The company cannot advertise the offering, cannot post it publicly, cannot use general marketing to solicit investors. The company must have a pre-existing substantive relationship with the investor (or the investor must have been introduced by a registered broker-dealer or by an investment adviser).
- **Accredited status verified by self-certification.** Investors typically sign a subscription agreement or investor questionnaire representing their accredited status. The company relies on that self-certification unless the company has knowledge that would make reliance unreasonable.
- **State-law preemption.** 506(b) offerings preempt state Blue Sky substantive regulation (National Securities Markets Improvement Act of 1996 — NSMIA — codified at 15 USC § 77r). The company still has to file state notice filings and pay state fees but does not have to substantively qualify the offering in each state.
- **Form D required** — 15 days after first sale (see below).
- **"Bad actor" disqualification** applies (Rule 506(d)) — certain individuals with disciplinary histories cannot be involved in the offering.

The 506(b) profile: accredited-only in practice, no advertising, minimal verification, Form D filed, state notices filed. This is the default for a founder-led seed round.

### Rule 506(c) (17 CFR § 230.506(c))

Added by the JOBS Act in 2013, effective September 2013. Solves the general-solicitation problem for accredited-only offerings.

- **Unlimited raise size.**
- **Only accredited investors permitted.** No non-accredited investors, ever, under 506(c). This is stricter than 506(b).
- **General solicitation and advertising permitted.** The company can advertise the offering — Twitter, LinkedIn, a public pitch deck, a mass email, a demo-day livestream, an AngelList post that any member of the public can see.
- **Accredited status must be verified by "reasonable steps"** — not self-certification. The company must take specific reasonable-verification steps such as:
  - Reviewing the investor's tax returns, W-2s, or brokerage statements for income or asset verification.
  - Obtaining a written certification from a licensed professional (attorney, CPA, registered broker-dealer, or SEC-registered investment adviser) that the investor is accredited.
  - Verifying against publicly available filings (e.g., 13F filings for institutional investors).
  - Using a third-party accreditation-verification service (VerifyInvestor, EarlyIQ, and similar).
  - The SEC has issued non-exclusive verification methods in Rule 506(c)(2)(ii); other methods qualify if they are reasonable under the specific circumstances.
- **State-law preemption.** Same as 506(b).
- **Form D required.**
- **"Bad actor" disqualification applies.**

The 506(c) profile: accredited-only, general solicitation OK, real verification required, Form D filed. Used when the company wants to publicly advertise the raise or use crowdfunding-style platforms (AngelList Syndicates and certain other platforms are 506(c)-based).

## The accredited investor definition (17 CFR § 230.501(a))

The accredited-investor definition, expanded in 2020, includes:

**Natural persons:**
- Individual income over $200,000 (or joint income with spouse or spousal equivalent over $300,000) in each of the two most recent years, with a reasonable expectation of the same in the current year.
- Individual net worth (or joint with spouse/spousal equivalent) over $1,000,000, excluding the value of the primary residence.
- **Holders of certain professional certifications, designations, or credentials** as designated by the SEC (currently: Series 7, Series 65, and Series 82 licence holders in good standing).
- **"Knowledgeable employees"** of certain private funds with respect to that fund.

**Entities:**
- Banks, insurance companies, registered investment companies, business development companies, small business investment companies.
- Employee benefit plans with plan assets over $5,000,000.
- Any entity in which all equity owners are accredited investors.
- Any entity with total assets over $5,000,000 not formed for the specific purpose of acquiring the securities offered.
- Family offices with assets under management over $5,000,000 and their family clients.
- Investment advisers registered under the Investment Advisers Act (SEC- or state-registered) and exempt reporting advisers.
- **Any entity that owns "investments" in excess of $5,000,000** (added in 2020).

The definition is broader than "rich person" — a small VC fund, a family office, or a corporate strategic investor can qualify under the entity limbs even if none of the individual principals are personally accredited under the natural-persons test.

The 2020 update also added the "knowledgeable employees" limb, the professional-credentials limb, and several entity-type expansions. Confirm the current SEC rule text (Rule 501) rather than relying on outdated summaries.

## Form D — the notice filing

**Filing obligation** (Rule 503 of Reg D). A company relying on Rule 504 or Rule 506 (b or c) must file a Form D notice with the SEC within **15 calendar days after the first sale** of securities in the offering. "First sale" means the first date on which an investor has become irrevocably committed to purchase and payment has been made (or the company has irrevocably committed to sell — subtly different in some interpretations).

**Filing method.** Form D is filed electronically through the SEC's EDGAR system (edgar.sec.gov). The company must first obtain EDGAR filer credentials (a Central Index Key — CIK — and access codes), which takes a few days if not already established. Filing Form D itself takes 15-30 minutes for a familiar filer, longer for a first-timer.

**Content of Form D.** The filing discloses:
- Company identity (name, jurisdiction, principal address, phone).
- Type of issuer (corporation, LP, LLC, etc.).
- Related persons (executive officers, directors, promoters, beneficial owners of 10%+ of any class of the issuer's equity).
- Type of Reg D exemption relied upon (504, 506(b), 506(c)).
- Type of securities offered.
- Whether the offering is intended to last more than one year.
- Aggregate offering price, aggregate amount sold to date, minimum investment accepted.
- Number of investors (accredited and non-accredited separately).
- Sales compensation paid to brokers/finders, if any.
- Use of proceeds category.
- Signature by an authorised officer.

**Amendments.** File a Form D amendment when material information changes — for example, when the offering closes and the total amount sold materially exceeds the amount originally reported. Annual amendments are required for offerings that stay open more than a year.

**State notice filings.** Each state where a purchaser resides typically requires a copy of the Form D and a state notice-filing fee (typically $100-$500 per state). Track state filings separately from the federal Form D; use a paralegal or a service like COGENCY Global or CT Corporation for state notice filings if selling across many states.

**Consequences of missing the deadline.** The SEC does not automatically blow the Reg D exemption for a late Form D — the specific safe-harbour text is in Rule 507, which imposes disqualification only after a court injunction against the specific failure. But: (a) states may treat their notice-filing deadline as a specific-compliance condition of state-law exemption, (b) the SEC has issued guidance that a pattern of late or missed filings can weigh against exemption reliance, and (c) later diligence firms often flag missed Form D filings as an issue that requires remediation.

## Choosing 506(b) vs. 506(c) — the decision tree

The choice between 506(b) and 506(c) is driven almost entirely by whether the founder wants to advertise the raise.

**Choose 506(b) when:**
- The founder is running a private, relationship-based fundraise. Investors are introduced through the founder's network, YC network, existing investors, or a registered broker-dealer.
- The founder has not tweeted about the raise, has not posted the pitch deck publicly, has not spoken about the specific offering on a podcast (some grey area — general "we're fundraising" comments are usually fine; specific "we're raising $X at $Y cap and here's how to invest" is a general solicitation).
- The founder plans to take money only from accredited investors that the founder or the founder's counsel can verify by self-certification.
- The founder is not using AngelList Syndicates, Republic, or any similar crowdfunding-style platform for the offering (most of those are 506(c)-based).

**Choose 506(c) when:**
- The founder is publicly promoting the raise — tweets about it, publicly-posted pitch deck, mass emails, demo-day livestream.
- The founder is using AngelList Syndicates, Republic, or a similar platform where the deal is exposed to platform members who are not in a pre-existing relationship with the company.
- The founder wants to solicit an audience beyond the founder's direct network.

**The transition risk.** A company can start on 506(b) and later switch to 506(c) (or vice versa) but must be careful about the sequence. Once general solicitation has occurred, all subsequent sales in the same offering must be under 506(c). A company that solicits generally and then tries to fall back on 506(b) has blown the 506(b) exemption for the subsequent sales because the earlier solicitation is imputed. Practical rule: pick one exemption per offering and stick with it. Related SEC guidance is at Compliance and Disclosure Interpretations (C&DIs) 260 and following.

**Integration.** Multiple offerings by the same company may be "integrated" into a single offering for exemption purposes, meaning restrictions from one offering apply to another. The SEC substantially reformed integration in 2020 (Rule 152) — the general rule is that offerings more than 30 days apart, or offerings that use different exemption paths in an ordered sequence, are typically not integrated. But this is a fact-specific determination; confirm with counsel before running two closings back-to-back under different exemptions.

## Bad-actor disqualification (Rule 506(d))

Rule 506 (both (b) and (c)) prohibits reliance on the exemption if any of the following "covered persons" is subject to a "disqualifying event":

- The company itself.
- Any director, executive officer, general partner, or managing member of the company.
- Beneficial owners of 20% or more of any class of the company's outstanding voting equity.
- Any promoter of the company connected in any capacity with the sale of the securities.
- Any investment manager, general partner, or managing member of a private fund that is a related party.
- Any compensated solicitor of investors for the offering, plus their principals.

"Disqualifying events" include SEC or state securities-regulator injunctions, court orders, administrative bar orders, criminal convictions relating to securities activities, and other similar findings. Full list at Rule 506(d)(1). The disqualification is 5-10 years long depending on the event.

Practical implication: at seed and Series-A, run a "Rule 506(d) bad-actor questionnaire" through every director and 20%-plus stockholder. If any covered person has a disqualifying event, the company must either (a) rely on the reasonable-care exception (Rule 506(d)(2)(iv)) — the company took reasonable care and did not know and could not have known — or (b) apply to the SEC for a waiver, or (c) restructure the offering to remove the disqualified covered person.

## Beyond Reg D — briefly

Reg D is the dominant seed-stage regime. A CFO should also know these adjacent regimes exist and defer to counsel on which applies:

- **Rule 701** — offering-exemption for equity compensation to employees, directors, consultants. Not applicable to fundraising offerings but adjacent — governs option grants under an equity incentive plan. Chapter 6 of [`mod-104`](../mod-104-cap-tables-and-equity-compensation/06-rule-701-caps-and-form-s-8-graduation.md) covers 701 in detail.
- **Regulation Crowdfunding (Reg CF)** — 17 CFR §§ 227.100+. Allows sales of up to $5,000,000 per 12 months to non-accredited investors via SEC-registered funding portals. Rarely used at YC-style seed stage but shows up in some consumer-brand and hardware raises.
- **Regulation A / Regulation A+** — a "mini-IPO" for offerings up to $75M with SEC-qualified offering statement. Not seed-stage; rare for venture-backed startups.
- **Section 4(a)(2)** — the statutory private-placement exemption (not a rule under Reg D). Reg D is a safe harbour under 4(a)(2). Some offerings that don't fit inside a Reg D safe harbour may still qualify under the 4(a)(2) statute directly, but the analysis is fact-specific and less reliable than fitting inside Reg D.
- **State-only offerings** — some very small closings may qualify under state-level exemptions alone (e.g., a single-state closing to a single accredited investor for a small amount). These do not preempt federal law, so must still fit inside a federal exemption. Rarely used for seed-stage venture rounds.

## The seed-round compliance checklist

For each SAFE, note, or preferred-round closing:

- Confirm the exemption chosen (Rule 506(b) is the default for private, network-only raises; 506(c) if publicly advertised).
- Collect an investor questionnaire from each investor confirming accredited status (self-certification for 506(b)) or run verification for 506(c) (documented reasonable steps).
- Confirm no general solicitation has occurred if relying on 506(b). If in doubt, ask counsel.
- Run the bad-actor questionnaire on every covered person.
- Prepare and file Form D within 15 days of first sale.
- Prepare and file state notice filings within each state's required window (varies by state — many are also 15 days from first sale).
- Log the closing in the corporate record with references to the SAFE / note instrument, the subscription agreement / investor questionnaire, the Form D filing acknowledgment from EDGAR, and the state notice-filing confirmations.

## Common founder traps

- **Tweeting "we're raising a seed round" without thinking about 506(b) vs. 506(c).** A tweet that says "we're raising a $2M seed at a $15M post-money cap, DM if interested" is a general solicitation and forces the offering onto 506(c) (and forces verification). A tweet that says "we're a company doing X and we're growing quickly" is usually not a general solicitation of a specific offering. The line is fact-specific.
- **Accepting an investor without confirming accredited status.** Under 506(b) self-certification is fine but must actually be collected. Under 506(c) verification is required and cannot be waived.
- **Missing the 15-day Form D deadline.** The most common Reg D compliance failure at seed. Set a calendar reminder at first-sale-plus-14-days.
- **Assuming Form D covers state filings.** It does not. Each state where an investor resides may require a separate notice filing, and each has its own deadline and fee.
- **Running two closings back-to-back under different exemptions without an integration analysis.** A 506(b) closing followed 20 days later by a 506(c) closing may be integrated by the SEC into a single offering, which blows the 506(b) portion.
- **Selling to a non-accredited investor under 506(b) without the required disclosures.** Even one non-accredited investor triggers the disclosure obligations, which are cost-prohibitive at seed. Just stick to accredited-only.
- **Bad-actor problems discovered at Series A.** If the seed round had a director who had an old SEC bar order and no one asked, the seed offering may have been non-exempt. Series-A diligence catches this; remediation is expensive.

## What good looks like

A CFO or founder running Reg D compliance:

- Chooses **506(b) as the default** and **506(c) only when general solicitation is intended**. Never 504 for a venture-scale seed.
- Uses a **subscription-agreement template** (or the counsel-supplied form) that includes an investor questionnaire, accredited-status representation, bad-actor questions if the investor is a fund whose principals are covered persons, and jurisdiction consent.
- **Files Form D within 15 days of first sale**, every time, with a calendar reminder set at closing.
- **Files state notice filings** for every state where an investor resides, tracked in a compliance log.
- Runs a **bad-actor screen** on every director, officer, promoter, and 20%+ holder.
- **Distinguishes between general talk about fundraising and specific solicitation** and, when in doubt, gets counsel's opinion before posting.
- **Maintains a per-closing compliance file**: SAFE / note instruments, subscription agreements, investor questionnaires, Form D filing acknowledgments, state notice-filing confirmations, bad-actor questionnaires, and any verification documentation (for 506(c)).

## Summary

- Every SAFE, note, and preferred-round closing is a securities offering that requires a private-placement exemption from Section 5 of the Securities Act. The dominant regime is Regulation D.
- Reg D has three current rules: 504 (small-offering, up to $10M in 12 months, rarely used for venture rounds); 506(b) (unlimited raise, accredited-only in practice, no general solicitation, self-certification of accreditation); 506(c) (unlimited raise, accredited-only, general solicitation permitted, verified accreditation required).
- The accredited-investor definition (Rule 501) covers natural persons above income or net-worth thresholds, holders of certain professional certifications, and a broad range of entity types.
- Form D must be filed with the SEC within 15 calendar days after first sale of securities. State notice filings are separate.
- Choose 506(b) as the default for private network-based raises; 506(c) when the raise is publicly advertised or run through a solicitation platform. Do not mix exemptions across integrated offerings.
- Rule 506(d) bad-actor disqualification requires screening all covered persons for disqualifying events.

Chapter 7 turns to the specific failure modes of convertible-instrument programmes — SAFE overhang, mixed pre-/post-money stacks, notes maturing without a QF — and the prescribed remediation for each.
