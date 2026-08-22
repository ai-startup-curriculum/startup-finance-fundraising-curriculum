# The Finance Function's First Ten Hires — Sequencing, Triggers, and Comp Benchmarks

## Why this matters

The stack (chapter 1) is the plant and equipment; this chapter is the crew. The CFO builds the finance function one hire at a time, roughly in the same order at every venture-backed company, and roughly against the same stage triggers. Get the sequence wrong — hire a Head of FP&A before you have a controller, hire a treasury lead before you have $50M in the bank, hire a VP People / Head of Talent hire disguised as a "Chief of Staff to the CFO" — and each subsequent hire has to work around the misfire. Get the sequence right and each hire slots into a specific gap the previous one created, at a stage where the company can actually use them.

The compensation math is the second half of the discipline. Every one of these hires is comp-benchmarked in the public data — Carta State of Startup Compensation, Pave, Option Impact, Radford — and mispricing a hire either burns the ESOP faster than it needs to (over-paid) or loses the candidate to a better-priced offer at a peer company (under-paid). The CFO reads the benchmarks; the People / Talent function runs the offer; the CFO's decision is *which band on the benchmark* the role belongs in.

## The canonical ten-hire sequence

The sequence below is the reference. Real companies deviate — a highly-technical CEO may skip the fractional CFO; an international-first company may hire a tax lead earlier; a services-heavy business may need a revenue-operations analyst before an FP&A analyst — but the shape recurs. Deviations should be *deliberate* against a named reason, not accidental against org drift.

### 1. Outsourced accountant / bookkeeper (PRE-SEED)

**Trigger.** First outside capital raised. Founder needs someone to close the books, pay vendors, and file the annual tax return.

**Shape.** Outsourced firm, not a hire. Kruze, Pilot, Bench, Zeni, or a local CPA firm. Cost: $2K-$8K / month depending on transaction volume and whether they handle just bookkeeping or also tax and 409A refresh.

**What they own.** Monthly close (on cash basis), payroll runs (if the firm does payroll), 1099s, annual tax filings, R&D-credit filings (chapter 6, if qualifying). They do *not* own strategic finance decisions.

**Why not hire in-house.** At pre-seed headcount and transaction volume, an in-house bookkeeper is over-hired. The outsourced firm gives you a CPA-quality book on your specific scale without the fixed cost.

### 2. Outsourced or fractional CFO (SEED)

**Trigger.** First priced round is on the calendar, or the founder needs help constructing a defensible financial model / KPI framework / board reporting cadence, or the outsourced accountant has flagged a strategic decision (revenue-recognition policy, entity structure, tax election) the founder cannot make alone.

**Shape.** Fractional CFO on a $3K-$15K / month retainer, or a firm-provided CFO layered on top of the outsourced accounting (Kruze, Pilot, Burkland offer this bundled). Typical engagement: 10-20 hours / month at seed, ramping toward 40 hours / month if a fundraise is active.

**What they own.** The financial model (mod-103), the board deck financials, the fundraise data-room preparation (mod-107), the term-sheet analysis (mod-108), and the "which of the outsourced accountant's recommendations to take" arbitration.

**When to skip.** A founder with a genuine finance background (VC associate, ex-banker, ex-startup CFO) may skip the fractional and go straight to the first full-time hire below. Rare but real.

### 3. First controller (SERIES-A or approaching)

**Trigger.** Approaching Series-A, or Series-A closed. The company can no longer run on an outsourced accounting service plus fractional CFO — someone needs to own the ledger, own the close, own the AP flow, own the payroll cadence, and own the audit-readiness workstream that is now on the horizon.

**Shape.** Full-time, US-based, CPA typical though not always required, 5-15 years of experience. Title is sometimes "Head of Finance" or "Head of Accounting" or "Controller" — the *function* is the same regardless of title: own the accounting-operations layer end-to-end.

