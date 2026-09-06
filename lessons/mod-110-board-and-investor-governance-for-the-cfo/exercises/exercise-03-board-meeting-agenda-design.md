# Exercise 03 — Board Meeting Agenda Design

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 3 (board meeting design and the walk-the-pack anti-pattern). Chapter 2 (the pack the meeting operates on) is a strong dependency; you should have completed exercise 02 or have a comparable pack in hand.

## Problem statement

For a specified quarterly board meeting, design the full agenda with time-boxing, produce the pre-read distribution schedule, and author the meeting-minutes template. The agenda must follow the chapter-3 reference structure (pre-read → 30-minute KPI check-in / financials → 60-minute strategic deep-dive → 30-minute risks / decisions / consents → 15-30 minute executive session), scale the time-boxing to the specific meeting's content, and be paired with a minutes template that captures every decision, vote, action item, and consent for the corporate minute book.

The exercise trains the meeting-design discipline. The pack (exercise 02) is only half the mechanism; the meeting is where the pack does its work, and the meeting design determines whether the standing calendar produces governance value or produces the walk-the-pack pattern.

## Scenario — the same Series-B company as exercise 02

Use the company from exercise 02 (or, if you did not complete exercise 02, author a comparable Series-B B2B SaaS company at $12M-$18M ARR, seven directors, quarterly cadence, currently the Q3 pack).

**The specific meeting.** Q3 quarterly board meeting, in person at the company's headquarters, scheduled for a Tuesday afternoon (2pm-5pm). Six voting directors plus one observer plus the CEO and CFO in the room; corporate counsel dials in for the risks / decisions / consents section. The strategic deep-dive is on the go-to-market segment-focus decision (from exercise 02).

**Additional context.** The Q3 quarter had a small ARR miss (6% MoM vs. 8% plan) that is not existential but is worth a real discussion. The pack contains one decision item (the segment-focus affirmation) and one placeholder decision item (a specific senior hire above the compensation-committee-approval threshold). Consents include the ordinary quarterly items and one non-standard consent (an insider-note term-sheet authorisation). One senior departure occurred during the quarter and warrants an executive-session discussion.

## Requirements

Produce a submission directory containing the following.

1. **The meeting agenda** (`01-agenda.md`). Two-to-three pages. Structure:
   - Meeting date, time, location, attendees (voting, non-voting observers, management, counsel).
   - Pre-meeting activity summary: pack sent date, pre-read call schedule (per chapter 3), materials distribution reference.
   - Full time-boxed agenda from 2:00pm through 5:00pm with 5-minute buffers:
     - 2:00 - 2:10 — call to order, prior-minutes approval, agenda confirmation.
     - 2:10 - 2:40 — KPI check-in and financials (30 minutes).
     - 2:40 - 3:40 — strategic deep-dive: segment-focus decision (60 minutes).
     - 3:40 - 4:10 — risks / decisions / consents (30 minutes).
     - 4:10 - 4:15 — action-item recap; next-meeting deep-dive topic selection.
     - 4:15 - 4:45 — executive session (management steps out).
     - 4:45 - 5:00 — post-session debrief between the lead independent director and the CEO.
   - For each agenda block, name the specific facilitator (typically CEO for KPI check-in and deep-dive; CFO for financials and risks / decisions / consents; lead independent director for executive session).
   - For each agenda block, name the specific pack references (KPI dashboard page, financials narrative, deep-dive memo, risks section, consents list).
   - For each agenda block, name the specific expected outcome (a decision recorded, a shared read confirmed, a follow-up recorded).

2. **The pre-read distribution schedule** (`02-pre-read-schedule.md`). One-to-two pages. Includes:
   - The specific date and time the pack lands (72 hours before the meeting; the exact business-day-hour clocking).
   - The distribution list (voting directors, observers, counsel, any advisors receiving the pack).
   - The specific pre-read calls the CFO / CEO will run: two-to-three calls in the 72-hour window, with the specific director, the proposed call time, the specific topics the CFO expects to raise, and the specific concerns the CFO expects the director to raise.
   - The specific questions the CFO plans to send to the whole board 24 hours before the meeting as a "questions you might want to think about" note (per some CFO practice; optional but a specific chapter-3 mechanic worth practising).
   - The version-control convention for the pack.

