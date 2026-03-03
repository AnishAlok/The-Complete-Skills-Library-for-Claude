# database-schema-doc.md

> **Skill:** Produces database schema documentation covering table definitions, column descriptions, constraints, indexes, relationships, and the design rationale for a relational or document database.

---

## TLDR

Database schema documentation is the reference for understanding how data is structured, why it is structured that way, and how tables relate to each other. Beyond the schema itself, it documents design decisions, normalization choices, index strategy, and migration history. Used by engineers, data analysts, and anyone who needs to query or modify the data model.

---

## Topic Explanation

### Why Schema Documentation Exists Separately from Code

The schema lives in migrations and database introspection tools. What those do not capture: why columns are named as they are, what business concept a table represents, why certain normalization decisions were made, and why specific indexes were added.

Schema documentation closes the gap between "what is in the database" and "what it means and why it was designed this way."

### Normalization Levels

**1NF (First Normal Form):** No repeating groups. Each column contains atomic values. Each row is unique.
**2NF (Second Normal Form):** 1NF + no partial dependencies on composite keys.
**3NF (Third Normal Form):** 2NF + no transitive dependencies. Non-key columns depend only on the primary key.
**Denormalization:** Intentional deviation from 3NF for performance. Common in reporting tables, caches, and high-read systems. Should be documented and justified.

### Index Strategy Documentation

Indexes should be documented with the specific query patterns they support. An index with no documented query pattern is a candidate for removal. Documenting: index name, columns, type (BTree, GIN, etc.), the query it supports, and the cardinality it relies on.

---

## Output Format

```
1. SCHEMA OVERVIEW
   Database type and version.
   High-level entity model: the main domain objects and their relationships.
   Naming conventions used.
   Key design decisions (normalization level, UUID vs. auto-increment, soft deletes, etc.)

2. ENTITY RELATIONSHIP SUMMARY
   Text or ASCII diagram of tables and their relationships.
   Cardinalities: one-to-one, one-to-many, many-to-many.

3. TABLE DOCUMENTATION
   For each table:
   - Table name and purpose
   - Business concept it represents

   COLUMNS:
   | Column | Type | Nullable | Default | Constraints | Description |

   INDEXES:
   | Index name | Columns | Type | Purpose / Query supported |

   FOREIGN KEYS:
   | FK name | Column | References | On delete behavior |

   NOTES:
   Design decisions, denormalization choices, soft delete strategy.

4. MANY-TO-MANY JUNCTION TABLES
   Purpose of each junction table.
   Additional columns beyond the foreign key pair.

5. ENUM TYPES AND LOOKUP TABLES
   All enum values with descriptions.
   Lookup table contents and update policy.

6. MIGRATION HISTORY SUMMARY
   Major schema changes with version/date and rationale.
   Breaking changes and how they were handled.

7. QUERY PATTERNS
   Common queries and the indexes that support them.
   N+1 risks and how they are mitigated.

8. DATA GOVERNANCE
   PII columns (for compliance documentation).
   Retention policy per table.
   Access controls.
```

---

## Starter Prompt

```
You are a senior engineer writing database schema documentation.

Database type: [PostgreSQL / MySQL / MongoDB / etc.]
Domain: [what business domain the schema models]
Tables to document: [list of tables with their purpose]
Key relationships: [the important relationships between tables]
Design decisions: [normalization approach, UUID vs. serial, soft deletes, etc.]
Index strategy: [key indexes and what queries they support]
PII fields: [columns containing personal data]

Produce complete schema documentation including entity relationship summary,
full table documentation with column descriptions and constraints,
index documentation with supported queries, and migration history.
Flag any table without a primary key, any column without a description,
and any foreign key without documented cascade behavior.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
