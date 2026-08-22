# ESOP Top-Ups and Pool Sizing Through Rounds

## Why this matters

The pool question that produces the option-pool shuffle at Series-A (chapter 2) is really a **sizing** question: how many shares should the pool actually hold, right after the round closes, so that it lasts until the next round without a top-up in the middle? Get it right, and the pool is sized to the hiring plan and lasts 18-24 months. Get it wrong in one direction — oversize now — and the founder pre-dilutes themselves for hires that never happen. Get it wrong in the other direction — undersize now — and 12 months later there is an emergency top-up right before Series-B that dilutes the founder at the *old* Series-A price, missing all the value creation in between.

The cadence is roughly: a pool is created at incorporation, topped up at seed, topped up (usually with the shuffle) at Series-A, topped up at Series-B, topped up at Series-C, and eventually converted or absorbed into a public-company equity plan at IPO. Between rounds, the pool is a running balance: grants come out, occasionally forfeitures come back in, and the CFO watches the "pool remaining" number against the hiring plan the same way the CFO watches cash against burn.

This chapter installs the sizing decision, the benchmarks, the between-rounds monitoring, and the recognition of when a top-up is required outside the round cycle.

## The sizing decision — bottom-up hiring plan vs. top-down benchmark

There are two ways to size the pool at any given round, and both have to be run in parallel because each catches errors the other misses.

**Bottom-up: from the hiring plan.** The 18-24 month hiring plan the CFO built inside the three-statement model ([`mod-103`](../mod-103-three-statement-model-and-driver-based-forecasting/03-hiring-plan-as-the-opex-driver.md)) lists every planned hire with role, level, start month, and department. Each hire has an expected equity grant expressed as a percent of fully-diluted post-close. Sum those grants, add a buffer for over-hiring or upgrades, add a refresh-grant reserve for existing employees at promotion / annual-refresh moments, and you have a pool size in shares.

Worked example. Series-A close with a 12-month hiring plan of 20 hires:

- 2 senior engineers (Staff level) at 0.30% each = 0.60%
- 6 mid-level engineers at 0.10% each = 0.60%
- 3 senior GTM (AE / CSM) at 0.10% each = 0.30%
- 5 mid GTM at 0.05% each = 0.25%
- 2 senior product / design at 0.20% each = 0.40%
- 1 VP Engineering at 0.75% = 0.75%
- 1 VP Sales at 0.75% = 0.75%
- Refresh-grant reserve for existing 20 employees: ~0.30%

Total grant demand: ~3.95%. Add a 20% buffer for upgrades / hard-to-fill roles: ~4.75%. Add a further 20% buffer for the last 6 months of the 18-24 window when the pool cannot yet be topped up: ~5.7% call it 6%.

That is a bottom-up 6% pool ask. Compare to the investor's ask of "12% pool per the Carta benchmark" (chapter 2) — the founder now has a specific counter with a hiring plan behind it.

**Top-down: from benchmark data.** Public sources — the Carta State of Private Markets report, Pave equity benchmarks, Peterson Partners / Compensia comp surveys — publish typical pool sizes by stage. The rough shape as of the mid-2020s:

- **Series Seed:** 10-12% target post-close (relatively larger because the pool must cover the pre-seed team retroactively plus the seed hires).
- **Series A:** 10-15% target post-close (the shuffle chapter default).
- **Series B:** 8-12% target post-close (slightly smaller as grants shrink relative to the growing fully-diluted base).
- **Series C+:** 6-10% target post-close.
- **Pre-IPO:** shrinks further as RSUs (chapter 7) start replacing options and the fully-diluted denominator swells.

The benchmark is a *sanity check*, not a target. A benchmark says "the top quartile of Series-A companies has a 15% pool" but does not say what your specific hiring plan needs. The bottom-up number is what the pool should be; the benchmark tells you if you're wildly off.

<!-- needs-research: verify current-year Carta State of Private Markets pool-size distributions by stage and cite the specific edition once WebFetch is available; Carta publishes a new edition each quarter. -->

**When bottom-up and top-down diverge.** The bottom-up number is smaller than the benchmark in almost every case where the founder has actually built a hiring plan. That is because the benchmark aggregates companies with sloppy planning discipline together with companies that had genuine surprise-hire needs. If the bottom-up is 6% and the benchmark is 12%, the correct move is not to split the difference — it is to have the bottom-up defence in hand and to negotiate the pool down to the hiring-plan number plus a defensible buffer.

## Grant benchmarks by level and function

The bottom-up calculation needs per-hire grant sizes. Two current-generation reference sources:

- **Pave equity benchmarks.** Pave publishes stage-adjusted equity ranges by level (IC1-IC7 / M1-M6), function (engineering, product, design, sales, marketing, ops, finance), and location. The typical shape at Series-A: engineering ICs range from 0.03-0.05% for mid-level to 0.15-0.30% for staff / principal, VPs run 0.5-1.5%, C-suite hires 1-4%.
- **Carta State of Private Markets.** Carta's report covers pool sizes, grant sizes by level, and secondary tender volumes.

