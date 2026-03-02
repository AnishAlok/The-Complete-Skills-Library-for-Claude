# competitive-intelligence-report.md

> **Skill:** Produces a structured competitor deep-dive report that goes beyond surface-level feature comparison to analyze strategy, positioning, product direction, financials, talent signals, and vulnerability for a specific competitor.

---

## TLDR

This skill helps you answer: *"What is this specific competitor actually doing, where are they going, what are their weaknesses, and how should we respond?"* It produces a comprehensive competitive intelligence report on a single competitor covering product, positioning, strategy, financials, team, and vulnerability analysis. Used for strategic planning, product roadmap decisions, sales enablement, and board preparation when a specific competitor requires deep analysis rather than a landscape overview.

---

## Topic Explanation

### Competitive Intelligence Report vs. Competitive Landscape Map

These are two distinct documents that serve different purposes:

**Competitive landscape map** (`competitor-landscape-map.md`): A broad analysis of all competitors across the market. Multiple players plotted on shared dimensions. Used for market overview, positioning, and whitespace identification.

**Competitive intelligence report** (this skill): A deep dive on a single competitor. Used when one player requires close analysis because they are a primary threat, a frequent deal competitor, a potential acquisition target, or a bellwether for where the market is heading.

The landscape map is strategic breadth. The intelligence report is strategic depth.

### Intelligence Sources: Where to Look

Competitive intelligence is only as good as the sources it draws from. The best competitive intelligence triangulates across many source types, each of which reveals a different facet of the competitor:

**Public positioning sources**
- Company website, product pages, pricing page
- Blog content and thought leadership
- Case studies and customer stories
- Job descriptions (reveal strategic priorities and capability gaps)
- Press releases and news coverage
- Conference talks and webinar recordings

**Customer voice sources**
- G2, Capterra, Trustpilot, and App Store reviews
- Reddit, Slack communities, Twitter/X discussions
- Social media comments and complaints
- Analyst reports that include customer feedback

**Financial and growth signals**
- Crunchbase/PitchBook funding history
- LinkedIn headcount trends (growth rate signals revenue trajectory)
- Glassdoor reviews (culture and leadership signals)
- SEC filings if public or pre-IPO
- Revenue estimates from Lattice, SimilarWeb, or industry analysts

**Product signals**
- Product changelog and release notes
- API documentation and developer resources
- Feature announcements and launch posts
- Customer community and support forums

**Talent and capability signals**
- Job postings (what are they hiring for?)
- LinkedIn job title distribution (what is the ratio of sales to engineers to CS?)
- Leadership hires (who are they bringing in and from where?)
- Key departures (who left and where did they go?)

**Sales and GTM signals**
- Pricing page structure and tier logic
- Sales decks and collateral that have been shared publicly
- Partner and integration announcements
- Event sponsorships and content marketing cadence

### The Intelligence Report Structure

A deep-dive competitive intelligence report covers seven analytical dimensions:

1. **Company overview:** Who they are, what they built, when, funding history, scale.
2. **Product analysis:** What they actually offer, how it works, where it is strong and weak.
3. **Positioning and messaging:** How they present themselves to the market and why.
4. **Customer reality:** What actual customers say versus what marketing claims.
5. **Strategy and direction signals:** Where they appear to be going based on available evidence.
6. **Financial and operational health:** Growth rate, burn, runway, and scale indicators.
7. **Vulnerability analysis:** Where they are weak and where you can win against them.

### The Vulnerability Framework

The most actionable section of any competitive intelligence report is the vulnerability analysis. Vulnerabilities exist in four categories:

**Product vulnerabilities:** Features missing, use cases underserved, technical limitations, quality issues identified in reviews.

**Market vulnerabilities:** Customer segments underserved, geographies not covered, buyer types ignored, pricing model that excludes certain segments.

**Operational vulnerabilities:** Support quality issues, onboarding friction, implementation complexity, talent gaps.

**Strategic vulnerabilities:** Overextension across too many segments, over-reliance on a single channel, cultural or leadership issues signaled by Glassdoor data or public reports.

---

## When to Use This Skill

Use when:
- A competitor is winning deals you are losing and you need to understand why
- A well-funded competitor has just launched or raised and needs urgent analysis
- Preparing a sales battlecard for a specific competitor and needing the deep analysis to build from
- A board or investor asks for a detailed view of your most dangerous competitor
- Evaluating an acquisition target and needing to understand their competitive position and health
- A competitor appears to be moving into your core customer segment and you need to assess the threat
- Quarterly competitive review process for a specific tier-1 competitor

Do NOT use when:
- You need a broad view of all competitors (use `competitor-landscape-map.md`)
- You need a quick sales-ready battlecard (use `competitive-battlecard.md`, which uses this report as input)
- You need market sizing (use `market-opportunity-analysis.md`)

---

## Dos

