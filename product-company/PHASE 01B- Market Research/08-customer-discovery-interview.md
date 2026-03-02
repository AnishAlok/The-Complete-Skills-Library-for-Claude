# customer-discovery-interview.md

> **Skill:** Produces a complete problem interview script and synthesis framework for customer discovery, designed to uncover real pain, validate or invalidate assumptions, and generate insight that drives product and strategy decisions.

---

## TLDR

This skill helps you answer: *"Are we solving a real problem that real people care enough about to change their behavior?"* It produces a problem-focused interview script, a facilitation guide, and a synthesis framework for extracting patterns across multiple interviews. Used before building anything, before repositioning, before a major product bet, or any time the team needs to get out of the building and test its assumptions against reality.

---

## Topic Explanation

### What Is Customer Discovery?

Customer discovery is the systematic process of testing the core assumptions of a business or product by getting out of the building and talking to real potential customers. The term was coined by Steve Blank and forms the first phase of the Customer Development methodology described in his book *The Four Steps to the Epiphany* (2005), later popularized by Eric Ries in *The Lean Startup*.

The fundamental premise is that no business plan survives first contact with customers. The assumptions baked into every product roadmap, pitch deck, and strategy document are hypotheses, not facts. Customer discovery is the process of testing those hypotheses before spending significant time and money on them.

A customer discovery interview is specifically a problem interview: a conversation designed to understand whether a problem exists, how painful it is, how people currently solve it, and whether they would seek a better solution. It is not a feature interview ("what would you want this product to do?") and it is not a usability test ("can you use this interface?").

### Problem Interviews vs. Solution Interviews

Customer discovery typically has two stages:

**Problem interviews (this skill):** Conducted before a solution exists or before it is shown to the customer. The goal is to understand the problem space deeply without contaminating the customer's thinking with your proposed solution. You are validating that the problem is real, painful, and worth solving.

**Solution interviews:** Conducted after a solution concept has been developed, typically with a prototype, mockup, or demo. The goal is to test whether your solution resonates and whether customers would actually adopt it.

This skill covers problem interviews. Solution interviews are covered in `usability-test-script.md` and `prototype-spec.md`.

### The Mom Test

Rob Fitzpatrick's *The Mom Test* (2013) is the most practically useful guide to customer discovery interviewing. Its core insight is that most customer interviews produce false positives because interviewers ask questions that are easy to answer positively.

The Mom Test rules:
- Talk about their life, not your idea
- Ask about specifics in the past, not generics or hypotheticals about the future
- Listen more than you talk

Bad question: "Would you use a tool that automated your payroll compliance?" (hypothetical, future, easy to say yes)
Good question: "Tell me about the last time you ran payroll. What was the hardest part?" (past, specific, behavioral)

The difference is the difference between learning and receiving validation. The first question type produces validation that feels good and teaches nothing. The second type produces insight that may be uncomfortable but is genuinely useful.

### The Structure of a Problem Interview

A well-designed problem interview has five phases:

**1. Welcome and framing (2 to 3 minutes)**
Establish rapport, explain the purpose (you are learning, not selling), confirm recording consent, set the expectation that there are no right or wrong answers.

**2. Background and context (5 to 10 minutes)**
Understand who this person is, what their role involves, what their workflow looks like. This grounds all subsequent answers in a specific reality.

**3. Problem exploration (15 to 20 minutes)**
The core of the interview. Ask about specific past experiences related to the problem domain. Probe for: frequency, pain level, workarounds, cost of the problem, previous attempts to solve it.

**4. Current solution analysis (5 to 10 minutes)**
How do they currently address this problem? What do they use? What do they like and dislike about it? How did they find it? What would make them switch?

**5. Wrap-up and referrals (2 to 3 minutes)**
Is there anything important you did not ask? Who else should you talk to? Would they be willing to speak again?

### Synthesis: From Interviews to Insight

Individual interviews produce raw data: stories, quotes, observations. The insight comes from pattern recognition across multiple interviews. A finding that appeared in one interview is an anecdote. A finding that appeared in 8 of 12 interviews is a signal.

Synthesis involves:
- Writing up each interview within 24 hours while memory is fresh
- Extracting discrete observations and quotes onto individual cards or notes
- Grouping observations by theme across all interviews
- Identifying patterns: what appears consistently? What appears only in specific segments? What surprised you?
- Testing your original hypotheses against what you found

---

## When to Use This Skill

Use when:
- Starting a new product or company and needing to validate the problem before building
- Evaluating a new product bet or major feature investment before committing resources
- Entering a new customer segment and needing to understand the problem space
- A product has stalled and you suspect you may be solving the wrong problem
- Repositioning a product and needing to understand how customers currently frame their needs
- Preparing an investment thesis and needing evidence that the problem is real and significant

Do NOT use when:
- You need to test a specific product or interface (use `usability-test-script.md`)
- You need to understand why customers churned (use `churn-interview.md`)
- You need to understand why you win or lose deals (use `win-loss-analysis.md`)
- You have already validated the problem and need quantitative confirmation (use `survey-design.md`)