**Comp benchmark.** The exact band shifts year over year; check Carta State of Startup Compensation, Pave Benchmarks, and Option Impact for the specific role and stage. Rough shape at time of writing: base $150K-$220K, target bonus 10-20% of base, equity 0.15%-0.60% depending on stage and geography <!-- needs-research: pull the current Carta / Pave median cash and equity for "Controller" at Series-A with SF / NY / remote splits -->. The CFO's job is to pick the percentile — mid-range for a solid market hire, upper decile if this is the person who will grow with the company to Head of Accounting or Chief Accounting Officer.

**What they own.** Close ownership (chapter 3), audit-prep ownership (chapter 4), the NetSuite migration if not already done (chapter 1), the sub-ledgers (AR, AP, deferred revenue, fixed-asset schedule), the outsourced-firm relationship (they become the client-side owner of the outsourced accountant), the annual budget process alongside the CFO.

**The controller-first rule.** The controller should be hired *before* the first FP&A analyst. FP&A without a solid ledger produces reports built on shifting sand. Controller without FP&A produces a clean ledger without a decision-support layer, which is still useful. This is the specific hire whose out-of-order placement most reliably breaks the finance function.

### 4. First FP&A analyst (SERIES-A / SERIES-A+)

**Trigger.** The financial model has moved from a founder-CFO artifact to something the board and the operating team both want to interrogate weekly. The CFO does not have time to run the model updates, produce actuals-vs.-plan variance analysis, and refresh the driver assumptions across every function. The company has enough operating history (typically 12+ months of actuals) that variance analysis produces useful signal.

**Shape.** 2-5 years of experience, often ex-banking / ex-consulting / ex-management-consulting first-jump, sometimes ex-FP&A from a slightly larger company. Comp benchmark: base $110K-$160K, equity 0.05%-0.15% <!-- needs-research: pull current Carta / Pave median for "Senior FP&A Analyst" / "FP&A Manager" at Series-A/B -->.

**What they own.** Model maintenance (the actuals-vs.-plan variance walk after each close), department-level operating reviews, ad-hoc analysis for the CFO, board-pack production alongside the CFO. Under a well-run controller they get clean actuals to work against; without a controller they spend 60% of their time chasing ledger issues instead of producing analysis.

### 5. Head of Accounting (SERIES-B)

**Trigger.** The controller has grown into a management role — three to six people underneath doing the sub-ledger work — and either (a) the controller has expanded scope and is now functionally Head of Accounting, or (b) the controller is not the right person to manage a team and a separate Head of Accounting is layered over the controller. The audit workstream (chapter 4) is now a rolling annual project; the NetSuite instance is running production; the deferred-revenue subledger is at hundreds of active contract-months.

**Shape.** 10-20 years, CPA required, Big Four experience common though not required, often with a public-company reporting background if the IPO track is live. Comp benchmark: base $200K-$300K, equity 0.10%-0.40% <!-- needs-research: pull current Carta / Pave median for "Head of Accounting" / "Chief Accounting Officer" at Series-B/C -->.

**What they own.** The full accounting function (controller + AP + AR + payroll + sub-ledger owners underneath), audit relationship end-to-end, technical accounting positions (revenue-recognition, stock-based comp under ASC 718, business-combination accounting if there is an M&A), SOX-404 documentation lead if the IPO track is on.

### 6. Treasury lead (SERIES-B / SERIES-C, or earlier if cash pile is large)

**Trigger.** Cash on the balance sheet crosses roughly $50M-$100M (large post-Series-B raise or post-Series-C), FX exposure exists across multiple entities, or a debt facility (venture debt or growth debt from mod-109) creates covenant-monitoring work.

**Shape.** 8-15 years, often CFA, ex-treasury from a bank or a growth-stage company. Comp benchmark: base $175K-$275K, equity 0.05%-0.20% <!-- needs-research: pull current Carta / Pave median for "Head of Treasury" / "Treasury Manager" at Series-B/C -->.

