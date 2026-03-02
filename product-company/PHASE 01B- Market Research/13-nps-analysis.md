# nps-analysis.md

> **Skill:** Designs NPS survey programs, interprets score results, segments responses by driver and cohort, closes the loop with detractors and passives, and produces actionable reports that connect NPS data to specific product and CS improvements.

---

## TLDR

This skill helps you answer: *"How do our customers actually feel about us, why do they feel that way, and what do we do about it?"* It produces a complete NPS program design including survey structure, timing, follow-up protocols, driver analysis, cohort segmentation, and reporting format. Used by customer success, product, and leadership teams to measure satisfaction, identify risk, surface product feedback, and demonstrate customer health to investors.

---

## Topic Explanation

### What Is NPS?

Net Promoter Score (NPS) was developed by Fred Reichheld of Bain and Company and introduced in his 2003 Harvard Business Review article "The One Number You Need to Grow." It has since become the most widely used customer satisfaction metric in business.

The NPS question: "On a scale of 0 to 10, how likely are you to recommend [company] to a colleague or friend?"

Respondents are grouped:
- **Promoters (9 to 10):** Loyal enthusiasts who will refer others and fuel growth.
- **Passives (7 to 8):** Satisfied but not enthusiastic. Vulnerable to competitive offers.
- **Detractors (0 to 6):** Unhappy customers who can damage brand and generate churn.

**NPS = % Promoters minus % Detractors**

Score interpretation:
- Above 70: World class (Apple, Nordstrom territory)
- 50 to 70: Excellent
- 30 to 50: Good
- 0 to 30: Acceptable, room for improvement
- Below 0: Urgent attention needed

NPS ranges vary by industry. A score of 40 in enterprise B2B SaaS is excellent. A score of 40 in consumer e-commerce is below average. Always benchmark against your specific industry.

### Why NPS Alone Is Not Enough

A single NPS number tells you the outcome (customer sentiment) but not the cause (why they feel that way). An NPS program without driver analysis and close-the-loop protocols produces a vanity metric, not actionable insight.

A complete NPS program has four components:

**1. Score measurement:** The 0 to 10 rating question.
**2. Driver analysis:** An open-text follow-up ("What is the primary reason for your score?") that reveals why customers gave the score they did.
**3. Close the loop:** Personal follow-up with detractors and passives within 48 hours to address issues, demonstrate responsiveness, and convert at-risk customers.
**4. Pattern analysis:** Systematic coding of open-text responses across all respondents to identify the most common drivers of promoter, passive, and detractor scores.

### NPS Program Types

**Relational NPS:** Sent to the full customer base on a scheduled cadence (quarterly or annually). Measures overall relationship health. Good for tracking trend and benchmarking.

**Transactional NPS:** Sent after a specific interaction (support ticket close, onboarding completion, feature launch, renewal). Measures satisfaction with that specific moment. Good for identifying which touchpoints are creating promoters vs. detractors.

**In-product NPS:** Triggered within the product based on usage events. Measures satisfaction in context. Good for capturing sentiment while it is fresh.

Most mature NPS programs use a combination. For early-stage companies, a quarterly relational NPS with close-the-loop protocols is the right starting point.

### Statistical Validity Considerations

NPS is only statistically meaningful at sufficient sample sizes. A rough guide:

- Under 30 responses: Directional only. Do not report as a precise score.
- 30 to 100 responses: Usable but confidence interval is wide (approximately ±15 points).
- 100 to 300 responses: Good reliability (confidence interval approximately ±7 points).
- Over 300 responses: High reliability (confidence interval approximately ±3 to 5 points).

For small customer bases, report NPS as a range with the confidence interval rather than as a single precise number. Trend is more meaningful than point-in-time score for small samples.

### The Follow-Up Question Is More Important Than the Score

Many companies focus on the NPS score and treat the open-text follow-up as optional. This inverts the value equation. The score tells you the outcome. The follow-up tells you the cause.

Best practices for the follow-up question:
- Ask separately from the rating (do not combine into one question)
- Keep it open-ended: "What is the primary reason for your score?"
- Do not ask separate questions for promoters vs. detractors at survey time. Segment the analysis afterwards.
- Code responses systematically after collection using a consistent taxonomy

---

## When to Use This Skill

Use when:
- Launching or redesigning an NPS program for a SaaS or subscription business
- NPS scores have declined and the team needs to understand why
- Preparing investor or board materials that reference customer satisfaction
- A product launch or pricing change may have affected customer sentiment
- Customer health scores are not correlating with churn and you want to test whether NPS is predictive
- You want to identify at-risk accounts before they churn using NPS signals

Do NOT use when:
- Your customer base is under 50 accounts (NPS is not statistically useful at small scale; use interviews instead)
- You want to understand individual customer needs in depth (NPS is aggregate; use `customer-discovery-interview.md`)
- The primary goal is feature feedback (use a targeted feedback survey or `survey-design.md`)
- You need post-purchase satisfaction measurement for a one-time transaction product

