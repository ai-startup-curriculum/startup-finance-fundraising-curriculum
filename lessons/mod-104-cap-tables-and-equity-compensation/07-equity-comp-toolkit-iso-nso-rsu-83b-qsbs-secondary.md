# Equity-Comp Toolkit — ISO, NSO, RSU, 83(b), Early Exercise, QSBS, Secondary

## Why this matters

The cap-table anatomy, the pre-money math, the pool sizing, the waterfall, the 409A, and the Rule 701 regime all serve one endpoint: the **actual equity instrument** given to a particular employee at a particular career-stage moment. The choice among ISO, NSO, RSU, restricted stock — plus the ancillary decisions around vesting, cliff, 83(b) election, early exercise, QSBS eligibility, and secondary-tender access — determines the employee's tax outcome, the company's ASC 718 expense, and the diligence-defensibility of the entire equity story.

Get the instrument choice right and the equity is a genuine wealth-creation tool the company deploys to attract, retain, and align. Get it wrong and the employee's grant delivers less value than an equivalent cash bonus after tax, and the company creates preventable friction at exit.

This chapter is a decision-matrix chapter. It installs each instrument's mechanic, the tax treatment at each moment (grant, vest, exercise, sale), and the employee-lifecycle mapping that determines which instrument fits which stage. It does **not** try to be a complete tax treatise (that's what tax counsel is for) or to author equity-comp *policy* (grant guidelines, refresh cadence, IC-plan structure — that's `startup-operations-governance-curriculum`).

## The four instruments — quick reference

| Instrument | Who typically gets it | Strike / purchase | Vesting | Employee tax at grant | Employee tax at vest | Employee tax at exercise | Employee tax at sale | Company deduction |
|---|---|---|---|---|---|---|---|---|
| Restricted Stock (RS) | Founders, earliest-stage employees | At FMV, paid up-front | Same-shaped schedule | None if 83(b) filed | None if 83(b) filed | N/A | LT cap gains if held 1+ year past 83(b) | None (unless SBC accounting requires it) |
| Incentive Stock Option (ISO) | Employees (only) | At or above FMV per 409A | Typically 4-year / 1-year cliff | None | None | None for regular tax; AMT applies to spread | LT cap gains if ISO holding periods met; otherwise disqualifying disposition = ordinary income on spread | None if ISO qualifying; if disqualifying, ordinary income becomes deductible |
| Non-Qualified Stock Option (NSO) | Non-employees, consultants, employees exceeding ISO $100K limit | At or above FMV per 409A | Typically same as ISO | None | None | Ordinary income on spread at exercise; employment taxes if employee | LT / ST cap gains on further appreciation post-exercise | Yes — deductible as compensation |
| Restricted Stock Unit (RSU) | Late-stage employees (double-trigger) | Nothing paid | Time + liquidity trigger | None | None (if double-trigger deferred) | N/A | Ordinary income on FMV at settlement (liquidity event); further gain LT/ST | Yes — at settlement |

## Restricted stock (founder grants)

At formation and in the earliest weeks after, founders acquire common stock via a **restricted stock purchase agreement**. They pay the current FMV (fractions of a cent per share) in cash and receive shares subject to a **repurchase right** the company can exercise if the founder leaves before vesting is complete. The vesting schedule is typically 4 years with a 1-year cliff, mirroring what the founder would offer employees.

The critical mechanic is the **83(b) election**. Section 83 of the Internal Revenue Code says that if property is transferred to a service provider subject to a "substantial risk of forfeiture" (i.e., the vesting condition), the recipient recognises ordinary income equal to the FMV of the property *at each vesting date* as the risk lapses. Without an 83(b), the founder would owe ordinary income at each monthly (or milestone) vesting event on the *then-current* FMV — potentially six or seven figures of income tax over the vesting period as the company's value grows.

The 83(b) election flips this: the founder elects to be taxed at grant (on the FMV at grant, minus what they paid — which is often zero since they paid FMV). No further income recognition happens during vesting. Any subsequent gain is capital gain at sale.

**How to file:** the 83(b) election is filed with the IRS within **30 days of the transfer** of the property. It's a one-page form. The 30-day deadline is strictly enforced — there is no cure for a missed 83(b) election. A copy is filed with the IRS (certified mail or registered mail with return receipt is the safe practice), a copy is provided to the company, and a copy is included with the founder's next tax return.

Founder 83(b) elections filed within the 30-day window are the single most valuable tax move a founder makes. Missing the deadline is a well-known founder-error that costs six or seven figures of tax over the vesting period.

Restricted stock is also occasionally granted to the earliest 5-10 employees when the company is still at very low FMV (fractions of a dollar per share) and the employee can afford to buy up front. Each such employee files their own 83(b).

## Incentive Stock Options (ISOs)

The ISO is the tax-favoured option available only to employees (not consultants, not board members who aren't employees). ISO tax treatment:

- **At grant:** no tax.
- **At vesting:** no tax.
- **At exercise:** no *regular* income tax on the spread (FMV − strike). But — critical — the spread is a **positive adjustment for Alternative Minimum Tax** (AMT) purposes. An employee who exercises deep in the money can trigger significant AMT liability in the exercise year, even though no cash has changed hands.
- **At sale, if ISO holding periods met** (2 years from grant date and 1 year from exercise date): the entire gain (sale price − strike) is long-term capital gain. This is the pot of gold that makes ISOs valuable.
- **At sale, if holding periods not met** (a **disqualifying disposition**): the spread at exercise (up to the actual gain if lower) becomes ordinary income; further gain is capital gain (short-term if sold within 1 year of exercise, long-term after). The company gets a compensation-expense deduction equal to the ordinary-income amount.

**The $100K limit.** ISO status is limited to $100K of first-time-exercisable value per employee per calendar year, measured at grant-date FMV. Grant value beyond $100K/year automatically converts to NSO treatment. A large grant (a VP-level grant, say, $500K of grant-date FMV vesting monthly over 4 years) has about $100K first-time-exercisable in year 1 as an ISO, and the remaining ~$400K is NSO.

**Who ISOs are best for.** Employees who plan to exercise and hold to satisfy the ISO holding periods, and who can either (a) exercise while the spread is small (early in the employment period, before the FMV has run up) or (b) plan around the AMT hit at exercise. ISOs plus early exercise (below) plus 83(b) can produce a very tax-efficient outcome for early employees.

**Who ISOs are worst for.** Late-stage employees exercising deep in the money and selling promptly. The AMT hit at exercise plus the disqualifying-disposition treatment (if sold within 1 year of exercise) often makes NSO treatment simpler and not much worse economically.

## Non-Qualified Stock Options (NSOs)

The NSO is the default option that everyone else gets — non-employees (consultants, advisors, some board members), employees at grant amounts exceeding the ISO $100K limit, and employees at some companies as a matter of policy. NSO tax:

- **At grant:** no tax.
- **At vesting:** no tax.
- **At exercise:** ordinary income on the spread (FMV − strike). For employees, this is subject to income-tax withholding and payroll taxes (FICA, FUTA). The company gets a compensation-expense deduction equal to the spread.
- **At sale:** capital gain (or loss) on the difference between the sale price and the FMV-at-exercise (which was already taxed as ordinary income). Short-term if held < 1 year post-exercise, long-term if held ≥ 1 year post-exercise.

The company's ability to deduct the ordinary income at exercise is the reason NSOs are sometimes preferred at the company level even when the employee would slightly prefer ISOs — the deduction offsets the compensation expense on the P&L (and the ASC 718 expense at grant).

## Restricted Stock Units (RSUs)

RSUs are a contractual promise to deliver a share of stock upon the satisfaction of a vesting condition. There's no exercise, no strike price — just delivery of the share at vesting (or later, at "settlement," which can be a separate event).

**In a public company**, the RSU is straightforward: vest, settle, employee pays ordinary income tax on FMV at settlement, employee owns the share.

**In a private company**, the RSU has a problem: at time-based vesting, the employee owes ordinary income tax on the FMV, but there's no market to sell into to fund the tax payment. Private-company RSUs solve this by using a **double-trigger** vesting structure:

- **First trigger:** time-based vesting (typically 4 years / monthly).
- **Second trigger:** a liquidity event (IPO, acquisition, or, at some late-stage companies, a qualifying tender offer).

The RSU only "settles" (i.e., delivers the share and triggers taxation) when *both* triggers are met. This defers the tax liability until the employee has a market to sell into.

**When to use private-company RSUs vs. options.** The typical inflection is at **Series-C or later**, when the FMV has risen enough that an employee exercising options would face a large cash outlay (strike × shares) that they can't afford, and where the company can credibly argue that a liquidity event is within the reasonable near future (so the second trigger is not indefinite). Before Series-C, options are almost always the right instrument.

**Why not just always use RSUs.** Two reasons: (i) the ISO benefit (LT cap gains on the entire spread from strike to sale) is only available with ISOs, not RSUs — so an early employee who exercises and holds gets a much better tax outcome under an ISO than under an RSU. (ii) The private-company RSU is more complex to administer, requires the double-trigger design, and creates income-inclusion complexity at IPO or acquisition when the RSUs suddenly settle en masse.

<!-- needs-research: cite the Carta State of Private Markets data on the private-company shift from options to RSUs by stage — the shift accelerated in ~2020-2022 for late-stage companies but the specific inflection percentages depend on the current-year report. -->

## Early exercise (and its interaction with 83(b))

Some companies offer **early exercise** on options — the ability for an employee to exercise the *unvested* portion of their options and hold the resulting stock subject to the company's repurchase right (which lapses on the same schedule as the original vesting).

The early-exercise mechanic + 83(b) election produces the most tax-efficient possible outcome:

1. Employee joins, receives an option grant at a low FMV (say, $0.50 strike).
2. Employee immediately (within 30 days) exercises the entire grant, paying $0.50 × total shares = whatever the total-strike outlay is. In an early-stage company this can be modest ($5K-$50K for a typical employee grant).
3. Employee **files an 83(b) election** within 30 days of the exercise, treating the acquired shares as compensation income at the current FMV (which equals the strike, so income is zero).
4. Shares are now held as restricted stock subject to repurchase, with the repurchase right lapsing on the vesting schedule.
5. Any future appreciation is capital gain, long-term if held 1+ year from exercise date.
6. If the employee leaves before vesting completes, the unvested shares are repurchased at cost (the strike), and the employee has no downside beyond the initial outlay.

The result: no ordinary income at any point (assuming the strike equals FMV at exercise), and all future gain is long-term capital gain if held ≥ 1 year. This is far better than either ISO or NSO treatment for an employee who can afford the up-front outlay and expects the company to grow.

Not every company offers early exercise. Reasons a CFO / GC might restrict it: administrative complexity (each early-exercise triggers a fresh 83(b) coordination), audit / valuation risk (a bunch of exercised-then-forfeited shares create a mess for the 409A appraiser), and adverse-selection concerns (only employees who expect to leave early would early-exercise). The industry pattern: most seed and Series-A companies do offer early exercise, some Series-B+ companies restrict it to executives, most Series-C+ companies restrict it or drop it.

## QSBS — Section 1202

**Qualified Small Business Stock (QSBS)** under Internal Revenue Code Section 1202 is a founder-and-early-employee benefit that, when applicable, exempts up to **the greater of $10M or 10x the taxpayer's aggregate adjusted basis** in the stock from federal capital-gains tax at sale. The exemption is 100% for stock acquired after September 27, 2010, and held for at least 5 years. This is potentially the single largest tax benefit available to a startup employee.

**Requirements for QSBS treatment:**

1. The stock must have been issued by a **C corporation** (not an LLC, not an S-corp).
2. The corporation's gross assets at the time of stock issuance must have been **$50 million or less** (raised from $50M via inflation adjustment; still $50M as of the most recent update). This is measured at the time of issuance, so stock issued to a founder at formation is easy to qualify; stock issued as a Series-B option exercise years later may miss if the assets exceed $50M at that grant date.
3. The corporation must be an **active business** in a qualifying industry (excluded industries: professional services, banking, farming, hospitality, mining — the exclusions are broad, and a technology / software company almost always qualifies).
4. The taxpayer must have **acquired the stock at original issuance** (i.e., directly from the company, not from a secondary purchase) — with exceptions for gifts and inheritance.
5. The taxpayer must have **held the stock for at least 5 years** by the sale date.

For an employee with options, the stock is issued at *exercise*, not at grant. The 5-year clock starts at exercise. This is why early exercise + 83(b) is doubly valuable — it starts the QSBS clock as early as possible, and it starts the LT-capital-gains clock at the same time, both from the same date.

<!-- needs-research: verify the current status of any inflation adjustment or amendment to Section 1202's $50M gross-assets test or the 100% exclusion — the exclusion has been at 100% since 2010 but proposals to modify it have been circulated periodically. -->

**State conformity.** Some states conform to the federal QSBS exclusion (Colorado, New York, others). California explicitly does *not* conform — California residents owe state tax on gains that are federal-QSBS-exempt. A California-based founder planning around QSBS should plan around this, potentially with residency changes at the exit.

**The 5-year clock trap.** An employee who exercises at year 4 of employment and the company sells 8 months later has a QSBS holding period of 8 months, not 8 years. QSBS is claimed on the ordinary-income-vs.-cap-gain classification at sale, so a sale before the 5-year mark misses the exclusion entirely.

**The 10x-basis rule.** For very-early-stage founders whose basis is essentially zero (they paid fractions of a cent per share), the $10M cap dominates. For later-stage employees exercising at meaningful strikes, the 10x-basis rule can produce a larger exclusion. A VP who exercised $2M of options at strike is holding $2M of basis, and the 10x rule caps their exclusion at $20M (not $10M).

The QSBS exclusion is often the single most valuable tax planning move at exit. The CFO's job is not to give tax advice per se, but to make sure employees are informed about the eligibility — and to make sure the company's C-corp status, active-business qualification, and $50M gross-assets test are documented across the company's history so QSBS can be defended by the founders' and employees' tax advisors at sale.

## Secondary tenders — the pre-exit liquidity vent

Late-stage companies increasingly offer **secondary tender offers** — a company-facilitated purchase of vested employee shares by an existing or new investor at a specified price. Tender offers vent liquidity to employees and founders before the exit event, at the cost of some cap-table complexity (the tender participants become smaller holders, the tender investor becomes a larger holder).

**Mechanics:**

1. Company negotiates with an existing or new investor a per-share tender price for common stock. The price is usually at a discount to the current preferred-stock round price (because common lacks the preference stack) but at a premium to the current 409A common FMV.
2. Company offers all eligible employees (typically vested holders with ≥ some tenure, capped at some percent of their vested holdings) the opportunity to sell shares to the tender investor.
3. Tender is executed through a specific SEC-compliant tender-offer process (Rule 13e-3 doesn't apply for private companies but Section 14(e) and Rule 14e-1 govern; specific counsel-led process design).

**Tax and 409A consequences:**

- Employees selling in the tender recognise capital gain (or loss) on the sale — long-term if held ≥ 1 year from acquisition (either exercise for options or grant for restricted stock).
- The tender price is new market data for the 409A appraiser. Depending on volume and structure, the tender may or may not require a fresh 409A immediately, but the CFO should assume it will.
- The tender may also affect **QSBS holding periods** — a secondary sale ends the QSBS holding period for those shares; the employee should be aware that partial tenders don't necessarily terminate QSBS on the retained portion (each share is separately traceable).

**Why the CFO cares about tender design.** A poorly-designed tender offer produces (i) an outsized 409A adjustment that hits the strike price of future grants, making the company less attractive to future hires, (ii) securities-law compliance risk, (iii) a signal to the market that the company can't achieve an IPO / M&A exit in a reasonable time-frame.

A well-designed tender is a valuable retention tool. Common design constraints: eligibility (2+ years tenured; vested only), participation cap (25-50% of vested shares), pricing floor (some fraction of most recent preferred), pricing methodology (independent-appraiser opinion or a market discovery process).

## Vesting norms

The industry-standard vesting schedule:

- **4-year total vesting term.**
- **1-year cliff** — no vesting until the 1st anniversary of the vesting-commencement date, at which point 25% vests.
- **Monthly vesting thereafter** — 1/48th (of the total grant, or 1/36th of the post-cliff remainder — implementations vary slightly) each month for 36 months.

Some variations:

- **Backloaded vesting** — 10% year 1, 20% year 2, 30% year 3, 40% year 4. Increasingly common at late-stage companies (Amazon-style) as a retention mechanism, less common at startups. Backloaded schedules are unpopular with employees and unlikely to become a startup norm.
- **5-year or 6-year vesting** — occasionally seen at very early-stage founding roles.
- **Milestone vesting** — vesting on the achievement of specific milestones (product ship, revenue target). Common for advisor / consultant grants; rare for employee grants because of ASC 718 complexity.

**Acceleration** — a separate contractual provision governing what happens to unvested equity on a change of control. Two flavours:

- **Single-trigger acceleration:** on a change of control, unvested equity accelerates automatically. Rare for rank-and-file employees; common for a few named executives (typically CEO, sometimes CFO / VPs).
- **Double-trigger acceleration:** on a change of control **followed by** a termination-without-cause (or with-good-reason resignation) within a defined window (typically 12 months), unvested equity accelerates. More common as a default employee benefit at Series-B+ companies.

Acceleration is negotiated at hire and defined in the offer letter or a separate acceleration agreement. It matters in the waterfall (chapter 4): fully-vested-including-accelerated shares are on the common line at sale, so acceleration decisions directly affect the residual distribution.

## Vesting-commencement date subtleties

The vesting-commencement date (VCD) is not always the grant date. Common variations:

- **VCD = start date at company** (default; employee starts, VCD = start date, first grant at first board meeting sometimes weeks later with VCD backdated to start date).
- **VCD = prior date for pre-hire work** (e.g., a contractor who converted; VCD backdated to reflect their pre-conversion tenure).
- **VCD = date of promotion** for a promotion grant.

Backdating VCDs is legal *if* the underlying rationale (prior service, etc.) is documented — but the strike price still has to be FMV **at the grant date** (per 409A), not at the VCD. Confusing these produces mis-priced grants and 409A exposure.

## Decision matrix — which instrument at which stage

**Founders at formation.** Restricted stock at FMV (fractions of a cent), 83(b) election filed within 30 days. QSBS clock starts at grant.

**Pre-seed / seed employees, first 5-10 hires.** Options with early-exercise privilege + 83(b) on exercise. Same tax outcome as founder RS but with the option-holder's optionality if the company fails.

**Series-A / Series-B employees, general grants.** ISOs up to the $100K annual limit; NSOs above. Early-exercise availability depends on company policy but is increasingly restricted at this stage.

**Series-C+ employees.** Mix of ISOs / NSOs (still valuable up to the $100K limit and for employees who exercise early) plus RSUs (double-trigger) for the bulk of larger grants. The FMV is high enough that pure options would create prohibitive up-front strike costs and AMT exposure for many employees.

**Late-stage pre-IPO / high-FMV employees.** Primarily RSUs (double-trigger), with the second trigger being IPO or acquisition. Options phased out for new grants at this stage.

**Consultants, advisors, non-employee board members.** NSOs. Restricted stock rare. RSUs occasionally for very late-stage advisors with a clear liquidity event on the horizon.

**Founder refresh grants** (mid-stage). Usually NSOs (founders exceed the $100K ISO limit easily). Sometimes structured as a mix with restricted stock and a fresh 83(b) if the FMV allows.

## What good looks like

The CFO who has this material installed:

- Ensures every founder files an 83(b) within 30 days of formation restricted-stock grant (or arranges the reminder infrastructure via counsel to make sure it happens).
- Designs the equity incentive plan to allow ISOs, NSOs, restricted stock, and RSUs — so the company has all the instruments available and can choose per grant.
- Runs the ISO $100K allocation calculation before each large grant.
- Documents the early-exercise policy (yes / no / restricted to what level) with counsel and communicates it in the offer-letter equity summary.
- Reviews the company's C-corp status, active-business status, and gross-assets history annually to document QSBS eligibility for founders' and employees' future tax planning.
- Coordinates each tender offer as a securities-law + 409A + tax + cap-table + employee-communication event, with counsel in the lead.
- Reviews vesting schedules per grant against the company's standard (deviations require a written justification).
- Ensures acceleration provisions are documented in offer letters at hire, so there's no ambiguity at a change of control.

## Summary

- Restricted stock + 83(b) is the founder default. The 30-day 83(b) window is strictly enforced; missing it is one of the most expensive avoidable founder errors.
- ISOs are the tax-favoured option available only to employees, with a $100K annual first-time-exercisable limit. LT-cap-gains treatment on the full spread requires satisfying the ISO holding periods; AMT at exercise is the main gotcha.
- NSOs are the default for non-employees and for employees exceeding the ISO $100K limit. Ordinary income on the spread at exercise; the company gets a matching deduction.
- Private-company RSUs use double-trigger vesting (time + liquidity) to defer tax until the employee has a market to sell into. Typical inflection to RSUs is Series-C or later.
- Early exercise + 83(b) is the most tax-efficient combination for employees who can afford the up-front strike outlay — no ordinary income at any stage, all gain long-term capital gain, and the QSBS clock starts at exercise.
- QSBS under Section 1202 can exempt up to $10M (or 10x basis) of gain from federal capital-gains tax if the C-corp / $50M-assets / active-business / 5-year-hold requirements are all met. State conformity varies (California doesn't conform).
- Secondary tender offers vent late-stage liquidity to employees and founders, at the cost of cap-table complexity and 409A implications. Well-designed tenders are a retention tool; poorly-designed tenders create securities-law and valuation problems.
- Vesting norms: 4-year, 1-year cliff, monthly thereafter. Acceleration is a separate provision — single-trigger for a few named executives, double-trigger as the more common employee default at Series-B+.
- The equity-comp instrument choice is a **decision matrix** across stage, level, and employee circumstance. The pool, 409A, and Rule 701 machinery from the prior chapters exists to make each of these instrument choices defensible and correctly priced.

This concludes the equity-economics content of the module. Refer to the exercises for hands-on practice building each of these instruments into a real cap-table decision, and to [`resources.md`](resources.md) for the primary sources — NVCA model documents, YC SAFE library, IRC / Treasury regs, AICPA Practice Aid — that sit behind every chapter.
