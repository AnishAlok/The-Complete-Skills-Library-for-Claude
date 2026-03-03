# demand-gen-campaign.md

> **Skill:** Produces a demand generation campaign brief with audience, messaging, channel plan, asset list, and copy for a multi-channel campaign designed to generate pipeline.

---

## TLDR

A demand generation campaign is a coordinated, multi-channel marketing effort designed to generate pipeline: awareness among the right people, interest that converts to a lead, and progression through the funnel to an opportunity. This skill produces the campaign brief and copy: the strategic decisions (audience, message, offer) and the tactical execution (channel plan, asset list, copy for each asset).

---

## Topic Explanation

### Demand Generation vs. Lead Generation

These terms are often used interchangeably and mean different things to different teams. For purposes of this skill:

**Demand generation:** creating awareness and interest among the target audience, including people who are not yet in the market. Broader, top-of-funnel orientation. Goal: expand the pool of aware, interested potential buyers.

**Lead generation:** converting interested buyers into identified contacts in the database. Narrower, mid-funnel orientation. Goal: capture contact information and intent signals.

A full-funnel demand gen campaign does both: it creates demand and captures the leads that demand generates.

### The Campaign Architecture

A demand gen campaign is built on three strategic decisions:

**Audience:** a specific, defined segment with a shared problem or characteristic. The more specific the audience, the more resonant the message. Campaigns targeted at "B2B companies" perform worse than campaigns targeted at "VP of Engineering at 100-500 person SaaS companies."

**Offer:** what you are giving the audience in exchange for their attention and contact information. A compelling offer must have genuine value for the audience: a specific tool, framework, research finding, or experience they cannot easily get elsewhere.

**Message:** the specific angle that connects the audience's problem to the offer. One campaign, one message. Campaigns trying to communicate multiple things communicate nothing clearly.

---

## Output Format

```
DEMAND GEN CAMPAIGN BRIEF

Campaign name: [name]
Campaign goal: [MQLs / pipeline / ARR influenced]
Target metric and goal: [e.g., 200 MQLs within 6 weeks of launch]
Campaign duration: [start date to end date]
Budget: [total allocated]
Campaign owner: [name]

---

1. AUDIENCE
   Segment: [specific ICP definition]
   Size of targetable universe: [estimated reachable audience]
   Stage of awareness: [unaware / problem aware / solution aware / product aware]
   Where they are: [channels they use, communities they belong to, events they attend]
   What they care about right now: [the timely problem or trigger this campaign addresses]

2. CAMPAIGN OFFER
   Offer type: [content download / webinar / free tool / assessment / trial / demo]
   Offer name: [specific title]
   Why this audience wants it: [the specific value it delivers]
   What makes it compelling vs. generic: [the differentiated angle]

3. CAMPAIGN MESSAGE
   Core message: [one sentence connecting the audience's problem to the offer]
   Supporting messages: [2 to 3 proof points or supporting claims]
   Urgency or timeliness factor: [why now]

4. CHANNEL PLAN
   For each channel:
   Channel | Audience segment | Format | Budget allocation | Goal metric

   Standard channel mix:
   - Paid social (LinkedIn): ICP targeting by title/company/industry
   - Paid search: intent-based keyword targeting
   - Email to house list: segmented by ICP
   - Content syndication (if applicable)
   - Retargeting: website visitors who did not convert

5. ASSET LIST WITH COPY
   For each asset needed:

   ASSET: [e.g., LinkedIn sponsored post]
   Audience: [targeting parameters]
   Copy: [full ad copy following ad-copy.md format]

   ASSET: [e.g., Email to house list]
   Subject line: [A and B options]
   Copy: [full email body]

   ASSET: [e.g., Landing page]
   Headline: [headline copy]
   Body: [key copy blocks]
   CTA: [button copy]

6. NURTURE PLAN
   What happens after a lead converts on the offer:
   Immediate: [confirmation email content]
   Day 2 to 14: [follow-up sequence reference to email-nurture-sequence.md]
   SDR handoff criteria: [when a lead becomes sales-ready]

7. MEASUREMENT AND REPORTING
   Primary KPI: [the number that defines success]
   Secondary KPIs: [CPL, conversion rate, influenced pipeline]
   Reporting cadence: [weekly during campaign, final report at end]
   Attribution model: [first touch / last touch / multi-touch]
```

---

## Starter Prompt

```
You are a demand generation marketer writing a campaign brief.

Campaign goal: [MQLs / pipeline target / brand awareness]
Target audience: [specific ICP segment]
Campaign offer: [what you are offering in exchange for attention/contact]
Core message: [the angle connecting the audience's problem to the offer]
Channels available: [LinkedIn / Google / email / content syndication / retargeting]
Budget: [total campaign budget]
Duration: [campaign timeframe]
SDR or sales follow-up plan: [how leads will be worked after conversion]

Produce a complete demand gen campaign brief with all 7 sections.
Include full copy for at least one ad, one email, and the landing page headline.
The offer must have a clear, specific value proposition for the target audience.
```

---

*Skill file version: 1.0 | Phase: 09 - Marketing | Company type: Product*
