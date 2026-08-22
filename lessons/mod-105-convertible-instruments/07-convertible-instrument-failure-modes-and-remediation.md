# Convertible-Instrument Failure Modes and Remediation

## Why this matters

The convertible-instrument playbook — SAFEs, notes, MFN side letters, Reg D compliance — has a small number of characteristic ways it goes wrong. Every one of them is diagnosable from the cap table and the instrument register, and every one has a specific remediation the CFO can propose. What separates a defensible priced-round pro-forma from a chaotic one is whether the CFO has identified and remediated these failure modes before the diligence firm finds them.

This chapter catalogues the three most common failure modes and prescribes the fix for each. Each one has been mentioned across chapters 1-6; this chapter is where they get treated as their own topic with a specific remediation playbook.

## Failure mode 1 — the SAFE overhang

**Definition.** The SAFE overhang is the arithmetic problem that arises when the aggregate `investment / cap` percentage across the SAFE stack exceeds what the founder intended to sell at the priced round. The SAFE holders' collective slice — computed as the sum of `investment / cap` across all post-money SAFEs — is a lower bound on their combined post-conversion ownership. If that lower bound is much larger than the founder anticipated when signing the SAFEs, the founder-post-priced-round percentage is materially smaller than they planned.

**Diagnosis.** Compute `Σ (investment_i / cap_i)` across all post-money SAFEs on the table. This is the SAFE-holder aggregate percentage of the pre-new-money post-conversion company. Compare to the founder's intended-sold-to-SAFE-holders percentage. A gap of more than 5 percentage points is meaningful. A gap of more than 15 percentage points is a real problem.

**How it happens.** The founder signs several SAFEs over an 18-24 month seed programme without maintaining a live aggregate. Each SAFE at signing looks reasonable — $500K at $10M cap is 5% on that SAFE's line. Six SAFEs at similar terms is 30% on the SAFE holders' aggregate line. Add another SAFE from an angel who insists on a $6M cap for a $500K cheque — that alone is 8.3%. Now the SAFE stack is at 38-40% of the post-conversion company. The priced round adds another 20-25%. The pool is 10%. The founder is at 25-30% at Series-A close, when the founder had been mentally modelling 45-50%.

The overhang is invisible one closing at a time. It becomes visible only in the pro-forma (chapter 4). Founders who don't maintain a live aggregate `Σ (investment / cap)` after each SAFE closing walk into the priced round without seeing it coming.

**Consequences.**

- **Priced-round terms get renegotiated.** The lead investor, seeing the pro-forma, may push back on the round size (lower cheque means less new-money dilution) or on the pool target (lower pool means less pool dilution). Neither materially improves the founder's outcome — the SAFE overhang is already there. What the negotiation actually shifts is small amounts across the pool and the priced-round investor.
- **The lead may condition the round on renegotiating the SAFEs.** In extreme cases the lead will require SAFE holders to accept an amendment (a higher cap, a discount rollback, or a conversion to common at a lower valuation) as a condition of closing. This is a negotiation with each SAFE holder individually and requires their consent. Some will agree; some will not; the SAFE holders who refuse hold up the round.
- **The founder walks away from the term sheet or restructures the round.** In the worst case, the founder can't get to a stack that the incoming investor is willing to price, and the round doesn't close. The company then continues on runway, potentially raising a bridge note to buy time, which adds to the overhang.

**Remediation.**

- **Prevention is the primary remediation.** Maintain a live SAFE register (chapters 1 and 4) with a running `Σ (investment / cap)` calculation updated after every closing. Set an internal ceiling — commonly 20-25% aggregate SAFE-holder slice — beyond which the founder does not close additional SAFEs without renegotiating one of the existing ones (usually by asking earlier holders to accept a higher cap in exchange for something).
- **When overhang is already in place**, the remediation options are:
  - **Increase the priced-round valuation.** A higher pre-money means the SAFE holders' fixed slice (in post-money percentage terms) shrinks, since `investment / cap` is a fixed percentage of pre-new-money and pre-new-money is a smaller fraction of a larger post-money. Marginal but real.
  - **Ask SAFE holders to accept an amendment.** Common asks: raise the cap by X% in exchange for pro-rata rights the SAFE holder doesn't currently have; extend the SAFE's participation into a follow-on with side-letter guarantees; or convert to common at a specified price if the holder is willing. Requires each SAFE holder's consent. Uncertain outcome.
  - **Do a "SAFE cleanup" round.** Some companies do a small preferred round specifically to convert the SAFEs at a mutually agreed valuation, cleaning up the stack, and then run the "real" priced round from a cleaner cap table. This is a two-step approach that some investors find awkward but that can preserve founder ownership better than converting a chaotic stack.
  - **Change instruments going forward.** If more capital is needed and the SAFE stack is already at the ceiling, take the next cheques as small preferred issuances (a mini Series-Seed) rather than more SAFEs. This fixes the ownership at a specific priced number rather than adding to the overhang.
  - **Walk from the round.** If the overhang plus the priced-round terms don't produce a founder outcome the founder can live with, don't close. Extend runway on other capital and re-price at a subsequent round.