<!-- needs-research: Pave and Carta figures vary quarter-to-quarter; verify with the current edition before quoting specific percentages. -->

The founder / CFO's job at the pool-sizing step is not to fix per-hire grant sizes across the whole hiring plan — that is equity-comp *policy* and defers to [`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum). It is to sum the plan's projected grants under a defensible per-hire size and produce a pool number.

The compounding-error trap: a 25-hire hiring plan with grant sizes 20% higher than benchmark creates a pool sizing that is 20% too big, and the founder pays for the whole 20% overshoot in dilution. Undersized per-hire grants create the opposite problem — the pool is too small, the offers get uncompetitive, and the company loses recruiting battles.

## The trade-off — oversize vs. undersize

The over-sizing failure mode: the pool is bigger than the hiring plan requires. Founder pre-dilutes themselves for grants that never happen. The unused pool sits as fully-diluted overhang forever (in Delaware C-corp mechanics, unissued pool shares don't come back — they either get granted, get repurposed for later rounds' pool needs, or sit in the fully-diluted denominator diluting founder ownership). At the next priced round, if the pool from the last round has a large unissued balance, the new round investor may push for a *smaller* pool top-up (because the existing pool covers it), but the founder is already carrying the dilution from the over-sizing at the prior round.

The under-sizing failure mode: the pool runs out before the next priced round, and an emergency top-up is required. This top-up is dilutive at the *current* fully-diluted denominator and — critically — at the *last round's* pricing baseline. If the last round was a $30M pre-money and the company has since 2x'd in value, the emergency top-up dilutes existing holders (founders included) at the $30M valuation, but the value being spent on grants is at the $60M current-baseline valuation. The founder gets the worst of both — dilution now, at old prices.

Worse: an emergency top-up right before Series-B closes signals to the incoming Series-B investor that the founder does not manage the pool with discipline. That is a small negative signal, but negative signals stack.

The right instinct: **size the pool for the shortest defensible hiring plan** (18 months, not 24) **with a modest buffer** (10-20%, not 50%), **and plan for the top-up at each priced round** as the correction mechanism.

## The between-rounds pool-monitoring cadence

Between priced rounds, the pool is a running balance the CFO tracks monthly or quarterly. The mechanic:

