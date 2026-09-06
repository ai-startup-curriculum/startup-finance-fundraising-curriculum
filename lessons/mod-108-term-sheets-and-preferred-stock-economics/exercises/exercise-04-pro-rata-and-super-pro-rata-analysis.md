# Exercise 04 — Pro-Rata and Super-Pro-Rata Analysis

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 5 (pro-rata, super-pro-rata, lead-pro-rata; the compression math). Uses [`mod-104`](../../mod-104-cap-tables-and-equity-compensation/) chapter 1 (four-share-count discipline) and [`mod-107`](../../mod-107-fundraising-strategy-and-investor-targeting/) chapter 1 (round-sizing).

## Problem statement

Model the pro-rata absorption of a Series-B round by the Series-A investor stack, then simulate a super-pro-rata request from the Series-A lead. Produce the "how much room is left for the new Series-B lead" table across three round-size scenarios. Author the memo the CFO writes to the CEO and the incoming Series-B lead explaining the specific absorption math and the negotiation asks.

The exercise trains the specific arithmetic that founders and CFOs most frequently get wrong at the Series-B stage: the assumption that a "$30M Series B" leaves $30M of allocation to the new lead. It rarely does. Pro-rata rights held by the Series-A stack absorb some of the round; super-pro-rata requests absorb more; and if the CFO has not modelled the absorption before agreeing the round size, either the round is under-allocated to the new lead or oversized against the founder's target dilution.

## Scenario — post-Series-A close

Use this specific cap table as the starting state.

**Post-Series-A close.**

- Common: 8,000,000 shares.
- Options granted: 1,500,000 shares. Unissued pool: 500,000 shares.
- Series A Preferred: 2,000,000 shares. Raised $10,000,000 at $5.00 per share.
- Broad-based fully-diluted: 12,000,000 shares. Series-A as-converted: 16.67%.
- Series-A investor composition:
  - Lead A: $6,000,000 (1,200,000 shares, 60% of round). Pro-rata rights on a fully-diluted basis, no super-pro-rata reserved. Major-Investor threshold met.
  - Follower A1: $2,000,000 (400,000 shares, 20%). Pro-rata rights, MI threshold met.
  - Follower A2: $1,500,000 (300,000 shares, 15%). Pro-rata rights, MI threshold met.
  - Follower A3: $500,000 (100,000 shares, 5%). No pro-rata rights (below MI threshold).

**Series-B round (the negotiation-in-progress).**

- Company plans a Series B at approximately $90M pre-money / $30M new money / $120M post-money (baseline scenario).
- Series-B price per share: `$90M / 12,000,000` = $7.50 per share (pre-money on FD, no pool top-up in the baseline; model the pool top-up as an extension).
- Series-B shares issued at baseline: `$30M / $7.50` = 4,000,000 shares.
- New Series-B lead is targeting a $25,000,000 cheque and a target ownership of 20% post-close.

## Requirements

Produce a workbook (four tabs) plus the CFO memo.

1. **Setup tab.** The starting cap table, the Series-A investor composition with pro-rata parameters, the Series-B baseline assumptions, and three round-size scenarios (below).

2. **Baseline pro-rata absorption tab.** For each Series-A holder with pro-rata rights, compute:
   - The pro-rata percentage using the FD-total denominator: `(holder's shares as-converted) / (total FD as-converted)`.
   - The pro-rata invitation in dollars and in shares for the Series-B round.
   - The assumed exercise rate. Model three exercise scenarios: (a) all pro-rata exercised; (b) 50% exercised (lead exercises full; followers exercise half); (c) minimum exercised (lead exercises full; followers waive).
   Under each of the three exercise scenarios, compute:
   - Aggregate Series-A pro-rata dollars taken up.
   - Aggregate Series-A pro-rata shares.
   - Remaining "room" for the new Series-B lead (in dollars and in target-ownership percentage post-close).

3. **Super-pro-rata scenario tab.** Assume the Series-A lead asks for super-pro-rata rights in the Series-B round, defined as "up to 2x pro-rata." Model:
   - The lead's super-pro-rata invitation ($ and shares).
   - The lead's likely exercise (assume the lead takes the full super-pro-rata).
   - The new remaining room for the incoming Series-B lead.
   - The comparison against the baseline pro-rata: how many pp of target Series-B lead ownership does the super-pro-rata absorb?

4. **Round-size sensitivity tab.** Model three round sizes at the same pre-money and per-share price:
   - Scenario 1: $20M new money / $110M post-money.
   - Scenario 2: $30M new money / $120M post-money (baseline).
   - Scenario 3: $40M new money / $130M post-money.
   For each round size, run the baseline pro-rata absorption (all exercised, 50% exercised) and the super-pro-rata scenario (lead takes full 2x pro-rata). Produce a table showing the incoming Series-B lead's remaining room in each of six cells (three round sizes × two exercise scenarios), plus the super-pro-rata overlay.

