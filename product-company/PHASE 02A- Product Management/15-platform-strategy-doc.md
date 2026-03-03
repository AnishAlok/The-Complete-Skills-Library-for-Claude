# platform-strategy-doc.md

> **Skill:** Produces a platform and ecosystem strategy document defining how the product will expand from a standalone application to a platform that enables third-party development, integrations, or marketplace participation.

---

## TLDR

A platform strategy document defines how a product transitions from a self-contained application to a platform: a system that enables external developers, partners, or customers to build on top of it and create value the core team cannot build alone. This skill documents the platform vision, design principles, ecosystem model, and go-to-market approach for a platform strategy.

---

## Topic Explanation

### What Makes Something a Platform

A platform creates value by facilitating interactions between two or more groups. Pipelines (traditional businesses) create value through a linear production process. Platforms create value through network effects: the platform becomes more valuable as more participants join.

Types of platform models:
**Developer platform:** Third-party developers build applications on top of the platform (Salesforce AppExchange, Shopify App Store).
**Integration platform:** The product connects with other tools customers already use (Zapier, HubSpot integrations).
**Marketplace platform:** Buyers and sellers transact through the platform (Amazon Marketplace, Fiverr).
**Data platform:** Third parties build on top of the platform's data assets.

Most B2B SaaS companies pursue integration platforms first. Developer platforms require significant investment in API maturity and developer ecosystem building.

### Platform Design Principles

**Openness:** How open is the platform? Full API access, limited integration partners, or curated marketplace?
**Control vs. flexibility:** How much can builders customize? What is locked down?
**Value distribution:** How is value shared between the platform and builders?
**Quality governance:** How is quality on the platform maintained? Certification? Reviews? Curation?

---

## Output Format

```
1. PLATFORM VISION
   What the platform will enable that the core product cannot.
   Who the builders are and what they will create.
   The ecosystem the platform will power.

2. PLATFORM TYPE AND MODEL
   Which platform model (developer / integration / marketplace / data).
   How the platform creates and captures value.

3. STRATEGIC RATIONALE
   Why becoming a platform is strategically important now.
   How the platform accelerates the product vision.
   The network effects the platform will generate.

4. ECOSYSTEM DESIGN
   Who are the builders/partners we are targeting?
   What value do they get from building on the platform?
   What value do their customers get?
   How does the platform win if builders win?

5. PLATFORM CAPABILITIES ROADMAP
   What must be built to enable the platform:
   - API maturity requirements
   - Developer tooling and documentation
   - Authentication and permission model
   - Marketplace or discovery mechanism
   - Revenue sharing model

6. OPENNESS AND GOVERNANCE MODEL
   What is open vs. closed on the platform.
   Quality and certification standards.
   How platform policies will be enforced.

7. GO-TO-MARKET FOR THE PLATFORM
   How will the first builders be recruited?
   What development incentives exist?
   How will the platform be marketed to builders?

8. SUCCESS METRICS
   Active builders / integrations.
   Platform-sourced revenue or retention.
   Ecosystem health indicators.

9. RISKS AND MITIGATIONS
   Disintermediation risk.
   Quality control risk.
   Developer dependency risk.
```

---

## Starter Prompt

```
You are a product leader writing a platform strategy document.

Current product: [what the product does today]
Platform vision: [what the platform would enable]
Target builders: [who would build on the platform]
Platform type: [developer / integration / marketplace / data]
Strategic rationale: [why become a platform and why now]
Current API maturity: [what is already available to build on]

Produce a complete platform strategy document covering ecosystem design,
capability roadmap, governance model, and go-to-market approach.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
