# Exercise 01 — Monthly Investor Update Authoring

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 1 (the monthly investor update — the signal channel between board meetings). Familiarity with mod-102 (KPI definitions) and mod-103 (driver-based model) helps but is not required; this exercise trains the *authoring discipline* against the four-part structure.

## Problem statement

You are the CFO of a Series-A B2B SaaS company. Author three consecutive monthly investor updates — one on-plan month, one miss month, one ask-heavy month — for the same underlying company. Each update follows the chapter-1 four-part structure (top KPI, ask, risks, wins and losses), is written in the signal voice (specific numbers, named causes, explicit interpretation, no adjectives that sell), fits on one page of prose plus one page of charts, and lands on a predictable business-day-10-15 cadence.

The exercise trains three linked skills at once: the voice discipline, the miss-month discipline, and the ask-authoring discipline. All three fail differently, and all three have to be practiced against the same running company narrative so that the reader (a hypothetical investor) sees the trajectory across three months, not three unrelated one-pagers.

## Scenario — build your own running company

Author the company context you will write the three updates for. Anonymise if using a real company.

**Company context.** B2B SaaS, currently at $2.8M-$4.5M ARR, growing 5-10% MoM, 25-40 employees, closed a $9-15M Series-A 6-10 months ago at a $35-55M post-money. Existing investor set: one Series-A lead (with a board seat and pro-rata rights), one Series-A co-investor (no board seat, board observer), the seed lead (board observer, pro-rata rights up to a threshold), an accelerator, and 4-8 angels. Current cash on hand $6-11M with $500K-$800K monthly burn, giving 10-18 months of runway on the current plan.

Document the company context on a "context" page: name (fictional), stage, ARR at the start of the three-month window, headcount, cash / burn / runway, product category in one sentence, top three KPIs the board tracks (ARR, NRR, gross margin, or company-appropriate equivalents), and the annual plan target (ARR at year-end, headcount at year-end, cash-out date projected). This context page is the internal reference you will write the updates against; it does not go into any update.

**The three months.** Author the following three-month trajectory:

- **Month N (on-plan).** ARR grew 7% MoM, on plan; pipeline coverage healthy; two hires closed; one product ship. Nothing dramatic. This is the month that tests whether you can write an on-plan update without either padding it (marketing voice) or making it sound boring in a way that reads as unengaged.
- **Month N+1 (miss).** ARR grew 3% MoM against a plan of 7%. Net-new ARR was $95K against a plan of $220K, driven by one enterprise deal slipping and one committed logo churning unexpectedly. Cash and burn on plan. This is the month that tests the honest-signal discipline against the founder / CEO's likely desire to soften.
- **Month N+2 (ask-heavy).** ARR growth recovered partway to 5% MoM (still below the 7% plan). The CFO-CEO team is now actively targeting three specific asks: two named exec hires (VP Sales and Head of Product Marketing), warm intros to five named enterprise prospects, and a specific feedback request on a strategic decision (whether to open a European sales beachhead in Q4 or defer to Q1 of the following year). This is the month that tests the one-specific-ask-per-month discipline being deliberately violated for a well-justified reason.

## Requirements

Produce a submission directory with the following.

1. **The company-context page** (`company-context.md`). One page. All of the fields above.

2. **The three monthly updates** (`update-month-N.md`, `update-month-N+1.md`, `update-month-N+2.md`). Each update is:
   - One page of prose in the four-part structure: top KPI, ask, risks, wins and losses.
   - One page of charts (or a chart-page description if you do not have chart-rendering tooling): four to six charts covering ARR, monthly cash, headcount, top-of-funnel or pipeline, cohort retention or NRR, and optionally a product-usage or engagement metric. Zero-based Y-axes; current-month callouts; consistent chart types across all three months.
   - Written in the signal voice per chapter 1. Specific numbers. Named causes. Explicit interpretation.
   - A subject-line and a from-address at the top (as if it were the email being sent).
   - A distribution-list note at the bottom (BCC-full-list or personally-addressed via mail-merge, per chapter 1).

3. **The KPI-definition footnote** (in each update, or as a separate `kpi-definitions.md` referenced from each update). For each KPI you cite in an update, the exact calculation, the source of the underlying data, and the update cadence. This is the discipline that closes definitional drift across months.

4. **The self-review memo** (`self-review.md`, 1 page). After you have drafted the three updates, review your own drafts against these questions:
   - Does the top KPI section of the miss-month update name the miss in the header, or is it buried?
   - Does the miss-month update over-commit to making up the shortfall?
   - Does the miss-month update contain a "silver lining" sentence? If yes, cut it.
   - Does every update contain exactly one specific ask (or, in the ask-heavy month, does the multiple-ask structure explicitly justify why this month breaks the one-ask rule)?
   - Does the voice sound like the CFO writing to a peer, or like a marketing page?
   - Are chart types and Y-axis conventions consistent across the three months?
   - Would the reader of the three updates in sequence form a coherent trajectory picture?
   - Rewrite any section that fails one of these tests, and document the rewrite in the self-review memo.

