# sql-query-doc.md

> **Skill:** Produces SQL query documentation that explains the purpose, logic, inputs, outputs, performance considerations, and usage guidance for complex or reusable SQL queries.

---

## TLDR

SQL query documentation makes complex queries understandable and maintainable: it explains what the query does, why it is written the way it is, what the inputs and outputs are, and how to use it correctly. Used for queries that are complex, widely used, critical to business reporting, or likely to be maintained by others.

---

## Topic Explanation

### When SQL Queries Need Documentation

Not every SQL query needs documentation. A simple `SELECT * FROM users WHERE plan_type = 'pro'` is self-explanatory. Documentation is warranted when:
- The query involves complex logic (window functions, recursive CTEs, multi-step transformations)
- The query is the source of a critical business metric
- The query contains non-obvious logic that could be misunderstood by a future maintainer
- The query has performance implications that require specific execution contexts
- The query is shared and used by multiple analysts

### Common SQL Documentation Failures

**Missing business context:** "This query returns the monthly cohort retention table" is not sufficient. A maintainer needs to understand: what is included, what is excluded, how "active" is defined, and what business decision this enables.

**Undocumented business rules in WHERE clauses:** A `WHERE status != 'internal_test'` that filters test accounts is a business rule. Without documentation, a maintainer might not know it is intentional.

**No performance notes:** A query that must be run on specific partitions to avoid full-table scans needs that documented. Without it, a well-meaning engineer will run it on an unpartitioned table and time out.

**No output schema description:** A complex query that returns 15 columns needs each column explained.

---

## Output Format

```
1. QUERY DOCUMENTATION HEADER
   Query name, author, date created, last modified, purpose.
   Data warehouse: BigQuery / Snowflake / Redshift / etc.
   Reviewed by.

2. BUSINESS CONTEXT
   What business question does this query answer?
   What decisions or reports does it power?
   Who uses it?

3. QUERY OVERVIEW
   What the query does in plain language.
   Key transformation steps.

4. INPUTS
   Source tables:
   | Table | Schema | Description | Key columns used |

   Parameters or variables (if any):
   | Parameter | Type | Description | Default |

   Dependencies: other queries or models that must run first.

5. OUTPUT SCHEMA
   | Column name | Type | Description | Example value |

6. KEY LOGIC EXPLANATION
   For each complex or non-obvious section:
   - What the section does
   - Why it is written this way
   - The business rule it implements

7. KNOWN LIMITATIONS AND EDGE CASES
   Data quality issues to be aware of.
   Intentional exclusions.
   Known gaps or imperfections.

8. PERFORMANCE NOTES
   Expected runtime and row count at current data volume.
   Required partitions or filters for acceptable performance.
   Indexes or clustering columns used.
   When NOT to run (e.g., during peak warehouse load).

9. THE QUERY (fully commented)

   [Annotated SQL with inline comments explaining each CTE and complex section]

10. USAGE EXAMPLES
    Common use cases with example parameter values.
    How to modify for common variants.
```

---

## Starter Prompt

```
You are a data engineer documenting a SQL query.

Query purpose: [what business question it answers]
Source tables: [tables and schemas used]
Key logic: [the important transformations and business rules]
Output: [what the query returns]
Performance considerations: [any known performance requirements or limitations]
Edge cases: [known data quality issues or intentional exclusions]
Users: [who uses this query]

Produce complete SQL query documentation including business context,
input/output schema, logic explanation, and the annotated query.
Every non-obvious WHERE clause and business rule must be documented.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
