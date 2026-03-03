# experience-map.md

> **Skill:** Produces a broad experience map documenting the full customer journey across all channels, touchpoints, and time periods from initial awareness through long-term relationship, identifying friction and opportunity across the complete arc.

---

## TLDR

Broader than a user journey map, an experience map covers the full customer lifecycle: from first awareness of a problem through discovery, evaluation, purchase, onboarding, active use, renewal, and advocacy. It spans multiple channels and is often persona-agnostic to reveal universal experience patterns. Used for strategic decisions about where to invest in experience improvement across the full customer lifecycle.

---

## Topic Explanation

### Experience Map vs. Journey Map vs. Service Blueprint

| Dimension | User Journey Map | Experience Map | Service Blueprint |
|---|---|---|---|
| Scope | Specific task or goal | Full lifecycle | Full lifecycle + operations |
| Persona | Specific user type | Often generic | Specific user + org view |
| Timeframe | Minutes to hours | Days to years | Same as experience map |
| Primary use | Product UX | Strategic investment | Service design |
| Backstage | No | No | Yes |

### What an Experience Map Reveals That a Journey Map Does Not

Journey maps focus on a bounded interaction with a product. Experience maps reveal:
- **Pre-product experiences:** How customers form beliefs about the problem and the category before ever touching your product
- **Channel transitions:** Where the experience crosses from marketing to sales to onboarding to support and whether those transitions are coherent
- **Relationship arc:** How the emotional relationship with the brand evolves over time from stranger to advocate
- **Long-tail experiences:** What happens at renewal, at referral, at expansion, at potential churn

### Swim Lane Structure

Experience maps use swim lanes: horizontal bands that each represent a different perspective or dimension of the experience. Common swim lanes:

- Customer actions (what they do)
- Customer touchpoints (where they interact)
- Thoughts and questions (what they are thinking)
- Emotional arc (how they feel)
- Jobs being done (what they are trying to achieve)
- Moments of truth (high-stakes moments that disproportionately shape perception)
- Pain points
- Opportunities

The moments of truth swim lane is particularly important: research by McKinsey and others shows that a small number of high-stakes moments disproportionately shape overall customer perception. Identifying these moments is a primary strategic output of the experience map.

---

## When to Use This Skill

Use when:
- Conducting a strategic review of the full customer experience before a major product or go-to-market investment
- Identifying where the customer experience is weakest across the full lifecycle
- Aligning product, marketing, sales, and CS around a shared view of the customer journey
- Designing a new product or service from scratch and needing to understand the full experience arc

---

## Dos

- **Do include the pre-product experience.** What does the customer experience before they encounter your product? Their beliefs, behaviors, and alternatives shape how they experience your product.
- **Do mark "moments of truth."** Not all touchpoints are equal. Identify the 3 to 5 moments that most shape customer perception of the relationship.
- **Do use research data.** Like journey maps, experience maps based on assumptions rather than research are hypothetical, which should be clearly labeled.
- **Do validate with multiple customer segments.** A single experience map risks reflecting the experience of only one type of customer. Validate across segments or produce segment-specific maps.

---

## Output Format

```
1. MAP HEADER
   Customer type(s), scope (start and end), date, data sources, version.

2. LIFECYCLE STAGES (6 to 10)
   Named from the customer's perspective:
   e.g., Unaware / Aware / Considering / Evaluating / Purchasing /
   Onboarding / Using / Expanding / Advocating / Churning

3. SWIM LANES FOR EACH STAGE
   - Customer actions
   - Touchpoints (channel, interface, or person)
   - Questions and thoughts
   - Emotional state
   - Jobs being done
   - Moments of truth (flagged)
   - Pain points
   - Opportunities

4. EMOTIONAL ARC
   High/low visualization across the full lifecycle.
   Highest and lowest moments identified and annotated.

5. MOMENTS OF TRUTH ANALYSIS
   The 3 to 5 moments that most determine customer perception.
   Evidence for why these are disproportionately important.
   Current quality at each moment.

6. STRATEGIC OPPORTUNITY AREAS
   The 3 to 5 highest-leverage areas for experience improvement.
   Mapped to specific lifecycle stages.

7. CROSS-FUNCTIONAL IMPLICATIONS
   Which team owns each stage and opportunity.
   Where handoffs between teams create experience seams.
```

---

## Starter Prompt

```
You are a customer experience strategist building an experience map.

Customer type(s): [persona or customer segment]
Journey scope: [from first awareness to what end point]
Research data: [key findings from interviews, surveys, or VoC programs]
Known pain points: [what you already know about where the experience breaks down]
Known touchpoints: [all customer-facing interfaces, channels, and people]
Strategic purpose: [what decisions this map will inform]

Produce a complete experience map with lifecycle stages, swim lanes,
moments of truth analysis, and strategic opportunity areas.
Flag any stage where evidence is thin and further research is recommended.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
