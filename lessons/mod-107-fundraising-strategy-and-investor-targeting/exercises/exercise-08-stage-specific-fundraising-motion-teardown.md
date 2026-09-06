# Exercise 08 — Stage-Specific Fundraising Motion Teardown

**Estimated time:** ~5-7 hours (three real-fundraise teardowns, each requiring source research).
**Prerequisites:** Chapter 9 (stage-specific dynamics), plus the full mod-107 stack (chapters 1-8 provide the mechanics that each teardown analyses).

## Problem statement

Tear down three publicly-known fundraises — one seed, one Series-A, and one Series-B, all in the same sector — against the stage-specific motion patterns from chapter 9. For each raise, reconstruct (from public sources) what was being underwritten, what the proof-artifacts likely were, what the motion looked like, and where the raise nearly missed or ran the wrong motion for its stage. Produce a synthesis memo comparing the three motions and extracting the specific stage-transition lessons for a CFO.

The point of the exercise is to install the pattern-recognition of stage-specific motion — the ability to look at any raise and identify whether it is being run as a seed, Series-A, or Series-B motion, and whether that motion matches the stage's underwriting frame. Doing three real raises in one sector — where sector-specific dynamics are held constant — makes the stage differences visible.

## Scenario — pick three real raises

Pick a sector where publicly-known fundraises span all three stages within the last 2-4 years. Good candidates:

- **B2B SaaS** — many announced rounds with public deck / interview / press coverage.
- **Vertical SaaS** (legal-tech, med-tech, con-tech, fin-tech) — high-visibility raises.
- **Fintech infrastructure** — heavily covered by tech press.
- **Developer tools** — often has public founder blog posts on the raise.
- **AI infrastructure / AI applications** — high-visibility recent-vintage raises.

Choose three specific companies in the sector, one per stage. Prefer companies with:

- **Public announcements** — press release, TechCrunch / The Information article, founder blog post.
- **Public deck or deck excerpts** — some founders publish the deck post-raise; others discuss it in interviews.
- **Public interview content** — founder-CEO interviews on 20VC, Acquired, ProductHunt, Y Combinator content, etc.
- **Public cap-table data** — SEC Form D filings, PitchBook / Crunchbase records.
- **Known investors** — the identity of the lead(s) is public and researchable.

Avoid raises where information is very thin or where the round was highly unusual (bridge / take-private / down round) — the standard-motion teardown is what the exercise practices.

For each of the three raises, document the source stack you are relying on (URLs, publication dates, note whether primary or secondary). Use `<!-- needs-research: ... -->` tags for any claim you cannot cite to a public source.

## Requirements

### 1. Per-raise teardown (3 teardowns, ~2-3 pages each)

Each teardown structured as follows:

**Company and round summary.**

- Company, stage of raise (seed / Series-A / Series-B), round date, round size, lead investor, other named participants, post-money valuation (if public).
- The company's state at raise time: ARR (if public), customer count, team size, primary product.
- The specific market conditions at raise time (e.g., "Q3 2023, mid-compression cycle"). Reference the market-conditions context from mod-106.

**What was being underwritten.**

- The specific underwriting frame — founder-and-insight (seed), traction-and-wedge (Series-A), or operating-model-and-team (Series-B) — matched against chapter 9's descriptions.
- Evidence for the frame from public sources (interview quotes, article language, deck slides).
- Any signals that the raise's underwriting frame was different from the stage-typical frame (e.g., a Series-A raised primarily on the founder's prior-exit reputation with light traction — a "seed-like Series-A").

**What the proof-artifacts likely were.**

