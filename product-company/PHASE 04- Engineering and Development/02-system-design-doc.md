# system-design-doc.md

> **Skill:** Produces a system architecture document covering the overall design of a system or service, its components, interactions, data flows, scalability approach, and operational characteristics.

---

## TLDR

A system design document describes how an entire system is architected: its components, how they interact, how data flows through them, how the system scales and fails gracefully, and what the operational model looks like. Broader in scope than a technical spec (which covers a single feature), a system design doc covers a service or platform as a whole. Used when building a new service or significantly redesigning an existing one.

---

## Topic Explanation

### System Design vs. Technical Spec

**Technical spec:** Covers a specific feature or change. "How will we implement the async export job?"
**System design doc:** Covers a full service or platform. "How is the export service designed: its components, interfaces, data storage, scaling model, and operational approach?"

A codebase may have dozens of technical specs but one system design document per service. The system design doc is the authoritative reference for how the system works.

### C4 Model (Simon Brown)

The C4 model provides a standard visual vocabulary for system architecture documentation:
- **Context (C1):** The system in its environment. External actors and systems it interacts with.
- **Containers (C2):** The deployable units: applications, services, databases, message queues.
- **Components (C3):** Major logical components within a container.
- **Code (C4):** Classes and functions. Usually too detailed for system docs; belongs in code itself.

Using C4 levels explicitly makes system documentation navigable: readers can choose the level of detail they need.

### The Twelve-Factor App

For web services, the Twelve-Factor App methodology (Heroku) defines best-practice architectural patterns. A system design doc should implicitly or explicitly address how the service aligns with factors like: config in environment, stateless processes, explicit dependencies, and disposable/fast-starting processes.

---

## Output Format

```
1. SYSTEM OVERVIEW
   What this system does and its business purpose.
   Current scale: requests/day, users, data volume.
   Target scale.

2. CONTEXT DIAGRAM (C1)
   The system and all external actors/systems it interacts with.
   Data flows at the context level.

3. CONTAINER DIAGRAM (C2)
   All deployable units: services, databases, caches, queues, CDNs.
   Interfaces between containers.
   Technology choices for each.

4. COMPONENT DESIGN (C3 - for key containers)
   Major logical components within each service.
   Responsibilities and interfaces.

5. DATA ARCHITECTURE
   Primary data stores and their purpose.
   Data flow: where data originates, how it moves, where it lands.
   Caching strategy.
   Data retention and archival.

6. API SURFACE
   External-facing APIs.
   Internal service-to-service APIs.
   Reference to API design docs.

7. SCALABILITY AND PERFORMANCE
   How the system scales horizontally.
   Bottlenecks and how they are addressed.
   Performance SLOs: latency and throughput targets.

8. RELIABILITY AND FAULT TOLERANCE
   Single points of failure and how they are mitigated.
   Degradation modes when components fail.
   Data durability and backup strategy.

9. SECURITY MODEL
   Authentication and authorization.
   Data encryption at rest and in transit.
   Network security model.

10. OPERATIONAL MODEL
    Deployment architecture.
    Monitoring and alerting approach.
    On-call model.
    Incident response.

11. KNOWN LIMITATIONS AND FUTURE DIRECTION
    Current technical debt in the design.
    Planned evolution.
```

---

## Starter Prompt

```
You are a senior engineer writing a system design document.

System: [name and business purpose]
Scale: [current and target requests/users/data]
Components: [services, databases, queues, external systems]
Data flows: [how data moves through the system]
Scalability approach: [how the system handles load growth]
Reliability approach: [how the system handles failures]
Security model: [auth, encryption, network]

Produce a complete system design document using C4 model levels.
Include data architecture, API surface, scalability, reliability, and security.
Flag any single points of failure that lack mitigation.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
