# dark-mode-spec.md

> **Skill:** Produces a dark mode design specification documenting color token mappings, elevation reversal logic, component adaptations, and image/media handling for dark mode implementation.

---

## TLDR

A dark mode spec defines how the product's visual design system adapts to dark mode: not a simple color inversion, but a thoughtful remapping of color tokens, elevation logic, and component behavior that maintains usability, contrast, and brand identity in low-light contexts. Used by design and engineering teams to implement dark mode consistently and correctly.

---

## Topic Explanation

### Dark Mode Is Not Color Inversion

The most common dark mode mistake is inverting light-mode colors. This produces technically dark colors but aesthetically and functionally wrong results. Black text on white becomes white text on black, which has higher contrast than intended and causes eye strain. Light shadows become light glows, which makes no physical sense.

Dark mode requires rethinking the color semantics:
- **Backgrounds:** Dark backgrounds should use dark grays, not pure black. Pure black next to white creates too much contrast.
- **Elevation:** In light mode, elevation is communicated with drop shadows (darker than the surface). In dark mode, elevation is communicated with surface lightness (lighter backgrounds are higher). Shadows do not work in dark mode.
- **Color:** Saturated colors used in light mode are often too vibrant in dark mode. Dark mode often uses desaturated or reduced-opacity variants.
- **Text:** Primary text should not be pure white on dark backgrounds. Off-white (#E2E8F0, not #FFFFFF) reduces eye strain.

### Design Token Strategy for Dark Mode

The cleanest dark mode implementation uses semantic design tokens that can be remapped:

**Light mode:** `color-surface-primary: #FFFFFF`
**Dark mode:** `color-surface-primary: #1A1A2E`

The component references `color-surface-primary` in both modes. The token value changes with the mode. No component code needs to change.

This only works if the design system uses semantic tokens (alias tokens) rather than hard-coded color values. A component that hardcodes `color: #1F2937` instead of `color: {color-text-primary}` will not support dark mode without code changes.

---

## Output Format

```
1. DARK MODE PRINCIPLES
   How the product approaches dark mode.
   Key design decisions made (e.g., elevation via lightness not shadows).

2. COLOR TOKEN REMAPPING
   Table: token name / light mode value / dark mode value.
   Covers: surface backgrounds, interactive surfaces, borders, text, icons,
   status colors, brand colors.

3. ELEVATION AND SHADOW ADAPTATION
   How elevation is communicated in dark mode.
   Shadow token values in dark mode.
   Surface lightness scale for elevation levels.

4. COMPONENT-BY-COMPONENT DARK MODE NOTES
   For each component with non-trivial dark mode behavior:
   - What changes in dark mode
   - Any variants that need specific dark mode treatment

5. IMAGE AND MEDIA HANDLING
   How photographs adapt (dimming, replacement, no change).
   How illustrations with light backgrounds adapt.
   SVG icon adaptation (color and opacity changes).

6. IMPLEMENTATION APPROACH
   CSS custom property strategy.
   Media query: prefers-color-scheme.
   Manual toggle: how user preference is stored and applied.
   System default: how the OS preference is respected.

7. TESTING CHECKLIST
   Key checks before shipping dark mode.
   Contrast ratios to verify.
   Components to visually verify.
```

---

## Starter Prompt

```
You are a UX designer writing a dark mode specification.

Current light mode token system: [describe the color tokens or paste values]
Product character in dark mode: [how it should feel - sophisticated, developer-focused, etc.]
Key components to specify: [the main components that need dark mode treatment]
Elevation system: [how elevation currently works in light mode]
Images and illustrations: [types of visual assets that need adaptation]
Implementation platform: [web CSS / iOS / Android / cross-platform]

Produce a complete dark mode spec including color token remapping,
elevation adaptation, component-specific notes, image handling,
and implementation approach.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
