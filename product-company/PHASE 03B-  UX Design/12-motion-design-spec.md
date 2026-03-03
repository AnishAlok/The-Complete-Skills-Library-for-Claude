# motion-design-spec.md

> **Skill:** Documents animation principles, timing standards, easing functions, and specific motion specifications for UI transitions and micro-interactions.

---

## TLDR

A motion design spec defines the principles and standards for all animation in a product: how and why things move, what timing and easing values to use, and the specific motion behaviors for key UI patterns. It prevents animations that feel inconsistent, arbitrary, or gratuitously decorative by grounding motion in purpose and establishing system-wide standards.

---

## Topic Explanation

### The Four Functions of Motion in UI

Motion in UI should serve one of four purposes. Motion that serves none of them is decorative at best and distracting at worst:

**Orientation:** Motion communicates where something came from and where it went, preserving the user's spatial model. A panel sliding in from the right establishes that it came from somewhere to the right.

**Feedback:** Motion confirms that an action was received and processed. A button that briefly presses in provides confirmation without a separate message.

**Transition:** Motion bridges states, making the relationship between before and after legible. An accordion expanding rather than snapping open communicates that the content was always there.

**Focus:** Motion draws attention to what matters. A notification badge pulsing once indicates there is something new to see.

Motion without purpose should be removed.

### Duration and Easing Standards

**Duration:** UI motion should feel immediate and responsive. Research and practice converge on:
- Micro-interactions and feedback: 100 to 150ms
- Element transitions (appear/disappear): 150 to 250ms
- Layout changes and page transitions: 250 to 400ms
- Complex choreographed motion: up to 500ms

Durations above 500ms feel slow. Durations above 1000ms feel broken.

**Easing:** Easing makes motion feel physical and natural.
- **Ease-in-out:** Used for elements moving within a scene. Starts and ends slowly.
- **Ease-out (deceleration):** Used for elements entering the screen. Starts fast, ends slowly. Natural for objects arriving.
- **Ease-in (acceleration):** Used for elements leaving the screen. Starts slowly, ends fast. Natural for objects departing.
- **Linear:** Only for continuous animations (spinners, progress bars). Feels mechanical for transitions.

---

## Output Format

```
1. MOTION PRINCIPLES
   3 to 5 guiding principles for motion in this product.
   For each: name, description, rationale, example.

2. TIMING STANDARDS
   Standard duration values as tokens.
   Duration token table: name, value, intended use.

3. EASING STANDARDS
   Standard easing functions as tokens.
   Easing table: name, value (cubic-bezier), intended use.

4. REDUCED MOTION
   How the design respects prefers-reduced-motion.
   What changes when reduced motion is enabled.
   Which animations are removed entirely vs. simplified.

5. MOTION PATTERNS BY CATEGORY
   For each UI pattern category (appearing, disappearing, expanding,
   loading, feedback, page transitions):
   - Default motion specification: property, duration, easing
   - Rationale
   - Code/design reference

6. COMPONENT-SPECIFIC MOTION
   For key components with defined motion:
   - Component name
   - Motion description
   - Timing and easing values
   - Reference to design file or code example

7. ANTIPATTERNS
   Motion patterns to avoid in this product.
   Why they are problematic.
```

---

## Starter Prompt

```
You are a motion designer documenting animation standards for a product design system.

Product character: [how the product should feel - e.g., "efficient, professional, clean"]
Key UI patterns: [the main interaction patterns that involve motion]
Platform: [web / iOS / Android / cross-platform]
Existing timing values: [any timing tokens already in use]
Accessibility requirements: [prefers-reduced-motion requirements]

Produce a motion design spec including principles, timing standards as tokens,
easing standards as tokens, reduced motion policy, and motion patterns
for key UI categories.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
