# design-system-doc.md

> **Skill:** Produces comprehensive design system component documentation covering anatomy, variants, usage guidelines, do/dont examples, accessibility, and code integration for a design system component library.

---

## TLDR

Design system documentation is the contract between the design system and its consumers: designers and engineers who need to know when to use a component, how to use it correctly, what variants exist, and what behavior to expect. This skill produces documentation for a single design system component or a full design system section, following the structure used by best-in-class design systems (Material Design, Atlassian Design System, Carbon, Polaris).

---

## Topic Explanation

### Why Design System Documentation Fails

Most design systems have documentation. Few have documentation that gets used. The difference between documentation that collects dust and documentation that actually prevents misuse:

**Specificity:** "Use the primary button for the main action" is not enough. "Use exactly one primary button per page or modal. It represents the single most important action. When there is no obvious primary action, use secondary buttons for all actions" is specific enough to guide decisions.

**Do and dont examples:** Abstract guidelines are less effective than concrete visual examples of correct and incorrect usage. "Dont use primary buttons for destructive actions" paired with a red/green comparison image is far more memorable than the guideline alone.

**Rationale:** Consumers who understand why a guideline exists are more likely to follow it and less likely to look for loopholes. "Dont stack more than three notifications because users in testing stopped reading after two" is more persuasive than "Dont stack more than three notifications."

**Completeness:** Documentation that covers only the happy path forces consumers to make decisions the design system should be making for them.

### Anatomy Documentation

Every component's documentation should begin with an anatomy section that labels every element of the component. Anatomy serves two purposes:

1. It creates a shared vocabulary for the team to use when discussing the component. "The leading icon," "the helper text," and "the label" are unambiguous when the anatomy defines them.

2. It makes explicit which elements are required, optional, and conditional. This prevents implementations that omit required elements or misplace optional ones.

### Variant Documentation

Variants are the officially supported configurations of a component. Every variant that is not documented is a variant that will be invented by someone who needed something the design system did not provide. Documenting variants (and documenting what is NOT a variant) prevents design drift.

For each variant, document:
- When to use it vs. other variants
- How it differs from the default
- What cannot be changed within this variant
- What should not be combined with this variant

---

## When to Use This Skill

Use when:
- Adding a new component to the design system that needs to be documented for team use
- An existing component is being used inconsistently and needs clear documentation to standardize usage
- Building a design system documentation site or internal wiki
- Onboarding new designers or engineers to the design system

---

## Dos

- **Do write from the perspective of a first-time consumer.** Someone who has never seen this component should be able to read the documentation and use it correctly.
- **Do document what NOT to do with equal rigor to what TO do.** Donts are often the more valuable guidance because they prevent the most common misuse patterns.
- **Do include real product examples.** Showing the component in actual product context is more useful than abstract examples.
- **Do keep documentation in sync with the component.** Documentation that lags the component actively misleads consumers. Documentation updates should be part of every component change.

---

## Output Format

```
1. COMPONENT OVERVIEW
   What this component is, what problem it solves, and its role in the system.
   When to use this component vs. similar alternatives.

2. LIVE EXAMPLE
   Reference to interactive demo or design file showing the component.

3. ANATOMY
   Labeled diagram of the component's elements.
   For each element: name, required/optional, description.

4. VARIANTS
   For each variant:
   - Variant name and visual reference
   - When to use
   - Key differences from default
   - Restrictions: what cannot be changed in this variant

5. PROPERTIES AND PROPS
   All configurable properties with: name, type, default value, description.

6. USAGE GUIDELINES
   When to use this component.
   When NOT to use this component (use X instead).
   How many can appear on a page simultaneously.
   How it combines with other components.

7. DO AND DONT EXAMPLES
   Paired visual examples for each major guideline.
   Do: correct usage with annotation.
   Dont: incorrect usage with annotation explaining why.

8. STATES
   All supported states with visual references.
   Behavior description for each state.

9. CONTENT GUIDELINES
   Character limits for all text elements.
   Writing guidance (tone, length, format).
   Required vs. optional copy.

10. ACCESSIBILITY
    ARIA role and required attributes.
    Keyboard interaction pattern.
    Screen reader behavior.
    Color contrast tokens used.
    Touch target size if mobile.

11. RESPONSIVE BEHAVIOR
    Behavior at each breakpoint.
    Any variant changes at mobile sizes.

12. CODE USAGE
    Import statement.
    Basic usage example.
    Prop examples for key variants.
    Reference to full API documentation.

13. CHANGELOG
    Version history for significant changes.
    Migration notes for breaking changes.
```

---

## Starter Prompt

```
You are a design system specialist writing documentation for a design system component.

Component name: [name of the component]
Component description: [what it is and what it does]
Variants: [list all supported variants]
Properties/props: [configurable properties and their types]
Usage context: [where and how it is used in the product]
Common misuse patterns: [ways the component is frequently used incorrectly]
Accessibility requirements: [known ARIA and keyboard requirements]
Platform: [web / iOS / Android / cross-platform]

Please produce complete design system documentation including:
1. Component overview with when-to-use guidance
2. Anatomy with all elements labeled and required/optional status
3. All variants with when-to-use guidance
4. Usage guidelines with explicit do and dont examples
5. All states documented
6. Content guidelines with character limits
7. Accessibility section (ARIA, keyboard, screen reader)
8. Code usage examples

For each dont guideline, explain why the pattern is problematic.
Document what is NOT a supported variant or usage to prevent design drift.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `design-tokens-doc.md` | Component documentation references design tokens |
| `component-library-guide.md` | Component docs are organized within the library guide |
| `design-spec.md` | Component specs inform and become design system documentation |
| `wcag-compliance-report.md` | Accessibility section should reflect WCAG compliance status |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
