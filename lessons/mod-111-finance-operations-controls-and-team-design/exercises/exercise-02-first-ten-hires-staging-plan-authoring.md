# Exercise 02 — First-Ten Hires Staging Plan Authoring

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 2 (first-ten hires sequencing and comp benchmarks).

## Problem statement

Author a full finance-org staging plan for a specified company covering the sequence from pre-seed founder-bookkeeping through late Series-C / pre-IPO. For each hire (or outsourced-firm engagement) name the specific stage trigger, the ownership scope, the comp band (cash + equity, referencing a public benchmark by source), the reporting line, and the exit-out trigger (the milestone that turns this role into a team, a promotion, or a hand-off). Produce the CFO-readable Gantt-style chart that shows when each hire lands relative to the company's stage timeline.

The goal is muscle memory: after this drill you should be able to look at any startup's stage and headcount plan and predict — within one hire — what the next finance-org gap will be.

## Scenario — build your own

Construct (or use a real one) a company with the following minimum characteristics:

- Founding date and roughly-planned stage progression: pre-seed year 0, seed year 1, Series-A year 2-3, Series-B year 4-5, Series-C year 6-7, IPO year 8-9. Adjust to your scenario.
- Business model: SaaS (subscription, usage-based, or hybrid — pick one).
- Total headcount plan: ~15 at seed, ~50 at Series-A, ~150 at Series-B, ~400 at Series-C, ~800 at pre-IPO. Adjust.
- Geographic mix: US-centric with international expansion beginning ~Series-A.
- Capital raised by stage: ~$3M seed, ~$15M A, ~$50M B, ~$150M C, IPO proceeds ~$200M+.
- Anticipated audit-commit timing: Series-B.
- Anticipated IPO fiscal year: Y+8 or Y+9.

## Requirements

Produce a memo (Markdown, 6-10 pages) plus a companion spreadsheet or timeline visualisation.

### Section 1 — The hire register

A table with one row per hire (or outsourced engagement), with columns:

- Sequence # (1-10, plus additional layers-of-management hires as the company scales)
- Role title (internal) and function (accounting / FP&A / tax / treasury / IR / audit)
- Stage trigger (specifically: what happens in the business or stack that fires this hire)
- Ownership scope (one paragraph: what the role owns end-to-end)
- Reporting line (to whom)
- Comp band (cash base range, target-bonus %, equity % — with the source benchmark cited by name and date)
- Team-under-them at 12 months post-hire (0 for individual contributor, or the initial team shape)
- Exit-out trigger (the milestone at which this role becomes a team or is promoted or hands off)

### Section 2 — Timeline chart

A Gantt-style chart (spreadsheet, Notion, Figma, or similar) that shows the finance-org headcount over time, layered by role, with markers for the stage transitions and the anticipated audit-commit and IPO milestones. The chart should let a reader see, at a glance, when each hire lands relative to the raise cadence.

### Section 3 — The three-hire "always" and the "sometimes" hires

A short section (1-2 pages) naming:

- **The three hires that always happen in this order** and why any deviation is a design mistake: outsourced accountant → fractional CFO → first controller. Cite the specific chapter-2 reasoning against each ordering permutation.
- **The three hires that vary by company** (with the specific reason to consider deviating from the canonical sequence): treasury lead (depends on cash pile size), tax lead (depends on international / M&A / R&D-credit intensity), Head of IR (depends on dual-track / IPO trajectory).
- **The one hire that most companies mis-time** — argue for either "too early" or "too late" with a specific position: Head of FP&A hired before first FP&A analyst has been in role 18 months, or full CFO hired before the operating layer exists to sit on top of, etc.

### Section 4 — Comp benchmark research

For at least three of the roles (recommendation: Controller, Head of Accounting, Head of FP&A), pull the current comp benchmark from at least two public sources (Carta State of Startup Compensation, Pave, Option Impact, Radford, if accessible — otherwise cite Kruze / Pilot / other publicly-published startup-CFO content). Present the pulled numbers in a comparison table with (a) source, (b) role definition per source (verify the source's definition matches your internal role), (c) cash base median, (d) equity median at your company's stage, (e) geography adjustment applied.

For each comparison, note where the sources agree and where they diverge, and explain how you'd reconcile the divergence when making an actual offer.

### Section 5 — The mis-hire recovery playbook

A one-page section: for each of the "order-of-hire mistakes" from chapter 2 (Head of FP&A before controller, CFO before operating layer, treasury lead before cash pile, Head of IR before dual-track, disguised people-ops hire), describe the specific recovery playbook if the mistake has been made — what changes, who leaves, who gets re-scoped, what gets hired next.

## Starter guidance

- Sketch the timeline chart first — it forces you to commit to the stage-progression assumptions.
- For each hire, write the *stage trigger* before the *comp band*. If you can't articulate the trigger in one sentence, the hire is not yet crisp.
- For the comp benchmarks, treat the exact numbers as illustrative — the point of the exercise is to teach the *reading discipline* (match role to benchmark title not internal title, match stage precisely, match geography, read cash + equity together, refresh quarterly), not to produce a mechanically-correct offer.
- Cross-reference your hires against the module chapters they map to — the controller hire fires the chapter-3 close discipline, the tax lead fires the chapter-6 R&D-credit ownership, etc.

## Acceptance criteria

- **Every hire has a specific stage trigger.** Not "when we can afford it" — a business event.
- **Every hire has a documented reporting line and team-shape.** Ambiguous org-chart placements are rejected.
- **Comp benchmarks are cited by source and date.** Not "market standard" — a specific published source.
- **The three-always and one-mis-time sections make specific arguments** that a reader could push back on. Vague "it depends" answers are rejected.
- **The timeline chart is readable in one glance** and lets a reader trace each hire back to a stage marker.

## Deliverables

- The memo (Markdown or PDF, 6-10 pages).
- Timeline chart (spreadsheet, Notion, Figma, or PDF export).
- Comp-benchmark comparison table.

## Extensions (optional)

- Model the same plan for a very-differently-shaped company: a services / consulting business (revenue timing very different), a hardware / deep-tech company (COGS management very different), a fintech (regulatory-compliance headcount very different).
- Add the *outsourced-firm* line: at each stage, which functions are still outsourced (bookkeeping, tax, R&D credit, sales-tax filing, 409A) and when each moves in-house.
- Overlay the *finance-team-as-percent-of-total-headcount* against a benchmark for pre-IPO SaaS and comment on whether your plan is over-headcount or under-headcount relative to peers.
