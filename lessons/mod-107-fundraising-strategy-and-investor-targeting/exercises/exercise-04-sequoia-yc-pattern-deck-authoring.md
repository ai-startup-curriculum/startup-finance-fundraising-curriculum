# Exercise 04 — Sequoia / YC Pattern Deck Authoring

**Estimated time:** ~5-8 hours (deck authoring is iterative; expect two or three passes).
**Prerequisites:** Chapter 4 (the eleven-slide pattern and per-slide architecture), plus a working knowledge of the target company (from exercise 01 / 02) and the unit-economics vocabulary (mod-102).

## Problem statement

Author a seed or Series-A pitch deck for a hypothetical (or real, anonymised) target company end-to-end in the Sequoia / YC pattern. Each slide follows the canonical structure from chapter 4 — company purpose, problem, solution, why now, market size, competition, product, business model, team, financials / traction, the raise. Annotate each slide with the specific diligence question it is intended to answer, and diagnose any deviation from the canonical structure with an explicit "why" note.

The point of the exercise is not to produce a design-award-winning deck. It is to install the *architectural discipline* — the eleven slides in the specific order, with each slide doing its specific job of answering a specific diligence question. The design polish comes second; the architecture is what closes the meeting.

## Scenario — build your own

Pick one target company. Reuse the company from exercise 01 / 02, or build a fresh one (with less repetition of scenario detail across the module — extending prior work is preferred). Minimum specificity:

- Sector and business model (specific — see exercise 02).
- Stage (seed or Series-A).
- Current traction numbers (ARR, customer count, cohort characteristics if any — mod-102 chapter 4 for cohort table shape).
- Round size and round-shape (from exercise 01 sizing).
- Team and founder-market-fit narrative.
- Product summary — what it does in one sentence, who it's for, why it matters.

Document the target-company profile as an appendix to the deck.

## Requirements

### The deck — 11-13 slides plus an appendix

Author each slide following the chapter 4 architecture. For each slide:

1. **Content** — the actual slide (text, visuals, chart mockups where relevant).
2. **The diligence question this slide answers** — one sentence naming the specific investor-side question the slide is meant to answer.
3. **Speaker notes** — 3-6 sentences on the verbal delivery that the founder-CEO would give with the slide.
4. **Design notes** — brief notes on visual hierarchy and what a well-designed version would emphasise (e.g., "the ARR chart should dominate the traction slide," "the team photo grid should show experience-badges").

**Slide 1 — Company purpose.** A single-sentence positioning of what the company is. See chapter 4 for the specific pattern. Optionally add the tagline and one background image.

**Slide 2 — Problem.** The specific customer problem in the customer's own vocabulary, with the pain quantified where possible.

**Slide 3 — Solution.** The specific way the company solves the problem — what the product does at the atomic-value-delivered level.

**Slide 4 — Why now.** The specific technology / regulatory / distribution / behavioural shift that makes this company possible now. This slide is often skipped or hand-waved; do not skip.

**Slide 5 — Market size.** Bottom-up (customer × ACV × penetration) preferred; top-down as a sanity check. Show your arithmetic. Do not use TAM / SAM / SOM as a fig leaf.

**Slide 6 — Competition.** Honest positioning against the competitive set — direct competitors, adjacent competitors, and status-quo alternatives (spreadsheets, in-house builds, "do nothing").

**Slide 7 — Product.** A specific demonstration of the product — screenshots, short workflow, or a linked demo. Not a feature list.

**Slide 8 — Business model.** Pricing, packaging, unit economics — CAC, LTV, gross margin, payback (mod-102). At seed the numbers may be projected; at Series-A they should be observed.

**Slide 9 — Team.** Founders and key hires. Founder-market-fit evidence.

**Slide 10 — Financials / traction.** The load-bearing slide at Series-A. ARR trajectory, cohort retention, growth rate, key KPIs. For seed, this slide often shows early-signal data (design partners, pipeline, beta usage) rather than ARR.

**Slide 11 — The raise.** Round size, use of funds (from exercise 01 sizing), milestones to next round.

**Appendix (as needed).** Additional slides for common diligence questions the main deck does not answer but that a partner might raise:
- Detailed cohort table (mod-102 chapter 4).
- Sales-productivity breakdown (Series-A onward).
- Detailed competitive teardown.
- Technical architecture summary.
- Detailed hiring plan (from the operating plan in exercise 01).

### The annotation layer

For each of the 11 main slides, produce:

