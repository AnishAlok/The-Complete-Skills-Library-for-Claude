# participant-consent-form.md

> **Skill:** Produces participant consent forms for research studies, including recording consent, data use agreements, NDA clauses where needed, and participant rights language compliant with standard research ethics and GDPR principles.

---

## TLDR

Participant consent forms protect both the research participant and the organization by documenting what the participant has agreed to, how their data will be used, and their rights. This skill produces a consent form appropriate for UX research, customer research, or market research sessions, with optional NDA provisions, recording consent, and GDPR-compliant data handling language.

---

## Topic Explanation

### What Consent Forms Must Cover

Under research ethics standards (APA, BPS, ESOMAR) and applicable privacy law (GDPR, CCPA), participant consent must be:

**Informed:** Participants must understand what they are agreeing to before they agree. The form must be in plain language, not legal jargon.

**Freely given:** Participation must be voluntary. Participants must know they can withdraw at any time without penalty.

**Specific:** Consent for recording is separate from consent for participation. Consent for use in internal reports is separate from consent for use in external publications or marketing.

**Documented:** Written consent is required for most commercial research. Verbal consent may be acceptable for some low-risk remote studies but written is always preferable.

### Key Elements of a Research Consent Form

**Study purpose:** A brief, honest description of what the research is about. Does not need to reveal specific hypotheses but must not deceive the participant about the nature of the research.

**What participation involves:** What the participant will be asked to do. How long it will take.

**Recording consent:** Specific consent for audio, video, and/or screen recording. Who will have access to recordings. How long recordings will be retained.

**Data handling:** How data will be stored, who will have access, and how long it will be retained. For GDPR: legal basis for processing, data subject rights.

**Confidentiality:** Whether the participant's identity will be protected. Whether any quotes will be attributed.

**Voluntary participation and right to withdraw:** Explicit statement that participation is voluntary and participants can withdraw at any time.

**Contact information:** Who to contact with questions or to exercise data rights.

**Signature:** Participant and witness/researcher signature with date.

### NDA Provisions

Some research sessions involve showing unreleased products, confidential roadmaps, or sensitive company information. In these cases, a mutual NDA clause can be added to the consent form. Key NDA elements:
- What information is considered confidential
- How long the confidentiality obligation lasts
- That it is mutual (the company also agrees not to identify the participant)

For most standard UX research, a full NDA is not necessary. A confidentiality clause stating that observations will not be publicly attributed to the participant is usually sufficient.

---

## When to Use This Skill

Use when:
- Any research session involves recording
- Research involves showing unreleased product features
- Research involves vulnerable populations
- GDPR or other privacy law applies to participants
- Research will be used in publications, marketing, or investor materials

---

## Dos

- **Do write in plain language.** Participants must understand what they are agreeing to. Legal language that participants cannot understand does not constitute informed consent.
- **Do separate consent for different uses.** Consent for internal analysis is separate from consent for external marketing use. Use checkboxes for distinct uses.
- **Do include a right-to-withdraw statement.** This is both ethically required and often legally required.
- **Do specify recording retention period.** Vague "for research purposes" is not sufficient under GDPR.

---

## Output Format

```
1. FORM HEADER
   Study title (can be descriptive rather than revealing), organization name,
   date, version.

2. STUDY DESCRIPTION
   Plain-language description of the research purpose.
   What participation involves and how long it will take.
   Who is conducting the research and who it is for.

3. PARTICIPATION CONSENT SECTION
   What the participant is agreeing to.
   Voluntary participation statement.
   Right to withdraw at any time without penalty.
   Participant signature and date.

4. RECORDING CONSENT SECTION (separate checkboxes)
   [ ] I consent to audio recording
   [ ] I consent to video recording
   [ ] I consent to screen recording
   Who will have access to recordings.
   How long recordings will be retained.
   What recordings will be used for.

5. DATA HANDLING SECTION
   How data will be stored and protected.
   Who will have access.
   Retention period.
   GDPR rights (if applicable): right to access, correct, delete, object.
   Contact for data rights requests.

6. CONFIDENTIALITY STATEMENT
   How participant identity will be protected in any reports or outputs.
   NDA clause if applicable.

7. CONTACT INFORMATION
   Research lead name and contact.
   Data protection contact if applicable.

8. SIGNATURES
   Participant name, signature, date.
   Researcher name, signature, date.

9. GDPR-SPECIFIC ADDENDUM (if applicable)
   Legal basis for processing.
   Data controller identification.
   International transfer information if relevant.
```

---

## Starter Prompt

```
You are a research operations specialist drafting a participant consent form.

Study type: [UX research / market research / customer interview]
Recording types: [audio / video / screen]
Whether unreleased product is shown: [yes/no - NDA needed?]
Participant location: [US / EU / global - GDPR applicability]
Data retention period: [how long recordings and notes will be kept]
External use of findings: [internal only / publications / marketing material]
Organization name and contact: [for the form header and data contact]

Produce a complete participant consent form in plain language with all
required sections, including separate checkboxes for different recording types
and data uses. Include GDPR-specific language if EU participants are involved.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