- **Opening balance:** pool remaining at start of period, in shares.
- **Grants issued:** grants approved by board consent during the period, in shares (from the option-grant register / Carta grant activity).
- **Forfeitures:** grants returned to the pool when an employee leaves before vesting (or during a post-termination window if they don't exercise). This usually adds shares back.
- **Closing balance:** opening − granted + forfeited.

The "pool remaining" number belongs on the board KPI dashboard next to cash and runway. When pool remaining hits ~20% of the pool's initial size, or covers less than the next 4-6 months of the hiring plan, the CFO needs to be planning the top-up mechanism — either a board-authorised top-up between rounds (requires stockholder consent because it amends the equity incentive plan) or a top-up at the next priced round.

A **standalone top-up between rounds** is uncommon but possible: the board and stockholders approve an amendment to the equity incentive plan to increase the pool by X shares. The amendment requires majority stockholder consent (which usually includes the preferred investors' consent), which means the CFO is negotiating the top-up amount with the existing investors, who may push back because the top-up dilutes them without a fresh cash injection. This is why the between-rounds top-up is usually avoided unless absolutely necessary.

A **top-up at the next priced round** is the standard mechanism. The incoming round's term sheet specifies the target pool percent post-close, and the top-up is the delta between existing pool and the target. The option-pool shuffle (chapter 2) then determines whether the top-up is founder-dilutive (pre-money) or all-parties-dilutive (post-money).

## Refresh grants — the pool driver founders forget

The bottom-up hiring plan captures new hires. It usually forgets **refresh grants** — additional equity granted to existing employees at annual-review time (annual refreshes), at promotion moments (promo grants), and to key employees at retention-risk moments (retention grants).

Rough sizing:

- **Annual refresh:** typically 25-50% of the original new-hire grant amount, granted annually starting 2-3 years after the initial grant. Purpose: keep the employee's *unvested* equity pool at roughly the same level as the day they joined, so they have as much reason to stay in year 4 as in year 1.
- **Promotion grant:** a one-time top-up when an employee is promoted, sized to bring their equity to the new-hire level for the new title (i.e., what the company would grant a new hire coming in at the new level, less what they already have unvested).
- **Retention grant:** used sparingly when a key employee is a flight risk, sized to whatever it takes to change the calculation. Usually a board-conversation-level grant.

For a 30-person team at Series-A, refresh grants can easily consume 0.5-1.0% of fully-diluted per year — a meaningful line in the pool-sizing calculation that founders regularly miss. A pool sized for hires-only will run out early, at which point the emergency top-up conversation starts.

The refresh policy itself is *policy*, not economics — it defers to `startup-operations-governance-curriculum`. But the *shares* the policy consumes come out of this module's pool.

## The pool per-round cadence — a worked story

Follow a company from formation to Series-B:

**Formation.** 10,000,000 authorised common. 8,000,000 issued to two founders. **Board reserves 1,000,000 for the pool** — 11.1% of pre-money fully-diluted. No grants yet.

**Seed round.** Company raises $2M on a $8M pre-money post-money SAFE (converts at next round) plus $1.5M priced Seed at $10M pre. Between formation and seed, the company hired 8 people and granted ~250,000 options; ~50,000 forfeited when two of the 8 left. Pool remaining: 800,000. The priced Seed's term sheet requires 12% post-close pool. Top-up needed: (12% × post-close FD) − 800,000. Working through the math ends up needing ~600,000 top-up shares at the seed close, which is the founder-dilutive cost of the pool refresh. Post-seed pool: 1,400,000 shares, ~12% of post-close FD.

**Between Seed and Series-A (18 months).** Team grows from 15 to 40. Grants issued: ~900,000. Forfeitures: ~100,000. Pool remaining at start of Series-A discussions: ~600,000, which is roughly 3% of the current FD — enough for a couple more hires but nowhere near enough to run the 18 months to Series-B.

**Series-A.** Term sheet: $10M on $30M pre / $40M post with **10% post-close pool**. Existing pool of 600,000 shares needs top-up to hit 10% of post-close FD. The negotiation of pre-money vs. post-money placement (chapter 2) determines whether the top-up is founder-dilutive or shared. Post-Series-A the pool is at 10% target and starts running down again.

**Between Series-A and Series-B (18-24 months).** Same pattern — pool consumed by hiring plan plus refreshes, monitored on the KPI dashboard, expected to be near-empty by the time Series-B is being discussed.

**Series-B.** Term sheet: 8% post-close pool. Top-up mechanics repeat.

By Series-C or so, the RSU discussion (chapter 7) starts to displace new options grants, and the pool discussion shifts. But the *pool-monitoring* mechanic — treat it like cash, watch the balance, plan the top-up at the next round — persists all the way to the pre-IPO equity plan conversion.

## The board / stockholder mechanics

The pool cannot be expanded by CFO decree; it requires **board approval** to amend the equity incentive plan and, for material changes, **stockholder consent** (majority of common, and typically majority of each preferred series voting separately per the plan protective provisions).

The mechanics:

1. **Draft an amendment to the equity incentive plan** raising the share reserve by X shares.
2. **Board consent** approving the amendment (all board members' signature).
3. **Stockholder consent** (or vote at annual meeting) approving the amendment. Preferred investors' protective provisions (mod-108) typically require their consent for any increase in the pool above a certain size.
4. **Update the cap table** and the corporate record with the amended plan and the new pool balance.
5. **Update the Rule 701 aggregate calculation** (chapter 6) — the pool expansion is not itself an issuance, but future grants against the expanded pool will consume Rule 701 capacity.

Missing step 3 is the failure mode. A CFO / GC who grants against a pool that has not been properly authorised is granting options that don't exist — a mess to unwind at diligence.

## What good looks like

- The pool has a shares number on the cap table, not just a percent.
- The bottom-up hiring plan explicitly generates the pool ask each round, with the plan attached to the board pack.
- The refresh-grant policy is a documented driver in the pool calculation.
- The pool remaining is on the monthly board KPI dashboard next to cash.
- The between-rounds top-up trigger is documented (e.g., "top-up conversation begins when pool remaining < 4 months of planned hires").
- The top-up cadence is planned to align with priced rounds; emergency mid-round top-ups are avoided.
- Every top-up has a board consent and stockholder consent in the corporate record; every amendment to the equity incentive plan is filed.
- The next round's expected pool top-up is modelled in the founder's post-round cap-table scenario (chapter 2).

## Summary

- Pool sizing at any priced round is a bottom-up hiring plan question first, a benchmark-check question second. The benchmark is a sanity check, not a target.
- The over-sizing failure mode is pre-dilution for hires that never happen. The under-sizing failure mode is an emergency top-up right before the next round that dilutes founders at the *old* round's valuation, missing the interim value creation.
- Refresh grants — annual refresh, promotion grants, retention grants — are a real driver of pool consumption that founders regularly miss. A pool sized for hires-only will run out early.
- Between rounds, the pool is a monthly-monitored running balance: opening minus granted plus forfeited equals closing. The number belongs on the board dashboard next to cash.
- Between-rounds top-ups are possible but usually avoided; the standard cadence is to top up at each priced round.
- Every pool change requires board consent and stockholder consent per the equity incentive plan protective provisions; grants against an improperly authorised pool are the mess a CFO does not want to unwind at diligence.

Chapter 4 turns to the liquidation waterfall: the exit-analysis mechanic that determines who gets what when the company is sold, and why "sale above the last round's valuation" is not always a founder win.
