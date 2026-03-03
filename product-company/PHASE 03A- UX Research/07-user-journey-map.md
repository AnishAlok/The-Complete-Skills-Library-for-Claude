# user-journey-map.md

> **Skill:** Produces a structured user journey map documenting the stages, steps, touchpoints, thoughts, emotions, and pain points of a user's experience with a product or service over time.

---

## TLDR

This skill helps you answer: *"What is the complete experience of a user trying to accomplish a goal, where are the highest points of friction or emotion, and where should we invest in improvement?"* It produces a journey map with stages, steps, touchpoints, emotional arc, pain points, and opportunity areas in a format suitable for team workshops and product decisions.

---

## Topic Explanation

### Journey Map vs. Experience Map vs. Service Blueprint

These three tools are often confused. They share a linear, time-based structure but differ in scope and audience:

**User journey map:** Focused on a specific user type completing a specific task or goal. Covers a bounded timeframe. Includes the user's thoughts and emotions. Used for product and UX improvement.

**Experience map:** Broader than a journey map. Covers the full experience arc across all touchpoints and over a longer time period. Often agnostic to a specific product. Used for understanding the broader customer lifecycle.

**Service blueprint:** Includes both the front-stage user experience and the back-stage organizational processes that support it. Used for service design and operational improvement.

This skill covers the user journey map. See `experience-map.md` and `service-blueprint.md` for the others.

### Journey Map Components

A standard journey map has these horizontal layers, each spanning across the stages:

**Stages:** The major phases of the journey. Typically 4 to 8 stages. Named from the user's perspective ("Discover" not "Acquisition").

**Steps / Actions:** The specific things the user does within each stage.

**Touchpoints:** Where the user interacts with the product, service, or organization. Which channel, interface, or person.

**Thoughts:** What the user is thinking at each stage. Based on research data, not assumed.

**Emotions:** How the user feels at each stage. Often represented as an emotional arc (line graph showing high/low emotional states over the journey).

**Pain points:** Moments of friction, confusion, frustration, or failure. The most actionable layer.

**Opportunities:** Potential design or product improvements that address specific pain points.

### Journey Map ≠ User Flow

A user journey map is not a user flow or a task flow. User flows document the paths through an interface. Journey maps document the human experience of a goal. Journey maps include the user's thoughts and emotions. User flows do not. Journey maps span across channels and touchpoints. User flows typically document a single interface.

### Evidence-Based vs. Hypothetical Journey Maps

Journey maps should be based on research data, not assumed experiences. The most common failure of journey maps is that they are designed by the product team based on assumptions rather than grounded in observation and interviews.

**Evidence-based:** Each cell in the map can be attributed to research data. "User is frustrated at the compliance step" because 7 of 12 interview participants described specific frustration at that moment.

**Hypothetical:** The team's best guess at the experience. Useful as a starting point for research but should be clearly labeled as hypothetical until validated.

---

## When to Use This Skill

Use when:
- Understanding the full experience of a user trying to accomplish a goal
- Identifying the highest-friction moments in a user's experience for prioritized improvement
- Aligning a cross-functional team on a shared understanding of the user experience
- Communicating the user perspective to stakeholders who do not directly work with users
- Before a redesign initiative, to establish the current-state experience as a baseline

Do NOT use when:
- Documenting interface flows or navigation paths (use user flow diagrams)
- Mapping the full service experience including back-stage operations (use `service-blueprint.md`)
- Mapping the broader multi-year customer lifecycle (use `experience-map.md`)

---

## Dos

- **Do base the map on actual research data.** Label each element with its evidence source.
- **Do write all labels from the user's perspective.** Stage names, thoughts, and emotions should use the user's language, not internal product terminology.
- **Do include the emotional arc prominently.** The highest and lowest emotional points are typically the most important design opportunities. Make the arc visible.
- **Do define a specific persona and scenario.** A journey map for "all users" is a map for no user. Name the user type and the specific goal or scenario.
- **Do distinguish the current-state map from the future-state map.** These are two different artifacts. Do not blend what is with what should be.