- **Do triangulate every significant claim across at least two independent sources.** A single source for a competitive claim is fragile. Two independent sources pointing the same way is a finding.
- **Do date every piece of information.** Competitive intelligence goes stale fast. Every data point must carry the date it was sourced.
- **Do separate observation from interpretation.** "Competitor X posted 12 engineering job listings in Q1" is an observation. "Competitor X appears to be accelerating product development" is an interpretation. Both are valuable. Label them clearly.
- **Do read the negative reviews, not just the positive ones.** The most strategically valuable customer intelligence is in the 1-star and 2-star reviews, not the 5-star ones.
- **Do analyze job postings systematically.** What a company is hiring for reveals their strategic priorities 6 to 12 months before they announce them publicly.
- **Do compare their messaging to their reviews.** Where marketing claims diverge from customer experience is where the vulnerability lives.
- **Do track headcount growth as a revenue proxy.** Without public financials, LinkedIn headcount growth rate is the best available proxy for revenue trajectory.
- **Do assess the leadership team.** Founder-led vs. professional management, recent key hires and departures, and the experience profile of the leadership team all signal strategic direction and execution capability.

---

## Donts

- **Dont include unverified claims without flagging them as unverified.** Rumors, anonymous forum posts, and single-source claims should be labeled as low-confidence findings.
- **Dont confuse their marketing positioning with their actual product.** What a company says on its website is designed to be compelling, not accurate. Customer reviews are closer to reality.
- **Dont produce a feature comparison table as the primary output.** Feature tables are the least useful part of competitive intelligence. Vulnerability analysis and strategic direction are far more actionable.
- **Dont let the report become stale.** A competitive intelligence report more than 6 months old on a high-velocity competitor may be actively misleading. Note the date and flag for refresh.
- **Dont make vulnerability claims you cannot support with evidence.** Every vulnerability identified should have at least one piece of evidence: a customer review, a missing feature, a job posting pattern, or a strategic inconsistency.
- **Dont limit analysis to their current product.** The most important competitive intelligence is directional: where are they going? What capabilities are they building? What customer segments are they expanding into?
- **Dont ignore the human intelligence layer.** Talk to customers who evaluated and chose the competitor. Talk to customers who left the competitor. Talk to former competitor employees who are now public on LinkedIn. These sources are worth more than any public document.
- **Dont present this report directly to customers or prospects.** Competitive intelligence reports contain your internal analysis and strategic thinking. They are internal documents that inform battlecards, not external documents for customer consumption.

---

## Ideal Inputs

### Required
```
1. THE COMPETITOR TO ANALYZE
   Company name and a brief description of what they offer.

2. WHY THIS COMPETITOR IS BEING ANALYZED NOW
   What triggered this report? A funding raise? Losing deals to them?
   Board request? Quarterly review?
   The purpose shapes which dimensions require the most depth.

3. YOUR PRODUCT AND MARKET CONTEXT
   What do you offer and who do you serve?
   This is needed to make the vulnerability analysis relevant to you specifically.

4. WHAT YOU ALREADY KNOW
   Prior knowledge about this competitor.
   Any prior intelligence work that this report builds on.

5. KEY QUESTIONS TO ANSWER
   The 3 to 5 specific questions this report most needs to address.
   Examples: "Why are we losing to them on price?" or
   "Are they moving upmarket to enterprise?" or
   "What is their actual product quality like vs. their marketing claims?"
```

### Optional but Valuable
```
6. DEAL INTELLIGENCE
   Any information from your sales team about what this competitor
   says or does in deals. What claims do they make? What discounts?
   What do customers who chose them say about why?

7. CUSTOMER INTELLIGENCE
   Any conversations with customers who evaluated this competitor
   or previously used their product.

8. PRIOR REPORTS
   Any previous competitive analysis on this company.
   What has changed since then?

9. PUBLIC FINANCIAL DATA
   Any available funding data, revenue estimates, or headcount data
   you already have access to.

10. ACCESS TO REVIEW PLATFORMS
    Confirmation of access to G2, Capterra, Glassdoor, and similar
    sources for customer and employee feedback.
```

### Example of a Strong Input Prompt
```
Competitor: Vanta (compliance automation SaaS)
Why now: Vanta just raised a $150M Series C at a $1.6B valuation and is
expanding its marketing aggressively in our target segment (fintech startups).
Our context: We are a compliance automation tool for fintech startups focused on
SOC 2 and ISO 27001, currently at $2.1M ARR. We are losing 40% of competitive
deals to Vanta based on brand recognition and integrations.
What we know: Vanta has strong brand, broad integrations, and good design.
Customers complain about price and customer support quality in reviews.
Key questions:
1. Is Vanta moving toward continuous monitoring or staying in audit-prep?
2. How do their actual customers rate support quality compared to their claims?
3. What customer segments are they underserving that we could own?
4. What are they hiring for right now and what does that signal?
5. Where specifically do customers choose us over them?
Deal intelligence: Our sales team reports Vanta offers 30 to 40% discounts
to close competitive deals. Customers say Vanta has more integrations but
our onboarding is faster.
```

---

## Output Format