- **After the priced round**, the overhang is cemented. The founder's percentage is what it is. The lesson for the next fundraise: maintain the register, respect the ceiling, and monitor cumulative SAFE percentage aggressively.

## Failure mode 2 — mixed pre- and post-money SAFEs on the same table

**Definition.** Some SAFEs on the table are pre-money legacy (chapter 2), some are post-money (chapter 1). The two mechanics interact at conversion in a way that most founders and many junior counsel do not model correctly.

**Diagnosis.** Read each SAFE's form. If the "SAFE Price" definition references "Pre-money Valuation Cap" and includes shares "issuable pursuant to this SAFE" but excludes shares issued in the priced round, the SAFE is pre-money. If the definition references "Post-money Valuation Cap" and the company capitalisation includes all converted SAFEs and notes, the SAFE is post-money. Any SAFE closed before mid-2018 is almost certainly pre-money.

**How it happens.** A founder starts fundraising in 2017 and closes two pre-money SAFEs. In 2019 they close three more using the then-current post-money form, not noticing that the mechanic is different. Or a founder receives a template from a non-YC investor that was based on a pre-money form and continues using it after 2018. Or an angel sends a "SAFE" they had lying around from a previous investment and it turns out to be a 2015 pre-money vintage.

**Consequences.**

- **The pro-forma conversion arithmetic gets much harder.** A single-formula computation is wrong; you must run the pre-money SAFEs through the pre-money mechanic and the post-money SAFEs through the post-money mechanic in the same solve. Chapter 4's stack was all post-money; adding pre-money SAFEs requires a system of equations.
- **The founder outcome differs from either homogeneous case.** Under an all-pre-money stack, the SAFE holders share the priced-round dilution with the founder. Under an all-post-money stack, the SAFE holders do not. Under a mixed stack, the post-money SAFE holders don't share the priced-round dilution but the pre-money SAFE holders do — meaning the pre-money SAFE holders effectively subsidise the post-money SAFE holders at the priced round. The pre-money SAFE holders often notice this at closing and complain.
- **Diligence attorneys sometimes flag the inconsistency itself as a governance issue.** "Why does this company have three different SAFE mechanics on its table?" is a signal of casual documentation practice that leads to other errors.

**Remediation.**

- **Ideal fix (before the priced round): convert the pre-money SAFEs to post-money.** This requires the pre-money SAFE holder's consent — the amendment is bilateral. In exchange for the conversion, the founder typically offers the SAFE holder a modest cap improvement or a pro-rata right. The mechanics of the conversion: rewrite the SAFE's "SAFE Price" definition to be based on the post-money cap that produces the same effective share count at the current pre-money FD; document the amendment as a signed instrument.
  - This works cleanly only if the pre-money and post-money share counts can be reconciled at the current denominator. If new SAFEs have been added since the pre-money SAFE was signed, the pre-money holder's implied percentage has already shrunk; converting to post-money "freezes" them at that shrunken percentage. The pre-money holder may not want to accept this.
- **Alternative fix (at the priced round): run both mechanics in the pro-forma, disclose the mixed treatment openly.** This is not a remediation of the underlying inconsistency but is the honest approach. The CFO explicitly identifies each SAFE as pre- or post-money in the pro-forma, runs both mechanics, and produces the resulting shares. The lead's counsel red-lines the closing docs to match.
- **Prevention going forward.** Standardise on the current YC post-money SAFE for all new closings. If an investor sends a non-YC template, either (a) convince them to switch to a post-money form or (b) confirm the mechanic they intend and document it explicitly. Do not accept a form without reading which mechanic it uses.

## Failure mode 3 — notes converting at maturity because no qualified financing happened

**Definition.** A convertible note reaches its maturity date. The qualified financing that was supposed to trigger conversion has not happened. The note's maturity mechanic fires. This may or may not be economically catastrophic for the founder depending on what the note's maturity clause says.