---

## Donts

- **Dont make the map too granular.** Capturing every micro-step produces a map too complex to be useful. Aim for 3 to 6 steps per stage.
- **Dont invent emotions.** "User is delighted" without research evidence is assumption, not data. Use hedged language if the evidence is thin: "User may feel..."
- **Dont produce the map without sharing it.** A journey map that lives in a Figma file and is never discussed has no value. Plan for a working session or review.
- **Dont skip the opportunity layer.** The map without opportunities is a documentation exercise. The opportunity layer is what converts the map into a design input.

---

## Ideal Inputs

```
1. USER TYPE / PERSONA
   Who is this journey map about?
   What are the key characteristics of this user?

2. SCENARIO
   What goal is the user trying to accomplish?
   What triggers the start of the journey?
   What defines the end?

3. RESEARCH DATA
   Interview quotes, observation notes, usability test findings.
   The evidence that will populate thoughts, emotions, and pain points.

4. CURRENT TOUCHPOINTS
   What interfaces, channels, and human interactions exist in this journey?
   What does the user encounter along the way?

5. SCOPE
   What timeframe does this journey cover?
   Does it start before using the product (awareness/discovery) or
   at first product interaction?
```

---

## Output Format

```
1. MAP HEADER
   User persona or type, scenario / goal, scope (start and end point),
   date, data sources, version (current-state or future-state).

2. STAGES
   4 to 8 stages named from the user's perspective.
   Each stage with a brief description of what is happening.

3. LAYERED MAP TABLE
   Horizontal layers: Stages
   Vertical rows:
   - Steps/Actions: what the user does
   - Touchpoints: what channels or interfaces are involved
   - Thoughts: what the user is thinking (in quotes or paraphrased)
   - Emotions: emotional state (word and/or score)
   - Pain Points: specific moments of friction or failure
   - Opportunities: potential improvements (kept brief, to develop further)

4. EMOTIONAL ARC
   A line graph or visual representation of emotional high and low points
   across the journey, annotated with the key moments.

5. TOP PAIN POINTS SUMMARY
   The 3 to 5 most significant pain points from the map, ranked by
   severity and opportunity for impact.

6. OPPORTUNITY AREAS
   Brief descriptions of 3 to 5 opportunity areas for design improvement.
   Each linked to a specific pain point in the map.

7. EVIDENCE LOG
   Sources for key cells in the map.
   Flags where evidence is thin and further research is recommended.
```

---

## Starter Prompt

```
You are a UX designer and researcher building an evidence-based user journey map.

User type and persona: [who this journey is about]
Scenario: [the specific goal the user is trying to accomplish]
Journey scope: [where the journey starts and ends]
Research data: [paste interview quotes, observations, or key findings]
Current touchpoints: [interfaces, channels, and interactions in this journey]
Is this current-state or future-state: [which version is needed]

Please produce a complete user journey map including:
1. Map header with user type, scenario, scope, and data sources
2. Stage definitions with names from the user's perspective
3. A layered map covering steps, touchpoints, thoughts, emotions,
   pain points, and opportunities for each stage
4. An emotional arc narrative describing the highest and lowest points
5. A top 3 to 5 pain points summary with severity ratings
6. Opportunity areas linked to specific pain points
7. An evidence log flagging where data is solid vs. thin

Write all labels from the user's perspective using their language.
Flag any cell that is based on assumption rather than research evidence.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `experience-map.md` | Expand to the broader experience across the full customer lifecycle |
| `service-blueprint.md` | Add the back-stage organizational view to the journey |
| `affinity-mapping.md` | Use affinity mapping as input to identify journey stages and pain points |
| `heuristic-evaluation.md` | Evaluate specific touchpoints identified in the journey map |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