---

## Dos

- **Do ask about the past, not the future.** "Tell me about the last time this was a problem" is a question about reality. "Would you want a tool that..." is a question about imagination. Reality wins.
- **Do stay in problem space, not solution space.** The moment you describe your solution, the interview shifts from discovery to validation theater. Resist the urge to pitch.
- **Do follow the energy.** When a participant becomes animated, leans forward, or pauses thoughtfully, that is where the real pain lives. Probe deeper.
- **Do ask for specifics and stories.** "Can you walk me through the last time that happened?" produces richer data than "Does that happen often?"
- **Do let silence do the work.** After a participant answers, wait 3 to 5 seconds before speaking. Silence often produces the most honest, unfiltered follow-up.
- **Do capture verbatim quotes.** The exact words participants use to describe their problems are data. Do not paraphrase in your notes.
- **Do ask "why" at least twice per topic.** The first answer is usually the surface answer. The second and third "why" gets to the real motivation.
- **Do end by asking for referrals.** "Is there anyone else you think I should speak with?" is one of the most valuable questions in any discovery interview. The best participants find more best participants.
- **Do debrief immediately after each session.** Write up the key takeaways, surprises, and quotes within an hour of finishing. Memory degrades fast.

---

## Donts

- **Dont pitch.** If you are explaining your product or idea during a problem interview, you are no longer learning. You are selling. Stop.
- **Dont ask leading questions.** "Would it be useful if you could do X faster?" implies that faster is better. Ask instead: "How do you currently approach X? What frustrates you about that?"
- **Dont accept "yes" as an answer.** "Yes, that would be useful" or "yes, that is a problem" is the beginning of a conversation, not the end. Always follow up: "Tell me more about that. When did that last happen? What did you do?"
- **Dont ask hypothetical questions.** "Would you pay for this?" tells you nothing. "Have you paid for anything like this before?" tells you something.
- **Dont interview people who are too nice.** Close friends, family, and your most loyal customers will tell you what you want to hear. Seek out skeptics and people with no relationship to you.
- **Dont stop at 3 interviews.** Three interviews is not a sample. Eight to twelve interviews across a defined participant type is the minimum for pattern recognition in qualitative research.
- **Dont conduct interviews in groups.** Group dynamics produce social performance, not honest individual responses. Interview one person at a time.
- **Dont record key findings only in your memory.** Take structured notes during or immediately after every session. Verbal debriefs that are not written down produce nothing.
- **Dont ignore the participants who do not fit your hypothesis.** The interviews that challenge your assumptions are more valuable than the ones that confirm them.

---

## Ideal Inputs

### Required
```
1. THE HYPOTHESIS BEING TESTED
   What specific problem does the team believe exists?
   What assumption about the customer or their pain are you testing?

2. THE TARGET PARTICIPANT TYPE
   Who should be in these interviews?
   Specific criteria: role, industry, company size, behavior, experience.

3. THE PROBLEM DOMAIN
   What area of their work or life are you exploring?
   What activity, workflow, or situation is the focus?

4. THE DECISION THIS WILL INFORM
   What will you do differently depending on what you find?
   If you discover the problem is not real, what changes?
   If you confirm it is real, what happens next?

5. WHAT YOU ALREADY KNOW
   What prior research, customer conversations, or data already exists?
   What patterns have you already observed?
```

### Optional but Valuable
```
6. CURRENT HYPOTHESES TO TEST
   The specific assumptions you most need to confirm or invalidate.
   These become the probing areas in the interview guide.

7. PRIOR INTERVIEW LEARNINGS
   If this is not the first round of discovery, what did previous
   interviews surface that this round should build on?

8. SEGMENT DIFFERENCES TO EXPLORE
   Are there different customer types you suspect have meaningfully
   different experiences of the problem?

9. WORKAROUNDS ALREADY OBSERVED
   Any specific workarounds or shadow systems you have already seen
   that the interview should probe.

10. TARGET NUMBER OF INTERVIEWS
    How many interviews are planned?
    This affects synthesis planning.
```

### Example of a Strong Input Prompt
```
Hypothesis: Independent restaurant operators spend 3 to 5 hours per week on
payroll-related compliance tasks and are anxious about compliance errors
that could result in audits or employee disputes.
Target participants: Restaurant owners or operators with 1 to 5 locations
who currently manage their own payroll (not outsourced to a PEO).
Problem domain: Weekly payroll process, tip pooling, compliance reporting.
Decision: If 7 of 10 interviews confirm significant pain and time cost,
we proceed with building. If fewer than 5 confirm it, we pivot.
What we know: 3 early customers found us organically and describe exactly
this pain. We do not know if they are representative or outliers.
Hypotheses to test:
1. The problem is significant enough that operators would pay to solve it.
2. The pain is around compliance specifically, not just general payroll admin.
3. Operators do not trust generic payroll tools to handle restaurant compliance.
Target interviews: 12 interviews across different restaurant types and sizes.
```

