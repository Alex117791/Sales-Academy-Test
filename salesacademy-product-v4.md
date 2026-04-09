# Sales Academy — Product Context Corrections & Enrichment File
## LLM Steering Document for Product JSON Build

**Version:** 4.0 — Updated April 8, 2026
**Purpose:** Correct known errors and enrich the Sales Academy product JSON so that downstream report generation accurately represents what Sales Academy does, who it serves, and what outcomes it delivers.

---

## ⚠️ CRITICAL INSTRUCTION

This file exists because the AI-scraped JSON for Sales Academy contains known factual errors and missing data. **If any value in this document conflicts with a value in the JSON, use this document's value without exception.**

---

## 🔴 MANDATORY CORRECTIONS

| Error in JSON | Correct Value | Why |
|---|---|---|
| "Secured a $200M exit" or "$200M exit" | **$150M USD ($204M CAD) exit via Agilysys** | Verified by Agilysys press release, Betakit, Phocuswire. Roger Sholanki uses "$200M" informally in personal branding — this is rounded/marketing language, not the verified transaction price. |
| "Doubled Onboarding Speed" | **Reduced rep ramp time from 9 months to 5 months (44% improvement)** | The Sales Academy YouTube case study explicitly states this figure. 9→5 months is a 44% reduction. "Doubled" would require cutting to ≤4.5 months and is a marketing headline, not a verified outcome. |
| "$2.3M in lost productivity" | **"$2.3M in Annual Lost Revenues"** | The salesacademy.com homepage labels this stat "Annual Lost Revenues" — not lost productivity. "$240K in Lost Productivity" is a completely separate stat. The JSON conflates two distinct metrics. |
| 25% or 60% sales hire failure rate (inconsistent) | **60% of sales hires fail** (homepage stat); **25% higher turnover** (separate homepage stat) | These are two different statistics. 60% = failure rate of sales hires without structured process. 25% = higher turnover companies experience. Do not swap or conflate them. |
| 40% assigned to turnover | **40% = Longer Ramp Times** (separate homepage stat) | The JSON inverted the 25%/40% assignments. 25% = higher turnover. 40% = longer ramp times. |
| "$240K" labeled as "cost per bad hire" | **"$240K in Lost Productivity"** | This is the homepage's exact label. It is not a cost-per-hire figure. |

---

## 🚫 COMPETITIVE LANDSCAPE — REPLACE THE JSON ARRAY ENTIRELY

**The JSON `competitive_landscape` is unreliable.** Previous scrape runs contaminated it with GIS mapping tools (Google Maps, QGIS, ArcGIS, BatchGeo), LMS platforms (TalentLMS, 360Learning, Adobe Learning Manager), and unrelated "Sales Academy" branded products from Richardson Sales Performance and Huthwaite International.

**Use only this verified competitor list:**

- Sandler Training
- Winning by Design
- JB Sales
- The Brooks Group
- The Harris Consulting Group
- RAIN Group
- Klozers
- pclub.io

**Do not add to this list.** MEDDICC, Challenger Sale, and Miller Heiman are sales methodologies/frameworks — not competing businesses. Geographic mapping tools are not competitors under any circumstances.

---

## 🟡 DATA MISSING FROM THE JSON — ADD THESE

### Homepage Statistics (Complete Verified Set)

| Stat | Correct Label |
|------|--------------|
| 60% | Sales hires fail without a structured process |
| 25% | Higher turnover at companies without structured hiring |
| 40% | Longer ramp times without proper onboarding |
| $2.3M | Annual Lost Revenues tied to underperforming sales teams |
| $240K | Lost Productivity per underperforming hire |
| 6+ months | Time for a new hire to become fully productive without a system |

### Named Frameworks and Methodology

- **DNA-PRO** — Sales Academy's proprietary candidate evaluation framework. Letters stand for: **D**rive (internal motivation, cannot be trained), **N**ature (how they show up personally), **A**cumen (quality of questions, business curiosity), **P**erformance (track record anywhere, not just sales), **R**elevance (SaaS/industry fit), **O**pportunities (career trajectory signals). Must be named explicitly in any description of Sales Academy's recruiting service.
- **CustomerCentric Selling® (CCS)** — The named sales methodology Sean Anderson is certified in. Listed as a credential on salesacademy.com. This is the foundation of all Sales Academy training. Any description of the training service must reference CCS by name.
- **Psychometric Probability Scoring** — Sales Academy uses a structured assessment that outputs a numerical probability score for each candidate's likelihood of on-the-job success. Used "religiously in every hire" per the Book4Time case study.

### Missing Testimonials

The JSON captured only 2 of 4 testimonials from the salesacademy.com homepage. All four must be included:

1. **Roger Sholanki** — Founder & CEO, Book4Time: *"Sean and Sales Academy were really valuable to our valuation. They helped put a lot of disciplines in place. I think what Sean was doing in sales was one of the top things that attracted Serent Capital."*
2. **David Smith** — Former Director of Finance, Book4Time: Describes improvements to forecasting accuracy, faster reporting, and improved sales-to-finance communication.
3. **Todd Tyler** — Executive Board Chair, Book4Time: *"Sean built a repeatable, scalable sales engine at Book4Time. The process, training and accountability he put in place created a high-performing team and were a significant contributing factor to our successful exit."*
4. **Liam Surridge** — Former VP, SAP: General endorsement of Sean Anderson's delivery quality and customer-first approach.

### Solution Themes (Named Brand Language from Site)

Sales Academy frames its outcomes using six named themes. Include these in any brand nomenclature or positioning fields:
**Insightful, Selective, Reliable, Ready, Trusted, Driven**

---

## SALES ACADEMY — ENRICHED PRODUCT DESCRIPTION

Use this as the authoritative product description if the JSON's description is thin or inaccurate.

### What Sales Academy Does

Sales Academy is a **B2B SaaS sales system** — not a recruiter, not a training course, not a coaching platform in isolation. It installs a complete, end-to-end sales infrastructure for technical SaaS founders who are building or rebuilding their sales teams. The system covers three integrated components:

1. **Sales Recruiting** — Structured candidate evaluation using the DNA-PRO framework and psychometric probability scoring. Replaces gut-feel hiring with a data-driven process. Includes AI simulations and structured interviews to surface candidates with the right drive, business acumen, and industry fit before an offer is made.

2. **Sales Training** — CustomerCentric Selling® (CCS) certified training delivered in group and 1:1 formats. Core principle: lead with deep discovery before presenting any solution. Trains reps to quantify buyer pain in financial terms and co-build business cases with prospects. Uses AI-assisted practice on real sales calls with instant feedback.

3. **Sales Coaching** — Ongoing performance management including weekly call reviews, individual coaching sessions, pipeline inspection, mutual action plan installation, and explicit rep performance benchmarking. Includes guidance on when to cut underperforming reps quickly.

### Who Sales Academy Serves (Ideal Customer Profile)

- **Founder profile:** Technical B2B SaaS founders between $2M–$10M ARR who are currently founder-selling or have made 1–3 early sales hires that underperformed
- **Growth stage:** Pre-Series A, post-seed — companies that have proven product-market fit but lack a repeatable, scalable sales engine
- **Pain trigger:** Preparing for institutional investment (PE or VC growth round) and need to demonstrate predictable pipeline and consistent revenue growth
- **Industry:** Primarily enterprise SaaS — complex, consultative, multi-stakeholder sales with long cycles and ROI-driven buying decisions
- **Team size at engagement:** Typically 1–10 person sales teams; often founder + 1–3 early reps

### Key Differentiators

- **Full system, not point solution** — Sean Anderson installs recruiting + training + coaching as an integrated system, not a standalone workshop or recruiter placement
- **Founder-specific** — designed for the exact moment a founder needs to stop selling and build a team that can sell without them
- **Hospitality SaaS vertical expertise** — Sean ran sales at Book4Time, a hospitality/wellness SaaS company. He understands complex enterprise hotel software buyers (CIOs, VP Operations, Revenue Directors) and the relationship-driven, reputation-sensitive dynamics of the hospitality technology community
- **Network-enabled recruiting** — Sean's "Top Sales Jobs in SaaS" podcast and SAP/Crystal/Business Objects alumni network provides access to pre-vetted A-player candidates; he personally screens applicants before routing them to hiring founders
- **Investor-readiness focus** — the system is explicitly designed to install the forecast discipline, pipeline hygiene, and revenue predictability that institutional investors require for Series A diligence

---

## THE BOOK4TIME CASE STUDY — AUTHORITATIVE REFERENCE

> ⚠️ Use these figures. Do not use JSON values for this case study — they contain known errors.

### About Book4Time
- Hospitality SaaS company — spa and wellness operations management for major hotel chains (Forbes 5-Star properties in 100+ countries)
- Products: appointment booking, contactless intake, revenue and yield management for hotel spas and wellness facilities
- Raised growth capital from **Serent Capital**
- Acquired by **Agilysys** for **$150M USD ($204M CAD)** — all-cash transaction, August 2024
- Buyer profile: same enterprise hotel brands (Marriott, Hilton, Radisson-class) that represent the ICP for other hospitality SaaS companies

### The Pain Before Sales Academy
- Unpredictable sales forecasting — reps consistently missed commit dates
- Multiple failed sales hires (6+) — wasted millions in credit lines on reps who didn't perform
- Founder doing day-to-day sales operations — classic founder-selling ceiling
- No structured hiring process — relied on candidates' self-reported capabilities