**What they own.** Investment policy for excess cash (money-market funds, laddered T-bills, corporate paper — with an explicit risk policy signed by the audit committee — chapter 6 of [mod-110](../mod-110-board-and-investor-governance-for-the-cfo/06-board-committees-audit-comp-transaction.md)), FX policy for multi-entity operations, bank-relationship management, debt-covenant monitoring, letter-of-credit and treasury-services work.

**When to skip.** Companies with less than ~$30M in the bank rarely need a dedicated treasury lead; the controller or CFO owns the money-market decision directly. Post-SVB-2023, some companies added a treasury advisory relationship earlier without hiring a full-time lead.

### 7. Tax lead (SERIES-B / SERIES-C)

**Trigger.** The company's tax profile has become too complex for the outsourced tax firm to handle without a full-time internal owner: multi-state nexus and registration (chapter 7), first international subsidiary and transfer-pricing work, R&D credit optimisation at scale (chapter 6), first significant M&A that creates tax-attribute-preservation issues, or the audit-committee has started asking for a tax provision that ties to the audited financials with a documented effective tax rate.

**Shape.** 8-15 years, JD or CPA, often ex-Big Four or ex-in-house from a larger tech company. Comp benchmark: base $190K-$290K, equity 0.05%-0.20% <!-- needs-research: pull current Carta / Pave median for "Head of Tax" / "Senior Tax Manager" at Series-B/C -->.

**What they own.** Federal and state income tax, sales tax and VAT (with the outsourced firm doing the filings — chapter 7), international tax and transfer pricing, R&D-credit optimisation and payroll-offset election filing, tax-provision preparation for audit, M&A tax due diligence and structuring, tax positions in the eventual S-1 (chapter 8).

**When to skip.** Domestic-only companies without significant M&A activity can defer this hire to the pre-IPO stage and continue running on the outsourced firm plus a Big Four tax provision review annually.

### 8. Head of FP&A (SERIES-B / SERIES-C)

