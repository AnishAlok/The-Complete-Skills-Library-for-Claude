# voice-of-customer.md

> **Skill:** Designs a systematic Voice of Customer (VoC) data collection program, synthesizes signals from multiple feedback channels into prioritized themes, and produces an integrated customer perspective that drives product, messaging, and strategy decisions.

---

## TLDR

This skill helps you answer: *"Across all the ways our customers talk to us and about us, what are they actually telling us, and what does it mean?"* It produces a VoC program design with source mapping, a collection protocol, a theme synthesis methodology, and a reporting format that integrates customer signals from interviews, surveys, support tickets, reviews, sales calls, and social channels into a unified, prioritized customer perspective. Used for product roadmap prioritization, messaging development, executive reporting, and customer-led strategy.

---

## Topic Explanation

### What Is Voice of Customer?

Voice of Customer (VoC) is a research methodology and business practice that captures customers' expectations, preferences, and aversions through multiple listening channels, and synthesizes them into an integrated, representative customer perspective that informs business decisions.

VoC differs from individual research methods in a critical way: it is a program, not a project. A customer discovery interview produces point-in-time insight. An NPS survey produces periodic satisfaction data. A VoC program integrates signals from all of these channels continuously and produces an always-current picture of what customers think, feel, need, and want.

### The VoC Signal Sources

A complete VoC program draws from multiple data streams, each of which captures a different dimension of customer perspective:

**Solicited feedback (customers responding to your request):**
- Customer interviews and focus groups
- NPS surveys and follow-up open text
- CSAT surveys after support interactions
- Product feedback surveys
- Win/loss interviews
- Churn exit interviews
- Customer advisory board discussions

**Unsolicited feedback (customers expressing themselves unprompted):**
- Support tickets and chat logs
- Review platform posts (G2, Capterra, Trustpilot, App Store)
- Social media mentions
- Community forum posts
- Sales call recordings and deal notes
- Customer success meeting notes and QBR summaries

**Observed behavior (what customers do, not what they say):**
- Product analytics and usage data
- Feature adoption rates
- Churn patterns and cohort analysis
- Search and help article traffic
- Onboarding completion rates

The synthesis challenge is that each source produces different signal types (qualitative vs. quantitative, solicited vs. unsolicited, attitudinal vs. behavioral) that must be weighted and integrated intelligently.

### The VoC Synthesis Hierarchy

Not all customer signals are equally valuable for every purpose. A practical weighting framework:

**For product decisions:** Weight unsolicited feedback (support tickets, reviews) and observed behavior (analytics, adoption) most heavily. These reveal real pain without social desirability bias.

**For messaging decisions:** Weight solicited attitudinal feedback (interviews, NPS open text) most heavily. These reveal how customers describe their needs and the language they use.

**For retention decisions:** Weight behavioral signals (usage decline, churn patterns) and transactional NPS most heavily. Behavioral data is the earliest and most reliable leading indicator.

**For positioning decisions:** Weight win/loss interviews, competitive review data, and sales call themes most heavily. These reveal how customers evaluate you relative to alternatives.

### The Difference Between Data Collection and Insight

The most common VoC failure is collecting data without synthesizing it. A company that has 300 support tickets, 80 NPS responses, and 15 G2 reviews has data. The insight is the cross-channel pattern that emerges when those signals are synthesized.

Synthesis involves three steps:

**1. Normalization:** Converting signals from different sources into a common format for comparison. A support ticket, a G2 review, and an interview quote all expressing frustration with onboarding are the same signal even though they arrived through different channels.

**2. Codification:** Assigning consistent tags to normalized signals so patterns can be identified quantitatively. "Onboarding too complex" as a code applied across all sources enables frequency counting and trend tracking.

**3. Pattern identification:** Finding the themes that appear consistently across multiple sources and multiple customers. A pattern that appears in interviews AND support tickets AND reviews is a high-confidence finding. A pattern that appears only in one source warrants investigation but not yet action.

---

## When to Use This Skill

Use when:
- Designing a systematic customer feedback program that integrates multiple channels
- Preparing a quarterly or annual customer perspective report for product and leadership
- Product teams are making roadmap decisions without a clear, integrated view of what customers need
- Customer signals from different teams (CS, sales, product) are not being shared or integrated
- You want to build a customer advisory board program or customer research repository
- Investor or board due diligence requires demonstration of a systematic VoC capability

Do NOT use when:
- You need a single focused research study rather than an ongoing program (use `primary-research-plan.md`)
- You need deep insight on a specific question (use `customer-discovery-interview.md`, `churn-interview.md`, or `win-loss-analysis.md`)
- The customer base is too small to produce meaningful aggregate patterns (fewer than 20 customers)

---

## Dos

