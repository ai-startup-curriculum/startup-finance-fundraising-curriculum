# Exercise 01 — Round Sizing Against the Milestone Bar

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 1 (sizing against the milestone bar), plus prior familiarity with the driver-based three-statement model (mod-103) and cohort unit economics (mod-102).

## Problem statement

Size two rounds — a seed and a Series-A — against the next-round milestone bar, not against a target dilution or a market-median round-size norm. For each round, produce the four-step sizing output from chapter 1: the validated next-round bar, the operating plan that clears it, the cost of the plan, and the milestone buffer. Then produce a founder-facing sizing memo that defends the number.

The point of the exercise is to install the discipline of sizing as the *output* of a milestone-bar-plan rather than the *input*. Naïve sizing ("we'll raise $5M because that's the norm") is a specific failure mode that shows up 12-24 months later at the next raise. Doing the four steps end-to-end for two rounds — one seed, one Series-A — installs the muscle for both.

## Scenario — build your own

Pick two hypothetical companies, or one real company with anonymised numbers plus one hypothetical, meeting the following shape.

**Company A — pre-seed / seed candidate.**

- B2B SaaS or B2B fintech, currently at $150K-$400K ARR.
- Founding team of 2-4, at least one design-partner customer.
- Product in early customer use, not yet a repeatable sales motion.
- Planning to raise its first institutional priced round (seed).
- Prior capital: some combination of SAFEs from angels / accelerator; nothing priced yet.

**Company B — Series-A candidate.**

- B2B SaaS, currently at $1.5M-$3M ARR, growing 5-10% MoM.
- Team of 15-30 across engineering, GTM, and G&A.
- NRR 100-120%, GRR 80-95%, gross margin 65-80%.
- Has raised a prior seed ($3M-$6M range) 15-24 months ago; that runway is now 4-9 months from cash-out.
- Planning to raise a Series-A in the next 3-6 months.

The specific numbers do not need to be realistic in every dimension, but each company should be internally consistent and detailed enough to build an operating plan against. Document the starting-state numbers on a "context" tab of the sizing workbook.

## Requirements

Produce, for each of the two companies, a sizing workbook (spreadsheet, Excel or Google Sheets) and a sizing memo (Markdown), plus a naïve-sizing comparison and a joint-lessons memo. Specifically:

### For each company (A and B):

1. **Step 1 — Next-round bar.** Write down the specific KPIs and thresholds the next round (Series-A for company A; Series-B for company B) requires the company to clear. Include:
   - The ARR (or equivalent) threshold.
   - The growth-rate expectation at that ARR band.
   - NRR / GRR expectations.
   - CAC-payback and burn-multiple expectations.
   - Any sector-specific benchmarks (Rule of 40 for later stages; engagement metrics for consumer; take-rate for marketplace).
   - The specific source of each expectation — a citable practitioner report, an investor blog, or a "hypothetical partner conversation" (mark hypothetical explicitly and describe what a real partner conversation on that KPI would ask). Use `<!-- needs-research: ... -->` on any expectation you cannot cite to a specific published source.
2. **Step 2 — Operating plan.** Build a monthly driver-based operating plan over 18-24 months from the current-state numbers to the next-round bar. At minimum:
   - Monthly ARR trajectory from current to next-round bar with a specific growth path.
   - Hiring plan by function (engineering, GTM broken into AE / SDR / CS, G&A) with month-by-month adds and fully-loaded costs.
   - GTM funnel (leads → SQLs → opps → wins) that supports the ARR trajectory (mod-103 exercise 03).
   - Non-payroll opex by function.
   - Working capital drivers (DSO, DPO, deferred revenue if annual-prepay is in the mix).
3. **Step 3 — Cost the plan.** Produce a monthly cash-flow view of the plan showing:
   - Gross burn by month.
   - Net burn by month (gross burn minus revenue).
   - Cumulative burn over 18 months and over 24 months.
   - Peak monthly burn and the month it occurs.
   - Cash-out date under the current cash balance without a new raise.
4. **Step 4 — Milestone buffer.** Add 3-6 months of buffer on top of the plan (justify the specific buffer chosen — 3 months for a fast-moving cheap-to-run plan, 6 months for a hardware or long-sales-cycle plan). Compute:
   - Buffer months × peak-months burn = buffer $.
   - Total round size = plan burn + buffer.
5. **Naïve-sizing comparison.** Independently compute the round size you would arrive at under each of the three canonical wrong framings from chapter 1:
   - Target-dilution framing: "we want to sell 20% at the market-standard pre-money for the stage — what round is that?"
   - Target-valuation framing: "we want a specific headline valuation number — what round is that at 20% dilution?"
   - Round-size-norm framing: "seed is $5M, Series-A is $15M — what would that round look like against the plan?"
   Show the delta between each naïve number and the milestone-bar number and diagnose the specific mismatch (over-raise or under-raise), plus the specific downstream cost at the next round.
