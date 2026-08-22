# Hiring Plan as the OPEX Driver

## Why this matters

Payroll is by far the largest cost line in most software startups — commonly 60-80% of operating expense from Seed through Series-B — and it is the line the CFO has the most control over. Every hire is a decision to add roughly $200-450K per year of fully-loaded cost that persists as long as the employee stays. A model whose payroll line is "trend it up by 15% per quarter" gives the CEO no ability to answer *"what if we froze hiring in Sales for a quarter?"* or *"what does the burn look like if we push the two Series-A engineering leads from March to June?"*

The hiring plan is the tab that answers those questions. It is a monthly grid of planned hires, each row tagged with role, level, start month, fully-loaded cost, and department; the P&L payroll line, the opex-by-function split, the deferred-commission asset movement, and the SBC line all reference it. Change a single start month on the hiring plan and every downstream cost cell in every forecast month updates.

This chapter installs the hiring plan as the operating-expense driver — its shape, the fully-loaded-cost calculation, the department allocation, the timing conventions, and the integration with the S&M / R&D / G&A opex categories on the P&L.

## The hiring-plan tab — shape

The hiring plan is a table, not a set of scalars. One row per current or planned employee, with columns for the attributes that drive the P&L. A minimum column set:

| Column | Type | Purpose |
|---|---|---|
| Employee ID / hire number | text / int | Unique identifier for tracing back to the roster |
| Role (title) | text | E.g., "Senior Backend Engineer", "Account Executive" |
| Level | ordinal | E.g., IC3 / IC4 / IC5, M3 / M4 (see comp benchmarks below) |
| Department | enum | S&M / R&D / G&A / COGS (customer support) |
| Location | text | Drives salary band and employer-tax rate |
| Start month | date | Month of first day; drives when payroll begins |
| End month | date (nullable) | Left blank if still active; a date if attrition or planned departure |
| Base salary (annual) | $ | Cash salary |
| Target bonus / commission (%) | % | Applied to base for total cash comp |
| Benefits load (%) | % | Health, dental, retirement match, other benefits |
| Employer taxes (%) | % | Payroll tax employer portion (US: FICA 7.65% + FUTA + state SUTA) |
| Fully-loaded monthly cost | $ | Formula: `(base × (1 + bonus%) × (1 + benefits% + employer_tax%)) / 12` |
| Equity grant (# shares) | int | Initial grant on hire; drives SBC schedule |
| Vest schedule | text | Standard 4-year with 1-year cliff, or variant |
| Commission-capitalisation flag | Y/N | Under ASC 340-40: commissions capitalise and amortise over expected customer life |

A well-built hiring-plan tab has this table on the left and a monthly-cost grid on the right — one column per calendar month across the forecast horizon, with a cell in each column that is either the fully-loaded monthly cost of that employee (if the month falls between start and end), or zero (if not). The bottom row of the grid is total monthly payroll, which is the input to the P&L payroll line and to the department-split calculations.

The tab uses Excel Tables or Google Sheets' data ranges so that adding a new hire is a matter of adding one row, not editing formulas. The monthly-cost grid extends the table's formulas automatically to the new row.

## Fully-loaded cost — what to include

"Fully-loaded" is the CFO-grade convention for payroll cost. The base-salary number in an offer letter is roughly 60-75% of what the employee actually costs the company. The gap is:

- **Employer taxes.** In the US: FICA (Social Security 6.2% up to the wage base, Medicare 1.45% uncapped) contributes 7.65% on the first $168,600 of 2025 wages, then 1.45% (Medicare) uncapped. Additional Medicare tax (0.9%) applies over $200K but is employee-paid. FUTA (federal unemployment) is 6% on the first $7,000 per employee, typically reduced to 0.6% with state credit. State SUTA (state unemployment) varies by state and employer experience rating, typically 1-6% on the first $10-20K. Practical burden rate for US employees is 8-10% of gross pay for most compensation bands, dropping to closer to 2% for high earners past the FICA wage base.
- **Benefits.** Health / dental / vision insurance, retirement match (typically 3-6% of salary as an employer match), life insurance, disability, HSA / FSA contributions. Typical range: 10-20% of salary for a US company offering competitive benefits; higher for very generous benefits packages.
- **Bonus / commission.** Target bonus (typically 10-20% for engineering / product, 30-60% variable for sales roles between base and commission), calculated at target attainment. The commission accrual on the P&L should be at target unless a specific attainment scenario is being modelled.
- **Stock-based comp** — treated separately as a non-cash P&L expense (see below); not counted in the cash payroll load but included in the "cost of the employee" from a P&L perspective.
- **Recruiting cost** — external recruiter fees (typically 20-25% of first-year comp for executive and specialised technical roles) — either amortised as G&A or expensed at hire; usually not baked into the per-employee fully-loaded number but pooled in a separate recruiting line under G&A.
- **Equipment and workspace** — laptop, home-office stipend, office rent per seat, coworking allowances — usually pooled in G&A rather than allocated per hire, but relevant to the total cost of a headcount decision.

A defensible fully-loaded burden rate for a US software startup:

- **Individual contributors, $100-200K base:** salary × 1.28-1.35 (base + bonus + benefits + employer taxes, no SBC).
- **Senior ICs / managers, $200-350K base:** salary × 1.22-1.30 (benefits and employer taxes are a smaller percentage as salaries rise past the FICA wage base).
- **Executives, $350K+ base:** salary × 1.18-1.25 (mostly base drift past the FICA cap).
- **Sales roles at $150-250K OTE:** salary × 1.30-1.40 (higher benefits, higher commission-driven bonus load, higher recruiting cost that some CFOs load per-role).

Regional and international variations matter and should be modelled explicitly if the company hires internationally — UK employer NIC is 15% (2025 rate); Canadian EI/CPP is 8-11%; Germany's social-insurance load is 20-25%. A hiring plan that hires "in Berlin" at the same burden rate as San Francisco understates cost by 10-15%.

The convention that survives diligence: name the burden-rate assumption on the assumption tab (`US_burden_rate = 30%`, `UK_burden_rate = 32%`, etc.), and apply it consistently across all US / UK / etc. hires on the hiring-plan tab. A per-employee override is fine for a specific case (an executive whose benefits are grandfathered from a prior employer, for example) but should be flagged.

## Timing conventions — start dates and mid-month hires

An offer accepted in February may start on 15 March. The P&L expense in March is roughly half the fully-loaded monthly cost — half a month of pay, plus whatever benefits accrue for a partial-month enrolment. Common conventions:

- **Full-month convention:** every hire starts on the first of a month. Simpler; overstates or understates first-month payroll by up to 50%.
- **Half-month convention:** any hire starting in the first half of a month counts as a full-month payroll; second half counts as half a month. A common compromise between simplicity and accuracy.
- **Prorated:** exact fraction of the month between start date and month-end. Most accurate; slightly more complex formulas.

For a startup with 5-15 hires per month, the half-month convention is enough. For a growth-stage company with 30+ hires per month, prorated is worth the marginal complexity. Whichever convention is chosen, document it on the assumption tab and apply it consistently.

The same convention applies to departures — an end date in the middle of the month is either full-month, half-month, or prorated on the same rule.

Sign-on bonuses and referral bonuses are separate one-time payroll lines, usually paid in the first month of employment (sign-on) or the first month after the referred hire's start date (referral). These are typically small enough to pool in a "one-time payroll" line under G&A rather than modelling per-hire, unless a specific hiring cohort has large sign-ons (an executive hire).

## Department allocation — the S&M / R&D / G&A split

The P&L splits opex into S&M, R&D, and G&A (SaaS-standard presentation; some industries also split out COGS-embedded headcount like customer support). Every hire on the hiring-plan tab is tagged with one department; the driver tab sums fully-loaded payroll by department by month; those sums feed the three P&L opex lines.

Department mapping conventions:

- **Sales & marketing (S&M):** every AE, SDR, sales engineer, marketing team member (demand-gen, product-marketing, brand-marketing, growth-marketing), revenue operations. The CS team is *usually* R&D or COGS but there are conventions where CS is loaded to S&M — pick one convention and document it.
- **Research & development (R&D):** every engineering role (product engineering, infrastructure, platform, security, ML), every product-management role, every design role. UX researchers, data engineers, data scientists. Sometimes IT-support is loaded to R&D at Series-A and earlier, then split off to G&A as the company grows.
- **General & administrative (G&A):** finance, accounting, legal, HR / people-ops, executive (CEO, COO if not part of S&M), IT-support at scale, facilities, office managers, executive assistants.
- **Cost of revenue (COGS):** customer support (in most SaaS conventions), professional-services delivery, customer-success onboarding (partial allocation), and any hosting-adjacent engineering that supports production ops.

The convention debate that matters most for a growth-stage startup: **how much of customer-success is COGS vs. S&M or R&D.** The SaaS-metrics canon (see [ForEntrepreneurs](https://www.forentrepreneurs.com/) and the OpenView SaaS Benchmarks) tends to load CSM headcount to COGS for gross-margin purposes when the CSM is delivering the paid service, and to S&M when the CSM is closing renewals and expansions. Pick a rule, document it, apply it consistently — a change in convention mid-year is a red flag in diligence.

The department tag on the hiring plan drives the split. If a specific hire straddles two departments (e.g., a solutions engineer who spends 60% on pre-sales and 40% on post-sales), model it as two rows with a fractional allocation, or split the fully-loaded cost across two department columns.

## Non-payroll opex — the ratio approach

Every department has non-payroll opex — the tools, the ad spend, the office costs, the legal fees. Modelling every non-payroll line individually is possible but usually overkill; the working convention is to drive non-payroll opex as a ratio.

- **S&M non-payroll (paid media, tools, events, agency):** either as a percentage of S&M payroll (typical range 40-100% for a Series-A B2B SaaS depending on paid-motion intensity), or as a percentage of revenue (10-30% typical, higher for a heavy paid-motion company), or per-lead / per-SQL / per-customer if the mod-102 unit-economics work has produced those numbers.
- **R&D non-payroll (cloud infra for engineering, dev tools, contractors):** typically 10-25% of R&D payroll for a modern-stack SaaS company.
- **G&A non-payroll (rent, insurance, legal, tax, audit, general tools):** typically 15-30% of G&A payroll, plus the specific line items that don't scale with headcount (office rent per lease term, D&O insurance per year, audit fees when the first audit hits).

The ratios are set on the assumption tab; the driver tab multiplies them by the payroll base or revenue base and pipes the result to the P&L. A change to the S&M non-payroll ratio produces the correct dollar movement on the S&M opex line without editing the P&L directly.

Certain non-payroll G&A lines are large, lumpy, and worth modelling individually rather than as ratios:

- **Office rent** — set by lease terms; step-function changes when the company moves to a new lease.
- **D&O insurance** — annual, tends to jump at fundraise events (a Series-A close usually triples the D&O premium; a Series-C close usually adds a run-off tail on the pre-money coverage).
- **Audit fees** — zero until the first outsourced audit (typically Series-B), then a step-function jump; recurring annually after.
- **Legal fees** — lumpy, tend to spike around fundraise events, M&A, litigation. Model a baseline plus event-driven spikes.
- **R&D tax credit** — if the company qualifies under IRC §41 and has elected the payroll offset under §41(h), model a monthly credit against employer payroll tax up to the current cap ($500,000 per year for qualifying small businesses under the Inflation Reduction Act's 2023 update). This is a cash saving, not a P&L saving.

Each of these gets its own row on the driver tab with an explicit forecast; the ratios pick up the rest.

## Deferred sales commissions under ASC 340-40

Sales commissions on new bookings and on multi-year renewals are the largest capitalised expense on most SaaS balance sheets. Under [FASB ASC 340-40](https://asc.fasb.org/), the incremental costs of obtaining a contract (typically sales commissions plus employer taxes and benefits on the commission portion) are capitalised as a "deferred contract cost" asset and amortised as commission expense over the expected customer life — usually 3-7 years, and typically longer than the initial contract term.

The hiring plan feeds this schedule via the sales headcount and the commission plan on the assumption tab. The driver tab produces:

- **New-bookings commission accrual per month** — sum of commissions payable on contracts closed that month at target quota attainment.
- **Deferred contract cost roll-forward** — opening balance + new capitalisation - amortisation = closing balance.
- **Commission expense on the P&L (S&M line)** — the amortisation amount.
- **Deferred contract cost on the balance sheet** — the closing balance, split short-term (next 12 months of amortisation) and long-term (remainder).
- **Cash impact on the CFS** — the actual cash paid to sales reps for the month (usually roughly equal to new-bookings accrual, with some lag for paid-when-collected clauses), NOT the amortisation on the P&L.

The critical modelling point: the P&L commission expense and the cash commission payment are different numbers. A high-growth startup capitalising commissions can show S&M commission expense of $200K/month on the P&L while paying $600K/month in cash to sales reps — the $400K delta is the working-capital use that shows up on the CFS as an increase in deferred contract costs. A P&L-only model shows the smaller number and understates cash burn by 66%.

Chapter 6 of [`mod-101`](../mod-101-startup-accounting-foundations/) and chapter 1 of [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/) cover ASC 340-40 mechanics in detail; this chapter is about wiring it into the hiring plan.

## Stock-based compensation — the parallel schedule

SBC is a non-cash P&L expense that runs alongside the cash payroll. Every employee's equity grant (initial grant on hire, plus annual refresh grants) produces an SBC expense that lands on the P&L over the vest schedule — typically 4-year straight-line with a 1-year cliff, though some companies use graded vesting (front-loaded to first year) or milestone vesting for executives.

The driver tab produces:

- **Per-employee SBC expense per month** — grant fair value at grant date × (1 / vest months), with a forfeiture adjustment for the expected turnover (typically 5-10%).
- **Total SBC by department per month** — sum of per-employee SBC, tagged by the same department as cash payroll.
- **SBC lines on the P&L** — added to the S&M / R&D / G&A opex lines; sometimes broken out as a separate sub-line for clarity.
- **APIC (additional paid-in capital) on the balance sheet** — increases each month by total SBC expense.
- **SBC add-back on the CFS** — added back to net income in the operating-activities section (non-cash item).

Fair-value valuation of options requires either a Black-Scholes model or a Monte Carlo model; most startups apply a Black-Scholes value from the most recent 409A valuation and rebuild the SBC schedule at each 409A refresh (annually or on a material event). The 409A methodology is covered in [`mod-104`](../mod-104-cap-tables-and-equity-compensation/).

For the three-statement model, SBC is a parallel schedule on the hiring-plan tab that feeds the P&L (opex add), the balance sheet (APIC increase), and the CFS (non-cash add-back). The three ties reconcile every month.

## Turnover, backfills, and the ramp adjustment

A hiring plan that assumes zero turnover is fiction. Every model needs an attrition assumption — a monthly probability of departure by role — that generates end-dates on existing employees. Backfill logic then determines whether departed roles are re-hired (usually yes, at the same fully-loaded cost) or absorbed (rare, and requires an explicit CEO decision).

Additionally, new hires are not fully productive on day one. The ramp-to-productivity varies by role:

- **Sales reps (AEs):** 3-6 month ramp to full quota attainment. During ramp, the AE is expensed at 100% but produces closed bookings at 25-50% of the ramped-quota level. This should feed the GTM funnel model (chapter 4) as a productivity coefficient, not the P&L directly.
- **SDRs:** 1-3 month ramp to full outbound activity levels; similar productivity modelling in the funnel.
- **Engineers:** 3-6 month ramp to full productivity; harder to model directly but shows up as slower feature velocity.
- **Customer success:** 1-3 month ramp; typical to load a new CSM at 50% of full book of business until they onboard.

Ramp doesn't change the P&L payroll cost — the CFO pays the full salary from day one — but it changes the *output* the model expects from each hire. This is why the hiring plan is the input to the GTM funnel (chapter 4) as well as to the P&L: the funnel's SQL-per-SDR-per-month coefficient depends on how many SDRs are past ramp in each month.

## Integration with the P&L — the three lines

The hiring-plan tab drives three lines on the P&L via the driver tab:

1. **Payroll expense** — sum of fully-loaded monthly cost across all active employees, split by department (S&M / R&D / G&A / COGS-embedded).
2. **Non-payroll opex** — driven by ratio-to-payroll or ratio-to-revenue rules on the assumption tab.
3. **Stock-based comp** — sum of SBC expense across all active employees with unvested equity, split by department.

The P&L S&M line = S&M payroll (from hiring plan) + S&M non-payroll (from ratio) + S&M SBC (from hiring plan). Same for R&D and G&A. The COGS embedded lines (customer support, ProServ) work the same way; the P&L presents them under Cost of Revenue rather than under Operating Expenses.

Every one of these numbers changes when a hire's start month changes, when a burden rate changes, when a ratio changes, when a scenario switch flips. The hiring plan is the single source of truth; the P&L is the derived output.

## Summary

- The hiring plan is a monthly table of every current and planned employee, tagged with role, level, department, location, start month, base salary, and equity grant. The monthly-cost grid on the right derives fully-loaded cost by month by employee.
- Fully-loaded cost = base × (1 + bonus%) × (1 + benefits% + employer_tax%), varying by geography. Typical burden rates: 28-35% for US ICs, 20-25% for US executives past the FICA cap, higher for European geographies.
- Timing conventions: half-month for most startups, prorated for growth-stage. Apply the convention consistently to hires and departures.
- Department allocation (S&M / R&D / G&A / COGS-embedded) is per-hire on the hiring plan; the driver tab sums by department and feeds the three P&L opex lines.
- Non-payroll opex is driven by ratios on the assumption tab (S&M as % of S&M payroll, R&D as % of R&D payroll, G&A as % of G&A payroll or per-line schedule for lumpy items like rent / audit / D&O).
- Deferred sales commissions under ASC 340-40 produce a P&L amortisation expense different from the cash commission paid — the delta is a working-capital use on the CFS. The hiring plan feeds the commission-capitalisation schedule.
- SBC is a parallel schedule that produces a non-cash P&L expense, increases APIC on the balance sheet, and adds back to CFO on the cash-flow statement. Every employee's grant contributes over their vest schedule.
- Turnover, backfill, and ramp assumptions are on the assumption tab; ramp coefficients feed the GTM funnel model, not the P&L payroll line.
- The three P&L opex lines (S&M, R&D, G&A) are the driver-tab sum of `payroll + non-payroll + SBC`, per department. No P&L cell contains a raw payroll number.

Chapter 4 turns to the GTM funnel — the tab that drives the revenue line, the counterpart to the hiring plan.
