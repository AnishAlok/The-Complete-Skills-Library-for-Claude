# research-ops-plan.md

> **Skill:** Produces a research operations plan that defines the systems, processes, tools, and practices needed to run a scalable, high-quality research function within a product organization.

---

## TLDR

Research operations (ReOps) is the discipline of managing the infrastructure, processes, and practices that enable a research function to run efficiently at scale. This skill produces a ReOps plan covering: participant management, tool stack, templates and standards, knowledge management, research enablement, and team practices. Used when a research function is growing and needs operational infrastructure to scale without losing quality.

---

## Topic Explanation

### What Research Operations Covers

Research operations handles everything that is not the research itself but makes the research possible at scale:

**Participant management:** Recruiting panels, consent management, incentive processing, participant CRM, do-not-contact management.

**Tool stack management:** Selecting, onboarding, and maintaining research tools. Recording and storage, synthesis platforms, survey tools, prototype testing platforms, scheduling.

**Templates and standards:** Standardized research plan templates, consent forms, reporting formats, tagging taxonomies. Consistency enables comparison and institutional learning.

**Knowledge management:** Research repository design, insight tagging, cross-study synthesis, onboarding new team members to prior research.

**Research enablement:** Making research accessible to non-researchers. Training PMs and designers to conduct lightweight research. Building self-serve research capabilities.

**Compliance and ethics:** IRB processes, GDPR compliance, data retention policies, recording consent management.

**Team practices:** Recruiting processes, researcher onboarding, quality review, skill development.

### When to Invest in Research Operations

Research operations investment is typically justified when:
- The research team is doing more than 2 to 3 studies per month
- Recruiting the same types of participants repeatedly and lacking a system
- Multiple researchers are producing inconsistent documentation
- Research findings are hard to find or reuse
- Non-researchers want to conduct research but lack infrastructure and guardrails
- Legal or compliance requirements for data handling are becoming more complex

---

## Output Format

```
1. REOPS AUDIT
   Current state: what infrastructure exists and what is missing.
   Priority gaps: the 3 to 5 most impactful missing capabilities.

2. TOOL STACK RECOMMENDATION
   Recruiting and participant management tool.
   Session recording and storage tool.
   Synthesis and analysis tool.
   Repository and knowledge management tool.
   Survey platform.
   Prototype testing platform.
   With: recommended tool, rationale, cost, integration notes.

3. PARTICIPANT MANAGEMENT SYSTEM
   Panel recruitment and maintenance approach.
   Consent and GDPR compliance workflow.
   Incentive processing workflow.
   Participation frequency limits and do-not-contact management.

4. TEMPLATES AND STANDARDS LIBRARY
   List of templates to create or standardize.
   Tagging taxonomy for research repository.
   Reporting format standards.
   Where templates live and how they are accessed.

5. RESEARCH ENABLEMENT PROGRAM
   Which non-researchers will be enabled to conduct research.
   Training and guardrail approach.
   Approved lightweight research methods.
   Review and quality check process.

6. COMPLIANCE AND ETHICS FRAMEWORK
   Consent form standards.
   Recording storage and retention policy.
   PII handling guidelines.
   Escalation process for sensitive research topics.

7. TEAM PRACTICES AND NORMS
   Research request intake process.
   Prioritization criteria for research requests.
   Quality review process.
   New researcher onboarding.

8. REOPS ROADMAP
   Phase 1 (immediate): highest-priority infrastructure gaps.
   Phase 2 (within 3 months): operational improvements.
   Phase 3 (within 6 months): scale and enablement.
   Owner and effort estimate for each initiative.
```

---

## Starter Prompt

```
You are a research operations specialist building a ReOps plan.

Research team size: [number of researchers and their roles]
Research volume: [studies per month, types of research conducted]
Current infrastructure: [what tools and processes already exist]
Known pain points: [the biggest operational problems]
Budget constraints: [tool budget available]
Non-researcher enablement interest: [whether PMs/designers want to run research]
Compliance requirements: [GDPR, IRB, or other relevant requirements]

Produce a complete research operations plan covering all seven areas.
Prioritize recommendations by impact on research quality and velocity.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