- **Do map all existing signal sources before designing new ones.** Most companies already have more VoC data than they realize: support tickets, CS call notes, NPS responses, sales recordings. Start by cataloging what exists.
- **Do create a consistent tagging taxonomy before collection begins.** Tags applied inconsistently across sources produce data that cannot be compared. Establish the taxonomy first.
- **Do weight signals by source quality for different purposes.** Unsolicited feedback gets more weight for product prioritization. Solicited feedback gets more weight for messaging. Weight explicitly, not by gut.
- **Do bring in the voice of customers who are not talking to you.** Reviews, social mentions, and competitor reviews from your target customers are as important as direct feedback from your own base.
- **Do distinguish between frequency and importance.** The most frequently mentioned issue is not always the most strategically important one. A rare but severe pain point may matter more than a common but minor one.
- **Do close the feedback loop with customers who provide it.** Customers who see their feedback acted on become repeat contributors. Those who never see any response stop contributing.
- **Do share VoC findings cross-functionally.** VoC is most valuable when it reaches product, marketing, sales, and CS simultaneously. Siloed VoC data helps only the team that collected it.
- **Do review and update the taxonomy quarterly.** New themes emerge as the product and market evolve. A static taxonomy misses new signals.

---

## Donts

- **Dont build a VoC program that produces data no one reads.** Before designing collection, establish who will receive findings, how often, in what format, and what decisions they will make with them.
- **Dont treat all customer voices as equally representative.** Power users speak louder than occasional users. Churned customers represent a specific experience. New customers represent onboarding reality. Weight appropriately.
- **Dont confuse volume with importance.** The loudest customers (the ones who send 20 support tickets) represent themselves, not the customer base. Prolific feedback contributors should be identified and their signals normalized.
- **Dont let VoC become a sales tool.** Selectively amplifying positive signals to make the product look better is not VoC. It is PR. Real VoC requires equal weight to negative signals.
- **Dont aggregate away the nuance.** "Customers want better onboarding" is a finding that produces nothing. "Customers with 2 to 5 locations find the initial data import too complex and abandon before their first payroll run" is a finding that produces a product action.
- **Dont skip the behavioral signals.** What customers say and what customers do are often different. Usage data, completion rates, and feature adoption are as important as what customers say in interviews.
- **Dont run VoC without a cadence.** A one-time VoC synthesis is a snapshot. A quarterly or monthly VoC review is a system. The value compounds over time.

---

## Ideal Inputs

### Required
```
1. YOUR CURRENT FEEDBACK CHANNELS
   Which sources of customer feedback already exist?
   Which are active and which are dormant?
   Rough volume from each source.

2. THE PRIMARY DECISIONS VoC SHOULD INFORM
   Product roadmap? Positioning? Customer success motion?
   Knowing the downstream use determines which signals to weight most heavily.

3. THE CUSTOMER BASE
   How many customers? What segments?
   Are there customer types who are under-represented in current feedback?

4. CURRENT GAPS
   What do you not know about your customers that you need to know?
   What signals are you currently missing or not using?

5. TEAM CAPACITY
   Who will collect, tag, synthesize, and report on VoC data?
   How much time can they dedicate to it?
```

### Optional but Valuable
```
6. PRIOR VoC OR RESEARCH DATA
   Any existing synthesis documents, research reports, or customer feedback
   repositories that this program builds on.

7. PRODUCT STAGE AND ROADMAP CONTEXT
   Are you in active discovery mode (need generative VoC) or
   in optimization mode (need evaluative VoC)?

8. COMPETITIVE VoC INTEREST
   Is competitor customer voice (reviews of competitor products) in scope?

9. REPORTING AUDIENCE
   Who will receive VoC reports: the full company, leadership only, board?
   This affects depth, format, and frequency.

10. TOOLS AND INFRASTRUCTURE
    What tools are already in use?
    CRM, CS platform, product analytics, survey tool, research repository.
```

### Example of a Strong Input Prompt
```
Current feedback channels:
- Quarterly NPS (85 customers, avg 60% response rate, open text collected but uncoded)
- Support tickets (avg 40 per month, no tagging system)
- CS team notes from quarterly business reviews (10 to 15 enterprise customers only)
- G2 reviews (22 reviews, not systematically reviewed)
- Product team interviews (ad hoc, maybe 6 per quarter, no repository)
Primary decisions: Product roadmap prioritization for Q3 and Q4.
Secondary: Messaging refresh for Series A.
Customer base: 85 B2B SaaS customers, mix of SMB and mid-market restaurants.
Current gaps: We do not have a systematic view of what features are blocking
expansion. We do not use our NPS open text data effectively.
Team capacity: One CS analyst, half time. One PM, quarter time.
Reporting audience: Product team weekly. Leadership team monthly. Board quarterly.
Tools: HubSpot CRM, Intercom for support, Typeform for NPS, Notion for notes.
```

---

## Output Format

