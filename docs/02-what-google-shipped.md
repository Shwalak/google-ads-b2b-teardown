# 2. What Google has shipped (and why that shaped this teardown)

*As of 2026-11-04. Grades in [sources.md](sources.md).*

I started with one hypothesis: *"B2B advertisers need CRM outcomes fed back into bidding."* Research showed Google has been building exactly that. Proposing it as a gap would have been wrong, so I read the timeline first and redirected the project.

## Timeline

| When | What | What it does for lead gen | Status | Grade |
|---|---|---|---|---|
| Apr 30, 2025 | **Performance Max reporting expansion**: channel performance, full search terms, richer asset metrics | More visibility into where automated spend goes | Open beta announced | P |
| May 2025 | **AI Max for Search campaigns** | Search term matching, text customisation, final URL expansion on top of Search campaigns | Beta at launch; documented as a Search optimisation layer | P |
| 2025 | **Smart Bidding Exploration** (Search) | Bids with a ROAS tolerance to find less obvious converting queries | Launched for Search; expansion to Performance Max announced May 2026 | P |
| Apr 2026 | **Unified enhanced conversions setting** | Web and leads data accepted together; no need to choose a method | Rolling out | P |
| May 7, 2026 | **Journey-aware bidding** | Search campaigns on Target CPA learn from biddable *and* non-biddable goals across the lead-to-sale journey | Beta | P |
| May 2026 (Google Marketing Live) | **Leads in Google Ads** and **Lead Journey Mapping** | A lightweight CRM for Google-hosted form leads, and a way to map sales stages | Pilot; scope varies by source | P (titles) / S (details) |
| May 2026 (Google Marketing Live) | **Business Agent for Leads** | A Gemini agent inside the ad answers questions from the advertiser's site before a form is submitted | Pilot | P |
| Jun 15, 2026 | **Offline conversion and enhanced conversions for leads uploads moved to the Data Manager API**; blocked in the Google Ads API | Changes the plumbing advertisers use to send outcomes back | In force | P |
| Oct 2026 | **Alphabet Q3 results** | Search & other $63.35B vs $56.57B a year earlier (+12%); reported lower monetisation of AI Mode queries | Reported | P / S |

## The pattern I see

1. **The optimisation target is moving from an event to a journey.** Enhanced conversions, journey-aware bidding and the Leads screen all point the same way: from "a form was filled" toward "this lead became something".
2. **Automation is widening while controls and reports follow.** AI Max expands matching and creative; brand controls, locations of interest and extra search-term reporting arrive alongside it. Google frames this as "automation with control".
3. **Google is moving into lead capture and qualification itself.** Google-hosted lead data, a lead-stage screen, and a conversational agent bring more of the funnel inside Google's surfaces.
4. **The plumbing keeps changing.** A mandatory API migration in June 2026 is a reminder that "close the loop" is ongoing work for advertisers, not a one-time setup.

## Context I treat as interpretation, not fact

**(my view)** Alphabet reported Search & other growing 12% year on year, and press coverage of the earnings call says Google acknowledged that AI Mode queries earn less than comparable web searches while it expands ads in AI Mode. That does **not** show that Google is steering advertisers toward waste, and I am not claiming it. It does mean advertisers have good reason to want independent ways to check that expanding automation is still producing outcomes they value. Verification is a reasonable thing for any buyer of automated media to want, whatever the seller's intentions.

## What this changes in my thesis

| Before research | After research |
|---|---|
| "Feed CRM outcomes into bidding." | Google is building that. Not a gap. |
| "Lead quality is invisible." | Partly false: you can segment conversions by action today, and new stage views are arriving. |
| **Revised:** the pipes exist. The open question is whether an advertiser can **verify, trust and act on** what automation produces, with sparse, slow, messy B2B data. | |

Next: [3. User problems](03-user-problems.md)
