# Recapitalisations, Cram-Downs, and Common-Employee Re-Up Grants

## Why this matters

Pay-to-play and senior-preference stacking (chapter 3) work when the existing preferred stack is small enough, the story is credible enough, and the incoming-lead terms are moderate enough that the majority of existing investors will participate. When those conditions don't hold — because the preference stack is very deep after several rounds, because the incoming lead is only willing to underwrite a much smaller company, because a subset of existing investors will actively block instead of accept a shadow-preferred outcome — the CFO reaches for the harder tools: a **recapitalisation** that collapses the existing preference stack entirely, a **cram-down** that overrides holdout investors through the exercise of drag-along and other charter mechanics, and a **common-employee re-up grant programme** that restores the option holders' economic upside after either mechanic reshapes the cap table.

None of these is a first-choice tool. They are the toolkit of last resort before the alternatives in [`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum) — a sale process, an orderly wind-down, an assignment for the benefit of creditors (ABC). The CFO's job is to know the mechanics well enough to work through them cleanly when they are the right tool, and to run the parallel human-and-communication work that makes them survivable for the team.

## Recapitalisation — the mechanic

**The concept.** A **recapitalisation** ("recap") restructures the entire cap table, most commonly by converting all existing preferred to common at defined ratios (or by cancelling and re-issuing at meaningfully changed terms), so that the incoming financing lead is not underwriting into a deep preference stack. The company effectively wipes the preferred and starts fresh with the incoming lead's new preferred class as the top (and often only) preferred tier.

**Why this is sometimes the only option.** A cumulative preference stack of $50M or $100M across a Series-A, B, and C weighs on every subsequent price and every subsequent recovery calculation. An incoming lead asked to underwrite a $10M down-round Series-D on a company whose existing preference stack is $80M knows that any sale below $90M returns almost nothing to the incoming lead's common holders and returns very little to the incoming lead's preferred either (because the participating preference of the existing stack, if any, eats into the exit). Recapitalising — collapsing the $80M stack — is the only way to make the underwriting work.

**The mechanics.**

- The charter is amended to convert each existing preferred series to common at defined ratios. The ratios are the primary negotiation lever: 1:1 conversion (existing preferred becomes common share-for-share) is the founder-favourable extreme; a converted-at-a-fraction ratio (each existing preferred share becomes 0.5 or 0.25 of a common) is the incoming-lead-favourable extreme.
- Alternatively, some existing preferred is offered the choice to convert or to accept a **shadow preferred** with materially reduced rights (nominal 1x preference, no participation, no anti-dilution, no protective provisions) plus optional add-on economics (a warrant coverage on the recap, a right to invest in the next round at a discount).
- The new preferred class from the incoming lead is issued at the recap-priced pre-money, senior to whatever residual preferred remains.
- Existing investors who declined to participate in the recap can be forced through the mechanisms below.

**The vote and consent choreography.** The recap requires:

- Approval of the charter amendment. Class votes required per each existing series' protective provisions. If any single existing series has a supermajority requirement, the CFO must line up that supermajority in advance.
- Approval of the definitive agreements. Same board and preferred consents as any priced round.
- Rescission or amendment of registration rights, information rights, and other IRA-embedded rights that would otherwise pass through unchanged. Existing investors that will be materially reshaped by the recap sometimes hold IRA rights that need explicit amendment.
- A drag-along or specific tag-along consent, if the recap resembles a sale mechanically (some recaps use the drag-along machinery to force the outcome — see the cram-down section below).

The choreography is high-stakes. Missing a required vote or class-vote sub-threshold blocks the recap. The CFO's job is to identify every vote gate in advance and to have a documented commitment from the necessary holders before the term sheet is signed.

## Recapitalisation — the trade-offs

**For the incoming lead.** Positive: clean top-of-stack. Negative: has to fund the additional dilution needed to compensate the founders and employees for their disproportionate share of the reset (the "management retention pool" that usually accompanies a recap — see the common-employee re-up section below).

**For the participating existing preferred.** Positive: they get to write a check into a lower-valuation next round with better economics per dollar than the last round provided. Some participation offsets the value they wrote off in the recap. Negative: they take a real mark on the existing shares.

**For the non-participating existing preferred.** Negative on all axes. Their preferred is collapsed (or, in a cram-down, cancelled) with reduced or no seniority. They have no option to write a check in at the new lower price without also participating in the recap on the reduced terms. They frequently pursue litigation (rare in practice) or bad-actor blocking (more common in the near term).

**For the founders and employees (common holders).**

- Positive: elimination of the preference overhang means common recovers value at meaningfully lower exit prices than under the pre-recap stack.
- Positive: management retention pools (the common re-up section) restore the option upside to a level that is meaningful for team retention.
- Negative: the ownership on the pro-forma cap table has been reset — the founders end up with a much smaller percentage on a much smaller-valuation company. This is a painful mark that requires honest communication and a real story about what the recap unlocks.

**Signalling and follow-on-fundraising consequence.** A recap is a strong distress signal to the market. The company that has recap'd once will be scrutinised heavily in subsequent fundraises for whether the recap actually reset the underlying trajectory. Recaps that work — the KPIs turn, the company grows into the reset valuation, the next round prices above the recap — are recoverable events, and the market will eventually forget them. Recaps that do not are followed by a sale process (chapter 8 handoff), not a next round.

## Cram-down — the mechanic

**The concept.** A **cram-down** forces the recap or the down-round terms on non-consenting holders using the charter's drag-along, majority-vote, or blank-check-preferred mechanics, so that the transaction closes even without their affirmative consent. In effect, the majority uses pre-agreed mechanisms to override the minority.

**The tools.**

- **Drag-along.** The Voting Agreement's drag-along (mod-108 chapter 8) is drafted for a "sale of the company," but in some drafts includes charter-amending recapitalisations that are the economic equivalent of a sale. If the drag-along fires — typically triggered by a majority of preferred plus a majority of common (or a specified subset) approving a defined transaction — the minority is obliged to vote in favour and to sign the definitive documents.
- **Majority preferred vote.** Some protective provisions require only a majority (not a supermajority) of the preferred class. If the majority favours the recap, the class vote passes over minority opposition.
- **Blank-check preferred.** Some charters authorise a large pool of "blank-check" preferred that the board can designate and issue without a separate shareholder vote. The board can use this to issue a new senior preferred class with terms that effectively cram down the existing preferred — the existing preferred is now junior to a class it did not vote on.
- **Reverse stock split combined with a re-issuance.** A large reverse stock split (say 1000:1) followed by a fresh issuance of preferred and common leaves the pre-split holders holding fractional shares that get rounded down to zero. This is aggressive and pursued only under specific charter authority. Rarely used.

**When cram-downs are needed.** The most common trigger is a small holdout — one or two funds that will not participate and will not consent, but that hold enough shares to block a charter amendment under a supermajority requirement. If the economic case for the recap is strong (the alternative is the company runs out of cash), the CFO and counsel use the available cram-down tools to force closure.

**Litigation risk.** Cram-down mechanics carry real litigation risk. Directors owe fiduciary duties to the common shareholders (and often to disinterested preferred as well). A recap or cram-down structured to unfairly benefit insider-participating investors at the expense of non-participating investors and common can be challenged under Delaware fiduciary-duty doctrine (the *Trados* line of cases is the standard reference). The CFO's job is to work with counsel to ensure the process meets the standards that entire-fairness or business-judgment review would apply — independent director approval, fairness opinion where warranted, pro-rata participation right offered to all existing preferred, market-terms comparable data supporting the pricing.

## Common-employee re-up grants — the mechanic

**The concept.** After a down round or (especially) a recap, the option pool is meaningfully out-of-the-money — the strike prices on outstanding options were set when the fair market value was materially higher, and the options are now underwater. The employees who hold them have lost their equity motivation. A **re-up grant** issues new options at the current (lower) fair market value, either as new grants stacked on top of the underwater existing grants, or as a re-strike that resets the strike price of existing grants to the new FMV.

**The mechanics.**

- **New-grant re-up.** New options granted at the new post-recap 409A FMV. Simpler mechanically; the underwater options continue to exist and expire on schedule. The employee's total grant count increases, which requires the recap term sheet to include an option-pool top-up sized to support the re-up plus normal ongoing hiring.
- **Option repricing / re-strike.** The board formally reduces the strike price of the existing options (usually to the new post-recap FMV). Requires shareholder approval in some cases (NYSE / Nasdaq rules for public companies; some private-company charters require it as well). Creates accounting expense (variable-accounting rules or ASC 718 modification-accounting rules). The underwater options are now at-the-money again with no dilution beyond the pre-existing grant.
- **Exchange programme.** Employees exchange N underwater options for M new options (M usually < N) at the new FMV. Balances dilution against employee motivation. Requires careful design to avoid discouraging participation.

**Sizing.** The typical management retention pool that comes with a recap is 10-20% of the post-recap fully-diluted cap table, sometimes higher. That size is negotiated with the incoming lead as part of the term sheet — the lead's incentive is to keep it as small as possible; the CFO's incentive is to make it large enough that the team stays and grows. The founder-specific portion of the pool (a "founder re-up") is often carved out separately with explicit performance vesting tied to milestones the incoming lead needs the founder to hit.

**Vesting.** Re-up grants use fresh 4-year vests with 1-year cliffs, typical of any new grant. Sometimes performance vesting is layered on top (grant vests on hitting a specific ARR milestone or on a specific successful next round). Cliffs are usually necessary — a re-up grant given the day of the recap that vests over four years reads to the employees as "the leadership is committed to the next four years," which is exactly the signal the recap needs.

**409A revaluation.** The recap resets the fair market value of the common. The 409A appraisal has to be updated (or the company relies on the recap transaction itself as the market-tested FMV under the appropriate 409A safe harbour). New grants use the new FMV. If the FMV has dropped meaningfully (which it usually will after a recap), the new grants are at a lower strike, which is exactly the intent — the employees get options that are worth exercising and are at-the-money.

**Communication.** The re-up programme has to be communicated to the team in the same conversation as the recap. Employees who learn about the recap on Monday and the re-up on Friday spent four days demoralised needlessly. The founder and CFO deliver both messages together: "here is what has happened to the cap table, here is why, here is what we have done to make sure the team's economic upside is restored, here is what the new grant looks like for you."

## The human-and-legal work list

For a company going through a recap and re-up simultaneously, the CFO's work list is:

**Legal.**
- Term sheet negotiation with incoming lead (recap ratios, pool size, senior preference, pay-to-play mechanics if any).
- Charter amendment (conversion mechanics, blank-check authority use, new preferred designation).
- Board and preferred vote choreography (identify every vote gate, secure written commitments in advance).
- IRA and Voting Agreement amendments as required.
- Repricing plan documentation (shareholder-consent requirements checked, ASC 718 accounting mapped out).
- 409A revaluation ordered and delivered before the grants are made.

**Cap-table.**
- Pro-forma cap table under multiple recap scenarios (different conversion ratios, different pool sizes).
- Waterfall analysis at multiple exit prices for founders, employees, existing preferred (participants and non-participants), incoming lead.
- Explicit modelling of the re-up: total additional shares, per-employee grants, vesting, dilution to incoming lead.
- Updated capital plan post-recap.

**Communication.**
- Board-materials for the recap approval.
- Detailed memo to existing preferred laying out participation economics, non-participation consequences, and the pro-rata offer.
- Founder-to-employee communication: the recap explained, the re-up programme explained, the individual grant per employee shown in advance.
- Manager-to-team talking points so line managers can answer questions consistently.
- All-hands meeting or its equivalent with founder and CFO answering questions live. Avoid the "email-only" delivery.

**Process.**
- Milestone-tracking of the fundraising close.
- Cash-tracking against the runway plan; if the recap slips, the plan-B path (chapter 1's 3-month emergency) activates.
- Post-close reconciliation of the definitive cap table to the term sheet and the pro-forma model.

## Common failure modes

- **Modelling only the "everyone participates" case.** The recap that "works" if everyone plays is not the recap you have on the day it closes. Model the worst realistic participation case first.
- **Not identifying every vote gate in advance.** A supermajority requirement discovered at the eleventh hour blocks the close. Counsel and the CFO map every gate, get written commitments, and re-check when the term sheet moves.
- **Cram-down without process rigor.** Aggressive mechanics without independent-director approval, without offering pro-rata to all existing preferred, without documented fairness — invite litigation and can undo the transaction. The lawyer work here is not optional.
- **Sizing the re-up pool too small.** The re-up that leaves engineers underwater the day after the close will not retain the team. Fight for the size that actually works.
- **Repricing without ASC 718 modelling.** The repricing accounting expense can be material and will show up in the next audit. The CFO models it in advance and communicates the impact to the board.
- **Communication delivered piecemeal.** Recap first, re-up next week, communication cascade the week after. By the time the re-up is delivered, the team has already been recruited away. Deliver together.
- **Not planning for the departure of some team members.** Even a well-executed recap plus re-up will lose some team. The CFO plans hiring backfills into the post-close plan and does not treat the retention as certain.

## What good looks like

A CFO who has this material installed:

- Distinguishes between "pay-to-play with participation offer" (chapter 3) and "recap plus re-up" (this chapter) situations, and reaches for the harder tool only when the softer one will not close the round.
- Models the recap and re-up simultaneously — the recap is only survivable with the re-up in place, and the CFO does not present one without the other.
- Identifies every vote gate and secures written commitments before the term sheet is finalised.
- Works with counsel to meet the process standards that a fairness challenge would apply (independent-director approval, pro-rata offer to all existing preferred, market-terms comparables).
- Delivers the communication cascade — board, existing preferred, employees, hires-in-flight — in a coordinated single window, not piecemeal.
- Prices the re-up pool to actually retain the team and defends the pool size in the term-sheet negotiation as a term the CFO will not concede below a defensible floor.
- Reconciles the post-close cap table to the term sheet and the pro-forma model, and files the corporate records so that the next diligence read reads clean.

## Summary

- Recapitalisations collapse the existing preferred stack (usually by conversion to common at defined ratios) to make the incoming lead's underwriting work when the accumulated preference is too deep for a simple pay-to-play to solve.
- Cram-downs force the recap or down-round terms on non-consenting holders using drag-along, majority-vote, or blank-check preferred mechanics. Cram-down carries real litigation risk under Delaware fiduciary-duty doctrine — process rigor is not optional.
- Common-employee re-up grants (new grants at the new post-recap FMV, or option repricing / exchange programmes) restore the option pool's value after the recap has re-set the underlying FMV. Typical pool size 10-20% of the post-recap FD.
- The re-up must be sized, structured, and communicated in the same window as the recap. The two are a single event, not a sequence.
- The CFO's work list spans legal (charter amendment, IRA, vote choreography), cap-table (pro-forma under multiple participation scenarios), communication (board, existing preferred, employees, hires-in-flight), and process (milestone tracking, cash tracking, post-close reconciliation).
- The alternative to a well-executed recap + re-up is not a better fundraise — it is the sale process, wind-down, or ABC path in `startup-exit-curriculum`.

Chapter 5 turns to the debt side of the capital-instrument menu — venture debt from the SVB / TriplePoint / Runway Growth / Hercules Capital pattern, warrant coverage, financial covenants, MAC clauses, and the specific trade-off between using debt to extend runway to a stronger next round and using debt to postpone a decision that should have been faced earlier.
