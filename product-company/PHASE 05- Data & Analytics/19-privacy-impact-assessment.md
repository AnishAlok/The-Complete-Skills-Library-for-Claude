# privacy-impact-assessment.md

> **Skill:** Produces a Data Protection Impact Assessment (DPIA) for new data initiatives that identifies privacy risks, assesses necessity and proportionality, and documents mitigation measures and residual risk.

---

## TLDR

A Data Protection Impact Assessment (DPIA) is a structured privacy risk analysis required under GDPR for high-risk data processing activities and considered best practice for any new data initiative. It documents what data is processed, why, the risks to individuals, the measures taken to mitigate those risks, and the residual risk after mitigation.

---

## Topic Explanation

### When a DPIA Is Required

Under GDPR Article 35, a DPIA is mandatory when processing is "likely to result in a high risk to the rights and freedoms of natural persons." The Article 29 Working Party guidelines identify triggers including:

- Large-scale processing of sensitive data (health, biometric, financial)
- Systematic monitoring of a publicly accessible area
- Automated decision-making with significant effects on individuals
- Combining datasets in ways that were not originally anticipated
- Innovative technology with unknown privacy implications

Best practice is to conduct a lightweight DPIA for any new data processing activity and a full DPIA when any trigger condition applies.

### Necessity and Proportionality

Every data processing activity must meet the necessity and proportionality test:

**Necessity:** Is this data processing necessary for the stated purpose? Could the same purpose be achieved with less data or less intrusive processing?

**Proportionality:** Is the privacy cost proportionate to the benefit? Even necessary processing may fail proportionality if the benefit is minor but the privacy impact is significant.

These tests should be applied rigorously, not as box-checking exercises.

### Residual Risk vs. Acceptable Risk

No data processing activity is zero-risk. The DPIA documents the residual risk after all mitigations have been applied and asks: is this residual risk acceptable given the benefit of the processing?

If residual risk is unacceptable, the processing should not proceed or must be redesigned. If residual risk is acceptable, the DPIA documents the decision and rationale.

---

## Output Format

```
1. DPIA HEADER
   Initiative name, version, date, controller, author.
   DPO consulted, legal reviewed, approval status.

2. INITIATIVE DESCRIPTION
   What is being built or changed.
   Business purpose and expected benefits.
   Technical description of the processing.

3. DATA PROCESSING DESCRIPTION
   Personal data categories processed.
   Sensitive categories (Article 9 data): yes / no / which categories.
   Data subjects: who is affected.
   Volume and frequency.
   Source of data.
   Recipients: who receives the data.
   International transfers: any transfers outside EEA.

4. LEGAL BASIS FOR PROCESSING
   Legal basis under GDPR Article 6.
   For sensitive data: Article 9 exception relied upon.
   Legitimate interests assessment (if applicable).

5. NECESSITY AND PROPORTIONALITY ASSESSMENT
   Is this processing necessary for the purpose? Evidence.
   Can the purpose be achieved with less data or less intrusive processing?
   Is the benefit proportionate to the privacy cost?
   Data minimization: only the minimum necessary data is processed.
   Purpose limitation: data is not used beyond the stated purpose.

6. RISK IDENTIFICATION
   For each identified risk to data subjects:
   - Risk description: what could go wrong for individuals
   - Likelihood: High / Medium / Low
   - Severity: High / Medium / Low
   - Risk level: Likelihood × Severity

7. MITIGATION MEASURES
   For each risk:
   - Technical measures: encryption, access controls, pseudonymization
   - Organizational measures: policies, training, contracts
   - Residual risk after mitigation: High / Medium / Low

8. DATA SUBJECT RIGHTS
   How access rights are fulfilled.
   How erasure requests are handled.
   How portability requests are handled.
   How objection is handled.

9. RESIDUAL RISK ASSESSMENT
   Overall residual risk level.
   Is this residual risk acceptable? Rationale.
   If not acceptable: required changes before proceeding.

10. APPROVAL AND REVIEW
    DPO opinion.
    Conditions for approval.
    Review trigger: when DPIA must be updated.
    Next review date.
```

---

## Starter Prompt

```
You are a privacy officer or compliance analyst writing a DPIA.

Initiative: [what new data processing is being implemented]
Data categories: [what personal data is involved]
Data subjects: [who is affected]
Processing purpose: [why the data is being processed]
Legal basis: [the GDPR Article 6 basis]
Recipients: [who receives the data]
International transfers: [any data leaving the EEA]
Identified risks: [privacy risks to individuals]
Proposed mitigations: [technical and organizational measures]

Produce a complete DPIA covering necessity and proportionality assessment,
risk identification with scoring, mitigation measures, and residual risk assessment.
Flag any processing of sensitive data categories (Article 9) without explicit
documentation of the applicable exception.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
