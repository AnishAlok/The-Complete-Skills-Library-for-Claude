# email-nurture-sequence.md

> **Skill:** Produces a multi-email nurture sequence with subject lines, body copy, and CTAs designed to move a lead from initial interest to conversion through a structured content arc.

---

## TLDR

An email nurture sequence is a planned series of emails to leads who have not yet converted, designed to build trust, demonstrate value, handle objections, and create conditions for conversion. This skill produces the full sequence: the arc, all email copy, subject line variations per email, and CTAs for a 5 to 7 email series.

---

## Topic Explanation

### Nurture Sequences vs. Drip Campaigns

Drip campaigns: send the same emails to everyone on a time-based schedule regardless of behavior. Low effort, low relevance, low performance.

Nurture sequences: behavior-responsive content that adapts based on what the lead has engaged with (which links they clicked, which pages they visited). Higher complexity, significantly higher performance.

This skill produces the content for a nurture sequence. Whether it is implemented as behavior-triggered or time-based depends on the team's marketing automation capability.

### The Nurture Arc

The most effective B2B nurture sequences follow this content arc:

Email 1 (Welcome / Value delivery): deliver on the trigger promise and establish why this relationship is worth the reader's time.
Email 2 (Education): teach something valuable about the problem space. Not a product pitch.
Email 3 (Problem depth): help the reader understand why their current situation is costlier than they realize.
Email 4 (Social proof): show that people like them have solved this problem.
Email 5 (Solution): introduce the product directly and specifically.
Email 6 (Objection handling): address the most common reasons people do not convert.
Email 7 (Direct CTA): clear, direct, low-friction ask.

The most common failure: pitching the product in email 1 or 2. Trust must be built before conversion is earned.

### Subject Line Discipline

Subject lines have 10x more impact on open rates than body copy. Every email should have 2 to 3 subject line variations to test, each using a genuinely different approach: curiosity gap, direct benefit, question, social proof, personalization.

---

## Output Format

```
EMAIL NURTURE SEQUENCE

Sequence name: [name]
Enrollment trigger: [content download / webinar registration / trial signup / demo request]
Target audience: [ICP]
Sequence goal: [trial activation / demo booking / purchase]
Sequence length: [number of emails]
Send cadence: [Day 0, Day 2, Day 5, Day 9, Day 14, Day 21]

---

EMAIL [N]: [Arc stage name]
Send timing: Day [X] from enrollment
Arc purpose: [what this email accomplishes in the sequence]

Subject A: [primary - state the angle]
Subject B: [test variant - different angle]
Subject C: [test variant - different angle]
Preview text: [complements subject, adds information not restated. Under 90 chars]

[Salutation]

[Opening line: the hook. 1 sentence. Reference the reader's situation or the trigger event.]

[Body: 3 to 5 short paragraphs. Short sentences. One idea per paragraph.
Conversational, human, not corporate. No bullet point lists unless genuinely list-like content.]

[CTA paragraph: one clear ask. The link text is the action.]

[Warm sign-off]

[First name only]

P.S. [Optional: use for a secondary point or urgency element. Only if it adds genuine value.]

CTA link text: [exact anchor text]
CTA destination: [URL]
Primary purpose of this email: [open / engage / convert]

---

[Repeat for each email]

---

SEQUENCE BENCHMARKS
Target open rate: [X%]
Target click rate: [X%]
Target conversion rate by end of sequence: [X%]

A/B TESTING PLAN
Email 1: Subject line angle (curiosity vs. direct benefit)
Email 5: CTA (trial vs. demo)
[Additional tests by email]
```

---

## Starter Prompt

```
You are a product marketer writing an email nurture sequence.

Enrollment trigger: [what enrolls someone in this sequence]
Target audience: [ICP with role and company context]
Sequence goal: [what conversion event you are working toward]
Number of emails: [5 to 7]
Core value proposition: [what the product does and for whom]
Educational insight to deliver: [what you can teach that builds trust and authority]
Customer proof to include: [a case study or stat for the social proof email]
Top objections to address: [what prevents conversion most often]
Tone: [conversational / professional / direct]

Produce a complete nurture sequence with all emails written in full.
Include 3 subject line variations per email with different angles.
The sequence arc must build trust before pitching the product.
Every email must have exactly one CTA.
```

---

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
