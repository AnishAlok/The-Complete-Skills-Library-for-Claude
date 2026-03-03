# competitive-battlecard.md

> **Skill:** Produces a sales battlecard for a specific competitor that equips sales representatives with positioning, differentiators, landmines, and verbatim response scripts for winning competitive deals.

---

## TLDR

A competitive battlecard gives sales reps exactly what they need to win deals where a specific competitor is in play: how to position against them, what strengths to lead with, where the competitor genuinely beats them (and how to handle it), what traps to set, and verbatim language for every scenario. Designed for use mid-deal in under two minutes of review. Opinionated, practical, ruthlessly brief.

---

## Topic Explanation

### What a Battlecard Is Not

A battlecard is not a balanced competitive analysis. It is not written for product managers, analysts, or marketing strategy. It is a practical sales tool designed to be read in 60 seconds before a call where a specific competitor has been mentioned.

The most common battlecard failure: it is too long, too balanced, and too fair to the competitor. A battlecard that says "Competitor X is strong in area Y" without telling reps exactly what to say when that strength comes up has failed its purpose. Balance is for academic papers. A battlecard is advocacy material for a sales rep who needs to win.

### The Honesty Principle

The second most common battlecard failure: it ignores competitor strengths entirely. Sales reps who discover that a competitor actually does beat the product in a specific area that the battlecard said was a win lose trust in all battlecard content permanently.

The rule: acknowledge every genuine competitor strength. Then provide specific, honest guidance on how to handle it. Reps can win deals even when competitors have real strengths — but only if they know about them and have a prepared response.

### The Landmine Technique

A landmine is a specific question the rep plants in the prospect's mind about a genuine competitor weakness. Landmines are not attacks or disparagement. They are honest questions that cause the prospect to investigate a real issue.

Effective landmine: "When you talk to them, ask them to show you how they handle [specific scenario they handle poorly] in a live demo. Ask to see it running with real data, not slides."

When the prospect asks the competitor about their landmine and receives a weak or evasive answer, the competitor's credibility drops without the rep having made a single negative claim.

---

## Dos

- **Do write every "our response" as verbatim language a rep can use without modification.** Generic guidance ("emphasize our strengths") is not a battlecard. Specific language ("say this: [exact words]") is.
- **Do update the battlecard after every significant competitive deal — win or loss.** Battlecards that are not updated based on field intelligence become misleading over time.
- **Do keep the total length to one page or equivalent.** A battlecard that takes five minutes to read will not be read.

---

## Donts

- **Dont encourage reps to bring up the competitor proactively.** Raising competitors who the prospect has not mentioned introduces them as options. The battlecard is for deals where the competitor is already in play.
- **Dont exaggerate competitor weaknesses.** Reps who oversell a competitor weakness, have the prospect verify it, and find it is not as severe as described lose credibility permanently.

---

## Output Format

```
BATTLECARD: [Competitor Name]
Last updated: [date] | Owner: [PMM name] | Version: [X.X]

QUICK SUMMARY
[2 to 3 sentences. Who this competitor is, who they sell to, and what their core pitch is.
Written from their perspective so reps recognize the pitch when they hear it from a prospect
who just came off a competitor call. Not our opinion of them. Their own positioning.]

WHY WE WIN
[3 to 5 bullets. Our strongest differentiators against this specific competitor.
Format: [Differentiator] — [specific proof point or example]
Be concrete: "We process X in Y seconds natively; they require an additional module
that costs $Z and takes 3 weeks to implement" not "we are faster and easier."]

WHY THEY WIN (be honest)
[2 to 3 bullets. Where the competitor genuinely has an advantage.
Format: [Their strength] — [how reps should handle this in a conversation]
Example: "They have deeper [specific integration]. Response: acknowledge it,
then redirect to whether that integration is in the prospect's workflow."]

THEIR PITCH
[The 3 to 4 claims this competitor makes about themselves.
Reps need to recognize these claims when a prospect repeats them after a competitor call.]
1. "[Exact language or close approximation they use]"
2. "[Exact language]"
3. "[Exact language]"

OUR RESPONSE TO THEIR PITCH
For each of their claims above:
Their claim: "[their language]"
Our response: "[Exact language a rep can use verbatim. 1 to 3 sentences.]"

LANDMINES
[3 to 5 specific questions to plant in the prospect's mind about genuine competitor weaknesses.
Format: "Ask them to [specific action] and observe the response."
Each must point to a real weakness, not a manufactured one.]
1. "Ask them to show you [specific capability they handle poorly] in a live demo with real data."
2. "Ask for a reference customer in [industry/size/use case where they struggle]."
3. "Ask how they handle [specific edge case] when [specific scenario]."

TRAP QUESTIONS THEY PLANT
[Questions this competitor's reps coach prospects to ask us. Forewarned is prepared.]
Their trap: "[the question they coach prospects to ask]"
Our answer: "[Specific, honest, confidence-building response. Not defensive.]"

WHEN THEY COME UP
[One short paragraph of guidance on when and how to raise competitive points.
Default guidance: do not bring up this competitor proactively unless the prospect mentions them.
If the prospect mentions them: [what to do first / what to do next].]

PROOF FOR THESE DEALS
[Customer references, win stories, or specific data points to use when this competitor
is in the deal. More credible than rep claims.]
```

---

## Starter Prompt

```
You are a product marketing manager writing a competitive battlecard for the sales team.

Competitor: [name]
Their target customer: [who they sell to and at what price point]
Their core pitch: [how they position and what they claim — in their own language]
Our strongest differentiators against them: [where we genuinely win and why]
Their genuine strengths: [where they beat us, stated honestly]
Common trap questions their reps plant: [questions they coach prospects to ask us]
Proof points for competitive deals: [references, win data, or specific results]
Genuine competitor weaknesses to expose via landmines: [real weaknesses worth surfacing]

Produce a complete battlecard following the format exactly.
Acknowledge every genuine competitor strength and provide specific handling guidance.
Every "our response" must be verbatim language a rep can use without modification.
Every landmine must point to a real weakness, not a manufactured criticism.
Total length: one page equivalent.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `positioning-doc.md` | Competitive alternatives in the positioning doc inform the battlecard content |
| `messaging-framework.md` | Competitive messages section of the framework feeds into each battlecard |

| Use This Alongside | Why |
|---|---|
| `sales-enablement-doc.md` | Battlecards are linked from and used within the sales enablement document |

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