- The deck (if public) — is it Sequoia / YC pattern (chapter 4)? Any deviations, with the visible "why."
- The data-room shape (if inferable from investor commentary or from the standard for the fund).
- The financial model likely required for the round (from mod-103 and chapter 9's stage-appropriate shape).
- Any third-party diligence involvement inferable from the round announcement (QoE firm, commercial-diligence firm).

**What the motion looked like.**

- Timeline — how long from process-start to term sheet, if public.
- Target list — which funds passed and which competed, if inferable from public commentary.
- CEO / CFO split — is there a CFO on the team? Did the CFO participate in the raise? (Often visible in team announcements and interview commentary.)
- Close mechanics — was there a competitive close, a single-lead close, an insider-led close?

**Where the raise nearly missed or ran the wrong motion.**

- Any public commentary on "we almost didn't get this" moments.
- Any signal that the motion was mismatched for the stage — over-formalised at seed, under-prepared at Series-A / Series-B.
- Any signal of over- or under-raising against the milestone bar (chapter 1) — visible in subsequent operating decisions (layoffs, extension rounds, rapid re-raise).

### 2. Synthesis memo (~2 pages, Markdown)

A cross-teardown synthesis covering:

- **The stage transitions in this sector.** What specifically changes from seed to Series-A to Series-B in this sector — the traction bar, the operating-model expectation, the team-composition expectation, the target-fund composition.
- **The specific motion pattern each stage rewarded.** Match the observed motions to chapter 9's motion patterns.
- **The "wrong motion" example.** Of the three, which raise (if any) ran a wrong motion for its stage, and what the specific cost was.
- **The specific CFO-role differences by stage.** Where the CFO shows up (or is absent) across the three raises.
- **Cross-sector generalisability.** Which lessons from this sector generalise to any sector, and which are sector-specific (SaaS-specific traction bars, marketplace-specific take-rate underwriting, etc.).

### 3. Per-raise decision-audit (half-page per raise, 1.5 pages total)

For each raise, produce a "if I were the CFO doing this raise" audit:

- Two specific things the CFO / CEO team did right that the reader would emulate.
- Two specific things the CFO / CEO team could have done better (based on public evidence).
- One specific thing the reader would have done differently — and why.

Grounded in specific chapter references (chapter N covers the mechanic; the raise applied / did not apply it as chapter N would recommend).

## Starter guidance

- **Choose the same sector across all three stages.** The point is to isolate stage differences by holding sector constant. Do not tear down a seed in SaaS, a Series-A in fintech, and a Series-B in consumer.
- **Choose companies where public information is deep enough for a real teardown.** Some companies publish extensively; others are opaque. The exercise fails if the teardown is 80% speculation.
- **Cite every non-obvious claim.** Every ARR number, every round-size number, every "the fund is a lead" claim needs a source URL or a `needs-research` tag. This is a public-facing analytical artifact; the sources matter.
- **Be honest about the limits of public information.** Some things (specific CEO-CFO dynamics, specific fund-side objections during the raise, specific term-sheet mechanics) are not public. Note the limit rather than speculating.
- **Do not attack the founders.** The exercise is about learning the pattern, not about second-guessing specific people. Frame every critique as "the specific choice, in retrospect, cost X" rather than as "the founder made a bad decision."
- **Anchor to chapter 9's motion patterns.** The teardown's structure is chapter 9's stage-specific pattern applied to real data. If you find yourself writing a teardown that does not track chapter 9's underwriting frames, motions, and stage-transitions, re-anchor.
- **Use the "would I make this same decision" test.** For each stage-decision the founder / CFO made (target list, timeline, deck approach, close mechanics), ask whether you would do the same. This forces specific engagement with the pattern.
- **Do not skip the "wrong motion" analysis.** The specific mismatches are where the learning is densest. If all three raises look like textbook executions of the stage-appropriate motion, either you chose an unrepresentative set or you are missing signal.

## Acceptance criteria

- **Three teardowns** — one seed, one Series-A, one Series-B, same sector — with each of the sections above populated.
- **Source stack cited for each teardown** — every non-obvious claim traceable to a public URL or a `needs-research` tag.
- **The stage-specific underwriting frame identified per raise** and matched (or contrasted) to chapter 9's canonical frame.
- **The synthesis memo** with specific cross-teardown lessons and specific chapter-referenced insights.
- **The per-raise decision-audit** with two right / two better / one different-choice per raise, chapter-referenced.
- **No inventions.** Every ARR number, valuation, or specific fund-side action either cited or explicitly flagged as inference-from-limited-signal.
- **Chapter-9 pattern-recognition visible throughout.** The teardown structure applies chapter 9's frames explicitly — the reader can see that the analysis is chapter-9-derived, not free-form.
- **The synthesis distills a specific transferable pattern.** Not "each stage is different" but "the specific transition from seed to Series-A in this sector requires these three specific artifact upgrades and this specific team addition."

## Deliverables

- Three teardowns (Markdown, ~2-3 pages each).
- The synthesis memo (Markdown, ~2 pages).
- The per-raise decision-audit (Markdown, ~half page per raise).

## Extensions (optional)

- **Add a fourth raise — a bridge or extension round.** Chapter 9 notes that off-cycle rounds run their own motion. Tear down a public bridge or extension round in the same sector and contrast it to the seed-Series-A-Series-B main sequence.
- **Overlay market conditions.** For the three raises, note the specific market-conditions context (mod-106 chapter 6-7). Does the stage-motion analysis change under different market conditions? Which patterns are robust across market cycles and which are cycle-dependent?
- **Investor-side lens.** For each raise, tear down the lead investor's decision. What was the fund underwriting? Which fund-math was in play (chapter 2 partnership-economics)? Where does the fund's decision look like a strong bet vs. a stretch?
- **Follow-through analysis.** For each of the three raises, check the company's state 12-24 months post-raise. Did the operating plan clear the milestone bar the round was sized against (chapter 1)? Did the CFO role visibly upgrade? Did the company raise the intended next round on the intended terms?
- **Cross-sector comparison.** Repeat the exercise in a different sector (e.g., B2B SaaS one way, consumer-marketplace another) and compare the stage-transition patterns.
- **Present the teardown live.** Present one of the three teardowns to a peer group and get pushback on the specific claims. Note where the analysis withstands challenge and where it needs revision.