5. **CFO memo** (`pro-rata-memo.md`, 1-2 pages). Written to the CEO and the incoming Series-B lead's counsel. Structure:
   - **Bottom-line summary.** One paragraph: "At the baseline $30M round, with all Series-A pro-rata exercised, the incoming Series-B lead has $X of allocation available toward its $25M target — a shortfall of $Y. If the Series-A lead requests super-pro-rata, the shortfall grows to $Z."
   - **The three options.** Option 1: hold the round size at $30M and ask Series-A holders to waive pro-rata to make room. Option 2: expand the round to $40M so that the incoming lead's $25M fits inside. Option 3: negotiate the Series-A lead's super-pro-rata request down to 1.25x pro-rata (or reject). For each: the specific consequence for the CEO, the incoming lead, and the founder's dilution.
   - **The negotiation asks.** For the incoming Series-B lead: "we can offer $X of allocation at a $30M round without pro-rata waivers; we can offer $Y if we expand to $35M." For the Series-A lead: "we ask you to exercise pro-rata but not super-pro-rata."
   - **The Voting Agreement / IRA drafting implication.** Which specific clause the CFO will edit going forward to prevent the same problem at Series C. (Pro-rata denominators, MI threshold, super-pro-rata carve-outs, waiver mechanics.)

## Starter guidance

- **Watch the pro-rata denominator carefully.** The baseline definition is `holder-FD-shares / total-FD-shares × new-issuance`. Some drafts use `holder-preferred-shares / total-preferred-shares × new-preferred-issuance`, which is much bigger. Chapter 5 walks the difference; the exercise assumes the FD-total denominator throughout (this is the market-standard NVCA form). Note the alternative in the memo.
- **Model exercise rates realistically.** The lead almost always exercises pro-rata; followers exercise sometimes; MI-threshold-failing holders have no pro-rata to exercise. Do not assume 100% exercise as the base case; model the range.
- **Super-pro-rata is denominated in "multiples of pro-rata," not in "additional %."** A 2x super-pro-rata means the lead can buy up to 2× its pro-rata invitation. The absolute dollar amount depends on the round size, not on a fixed cheque.
- **The incoming Series-B lead's target is a target-ownership percentage, not a target dollar amount.** A $25M cheque at $120M post is 20.83% ownership. If pro-rata absorbs $10M of the round, the incoming lead can only buy $20M — 16.67% ownership at $120M post. The gap between "target ownership" and "achievable ownership" is the specific number the memo must surface.
- **Sensitivity: pool top-up.** In the baseline, ignore the pool top-up. In an extension, add a top-up to 10% post-close and remodel. The top-up shifts the pre-money-per-share and the shares-issued math, which in turn shifts the pro-rata invitations.
- **Do not confuse pro-rata with anti-dilution.** They are two different clauses that both fire on new issuances; pro-rata gives the right to *invest* to maintain ownership, anti-dilution *adjusts the conversion price* if the new issuance is below the earlier price. This exercise is pro-rata only; exercise 03 was anti-dilution.

## Acceptance criteria

- **The pro-rata invitation for each Series-A holder is correctly computed** using the FD-total denominator. Reconcile: sum of pro-rata invitations ≤ aggregate Series-A FD share × Series-B $ raise.
- **The three exercise scenarios (all / 50% / minimum) produce distinct remaining-room outcomes** for the incoming lead. Direction: more exercised → less room.
- **The super-pro-rata scenario correctly models 2x pro-rata for the lead** and holds the followers at 100% baseline pro-rata.
- **The round-size sensitivity table has all six cells populated** with remaining-room dollars and target-ownership-percentage.
- **The memo names the three options** with a specific consequence for each.
- **The memo makes a specific recommendation** among the three options, with justification.
- **The memo names the IRA / Voting Agreement drafting change** that should happen at the Series-B close to prevent the same issue at Series C.
- **No fabricated market data.** Any incidence claim (e.g., "super-pro-rata is uncommon at Series-A") cited to a specific report or flagged `<!-- needs-research: ... -->`.

## Deliverables

- The workbook (`.xlsx` or Google Sheets link) with tabs: setup, baseline-absorption, super-pro-rata, round-size-sensitivity.
- The CFO memo (`pro-rata-memo.md`).

## Extensions (optional)

- **Add a pool top-up.** Series-B lead requires the pool to be re-topped to 10% post-close (pre-money placement). Recompute the pre-money-per-share and the pro-rata invitations. Show the specific pp of change to the incoming lead's remaining room.
- **Add a lead-pro-rata clause.** Instead of a super-pro-rata for the Series-A lead, model a "lead pro-rata": a specific fixed cheque size ($3M) reserved for the Series-A lead in the Series-B round, regardless of pro-rata percentage. Compare the two mechanics.
- **Model an insider-led "inside round" scenario.** No new Series-B lead; the Series-A holders alone finance a $12M bridge-to-Series-B on flat pre-money. All Series-A holders exercise pro-rata. Show the founder-dilution and the cap-table impact.
- **Model an unassignable pro-rata.** Some Series-A holders (like small angels or accelerator funds) hold pro-rata rights that cannot be assigned. Show the specific problem this creates when the fund declines to exercise but the incoming Series-B lead would have paid the pro-rata to acquire the right.
- **Preview Series-C compression.** Assume the Series-B closes at $30M with 50% Series-A pro-rata exercise. Roll the cap table forward to a Series-C at $60M raised on $250M pre-money. Model the aggregate Series-A + Series-B pro-rata absorption on Series C. Preview of the "pro-rata compression grows across rounds" pattern.
