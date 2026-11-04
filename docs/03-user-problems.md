# 3. User problems, with the evidence behind each

*Grades (P / S / A) are defined in [sources.md](sources.md). "Confidence" is my confidence that the problem is **real and material for B2B lead-gen advertisers**, not that it is common. I have no data on prevalence.*

## Summary

| # | Problem | Strongest evidence | Confidence | Google's response so far |
|---|---|---|---|---|
| P1 | Optimising to form fills pulls in low-quality leads | Google's own guidance (P); practitioner reports (A) | Medium | Deeper-funnel goals, enhanced conversions, journey-aware bidding (beta) |
| P2 | Deep-funnel B2B signals are too sparse and too slow for bidding to learn from | Documented volume guidance and upload windows (P) | Medium-high on the structure; unknown prevalence | Journey-aware bidding (beta) uses earlier stages as extra signal |
| P3 | Hard to see lead *quality* by segment inside automated campaigns | Manual segmentation exists (P); reporting is built around conversions (P); a vendor claim about cost (S, unverified) | **Low-medium: needs validation** | Expanded reporting; new lead-stage views (pilot) |
| P4 | The plumbing is real work and keeps changing | Migration and setting changes (P) | Medium | Unified setting; diagnostics report; Data Manager |
| P5 | Expanding automation can send traffic to places the advertiser did not intend | Google's own guidance suggests turning off final URL expansion if ads land on irrelevant pages (P) | Low-medium | Brand controls, locations of interest, extra search-term reporting |
| P6 | "Qualified" means different things to marketing and sales, so the signal is inconsistent | My experience only | **Hypothesis: no source** | None found |

## P1. Optimising to form fills pulls in low-quality leads

- **What happens:** the bidding system optimises toward whatever the advertiser tells it counts as a conversion. If that is a form submission, anything that submits the form, human or not, looks like success.
- **Evidence, Google (P):** the Performance Max lead-gen guidance says "AI is only as good as the inputs it receives", recommends goals such as "Qualified Lead" or "Converted Lead", and says these access "enhanced protections against invalid lead activity". It also tells advertisers to add qualifying questions, reCAPTCHA and server-side validation, which places spam mitigation partly on the advertiser.
- **Evidence, practitioners (A):** several agencies and forum threads describe junk leads from automated campaigns when only form fills are tracked.
- **Counter-evidence (A):** one agency reports Performance Max generating qualified B2B leads at lower cost than non-brand Search. These accounts are vendors describing their own results.
- **Limits:** none of this tells me how *many* advertisers are affected. The agency sources have an interest in selling the fix.
- **Residual gap:** advertisers still have to notice the problem and prove it with their own CRM data.

## P2. Deep-funnel B2B signals are too sparse and too slow

- **Evidence (P):** Google suggests a bidding goal with "at least 15 conversions in the last 30 days" for value-based bidding. Offline conversions uploaded more than **90 days** after the last click are not imported, and for enhanced conversions for leads the limit is **63 days**.
- **Why it bites B2B:** a deal that qualifies or closes after that window cannot be tied back to the click that started it. Small accounts may also never reach the volume Google suggests for a closed-deal goal.
- **Google's response (P):** journey-aware bidding (beta) lets Target CPA campaigns learn from earlier-stage goals as extra signal.
- **Limits:** I do not know how often B2B accounts actually hit these limits. It depends on sales-cycle length and volume. Effect size of the beta is unpublished.
- **Residual gap:** an advertiser cannot easily see whether their own signal is *sufficient*, or how much of their pipeline falls outside the attribution window.

## P3. Hard to see lead quality by segment inside automated campaigns

- **What exists (P):** you can segment the "All conversions" column by conversion action, and the API exposes the same breakdown. Performance Max now has channel performance, search terms and richer asset reports. AI Max adds match-source columns and search-term headline/URL reporting.
- **What I could not verify:** a **default, automated** view of cost per *qualified* lead by search term, asset, landing page or channel, with a warning when the sample is too small to trust.
- **Vendor claim (S, unverified):** segmenting by conversion action splits the conversions column but blanks the cost column, forcing a manual join of two reports. If true, this is a real friction point. I treat it as something to test.
- **Counter-consideration (P):** Google cautions that average return by channel "doesn't tell the full story" because of marginal ROI. Any quality view must not invite crude decisions like "cut the channel with the worst average".
- **Residual gap, if it holds:** the data exists, but turning it into a trustworthy decision takes manual work and statistical care that most advertisers will not do.

## P4. The plumbing is real work and keeps changing

- **Evidence (P):** enhanced conversions for web and leads merging into one setting (April 2026); offline and enhanced-conversions-for-leads uploads moved to the Data Manager API and blocked in the Google Ads API from June 15, 2026; developer tokens with no recent requests were not allowlisted for legacy access.
- **Google's response (P):** an enhanced conversions diagnostics report and an implementation checklist.
- **Residual gap:** moderate. A diagnostics report exists, so a new diagnostic must clear a higher bar.

## P5. Expanding automation can reach places the advertiser did not intend

- **Evidence (P):** Google's own Performance Max guidance says that if ads show on irrelevant pages of your own site, consider turning off final URL expansion. AI Max includes brand controls and locations of interest to give back some of the precision keywords provided.
- **Limits:** Google reports average uplifts for AI Max (14% in 2025, 7% in a 2026 subset) but they are not B2B-specific, and I found no independent B2B results.
- **Residual gap:** verifying that expansion helps *qualified* outcomes, not just conversions.

## P6. "Qualified" means different things to marketing and sales (hypothesis)

- **Source:** my own experience. I found nothing to cite, so this is **a hypothesis to test in interviews**, not a finding.
- **Why it matters if true:** the lens, journey-aware bidding and enhanced conversions all inherit the advertiser's definition. Inconsistent definitions would make every downstream metric unreliable.

## What I am not claiming

- That automation is bad for B2B, or that Google acts against advertisers. The sources show Google responding to the lead-quality problem with real products.
- That spam leads are common. The sources show the belief and some mechanisms, not prevalence.
- That any pilot feature is available to a given advertiser.

Next: [4. Opportunities and prioritization](04-opportunities-and-prioritization.md)