## Starter guidance

- **Read chapter 1 in full before drafting anything.** The four-part structure and the voice discipline are the whole exercise. Attempting the drafts without a re-read produces the two common failure voices (marketing and status-report) rather than the signal voice.
- **Write the miss-month update first, not the on-plan update first.** The on-plan month is easier to write in the signal voice once you have already committed to naming a miss clearly. Reversing the order produces a marketing-voice on-plan update that then makes the miss-month rewrite jarring.
- **Draft the update to a specific investor in your head, by name.** Chapter 1's discipline: write to your Series-A lead specifically, then remove the salutation. If you cannot picture the specific investor, invent one — a persona, with a specific background and a specific set of concerns.
- **Cut every adjective that sells the number.** "Strong," "impressive," "record," "exciting," "significant," "meaningful" — none of these belong in the signal voice. The number carries its own weight; adjectives read as either padding or as an attempt to persuade.
- **In the miss month, resist the "let me walk you through the mitigation plan" pivot.** Name the miss first. Explain the cause. State the operational response *last*. Reversing the order softens the miss and reads as spin.
- **In the ask-heavy month, be explicit about why the month breaks the one-ask rule.** "This month has three specific asks because the exec-hiring window and the customer-development window are aligning simultaneously" is a defensible frame; three asks with no meta-commentary reads as an unstructured wishlist.
- **Cite specific metrics on the charts.** The current-month value gets a callout label on every chart, so the reader does not have to read a table to see the number. The plan line or the trailing-three-month trend appears as a dashed line.
- **Do not fabricate benchmark comparisons.** If the update references SaaS-benchmark data ("our NRR is above the SaaStr median"), the citation must be to a specific report and vintage; if you cannot cite it, cut the comparison rather than invent it. Flag any unsourced comparison with `<!-- needs-research: ... -->`.

## Acceptance criteria

- **Three updates, one context page, one KPI-definition footnote or file, one self-review memo.** All present in the submission.
- **Every update fits on one prose page plus one chart page.** No 10-page decks.
- **Every update contains the four-part structure** in order: top KPI, ask, risks, wins and losses. No structural drift across the three months.
- **The miss-month update names the miss in the top-KPI section header**, not buried in prose. Specific number. Specific attributed cause. Specific operational response, placed *after* the acknowledgement of the miss.
- **Every update contains one specific ask** (or, in the ask-heavy month, the multiple-ask structure is explicitly justified in one sentence at the top of the ask section).
- **The chart page is consistent across the three months.** Same chart types. Zero-based Y-axes. Current-month callouts. Plan or trailing-trend line on the top KPI chart.
- **The voice is the signal voice.** Specific numbers, named causes, explicit interpretation, no selling adjectives. Have a peer read the three updates back-to-back and confirm they do not read as marketing.
- **The KPI-definition footnote or file exists and covers every KPI cited.** The reader can trace every number in every update to a defined calculation.
- **The self-review memo names at least three specific rewrites** the initial draft required to pass the four-part-structure and signal-voice tests, or explicitly notes that the drafts passed on the first attempt (uncommon; be honest).

## Deliverables

- `company-context.md` — the internal context page.
- `update-month-N.md` — the on-plan update.
- `update-month-N+1.md` — the miss-month update.
- `update-month-N+2.md` — the ask-heavy update.
- `kpi-definitions.md` — (optional standalone; may be embedded in each update).
- `self-review.md` — the post-draft review memo.

## Extensions (optional)

- **The engagement-tracking layer.** Draft the CFO's internal tracking sheet for investor engagement across the three months: which investor opened which update, which investor replied to which ask, which investor requested a follow-up call. Add a fourth-month "engagement debrief" memo the CFO takes into the CEO 1:1, identifying which investors are actively engaged and which have gone quiet.
- **The ad-hoc note.** Between the on-plan month (N) and the miss month (N+1), draft an ad-hoc update reflecting a specific material event: a customer win with a marquee logo, or a senior departure that pre-dates the miss month. Practice the "clearly labelled ad-hoc, does not substitute for the monthly cadence" pattern from chapter 1.
- **The fundraise-shift.** In month N+2, the CFO-CEO team has decided to open a Series-B raise in the next quarter. Shift the update cadence to weekly for the four weeks following month N+2. Draft the first two weekly updates. Practice the raise-window cadence exception per chapter 1.
- **The retrospective.** After the three updates are written, draft a one-page retrospective that a Series-B lead investor's associate might write after reading all three, plus the ad-hoc if you did the extension. What signal does the sequence carry? Would the associate recommend the raise proceed? Trains the reading of updates *from the receiving side*.
- **The two-list distribution split.** Draft the CFO's rationale for how the three updates are split between the "cap table" list and the "priority" list. Include the specific investors on each list and the specific-ask sensitivity of the ask-heavy month (some asks may go only to the priority list rather than the full list).
