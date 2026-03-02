# Claude Skills Library — Complete Company Lifecycle

> A comprehensive, production-ready library of ~445 skill files covering every role, every phase, and every document type across Product and Service companies.

---

## 🧭 What Is This Repo?

This repository is a structured knowledge base designed to work with Claude (or any LLM) as **prompt-level skill files**. Each file tells Claude *exactly* how to produce a specific professional document — with full context, best practices, dos/don'ts, and example inputs.

Think of it as: **a team of senior professionals encoded into markdown.**

Whether you're a solo founder, a product manager, a consultant, or running an agency, this library gives you the framework to produce expert-quality outputs fast.

---

## 🗂️ Repository Structure

```
skills-repo/
├── README.md                          ← You are here
├── INDEX.md                           ← Full searchable index of all 445 files
├── _TEMPLATE.md                       ← Base template every skill file follows
│
├── part1-product/                     ← Product & SaaS Company Lifecycle
│   ├── phase1-ideation-market-research/
│   │   ├── strategy-leadership/
│   │   └── market-research/
│   ├── phase2-product-strategy-planning/
│   │   ├── product-management/
│   │   └── program-project-management/
│   ├── phase3-ux-design/
│   │   ├── ux-research/
│   │   └── ux-design/
│   ├── phase4-engineering-development/
│   ├── phase5-data-analytics/
│   ├── phase6-quality-assurance/
│   ├── phase7-gtm-launch/
│   │   ├── product-marketing/
│   │   └── marketing/
│   ├── phase8-sales/
│   ├── phase9-customer-success-support/
│   │   ├── customer-success/
│   │   └── support/
│   ├── phase10-operations-finance/
│   │   ├── operations/
│   │   └── finance/
│   ├── phase11-people-hr/
│   └── phase12-legal-compliance/
│
├── part2-service/                     ← Service, Consulting & Agency Lifecycle
│   ├── phase1-business-development/
│   ├── phase2-client-onboarding/
│   ├── phase3-consulting-delivery/
│   │   ├── strategy-consulting/
│   │   ├── digital-technology/
│   │   └── management-consulting/
│   ├── phase4-agency-delivery/
│   │   ├── creative-design/
│   │   ├── digital-marketing/
│   │   └── ux-product-agency/
│   ├── phase5-project-reporting/
│   └── phase6-knowledge-management/
│
└── part3-cross-cutting/               ← Works for Both Company Types
    ├── communication-meetings/
    ├── learning-development/
    └── ai-automation/
```

---

## 📖 How To Use Each Skill File

Every skill file in this repo follows the same structure:

| Section | What It Contains |
|---|---|
| **TLDR** | 2-sentence summary of what this skill produces |
| **What Is This?** | Full explanation of the document type and why it matters |
| **When To Use** | Specific triggers, scenarios, and moments when this skill applies |
| **Do's** | Best practices that make the output great |
| **Don'ts** | Common mistakes that kill the quality |
| **Inputs** | Exactly what information you need to feed in for best results |
| **Output Format** | The structure Claude will produce |
| **Example Prompt** | A ready-to-copy prompt you can use immediately |
| **Pro Tips** | Expert-level nuances most people miss |

---

## 🚀 Quick Start

### For Product Companies
Start with these 10 files:
1. `part1-product/phase1-ideation/strategy-leadership/market-opportunity-analysis.md`
2. `part1-product/phase2-product-strategy/product-management/feature-spec.md`
3. `part1-product/phase3-ux-design/ux-research/ux-research-plan.md`
4. `part1-product/phase4-engineering/technical-spec.md`
5. `part1-product/phase5-data-analytics/ab-test-plan.md`
6. `part1-product/phase2-product-strategy/product-management/product-roadmap.md`
7. `part1-product/phase7-gtm-launch/product-marketing/case-study.md`
8. `part1-product/phase7-gtm-launch/product-marketing/launch-plan.md`
9. `part1-product/phase9-customer-success/customer-success/onboarding-plan.md`
10. `part1-product/phase11-people-hr/job-description.md`

### For Service / Consulting Companies
Start with these 10 files:
1. `part2-service/phase1-business-development/proposal-writing.md`
2. `part2-service/phase1-business-development/scope-of-work.md`
3. `part2-service/phase2-client-onboarding/discovery-interview-guide.md`
4. `part2-service/phase5-project-reporting/weekly-status-report.md`
5. `part2-service/phase3-consulting-delivery/strategy-consulting/executive-presentation.md`
6. `part2-service/phase3-consulting-delivery/strategy-consulting/workshop-facilitation.md`
7. `part2-service/phase3-consulting-delivery/strategy-consulting/strategic-recommendations.md`
8. `part2-service/phase1-business-development/case-study-services.md`
9. `part2-service/phase5-project-reporting/project-closeout-services.md`
10. `part2-service/phase4-agency-delivery/digital-marketing/monthly-performance-report.md`

---

## 🧠 How To Use With Claude

### Option 1: Paste the skill file directly
Copy the contents of any skill file and paste it at the start of your Claude conversation, then provide your specific inputs.

### Option 2: Reference the structure
Tell Claude: *"Use the skill file format from this repo to help me write a [document type]"* and paste the relevant skill file.

### Option 3: Build a Claude Project
Upload the entire repo (or relevant phase folders) into a Claude Project. Claude will use the skill files automatically when you ask for any document type.

---

## 📊 Library Stats

| Section | Files |
|---|---|
| Part 1: Product Company (Phases 1–12) | ~280 |
| Part 2: Service Company (Phases 1–6) | ~130 |
| Part 3: Cross-cutting | ~35 |
| **Total** | **~445** |

---

## 🔄 Contributing

Each skill file must follow the standard template. To add a new skill:

1. Identify the correct phase and folder
2. Copy `_TEMPLATE.md` as your base
3. Fill in all 9 sections completely — no placeholders
4. Submit a PR with a clear description of the new skill

---

## 📄 License

MIT — use freely, contribute back.

---

*Built for teams who want to move faster without sacrificing quality.*