- **Diligence question the slide is answering.** (One sentence.)
- **Chapter 4 architectural role** — what the chapter says this slide is for.
- **How your specific slide fulfills it** — 1-2 sentences.
- **Any deviation from the canonical structure with the "why."** If you swap the order of the market slide and the why-now slide, or fold the business model into the product slide, name the specific reason and identify the trade-off (see chapter 4's "Common deviations and their costs" section).

### The pitch-narrative memo (~1 page, Markdown)

A separate memo describing the overall narrative arc of the deck — the specific story the deck tells from slide 1 to slide 11. Explain why the specific order works for the specific company. This is what the founder-CEO uses to prep for delivery.

## Starter guidance

- **Write the story before you make the deck.** The one-page narrative memo should be complete before you touch slide-design software. The deck is the render of the story; the story is the substance.
- **Use the canonical order unless you have a specific reason not to.** Every deviation costs conversion (chapter 4). If you deviate, be explicit about why.
- **Numbers first, adjectives second.** Every slide should have a specific number, name, or visual that the reader can attach to. "We're growing" is not an evidence claim; "$1.8M ARR up from $500K 12 months ago" is.
- **Every slide answers a specific question.** If you cannot say "this slide answers question X for the partner," the slide is not doing work.
- **The traction slide (slide 10) is load-bearing at Series-A.** Spend the most time here. At seed, invest correspondingly less on traction (there isn't much) and correspondingly more on the why-now and team slides.
- **The team slide is often under-loved.** The right team-slide format is faces + specific credential-badges + a founder-market-fit sentence. See chapter 4 for the specific structure.
- **The raise slide is not just "the ask."** Chapter 4 covers what a good raise slide includes: round size (from exercise 01), use of funds tied to the milestone-bar plan, and specific milestones the round is buying.
- **Keep the main deck to 11-13 slides.** Every slide beyond that dilutes the story. Push detail into the appendix.
- **The appendix is for anticipated follow-up questions.** Build appendix slides for the specific diligence questions you expect a partner to ask.
- **Do not use jargon or acronyms that the partner will not immediately parse.** If the deck reads like a partner needs a translator, the deck is not doing its job.
- **Include one or two "kill-your-darlings" slides in a rejected-slides appendix.** These are slides you drafted and cut. Include them with a note on why they were cut. This forces the discipline of keeping the deck tight.

## Acceptance criteria

- **Eleven main slides in the canonical order** (or a defensibly-deviated order with the deviation-note explicit).
- **Each slide's diligence question is named.** No slide has an "unspecified purpose."
- **Each slide has speaker notes** — the verbal delivery, not just the visual.
- **The traction / financials slide is stage-appropriate.** At seed, early-signal proof. At Series-A, cohort-backed ARR trajectory.
- **The raise slide ties back to the exercise 01 sizing** — the round size and use of funds match the milestone-bar plan.
- **The team slide has founder-market-fit evidence**, not just names and titles.
- **The appendix has at least 3-5 anticipated-follow-up slides.**
- **The pitch-narrative memo** (one page) describes the arc from slide 1 to slide 11 with specific reasoning.
- **Rejected-slides appendix** with at least 2 cut slides and the reason for cutting.
- **No unsourced numbers.** Every market-size, growth-rate, benchmark, or competitor-claim number has a source or a `<!-- needs-research: ... -->` tag.

## Deliverables

- The deck (Google Slides, Keynote, PowerPoint, or PDF export).
- The annotation layer (per-slide diligence-question / architectural-role / fulfillment / deviation-note) as a separate document or as speaker-notes in the deck.
- The pitch-narrative memo (Markdown, ~1 page).
- The rejected-slides appendix (in the deck or as a separate file).

## Extensions (optional)

- **Author a Series-A version and a seed version** of the same target company (assume different traction states) and compare the slide-by-slide differences — especially the traction slide, the team slide, and the raise slide. Note how the underwriting frame shifts (chapter 9).
- **Do a "cold-open" 30-second version** — the two sentences you would say to open a first meeting before the deck comes up on screen. This is often more important than any single slide.
- **Do a "one-pager" version** — a single-page investor-facing summary. Note which slides collapse into which pieces and which are dropped.
- **Simulate DocSend metrics** — decide, before you send, which slides you expect to be the highest and lowest engagement. Prepare exercise 06 by pre-registering the hypothesis.
- **Adversarial redraft.** Give the deck to someone who has not seen the company and ask them to identify the three weakest slides in 15 minutes. Fix those three slides.
- **Present the deck live to a mock partner.** Have a peer or mentor role-play the partner, ask questions, and note where the deck fails to answer or where the founder has to reach for an appendix slide.
