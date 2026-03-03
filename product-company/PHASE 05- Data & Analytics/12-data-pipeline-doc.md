# data-pipeline-doc.md

> **Skill:** Produces data pipeline documentation covering source-to-destination data flow, transformation logic, schedule, error handling, monitoring, and operational procedures.

---

## TLDR

Data pipeline documentation describes how data moves from source systems to analytical destinations: what data, from where, through what transformations, on what schedule, with what quality checks, and what to do when something goes wrong. Used by data engineers and analysts to understand, maintain, and troubleshoot data pipelines.

---

## Topic Explanation

### The Modern Data Stack

Most data pipelines follow an ELT pattern (Extract, Load, Transform):
1. **Extract:** Pull raw data from source systems (application databases, APIs, SaaS tools)
2. **Load:** Store raw data in the data warehouse without transformation
3. **Transform:** Apply business logic in the warehouse using SQL (dbt, Dataform)

This contrasts with the older ETL pattern where transformation happened before loading. ELT is now dominant because modern cloud warehouses can handle transformation at scale, and keeping raw data enables re-transformation as logic changes.

### Data Quality in Pipelines

Pipelines fail in two ways: complete failures (the job errors and does not run) and silent failures (the job completes but produces incorrect or incomplete data). Complete failures are easier to detect. Silent failures are more dangerous because they feed incorrect data into reports and decisions without triggering alerts.

Data quality checks that run after each pipeline step detect silent failures:
- Row count checks: "table should have at least N rows"
- Freshness checks: "most recent record should be within 24 hours"
- Null rate checks: "key_field should be null in < 1% of rows"
- Range checks: "conversion_rate should be between 0 and 1"

### SLA Definition for Data Pipelines

Every pipeline should have a defined SLA: the time by which the data it produces must be available. An executive dashboard that stakeholders check at 8am needs a data pipeline SLA of 7:30am. Without defined SLAs, pipeline lateness is invisible until someone notices their report is stale.

---

## Output Format

```
1. PIPELINE DOCUMENTATION HEADER
   Pipeline name, owner, data engineer, last updated.
   SLA: data must be available by [time] for [consumer].

2. PIPELINE PURPOSE
   What business need this pipeline serves.
   Who consumes the output and how.
   Decisions enabled by the data.

3. DATA FLOW OVERVIEW
   Source → transformation → destination diagram.
   Pipeline tool/orchestrator: Airflow / Prefect / dbt Cloud / Fivetran / etc.

4. SOURCE SYSTEMS
   For each source:
   - System name and type
   - Connection method: direct DB / API / S3 / webhook
   - Data extracted: tables or endpoints
   - Extract frequency
   - Volume: approximate rows per run
   - Access credentials location

5. TRANSFORMATION LOGIC
   For each transformation step:
   - Step name and description
   - Tool: SQL / Python / dbt model
   - Input: source table(s)
   - Output: destination table
   - Key business logic applied
   - Reference to transformation code or dbt model

6. DESTINATION
   Target warehouse and schema.
   Tables produced.
   For each table: name, description, grain, update pattern (append / overwrite / upsert).

7. SCHEDULE
   Run frequency and schedule.
   Dependencies: other pipelines that must run first.
   Expected run duration.
   SLA: when output must be ready.

8. DATA QUALITY CHECKS
   For each check:
   - Check name and description
   - Check type: row count / freshness / null rate / range / uniqueness
   - Threshold: what triggers a failure
   - Action on failure: alert / halt pipeline / quarantine

9. ERROR HANDLING AND MONITORING
   Alert recipients and channels.
   Common failures and resolution procedures.
   How to manually re-run a failed pipeline.
   How to backfill historical data.

10. DEPENDENCIES AND DOWNSTREAM IMPACT
    What depends on this pipeline's output.
    Impact of pipeline failure on downstream consumers.
    Who to notify if SLA is at risk.
```

---

## Starter Prompt

```
You are a data engineer writing pipeline documentation.

Pipeline: [name and purpose]
Sources: [data sources with connection details]
Transformations: [the processing steps]
Destination: [target tables and warehouse]
Schedule: [when it runs]
SLA: [when data must be available]
Data quality checks: [validation checks applied]
Error handling: [what happens on failure]

Produce complete data pipeline documentation including data flow,
transformation logic, schedule, quality checks, and operational procedures.
Every quality check must have a defined threshold and failure action.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