3. **The meeting-behavior conventions memo** (`03-behavior-conventions.md`). One-to-two pages. The specific meeting-behavior conventions the meeting operates under (per chapter 3). Includes:
   - Devices and observer conventions (laptops / phones in or out; observer participation in discussion vs. listen-only).
   - The "no walk-the-pack" rule and the specific mechanic that enforces it (e.g., the CFO opens each section with two-to-three minutes of framing, then invites director questions).
   - The specific handling of a director interrupting during the KPI check-in for a topic that belongs in the deep-dive slot ("that's a great question; can we hold it for the deep-dive discussion").
   - The specific handling of a decision that runs long ("we've spent 45 minutes on this and haven't converged; are we deferring to a written consent, or scheduling a follow-up call this week, or making a decision now").
   - The specific expectation that the pre-read has been read (and the CFO's response if it clearly has not been).
   - The executive-session convention (voting members only; observers leave with management; scheduled every meeting to normalise its presence; the lead independent director leads).
   - The post-session debrief convention (5-15 minutes, lead independent director to CEO, verbal, no memo).

4. **The meeting-minutes template** (`04-minutes-template.md`). Two-to-four pages. A blank template a corporate secretary or the CFO can fill during / after the meeting. Includes:
   - Header: meeting date, time, location, presiding director (or CEO chair), secretary (typically CFO or corporate counsel), attendees (present / absent / observer status for each).
   - Preliminary matters section: call to order, quorum confirmation, prior-minutes approval, conflicts-of-interest disclosures.
   - Substantive-discussion sections (one per agenda block): topic, presenter, key points discussed, decisions made (with vote counts if applicable), action items generated (with owner and due date).
   - Written-consent section: any consent adopted at the meeting (with the specific resolution text or a reference to the drafted resolution).
   - Executive-session section: a one-line acknowledgement that the executive session was held with voting directors only, without any specifics of the discussion (the discussion itself is not minuted; the fact of the session is).
   - Adjournment: time of adjournment, secretary sign-off block, subsequent-meeting-schedule reference.
   - A specific note on minutes conventions: minutes record decisions and material discussion, not verbatim transcript; contentious debate is summarised rather than quoted verbatim unless a director specifically requests attribution.

5. **A sample completed minutes** (`05-sample-minutes.md`). Two-to-four pages. Fill the template with plausible content from this specific meeting: the segment-focus decision was affirmed by unanimous vote; the senior-hire decision was deferred pending a compensation-committee review; the insider-note consent was adopted by unanimous written consent to be circulated post-meeting; three action items were generated (the CFO owns two, the CEO owns one). The executive-session line records that the session was held; the post-session debrief conveyed a specific message on senior-team-succession planning (the specific message content is not minuted — only the fact of the debrief is recorded).

6. **The action-item register update** (`06-action-item-register.md`). One page. The running register of open items maintained by the CFO between meetings (chapter 4). Add the three new action items from this meeting to the running register; carry forward any prior open items (invent one or two prior open items to demonstrate the carry-forward mechanic). Columns: item, owner, opened date, due date, status, related decision or memo reference.

## Starter guidance

- **Read chapter 3 before designing.** The reference agenda, the walk-the-pack anti-pattern, and the specific meeting-behavior conventions are all there. Attempting the agenda without a re-read produces a walk-the-pack agenda by default.
- **The 30 / 60 / 30 / 15-30 time-boxing is a reference, not a straitjacket.** For this specific meeting (a small miss to discuss, one decision, one deferred decision, one non-standard consent, and an executive-session topic), the reference time-boxing fits. For a different meeting (a major fundraise decision consuming the whole strategic slot), the time-boxing might shift. State any deviation from the reference explicitly and justify it.
- **Every agenda block names its facilitator, pack references, and expected outcome.** An agenda without these three attributes is a topic list, not an agenda.
- **The pre-read call is a specific chapter-3 mechanic.** Do not skip it. Draft the two-to-three specific calls with named directors and expected topics. The value of the call is to surface a concern in private before it becomes a surprise in the meeting.
- **The meeting-behavior conventions are the mechanism that enforces the agenda.** Without the "no walk-the-pack" mechanic and the specific handling of long-running decisions, the agenda drifts within 20 minutes. The behavior conventions are what keep the agenda on track.
- **The minutes template is the corporate-record artefact.** It has legal weight (per the CFO's obligations under chapter 4). Draft it seriously. Look at a real minutes template if available (many law firm websites publish sample templates; NVCA does not publish minutes templates but Cooley GO and Orrick have public samples).
- **The sample minutes should be plausible.** The vote counts, the deferrals, the consents, and the action items should all reflect a real quarterly-meeting rhythm. Do not fabricate contentious discussion or dramatic votes; the reference meeting is one where the process works.
- **The executive-session line in the minutes is short by design.** The fact of the session is recorded; the content is not. The post-session debrief message is not recorded either — it is a verbal channel from the lead independent director to the CEO.

## Acceptance criteria

- **All six deliverables present.** Agenda, pre-read schedule, behavior conventions, minutes template, sample minutes, action-item register.
- **The agenda is fully time-boxed** from call-to-order through adjournment. Every block names facilitator, pack references, and expected outcome. Total meeting length fits in the 2.5-3 hour reference range or explicitly justifies deviation.
- **The pre-read distribution schedule specifies a 72-hour business-day-clocked pack-send time** and lists at least two specific pre-read calls with named directors and expected topics.
- **The behavior-conventions memo names the walk-the-pack anti-pattern explicitly** and specifies the mechanic that prevents it. It also specifies the executive-session convention and the long-running-decision handling.
- **The minutes template captures the corporate-record structure** — preliminary matters, substantive-discussion blocks with decisions and action items, written-consent section, executive-session line, adjournment. It notes the "record decisions, not verbatim transcript" convention.
- **The sample minutes are plausible and internally consistent** with the scenario. The segment-focus decision, the deferred hire, the insider-note consent, and the executive-session line all appear correctly.
- **The action-item register carries forward at least one prior item** and adds the three new items from this meeting.
- **The specific chapter-3 mechanics (pre-read, no-walk, executive session, post-session debrief) are all present.** A design missing any of these is a design that produces a walk-the-pack meeting.

## Deliverables

- `01-agenda.md`
- `02-pre-read-schedule.md`
- `03-behavior-conventions.md`
- `04-minutes-template.md`
- `05-sample-minutes.md`
- `06-action-item-register.md`

## Extensions (optional)

- **The compressed-timeline emergency meeting.** Six weeks after the quarterly meeting, a specific incident (a large customer signalling non-renewal, or a term-sheet response window closing) requires an emergency board meeting on 72-hour notice. Design the compressed agenda (60-90 minutes total; no strategic-deep-dive slot; single-topic focus), the compressed pre-read distribution (a 5-page memo rather than a 40-page pack), and the compressed minutes template. Practice the "exception to the reference agenda" mechanic per chapter 3.
- **The all-virtual meeting.** Rework the agenda and behavior conventions for an all-virtual (video-conference) meeting. Address specific virtual-meeting challenges: side conversations are impossible; observer participation is more disruptive; the executive session mechanic works differently; body language cues are muted.
- **The observer-participation matrix.** For a meeting with three observers (a Series-A board observer, a Series-B board observer, and one advisor entitled to attend), draft the specific participation rules for each: which sections they attend, whether they can speak, whether they attend the executive session. Practice the chapter-3 observer conventions.
- **The board-effectiveness self-assessment.** Draft a short annual board-effectiveness self-assessment questionnaire that each director completes after Q4. Includes: is the pack landing 72 hours out, is the pack readable, is the strategic deep-dive real, are decisions being reached in the meeting or deferred too often, is the executive session productive. Trains the meta-governance discipline chapter 3 gestures at.
- **The first-meeting-post-Series-B agenda.** Design the specific agenda for the first board meeting after the Series-B closes, where a new director joins for the first time. Includes an onboarding block (30 minutes on company context, product, financials, strategic plan) at the start of the meeting or as a separate onboarding session the day before.
