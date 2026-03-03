# component-library-guide.md

> **Skill:** Produces a component library guide that helps designers and engineers navigate, understand, and contribute to the component library effectively.

---

## TLDR

A component library guide is the meta-documentation of a design system: it explains how the library is organized, how to find components, how to use them correctly, and how to contribute new components. While individual component docs cover single components, the library guide covers the library as a system. Used for team onboarding and governance.

---

## Topic Explanation

### What a Component Library Guide Is Not

A component library guide is not a collection of component documentation. That is the component documentation itself. The library guide answers meta-questions: how is the library organized? What is the contribution process? How do we decide whether something is a component? What does the component lifecycle look like?

### Component Lifecycle

Every design system needs a defined component lifecycle to prevent both premature standardization (making a component official before it is ready) and indefinite gray areas (components that live forever in "experimental" limbo).

A standard component lifecycle:
1. **Proposed:** A need has been identified. Research is being done.
2. **In progress:** The component is being designed and developed.
3. **Beta:** Available for use but not yet stable. API may change.
4. **Stable:** Officially supported. Breaking changes require migration notes.
5. **Deprecated:** No longer recommended. Will be removed in a future version.
6. **Removed:** No longer available.

### The Contribution Process

Open contribution models (any designer or engineer can propose components) create more buy-in and surface more needs. They also create more governance overhead. Contribution documentation must clearly describe: how to propose a component, what review it goes through, who approves it, and what standard it must meet to be included.

---

## Output Format

```
1. WHAT IS THIS LIBRARY
   Purpose of the component library.
   Relationship to the broader design system.
   Who owns and maintains it.

2. HOW THE LIBRARY IS ORGANIZED
   Organization principle: by type, by category, by product area.
   Navigation guide: how to find what you need.

3. COMPONENT LIFECYCLE
   All lifecycle stages with definitions.
   How to tell what lifecycle stage a component is in.
   Guidance for using components in each stage.

4. HOW TO USE COMPONENTS IN DESIGN
   Setup: how to connect the library in Figma or equivalent.
   Using components: instances, detaching, overrides.
   What can be customized vs. what must not be changed.

5. HOW TO USE COMPONENTS IN CODE
   Installation and import.
   Where to find API documentation.
   Versioning and update process.

6. CONTRIBUTION PROCESS
   How to propose a new component.
   What information is required.
   The review and approval process.
   The standard a component must meet to be included.

7. GOVERNANCE
   Who makes decisions about the library.
   How to raise issues or request changes.
   Breaking change policy.

8. CHANGELOG
   Major version history.
   How to subscribe to updates.
```

---

## Starter Prompt

```
You are a design systems lead writing a component library guide.

Library scope: [what components are in the library]
Teams using it: [design and engineering teams]
Organization principle: [how the library is currently organized]
Contribution model: [open / governed / internal only]
Tech stack: [what framework the code components are built in]
Design tool: [Figma / Sketch / etc.]

Produce a complete component library guide covering library organization,
lifecycle stages, usage instructions for designers and engineers,
contribution process, and governance model.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
