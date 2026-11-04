# Sources and evidence grades

Everything factual in this repo traces to a source below. All pages were accessed on **2026-11-04**.
Product details change quickly, so treat anything here as true *as of that date*.

## How I grade evidence

| Grade | Meaning | How I use it |
|---|---|---|
| **P** | Primary: Google's own documentation, blog, announcement page or Alphabet filing. | Facts about what the product does or what Google claims. A Google *claim* about results is still a claim; I say "Google reports". |
| **S** | Secondary: reporting or analysis by a third party about a primary event. | Context, and details I could not find in a primary source. Flagged where used. |
| **A** | Anecdotal: forum posts, agency blogs, opinion. | Shows that a belief or experience *exists*. Never used as evidence of how common something is. |

Anything I could not verify is listed at the bottom and is not used as fact.

## Google primary sources (P)

| Topic | Source | Used for |
|---|---|---|
| AI Max: how it works | https://support.google.com/google-ads/answer/15910187 | Search term matching, asset optimisation, controls and reporting |
| AI Max: launch | https://blog.google/products/ads-commerce/google-ai-max-for-search-campaigns/ | Google-reported "14% more conversions or conversion value at a similar CPA/ROAS" (27% for exact/phrase-heavy campaigns) |
| AI Max: 2026 update | https://business.google.com/us/accelerate/announcements/ai-max-for-search-campaigns/ | Google-reported 7% figure (non-retail, 2026); AI Brief and text disclaimers |
| AI Max is a layer, not a campaign type | https://developers.google.com/google-ads/api/docs/campaigns/ai-max-for-search-campaigns/getting-started | Product map |
| Enhanced conversions for leads | https://support.google.com/google-ads/answer/15713840 | Hashed first-party data matching; June 15, 2026 Data Manager API migration; April 2026 unified setting |
| Offline import time limits | https://support.google.com/google-ads/answer/15081888 | **90 days** after last click (standard) and **63 days** (enhanced conversions for leads) |
| Conversion reporting by action | https://support.google.com/google-ads/answer/3419678 and https://developers.google.com/google-ads/api/docs/conversions/reporting | "All conversions" can be segmented by conversion action; the API exposes `segments.conversion_action` |
| Journey-aware bidding | https://blog.google/products/ads-commerce/bidding-budgeting-google-marketing-live-2026/ (dated 2026-05-07) and https://business.google.com/us/accelerate/announcements/journey-aware-bidding/ | Beta; Target CPA (and Maximize conversions per the Accelerate page); learns from biddable and non-biddable goals |
| Google Marketing Live 2026 highlights | https://business.google.com/us/accelerate/googlemarketinglive/ | Titles and one-line descriptions of Leads in Google Ads, Lead Journey Mapping, Business Agent for Leads, Missed Opportunity Reporting |
| Business Agent for Leads | https://blog.google/products/ads-commerce/google-marketing-live-search-ads/ | Gemini-built agent inside the ad |
| Performance Max best practices for lead gen | https://support.google.com/google-ads/answer/13775965 | "AI is only as good as the inputs"; use deeper-funnel goals; at least 15 conversions in 30 days for value-based goals; spam mitigations are advertiser-side (qualifying questions, reCAPTCHA, server-side validation) |
| PMax reporting expansion | https://blog.google/products/ads-commerce/channel-performance-reporting-coming-to-performance-max/ (2025-04-30) | Channel performance reporting, full search terms reporting, richer asset metrics; Google's caution that *average* return by channel "doesn't tell the full story" (marginal ROI) |
| Alphabet Q3 2026 results | https://s206.q4cdn.com/479360582/files/doc_financials/2026/q3/2026q3-alphabet-earnings-release.pdf | Google Search & other $63.35B vs $56.57B (+12%); Google advertising $82.0B |
| Alphabet CEO remarks, Q3 2026 | https://blog.google/company-news/inside-google/message-ceo/alphabet-earnings-q3-2026/ | Context on Search momentum |

## Vendor documentation (P for what the vendor says it does)

| Topic | Source | Used for |
|---|---|---|
| HubSpot to Google Ads conversion sync | https://knowledge.hubspot.com/ads/create-and-sync-ad-conversion-events-with-your-google-ads-account | Evidence that CRM-side connectors for lifecycle stage events exist |

## Secondary (S)

| Topic | Source | Used for | Caveat |
|---|---|---|---|
| Leads in Google Ads screen | https://ppc.land/google-ads-gets-a-native-leads-screen-that-bypasses-the-crm-tab/ | Description of the Leads screen: Google-hosted form leads, 60 days, four stages (raw, qualified, converted, lost) | Third-party report of a pilot. Google's own highlights page describes it as a "lightweight CRM built right into Google Analytics" while naming it "Leads in Google Ads"; I treat exact scope and availability as unverified. |
| AI Mode monetisation | https://searchengineland.com/google-earnings-call-q3-2026-499706 and https://arstechnica.com/gadgets/2026/10/google-admits-ai-search-makes-less-money-but-its-fixing-that-with-more-ads/ | Reported statement that AI Mode queries monetise less than comparable web searches; ads expanding in AI Mode | Google did not disclose the size of the gap (per Search Engine Land). |
| Journey-aware bidding setup advice | https://learn.jyll.ca/blog/google-ads-journey-aware-bidding-the-next-bid-strategy-for-lead-generation and https://www.getpassionfruit.com/blog/google-ads-journey-aware-bidding-what-advertisers-need-to-know | Practitioner reading: import CRM stages, categorise conversions, pick one end-stage goal | Availability ("closed beta") differs by source. |
| Conversion-by-action cost limitation | https://www.riibon.com/blog/see-conversions-by-individual-action-google-ads | A vendor says segmenting by conversion action splits the conversions column but blanks cost, so you must join reports | Vendor claim, not verified in the product. Used only as a hypothesis to test in interviews. |

## Anecdotal (A): evidence that a belief exists, not that it is common

| Topic | Source |
|---|---|
| Spam or junk leads under automation when only form fills are tracked | https://riverstonemarketingsolutions.com/performance-max-spam-leads/ (agency; says "our experience, not a controlled test"), https://www.definedigitalacademy.com/blog/performance-max-for-lead-gen-businesses-do-this-first, https://campdigital.com/2024/03/04/mastering-google-performance-max-for-lead-generation-a-troubleshooting-guide/, https://www.reddit.com/r/PPC/comments/1kd28qw/performance_max_advice_for_b2b_lead_gen/ |
| **Counter-example:** PMax worked for B2B lead gen | https://www.webfx.com/blog/ppc/pmax-for-b2b-lead-gen/ (agency) |

## Checked and not used

- A podcast recap claiming Google said it can predict conversion "with 90% certainty" from early signals (https://jyll.ca/insidegoogleads/121). Single secondary source, no primary confirmation.
- A practitioner claim that Performance Max "does not let you tie a single lead to a single placement". Plausible, but not verified.

## Not verified (treated as hypotheses wherever they appear)

- Real availability and eligibility of journey-aware bidding, Leads in Google Ads and Business Agent for Leads beyond the pilots described.
- Whether Google Ads has B2B firmographic targeting (company size, industry) in Search or Performance Max.
- Whether a default, automated cost-per-qualified-lead view by search term, asset or channel exists. Manual segmentation by conversion action does exist (see above).
- Any B2B-specific results for AI Max.
