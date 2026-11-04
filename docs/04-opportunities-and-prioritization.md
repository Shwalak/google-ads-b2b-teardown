# 4. Opportunities and prioritization

## Five candidate opportunities

| # | Opportunity | In one line |
|---|---|---|
| O1 | **Lead Quality Lens** | Cost per *qualified* lead by search term, match source, asset, landing page and channel, with uncertainty and "too early to tell" handling |
| O2 | **Quality-readiness diagnostic** | Detect form-fill-only goals, missing click IDs and unmapped stages, and guide the fix |
| O3 | **Bid-stage advisor** | Recommend which funnel stage to bid on, given conversion volume and sales-cycle length |
| O4 | **B2B firmographic controls** | Target or exclude by company size and industry in automated campaigns |
| O5 | **AI Max incrementality check** | A low-volume-friendly holdout test judged on qualified outcomes |

O4 is flagged now: I could not verify whether firmographic targeting already exists, and it carries privacy and policy risk. Its confidence is scored low for that reason.

## Scoring method

[RICE](https://www.intercom.com/blog/rice-simple-prioritization-for-product-managers/): score = Reach × Impact × Confidence ÷ Effort. **All inputs are my judgments**, not measurements. The point is to make my reasoning visible and challengeable.

| Input | Scale |
|---|---|
| Reach | 1 to 5: share of B2B lead-gen advertisers who meet the precondition and would use it |
| Impact | 0.25 minimal, 0.5 low, 1 medium, 2 high, 3 massive: effect on the share of spend judged and optimised on qualified outcomes |
| Confidence | 30% to 100%: how sure I am of the other three, given the evidence |
| Effort | Rough person-months for a first shippable version |

## Scores and rationale

| # | Reach | Impact | Confidence | Effort | **RICE** | Why |
|---|---|---|---|---|---|---|
| O1 Lens | 2 | 2 | 60% | 5 | **0.48** | Needs downstream stage data to exist, which limits reach. High impact: changes how spend is reallocated. Confidence capped by unknown statistical usefulness at B2B volumes and possible overlap with what Google already shows. |
| O2 Readiness | 4 | 1 | 70% | 2 | **1.40** | Touches nearly every lead-gen account. Medium impact: nudges setup, but cannot supply CRM follow-through. Cheap to build. |
| O3 Stage advisor | 2 | 1 | 50% | 3 | **0.33** | Advice only; Google already publishes guidance; journey-aware bidding behaviour unknown. |
| O4 Firmographics | 4 | 2 | 30% | 8 | **0.30** | Large potential, but existence unverified, and privacy and policy work is heavy. |
| O5 Incrementality | 3 | 1 | 40% | 4 | **0.30** | Informs a one-time decision; B2B volume makes tests noisy. |

## What the numbers say, honestly

**RICE ranks O2 first, about three times ahead of O1 (1.40 vs 0.48).** I did not adjust the scores to change that.

How robust is it?

| Change | O2 | O1 | Ranking |
|---|---|---|---|
| Baseline | 1.40 | 0.48 | O2 first |
| O2 impact drops to "low" (0.5) | 0.70 | 0.48 | O2 still first |
| O2 impact drops to "minimal" (0.25) | 0.35 | 0.48 | **O1 first** |
| O1 scored optimistically (reach 3, impact 3, confidence 80%, effort 4) | 1.40 | 1.80 | **O1 first** |

So the whole disagreement comes down to one question: **does a diagnostic change advertiser behaviour on its own?**

## Decision

**Deep-dive PRD: O1, the Lead Quality Lens, with O2 built in as its first phase.** This is a **judgment call that overrides the top RICE score, and I am flagging it as such.** My reasons:

1. **O2's impact is probably lower than I scored.** Google already ships an enhanced conversions diagnostics report and an implementation checklist. The blocker for most advertisers is more likely CRM follow-through than awareness. This is a belief, not a finding, and I will test it in interviews (see [07](07-interview-guide.md)).
2. **The two are not independent, and RICE treats them as if they were.** A diagnostic asks the advertiser for work (capture click IDs, map stages, upload outcomes). The Lens is the reward that makes that work worthwhile: complete the setup and you see where your spend actually produces qualified leads. O2 supplies the data; O1 supplies the reason.
3. **The RICE ordering still shapes the roadmap.** Because O2 is cheap and broad, it ships first as **Phase 0 (activation)** inside the PRD, before the Lens itself.

If interviews show a diagnostic *alone* moves behaviour, the right move is to ship O2 and shelve the rest of the Lens. The PRD includes that as an explicit kill criterion.

## What evidence would change this ranking

| Finding | Effect |
|---|---|
| Google already ships a default quality-adjusted breakdown by search term or asset | O1's impact and confidence drop sharply; promote O2 or O3 |
| Most target advertisers have no downstream stage data at all | O1's reach is smaller than 2; O2 becomes the prerequisite, not an add-on |
| Advertisers say they already join reports successfully and trust the result | O1's impact drops |
| Firmographic targeting is confirmed absent and feasible | O4's confidence rises; revisit |

Next: [5. PRD: Lead Quality Lens](05-prd-lead-quality-lens.md)
