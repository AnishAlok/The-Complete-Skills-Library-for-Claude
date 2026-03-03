# ad-copy.md

> **Skill:** Produces paid advertising copy variations for search, social, and display channels with a structured A/B testing framework for optimizing performance.

---

## TLDR

Ad copy is short-form marketing copy for paid channels: search (Google, Bing), social (LinkedIn, Meta), and display. This skill produces multiple copy variations per channel with distinct angles, along with a testing framework documenting what to test in what order and how to declare a winner.

---

## Topic Explanation

### Why Multiple Variations Are Required

Ad copy performance is difficult to predict. The headline the team agrees sounds most polished frequently underperforms a rougher, more direct alternative. The only reliable method: test distinct variations that represent meaningfully different angles, not just different word choices.

Best practice: write 3 to 5 variations per element (headline, body, CTA) where each represents a genuinely different approach. Test one variable at a time to produce interpretable results.

### The Six Advertising Angles

An advertising angle is the strategic frame used to communicate value. Different angles work for different audiences at different stages:

**Problem-led:** Lead with the pain. "Still building reports in spreadsheets?"
**Outcome-led:** Lead with the result. "Close your books 3x faster."
**Social proof-led:** Lead with credibility. "Join 10,000 finance teams who switched."
**Curiosity-led:** Create an information gap. "The one mistake most ops teams make."
**Fear of missing out:** Create urgency. "Your competitors already moved on from this."
**Direct offer:** Lead with the value of the trial or demo. "See a live demo in 20 minutes."

### Channel Constraints

Google Search: H1 (30 chars), H2 (30 chars), H3 (30 chars), D1 (90 chars), D2 (90 chars).
LinkedIn Sponsored Content: Intro text (150 chars recommended), Headline (70 chars), Description (100 chars).
Meta: Primary text (125 chars before truncation), Headline (40 chars), Description (20 chars).
Display/Banner: Headline (25 to 40 chars), Body (50 to 90 chars), CTA (15 to 25 chars).

---

## Output Format

```
AD COPY DOCUMENT

Campaign: [name]
Product/offer: [what is being advertised]
Target audience: [ICP and targeting parameters]
Campaign goal: [trial signups / demo requests / downloads]
Landing page: [destination URL]

---

GOOGLE SEARCH ADS

[Angle A: Problem-led]
H1 (30 chars): [headline]
H2 (30 chars): [headline]
H3 (30 chars): [headline]
D1 (90 chars): [description]
D2 (90 chars): [description]

[Angle B: Outcome-led]
H1: [headline]
H2: [headline]
H3: [headline]
D1: [description]
D2: [description]

[Angle C: Social proof-led]
[repeat format]

---

LINKEDIN SPONSORED CONTENT

[Angle A: Problem-led]
Intro text (150 chars): [text]
Headline (70 chars): [text]
Description (100 chars): [text]
CTA button: [Learn More / Download / Request Demo / Sign Up]

[Angle B: Outcome-led]
[repeat format]

[Angle C: Direct offer]
[repeat format]

---

META (Facebook/Instagram)

[Angle A: Problem-led]
Primary text (125 chars): [text]
Headline (40 chars): [text]
Description (20 chars): [text]
CTA: [Learn More / Sign Up / Get Started]

[Angle B and C: repeat]

---

TESTING FRAMEWORK

Test priority 1: Headline angle across channels (problem vs. outcome)
Variables: [what is being compared]
Minimum duration: [2 weeks or 1,000 impressions per variant, whichever comes first]
Winning criterion: [CTR / CPC / conversion rate to landing page]

Test priority 2: [next variable to test]
[repeat format]

Do not test simultaneously: [elements that should be held constant]
Brand safety exclusions: [angles or claims not to test]
```

---

## Starter Prompt

```
You are a product marketer writing paid advertising copy.

Product/offer: [what is being advertised]
Target audience: [ICP and targeting parameters by channel]
Campaign goal: [trial signups / demos / downloads]
Channels: [Google / LinkedIn / Meta / display]
Core value proposition: [primary benefit to emphasize]
Best proof point: [the most compelling metric or social proof]
Angles to test: [which of the six angles to create variations for]

Produce complete ad copy for each channel with at least 3 angle variations per channel.
Every variation must represent a meaningfully different angle, not just different wording.
Each variation must respect the character limits for that channel exactly.
Include a testing framework with clear winning criteria.
```

---

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
