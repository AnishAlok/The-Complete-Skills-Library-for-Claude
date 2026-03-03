# adr-architecture-decision.md

> **Skill:** Produces an Architecture Decision Record (ADR) that documents a single significant architectural choice, the context that drove it, the alternatives considered, and the consequences accepted.

---

## TLDR

An Architecture Decision Record is a short, focused document that captures one significant architectural decision: the context that made it necessary, the options that were considered, what was decided, and what consequences follow from that decision. ADRs are the institutional memory of an engineering organization's architectural choices. Used whenever a decision is made that will be hard to change and that future engineers will need to understand.

---

## Topic Explanation

### Why ADRs Matter

Every codebase accumulates decisions. Most are captured nowhere. A future engineer encountering a pattern they don't understand has three choices: ask someone (if there is anyone left who knows), reverse-engineer the intent from the code, or change it without understanding why it was done that way.

ADRs solve this by capturing decisions at the time they are made, when context is fresh. The goal is not to justify every micro-decision but to capture the decisions that:
- Were not obvious and had real alternatives
- Will be hard to change later
- Future engineers will encounter and wonder about
- Represent significant tradeoffs

### The Michael Nygard Format

The most widely used ADR format was defined by Michael Nygard in 2011. It has five sections:

**Title:** Short noun phrase. "Use PostgreSQL as the primary database."
**Status:** Proposed / Accepted / Deprecated / Superseded by [ADR number]
**Context:** The situation that makes this decision necessary. What forces are at play?
**Decision:** What was decided. Written as an active voice statement.
**Consequences:** What becomes easier and what becomes harder as a result of this decision. Both positive and negative.

The discipline of the format: every ADR should be completable in one page. If it requires multiple pages, the decision is probably multiple decisions and should be split.

### Immutability and Superseding

ADRs are immutable records of decisions made at a specific point in time. When a decision changes, the old ADR is marked "Superseded by ADR-[number]" and a new ADR documents the new decision with its own context and consequences.

This immutability is what makes ADRs valuable as a historical record. An ADR log that is edited in place loses the history of how thinking evolved.

---

## When to Use This Skill

Use when:
- A significant architectural decision must be made and documented
- The team is choosing between multiple viable approaches with real tradeoffs
- A decision once made will be hard to change without significant rework
- The reasoning behind an existing decision has been lost and should be reconstructed and documented

---

## Dos

- **Do write the ADR at decision time, not retrospectively.** Context is freshest immediately after the decision is made. Retrospective ADRs are better than nothing but less accurate.
- **Do document the options not chosen.** The rejected alternatives are as important as the accepted decision.
- **Do include negative consequences.** An ADR with only positive consequences is probably not honest. Every architectural decision involves tradeoffs.
- **Do number ADRs sequentially.** ADR-001, ADR-002, etc. This makes reference and superseding unambiguous.
- **Do keep each ADR to one decision.** An ADR covering three decisions is three ADRs trying to be one.

---

## Donts

- **Dont write ADRs for obvious decisions.** "Use Git for version control" does not need an ADR. A decision only needs an ADR if a reasonable engineer might ask "why did they do it this way?"
- **Dont edit accepted ADRs.** Mark them superseded and write a new one. The history matters.
- **Dont let the ADR become a lengthy design document.** Technical specs cover full designs. ADRs cover single decisions. If it is getting long, it is probably a tech spec or should be split.

---

## Output Format

```
# ADR-[number]: [Title - short noun phrase]

**Date:** [YYYY-MM-DD]
**Status:** [Proposed | Accepted | Deprecated | Superseded by ADR-XXX]
**Deciders:** [Names of people involved in the decision]
**Technical area:** [Database | API | Architecture | Infrastructure | Security | etc.]

---

## Context

[The situation that made this decision necessary. What forces are at play?
What constraints exist? What is the problem being solved?
Write this as if explaining to a future engineer who was not present.]

## Decision Drivers

- [Key factor 1 that influenced the decision]
- [Key factor 2]
- [Key factor 3]

## Considered Options

1. [Option A - what it is and key properties]
2. [Option B - what it is and key properties]
3. [Option C - what it is and key properties]

## Decision Outcome

**Chosen option:** [Option X]

**Rationale:** [Why this option was selected over the alternatives. Be specific.]

## Pros and Cons of Each Option

### Option A: [Name]
- Pro: [advantage]
- Pro: [advantage]
- Con: [disadvantage]
- Con: [disadvantage]

### Option B: [Name]
- Pro: [advantage]
- Con: [disadvantage]

### Option C: [Name]
- Pro: [advantage]
- Con: [disadvantage]

## Consequences

**Positive consequences:**
- [What becomes easier as a result of this decision]

**Negative consequences / tradeoffs accepted:**
- [What becomes harder or more constrained]

**Neutral consequences:**
- [Notable side effects that are neither clearly positive nor negative]

## Links

- [Related ADR-XXX: brief description of relationship]
- [Technical spec reference]
- [External documentation]
```

---

## Starter Prompt

```
You are a senior engineer writing an Architecture Decision Record.

Decision number: [ADR-XXX]
What was decided: [the decision in one sentence]
Context: [the situation and forces that made this decision necessary]
Options considered: [the alternatives that were evaluated]
Why the chosen option was selected: [the rationale]
Consequences: [both positive and negative effects of this decision]
Related decisions: [any ADRs this relates to or supersedes]

Please produce a complete ADR in the Nygard format including:
1. Clear title as a short noun phrase
2. Context explaining the situation to a future engineer
3. All options considered with pros and cons for each
4. Decision outcome with specific rationale
5. Both positive and negative consequences explicitly stated
6. Links to related decisions

The negative consequences section must be honest - every architectural decision
has tradeoffs. Flag if an ADR appears to document only benefits with no acknowledged costs.
```

---

## Related Skills

| Use This Alongside | Why |
|---|---|
| `technical-spec.md` | Tech specs reference ADRs for key decisions |
| `system-design-doc.md` | System designs are supported by a portfolio of ADRs |

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
