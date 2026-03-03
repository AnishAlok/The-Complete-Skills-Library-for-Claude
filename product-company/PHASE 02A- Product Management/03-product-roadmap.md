# product-roadmap.md

> **Skill:** Produces a product roadmap in now/next/later, quarterly, or theme-based format that communicates planned work, priorities, and strategic direction to the appropriate audience.

---

## TLDR

This skill helps you answer: *"What are we building when, and how do we communicate that in a way that is honest, useful, and appropriately committed?"* It produces a roadmap in the format best suited to the audience and purpose: a now/next/later view for strategic communication, a quarterly view for planning, or a theme-based view for customer communication.

---

## Topic Explanation

### The Roadmap Is Not a Commitment Schedule

The most common and most damaging misunderstanding of product roadmaps is treating them as delivery schedules. Roadmaps that are treated as commitments cause:
- Teams optimizing for hitting dates rather than learning and delivering value
- Customers expecting features on specific dates and feeling betrayed when plans change
- Organizational inability to adapt to new information because the roadmap "can't change"

The roadmap is a communication tool that conveys strategic priorities and approximate sequencing. It is not a contract. This distinction must be actively managed with every audience that receives the roadmap.

### Three Roadmap Formats

**Now / Next / Later (Opportunity-Based)**
Popularized by Janna Bastow (ProdPad). Organizes work into three time horizons without specific dates. Forces strategic prioritization rather than scheduling. Best for: internal strategic communication, early-stage teams, teams that need to communicate direction without over-committing to dates.

**Quarterly (Time-Boxed)**
Organizes work into calendar quarters. More commitment than now/next/later but less than sprint-level scheduling. Best for: cross-functional planning, board and investor communication, teams with established delivery predictability.

**Theme-Based**
Organizes work by strategic theme rather than time. "Onboarding," "Compliance Intelligence," "Multi-location." Best for: customer-facing communication where feature specifics should not be promised, executive communication emphasizing strategic direction.

Most product teams maintain multiple roadmap views for different audiences.

### What Belongs on a Roadmap vs. What Does Not

**Belongs on a roadmap:**
- Initiatives, themes, or epics (not individual features or tickets)
- Strategic intent for each item (why are we doing this?)
- Rough sequencing or priority
- Confidence level or status

**Does not belong:**
- Sprint-level tasks
- Bug fixes (except high-visibility ones)
- Infrastructure improvements (unless strategically significant)
- Precise delivery dates (in most formats)

---

## Dos

- **Do communicate the why, not just the what.** A roadmap item with a strategic rationale is much more useful than a feature name.
- **Do differentiate between high and low confidence items.** Items in the "now" horizon should be high confidence. Items in "later" may be speculative.
- **Do version and date the roadmap.** Recipients need to know which version they are looking at.
- **Do tailor the format to the audience.** Engineering needs a different view than the board, which needs a different view than customers.
- **Do explicitly state what is NOT on the roadmap.** A roadmap without deprioritization signals looks like everything is coming.

---

## Donts

- **Dont put specific dates on items you are not highly confident about.** Specific dates create customer expectations and organizational commitments that are very hard to walk back.
- **Dont list features without context.** "Multi-location support" means nothing to someone who does not know why multi-location matters now.
- **Dont share the internal roadmap with customers without editing.** Internal roadmaps contain context and specificity that is inappropriate for external communication.

---

## Ideal Inputs

```
1. ROADMAP FORMAT
   Now/next/later / quarterly / theme-based / combination?
   Why this format for this audience?

2. STRATEGIC CONTEXT
   The strategy this roadmap implements.
   The goals it is designed to achieve.

3. PLANNED INITIATIVES
   What is planned for each horizon or theme?
   Strategic rationale for each.
   Confidence level.

4. DEPRIORITIZED ITEMS
   What is explicitly NOT on the roadmap and why?

5. AUDIENCE
   Internal team / leadership / board / customers / investors?
   What do they need to understand vs. what should be omitted?
```

---

## Output Format (Now / Next / Later)

```
1. ROADMAP HEADER
   Product area, version, date, audience, horizon definitions
   (Now = current sprint/quarter, Next = 1 to 2 quarters, Later = 3+ quarters).

2. STRATEGIC CONTEXT (2 to 3 sentences)
   The goals and bets this roadmap is designed to pursue.

3. NOW (current horizon)
   For each initiative:
   - Name and brief description
   - Strategic rationale (why now)
   - Key user or business goal
   - Status and confidence

4. NEXT (following horizon)
   For each initiative:
   - Name and brief description
   - Strategic rationale
   - Key dependency or prerequisite
   - Confidence level

5. LATER (future horizon)
   For each theme or initiative:
   - Name and description
   - Why it matters but not yet
   - Open questions or dependencies

6. NOT PLANNING (explicit deprioritization)
   Items frequently requested that are not on the roadmap.
   Brief rationale for each.

7. SUCCESS METRICS
   How we will know this roadmap is achieving its goals.
```

## Output Format (Quarterly)

```
1. ROADMAP HEADER
   Product area, version, date, audience.

2. STRATEGIC CONTEXT
   The annual goals this quarterly roadmap serves.

3. QUARTER-BY-QUARTER TABLE
   For each quarter (Q1 through Q4):
   - Theme or focus
   - Initiatives with brief description and rationale
   - Key goals for the quarter
   - Success metrics

4. DEPENDENCIES AND RISKS
   Cross-team dependencies.
   Key risks that could shift the roadmap.

5. METRICS AND MILESTONES
   Quarterly goals and how success is measured.
```

---

## Starter Prompt

```
You are a product manager building a product roadmap.

Roadmap format: [now/next/later / quarterly / theme-based]
Audience: [internal team / leadership / board / customers]
Strategic context: [the goals and strategy this roadmap serves]
Planned initiatives: [list of planned items with rationale and confidence]
Deprioritized items: [what is explicitly not planned and why]
Time horizon: [how far out the roadmap should cover]

Please produce a complete product roadmap in the specified format including:
1. Strategic context statement
2. Initiatives organized by horizon or quarter with rationale for each
3. Explicit deprioritization section
4. Success metrics by horizon or quarter
5. Any relevant dependencies or risks

Write each roadmap item with a "why" - not just the feature name.
Flag any item where the confidence is low enough that it should not be
communicated as a commitment.
Tailor specificity to the stated audience.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `release-planning.md` | Roadmap items become release plans |
| `product-strategy-doc.md` | Strategy determines roadmap priorities |
| `feature-prioritization.md` | Prioritization frameworks inform roadmap ordering |
| `dependency-mapping.md` | Roadmap items reveal cross-team dependencies |

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
