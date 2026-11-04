# Automation vs control: a product teardown of Google Ads for B2B lead generation

> **Independent and unofficial.** Not affiliated with, endorsed by or written on behalf of Google. Written from public sources, current as of **2026-11-04**. Product details change fast, so check anything you plan to rely on.

**Thesis:** Google has built most of the *pipes* for lead-quality optimisation. The open B2B problem is whether an advertiser can **verify, trust and act on** what automation produces, with sparse, slow and messy data.

## The short version

- **I started with a hypothesis that turned out to be wrong.** I expected the gap to be "feed CRM outcomes back into bidding". Research showed Google is already building that (enhanced conversions for leads, journey-aware bidding in beta, a Leads screen and a lead-qualifying chat agent in pilot). So I redirected the project instead of proposing something already on Google's roadmap. See [what Google shipped](docs/02-what-google-shipped.md).
- **A structural constraint stays unsolved for long B2B sales cycles.** Per Google's help documentation, offline conversions uploaded more than **90 days** after the last click are not imported, and for enhanced conversions for leads the limit is **63 days**. A deal that qualifies or closes later cannot be attributed to its click.
- **The opportunity I chose:** a *Lead Quality Lens*, a report of cost per qualified lead by search term, asset, landing page and channel, honest about uncertainty and about leads that are still too young to judge. Its first phase is a readiness check, because the Lens only works for advertisers who supply stage data. See the [PRD](docs/05-prd-lead-quality-lens.md).
- **My own prioritisation did not pick it.** RICE ranked the cheaper readiness diagnostic first (1.40 vs 0.48). I chose the Lens anyway, flagged the override as a judgment call, folded the diagnostic in as Phase 0, and wrote down the evidence that would change my mind. See [prioritization](docs/04-opportunities-and-prioritization.md).
- **What I am least sure of:** whether a default quality-adjusted view already exists, and whether B2B volumes support the statistics. Both are named as open questions with a plan to test them.

## Read in this order

| # | Document | What it answers |
|---|---|---|
| 1 | [Product map](docs/01-product-map.md) | Who the users are, how data flows, what Google automates vs what the advertiser owns, constraints |
| 2 | [What Google shipped](docs/02-what-google-shipped.md) | 2025 to 2026 timeline and how it changed the thesis |
| 3 | [User problems](docs/03-user-problems.md) | Six problems, each with evidence strength, counter-evidence and confidence |
| 4 | [Opportunities and prioritization](docs/04-opportunities-and-prioritization.md) | Five options, RICE scores, sensitivity and the override decision |
| 5 | [PRD: Lead Quality Lens](docs/05-prd-lead-quality-lens.md) | The proposed product: phases, definitions, statistics, requirements, tradeoffs, risks, kill criteria |
| 6 | [Metrics and experiment plan](docs/06-metrics-and-experiment-plan.md) | Metric tree, guardrails, test design, sample sizes, decision rules |
| 7 | [Validation plan](docs/07-interview-guide.md) | Falsifiable hypotheses and the interview guide to test them |
| | [Sources and evidence grades](docs/sources.md) | Every source, graded primary / secondary / anecdotal, plus what I checked and did not use |

## How I handled evidence

Each claim is graded in [sources.md](docs/sources.md): **P** for Google's own pages, **S** for third-party reporting, **A** for anecdote. Anecdotes show that a belief exists, never how common something is. Google's reported results (for example, AI Max uplift averages) are labelled as Google's claims. Where I could not verify something it is marked as a hypothesis, and a few claims with only one weak source are left out on purpose. My interpretations are tagged **(my view)** so they are not mistaken for facts.

## Limits, stated plainly

- **No user research.** The interview plan is written; no interviews have been run. Everything about user behaviour is a hypothesis.
- **Public sources only.** I have not tested these features in a live account for this repo, and several 2026 features are pilots or betas whose availability I could not confirm.
- **My scores are judgments.** The RICE inputs are reasoned estimates, shown so they can be challenged, not data.
- **The concept sketch uses invented layout numbers** and is labelled as such. No figure in the sketch is real.
- **Sample sizes in the experiment plan use hypothetical baselines** to show the reasoning.

## About

Written by Saksham, an AI and technical product manager, from the perspective of someone who has managed B2B Google Ads campaigns. No employer data or confidential information is used anywhere in this repo. The research questions, the pivot, the prioritization override and the judgments are mine to defend.

A related project: **ShipGate**, a launch-readiness evals tool. The PRD's approach to gating generated summaries comes from it.

## License

MIT
