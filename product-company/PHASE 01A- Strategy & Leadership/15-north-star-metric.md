# north-star-metric.md

> **Skill:** Defines and documents a company's north star metric: the single metric that best captures the core value your product delivers to customers and predicts long-term business success.

---

## TLDR

This skill helps you answer: *"What is the one number that, if it grows, almost certainly means our customers are getting value and our business is healthy?"* It produces a fully documented north star metric definition including the metric itself, its rationale, its relationship to business outcomes, how it is measured, and the input metrics that drive it. Used for strategic alignment, product prioritization, team goal-setting, and investor communication.

---

## Topic Explanation

### What Is a North Star Metric?

The north star metric (NSM) is a concept popularized in the product and growth community, most prominently by Sean Ellis (who coined the term "growth hacking") and later developed by Amplitude in their work on product analytics. It refers to a single metric that:

1. Captures the core value your product delivers to customers
2. Is a leading indicator of long-term revenue and business health
3. Can be influenced by every team in the organization
4. Serves as the primary focus for product and growth decisions

The north star metric is not a vanity metric (pageviews, app downloads, registered users). It is not a revenue metric (ARR, MRR, revenue). And it is not a health metric (uptime, CSAT). It sits at the intersection of customer value and business outcome: if customers are getting value (captured by the NSM), revenue and growth follow as consequences.

### Why One Metric?

Most companies track dozens of metrics. The north star metric does not replace all others. It sits at the top of a hierarchy and provides strategic focus. When teams disagree on priorities, the question becomes: "Which option better advances the north star metric?" This resolves debates that would otherwise be political.

The discipline of choosing one metric also forces honesty. Teams that cannot agree on a single north star often have an underlying disagreement about what the product is fundamentally for. The process of finding the north star surfaces that disagreement so it can be resolved.

### Characteristics of a Good North Star Metric

**It measures value delivered to customers, not extracted from them.**
A north star that measures revenue first and customer value second will push product decisions toward monetization at the expense of value. The best NSMs measure something customers experience as valuable.

**It is a leading indicator of revenue, not revenue itself.**
Revenue is a lagging indicator. It tells you what happened. The NSM tells you what will happen. When the NSM grows, revenue should predictably follow. If they decouple, something is wrong.

**It is actionable.**
The team must be able to identify what they can do to improve it. A metric that cannot be influenced by product decisions is not a north star.

**It is understandable.**
Everyone in the organization should be able to explain what it measures and why it matters. A complex composite index that requires a data scientist to calculate is not a good north star.

**It is measurable consistently over time.**
The metric must be instrumentable, reproducible, and comparable period over period.

### The North Star Framework

The north star metric does not stand alone. It sits within a framework:

**Level 1: The North Star Metric**
The single metric that best captures core customer value delivery.

**Level 2: Input Metrics (Drivers)**
The 3 to 5 metrics that directly influence the north star. These are the levers teams pull.

**Level 3: Health Metrics**
The guardrail metrics that must stay within bounds while the team pursues the north star. These are not goals but floor/ceiling constraints. Examples: churn rate, support ticket volume, gross margin.

**Level 4: Project and Feature Metrics**
The specific metrics tied to individual experiments, features, or initiatives.

### North Star Metric Categories

Different types of businesses tend to have different categories of north star metric:

**Attention/engagement businesses** (social media, media, gaming):
Daily active users, time spent, sessions per user per week.
The core value is engagement. More time in product = more value delivered.

**Transaction businesses** (e-commerce, marketplaces, fintech):
Number of transactions completed, gross merchandise value, payment volume.
The core value is successfully completing a transaction.

**Productivity/SaaS businesses:**
Number of core actions completed, projects created, documents published,
workflow automations triggered.
The core value is work getting done more efficiently.

**Communication businesses:**
Messages sent, connections made, conversations initiated.
The core value is connection or communication happening.

**Growth/network businesses:**
Connected users, network nodes, relationships formed.
The core value is the network itself.

### Common North Star Metric Examples

| Company | North Star Metric | Why |
|---|---|---|
| Slack | Daily active users who send at least one message | Message sent = team is communicating, value is delivered |
| Airbnb | Nights booked | Booking completed = both sides got value |
| Spotify | Time spent listening | Listening time = user is enjoying the product |
| HubSpot | Weekly active teams | Team using it = customers extracting workflow value |
| Amplitude | Weekly queried charts | Chart queried = insight delivered to a user |
| Duolingo | Daily active users completing a lesson | Lesson completed = language learning is happening |

### North Star Metric vs. OKR Key Results

North star metrics and OKR key results are related but different:
- The north star metric is permanent (changes rarely, if ever)
- OKR key results change quarterly
- The north star metric is the target state
- OKR key results are the near-term progress markers on the way there

A company's quarterly OKRs should always be traceable to progress on the north star metric. If an OKR key result does not connect to the north star, ask whether it should exist.

---

## When to Use This Skill

