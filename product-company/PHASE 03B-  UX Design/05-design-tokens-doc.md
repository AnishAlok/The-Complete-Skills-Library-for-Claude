# design-tokens-doc.md

> **Skill:** Produces design token definitions, naming conventions, usage guidelines, and integration documentation for a design system's foundational visual values.

---

## TLDR

Design tokens are the named, stored values for all visual design decisions: colors, typography, spacing, shadows, border radii, motion. They create a single source of truth for visual values shared between design tools and code. This skill documents a token system including naming conventions, token hierarchy, usage guidelines, and integration notes.

---

## Topic Explanation

### Token Hierarchy: Global, Alias, Component

Best-practice token systems have three layers:

**Global tokens (primitives):** The full set of raw values in the design system. Colors as a full palette: `color-blue-500: #3B82F6`. Typography scale: `font-size-lg: 18px`. These are all possible values.

**Alias tokens (semantic/decisions):** Named by their intended use, not their value. `color-action-primary: {color-blue-500}`. `font-size-body: {font-size-base}`. These define what global tokens mean in context.

**Component tokens:** Specific to a component. `button-primary-background: {color-action-primary}`. Component tokens reference alias tokens, not globals.

This hierarchy means changing a brand color requires updating one global token. All alias and component tokens that reference it update automatically.

### Token Naming Convention

Token names should communicate: category, context/variant, property, state.

Format: `{category}-{variant}-{property}-{state}`

Examples:
- `color-interactive-primary-hover`
- `spacing-component-padding-sm`
- `typography-heading-font-size`
- `border-radius-component-interactive`

Avoid abbreviations that reduce clarity. `clr-int-pr-hv` is not a usable token name.

---

## Output Format

```
1. TOKEN SYSTEM OVERVIEW
   The three-tier hierarchy: global, alias, component.
   Naming convention with format and examples.
   Tools: where tokens live (Figma Tokens, Style Dictionary, etc.).

2. COLOR TOKENS
   Global palette (all named colors with values).
   Semantic/alias color tokens with references to globals.
   Dark mode alias tokens (if applicable).

3. TYPOGRAPHY TOKENS
   Font family tokens.
   Font size scale with token names.
   Line height and letter spacing tokens.
   Font weight tokens.

4. SPACING TOKENS
   Spacing scale with token names.
   Usage: which tokens for padding, margin, gap.

5. ELEVATION AND SHADOW TOKENS
   Shadow values with token names.
   When to use each elevation level.

6. BORDER RADIUS TOKENS
   Radius values with token names.

7. MOTION TOKENS
   Duration values.
   Easing function values.

8. INTEGRATION GUIDE
   How tokens are exported to code.
   Token format (CSS custom properties, JS, JSON, etc.).
   How to reference tokens in component code.
   How to update tokens and propagate changes.

9. DEPRECATED TOKENS
   Tokens that have been deprecated and their replacements.
```

---

## Starter Prompt

```
You are a design systems engineer documenting a design token system.

Token inventory: [the visual decisions to tokenize: colors, type, spacing, etc.]
Color palette: [the raw color values]
Typography scale: [the type values]
Spacing scale: [the spacing values]
Dark mode: [whether dark mode tokens are needed]
Code integration: [CSS custom properties / JS / platform]

Produce complete design token documentation including the three-tier hierarchy,
naming convention with examples, all token categories with values,
and integration guide for the target platform.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
