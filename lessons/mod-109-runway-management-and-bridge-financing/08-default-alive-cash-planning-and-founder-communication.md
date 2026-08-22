# Default Alive Cash Planning and Founder Communication

## Why this matters

Every previous chapter in the module has been about a specific capital instrument — the bridge structure, the down-round mechanic, the venture-debt facility, the RBF advance, the growth-stage instrument menu. All of them serve a single higher-level goal: keeping the company alive long enough to reach a milestone that justifies its next-round price. The **default alive** discipline is the frame that makes that goal operationable and — critically — the honest-signal frame that the CFO and CEO use to communicate about it internally, to the board, and to the team.

Paul Graham's 2015 essay *Default Alive or Default Dead* is the reference point. The essay draws the distinction: a startup is **default alive** if, on current growth assumptions and current burn, it becomes profitable before its cash runs out; it is **default dead** if it does not. The founder-numbers slice from `startup-foundations` covered the classification. This chapter layers CFO-grade discipline on top: what the classification actually requires as an operating trigger, how the CFO and CEO run the conversation about it, and how the handoff to `startup-exit-curriculum` fires when the classification cannot be honestly held.

Reference: Paul Graham, *Default Alive or Default Dead?* (October 2015), [www.paulgraham.com/aord.html](https://www.paulgraham.com/aord.html).

## The default alive / default dead classification — the CFO-grade version

Graham's original essay stated the classification informally: **"Assuming their expenses remain constant and their revenue growth is what it has been over the last several months, do they make it to profitability on the money they have left? Or to be more precise, by default do they? The default is what happens if they change nothing."**

The CFO-grade version tightens this:

- **Default alive** means that on the current operating plan (current headcount, current opex, current growth pace on the last three months' KPI actuals), the company reaches sustainable cash-flow positive within the runway available *before* needing to raise. The classification holds on the current base case; a modest shock (customer loss, hiring delay) does not immediately invalidate it.
- **Default dead** means it does not. The company will run out of cash on the current plan, and only a successful raise or a plan change (cost cut, growth acceleration) can change the trajectory.

The load-bearing addition beyond Graham: **on best-case operating KPIs** — that is, if the company hits or beats its current internal plan — the trajectory reaches cash-flow positive within the runway. This is the discipline the CFO enforces. It removes the ambiguity of "well, if we grow 3x from here, we're fine" — the point of the test is that under the company's own current best-case KPIs, does the math work out.

Formally, the test comes down to whether the cumulative sum of monthly cash flows over the remaining runway is greater than or equal to zero, evaluated against the current base-case operating plan. If yes, default alive; if no, default dead. Two supplementary variants:

- **Default alive with runway.** Baseline strict test: default alive on the current plan, with additional runway of six or more months after the crossover point. This is the "genuinely alive" version — the company has real optionality.
- **Default alive but tight.** Default alive but the crossover happens with only a few months of runway to spare. Not fully alive in a practical sense; a modest shock reverts to default dead.

Every CFO's monthly re-forecast pack (chapter 1) includes this classification as one of the top-line metrics, refreshed against the current-actuals base plan.

## The operating trigger — "default alive on best-case KPIs, or explicitly not"

The CFO-grade extension is the **explicit non-alive declaration**. If the company is not default alive, the CFO's monthly pack must state so explicitly, in the following form: **"We are default dead on the current plan. The plan of record is to close a raise of $X by month N. Absent that raise, plan B is [specific plan-B path from chapter 1: insider bridge, venture debt, cost reduction, or the handoff to sale process]."**

That declaration serves three purposes:

- **Prevents drift.** A company that quietly is default dead but does not state so tends to drift into distress. The declaration forces the honesty.
- **Forces the plan-B specificity.** Once the declaration is written, the plan B has to be named and dated. General "we'll figure it out" cannot survive the declaration format.
- **Creates a governance record.** The declaration on the monthly pack becomes the record the board can hold the CEO accountable to. If the plan B does not activate at the trigger, the board can raise the question with a specific reference to the memo.

Conversely, a company that is default alive should state so — and state it against a specific set of best-case KPI assumptions. The CFO does not want the board or the team to assume the company is default alive just because it is quiet on the topic; the declaration is affirmative.

## The founder communication practice

The default alive / default dead conversation belongs at the CEO-CFO level, at the board level, and — carefully — at the broader team level. The failure mode is either extreme: an all-hands announcement of "we are default dead" without a well-formed plan B (creates panic without direction) or complete silence (leaves the team unable to make sensible decisions about their own commitment).

**The disciplined CEO-CFO conversation.** Covered in chapter 1's standing monthly runway meeting. The default alive / default dead classification is the top-line output. If it changes classification, the change is discussed at length. If it stays the same, the confirmation is stated explicitly.

**The board conversation.** The classification is a standing item on the quarterly board deck. The board sees whether the company is default alive, default alive with runway, default alive but tight, or default dead. The board discusses trend (the classification a quarter or two ago; the trajectory forward). If the classification is default dead, the plan B is on the same page — the board does not need to ask "what are you doing about it."

**The team conversation.** Careful. Most teams should not be told "we are default dead" in those words, because it triggers a departure spiral that closes the plan-B window. But the team should be told, in a well-framed way, that the company is raising and that the raise is important to the company's forward path. Founders who overshare create anxiety; founders who undershare create a shock when the eventual reality lands. The middle path — a version of "we are raising a Series-B this half, we're in a strong position to close it, and we're preparing for both a fast close and a slower one" — communicates the reality without inducing departures.

The specific practice: the **quarterly all-hands** or its equivalent includes a "state of the raise" segment when a raise is active or imminent. The founder speaks; the CFO backstops with the specific numbers if appropriate; the message is honest but framed to preserve team focus. Employees who ask specific questions in 1:1s get more specific answers; the general presentation is calibrated to the median employee.

## The founder-communication artifacts

The CFO produces or contributes to several communication artifacts around the default alive / default dead classification:

- **The monthly re-forecast pack.** Includes the classification. Top-line metric. Fresh each month.
- **The board deck (quarterly).** Includes the classification. Includes the plan-B path if default dead. Includes the trigger-timing memo showing distance to each trigger.
- **The investor update (monthly).** For the broader existing investor base — investors beyond the board. Includes the classification indirectly, usually framed as "cash on hand, months of runway, trajectory." Does not require explicit "default dead" language but should be honest.
- **The team-facing "state of the company" quarterly.** Framed to preserve team focus. Founder-delivered, CFO-supported.
- **The bridge / down-round / debt-draw memo.** Any specific transaction the company undertakes to change its trajectory is memorialised. See chapters 2, 3, 4, 5.

The CFO's discipline is that these artifacts are consistent with each other. The board sees "default dead, closing bridge in Q3." The investors see "runway of 6 months, insider bridge closing shortly." The team sees "we're raising this quarter; the process is on track." All three are the same story; the framing differs by audience.

## When to hand off — the boundary with startup-exit-curriculum

Every previous chapter has been about extending the company's life through an ongoing-company capital-instrument selection. There is a boundary. When the runway plan resolves into a decision to **sell** the company, take the company **public** in an **IPO**, or **shut down** the company, the transaction execution work belongs to `startup-exit-curriculum`.

**Signals the handoff is at hand.**

- The CFO and CEO conclude that no realistic capital instrument extends the runway enough to reach the next-round price the company can defend. The company is default dead and the plan-B raise is not going to close.
- A strategic acquisition offer arrives that the board judges preferable to continuing as an independent company.
- The company crosses the growth-and-financial-profile threshold for a viable IPO and the decision is made to run the IPO process.
- The company runs out of cash and the CFO-CEO judgment is that an orderly wind-down or ABC is the best outcome for creditors, employees, and shareholders.

**What the handoff looks like.**

- **Sale process.** The CFO produces the diligence pack — three-statement financials, cap table, contracts library, IP portfolio, employee list, KPI dashboard — that the sale-process banker will use. The transaction execution (banker engagement, buyer outreach, definitive-document negotiation, closing choreography, post-close integration) lives in `startup-exit-curriculum`. This module's contribution is the well-organised financial-and-corporate infrastructure the sale process works from.
- **IPO.** Similar. The CFO produces the S-1-ready three-statement financials, the audited three years of history, the KPI dashboard, and the underwriter-diligence pack. The transaction execution (S-1 drafting, SEC comment cycle, roadshow, book-building, pricing, allocation, closing) lives in `startup-exit-curriculum`. See also [`mod-111`](../mod-111-finance-operations-controls-and-team-design/) for the IPO-readiness dual-track pre-work.
- **Orderly wind-down / ABC.** The CFO produces the current cash-and-obligations schedule, the creditor list, the employee list, the contracts inventory. The transaction execution (ABC agent engagement, sale of assets, closing of accounts, final tax and legal filings) lives in `startup-exit-curriculum`. This module's contribution is the honest declaration at the trigger point that this is now the right path.

The handoff is **explicit**. The CFO does not silently drift the runway plan into a sale process; the CFO writes the transition memo, brings it to the board, and hands the execution work to the relevant advisors (bankers for sale / IPO; ABC agent for wind-down) with clear input from the CEO and the board.

## The founder-communication practice at handoff

When the decision to hand off is made — sale process, IPO run, wind-down — the founder communication is different from the ongoing-company-runway-management communication and needs to be planned with equivalent rigor.

**Sale process.** Sale processes are typically not communicated to the broader team until well into the process, because a leak damages the process economics. The CFO and CEO communicate to the board first, to key executives selectively, and to the broader team only when the transaction is close to signed. When the transaction is announced, the CFO's job is to co-author the announcement communication, ensure the retention / severance framework is in place, and back-stop the CEO on the finance-question portion of the team Q&A.

**IPO.** Communicated broadly earlier — IPO processes require the team to be aligned with the disclosure and quiet-period restrictions. The CFO's job is to run the pre-IPO education on quiet-period rules, insider-trading windows, disclosure controls (that will apply post-IPO), and — after IPO — the ongoing investor-relations and periodic-reporting cadence.

**Wind-down.** The hardest communication. The CFO and CEO deliver together, with the timing pre-negotiated with counsel (WARN Act notice periods, state-specific requirements) and the severance / benefits package pre-designed. The specific ABC or Chapter 7 mechanics are handled by counsel; the CFO's job on the day is to answer the team's questions honestly and to be the source of truth on the wind-down mechanics.

## Common failure modes

- **Not declaring default dead when the company is default dead.** The most common failure mode. The classification stays soft, the plan B stays underdeveloped, the trigger never fires, and the company arrives at the 3-month emergency without a real plan. The declaration is the discipline that forces the honesty.
- **Declaring default dead without a plan B.** The opposite failure. The CFO writes "we are default dead" but has not named the specific plan-B path. The declaration without the plan-B is signalling without action.
- **Overcommunicating stress to the team.** All-hands announcements of runway stress that induce a departure spiral. The team's ability to work through a difficult raise depends on their belief that the company will get through it; that belief is what closes the plan-B window.
- **Undercommunicating stress to the team.** The opposite failure. The team is caught by surprise when the eventual layoff or acquisition or shutdown lands, and the trust deficit accumulates for whoever is running the next company.
- **Assuming the team doesn't know.** Team members read Glassdoor, LinkedIn, and the industry press. They know how their competitors are doing. Silence is not the same as absence of information; the team will construct their own narrative if the founders do not provide one.
- **Handing off to sale process too late.** A sale process that starts when the company has 60 days of cash left is priced against distress. A sale process that starts when the company has 6 months of cash left is priced against optionality. The CFO's job at the trigger is to be honest about which reality the company is in.
- **Handing off to sale process too early.** A sale process that starts when the company still has viable capital-instrument paths (bridge, insider recap, venture debt) is the CFO giving up prematurely. The trigger is not "no option is perfect"; the trigger is "no option is viable."

## What good looks like

A CFO who has this material installed:

- Maintains the default alive / default dead classification as a top-line metric on the monthly re-forecast pack.
- Declares the classification explicitly (default alive on best-case KPIs, or explicitly not) — no soft classification.
- Names the plan B on the same page as the declaration, with specific paths, dates, and triggers.
- Runs the CFO-CEO monthly runway meeting with the default alive / default dead conversation as its anchor.
- Ensures board and investor communications are consistent with the internal declaration.
- Handles the team-facing communication with a middle-path frame that is honest without inducing departures.
- Recognises the handoff signals to `startup-exit-curriculum` (sale, IPO, wind-down) and initiates the handoff explicitly, not silently.
- Coordinates the founder communication at handoff with counsel, HR, and advisors so that the team, the market, and the board hear a coherent story.

## Summary

- **Default alive / default dead** is the classification that anchors CFO-grade runway planning: on the current best-case operating KPIs, does the company reach cash-flow positive before running out of cash?
- The classification is a standing top-line metric on the monthly re-forecast pack. When default dead, the plan B is on the same page.
- The declaration is affirmative — default alive on best-case KPIs, or explicitly not. Soft classifications drift into distress.
- The founder-communication practice runs across three audiences: the CEO-CFO monthly meeting, the quarterly board deck, the team-facing "state of the company." All three are the same story with audience-appropriate framing.
- The handoff to `startup-exit-curriculum` fires when the runway plan resolves into a sale, IPO, or wind-down decision. The transaction execution belongs there; this module's contribution is the well-organised financial infrastructure and the honest declaration at the trigger.
- Common failure modes: silent drift on classification; declaration without plan B; over- or under-communication to the team; handoff too late (priced against distress) or too early (giving up premature options).

This closes the module. Chapters 1-8 have installed the runway-planning discipline (chapter 1), the bridge structures (chapter 2), the down-round mechanics (chapter 3), the recapitalisation / cram-down / re-up framework (chapter 4), venture debt (chapter 5), revenue-based financing (chapter 6), the growth-stage capital menu (chapter 7), and the default alive discipline that governs all of them (this chapter). The exercises apply each in a hands-on drill; the lab combines them into a simulated bridge-to-Series-B close.

The next module, [mod-110 — Board and Investor Governance for the CFO](../mod-110-board-and-investor-governance-for-the-cfo/), turns to the CFO's ongoing board and investor communication practice around all of this — the monthly investor updates, the quarterly board packs, the decision memos, and the CFO-CEO partnership work that runs continuously across the runway and capital cycle this module has covered.