---

## Dos

- **Do ask the follow-up open text question every time.** Without the reason, the score is a number with no actionability.
- **Do close the loop with detractors within 48 hours.** Speed of follow-up is the single most impactful variable in converting detractors. Waiting a week makes the follow-up feel perfunctory.
- **Do segment your NPS by cohort.** Overall NPS conceals important variation. Segment by customer segment, tenure, ACV, plan type, and feature usage. Patterns in the segments are where the insight lives.
- **Do track NPS trend over time, not just the current number.** A score of 42 is meaningless without context. Is it up from 31 last quarter or down from 54?
- **Do code open-text responses into a consistent taxonomy.** Uncoded open text is data you cannot act on. Code every response to a category (product gap / support quality / value realization / onboarding / pricing / etc.).
- **Do send NPS surveys from a named person, not from a company email.** Response rates improve significantly with personal sender attribution.
- **Do use NPS as an early churn warning system.** A detractor who has not yet churned is a churn risk. Build an at-risk workflow triggered by detractor scores that connects to the CS team within 24 hours.
- **Do benchmark against your industry.** NPS scores mean different things in different categories. Always contextualize your score against industry benchmarks.
- **Do make the survey short.** The NPS question plus the open-text follow-up is the complete survey for most purposes. Adding 8 more questions destroys completion rates.

---

## Donts

- **Dont report NPS as a precise number with small sample sizes.** With 40 respondents, your NPS has a confidence interval of about ±15 points. Report "approximately 38, based on 40 responses" not "our NPS is 38."
- **Dont send NPS surveys more than quarterly for relational measurement.** Survey fatigue is real. Over-surveying reduces response rates and makes the data less representative.
- **Dont ignore passives.** Passives (7 to 8) are often forgotten in NPS programs because they neither harm nor help the score. But they are the most convertible group and the most vulnerable to competitive offers. Engaging passives is often higher ROI than focusing only on detractors.
- **Dont treat NPS as a customer success metric alone.** NPS is a product metric, a support metric, a sales metric, and a leadership metric. The drivers of NPS touch every team. Own it cross-functionally.
- **Dont let NPS become a metric that gets gamed.** If reps cherry-pick which customers to send surveys to, or if customers are coached on responses, the data loses all value. Standardize who receives surveys and ensure it is not selectable by account owners.
- **Dont skip the driver analysis because it is qualitative.** Coding open-text responses takes effort. It is also the most valuable part of the program. A systematic driver taxonomy turns qualitative responses into quantitative patterns.
- **Dont compare your NPS to companies in different industries.** NPS benchmarks are highly industry-specific. A consumer app and an enterprise SaaS tool will have structurally different NPS scores reflecting different relationship dynamics.

---

## Ideal Inputs

### Required
```
1. YOUR CUSTOMER BASE SIZE AND COMPOSITION
   How many customers?
   What segments (by size, industry, plan, tenure)?
   This determines sampling approach and statistical validity.

2. NPS PROGRAM TYPE
   Relational (periodic to full base) or transactional (event-triggered)?
   Or in-product? Or a combination?

3. CURRENT NPS DATA (if analyzing existing results)
   Raw score distribution (count of each rating 0 to 10).
   Open-text responses if available.
   Any prior NPS scores for trend comparison.

4. KEY QUESTION TO ANSWER
   Is this about designing the program? Analyzing existing results?
   Understanding why scores are high or low?
   Identifying at-risk accounts?

5. WHAT ACTIONS WILL FOLLOW
   What will you do with the findings?
   Who will close the loop with detractors?
   What product or CS decisions will the analysis inform?
```

### Optional but Valuable
```
6. EXISTING SEGMENTATION DATA
   Can NPS responses be linked to customer firmographic or
   behavioral data in your CRM or product analytics?
   This enables cohort analysis.

7. PRIOR NPS PROGRAM DETAILS
   How was the survey sent? What was the response rate?
   Were there any methodology changes between surveys?

8. CHURN DATA
   Does NPS score correlate with churn in your data?
   What is the churn rate of detractors vs. promoters?

9. INDUSTRY BENCHMARK DATA
   Any NPS benchmark data for your specific industry or
   company stage for comparison.

10. DISTRIBUTION METHOD AND TIMING
    How will you distribute the survey?
    What email sender, what send time, what follow-up cadence?
```

### Example of a Strong Input Prompt
```
Customer base: 85 B2B SaaS customers using restaurant payroll software.
Mix: 60 independent restaurants, 15 small chains (2 to 5 locations),
10 food service companies. ACV range $2,400 to $24,000.
Program type: Quarterly relational NPS to full customer base.
Current NPS data (Q1 results): 52 responses out of 85 sent.
Score distribution: 6 detractors (0 to 6), 18 passives (7 to 8),
28 promoters (9 to 10). Raw NPS = (28/52 - 6/52) x 100 = 42.
Open-text themes (rough): Promoters mention "saves time on compliance."
Detractors mention "customer support slow" and "missing integrations."
Key question: Why are we at 42 and what would get us to 55+?
Actions to follow: CS team will contact detractors within 48 hours.
Product team will use driver data for Q2 roadmap prioritization.
Prior NPS: Q4 was 38 (improved 4 points).
Churn correlation: 4 of our 6 detractors from Q4 churned within 90 days.
Industry benchmark: B2B SaaS average NPS is approximately 30 to 40.
```

