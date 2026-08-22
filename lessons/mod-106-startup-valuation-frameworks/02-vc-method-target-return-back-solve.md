# The VC Method — Target Return, Target Exit Value, and the Back-Solve

## Why this matters

An anchor-method bracket (chapter 1) tells you what an angel-group screen will defend at a seed round. It does not tell you what an institutional VC will pay. Institutional VCs run a specific piece of arithmetic on every deal they see, and it is the arithmetic that ultimately determines whether they take the deal to their partnership: given the fund's target return, given the assumed multiple of invested capital they need out of this specific investment for the fund math to work, given the assumed dilution the company will take between now and the exit, given a plausible exit value — what pre-money can they pay today?

That arithmetic is the **VC method** (sometimes called the "venture capital method"), first formalised by Bill Sahlman at Harvard Business School in the 1980s and taught in most MBA venture-finance curricula since. Its published reference is Sahlman's "A Method for Valuing High-Risk, Long-Term Investments" (HBS Note 9-288-006, 1987, updated multiple times since). The version used in practice by working VCs is a slight simplification of Sahlman's academic version, but the structure is identical: work backwards from an exit-value hypothesis, apply a target return, adjust for dilution, and solve for a pre-money the VC can defend inside their fund's partnership economics.

A founder-CFO going into a priced round without having run this calculation from the VC's side is negotiating blind. The VC has run it. The lead partner has an internal target pre-money that satisfies the fund's return math. If the founder's asked-for pre-money is outside the VC's target, the round does not close — regardless of what the anchor-method bracket says, regardless of what the market-conditions data (chapters 6-7) suggest, regardless of what the founder's pitch narrative supports.

This chapter installs the VC method as a first-principles calculation, then walks the partnership economics that constrain the VC's target return, then shows the CFO-side use of the calculation as a check on the founder's asked-for pre-money.

## The method in its basic form

The VC method reduces to a chain of four numbers:

1. **Target exit value** (the estimated valuation at which the company exits — IPO or acquisition — in year N).
2. **Target return multiple** (the multiple of invested capital the VC needs on this specific investment for the fund math to work).
3. **Assumed dilution schedule** (the fraction of the company the VC's shares will represent at exit after future rounds and pool top-ups have diluted their ownership).
4. **Pre-money valuation** at today's round (the back-solved answer).

The identity that ties them together:

```
Required post-money ownership today
  = target return multiple × investment amount / target exit value × (1 + total future dilution)
```

Or, equivalently, if you want to expose the post-money directly:

```
Post-money today = (investment amount × target return multiple) / (post-round ownership at exit)
Pre-money today  = Post-money today - investment amount
```

Where **post-round ownership at exit** is the fraction of the exit-value proceeds the VC will receive after all future dilution has been applied to the ownership they buy today.

The mechanic in prose: the VC has to end up with enough of the exit-value pie to hit their target return multiple on the cheque they wrote today. Since the company will dilute them between today and exit, they have to buy a bigger slice today than they need at exit. The pre-money that lets them buy that bigger slice is what they can pay.

## Worked example — Sahlman's canonical structure

Setup:

- **Investment today:** $5,000,000 (a lead cheque into a Series-Seed).
- **Target exit value in year 5:** $500,000,000 (a plausible acquisition-scale exit for a well-executed SaaS company).
- **Target return multiple:** 10× (a modest early-stage target — chapter later on why the modal number is 20-30× for pre-seed).
- **Assumed future dilution:** the company will do a Series-A, Series-B, and Series-C, each of which will dilute existing shareholders. Assume the aggregate dilution from today's ownership to exit is 60%, meaning today's shareholder retains 40% of their post-Series-Seed ownership at exit.

**Step 1. Compute the VC's required exit-value share.**

- Required exit proceeds = investment × target return = $5M × 10 = **$50M**.
- Required share of exit value = $50M / $500M = **10%**.

**Step 2. Adjust for future dilution.**

- If the VC's ownership will be diluted to 40% of what they buy today, then to end up at 10% at exit they must buy 10% / 40% = **25%** today.

**Step 3. Solve for pre-money.**

- Post-money today = investment / today-ownership = $5M / 25% = **$20M**.
- Pre-money today = $20M - $5M = **$15M**.

**Interpretation.** At a $15M pre-money on a $5M cheque, the VC gets 25% of the company today. Through the assumed Series-A / B / C dilution, that 25% falls to 10% by exit. At a $500M exit, 10% is $50M, which is 10× the $5M investment. If the founder asks for a $30M pre-money, the VC's post-money slice is $5M / $35M ≈ 14.3% today, dropping through dilution to 14.3% × 40% ≈ 5.7% at exit, or $28.6M on a $500M exit — a 5.7× return, which is a losing pitch to the partnership.

## The four inputs, one at a time

### Input 1 — the target exit value

The target exit value is the single most-contested input. It has to be:

- **Anchored to real exits in the target's category.** Look at recent M&A transactions and IPOs in the target's specific space and read the disclosed transaction values (SEC 8-K filings for public acquirers, S-1 filings and IPO pricing data for IPOs, PitchBook or Crunchbase for private M&A). Ideally, cite specific comparable exits.
- **Plausible for the target company's trajectory.** A $500M exit hypothesis for a company that would need to reach $50M ARR at a 10× revenue-multiple exit is testable. Can the company reach $50M ARR in year 5? What growth trajectory does that require? What CAC / burn does that trajectory imply? If the model doesn't support the trajectory, the exit hypothesis doesn't support the pre-money.
- **Consistent with the market-conditions data.** Multiples move over time (chapter 4). An assumed 10× exit multiple in a market currently trading at 6× is a headwind on the exit hypothesis.

The VC will run their own exit hypothesis inside the partnership meeting. If the founder's pitch has a $2B exit hypothesis and the partner's independent read is $500M, the partner will use $500M in the VC-method calculation and derive a much lower pre-money offer. The founder's job is not to convince the VC of a specific exit value; it is to give the VC enough evidence to run a defensible internal exit hypothesis that supports the founder's asked-for pre-money.

### Input 2 — the target return multiple

The target return multiple is set at the **fund level**, not at the deal level. It is derived from the fund's target IRR, the expected loss ratio in the portfolio, and the expected time to exit.

The standard early-stage VC fund is structured as follows (Kupor, *Secrets of Sand Hill Road*, and Feld & Mendelson, *Venture Deals*, both cover this — see [`resources.md`](resources.md)):

- **Fund life:** typically 10 years (extendable), with the investment period in the first 3-5 years and harvest in the last 5-7.
- **Portfolio construction:** ~20-30 companies per fund.
- **Loss ratio:** the accepted rule-of-thumb pattern for a well-performing early-stage fund is roughly 1/3 total losses, 1/3 modest returns (1-3×), 1/3 meaningful returns (3×+), with the fund's total return driven by a small number of very large winners. Actual distributions vary widely — see the Correlation Ventures data (referenced in [`resources.md`](resources.md)) for empirical distributions of VC returns.
- **Fund target return:** most institutional early-stage funds target a fund-level 3× net-to-LPs or better, corresponding to roughly 25%+ IRR net of fees.
- **Per-deal target:** because most deals will return 0-1×, the winners need to return at very high multiples. A common heuristic: seed-stage lead investments should have a plausible path to **10-30× MOIC** (multiple on invested capital) for the fund math to work. Very early pre-seed cheques target 30×+.

That range — 10× at the low end for later-seed / Series-A, 30×+ for pre-seed — is the target-return input to the VC method. The number is not arbitrary; it comes from the fund's partnership economics, and the CFO can back-solve it if they know the fund's stage, fund size, and portfolio-construction pattern.

A separate consideration: the target return multiple **also depends on the assumed probability of success**. A "risk-adjusted" version of the VC method (Sahlman's academic formulation) applies a probability weight to the exit hypothesis and back-solves against expected value rather than target value. In practice VCs run the simple version with high target multiples that implicitly bake in the probability adjustment.

### Input 3 — the dilution schedule

Between today's round and exit, the company will:

- Raise one or more subsequent priced rounds (each of which sells new preferred to a new investor and dilutes existing shareholders).
- Refresh the option pool at each of those rounds (each pool refresh dilutes existing shareholders unless it is placed as new-money-dilutive, which is unusual — see [mod-104 chapter 2](../mod-104-cap-tables-and-equity-compensation/02-pre-vs-post-money-math-and-the-option-pool-shuffle.md) for the pool shuffle mechanic).
- Possibly do a secondary transaction (which typically does not dilute, but may reset the reference-price context — see chapter 8).

The assumed dilution is a **compound** of the per-round dilution. If a company does a Series-A (25% dilutive to existing shareholders, including the pre-priced-round pool shuffle), a Series-B (20% dilutive), and a Series-C (15% dilutive), a pre-Series-A shareholder ends up owning:

```
(1 - 0.25) × (1 - 0.20) × (1 - 0.15) = 0.75 × 0.80 × 0.85 = 0.51
```

51% of what they had before the Series-A. In the running example we assumed 40% retention (a somewhat more dilutive path), which is realistic for a company doing four rounds after today. The specific dilution assumption depends on:

- **How many rounds the company is likely to raise before exit.** More rounds = more dilution.
- **The typical per-round dilution at each stage.** Chapter 7's Carta data gives median dilution by stage; chapter 6's PitchBook-NVCA data cross-checks against a different dataset. Typical medians hover around 15-25% dilution per priced round.
- **The pool-refresh frequency and size.** A company that refreshes the pool to 10% at each round adds a further couple of percent per round to existing-shareholder dilution.

The CFO should build the assumed dilution as an explicit round-by-round ladder rather than a single lump-sum percentage. That makes the assumption debatable component-by-component in the negotiation.

### Input 4 — the pre-money (the output)

The pre-money is what falls out of the calculation once the other three inputs are set. It is *the answer*, not an input.

That framing matters because founders sometimes present the pre-money as a demanded input and then dispute the other three when the VC pushes back on the ownership implied. The productive negotiation posture is the reverse: agree on the four inputs (exit value, target return, dilution schedule), then the pre-money is determined arithmetically. Where the negotiation happens is in **what the four inputs should be**, not in an unmoored back-and-forth over the pre-money.

## The formal formula

The VC-method identity for pre-money, given the four inputs:

```
required ownership today = (target multiple × investment) / (target exit value × retention through dilution)

post-money today         = investment / required ownership today

pre-money today          = post-money today - investment
```

Substituting:

```
pre-money = investment × [(target exit value × retention) / (target multiple × investment) - 1]
         = investment × [(target exit value × retention) / (target multiple × investment)] - investment
         = (target exit value × retention) / target multiple - investment
```

Simpler form:

```
post-money today = (target exit value × retention) / target multiple
pre-money today  = post-money today - investment
```

Where **retention** is the fraction of today's ownership the investor retains through all future dilution (in the running example, 0.40).

Sanity check on the running example:

- post-money = ($500M × 0.40) / 10 = $200M / 10 = $20M ✓
- pre-money = $20M - $5M = $15M ✓

## Partnership economics — why the target multiple is what it is

A VC's target multiple on a deal is not the return the VC personally wants. It is the return the deal has to produce for the *fund* to hit its promised return to its *limited partners*, once the fund's math is unpacked.

The unpacking (simplified — Kupor's *Secrets of Sand Hill Road* is the canonical practitioner reference):

- A fund raises capital from LPs (institutional investors — pension funds, endowments, family offices, funds-of-funds). The LPs are promised a return, typically expressed as a target multiple (e.g., 3× the fund) or an IRR (e.g., 25% net).
- The fund's general partners (GPs) charge a **management fee** (typically 2% per year for the investment period, tapering) and **carried interest** (typically 20% of the fund's net gains above the LP-return hurdle).
- The fund invests over 3-5 years across 20-30 companies. Most of those companies will fail or produce modest returns. A small number will produce very large returns.
- For the fund to return 3× its capital, the aggregate exit proceeds from all portfolio companies must be 3× the fund size, net of losses.
- If two-thirds of the portfolio produces 0-1× and the remaining one-third has to carry the fund to 3×, the one-third must produce a blended ~9×. Within that one-third, a single "fund-returner" — a company that returns the entire fund size on the investment made — is what makes the math work.

The consequence for pricing: the lead partner on a specific deal is asking, "if I put $5M into this company, what has to happen for this deal alone to return the fund?" If the fund is $250M, returning the fund requires the $5M to become $250M — a 50× MOIC on this specific cheque. That number is why very-early-stage funds require the possibility of 30×+ returns on their winners.

That is also why a fund with a larger commitment size (e.g., $10M cheque into a $500M fund) has a lower per-deal target multiple than a $5M cheque into a $200M fund (50× vs. 50× on the surface, but the larger cheque has less remaining upside because the entry pre-money is higher). Bigger funds writing bigger cheques into later-stage rounds accept lower per-deal multiples and rely on more of the portfolio contributing to the fund return.

**Practical implication for the CFO:** when preparing for a fundraise, look up the target investor's most recent fund size and typical cheque size (public data from PitchBook, Crunchbase, or the fund's own website). Back into the fund-returner multiple. Use that as the target-multiple input to the VC method run from the investor's side. That is the number that determines whether the pre-money you're asking for clears the partnership.

## The three "flavours" of the VC method in practice

The academic VC method has three variants that the CFO should recognise:

### Flavour 1 — the basic VC method (Sahlman's original)

The version walked in the running example. Single-round investment, single-point exit hypothesis, single target-return multiple, single dilution assumption, back-solve to pre-money. This is the version most working VCs run in their head when they first see a deal.

### Flavour 2 — the risk-adjusted VC method

Adds probability weights to the exit hypothesis. Instead of a single "$500M exit" point, the VC assumes:

- 40% probability the company fails (exit value = $0).
- 30% probability of a modest exit ($100M).
- 20% probability of a meaningful exit ($500M).
- 10% probability of a large exit ($2B).

The expected exit value is `0.4 × 0 + 0.3 × 100 + 0.2 × 500 + 0.1 × 2000 = 0 + 30 + 100 + 200 = $330M`. The VC method is then run against $330M rather than $500M, producing a lower pre-money.

The risk-adjusted version is more theoretically defensible but harder to run in a partnership meeting because the probabilities are inherently subjective. Most working VCs use it as a sanity-check on the basic version, not as the primary calculation.

### Flavour 3 — the "target ownership" heuristic

A simpler variant that skips the exit-value hypothesis entirely. The VC says "we need to own X% of the company at first close for the fund math to work, target X% is Y%, our cheque is Z — so the post-money is Z / Y%." Common target ownership percentages at seed for institutional funds: 10-20%. This flavour is what a founder often encounters in the first partner conversation ("we need to own 15% here") before the deeper VC-method work happens in diligence.

The target-ownership heuristic collapses the VC method's four inputs into one number (the target ownership) that implicitly assumes the other three. When the CFO hears "we need to own X%," the CFO's mental translation should be "the VC has run the VC method against their target exit value and target multiple and dilution assumption, and X% is what fell out." The negotiation then proceeds by unpacking those implicit assumptions.

## The CFO's use of the calculation

The founder's CFO or finance lead should run the VC method **from the investor's side** before any partner meeting. The output tells them:

- **What pre-money is likely to close the round?** If the anchor-method bracket says $8M-$12M and the VC method from the target investor's side says $6M-$8M, the round is likely to close at $7M-$8M. Preparing to defend a $12M ask when the VC-method math supports $8M is a way to lose the round.
- **Which of the four inputs to negotiate?** The pre-money is what falls out of the four inputs; the productive negotiation is over the exit-value hypothesis (build the model that supports a higher exit), the assumed dilution (make the case for fewer or smaller future rounds), or the target multiple (unlikely to move — it is set at the fund level).
- **Which investors to target?** A fund with a smaller size, less need for a fund-returner from each investment, or a later-stage focus will accept lower per-deal multiples and a higher pre-money. A pre-seed fund whose entire portfolio construction requires 30×+ winners will not pay the pre-money a Series-A fund would pay for the same company.
- **When to walk from a round.** If no institutional investor's VC-method math clears the founder's minimum pre-money, either the founder's expected pre-money is wrong or the fundraise should be delayed until the company's exit hypothesis is bigger.

## Common founder traps

- **Treating the pre-money as an input.** Founders sometimes present a pre-money as a demanded number without articulating the exit-value, target-return, and dilution assumptions that would support it. The VC will silently run their own version of those three inputs and derive a different pre-money. The productive posture is to make the four inputs explicit.
- **Ignoring the fund-level math.** "Sequoia paid $50M pre for company X" is not evidence that Sequoia will pay $50M pre for your company; their VC-method math on company X supported that pre-money, and their math on your company will produce a different number.
- **Anchoring to a stale target-return heuristic.** In a rising market, target multiples can compress (bigger funds writing bigger cheques accept lower multiples). In a compressing market, target multiples expand (LPs demand higher IRRs; VCs demand higher-multiple deals). The 10-30× range is a rule of thumb, not a fixed constant.
- **Using an exit-value hypothesis the model doesn't support.** A $2B exit in year 5 requires a specific ARR and growth trajectory. If the driver-based model (mod-103) doesn't produce that trajectory, the exit-value hypothesis doesn't survive diligence.
- **Assuming zero further dilution.** Every subsequent round dilutes. Modelling with zero further dilution understates the pre-money the VC needs today and produces an over-optimistic answer.
- **Confusing the VC method with the DCF.** The VC method is not a DCF. It does not discount future cash flows; it back-solves from an exit-value hypothesis against a target return. Chapter 5 explains where a DCF applies and where it doesn't.
- **Failing to cross-check the VC method against the anchor bracket and the market-conditions data.** If the VC method says $15M pre, the anchor bracket says $8M-$12M, and the market says $5M-$9M for comparable rounds, the VC-method output is likely too aggressive. All three lenses have to agree for the price to hold.

## What good looks like

A finance leader running the VC method:

- Builds the calculation for each target lead investor on the list, using public data on the fund's size, stage, and cheque pattern.
- Sensitises across target-exit-value (base / bull / bear), target-return multiple (10× / 20× / 30×), and assumed dilution (three-round / four-round paths).
- Reconciles the calculation output with the anchor-method bracket (chapter 1) and the market-conditions data (chapters 6-7).
- Presents the exit-value hypothesis as an explicit, model-defensible number rather than a demanded pre-money.
- Prepares the founder to defend the four inputs component-by-component, not the pre-money as a single number.
- Knows which target investors' math clears the round's minimum pre-money and which don't, and prioritises accordingly.

## Summary

- The VC method back-solves a pre-money valuation from four inputs: target exit value, target return multiple, assumed dilution schedule, and investment amount.
- The identity: `post-money today = (target exit value × retention through dilution) / target multiple`; `pre-money today = post-money - investment`.
- The target return multiple is set at the fund level by the fund's partnership economics — LP-promised return, portfolio-construction pattern, loss ratio. Early-stage funds target 10-30× MOIC on their winners because most of the portfolio will return 0-1×.
- Three flavours: the basic method (single-point exit and multiple), the risk-adjusted method (probability-weighted exit), and the target-ownership heuristic (collapse the four inputs into a single ownership target).
- The productive negotiation is over the four inputs, not over the pre-money. The pre-money is what falls out of the arithmetic.
- The CFO's job is to run the calculation from each target investor's side, cross-check against the anchor-method bracket (chapter 1) and market-conditions data (chapters 6-7), and prepare the founder to defend the exit-value hypothesis, the dilution schedule, and (where possible) the target multiple.

Chapter 3 turns to revenue-multiple valuation — the framework that replaces the VC method (or complements it) as the primary anchor at Series-A and later, once the company has a defensible revenue trajectory that can be multiplied by a comp-set multiple.
