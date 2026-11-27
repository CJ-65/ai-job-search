# Hamburg & Berlin language screen

Product Manager / Product Owner roles in Hamburg and Berlin, each checked for whether the full job description asks for German at B1 or higher. Saved so later sessions can reuse it without re-scraping.

**Screened:** 27 November 2026. Postings change and expire, so re-check a role before applying.

## File

`hamburg_berlin_language_screen.csv` has one row per posting (50 rows):

| Column | Meaning |
|---|---|
| `id` | `p###` = row in the LinkedIn export (`postings_v2.csv` on the dashboard); `i##` = Indeed sample |
| `source`, `url` | Where the description was read |
| `german_status` | `english_ok`: no German requirement, or German only "a plus". `german_required`: B1 or higher stated, "fluent/confident/sehr gute Deutschkenntnisse", or a posting written entirely in German. `unresolved`: description not reachable or skipped (reason in `language_evidence`) |
| `language_evidence` | The posting's own words on language (short quote) |
| `years` | Years of PM/PO experience asked for |
| `domain_must` | Industry experience the posting requires; "(plus)" or "(soft)" marks a nice-to-have |
| `ai_own_work` … `backlog_agile` | 1 = the posting asks for it (coded for English-OK roles; German-required rows are only partly coded) |
| `fit`, `fit_note` | My read of fit against the master CV (`cv/main_product_manager.tex`): strong / partial / weak |

## Results

| | Resolved | English-OK | Share |
|---|---|---|---|
| Hamburg | 13 | 3 | 23% |
| Berlin | 22 | 14 | 64% |
| **Total** | **35** | **17** | **49%** |

15 more LinkedIn postings are unresolved (expired, blocked, or German-titled and skipped).

**Best fits (English-OK, `fit = strong`):** Tourlane (Agent Productivity), SWARCO (PO Traffic Domain), GLS/NXT (PO Locker.OS), Oldendorff (Data PM).

## Method and limits

- LinkedIn job pages cannot be scraped (Firecrawl rejects linkedin.com). Each LinkedIn posting was found again on the employer's careers page or a job aggregator through a Firecrawl search, then scraped. Matching was by company and title; the Mind Detect → lemon.markets match is probable, not confirmed.
- One person coded the postings by reading them. Treat counts as a structured reading, not a measurement.
- Firecrawl cost for this screen: about 70 credits (searches 2 credits each, scrapes 1 credit each).

## Coded descriptions (readiness report)

`descriptions_coded.csv` has 49 full job descriptions (Hamburg 17, Berlin 27, remote 5), each coded 0/1 on 21 competencies (stakeholder … okr_named). They come from the 18-posting Indeed sample, 18 language-screen rows, and 13 new Indeed postings. Columns `archetype` and `german` hold one reader's classification. This dataset feeds the "PM Market Readiness Report" artifact. Indeed lookups cost 0 Firecrawl credits.