```
1. VoC PROGRAM DESIGN

   Source inventory:
   Catalog of all current feedback channels with volume, quality,
   and coverage assessment.

   Source gaps:
   Feedback channels that should exist but do not.
   Customer segments not currently represented in any source.

   Collection protocol:
   What to collect from each source.
   Who collects it, how often, in what format.
   How it enters the shared repository.

2. TAGGING TAXONOMY
   Hierarchical code structure: top-level themes and sub-codes.
   Example: Onboarding > Data import complexity.
   Definitions for each code to ensure consistent application.
   Instructions for tagging ambiguous signals.

3. WEIGHTING FRAMEWORK
   How signals from different sources are weighted for different decisions.
   Table: source vs. decision type with weighting (high / medium / low).

4. SYNTHESIS PROTOCOL
   Step-by-step process for each synthesis cycle:
   Collect and normalize, code, count and rank, pattern-identify, interpret.
   Cadence: weekly, monthly, quarterly synthesis checkpoints.

5. CROSS-CHANNEL THEME REPORT FORMAT
   For each identified theme:
   - Theme name and description
   - Frequency: how many signals, from how many sources, from how many customers
   - Source distribution: which channels surfaced this theme
   - Customer segment distribution: which customer types report this
   - Verbatim examples: 2 to 3 representative quotes or signal excerpts
   - Trend: new / growing / stable / declining
   - Strategic importance: High / Medium / Low
   - Recommended action

6. EXECUTIVE VoC REPORT FORMAT
   Monthly or quarterly summary for leadership:
   - Top 3 to 5 themes with frequency and importance rating
   - What is improving vs. what is getting worse
   - The most urgent customer need not yet addressed
   - Customer signal of the period (most representative verbatim)
   - Actions taken based on prior VoC report

7. CLOSE-THE-LOOP PROTOCOL
   How customers who provide feedback are informed of actions taken.
   What gets communicated, by whom, to which segment.

8. PROGRAM HEALTH METRICS
   Feedback volume per source per period.
   Response rates for solicited channels.
   Tag coverage rate (% of signals coded).
   Time from signal to synthesis to action.
   Customer awareness that feedback was acted on.
```

---

## Starter Prompt

```
You are a Voice of Customer program designer helping me build a systematic
customer feedback collection and synthesis program.

Current feedback channels: [list all active channels with volume]
Primary decisions VoC should inform: [product roadmap / positioning / CS motion]
Customer base: [size and segments]
Current gaps: [what you do not know that you need to know]
Team capacity: [who will run this and how much time they have]
Reporting audience: [who receives findings and how often]
Tools in use: [CRM, CS platform, analytics, survey tool]
Prior VoC data: [any existing synthesis or research]

Please produce:
1. A source inventory assessing all current feedback channels for quality and coverage
2. Identification of source gaps: channels missing and underrepresented customer types
3. A collection protocol for each source
4. A hierarchical tagging taxonomy with definitions for consistent coding
5. A weighting framework by source type and decision type
6. A synthesis protocol with step-by-step process and cadence
7. A cross-channel theme report template
8. An executive VoC report format for monthly or quarterly leadership sharing
9. A close-the-loop protocol
10. Program health metrics for tracking program effectiveness

Distinguish between solicited and unsolicited feedback throughout.
Flag any channel that is high volume but low quality.
Note where behavioral signals should supplement attitudinal signals.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `research-repository.md` | Build the repository infrastructure that stores VoC data |
| `nps-analysis.md` | NPS is one of the core solicited VoC channels |
| `churn-interview.md` | Churn interviews are a critical VoC input for retention insight |
| `product-roadmap.md` | VoC theme prioritization feeds roadmap decisions |
| `messaging-framework.md` | Customer language from VoC synthesis informs messaging |

| Use This Before | Why |
|---|---|
| `primary-research-plan.md` | VoC synthesis may reveal specific questions requiring deeper primary research |
| `customer-discovery-interview.md` | VoC patterns surface the most important hypotheses to explore in interviews |

---

## VoC Source Quality Reference

| Source | Signal Type | Bias Risk | Volume | Actionability |
|---|---|---|---|---|
| Customer interviews | Attitudinal and behavioral | Social desirability | Low | Very High |
| NPS open text | Attitudinal | Response bias | Medium | High |
| Support tickets | Behavioral proxy | Problem-skewed | High | High |
| G2 and review platforms | Attitudinal | Self-selected extreme views | Medium | High |
| Sales call recordings | Attitudinal and decision | Sales influence | Medium | High |
| QBR and CS notes | Attitudinal | Relationship-skewed | Low | High |
| Product analytics | Behavioral | None | Very High | Medium |
| Social media mentions | Attitudinal | Vocal minority | Variable | Medium |
| Community forums | Attitudinal | Power user skewed | Low | High |
| Onboarding completion data | Behavioral | None | High | High |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
