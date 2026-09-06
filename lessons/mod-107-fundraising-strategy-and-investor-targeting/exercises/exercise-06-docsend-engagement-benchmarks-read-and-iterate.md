# Exercise 06 — DocSend Engagement Benchmarks: Read the Signal and Iterate

**Estimated time:** ~3-4 hours (one iteration cycle; extendable to a multi-cycle simulation).
**Prerequisites:** Chapter 6 (DocSend signals and iteration cycle), plus exercise 04 (the deck being iterated).

## Problem statement

Read a simulated DocSend engagement dataset for a live pitch deck (either the deck from exercise 04 or one provided below in the scenario). Diagnose the two or three weakest slides against the four canonical signals from chapter 6 (total time, drop-off point, return visits, forwards) and the aggregate benchmarks from DocSend's published reports. Author the specific deck iteration — which slides to rewrite, the specific rewrite, and the hypothesis to test with the next 5-10 views.

The point of the exercise is to install the discipline of iterating on the *signal* rather than on founder taste. A CFO who can turn a per-slide engagement heatmap into a three-slide rewrite plan in an afternoon is doing the iteration cycle chapter 6 describes. A founder who rewrites slides on gut feel is not.

## Scenario — a simulated DocSend dataset

**The setup.** The deck (from exercise 04, or the placeholder shape below) has been sent to 25 tier-2 and tier-1 fund viewers over three weeks. Each viewer has generated some engagement data. You have DocSend's per-viewer engagement summary.

**The deck** (11 slides + 4 appendix slides):

1. Company purpose
2. Problem
3. Solution
4. Why now
5. Market size
6. Competition
7. Product
8. Business model
9. Team
10. Traction / financials
11. The raise
12. Appendix — cohort table
13. Appendix — sales productivity
14. Appendix — technical architecture
15. Appendix — hiring plan detail

**Aggregate engagement (simulated).** Across the 25 viewers, the aggregate view is:

| Slide | Avg time (sec) | % viewers reached this slide | Return-visit rate | Notes |
|---|---|---|---|---|
| 1 | 8 | 100% | Low | Opens quickly, most read past |
| 2 | 22 | 100% | Low | Above-average time |
| 3 | 18 | 92% | Low | Standard engagement |
| 4 | 6 | 88% | Very low | Suspicious low time |
| 5 | 15 | 84% | Low | Standard |
| 6 | 32 | 76% | Moderate | Drop-off starts here for some |
| 7 | 20 | 60% | Low | Big drop-off between 6 and 7 |
| 8 | 12 | 56% | Very low | |
| 9 | 45 | 52% | High | High linger time; return visits |
| 10 | 40 | 48% | Moderate | Load-bearing slide but low reach |
| 11 | 10 | 40% | Low | |
| App 12 (cohort) | 25 | 24% | Moderate | Some readers dig here |
| App 13 (sales) | 5 | 12% | Low | |
| App 14 (arch) | 15 | 16% | Low | |
| App 15 (hiring) | 3 | 8% | Low | |

Additional per-viewer notes:

- **8 viewers spent under 60 seconds total on the deck.** Of these, 5 are from funds later confirmed as thesis-mismatched (post-hoc check against the target list). The other 3 are from funds that were natural-fits — a possible signal that the opening is not landing for on-thesis viewers.
- **6 viewers had at least one return visit.** Of these, 5 returned specifically to slide 9 (team) or slides 10 (traction) or the appendix cohort table (slide 12).
- **4 decks were forwarded within the recipient fund.** Of these, 3 were forwarded from the associate to a partner; 1 was forwarded from a partner to another partner (a strong signal — this fund progressed to a partner meeting).
- **The 12 viewers who reached slide 10 (traction) split roughly evenly** between those who continued to slide 11 (the raise) and those who dropped after slide 10.
- **The appendix hiring-plan slide (15) has 8% reach.** Almost no readers open it.

## Requirements

Produce a DocSend-signal analysis, a diagnosed weak-slide set, a per-slide rewrite plan, and a next-cycle hypothesis document.

### 1. DocSend-signal analysis (Markdown, ~2 pages)

Structured per chapter 6's four signals:

- **Total time on deck** — median across viewers, distribution shape, and any patterns to segment by (on-thesis viewers vs. off-thesis viewers, associate viewers vs. partner viewers if inferable).
- **Drop-off point** — where the deck loses viewers and what that says about which slides are failing.
- **Return visits** — which slides are being re-visited and what that suggests about reader interest.
- **Forwards** — the pattern of forwarding and what it says about the deck's internal-conversation-generating capacity.

For each signal, compare the observed data to the practitioner-benchmark pattern from chapter 6 and DocSend's published reports. Use `<!-- needs-research: ... -->` for any benchmark you cannot cite to a current-vintage source.

### 2. Diagnosed weak-slide set (Markdown, half page)

Identify the two or three specific slides most in need of iteration. For each:

- The observed engagement pattern (drop-off, low time, high time, return visits).
- The specific hypothesis for why the slide is underperforming (chapter 6's diagnostic patterns).
- The evidence strength — how confident you are in the diagnosis and what would strengthen it.

### 3. Per-slide rewrite plan (Markdown, ~2 pages)

For each weak slide identified, produce:

- **Current slide state** — a 1-2 sentence summary of what the slide currently shows.
- **Specific rewrite** — the new content, layout, and visual approach. Be specific enough that a designer could implement it.
- **The hypothesis being tested** — what the rewrite is trying to prove or disprove about reader engagement.
- **The specific metric to watch** — what engagement change would validate the rewrite (e.g., "time on slide 6 should increase from 32s to 45-60s, and drop-off between slide 6 and 7 should decrease from 21% to under 10%").
- **The revert criterion** — what would signal the rewrite made things worse and should be reverted.

### 4. Next-cycle hypothesis document (Markdown, half page)

- What deck version (v2) is being sent.
- Which specific fund segments the v2 is going to.
- The sample size needed before the next iteration decision (chapter 6 suggests 5-10 views).
- The specific pre-registered hypothesis — what change in engagement would confirm or refute the rewrite.
- The next-iteration trigger — what pattern in the v2 engagement would trigger a v3 iteration.

### 5. Second-order analysis (Markdown, half page)

- **Target-list quality check.** Of the 25 viewers, how many were on-thesis? Do the drop-off patterns support a "deck problem" or a "target-list problem" diagnosis? Cross-reference to exercise 02.
- **Appendix utilisation.** Is the appendix pulling its weight? The 8% reach on the hiring-plan slide (15) — is that a fine "backstop for a specific question" number, or is it evidence the slide is dead weight?
- **Founder-taste check.** Which of the diagnosed slides would the founder-CEO be tempted to rewrite based on their own taste, and does that taste align with the signal? Where they diverge, note it.

## Starter guidance

- **Start with the aggregate, not the per-viewer.** The per-viewer noise is high; the aggregate pattern is the signal. Look at the aggregate first, then dig into per-viewer as diagnostics require.
- **Distinguish signal from noise.** Twenty-five viewers is a small sample. A single viewer spending 90 seconds on a slide vs. the median 20 seconds is not a signal — it's a data point. Only patterns across 4-5+ viewers should trigger a rewrite decision.
- **Do not rewrite slides that are working.** Slide 9 (team) is receiving high time and return visits — the diagnosis might be "reader is engaging deeply" (working as intended) or "reader is confused" (not working). Look at the follow-through: do readers who linger on slide 9 continue to slide 10, or do they drop? The follow-through tells you which diagnosis is correct.
- **Anchor on the practitioner benchmarks, but use them as pattern-checks, not fixed targets.** Chapter 6's point is that the benchmarks are shape-benchmarks, not level-benchmarks. Do not try to hit a specific "3.5 minute total time" number; check the shape of the engagement against the shape of the benchmark.
- **The specific rewrite hypothesis matters more than the rewrite itself.** A rewrite without a pre-registered hypothesis is a rewrite you cannot learn from. Every rewrite should test something specific.
- **Note the causal-attribution problem.** In a live raise, deck iteration happens alongside target-list re-tiering, deck-versioning, and market-conditions changes. Attributing an engagement change to a specific slide rewrite is imperfect. Design the test to isolate as much as possible (fund segment, time window, deck-version).
- **Do not chase noise.** A single fund's engagement swing does not justify a rewrite. Wait for the sample to accumulate.

## Acceptance criteria

- **The four canonical signals** each addressed with specific observations from the dataset and compared to the practitioner benchmarks (cited or marked `needs-research`).
- **Two or three specific weak slides identified** with per-slide diagnostic evidence and hypothesis.
- **Per-slide rewrite plan** with specific rewrite, hypothesis, watch-metric, and revert criterion.
- **Next-cycle hypothesis document** with pre-registered expectations for v2 engagement.
- **The second-order analysis** — target-list check, appendix utilisation, founder-taste-vs.-signal check — is included.
- **Sample-size caveats acknowledged** — 25 viewers is a small sample; conclusions are appropriately hedged.
- **The rewrite is stage-appropriate.** Chapter 9's stage-specific patterns (traction slide is load-bearing at Series-A but often light at seed) inform the rewrite priorities.
- **The rewrite plan is not just "make it better."** Every rewrite is specific enough that a designer could execute it and specific enough that the resulting engagement change would be measurable.

## Deliverables

- The DocSend-signal analysis (Markdown, ~2 pages).
- The diagnosed weak-slide set (Markdown, half page).
- The per-slide rewrite plan (Markdown, ~2 pages).
- The next-cycle hypothesis document (Markdown, half page).
- The second-order analysis (Markdown, half page).

## Extensions (optional)

- **Simulate the v2 engagement.** Invent (or have a peer invent) a v2 engagement dataset that reflects a plausible response to the rewrite. Run the analysis again, decide on v3 iterations, and document the cycle.
- **Contrast a "reader-driven" iteration with a "founder-driven" iteration.** For the same weak slide, produce two rewrites — one on the signal, one on founder taste. Predict engagement differences and articulate why the signal-driven version is more likely to work.
- **Analyse a Series-B DocSend pattern.** Chapter 9 notes that Series-B pitches often route the deck through more viewers per fund (associates, partners, sometimes investment committee). Contrast the expected engagement pattern.
- **Isolate the "wrong fund" signal.** Of the low-engagement viewers, cross-reference to the target list from exercise 02 and identify which are thesis-mismatched. Adjust the target list.
- **Design a natural experiment.** Send v1 to half of the next batch of viewers and v2 to the other half. Compare engagement between the two groups. Note the specific caveats about A/B rigor in small samples.