```
1. REPORT HEADER
   Competitor name, report date, analyst name, version,
   classification (internal only), refresh date recommended.

2. EXECUTIVE SUMMARY (half page)
   The 5 most important findings about this competitor.
   The single most important strategic implication for your company.
   Overall threat level: Critical / High / Medium / Low with rationale.

3. COMPANY OVERVIEW
   Founded, founders, headquarters, funding history with amounts and investors,
   estimated current ARR or revenue range, headcount and growth rate,
   business model, stated mission and market category.

4. PRODUCT ANALYSIS
   Core product offering and how it works.
   Feature set: what they have, what they are known for, what is missing.
   Product quality assessment based on customer reviews and direct observation.
   Pricing model and tier structure with price points if available.
   Recent product launches and roadmap signals.

5. POSITIONING AND MESSAGING ANALYSIS
   Who they say they serve (stated ICP).
   Their stated value proposition and key messages.
   How their messaging has evolved over time (if trackable).
   Channels and content strategy.

6. CUSTOMER REALITY ANALYSIS
   What actual customers say: themes from review platforms with evidence.
   Most common praise themes (with example quotes, paraphrased).
   Most common complaint themes (with example quotes, paraphrased).
   Gap analysis: where marketing claims diverge from customer reality.
   Net sentiment: positive / mixed / negative with evidence.

7. STRATEGY AND DIRECTION SIGNALS
   Where they appear to be heading based on:
   - Job posting analysis (what are they hiring for?)
   - Recent product launches and feature announcements
   - Partnership and integration announcements
   - Leadership hires and their background
   - Investor statements and board composition signals
   - Conference talks and thought leadership themes
   Confidence level for each signal: High / Medium / Low.

8. FINANCIAL AND OPERATIONAL HEALTH
   Revenue estimate range with methodology.
   Headcount growth rate (LinkedIn analysis).
   Burn estimate if available.
   Glassdoor rating and key themes from employee reviews.
   Overall health assessment: Accelerating / Stable / Declining.

9. VULNERABILITY ANALYSIS
   Product vulnerabilities: specific gaps or quality issues with evidence.
   Market vulnerabilities: underserved segments, coverage gaps.
   Operational vulnerabilities: support, onboarding, implementation issues.
   Strategic vulnerabilities: overextension, channel concentration, cultural issues.
   For each vulnerability: the evidence and the opportunity it creates for you.

10. COMPETITIVE RESPONSE IMPLICATIONS
    Where you win against this competitor and why.
    Where you lose and what it would take to change that.
    The 3 to 5 most important actions to take based on this analysis.
    What to monitor going forward and how frequently.

11. SOURCES LOG
    All sources used with date of access and quality rating.
    Flagging any claims that are low-confidence or single-sourced.
```

---

## Starter Prompt

```
You are a competitive intelligence analyst helping me produce a deep-dive
competitive intelligence report on a specific competitor.

Competitor to analyze: [company name and brief description]
Why this report is needed now: [the trigger and purpose]
My product and market context: [what you offer and who you serve]
What I already know: [prior knowledge about this competitor]
Key questions to answer: [the 3 to 5 specific questions this report must address]
Deal intelligence: [what your sales team knows from competitive deals]
Customer intelligence: [conversations with customers who evaluated this competitor]
Access available: [G2, Capterra, Glassdoor, LinkedIn, Crunchbase, etc.]

Please produce a complete competitive intelligence report including:
1. Executive summary with threat level rating
2. Company overview with funding and scale data
3. Product analysis including feature set, quality assessment, and pricing
4. Positioning and messaging analysis with gap between claims and reality
5. Customer reality analysis using review platform data with paraphrased evidence
6. Strategy and direction signals from job postings, launches, and leadership moves
7. Financial and operational health assessment
8. Vulnerability analysis across product, market, operational, and strategic dimensions
9. Competitive response implications: where we win, where we lose, what to do
10. Full sources log with date and confidence rating

Separate observations from interpretations throughout.
Date every data point.
Flag any claim that is low-confidence or single-sourced.
Be direct: if this competitor is a serious threat in a specific dimension, say so clearly.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `competitive-battlecard.md` | Convert vulnerability analysis into a sales-ready battlecard |
| `competitor-landscape-map.md` | Place this competitor within the broader competitive landscape |
| `positioning-doc.md` | Use vulnerability gaps to sharpen your own positioning |
| `win-loss-analysis.md` | Validate competitive intelligence findings with real deal data |
| `product-roadmap.md` | Use competitor direction signals to inform roadmap priorities |

| Use This Before | Why |
|---|---|
| `competitive-battlecard.md` | The battlecard draws from the deep-dive report |
| `strategic-planning-doc.md` | Deep competitive analysis feeds the market context section |

---

## Intelligence Source Quality Reference

| Source | Signal Type | Freshness | Reliability |
|---|---|---|---|
| G2 and Capterra reviews | Customer reality | High | Medium (self-selected) |
| Job postings | Strategic direction | Very High | High |
| LinkedIn headcount | Growth signal | High | Medium |
| Glassdoor reviews | Culture and operations | High | Medium |
| Press releases | Positioning | High | Low (self-reported) |
| Funding announcements | Scale and trajectory | Medium | High |
| Conference talks | Strategy and vision | Medium | High |
| Former employee LinkedIn | Capability signals | Medium | Variable |
| Customer interviews | Reality check | Depends on recency | Very High |
| API and developer docs | Product capability | High | High |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
