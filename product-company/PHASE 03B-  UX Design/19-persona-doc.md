# persona-doc.md

> **Skill:** Produces a research-grounded persona document capturing the goals, behaviors, pain points, mental models, and context of a specific user type to guide design and product decisions.

---

## TLDR

This skill helps you answer: *"Who specifically are we designing for, what are they trying to accomplish, and what do we know about how they think and work?"* It produces a complete persona document that synthesizes user research into a representative, actionable user profile. Used to align cross-functional teams on who the user is and to keep design decisions anchored in real user needs.

---

## Topic Explanation

### Evidence-Based vs. Assumed Personas

Personas are only as valuable as the research behind them. The most common persona failure is building personas from assumptions rather than data, producing characters that represent the team's beliefs about users rather than actual user behavior.

**Evidence-based persona:** Built from primary research data (interviews, observation, surveys). Each behavioral and attitudinal attribute can be traced to specific research findings. May surprise the team.

**Hypothetical persona:** Built from assumptions, demographics, and team consensus. Reflects the team's existing mental models. Rarely surprises anyone. Tends to confirm existing biases.

Both can be useful, but they serve different purposes and must be clearly labeled. An evidence-based persona informs design decisions. A hypothetical persona is a research target: a profile of who you think your user is that should be validated against real research.

### Behaviors Over Demographics

Demographic information (age, location, job title) is the least useful layer of a persona for product design purposes. Two 42-year-old restaurant owners may have completely different technology relationships, workflows, and needs. Two people with very different demographics may have essentially the same product needs.

The most useful persona attributes are behavioral and attitudinal:
- How do they currently solve the problem this product addresses?
- What does their workflow look like on a typical day?
- What do they trust and distrust?
- How technically comfortable are they?
- What does success look like from their perspective?

Demographics give a persona face and context. Behaviors give it design utility.

### Goals Hierarchy

A well-constructed persona documents goals at three levels:

**End goals:** The outcomes the user ultimately wants. These are the "why" behind product use. "Run my restaurant without compliance anxiety."

**Experience goals:** How the user wants to feel during interaction. "Feel competent and in control without needing to be a payroll expert."

**Life goals:** Deeper personal motivations that contextualize the product relationship. "Be respected as a professional operator by my staff and accountant."

Designing only for end goals produces functional products. Designing for all three levels produces products that people choose and stay loyal to.

---

## When to Use This Skill

Use when:
- A product team lacks a shared, explicit definition of who the primary user is
- A new product area is being designed and user context needs to be established
- Multiple competing views of "the user" exist on the team
- Onboarding new team members who need to understand the user
- After a round of user research that generated enough data to build or update a persona

Do NOT use when:
- No user research exists and the persona would be entirely hypothetical (do the research first, or clearly label it as hypothetical)
- A well-validated persona already exists and only needs minor updating

---

## Dos

- **Do ground every attribute in research evidence.** Each behavioral claim should be traceable to interview data, observation notes, or survey findings.
- **Do focus on behaviors and mental models, not just demographics.** "Maria owns 3 restaurants" tells us less than "Maria checks her phone during prep time and does all admin work between the lunch and dinner rushes."
- **Do include frustrations and pain points specifically.** Generic frustrations ("wants things to be easier") are not useful. Specific ones ("frustrated that she has to recalculate tip credits manually every pay period") are.
- **Do validate the persona with real users.** Show the finished persona to 3 to 5 people who match the profile and ask if it resonates.
- **Do include a quote.** A verbatim or synthesized quote from research that captures the persona's essence makes the persona feel real.

---

## Donts

- **Dont make personas so specific that they feel like one real person.** A persona is a composite. If it could only describe one specific person, it has been over-specified.
- **Dont include attributes that do not affect product design decisions.** Age, hobbies, and family situation are only relevant if they directly affect how this person uses the product.
- **Dont create more than 3 to 4 primary personas.** A product designed for 8 distinct personas is a product designed for no one.
- **Dont print and frame the persona.** A persona that becomes wall art is a persona that has stopped being a working tool. Keep personas in tools the team uses daily.

---

## Ideal Inputs

```
1. RESEARCH DATA
   Interview quotes, observation notes, survey findings.
   The data that will ground the persona's behavioral attributes.

2. USER TYPE BEING DESCRIBED
   What role, segment, or user type is this persona representing?

3. PRODUCT CONTEXT
   What product or product area will this persona be used for?

4. GOALS AND MOTIVATIONS (from research)
   What are users in this segment trying to accomplish?
   What drives their behavior?

5. FRUSTRATIONS AND PAIN POINTS (from research)
   What is not working for them?
   What barriers do they encounter?
```

---

## Output Format

```
1. PERSONA HEADER
   Name (memorable, not a real person's name), role/title, photo placeholder,
   one-sentence summary. Version and date. Evidence base: number of research
   participants this persona is drawn from.

2. CONTEXT AND BACKGROUND
   Role description: what this person does day-to-day.
   Work environment: where and how they work.
   Technology context: tools they use, device preferences, technical comfort.
   Key context details that are relevant to product design.

3. GOALS
   End goals: 3 to 5 outcome-level goals.
   Experience goals: how they want to feel.
   Life goals (if relevant): deeper motivations.

4. A DAY IN THE LIFE
   Narrative walkthrough of a representative workday.
   Specifically: when and how they encounter the problem this product addresses.

5. BEHAVIORS AND PATTERNS
   How they currently solve the problem.
   Workflow patterns relevant to the product.
   Workarounds they have developed.
   Decision-making patterns.

6. FRUSTRATIONS AND PAIN POINTS
   Specific, research-grounded frustrations.
   What causes them and what effect they have.

7. MENTAL MODEL
   How they think about the domain.
   Key concepts they use.
   Where their model diverges from how the product works.

8. WHAT THEY TRUST AND DISTRUST
   Sources of credibility for this persona.
   What makes them skeptical.

9. REPRESENTATIVE QUOTE
   A verbatim or lightly synthesized quote that captures this persona's perspective.

10. DESIGN IMPLICATIONS
    3 to 5 direct implications for product and UX design.
    Written as: "Because [persona attribute], the design should [implication]."
```

---

## Starter Prompt

```
You are a UX researcher building an evidence-based persona.

User type: [the role or segment this persona represents]
Research data: [paste interview quotes, observation notes, or key findings]
Product context: [what product this persona is for]
Goals from research: [what this user type is trying to accomplish]
Frustrations from research: [what is not working for them]
Behavioral patterns: [how they currently work and solve problems]
Technology context: [their tools, devices, technical comfort]

Please produce a complete persona document including:
1. Header with memorable name, role, and one-sentence summary
2. Context and background with work environment and technology context
3. Goals at end, experience, and life levels
4. A day in the life narrative
5. Behaviors, patterns, and workarounds
6. Specific, research-grounded frustrations
7. Mental model of the domain
8. Trust and distrust signals
9. A representative quote
10. Design implications in "Because X, the design should Y" format

Ground every behavioral and attitudinal attribute in the research data provided.
Flag any attribute that is assumed rather than research-based.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `ux-design-brief.md` | Persona informs the user context section of the brief |
| `user-journey-map.md` | Journey maps are built for a specific persona |
| `market-segmentation.md` | Personas are the design expression of market segments |
| `jobs-to-be-done.md` | JTBD research enriches the goals and mental model sections |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
