# Pitch Deck — the Sequoia / YC Pattern and Why the Architecture Is Not Arbitrary

## Why this matters

The pitch deck is the single most-scrutinised artifact in the raise. It is what a partner reads before a first meeting, what an associate forwards to the sponsoring partner, what the sponsoring partner reviews before the full partnership meeting, and what circulates through the fund's internal Slack when the deal is being pattern-matched. In DocSend's data — reviewed in chapter 6 — an average VC spends under four minutes on a deck they read. In those four minutes, the deck either advances the process or ends it.

Two decades of practitioner writing (Sequoia's public "Writing a Business Plan" guide, YC's *How to Design a Better Pitch Deck*, Guy Kawasaki's 10/20/30 rule, Peter Thiel's *Zero to One* framing, and countless operator-blog posts from Wilson, Suster, Skok, and others) have converged on a specific pattern for what a seed / Series-A pitch deck contains and in what order. This pattern is not arbitrary. Each slide answers a specific diligence question the reader will ask, and the ordering is designed so that the reader can pattern-match the deal without having to piece it together across slides. Deviating from the architecture without a specific reason costs conversion — the reader spends the first thirty seconds trying to find the market-size slide instead of underwriting it.

This chapter walks the canonical architecture, the specific question each slide answers, the common deviations and their costs, and the diligence-mapping the CFO can use to sanity-check the deck's completeness.

## The canonical architecture

The Sequoia / YC pattern converges on approximately eleven slides for a full seed pitch deck. Different sources name and order the slides slightly differently, but the substance is stable. The canonical list, in the recommended order:

1. **Company purpose.** One sentence describing what the company does.
2. **Problem.** What is broken. Who is affected. Why the problem is worth solving.
3. **Solution.** How the company addresses the problem. The specific product wedge.
4. **Why now.** Why the timing is right — market, technology, regulatory, distribution shifts that make the solution possible or urgent now when it was not before.
5. **Market size.** TAM / SAM / SOM. How big the market is if the company wins.
6. **Competition.** Who else is solving this problem. How the company is differentiated.
7. **Product.** What the product actually does. Screenshots or demo clips. Product roadmap.
8. **Business model.** How the company makes money. Pricing. Unit economics summary.
9. **Team.** Who the founders are. Why they are the right team to solve this problem.
10. **Financials / traction.** Where the company is today. ARR, growth rate, key KPIs. Financial forecast.
11. **The raise.** How much is being raised. What the capital funds. What the milestone bar is.

Sequoia's own version of the guide (published as "Writing a Business Plan" on sequoiacap.com) has been the canonical reference for early-stage founders for nearly two decades. YC's version emphasises brevity and clarity of language. Peter Thiel's *Zero to One* provides the conceptual framing for the "why now" and "competition" slides. See [`resources.md`](resources.md) for the specific citations.

## Why the ordering is not arbitrary

The reader of the deck — a VC associate or partner — is running a specific mental process. They are asking:

1. **What is this?** (Purpose / one-line description.)
2. **Should I care?** (Problem — is this a real problem, and is it big enough?)
3. **Does this actually work?** (Solution + Product — is there a real product that solves it?)
4. **Why has no-one solved this before, and why now?** (Why now.)
5. **How big is the prize?** (Market size.)
6. **Why do these people win?** (Competition + Team.)
7. **How does the money work?** (Business model.)
8. **What is the proof?** (Financials / traction.)
9. **What are you asking for?** (The raise.)

The canonical slide order maps to this mental process. A deck that puts "the raise" on slide 3 forces the reader to answer "what are you asking for" before they have decided "should I care." A deck that puts "team" on slide 2 forces the reader to underwrite the team before they know what the company does.

The right way to think about the ordering: **the deck is a conversation, not a document**. The reader wants to know what the company does, then whether the problem is real, then whether the solution works, in that order. Each slide answers exactly one question, and the questions come in the order the reader would naturally ask them.

## Slide-by-slide, with the diligence question each answers

### Slide 1 — Company purpose

**Content.** One sentence. The company name and what it does. Ideally so tight that a partner reading the slide alone can describe the company to another partner.

**Diligence question.** "What is this?"

**Common examples of the form:**

- "We make [product] for [customer] so that they can [outcome]."
- "We are the [system-of-record / platform / infrastructure] for [industry / function]."
- "[Product] is [comparison]-like [system] for [category]."

**What to avoid.** Words like "revolutionise," "disrupt," "AI-powered," used to obscure what the company actually does. If the sentence does not communicate what the customer buys and why, rewrite it.