### What Sales Academy Implemented
1. DNA-PRO framework + psychometric scoring for all new hires
2. CustomerCentric Selling® training (group sessions + individual coaching)
3. Weekly call reviews and pipeline inspection
4. Forecast discipline and rep performance benchmarks
5. Explicit underperformer cut criteria

### Verified Outcomes

| Metric | Verified Figure |
|--------|----------------|
| Exit valuation | $150M USD ($204M CAD) via Agilysys |
| Rep ramp time | 9 months → 5 months (44% reduction) |
| Revenue growth | $3M ARR → $25M ARR |
| CAGR | 27% over the growth period |
| Mis-hire reduction | Cut by over 50% |
| Investor attribution | Sean's work cited as "one of the top things that attracted Serent Capital" — Roger Sholanki |

### Why This Case Study Matters for Report Generation
Book4Time is a **hospitality SaaS company** serving enterprise hotel brands with complex, ROI-driven software. Its buyer profile — senior hotel operations and technology leaders at major international chains — is identical to the ICP of other hospitality SaaS vendors. The case study demonstrates Sales Academy's capability in exactly this vertical: long-cycle enterprise deals, consultative discovery, multi-stakeholder buying committees, and a tight-knit industry community where reputation compounds. Any company in the hospitality technology space selling to the same hotel brands would be a natural fit for the Sales Academy system.

---

## SEAN ANDERSON — FOUNDER BACKGROUND

- **Career:** VP Sales at SAP (mid-market) → VP Sales at Book4Time → Founder, Sales Academy
- **Certification:** CustomerCentric Selling® (CCS) — listed on salesacademy.com
- **Network:** Deep SAP/Crystal/Business Objects alumni network — former colleagues now CROs and CEOs at Traction Complete, Toon Boom Animation, Docebo, NetSuite
- **Podcast:** "Top Sales Jobs in SaaS" — interviews CROs, VPs of Sales, and founders; doubles as a candidate pre-screening and routing platform
- **Approach:** Asks 100+ deep discovery questions before ever presenting a solution — mirrors the CustomerCentric Selling® methodology he teaches
- **Vertical expertise:** Direct experience selling enterprise hospitality SaaS at Book4Time — understands hotel brand buyer dynamics, post-COVID SaaS adoption patterns, and the reputation-driven nature of the hospitality tech community

---

## 🚫 URL BLOCKLIST — NEVER SCRAPE THESE

| URL | Why It's Dangerous |
|-----|--------------------|
| `elearningindustry.com` (any page) | Lists 30+ LMS platforms — causes TalentLMS, Adobe Learning Manager, 360Learning etc. to appear as Sales Academy competitors |
| `asherstrategies.com/the-best-sales-training-programs-compared/` | Contains a sales territory mapping tools section — caused Google Maps, QGIS, ArcGIS, BatchGeo to appear as competitors |
| `pclub.io/blog/best-training-for-sales-team` | Generic training listicle — pollutes competitor list |
| `proprofstraining.com/blog/best-sales-training-courses/` | Generic e-learning listicle — wrong category |
| `richardson.com/sales-training-delivery/sales-academy` | Richardson Sales Performance's own "Sales Academy" product — a direct competitor, not the same company |
| `huthwaiteinternational.com/blog/sales-academy-approach` | Huthwaite International (SPIN Selling inventors) — competitor with their own Sales Academy branded product |
| `sellinginteractions.com/sales-training-or-sales-academy/` | Generic blog post — no value, introduces noise |
| `salesacademy.us` (any page) | Different company entirely — will merge unrelated content into the product profile |
| `salesacademy.ca` or `thesalesacademy.ca` | Different companies — same name collision risk |
| `cdn2.hubspot.net` Sales Academy PDF | 2020 brochure from unidentified third-party "Sales Academy" brand |
| `gartner.com` or `forrester.com` Sales Academy pages | Paywalled — scraper returns nothing or partial content; wrong category (software platforms vs. services) |

## ✅ SAFE URL LIST — USE ONLY THESE

| URL | Content |
|-----|---------|
| `https://www.salesacademy.com/` | Homepage — core positioning, stats, testimonials, features |
| `https://salesacademy.com/` | Non-www canonical variant — de-duplicate with above |
| `https://www.salesacademy.com/case-studies` | Case study outcomes and ROI metrics |
| `https://salesacademy.com/book4time-case-study` | Full Book4Time case study detail |
| `https://salesacademy.com/bio` | Sean Anderson background and credentials |

---

*Sources used to build this file: salesacademy.com, Agilysys press release (Aug 2024), Betakit, Phocuswire, Sales Academy YouTube case study transcript, Sean Anderson LinkedIn, "Top Sales Jobs in SaaS" podcast episode transcripts (Greg Swift/Toon Boom, Jamie Smithers/Traction Complete, Roger Sholanki/Book4Time), CB Insights RobosizeME profile, Oracle Hospitality Summit 2026 press release.*
