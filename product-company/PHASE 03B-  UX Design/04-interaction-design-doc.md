# interaction-design-doc.md

> **Skill:** Documents interaction patterns, micro-interactions, and behavior logic for a product feature, providing engineering and design with a shared reference for how the UI responds to user actions.

---

## TLDR

An interaction design document captures the logic of how an interface behaves in response to user actions: what happens when a user clicks, hovers, swipes, types, or triggers a state change. It bridges the gap between static design files and live behavior, translating visual designs into behavioral specifications.

---

## Topic Explanation

### What Interaction Design Documentation Covers

Interaction design documentation is specifically about behavior over time. Static design files show how an interface looks. Interaction design docs describe how it moves, responds, and changes. Key dimensions:

**Input handling:** How the system responds to clicks, taps, keyboard input, gestures, voice.
**State transitions:** What triggers a state change and how the transition occurs.
**Feedback timing:** When feedback is immediate, when it is delayed, and how delay is communicated.
**Error and recovery:** How errors interrupt the interaction and how users recover.
**Micro-interactions:** Small, contained interactions that handle a single task (Dan Saffer's definition): a trigger, rules, feedback, and loops/modes.

### The Four Parts of a Micro-Interaction (Dan Saffer)

**Trigger:** What initiates the interaction. User-triggered (click, swipe) or system-triggered (new message arrives).
**Rules:** What happens when the trigger fires. The logic of the interaction.
**Feedback:** How the system communicates the interaction to the user. Visual, auditory, or haptic.
**Loops and modes:** Does the interaction repeat? Are there different modes depending on context?

Documenting micro-interactions in this four-part structure ensures completeness.

---

## Output Format

```
1. FEATURE CONTEXT
   What feature or flow this document covers.
   Design file reference.

2. INTERACTION INVENTORY
   List of all interactions covered in this document.

3. INTERACTION SPECIFICATIONS
   For each interaction:
   - Interaction name
   - Trigger: what initiates it
   - Rules: the logic of what happens
   - Feedback: how the user is informed
   - Timing: duration of transitions, delays, timeouts
   - Edge cases: what if the interaction fails or is interrupted
   - Loops/modes: repetition or modal behavior

4. STATE TRANSITION DIAGRAM
   Visual or text-based map of all states and the interactions that transition between them.

5. TIMING AND ANIMATION REFERENCE
   Transition durations and easing references.
   Link to motion design spec for standard values.

6. EDGE CASE HANDLING
   Offline behavior.
   Slow network behavior.
   Simultaneous action handling.
   Interrupted interactions.
```

---

## Starter Prompt

```
You are an interaction designer documenting interaction patterns for a product feature.

Feature: [what feature or flow is being documented]
User actions to document: [the interactions to specify]
Key states: [the states the feature can be in]
Known edge cases: [problematic scenarios to address]

Produce a complete interaction design document using the four-part micro-interaction
structure (trigger, rules, feedback, loops) for each interaction.
Include a state transition overview and edge case handling.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