**Trigger.** The first FP&A analyst (hire #4) has been in-role for 12-24 months, the FP&A workload is now three to six analysts' worth, the model has grown to a scale that requires a dedicated FP&A platform (Workday Adaptive, Anaplan — chapter 1), and the FP&A function has clear management responsibility separate from the CFO's calendar.

**Shape.** 12-20 years, often ex-investment banking / ex-consulting / ex-strategic-finance from a growth-stage or public company. Comp benchmark: base $220K-$320K, equity 0.10%-0.40% <!-- needs-research: pull current Carta / Pave median for "VP FP&A" / "Head of Strategic Finance" at Series-B/C -->.

**What they own.** The FP&A team (four to eight analysts and managers underneath by Series-C), the annual planning cycle end-to-end, the operating-model refresh cadence (typically monthly), the board-pack analytical narrative, the M&A financial-diligence work if the company is on the acquiring side.

**Function split.** Some companies split "FP&A" (backward-looking variance analysis) from "Strategic Finance" (forward-looking capital-allocation, fundraise support, M&A). At Series-C+, the split is common; at Series-B, one head runs both.

### 9. Head of Investor Relations (LATE SERIES-C / DUAL-TRACK)

**Trigger.** The dual-track (IPO-and-fundraise-parallel) work is now live (chapter 8), or the company has enough non-lead investors and secondary-market activity to require a dedicated IR channel, or the analyst-community coverage that comes with the IPO track requires a professional response function.

**Shape.** 12-20 years, often ex-public-company IR / ex-sell-side analyst / ex-buy-side. Comp benchmark: base $230K-$340K, equity 0.05%-0.20% <!-- needs-research: pull current Carta / Pave median for "Head of Investor Relations" at pre-IPO / IPO-year -->.

**What they own.** Sell-side analyst communication, buy-side outreach, quarterly earnings prep (from Q1 as a public company onward), the investor-day cadence, the IR page on the corporate website, the standing dialogue with existing investors that lets the CFO's calendar focus on operating work.

**When to skip.** Pure private-track companies without secondary activity often keep the CFO as the IR-front until the IPO track is committed. This hire *anticipates* the IPO; it is a signal the dual-track is real.

### 10. CFO team-of-team (SERIES-C+ / PRE-IPO)

By the time the company is at Series-C or later on a dual-track, the CFO's direct reports look like: Chief Accounting Officer / Head of Accounting, VP FP&A, Head of Tax, Head of Treasury, Head of IR, plus a Chief of Staff or Head of Finance Operations who runs cross-team cadence and process. Underneath each of them is a team of three to fifteen. Total finance headcount at IPO for a $100M-$500M revenue company typically runs 40-120 <!-- needs-research: pull current benchmarks on finance-headcount-as-percent-of-total-headcount for pre-IPO SaaS from Carta / Bessemer / Meritech data -->.

At this point the CFO is running a *team of teams*, the direct-work slice of the calendar is on the S-1, the audit committee, the analyst community, and the CEO-CFO partnership. The individual-contributor finance work of earlier stages is now done by directors and senior managers three levels deep in the org.

## Reading the comp benchmarks

Carta State of Startup Compensation, Pave, Option Impact, and Radford are the public / semi-public data sources. Reading them well:

- **Match role to the benchmark title, not the internal title.** A company's "Head of Finance" may be a controller (accounting) or a Head of FP&A (planning) depending on the org design; benchmark against the *function* not the *title*. Getting this wrong produces the "we're paying $250K for a controller but the benchmark says $180K" reaction from a comp-committee member who is reading the wrong column.
- **Match stage precisely.** Series-B and Series-C comp curves diverge sharply — Series-C has more equity value per point but usually less percentage. Reading Series-B comp for a Series-C hire under-pays; reading Series-C for a Series-B over-pays.
- **Match geography.** SF / NY / remote-with-tier-1 / remote-with-tier-2 are different comp bands. The remote-hiring policy (mod-110 chapter 6 on the comp committee) should specify which tier applies.
- **Read cash and equity together.** A candidate in a below-median cash band with an above-median equity band is being paid for the upside; the reverse pattern signals a candidate optimising for near-term liquidity, which is a valid choice for a mid-career hire but changes the retention profile.
- **Update the benchmarks quarterly.** Comp curves have shifted materially in each of the last several years; a benchmark from 12 months ago will mislead in either direction.

## The order-of-hire mistakes to avoid

- **Head of FP&A before controller.** Produces reports on top of an untrusted ledger. Every variance discussion turns into "is the actual right?" and stalls.
- **CFO before fractional CFO / controller.** Over-hires the strategic layer without the operating layer to sit on top of. The new CFO spends year one hiring the controller they should have hired first, and then leaves.
- **Treasury lead before there is cash to manage.** The role is under-utilised; the hire under-performs against expectation; the CFO explains the mis-hire in a comp-committee cycle.
- **Head of IR before the dual-track is real.** Signals to the market a track that has not been decided; over-hires against private-company IR needs.
- **VP People / Chief of Staff hire disguised as a finance role.** Every finance leader has been tempted to hire the highly-competent generalist who will "make things work"; if the underlying role is people-ops or business-ops, name it that and hire against a people-ops or business-ops benchmark, not a finance one.

## Summary

- The canonical ten-hire sequence: outsourced bookkeeper → fractional CFO → controller → first FP&A analyst → Head of Accounting → treasury lead → tax lead → Head of FP&A → Head of IR → CFO team-of-team.
- Each hire has a specific stage trigger — a stack graduation, a headcount threshold, an audit / IPO milestone, or a cash-pile / tax-profile inflection.
- Comp is benchmarked against Carta / Pave / Option Impact / Radford; read the *function*, the *stage*, the *geography*, and *cash-plus-equity together*, and refresh the benchmarks quarterly.
- The order-of-hire mistakes to avoid: FP&A before controller, CFO before operating layer, treasury before there is cash, IR before dual-track, disguised people-ops hires.
- By Series-C+, the CFO is running a team-of-teams; the individual finance work of earlier stages is done three levels down.

Chapter 3 turns to the discipline this team runs to: the month-end close.