---

## Output Format

```
1. INTERVIEW GUIDE HEADER
   Study purpose, participant criteria, interview length,
   recording consent approach, session format (in-person / video / phone).

2. INTERVIEWER PREPARATION CHECKLIST
   What to have ready before the session.
   What to review (participant background, prior interview themes).
   Mental preparation: remind yourself to listen, not pitch.

3. WELCOME SCRIPT (verbatim)
   Word-for-word opening the interviewer reads or adapts.
   Covers: purpose, no right/wrong answers, permission to record,
   approximate length, reminder that you are learning not selling.

4. BACKGROUND AND CONTEXT QUESTIONS (5 to 10 minutes)
   3 to 5 questions to understand who this person is and what their
   day-to-day looks like in the relevant domain.
   Probes for each question.

5. CORE PROBLEM EXPLORATION (15 to 20 minutes)
   The main interview questions, ordered from open to specific.
   For each question: the question itself, the intent behind it,
   and 2 to 3 follow-up probes.
   Focus on specific past experiences, not generics or hypotheticals.

6. CURRENT SOLUTION ANALYSIS (5 to 10 minutes)
   Questions about how they currently address the problem.
   What they use, what they like, what they do not like,
   what would make them change.

7. HYPOTHESIS TESTING QUESTIONS
   Specific questions designed to test the core assumptions
   without leading the participant.
   Each question paired with: what a confirming answer looks like
   and what a disconfirming answer looks like.

8. WRAP-UP AND REFERRALS (2 to 3 minutes)
   Open invitation for anything not covered.
   Ask for referrals to other potential participants.
   Confirm willingness to follow up if needed.

9. POST-INTERVIEW SYNTHESIS TEMPLATE
   Structured format to complete within 1 hour of each session:
   - 3 most important things learned
   - Verbatim quotes to preserve
   - Hypothesis status: confirmed / disconfirmed / unclear
   - Surprises
   - Follow-up questions for next interview

10. CROSS-INTERVIEW PATTERN SYNTHESIS TEMPLATE
    Template for use after all interviews are complete:
    - Common themes across interviews
    - Patterns by participant segment
    - Hypothesis scorecard: how many interviews confirmed vs. disconfirmed each assumption
    - Top 5 to 7 insights with supporting evidence
    - Recommended next steps based on findings
```

---

## Starter Prompt

```
You are a customer discovery specialist helping me design a problem interview
script and synthesis framework.

Hypothesis being tested: [the specific problem assumption you are testing]
Target participant type: [specific criteria for who to interview]
Problem domain: [the workflow, activity, or situation being explored]
Decision this will inform: [what changes depending on what you find]
What we already know: [prior research or observations]
Hypotheses to test: [specific assumptions to confirm or invalidate]
Prior interview learnings: [if this is a follow-on round, what was learned before]
Segment differences to explore: [different customer types to probe]
Target number of interviews: [how many sessions planned]

Please produce:
1. A complete problem interview script with welcome, background, core exploration,
   current solution analysis, hypothesis testing, and wrap-up sections
2. The intent behind each question (so the interviewer understands why it is there)
3. Two to three follow-up probes for every main question
4. A hypothesis testing section with specific questions that test assumptions
   without leading the participant
5. A post-interview synthesis template to complete within 1 hour of each session
6. A cross-interview pattern synthesis template for use after all interviews
7. An interviewer preparation checklist

Write every question following the Mom Test principles: past not future,
specific not hypothetical, behavioral not attitudinal.
Flag any question that could produce false validation and rewrite it.
Remind me throughout to stay in problem space and not pitch.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `research-synthesis-report.md` | Produce a formal findings report from the interview synthesis |
| `jobs-to-be-done.md` | Deepen problem interviews with JTBD methodology |
| `affinity-mapping.md` | Organize raw interview observations into themes |
| `market-opportunity-analysis.md` | Use confirmed pain and willingness to pay to inform market sizing |
| `product-vision-doc.md` | Use discovery findings to anchor the product vision |

| Use This Before | Why |
|---|---|
| `primary-research-plan.md` | Plan the full research initiative before designing the interview |
| `survey-design.md` | Problem interviews generate hypotheses that surveys then validate at scale |
| `mvp-definition.md` | Discovery confirms which problem to solve before scoping an MVP |

---

## Reference Frameworks

| Framework | Use For |
|---|---|
| The Mom Test (Rob Fitzpatrick) | Foundational principles for avoiding false validation in interviews |
| Customer Development (Steve Blank) | The four-step methodology that customer discovery interviews are part of |
| Lean Startup (Eric Ries) | Build-Measure-Learn loop that problem interviews feed |
| JTBD Switch Interview (Bob Moesta) | Deep behavioral interviewing technique for understanding motivation |
| Thematic Analysis (Braun and Clarke) | Systematic method for coding and synthesizing qualitative data |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