Use when:
- A company does not yet have a defined north star metric and is operating with fragmented goals
- Teams are misaligned on what to prioritize because there is no shared success metric
- Product and growth teams are optimizing for different things (e.g., product optimizes for engagement, growth optimizes for acquisition) with no integration
- Preparing for a strategic planning cycle and needing to anchor OKRs to a core metric
- Communicating to investors or board what the company optimizes for
- Onboarding a new product leader who needs to understand what success looks like
- A product has evolved significantly and the original north star metric no longer reflects core value delivery

Do NOT use when:
- You need specific quarterly OKRs (use `okr-framework.md`)
- You need a full metrics framework with dashboards (use `metrics-dashboard-spec.md`)
- You need a tracking plan and event taxonomy (use `tracking-plan.md`)
- You need a specific A/B test design (use `ab-test-plan.md`)

---

## Dos

- **Do center the north star metric on customer value, not company extraction.** The metric should increase when customers get more value from your product, not just when you extract more money from them.
- **Do validate that the north star metric predicts revenue.** Run a correlation analysis if data is available. If NSM growth does not predict revenue growth over a meaningful period, it is the wrong metric.
- **Do make sure all teams can influence it.** If only the product team can move the north star, it is not a company-level metric. Engineering, design, marketing, sales, and CS should all be able to draw a line from their work to the north star.
- **Do define the metric precisely.** "Daily active users" is vague. "Unique users who complete at least one core workflow within a 24-hour period" is precise. Precise definitions prevent measurement disputes.
- **Do document the input metrics alongside the north star.** The north star tells you whether you are winning. The input metrics tell you what to do about it.
- **Do test the metric against the "proud to optimize for this" check.** Would you be comfortable telling customers, employees, and investors that this is the number you optimize for? If not, it may be the wrong metric or it may be measuring extraction rather than value.
- **Do review the north star metric annually.** As products evolve, the core value delivered can change. A metric that was right at $1M ARR may be wrong at $20M ARR.
- **Do communicate the why, not just the what.** A north star metric without an explanation of why it captures customer value will not drive alignment. Every team member should be able to explain the connection between their work and the north star in one sentence.

---

## Donts

- **Dont choose a revenue metric as the north star.** Revenue is the output. The north star is the input that drives revenue. Choosing MRR or ARR as the north star encourages short-term extraction over long-term value creation.
- **Dont choose a vanity metric.** Downloads, signups, and page views look good in press releases but do not capture whether customers are getting value. A user who downloads and never uses the product has not received value.
- **Dont try to have more than one north star metric.** Multiple north star metrics are no north star at all. They recreate the alignment problem. If you have two competing candidates, pick one and put the other in the input metric layer.
- **Dont choose a metric the team cannot influence.** A metric driven entirely by external factors (macro economy, seasonal patterns) or by a single team does not serve as an organizational aligning force.
- **Dont confuse a health metric with a north star metric.** Churn rate, CSAT, and uptime are important health metrics (guardrails). They are not north star candidates because they measure the absence of failure, not the presence of value.
- **Dont set the north star and then measure it only quarterly.** A metric you review quarterly cannot drive daily and weekly product decisions. North star metrics must be tracked and visible in real time.
- **Dont accept "engagement" as a precise enough definition.** "Engagement" is a category, not a metric. Be specific: what action, how often, by whom, constitutes engagement in your product?
- **Dont skip the input metric layer.** A north star without input metrics is a destination without directions. The input metrics are the operational levers that teams use to drive the north star.

---

## Ideal Inputs

### Required
```
1. PRODUCT DESCRIPTION
   What does your product do? What is the core workflow or action
   your best customers take?

2. THE CORE VALUE DELIVERED
   When a customer says "this product changed how I work,"
   what specifically changed? What did they do before your product
   and what do they do now?

3. YOUR BEST CUSTOMER BEHAVIOR
   What does a highly engaged, high-value customer do in your product
   that a churned or low-value customer did not do?
   What actions correlate with retention and expansion?

4. CURRENT METRICS YOU TRACK
   What metrics does the company currently track?
   Which ones are most discussed in leadership?

5. BUSINESS MODEL
   How do you make money? Subscription, usage-based, transaction fee,
   freemium-to-paid? This constrains which metrics can serve as north star.
```

### Optional but Valuable
```
6. RETENTION AND ENGAGEMENT DATA
   What actions or behaviors predict long-term retention in your product?
   Any analysis of what differentiates retained vs. churned users?

7. COHORT ANALYSIS
   Do you know which cohorts retain well and why?
   What did high-retention cohorts do in their first 30 days?

8. CUSTOMER INTERVIEWS
   What do customers say they get from your product?
   What would they miss most if it disappeared?

9. CURRENT TEAM DISAGREEMENTS
   Are there existing debates about what metric to prioritize?
   Understanding existing tensions helps identify the alignment problem
   the north star needs to solve.

10. COMPARABLE COMPANY BENCHMARKS
    What north star metrics do comparable companies in your category use?
    This provides a useful reference point.
```