---

## Output Format

```
1. NPS PROGRAM DESIGN (if designing from scratch)
   Survey structure: rating question, follow-up question, optional segmentation questions.
   Distribution method and sender attribution.
   Timing: relational cadence or transactional trigger conditions.
   Sample size requirements and statistical validity thresholds.
   Close-the-loop workflow: who contacts whom, within what timeframe, using what script.

2. SCORE ANALYSIS
   Calculation: promoter %, detractor %, NPS score.
   Confidence interval given sample size.
   Trend vs. prior periods.
   Benchmark comparison with industry context.

3. COHORT SEGMENTATION
   NPS broken down by: customer segment, plan/ACV tier, tenure cohort,
   feature usage group, and any other available dimensions.
   Which cohorts are above and below overall NPS.
   Statistical significance note for small cohort samples.

4. DRIVER ANALYSIS
   Open-text responses coded to a consistent taxonomy.
   Driver frequency table: how often each driver is mentioned by each score group.
   Top 3 drivers for promoters.
   Top 3 drivers for detractors.
   Top 3 themes for passives.

5. PRIORITY MATRIX
   Each driver plotted on: frequency (how often mentioned) vs.
   impact on score (correlation between driver and 9-10 vs. 0-6 response).
   High frequency + high impact = urgent action items.

6. CLOSE-THE-LOOP PROTOCOL
   Detractor follow-up script (within 48 hours).
   Passive outreach script (within 1 week).
   Promoter ask script: referral, case study, or review request.

7. FINDINGS SUMMARY FOR LEADERSHIP
   NPS score, trend, and benchmark context.
   Top 3 things driving the score up.
   Top 3 things driving the score down.
   The 3 to 5 most important actions to take.
   Predicted NPS impact of each recommended action.

8. TRACKING AND REPORTING TEMPLATE
   Dashboard design: score over time, cohort breakdown, driver trend.
   Frequency of reporting and audience.
   How NPS data connects to churn risk workflow.
```

---

## Starter Prompt

```
You are an NPS analytics specialist helping me design, analyze, and act on
a Net Promoter Score program.

Customer base and composition: [number of customers and key segments]
NPS program type: [relational / transactional / in-product / combination]
Current NPS data: [score distribution if available, open-text response themes]
Key question: [program design / score analysis / driver identification / at-risk detection]
Prior NPS scores: [trend data if available]
Churn correlation: [any data on NPS vs. churn relationship]
Industry benchmark: [any benchmark data available]
Who will close the loop: [which team, what resourcing, what timeline]
What decisions this will inform: [product roadmap / CS motion / board narrative]

Please produce:
1. NPS survey design with rating question, follow-up question, and optional additions
2. Score calculation and confidence interval given sample size
3. Cohort segmentation analysis breaking down NPS by key customer dimensions
4. Open-text driver analysis with coded taxonomy and frequency table
5. A priority matrix mapping drivers by frequency and score impact
6. Close-the-loop scripts for detractors, passives, and promoters
7. A leadership summary report format
8. A dashboard and tracking template for ongoing program management

Flag any sample size limitations that affect the reliability of findings.
Note where industry benchmarks make the score look different in context.
Connect detractor themes directly to specific product or CS actions.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `churn-interview.md` | Use NPS detractor signals to trigger deeper churn-risk exit interviews |
| `voice-of-customer.md` | NPS open-text is a key input to the broader VoC data program |
| `customer-health-score.md` | NPS score is often a component of customer health scoring |
| `research-repository.md` | Store and tag NPS driver themes for ongoing retrieval |
| `product-roadmap.md` | NPS driver analysis feeds product gap prioritization |

| Use This Before | Why |
|---|---|
| `survey-design.md` | For deeper satisfaction measurement beyond NPS |
| `customer-discovery-interview.md` | NPS driver themes surface hypotheses for deeper qualitative exploration |

---

## NPS Industry Benchmark Reference

| Industry | Average NPS | Good NPS | Excellent NPS |
|---|---|---|---|
| B2B SaaS (overall) | 30 to 40 | 45 to 55 | 60+ |
| Professional services | 40 to 50 | 55 to 65 | 70+ |
| Consumer software / apps | 25 to 40 | 45 to 55 | 65+ |
| E-commerce | 45 to 55 | 60 to 70 | 75+ |
| Financial services | 30 to 40 | 45 to 55 | 65+ |
| Healthcare technology | 30 to 45 | 50 to 60 | 70+ |

*Benchmarks are approximate and vary by data source and year. Always use the most recent industry-specific data available.*

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
