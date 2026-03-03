# mental-model-map.md

> **Skill:** Produces a mental model map that documents how users conceptualize a domain, task, or system, revealing the gap between their mental model and the actual product model to guide design decisions.

---

## TLDR

A mental model map documents how users think about a domain: what categories they use, what they expect to happen, and how they reason about cause and effect. Comparing the user's mental model to the product's conceptual model reveals the sources of confusion, learnability failures, and terminology mismatches. Used to inform IA, navigation, labeling, and onboarding design.

---

## Topic Explanation

### What Is a Mental Model?

A mental model is a user's internal representation of how something works. It is built from prior experience, analogies to familiar systems, instructions, and direct product use. Mental models are:

- **Incomplete:** Users do not need to understand how a system works completely to use it adequately.
- **Often wrong:** Users form mental models based on inference, not complete knowledge.
- **Functional:** Mental models do not need to be correct. They only need to be functional enough to enable the user to predict what will happen and act accordingly.

The design implication is not that users must have correct mental models. It is that the product must either match users' existing mental models (exploiting familiar mental models) or provide sufficient scaffolding to build new correct ones.

### Mental Model Gap Analysis

The strategic output of mental model research is a gap analysis between:
- **Users' mental model:** How users think the system works
- **Product conceptual model:** How the product actually works
- **Design model:** How the designer intended users to understand it

When these three models diverge, usability problems occur. The mental model map makes these divergences visible and actionable.

### How to Elicit Mental Models

Mental models are not directly observable. They are inferred from:
- **Think-aloud protocols:** Users narrate expectations and surprises during task performance
- **Card sorting:** Users categorize and label concepts, revealing how they group things
- **Concept mapping:** Users draw or describe relationships between concepts
- **Protocol analysis:** Researchers analyze verbal data from task performance for model-revealing statements

---

## Output Format

```
1. DOMAIN OVERVIEW
   What domain or system this mental model map covers.
   The user type(s) studied.

2. USER MENTAL MODEL REPRESENTATION
   The key concepts users hold about this domain.
   How users categorize and relate these concepts.
   The language users use (their vocabulary, not product vocabulary).
   Common misconceptions or incorrect beliefs.

3. PRODUCT CONCEPTUAL MODEL
   How the product actually works.
   The categories and relationships the product uses.
   The product's vocabulary.

4. GAP ANALYSIS
   Where the user mental model and product conceptual model diverge.
   Specific mismatches: categories, terminology, cause-effect reasoning.
   The usability consequence of each gap.

5. DESIGN IMPLICATIONS
   For each significant gap:
   - Option A: Change the design to match the user's mental model
   - Option B: Change the onboarding/labeling to build the correct model
   - Recommendation and rationale

6. VOCABULARY MAP
   User language vs. product language for key concepts.
   Recommended design vocabulary based on user mental models.
```

---

## Starter Prompt

```
You are a UX researcher building a mental model map for a specific domain.

Domain or system: [what area of the product or service]
User type: [who was studied]
Research data: [interview quotes, card sort results, observation notes]
Current product conceptual model: [how the product actually organizes and labels things]

Produce a complete mental model map showing user concepts and vocabulary,
the gap analysis comparing user and product models, and design implications
for each significant gap.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
