# information-architecture.md

> **Skill:** Produces an information architecture document covering the navigation structure, content hierarchy, labeling system, and IA principles for a product.

---

## TLDR

Information architecture (IA) is the structure and organization of content and functionality in a product. A well-designed IA makes things findable without requiring users to know where to look. This skill produces IA documentation including the navigation hierarchy, labeling principles, findability testing plan, and governance for IA changes.

---

## Topic Explanation

### The Three Key IA Questions

Peter Morville and Louis Rosenfeld's foundational IA framework says users have three questions when navigating:

**"Where am I?"** The IA must communicate location clearly through breadcrumbs, active states, page titles, and consistent wayfinding.

**"What is here?"** The IA must communicate what content is in the current location and its structure.

**"Where can I go?"** The IA must communicate the navigation options available from the current location.

Good IA answers all three questions at every location in the product.

### IA vs. Navigation Design

IA and navigation are related but distinct:
- **IA** is the conceptual structure: how content and features are organized and related.
- **Navigation** is the UI through which users access the IA: the menus, tabs, sidebars, and breadcrumbs.

You can have the same IA implemented with different navigation patterns. IA decisions should be made before navigation UI decisions, not after.

### Labeling Systems

The most technically correct IA can fail because of poor labeling. Labels should:
- Use language users already know (from their mental model and vocabulary, not the product's internal terminology)
- Be distinct from each other (users should not be uncertain which label applies to their need)
- Be consistent in form (all nouns, all verbs, or a consistent mix)
- Be short enough to scan

Card sorting research (`card-sorting-report.md`) and tree testing (`tree-testing-report.md`) are the primary validation methods for IA decisions.

---

## Output Format

```
1. IA PRINCIPLES
   3 to 5 principles that govern IA decisions for this product.
   Example: "Organize by user goal, not by product feature."

2. NAVIGATION HIERARCHY
   The complete IA structure as a tree:
   Level 1: Primary navigation
   Level 2: Secondary navigation within each primary
   Level 3: Tertiary content if applicable
   With page/view title for each node.

3. LABELING SYSTEM
   Labels for all navigation nodes.
   Rationale for key labeling decisions.
   Terms that are deliberately avoided (and what is used instead).

4. CONTENT AND FEATURE INVENTORY
   All product content and features mapped to their IA location.
   Items with multiple possible locations and the decision rationale.

5. WAYFINDING SYSTEM
   Breadcrumb structure and rules.
   Active state behavior in navigation.
   Page title conventions.
   URL structure (if relevant).

6. FINDABILITY APPROACH
   How users with different mental models will find key items.
   Search strategy: where search is available and what it covers.
   Cross-linking strategy for related content.

7. IA CHANGE GOVERNANCE
   How IA changes are proposed and approved.
   When changes require tree testing.
   How IA changes are communicated to users.

8. VALIDATION PLAN
   Tree test tasks planned.
   Card sort questions if IA is evolving.
   Success metrics for IA (findability rate, navigation errors).
```

---

## Starter Prompt

```
You are an information architect documenting the IA for a product.

Product: [what the product does and who uses it]
Current navigation structure: [describe or list current nav if it exists]
Content and features: [all the things users need to find and do]
User mental models: [how users think about organizing these things, from research]
Known IA problems: [current findability issues]
Platform: [web / mobile / both]

Produce a complete IA document including principles, navigation hierarchy,
labeling system, wayfinding approach, and validation plan.
Ground labeling decisions in user mental model research.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
