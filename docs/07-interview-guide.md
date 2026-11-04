# 7. Validation plan and interview guide

> **Status: not yet run.** This repo contains no interview findings. Everything in documents 3 to 6 that depends on user behaviour is a hypothesis until this plan is carried out. This is the plan I would follow.

## Why this comes first

The [PRD](05-prd-lead-quality-lens.md) rests on six assumptions (its section 11). One of them, whether a default quality-adjusted view already exists, I can partly check by using the product. The rest need conversations.

## Hypotheses and what would falsify them

Target: **8 to 12 interviews.** Thresholds below assume 10; scale them if the number differs. They are decision rules I am committing to in advance.

| # | Hypothesis | Supported if | Falsified if | If falsified |
|---|---|---|---|---|
| H1 | Advertisers judge automated campaigns mainly on form fills or raw conversions, not on qualified outcomes | 6 or more say their main reported metric is leads or CPL | 3 or fewer | Quality is already central; the Lens's novelty drops |
| H2 | Getting stage data into the ad account is hard or unreliable | 6 or more report gaps (missing stages, late uploads, mismatches) | 3 or fewer | Activation is not the bottleneck; drop Phase 0 emphasis |
| H3 | Seeing quality by segment today requires a manual workaround | 6 or more describe a recurring manual segment-and-join process and call it painful | 3 or fewer | The pain is smaller than assumed; reconsider the Lens |
| H4 | Advertisers would change spend based on a quality view, if trustworthy | 6 or more describe a specific past decision made from similar evidence | 3 or fewer | Insight without action; narrow to diagnostics (O2) |
| H5 | Long sales cycles make downstream outcomes arrive too late to be useful for decisions | 5 or more say a meaningful share of deals qualify or close after about two months | 3 or fewer | The 63-day limit matters less than I think |
| H6 | "Qualified" is defined inconsistently between marketing and sales | 5 or more describe disagreement or recent changes in the definition | 3 or fewer | Remove R9's emphasis; definitions are stable |

## Who to talk to

- **Mix:** 4 to 5 in-house B2B marketers, 3 to 4 agency PPC managers, and 2 to 3 sales or RevOps colleagues who consume the numbers but do not use the ad platform.
- **Criteria:** runs or relies on Google Ads for B2B lead generation; has a CRM; has used or evaluated an automated campaign type (AI Max or Performance Max).
- **Exclude:** current Google employees and anyone who would be uncomfortable discussing their work openly.
- **Sourcing:** professional communities, my own network, and LinkedIn outreach with a clear, non-salesy ask.

## Screener (5 questions)

1. Do you run, or depend on the results of, Google Ads campaigns that generate B2B leads?
2. Is there a CRM or sales tracker where leads are marked as qualified, or not?
3. Have you used AI Max for Search or Performance Max in the last 12 months?
4. What is your role?
5. Roughly how long is your typical time from first click to a closed deal? (ranges, not exact)

## Session plan (45 minutes)

| Time | Section | Purpose |
|---|---|---|
| 0 to 5 | Consent and warm-up | Set expectations; explain I am not from Google and am not selling anything |
| 5 to 15 | **Walk me through the last time you judged whether your Google Ads leads were good** | Behaviour over opinion; surfaces H1, H3 |
| 15 to 22 | How "qualified" is decided, and how outcomes get back to the ad account | H2, H6 |
| 22 to 30 | Automation: what changed when you adopted it, what you check, what worries you | Trust and verification |
| 30 to 38 | Decisions: the last time you cut or shifted spend, and what evidence you used | H4 |
| 38 to 43 | **Only now** show the concept sketch and ask for reactions | Avoid priming earlier answers |
| 43 to 45 | Wrap-up and anything I missed | |

## Question bank (non-leading)

**Behaviour first, opinion last.**

| Instead of this (leading) | Ask this |
|---|---|
| "Do you struggle with lead quality?" | "Tell me about the last lead batch that surprised you." |
| "Would you use a report that shows cost per qualified lead?" | "How did you work out cost per qualified lead the last time you needed it? Can you show me?" |
| "Is it hard to upload CRM data?" | "Walk me through how a stage change in your CRM ends up in Google Ads, step by step." |
| "Do you trust AI Max?" | "What do you check after switching on a new automated feature, and why?" |

More prompts: "What did you do next?"; "How often does that happen?"; "Who else was involved?"; "What would have changed your decision?"; "What did you try that did not work?"

## Ethics and handling

- Written or recorded consent; recording only with permission.
- Ask people **not** to share confidential company data or customer details; screen-shares use redacted or sample accounts.
- Notes stored without names; findings reported in aggregate.
- I do not represent Google and do not pitch.

## Analysis

1. Within 24 hours of each interview, write a one-page summary and tag evidence against H1 to H6.
2. Affinity-map behaviours and quotes across interviews; keep a log of *contradicting* evidence.
3. Apply the decision rules in the table, with counts, before interpreting them.
4. Update [3](03-user-problems.md), [4](04-opportunities-and-prioritization.md) and the PRD's kill criteria with what was found, including where the evidence argues against the concept.

## What I would do with the results

| Outcome | Next step |
|---|---|
| H3 and H4 supported | Proceed to Phase 0 and a Phase 1 prototype test |
| H2 supported, H3 weak | Promote the readiness diagnostic (O2) and shelve the Lens |
| H1 falsified | Re-examine the thesis; quality may already be central for these advertisers |
| H5 strongly supported | Make the attribution-window blind spot a first-class feature |
