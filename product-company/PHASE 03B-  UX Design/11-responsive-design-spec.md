# responsive-design-spec.md

> **Skill:** Documents breakpoints, layout grid behavior, component adaptation rules, and content priority changes across screen sizes for a responsive design system or feature.

---

## TLDR

A responsive design spec defines how a product's layout and components adapt across different screen sizes. It specifies breakpoints, grid systems, component behavior at each breakpoint, and the content priority rules that determine what shows, hides, or reflows at smaller screens. Used by designers and engineers to implement consistent responsive behavior without guessing.

---

## Topic Explanation

### Breakpoints vs. Fluid vs. Adaptive

Three approaches to responsive design, often combined:

**Fluid design:** Layout elements scale proportionally as the viewport size changes. Width is expressed in percentages. The layout adapts continuously between breakpoints.

**Adaptive design:** Distinct fixed layouts for specific viewport sizes. The layout snaps from one configuration to another at defined breakpoints.

**Responsive design:** The combination of fluid and adaptive. Fluid scaling within ranges, adaptive layout changes at breakpoints. The standard modern approach.

A responsive design spec primarily documents the adaptive (breakpoint-based) decisions because those are the design decisions. Fluid behavior within a breakpoint range follows from the grid definition.

### Content Priority in Responsive Design

Responsive design is not just about layout rearrangement. It is about content priority decisions. At smaller screen sizes, some content must be hidden, condensed, or deprioritized. These decisions should be made deliberately by design, not incidentally by whoever writes the CSS.

Content priority documentation answers:
- What is visible at all breakpoints vs. only at wider screens?
- When navigation changes from a full menu to a hamburger, what is in each?
- Which table columns are visible on mobile vs. desktop?
- What image crops are used at each breakpoint?

---

## Output Format

```
1. BREAKPOINT DEFINITIONS
   Table of breakpoints with names and pixel ranges:
   xs (0 to 599px), sm (600 to 899px), md (900 to 1199px),
   lg (1200 to 1535px), xl (1536px+)
   (Adjust to match design system breakpoints)

2. GRID SYSTEM
   Number of columns at each breakpoint.
   Gutter width at each breakpoint.
   Margin/padding at each breakpoint.
   Maximum content width.

3. LAYOUT BEHAVIOR BY BREAKPOINT
   For each key layout pattern:
   - Default (desktop) layout description
   - Tablet adaptation
   - Mobile adaptation
   With visual reference frames.

4. COMPONENT ADAPTATION RULES
   For each component with responsive behavior:
   - Default (desktop) behavior
   - Changes at tablet breakpoint
   - Changes at mobile breakpoint
   - Components that are hidden at specific breakpoints

5. CONTENT PRIORITY RULES
   What is visible at all breakpoints.
   What is hidden below specific breakpoints.
   Navigation transformation rules (full menu to hamburger, etc.).
   Table/data display adaptation rules.
   Image and media behavior.

6. TYPOGRAPHY RESPONSIVE RULES
   Font size adjustments by breakpoint.
   Heading scale at each breakpoint.

7. TESTING CHECKLIST
   Required devices/viewports to test.
   Common issues to verify.
```

---

## Starter Prompt

```
You are a UX designer documenting responsive design specifications.

Product or feature: [what is being specified]
Current breakpoints: [the breakpoints in use or to define]
Grid system: [columns, gutters, margins at each breakpoint]
Key layouts: [the main page and component layouts to specify]
Navigation approach: [how navigation changes at smaller sizes]
Content priority rules: [what hides or changes at smaller sizes]

Produce a complete responsive design spec including breakpoint definitions,
grid system, layout behavior, component adaptation rules, and content priority decisions.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