6. **Sizing memo (Markdown, 1-2 pages per company).** Author a memo to the CEO and board defending the sizing. Structure:
   - **Recommended round size** and the summary sentence.
   - **The next-round bar** (KPIs, source).
   - **The operating plan** in one paragraph — the specific things the plan funds.
   - **The buffer justification.**
   - **What we deliberately did not size for** (the "why we're not raising $X million" section, referencing the naïve-sizing comparison).
   - **What signals a re-sizing** — the specific triggers (market conditions moving; hiring plan slipping; a new market-facing partner input) that would cause the CFO to re-open the sizing.

### Cross-company:

7. **Joint-lessons memo (Markdown, half page).** In one memo, list the three most useful lessons from doing the sizing for one seed and one Series-A back-to-back — specifically, what changes across stages (chapter 9 preview) about how the sizing conversation runs.

## Starter guidance

- **Start with the bar, not the plan.** The specific temptation is to jump to "how much do we want to raise" and back-solve. Resist. Write down the specific KPIs the next round needs to clear first, and only then start building the plan.
- **Use current-vintage benchmarks.** Practitioner benchmarks (Point Nine's Series-A Napkin, OpenView SaaS Benchmarks, Bessemer's State of the Cloud, DocSend's Startup Fundraising Report) refresh annually. Use the most recent published values, and cite the year explicitly. If a benchmark cannot be sourced to a current-vintage published number, mark it with `<!-- needs-research: ... -->` and describe what a target-partner conversation would confirm.
- **Build the plan monthly, not annually.** An annual plan hides the peak-burn month, which is where the buffer sizing actually matters. Use monthly columns for both companies.
- **Separate gross and net burn.** Gross burn is what the fund's associate underwrites against ("how expensive is this to run"); net burn is what the runway calculation runs against. Both matter.
- **Compute the peak, not the average.** Sizing to average burn under-funds the peak months. Size to peak.
- **Do the naïve comparison honestly.** The point is to show the founder how much they would have raised under a naïve framing and where the delta comes from. Do not stack the deck against the naïve numbers; use market-median pre-moneys for the target-dilution framing.
- **Keep the memo short.** A one-to-two-page memo defends a number; a five-page memo obscures it.

## Acceptance criteria

- **Both companies have a documented, sourced next-round bar** with the specific KPIs, thresholds, and citation-or-`needs-research` tags per number.
- **Both companies have a monthly operating plan** with hiring, revenue, and burn built up from drivers, not aggregated at the annual level.
- **Both companies have peak-burn and cumulative-burn identified** for 18 months and 24 months separately.
- **Both companies have a specific milestone buffer** with the buffer months and buffer $ justified.
- **Both companies have a naïve-sizing comparison** covering the three canonical wrong framings, with the delta and downstream cost identified.
- **Both companies have a sizing memo** in the specified structure, defending the number.
- **The joint-lessons memo** identifies three specific cross-stage differences in the sizing conversation.
- **Sources cited or marked `needs-research`** for every benchmark or partner-conversation input.
- **The round size is the output of the four steps, not backed into.** The workbook and memo show the arithmetic; the number is derived, not asserted.

## Deliverables

- Two sizing workbooks (one per company) as .xlsx or Google Sheets links.
- Two sizing memos (one per company) as Markdown.
- One naïve-sizing comparison document (Markdown, half page per company).
- One joint-lessons memo (Markdown, half page).

## Extensions (optional)

- **Sensitivity on the buffer.** Model the plan under a 20% hiring-plan slip and show the required buffer to still land above cash-out. Update the sizing recommendation.
- **Sensitivity on the growth rate.** Model the plan under a 25% growth-rate miss (plan says 10% MoM, achieved is 7.5% MoM). Show the ARR trajectory shortfall and the specific bar-clearance risk.
- **Sensitivity on market conditions.** Model the Series-A bar under a "more compressed market" scenario (bar is 20% higher on ARR and 500bps higher on efficiency) and show the operating-plan and round-size impact.
- **Cap-table integration.** For company B, integrate the round-size sizing with the mod-104 cap-table math and show the founder-post-raise ownership under three different pre-money scenarios. Note the trade-off between raising the milestone-bar number vs. taking the market-offered larger round.
- **Bridge alternative.** For company B, model a bridge-and-hold-off alternative (mod-109 preview): what if the company raised a $2M bridge from insiders instead of the full Series-A, ran another 6 months, and re-raised against a $3.5M ARR bar? Show the arithmetic and the trade-off.