**Diagnosis.** For every note on the cap table, log the maturity date and compare it to the current date and to the expected priced-round close. Any note whose maturity precedes the expected priced-round close by less than 6 months is a candidate for this failure mode. Any note whose maturity has already passed without conversion is already in the failure mode.

**How it happens.** The founder signs an 18-month note in month 6 of the fundraise, expecting the priced round to close by month 12. The priced round slips to month 24. Now the note has 6 months of maturity runway left; the priced round is another 6 months out. The maturity hits before conversion.

Alternative pathway: the "priced round" that eventually closes is smaller than the QF threshold in the note. The note doesn't automatically convert; the note-holder has a choice (voluntary conversion at the sub-QF price, or stand on the note and wait). If they stand on the note and the note has already matured, the situation is the same.

**Consequences.**

- **Repayment demand.** The note-holder demands cash repayment of principal plus accrued interest. Most seed-stage companies do not have this cash. If they do not pay, the note-holder has a debt claim they can enforce through the courts (rare in practice for seed-stage notes, more common in later-stage venture debt).
- **Automatic maturity conversion at a fallback formula.** Some notes convert automatically at maturity into common (or preferred) at a stated fallback price or valuation. These conversions are typically punitive to the founder — the fallback valuation is set low, so the note-holder gets a large slug of shares (chapter 3 walked a specific example).
- **Extension negotiations.** The most common real-world outcome. The founder asks the note-holder to extend maturity by 6-12 months in exchange for something — a cap reduction, a discount increase, an interest-rate bump, sometimes pro-rata rights. The negotiation happens from a position of relative weakness for the founder because the note-holder can force one of the two outcomes above if the extension isn't attractive.
- **Cross-default with other financing.** If the company has other debt (a venture-debt facility, another note), the note default may trigger cross-default provisions in those instruments, cascading the problem.

**Remediation.**

- **Prevention is the primary remediation, again.** At signing, set the maturity date with a buffer of at least 6 months past the expected priced-round close. If the expected close is 12 months out, sign a 24-month note. If the expected close is 18 months out, sign a 30-month note. Founders who sign 18-month notes when their priced round is 15 months out are asking for the failure mode.
- **Monitor maturity dates against runway forecast.** Every board deck should include a note-maturity table. If any note's maturity is within 12 months and the priced round isn't imminent, start the extension conversation early — preferably 90+ days before maturity — rather than at the deadline.
- **When maturity is close and no QF is imminent**, the standard playbook:
  - Approach the note-holder early and in good faith.
  - Propose a **maturity extension** of 12-18 months.
  - Offer specific consideration — commonly a modest cap reduction (10-20%), an interest-rate bump (from 6% to 8% or from 8% to 10%), or an additional pro-rata right.
  - Do *not* offer a conversion to common at a low fallback valuation. That is worse for the founder than the extension.
  - Document the extension as a signed amendment.
- **If the note-holder refuses to extend and demands repayment**, the options are:
  - **Repay from cash.** If the company has the cash, pay off the note. Recomputes runway.
  - **Refinance with another note or SAFE.** Raise a new instrument specifically to repay the old note. Adds to the overhang (failure mode 1) but retires the maturity clock.
  - **Convert to common at the fallback price if the note has that mechanic.** Founder-adverse but avoids default.
  - **Accept the default and negotiate under duress.** Rarely a good outcome. The note-holder now has legal leverage.
- **If the note has already matured without action**, the negotiation is entirely under the note-holder's control. The founder should engage counsel immediately and structure the remediation as a signed amendment (extending maturity retroactively, or converting the note to common on renegotiated terms).

## Adjacent failure modes worth naming

Three more failure modes that appear less frequently but merit mention:

**Failure mode A — MFN cascade the founder didn't model.** A later SAFE at a lower cap triggers MFNs on multiple earlier SAFEs. The founder never modelled the cascade before signing the later SAFE. The priced-round pro-forma reveals the earlier SAFEs have shifted terms. Diagnosis: any active MFN on an earlier SAFE, plus a later SAFE with better terms. Remediation: run the cascade check before every SAFE closing (chapter 5); if the cascade would trigger, price it into the trade or renegotiate the MFN before the new closing.

**Failure mode B — Reg D exemption blown by general solicitation.** The founder tweeted about the specific offering, or posted the deck publicly, or the raise went through a platform that solicits members generally, and the offering was on 506(b) rather than 506(c). Diagnosis: any public solicitation of the specific offering on a 506(b) raise. Remediation: file a rescission offer to affected investors, pause fundraising for a "cooling off" period (integration analysis under Rule 152), and re-open under 506(c) with verified accreditation for the balance of the raise.

