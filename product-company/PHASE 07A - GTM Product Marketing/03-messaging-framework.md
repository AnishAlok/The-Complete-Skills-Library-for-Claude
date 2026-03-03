# messaging-framework.md

> **Skill:** Produces a messaging framework translating positioning into specific copy: master headline, core value pillars, proof points, audience-specific variants, objection responses, and channel adaptations.

---

## TLDR

A messaging framework is the operational translation of positioning into language that appears in actual marketing materials. While positioning defines the strategic "why" and "what," the messaging framework provides the specific words: the headline, tagline, value pillars, proof points, and variants for different audiences and channels. It is the copy reference that keeps every team member saying the same thing in the right way.

---

## Topic Explanation

### Positioning vs. Messaging

Positioning is internal and strategic. It informs all communication but is never published directly as written.

Messaging is external and tactical. It is the specific language that appears in ads, landing pages, sales decks, and emails.

The messaging framework bridges the two. For every positioning claim, the framework defines the approved language that communicates that claim credibly to each audience.

### Message Architecture: Four Levels

**Level 1 (Master headline):** The single most important claim. One sentence. Appears on the homepage hero, the first slide of the pitch deck, and the launch email subject line. If only one message lands, this is it.

**Level 2 (Supporting pillars):** Three to four value pillars that support and explain the master headline. Each pillar: one claim plus one proof point.

**Level 3 (Proof points):** The evidence behind each pillar. Customer quotes, data, case study results, third-party validation. Proof is what separates claims from credible claims.

**Level 4 (Audience variations):** How the core message adapts for specific audiences: C-suite language vs. practitioner language, industry-specific vocabulary, buyer stage (awareness vs. evaluation vs. decision).

### Why Messaging Frameworks Break Down

The most common failure mode: every team member invents their own version of the core message. Sales says one thing, the website says another, and email campaigns say a third. Prospects receive an incoherent signal about what the product is.

The messaging framework is the single source of truth. When someone writes new copy, they adapt from the approved framework rather than starting from scratch. When it is used consistently, brand recognition compounds over time.

---

## Dos

- **Do ensure every claim has at least one proof point.** Claims without evidence are just assertions. Every pillar needs a customer quote, data point, or case study result attached.
- **Do write audience-specific messages in that audience's natural language.** A VP of Engineering and a CFO describing the same product benefit will use entirely different words. Write both versions.
- **Do explicitly ban phrases that sound good but mean nothing.** "Best-in-class," "industry-leading," and "seamless integration" appear in every competitor's messaging and communicate nothing.

---

## Output Format

```
1. FRAMEWORK HEADER
   Product, version, date, PMM owner. Reference to source positioning-doc.md.

2. MASTER HEADLINE
   The single most important message. One sentence.
   Primary audience this headline addresses.
   Alternate versions for A/B testing: 2 to 3 variations, each a different angle.

3. TAGLINE
   Short, memorable expression of core value.
   Primary tagline. Alternates considered and why they were not selected.

4. ELEVATOR PITCH (30 seconds, spoken)
   What the product does, for whom, and why they should care.
   Written as natural spoken language, not polished marketing copy.
   A rep should be able to say this without sounding like they are reciting.

5. VALUE PILLARS
   For each pillar (3 to 4 total):

   PILLAR [N]: [Pillar name in 3 to 5 words]
   Claim: [The specific value claim]
   Resonates most with: [which audience and why]
   Proof point: [customer quote, data point, or case study result — specific]
   Short form (10 to 15 words for ads and social): [version]
   Long form (2 to 3 sentences for sales and web): [version]

6. AUDIENCE-SPECIFIC MESSAGES
   For each key audience:
   Audience: [role or segment]
   Primary concern: [the one thing they care most about]
   Message: [how the product addresses that concern in their language]
   Register: [technical / business / executive]
   Avoid: [language or claims that do not resonate or actively backfire with this audience]

7. COMPETITIVE MESSAGES
   For each key competitor, how to respond when a buyer raises them:
   Competitor | Their positioning claim | Our counter-message | Supporting proof

8. OBJECTION RESPONSES
   For each common objection:
   Objection: [exact language buyers actually use]
   Root concern: [what they actually mean underneath the objection]
   Approved response: [exact language to use in reply]

9. CHANNEL ADAPTATIONS
   How the core message adapts with channel-specific constraints:
   Paid search: keyword alignment, character limits, high intent
   Email subject lines: length, personalization, curiosity vs. direct
   Sales deck: narrative arc, presenter-dependent
   Website: hierarchy, scroll behavior, supporting copy
   Event/verbal: spoken register, no visual support assumed

10. BANNED PHRASES
    Language explicitly not approved for use.
    For each: the phrase and the specific reason it is banned
    (generic / unsubstantiated / used identically by competitors / off-brand tone).
```

---

## Starter Prompt

```
You are a product marketing manager writing a messaging framework.

Product: [name and description]
Positioning reference: [the core positioning from positioning-doc.md]
Primary audience: [the main target buyer]
Secondary audiences: [other segments needing different messages]
Core value pillars: [the 3 to 4 claims that define the product]
Known proof points: [customer data, quotes, case study results]
Key competitors: [who buyers compare this product against]
Common objections: [what buyers push back on most frequently]
Channels to cover: [website, ads, email, sales deck]

Produce a complete messaging framework covering all 10 sections.
Every claim must have at least one proof point — no unsubstantiated assertions.
Audience-specific messages must use language natural to that audience's role.
Include at least 5 banned phrases with a specific reason for each.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `positioning-doc.md` | Positioning is the strategic foundation this framework translates |

| Use This Next | Why |
|---|---|
| `launch-plan.md` | Messaging framework provides the approved copy for all launch assets |
| `competitive-battlecard.md` | Competitive messages section feeds each battlecard |
| `sales-enablement-doc.md` | Objection responses and audience messages become sales enablement content |

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