### Example of a Strong Input Prompt
```
Product: B2B SaaS for restaurant payroll automation. Restaurants use it to
run payroll, manage tip pooling, and generate compliance reports.
Core value: Restaurant operators run their weekly payroll in under 20 minutes
instead of 3 to 4 hours. They stop worrying about tip credit compliance.
Best customer behavior: Customers who run payroll at least weekly and generate
at least one compliance report per month retain at 97%+ after 12 months.
Customers who only use payroll processing without compliance features churn at 18% monthly.
Current metrics: MRR, churned accounts per month, payrolls processed, active users,
support tickets
Business model: $199/month flat SaaS subscription per location
Retention data: Weekly payroll runs + at least one compliance feature = 97% 12-month retention.
Payroll only = 62% 12-month retention.
Team disagreements: Finance wants to optimize for MRR. Product wants to optimize for
weekly active users. Growth wants to optimize for new accounts.
```

---

## Output Format

```
1. NORTH STAR METRIC RECOMMENDATION
   The specific metric with a precise definition.
   Why this metric: the connection to customer value and business outcome.
   How it is calculated: exact formula and measurement method.

2. NORTH STAR METRIC RATIONALE
   The customer value story: what is happening in the product when this metric grows?
   The business logic: why does growth in this metric predict revenue growth?
   The leading indicator evidence: any data or logic connecting NSM to retention/revenue.

3. INPUT METRICS (3 to 5)
   For each input metric:
   - Metric name and precise definition
   - How it connects to the north star
   - Who owns driving this metric
   - Current baseline and target

4. HEALTH METRICS (guardrails)
   The 3 to 5 metrics that must stay within bounds
   while the team pursues the north star.
   Floor or ceiling value for each.

5. NORTH STAR METRIC HIERARCHY DIAGRAM
   A visual or structured representation showing:
   NSM at top, input metrics below, health metrics as guardrails.

6. ALTERNATIVE METRICS CONSIDERED
   The other metrics that were evaluated and why they were not chosen.
   This is important for team alignment: people whose preferred metric
   was not chosen need to understand why.

7. ALIGNMENT IMPLICATIONS
   How each team (product, engineering, marketing, sales, CS)
   connects their work to the north star metric.
   One sentence per team: "CS advances the north star by..."

8. MEASUREMENT AND INSTRUMENTATION REQUIREMENTS
   What needs to be tracked to measure the north star metric.
   Any gaps in current instrumentation that must be addressed.
   Recommended reporting cadence.
```

---

## Starter Prompt

```
You are a product strategy and growth analytics expert helping me define
and document a north star metric for my business.

Product description: [what your product does and who uses it]
Core value delivered: [what specifically changes for customers who get value from the product]
Best customer behavior: [what high-retention, high-value customers do that others do not]
Retention or engagement data: [any data on what predicts retention or churn]
Current metrics tracked: [what you currently measure]
Business model: [how you charge and generate revenue]
Current team disagreements: [any existing debates about what to optimize for]
Comparable company north stars: [if known]

Please produce:
1. A specific, precisely defined north star metric recommendation
2. The rationale connecting the metric to customer value and business outcome
3. Three to five input metrics that drive the north star, each with owner and baseline
4. Three to five health metrics as guardrails
5. A north star metric hierarchy showing the full framework
6. Alternative metrics considered and why they were not chosen
7. How each team connects their work to the north star in one sentence each
8. Measurement and instrumentation requirements

Be specific. "Engagement" is not a metric. Give me a precise definition
including what action is measured, over what time period, and by which users.
If the data I have provided suggests a clear leading indicator of retention,
prioritize that signal in the recommendation.
If there are two strong candidates and a genuine trade-off, present both
and explain the strategic choice involved in picking one over the other.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `okr-framework.md` | North star metric anchors company and team OKRs |
| `metrics-dashboard-spec.md` | Build a dashboard to track the north star and input metrics |
| `tracking-plan.md` | Instrument your product to capture the north star metric |
| `ab-test-plan.md` | Design experiments that test impact on north star and input metrics |
| `product-metrics-framework.md` | Build the full metrics hierarchy the north star sits within |

| Use This Before | Why |
|---|---|
| `customer-discovery-interview.md` | Interviews reveal what value customers actually experience |
| `cohort-analysis-report.md` | Cohort data reveals which behaviors predict retention |
| `funnel-analysis-report.md` | Funnel data identifies where customers reach or fail to reach core value |

---

## Reference Frameworks

| Framework | Use For |
|---|---|
| North Star Framework (Amplitude) | Core north star metric + input metrics + health metrics structure |
| AARRR / Pirate Metrics (McClure) | Understanding which stage of the funnel the north star belongs to |
| Jobs-to-be-Done (Christensen) | Identifying the core job that the north star should measure completion of |
| Aha Moment Analysis | Finding the product behavior that predicts long-term retention and centering the NSM on it |
| Growth Accounting Framework | Understanding how the north star metric moves: new users, retained users, resurrected users, churned users |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