**Failure mode C — Late Form D.** The 15-day filing deadline passed without a Form D on file. Diagnosis: EDGAR shows no Form D for the offering; the offering has closed sales. Remediation: file the Form D immediately, note the lateness, engage counsel on state notice-filing corrections. The federal exemption is not automatically blown by a late federal Form D (Rule 507 disqualification requires an injunction), but the state situation varies.

**Failure mode D — SAFE stack with an underlying instrument that isn't a SAFE.** A "SAFE" that on inspection is a bespoke convertible instrument with meaningfully different mechanics than the YC template. Diagnosis: read every SAFE, don't assume homogeneity. Remediation: model the actual mechanic, disclose it in the pro-forma, and consider whether to amend the instrument into a standard form before the priced round.

## The remediation-readiness checklist

Before the priced-round pro-forma is finalised:

- **SAFE overhang check.** `Σ (investment / cap)` across post-money SAFEs; sum of pre-money SAFE percentages against a common denominator; total combined SAFE percentage; comparison against the founder's intended ceiling.
- **Mixed-stack check.** Per-SAFE form identification (pre- or post-money); count of each; explicit pro-forma treatment of both mechanics.
- **Note maturity dashboard.** Per-note: principal, interest rate, accrued interest at closing, maturity date, QF threshold, whether QF is being triggered at this priced round.
- **MFN cascade check.** For each SAFE with active MFN, has any subsequent SAFE triggered the MFN? What are the effective terms after cascades? Does the pro-forma reflect them?
- **Reg D compliance check.** For each SAFE and note closing, Form D filed on time; state notice filings complete; bad-actor questionnaires collected; exemption chosen and consistently applied.
- **Corporate record reconciliation.** Every SAFE, note, and side letter tied to a signed instrument in the corporate record; nothing on the pro-forma without an underlying instrument.

## What good looks like

A CFO or founder with the failure modes on their radar:

- Maintains a **SAFE and note register** with all fields needed for the overhang, mixed-stack, and maturity checks (variant, cap, discount, MFN flag, side-letter flag, form pre- or post-money, principal, interest rate, maturity date, QF threshold, closing date, Form D filing status).
- Sets an **overhang ceiling** at the start of the seed programme (commonly 20-25%) and does not close SAFEs that would breach it without renegotiating the stack.
- **Runs the pro-forma quarterly**, not just before the priced round. This surfaces failure modes early enough to remediate them.
- **Reads every convertible before signing** and does not accept "just use the template" without confirming which template.
- **Talks to counsel early** about any non-standard structure, any planned public solicitation, or any note approaching maturity.
- **Documents amendments and extensions with signed instruments**, not with a handshake or an email exchange. Every change to the stack is a corporate record entry.

## Summary

- Three characteristic failure modes of the convertible-instrument playbook: SAFE overhang (aggregate SAFE percentage exceeds the founder's intended sold-to-SAFEs slice), mixed pre- and post-money SAFEs on the same table (two mechanics interacting in the same conversion), and notes converting at maturity because no qualified financing happened (maturity fires and the note enters repayment / fallback conversion / extension).
- Each failure mode is diagnosable from a properly-maintained SAFE and note register. The primary remediation for all three is prevention: maintain the register live, run the pro-forma regularly, monitor overhang against a set ceiling, standardise on the current post-money SAFE for new closings, and set note maturity dates with a real buffer past expected priced-round close.
- When failure modes are already in place, the remediation involves signed amendments (SAFE cap changes, note maturity extensions, form-switch amendments) that require the counterparty's consent and typically cost the founder specific consideration.
- Adjacent failure modes (MFN cascades, Reg D exemption failures, late Form D filings, bespoke SAFEs mis-treated as YC forms) show up less often but require the same discipline: read the actual instruments, run the actual cascade, file the actual form, disclose the actual mechanics.
- The remediation-readiness checklist is the pre-closing sanity check that catches all of these before the diligence firm does.

This closes the mod-105 chapter set. Chapter 4 of [`mod-106`](../mod-106-startup-valuation-frameworks/) picks up the valuation-cap-as-de-facto-ceiling thread from here; [`mod-108`](../mod-108-term-sheets-and-preferred-stock-economics/) picks up the priced-round preferred-stock terms that these convertibles convert into.
