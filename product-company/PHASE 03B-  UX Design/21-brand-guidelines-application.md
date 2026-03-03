# brand-guidelines-application.md

> **Skill:** Documents how to apply brand identity guidelines to product UI, translating marketing brand standards into usable product design tokens, component styles, and usage rules.

---

## TLDR

Brand guidelines are written for marketing. Product UI has different constraints: interactive states, accessibility requirements, information density, and functional clarity that marketing materials do not face. This skill produces documentation translating brand identity into product design decisions: which brand elements translate directly, which must be adapted, and which must be overridden in the interest of usability and accessibility.

---

## Topic Explanation

### Why Brand Guidelines Cannot Be Applied Directly to Product UI

Brand guidelines are designed for marketing contexts: large typography, controlled layouts, print and static digital media. Product UI faces constraints brand guidelines rarely address:

**Accessibility:** Brand colors are frequently chosen for aesthetics, not contrast. A brand's signature color may fail WCAG AA contrast requirements for text. The product design system must either adapt the color or override it for UI text.

**Interactivity:** Brand guidelines define colors for static elements. Product UI needs hover, focus, active, and disabled states. These states must be derived from brand colors in a way that maintains brand identity while communicating interaction state clearly.

**Information density:** Brand guidelines often assume generous whitespace. Product UI frequently requires dense information layouts that brand spacing guidelines would make unusable.

**Dark mode:** Brand guidelines rarely address dark mode. The product design system must derive dark mode values from brand colors.

### What "On-Brand" Means in Product UI

On-brand product UI is not literal application of brand guidelines. It is the product feeling like it belongs to the same family as the brand, while making appropriate adaptations for usability, accessibility, and interactivity. The brand guidelines define the identity; the product design system decides how to express that identity within product constraints.

---

## Output Format

```
1. BRAND IDENTITY SUMMARY
   Core brand values as they apply to product design.
   The emotional qualities the product UI should express.

2. COLOR APPLICATION
   Primary brand color: product UI applications and token mapping.
   Secondary brand colors: when and how used in product.
   Accessibility adaptations: where brand colors must be modified for contrast.
   Colors not used in product UI (and why).
   Derived UI colors: hover, focus, active states derived from brand palette.

3. TYPOGRAPHY APPLICATION
   Brand typeface(s) and their product UI applications.
   Any typeface substitutions for performance or licensing reasons.
   Type scale derived from brand typography.
   Functional type styles: labels, body, captions.

4. ICONOGRAPHY AND ILLUSTRATION STYLE
   Icon style consistent with brand.
   Illustration usage rules: when used and at what scale.
   Photography style if used in product.

5. LOGO AND BRAND MARK USAGE
   Where the logo appears in product UI.
   Minimum size and clear space requirements.
   Contexts where the logo should not appear.

6. BRAND ELEMENTS THAT DO NOT APPLY TO PRODUCT UI
   Brand guidelines that are intentionally not followed in product.
   Rationale: accessibility, usability, or technical constraints.

7. WHEN IN DOUBT ESCALATION
   How to resolve uncertainty about brand application.
   Who approves exceptions.
   How approved exceptions get documented.
```

---

## Starter Prompt

```
You are a product designer translating brand guidelines into product design rules.

Brand guidelines overview: [the key brand identity elements]
Brand color palette: [the brand colors and their values]
Brand typography: [the brand typefaces]
Product accessibility requirements: [WCAG AA or other standard]
Known conflicts: [brand elements that seem to conflict with usability or accessibility]
Product platform: [web / iOS / Android]

Produce a brand guidelines application document covering color, typography,
iconography, and logo usage for product UI.
Explicitly document where the brand must be adapted for accessibility
and provide the adapted values.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
