# prototype-spec.md

> **Skill:** Produces a prototype specification defining the scope, fidelity level, interaction coverage, and intended use of a prototype for research or stakeholder communication.

---

## TLDR

A prototype spec defines what a prototype will and will not do, at what fidelity level, and for what purpose. Without a spec, prototypes are frequently over-built (spending weeks perfecting something that needed to be tested in days) or under-built (a wireframe that cannot answer the research questions it was meant to address). The spec aligns effort with purpose.

---

## Topic Explanation

### Prototype Fidelity Levels

**Low fidelity (lo-fi):** Sketches, paper prototypes, or basic wireframes. No visual design. Fast to produce. Best for: early concept exploration, flow validation, generative research.

**Mid fidelity:** Wireframes with some interaction. Visual hierarchy but not final design. Design tokens applied but components not finalized. Best for: testing task flows, IA validation, internal alignment.

**High fidelity:** Pixel-accurate design with full visual treatment. Close to or identical to the final product. Best for: usability testing on a near-final design, stakeholder approval, investor demos.

The common mistake is defaulting to high fidelity when the research question only requires low fidelity. High-fidelity prototypes take longer to build and make participants feel they are evaluating a finished product, which suppresses honest critical feedback.

### What Prototypes Cannot Test

Prototypes are approximations. They cannot test:
- Real data behavior (unless connected to a live API)
- Performance and load times
- Complex backend logic
- Edge cases not specifically built into the prototype
- Accessibility for screen reader users (in most prototyping tools)

The prototype spec should document what the prototype cannot test so research findings are appropriately caveated.

---

## Output Format

```
1. PROTOTYPE HEADER
   Prototype name, version, designer, purpose, target use date, tool used.

2. PURPOSE
   What this prototype is for: usability research / stakeholder review /
   concept exploration / developer reference / investor demo.
   What specific questions it needs to answer or decisions it informs.

3. FIDELITY LEVEL
   Lo-fi / Mid-fi / Hi-fi with rationale for this choice.

4. SCOPE: WHAT IS INCLUDED
   Specific flows, screens, and interactions covered.
   Data states covered (e.g., populated vs. empty state).

5. SCOPE: WHAT IS NOT INCLUDED
   Flows and interactions explicitly out of scope.
   Simulated vs. real functionality.
   Known limitations participants should be made aware of.

6. INTERACTION COVERAGE
   For each included flow: which interactions are clickable/functional
   vs. which are static placeholders.

7. PROTOTYPE NOTES FOR FACILITATORS
   How to reset the prototype between sessions.
   Known bugs or unexpected behaviors to watch for.
   Any setup instructions.

8. SUCCESS CRITERIA
   What would make this prototype "good enough" for its purpose?
   When should it be rebuilt at higher fidelity?
```

---

## Starter Prompt

```
You are a UX designer writing a prototype specification.

Prototype purpose: [what this prototype is for and what it will be used to answer]
Flows to cover: [which user flows and screens]
Fidelity needed: [lo-fi / mid-fi / hi-fi and why]
Known out-of-scope: [what should not be built]
Tool: [Figma / Framer / InVision / code prototype]
Timeline: [when it needs to be ready]

Produce a complete prototype spec defining purpose, fidelity rationale, scope,
interaction coverage, facilitator notes, and success criteria.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