### Slide 2 — Problem

**Content.** What is broken today. Who suffers from it. What the cost of the problem is (in time, money, revenue, or safety). A quantified problem is better than an unquantified one.

**Diligence question.** "Is this a real problem, and is it big enough?"

**What to include.** A specific customer archetype. A specific pain the archetype experiences. A specific cost of the pain. If possible, a direct quote from a design-partner customer that names the pain in the customer's own words.

**What to avoid.** Framing the problem as "there is no [product category] for [customer]." That is a solution restated as a problem. A problem is a customer pain, not the absence of the specific solution you sell.

### Slide 3 — Solution

**Content.** How the company solves the problem. The specific product wedge — the narrow, focused starting-point that the company enters the market with, not the ten-year platform vision.

**Diligence question.** "How is the problem solved?"

**What to include.** The specific mechanism. What the customer does with the product. What the outcome is.

**What to avoid.** A ten-year platform vision on slide 3. The full vision belongs later. Slide 3 is about the specific solution the specific product provides today.

### Slide 4 — Why now

**Content.** What shifted in the world that makes the solution possible or urgent now. Technology (LLMs are now cheap; cloud storage is now free; mobile penetration crossed a threshold). Regulation (new law, new compliance regime). Distribution (a new channel opened). Cultural (a customer archetype's willingness to buy the category changed).

**Diligence question.** "Why hasn't this been solved before, and why is now the moment?"

**What to include.** A specific market change with a specific timeline. Not "everyone is going digital" but "the passage of [specific regulation] in [year] required [specific behaviour change] which now creates [specific opportunity]."

**What to avoid.** Vagueness. If the "why now" is generic ("cloud is big"), the slide is not doing its job.

**Why this slide is load-bearing.** Peter Thiel's *Zero to One* frames it well: every established market has a graveyard of past attempts to solve the same problem. The "why now" slide is the answer to "what makes this attempt different." A deck without a "why now" reads as an entrepreneur who has not thought about whether their idea has been tried before.

### Slide 5 — Market size

**Content.** TAM (total addressable market), SAM (serviceable addressable market), and SOM (serviceable obtainable market) — or some subset. A defensible bottom-up calculation is preferred to a top-down "cite an industry report" number.

**Diligence question.** "How big is the prize if this wins?"

**What to include.** For B2B: number of target customers × average annual contract value = TAM. For consumer: number of users × ARPU = TAM. Cite the specific numbers used (a public industry report, a cited company registry count, a specific benchmark) and the specific date.

**What to avoid.** Bottom-up market sizes with implausible penetration assumptions. Top-down "$100B market from Gartner" numbers without a bottom-up cross-check. Vague statements ("large and growing"). Cited numbers that do not survive a quick fact-check.

**What good looks like.** "TAM = 15,000 target companies in the US mid-market × $250K average ACV = $3.75B. SAM within our defined ICP = 5,000 companies × $250K = $1.25B. SOM at 5% share in year 5 = $62.5M ARR."

### Slide 6 — Competition

**Content.** Who else is solving this problem. How the company is differentiated. Some decks use a 2x2 matrix; some use a feature comparison table; some use a plain-language "here's what makes us different."

**Diligence question.** "Why do these people win? What is the moat?"

**What to include.** A specific list of competitors — direct, adjacent, and status-quo (do-nothing) — and a specific line of differentiation for each. The differentiation should be defensible, not just marketing ("we're faster" is weak unless quantified).

**What to avoid.** The dishonest 2x2 that puts every competitor in the bottom-left and the target company in the top-right. Every reader has seen the dishonest 2x2 a thousand times; it reads as unserious. Also avoid "we have no competition" — every problem has an existing solution (or nothing, which is itself competition).

### Slide 7 — Product

**Content.** What the product actually does. Screenshots. Video clips if possible. A brief product roadmap.

**Diligence question.** "What is the actual thing being sold, and what's the product proof?"

**What to include.** Real product screenshots (not mockups if the product exists). If the product is technical and hard to show visually, a workflow diagram or a specific use-case walkthrough.

**What to avoid.** Marketing screenshots that do not represent the actual product. Endless feature lists. A product-roadmap slide that spans ten years and is more aspirational than the seed round justifies.

### Slide 8 — Business model

**Content.** How the company makes money. Pricing (per-seat, per-transaction, per-consumption, tiered, freemium). Unit-economics summary (ARPU / ACV, gross margin, CAC payback if available).

**Diligence question.** "How does the money work, and does the math close?"

**What to include.** The specific pricing model. The specific ACV band. The specific unit economics that are defensible (mod-102). If unit economics are pre-mature, name that and describe the design-partner pricing.

**What to avoid.** A pricing model that requires the customer to buy at a price the competitive market does not support. A gross-margin claim that does not match the actual COGS structure.

### Slide 9 — Team

**Content.** Who the founders are. Why they are the right team. Key hires or hires imminent.

**Diligence question.** "Why do these specific people win?"

**What to include.** Prior founding / operating experience. Domain expertise. Any specific "founder-market fit" story (why the founders' background gives them a unique unfair advantage). Note key hires that indicate the team is scaling.

**What to avoid.** LinkedIn-style bullet lists that read as a resume. The team slide is a story about why these specific humans win this specific market, not a CV summary.

**Why this slide is load-bearing at seed.** At seed, the deck is mostly about the founder (see chapter 9). A team slide that does not communicate why these founders are the right founders costs conversion.

### Slide 10 — Financials / traction

**Content.** Where the company is today. ARR / MRR, growth rate, key KPIs (NRR, GRR, CAC payback for B2B; DAUs, retention curves, engagement for consumer). Two- to three-year financial forecast.

**Diligence question.** "What is the proof, and where is this going?"

**What to include.** Real numbers, not projections. If pre-revenue, say pre-revenue and show the design-partner pipeline. If post-revenue, show the ARR curve, the growth rate, and one or two efficiency KPIs. Two- or three-year forecast should tie to the operating plan (chapter 1) and the milestone bar.

**What to avoid.** A hockey-stick projection with no defence. A forecast that magically grows revenue 10x without a corresponding cost ramp. A traction slide that hides the current state (a company at $30K ARR should say so, not present it as "early proof").

### Slide 11 — The raise

**Content.** How much is being raised. What the capital funds. What milestone the capital moves the company to.

**Diligence question.** "What are you asking for, and what will the money do?"

**What to include.** The round size. The specific milestone bar the capital funds (chapter 1). The specific 18-24 month operating plan the round enables. The target close date if there is one.

**What to avoid.** A specific pre-money on the deck. Pre-money is a negotiation output; putting it on the deck anchors the negotiation before the fund has evaluated the deal. The right treatment is "we are raising $X on a market-rate priced round" — the specific pre-money is discussed in a live conversation, not on slide 11.

## Common deviations and their costs

Some deviations from the canonical order are conscious and defensible. Some are unconscious and expensive. Both are worth naming.

**Defensible deviations:**

- **Traction slide moved earlier for a strong-traction company.** A Series-A company with $2M ARR growing 3x YoY can put the traction slide at slide 3 or 4, before the problem-and-solution, because the traction is the strongest signal in the deck and pattern-matches immediately. Suster's *Both Sides of the Table* argues for this at Series-A specifically.
- **Team slide moved earlier for a repeat-founder team.** A team with a specific "we exited the last company for $1B" story can put the team slide at slide 2 because the team credential *is* the pattern-match.
- **Video demo of the product embedded on slide 3 (solution) rather than slide 7 (product).** A product-led company with a compelling visual demo can compress solution and product together.

Each of these deviations trades a specific reader-experience cost for a specific pattern-match gain. When they work, they work because the founder is playing to a specific strength.

**Undefended deviations that cost conversion:**

- **The raise on slide 3.** Founder is impatient to get to the ask. Reader has not decided whether they care.
- **Market size on slide 2.** Founder wants to establish "this is big" before establishing "this is real." Reader is not underwriting yet.
- **Team on slide 10 or 11.** Founder deprioritises team relative to product. Reader still cares about who the founders are, especially at seed.
- **No "why now" slide.** Founder has not thought about it. Reader wonders whether the timing is real.
- **No competition slide.** Founder thinks the company has no competition. Reader knows every company has competition and thinks the founder is naive or dishonest.
- **Traction not on the deck at all.** For a post-revenue company, this is a major flag — the deck cannot avoid the current-state question. If the traction is disappointing, put it on and explain why (design-partner phase, product-market-fit iteration cycle, deliberate slow ramp before scale).

## The appendix

Every good pitch deck has an appendix — 10-30 slides of backup material that answer specific diligence questions that will come up in the second and third meetings. Common appendix contents:

- **Detailed unit economics.** Cohort-based LTV / CAC / payback tables (mod-102).
- **Customer references and case studies.** Design-partner quotes, logos with permission, specific customer outcomes.
- **Detailed product roadmap.** 12-24 month product plan.
- **Detailed team plan.** Hiring plan against the milestone bar.
- **Detailed financial model.** P&L / balance sheet / cash-flow forecast (usually as a downloadable file rather than a slide).
- **Cap table.** Current cap table and post-round cap table.
- **Competitive teardown.** Specific competitor product screenshots, pricing pages, positioning notes.
- **Sales-motion detail.** ICP definition, ACP, sales cycle length, close rates, pipeline coverage math.
- **Deep-dive on the "why now."** Specific data points that support the timing thesis.

The appendix is what the founder brings to the second meeting, when the sponsoring partner is doing pattern-check with their partners. The first-meeting deck is the front-of-house; the appendix is the back-of-house.

## How the CFO sanity-checks a deck

The CFO's job on the deck is not to write the deck (that is the CEO's job, informed by the deck architecture and the story). The CFO's job is:

- **Sanity-check the market-size math.** If the TAM number does not survive a bottom-up cross-check, flag it.
- **Sanity-check the unit-economics claims.** If the deck claims a 6-month CAC payback and the mod-102 model produces 14 months, one of the two is wrong.
- **Sanity-check the financial forecast.** If the forecast implies a growth rate the operating plan does not support, flag it.
- **Sanity-check the raise sizing.** If the deck claims the raise funds 24 months and the mod-103 model implies 14 months, flag it.
- **Confirm every diligence-critical claim is defensible with a specific data-room artifact.** Every claim on the deck maps to a specific data-room document that supports it (see chapter 5).

## Common founder traps

- **Writing the deck before running the "who is the reader" question.** The deck for a seed pre-seed pitch is not the deck for a Series-B pitch. The reader's questions are different. Write to the reader.
- **Ignoring the canonical architecture without a specific reason.** Every deviation costs something. Only deviate when the founder can name the specific gain and can defend the specific cost.
- **A ten-year vision on slide 3.** The company is raising a specific round for a specific milestone bar; the ten-year vision is context, not content. Save it for the appendix.
- **Marketing copy in the problem slide.** The problem slide is the customer's problem in the customer's voice, not the founder's language about the problem.
- **The dishonest 2x2 competition slide.** Every reader has seen it. It costs credibility.
- **Overloaded slides.** A slide with twelve bullet points is a slide no partner reads. One point per slide, in the fewest words that carry it.
- **Non-native design.** The deck's visual quality is a proxy for the founder's care. A sloppy deck reads as a sloppy company.
- **Excessive length.** 30-slide first-meeting decks lose the reader. 12-18 slides is the target. Everything else goes in the appendix.
- **Pre-money on the raise slide.** Anchor removal. Do not put pre-money on slide 11.
- **Deck without a "why now."** The single most-frequent missing slide in first-time-founder decks.

## What good looks like

A well-authored deck:

- Follows the canonical eleven-slide architecture unless a specific reason justifies deviation.
- Is 12-18 slides for the front-of-house version and 20-40 additional slides in the appendix.
- Each slide answers exactly one diligence question, in the order the reader would ask.
- The company-purpose slide 1 communicates what the company does in one sentence a partner can repeat to another partner.
- The traction / financials slide has real numbers and a defensible forecast.
- The raise slide names the milestone bar and the operating plan, not just the dollar amount.
- Every deck claim is backed by a specific data-room artifact.
- The visual quality is high enough that the deck reads as a serious artifact.
- The deck is versioned (v1, v2, v3) with clear notes on what changed between versions and why — critical for the iteration against DocSend signal (chapter 6).

## Summary

- The canonical Sequoia / YC pitch-deck pattern converges on approximately eleven slides in a specific order: company purpose, problem, solution, why now, market size, competition, product, business model, team, financials / traction, the raise.
- Each slide answers a specific diligence question the reader will ask; the ordering matches the natural sequence of the reader's questions.
- Deviating from the architecture without a specific reason costs conversion — the reader spends effort searching for the missing information instead of underwriting the deal.
- The CFO's job is not to write the deck but to sanity-check every quantitative claim, confirm every deck claim maps to a data-room artifact, and defend the completeness of the architecture against undefended deviations.
- The appendix (20-40 slides) is the back-of-house content that answers specific diligence questions at the second and third meetings; it is a separate artifact from the front-of-house deck.
- Common traps: the raise slide too early, no "why now," dishonest 2x2 competition, overloaded slides, pre-money on the raise slide, excessive length, and undefended deviation from the canonical order.

Chapter 5 turns to the data room — the specific set of artifacts the fund's diligence process reads once the sponsoring partner has committed to a term sheet.
