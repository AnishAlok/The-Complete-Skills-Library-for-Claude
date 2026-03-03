# product-vision-doc.md

> **Skill:** Produces a product vision narrative that articulates where the product is going, why it matters, and what the world looks like when it succeeds, in a form that inspires and aligns teams over a multi-year horizon.

---

## TLDR

This skill helps you answer: *"What is this product ultimately trying to become, and why does that future matter enough to build toward?"* It produces a compelling vision narrative that provides strategic direction without prescribing the path, enabling teams to make aligned decisions without constant top-down direction. Used at company formation, major pivots, and whenever the product needs renewed strategic coherence.

---

## Topic Explanation

### Vision vs. Strategy vs. Roadmap

These three documents form a hierarchy of increasing specificity and decreasing time horizon:

**Vision:** Where you are going and why it matters. 3 to 10 year horizon. Does not specify how you will get there. Should not change frequently.

**Strategy:** The choices you are making to reach the vision. Which bets, which markets, which capabilities. 1 to 3 year horizon. Changes as you learn.

**Roadmap:** The specific things you are building to execute the strategy. 6 to 18 month horizon. Changes frequently.

A vision without a strategy is aspiration. A strategy without a vision is tactics. A roadmap without a strategy is a to-do list.

This skill covers the vision. Strategy is covered in `product-strategy-doc.md`. Roadmap in `product-roadmap.md`.

### What Makes a Vision Compelling

A product vision is not a mission statement, a tagline, or a feature list. It is a narrative description of a future state that is:

**Specific enough to be directional:** "Become the leading platform for restaurant compliance" is directional. "Make restaurant operations better" is not.

**Ambitious enough to be inspiring:** A vision that describes the product's current state + 20% is not a vision. It is a Q3 goal.

**Concrete enough to test against:** Teams should be able to ask "does this decision move us toward the vision?" If the answer is always "maybe," the vision is too abstract.

**Human enough to care about:** The best visions describe a changed human experience, not a market position. "A world where no restaurant operator loses sleep worrying about a payroll audit" is human. "The market leader in restaurant HCM" is not.

### The Geoffrey Moore Vision Template

Geoffrey Moore's vision template from *Crossing the Chasm* is the most widely used structured format for product vision:

"For [target customer] who [has this need or problem], [product name] is a [product category] that [key benefit]. Unlike [competitive alternative], our product [primary differentiation]."

This template is useful for clarity but can feel mechanical. The best product visions use this structure as a foundation and build a richer narrative around it.

### Narrative Vision Format

Amazon's "working backward" approach uses a press release narrative written as if the product has already succeeded. This format forces specificity about what success actually means and for whom. The press release:
- Has a specific date in the future
- Describes a specific customer whose life has changed
- Is written in the past tense (the product has already succeeded)
- Contains specific details about what changed and why it mattered

This is more labor-intensive than the Moore template but produces richer, more inspiring, and more testable visions.

---

## When to Use This Skill

Use when:
- Starting a new product or company and establishing the founding vision
- A product has drifted and needs a re-anchoring on purpose and direction
- Joining a new leadership role and needing to understand and articulate the vision
- Preparing an investor pitch or board presentation that requires clear vision articulation
- Team alignment has broken down and a return to first principles is needed

Do NOT use when:
- The vision is already clear and agreed upon (produce the strategy or roadmap instead)
- The horizon is too short for a vision (under one year is strategy or execution, not vision)

---

## Dos

- **Do describe a changed human experience, not a product state.** "Restaurant operators sleep soundly knowing their payroll is compliant" not "a comprehensive payroll compliance platform."
- **Do make it time-bounded.** "In 2030..." forces specificity. "Someday..." does not.
- **Do test it against real decisions.** After writing the vision, bring it to a team meeting and ask: "Does this vision help us decide between option A and option B?" If it does not, it is too abstract.
- **Do keep it short enough to be memorized.** A vision no one can remember without looking it up is a vision that will not guide decisions.
- **Do make it believable, not just ambitious.** A vision that sounds impossible produces cynicism rather than inspiration in most people.
- **Do separate the vision from the strategy.** The vision does not include "how." How is the strategy.

---

## Donts

- **Dont describe current product features.** A vision that could describe what you built last year is not a vision.
- **Dont use jargon and category terms as the substance.** "The operating system for restaurant businesses" sounds visionary but means nothing without the human story behind it.
- **Dont make it committee language.** Visions written by consensus tend toward inoffensive generality. A good vision makes specific choices.
- **Dont confuse the vision with the mission.** The mission describes why you exist (purpose). The vision describes where you are going (aspiration). Both are needed; they are not the same document.

---

## Ideal Inputs

```
1. PRODUCT CONTEXT
   What does this product do today?
   Who does it serve?
   What problem does it solve?

2. WHY THIS MATTERS
   What happens in the world if this product succeeds?
   Who benefits and how?
   Why does this problem deserve to be solved?

3. MARKET AND COMPETITIVE CONTEXT
   What alternatives exist today?
   Why are those alternatives insufficient?
   What would "winning" look like?

4. TIME HORIZON
   How far out should this vision look?
   What is the intended tenure of this vision?

5. STRATEGIC BETS
   What assumptions about the future is this vision built on?
   What must be true for this vision to be achievable?
```

---

## Output Format

```
1. VISION HEADLINE
   One sentence that captures the essence of the vision.
   Memorable, specific, and directional.

2. THE WORLD WE ARE BUILDING TOWARD
   A narrative description of the future state.
   Who benefits, how, and why this matters.
   Written in the present tense as if that future has arrived.
   2 to 4 paragraphs.

3. THE PROBLEM WE ARE ELIMINATING
   The specific pain, friction, or injustice in the current world
   that this vision eliminates.
   Specific enough to be vivid.

4. WHY NOW
   Why is this vision achievable now when it was not before?
   What has changed in technology, market, or behavior?

5. WHO WE SERVE
   The specific people whose lives change.
   Not a market segment description but a human description.

6. WHAT WE ARE NOT
   What the vision explicitly excludes.
   What we will not become even if we could.
   This is as important as what the vision includes.

7. ASSUMPTIONS AND BETS
   What must be true for this vision to be right?
   These are the strategic hypotheses the vision rests on.

8. HOW WE KNOW WE ARE GETTING THERE
   3 to 5 indicators that the vision is being realized.
   These become the north star metrics.
```

---

## Starter Prompt

```
You are a product leader writing a compelling product vision document.

Product context: [what the product does and who it serves today]
Why this matters: [what changes in the world if this succeeds]
Market context: [what alternatives exist and why they are insufficient]
Time horizon: [how far out this vision should look]
Strategic bets: [the assumptions this vision rests on]
What we are not: [explicit exclusions from the vision]

Please produce a complete product vision document including:
1. A memorable one-sentence vision headline
2. A 2 to 4 paragraph narrative of the future state in present tense
3. A vivid description of the problem being eliminated
4. A "why now" section grounded in real market or technology shifts
5. A human description of who we serve
6. An explicit "what we are not" section
7. The strategic assumptions this vision rests on
8. 3 to 5 indicators that the vision is being realized

Write in a tone that inspires without overpromising.
Describe changed human experiences, not product states.
Flag any vision element that sounds like a current product feature rather than a future aspiration.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `product-strategy-doc.md` | Vision informs the strategic choices made to pursue it |
| `product-principles.md` | Principles are derived from vision values |
| `north-star-metric.md` | The vision indicators become the north star metric framework |
| `investment-thesis.md` | Vision anchors the investor narrative |

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
