# data-model-doc.md

> **Skill:** Produces a data model and entity-relationship documentation that describes the business domain objects, their attributes, relationships, and the rules governing the data.

---

## TLDR

A data model document describes the domain entities that a system manages: what they are, their properties, how they relate to each other, and the business rules that govern them. It bridges the business domain (conceptual model) and the database schema (physical model). Used by engineers, product managers, and data analysts to understand the core data structures of a system.

---

## Topic Explanation

### Three Levels of Data Modeling

**Conceptual model:** Business-level. What are the main entities and their relationships? No technical detail. Appropriate for PMs and business stakeholders.

**Logical model:** Detailed entity-relationship model. Entities, attributes, relationships, cardinalities. Technology-agnostic. Appropriate for engineers designing systems.

**Physical model:** The actual database schema. Tables, columns, data types, indexes. Derived from the logical model with database-specific optimizations.

A data model document typically covers the conceptual and logical levels. The physical level is covered by `database-schema-doc.md`.

### Domain-Driven Design Vocabulary

DDD (Domain-Driven Design) provides useful vocabulary for data modeling:

**Entity:** An object with a unique identity that persists over time. A user, an order, an organization.

**Value Object:** An object without identity, defined by its attributes. A money amount, an address. Two value objects with the same attributes are equal.

**Aggregate:** A cluster of entities and value objects with a root entity that enforces invariants. An Order is an aggregate root with OrderLineItems as children.

**Repository:** The pattern for accessing aggregates from storage.

### Invariants and Business Rules

Every entity has invariants: business rules that must always be true. An order total must equal the sum of its line items. A user cannot have two active subscriptions. A payroll run cannot be approved if any pay stubs have failed calculations.

Documenting invariants in the data model document prevents engineers from implementing storage logic that violates business rules and helps teams understand where validation logic should live.

---

## Output Format

```
1. DOMAIN OVERVIEW
   The business domain being modeled.
   Core entities and their relationships at a conceptual level.
   Entity-relationship diagram (text-based or reference to diagram).

2. ENTITY DEFINITIONS
   For each entity:
   - Name and definition (what this entity represents in the business domain)
   - DDD classification: Entity / Value Object / Aggregate root
   - Unique identifier
   - Core attributes with business meaning
   - Lifecycle: how entities are created, updated, and terminated
   - Invariants: business rules that must always be true

3. RELATIONSHIP DOCUMENTATION
   For each significant relationship:
   - Entities involved
   - Cardinality: one-to-one / one-to-many / many-to-many
   - Directionality
   - Business meaning: what the relationship represents
   - Referential integrity rules: what happens when one entity is deleted

4. DOMAIN EVENTS
   Events that occur in the domain that other systems care about.
   What triggers each event.
   What data the event carries.

5. BUSINESS RULES
   Validation rules: constraints on attribute values.
   Derivation rules: calculated fields and how they are computed.
   Authorization rules: who can create/read/update/delete each entity.

6. GLOSSARY
   Domain terms that have specific meanings in this model.
   Terms that might be confused with each other.

7. MODEL EVOLUTION
   How the model has changed significantly.
   Migration considerations for breaking changes.
```

---

## Starter Prompt

```
You are a senior engineer writing a data model document.

Business domain: [what business concepts the model represents]
Core entities: [the main domain objects]
Relationships: [how entities relate to each other]
Business rules and invariants: [rules that must always be true]
Domain events: [significant events in the domain]
Current model gaps or pain points: [any known model problems]

Produce a complete data model document covering all three conceptual levels.
For each entity: define its business meaning, attributes, lifecycle, and invariants.
Document every business rule explicitly.
Flag any entity whose invariants may be difficult to enforce at the data layer.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
