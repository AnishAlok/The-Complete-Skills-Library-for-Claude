# product-strategy-doc.md

> **Skill:** Produces a product strategy document that translates vision into specific strategic choices: which bets to make, which markets to prioritize, which capabilities to build, and which tradeoffs to accept.

---

## TLDR

This skill helps you answer: *"Given where we want to go, what specific choices are we making about where to focus and what to deprioritize?"* A product strategy document makes the choices explicit so teams can make aligned decisions without relitigating direction in every meeting. Used annually or at major strategic inflection points.

---

## Topic Explanation

### Strategy Is About What You Choose Not to Do

Michael Porter's foundational insight on strategy: competitive advantage comes from choosing a different set of activities than your competitors. A strategy that tries to do everything is not a strategy. The choices you do NOT make are as strategically important as the ones you do.

A product strategy document must be explicit about what is being deprioritized and why. A strategy that does not rule anything out is not a strategy.

### The Three Levels of Strategic Choice

**Where to play:** Which markets, customer segments, and use cases to pursue. Which to ignore.

**How to win:** What the product must do better than alternatives to succeed in the chosen space. The basis of competition.

**What to build:** Which capabilities must be developed to support where-to-play and how-to-win choices. The investment thesis.

These three levels form a coherent hierarchy. If "where to play" and "how to win" change, "what to build" must change accordingly.

### Good Strategy / Bad Strategy (Richard Rumelt)

Richard Rumelt's *Good Strategy Bad Strategy* is the most rigorous framework for thinking about what strategy actually is. His "kernel of strategy" has three parts:

**Diagnosis:** The specific challenge or obstacle that strategy must address. Not a generic description of the situation, but the precise crux of the problem.

**Guiding policy:** The approach or method the strategy takes to address the diagnosis. This is the "how" at the strategic level.

**Coherent actions:** The specific commitments, resource allocations, and initiatives that implement the guiding policy. These actions reinforce each other.

Rumelt's most important critique of bad strategy: it is "fluffy." Goals dressed up as strategy ("we will be the leader in X") are not strategy. Strategy explains how the goal will be achieved.

---

## When to Use This Skill

Use when:
- Annual or bi-annual strategic planning cycle
- Major market shifts requiring strategic reassessment
- Post-funding round when resources and expectations change
- A new product leader joins and needs to establish strategic direction
- Team alignment has broken down on what to prioritize and why

---

## Dos

- **Do make the choices explicit.** The strategy should explicitly state what is being prioritized AND what is being deprioritized. A strategy with no deprioritization is a wish list.
- **Do articulate the basis of competition.** How does this product win? What does it do better than any alternative? This is the core of strategy.
- **Do connect strategy to vision.** Every strategic bet should connect to the vision it serves.
- **Do include the bets being made.** Strategies rest on assumptions about the market, technology, and customer behavior. Making these assumptions explicit enables learning and adjustment.
- **Do assign timeframes to strategic priorities.** "This year's focus is X" is more useful than "we prioritize X."

---

## Donts

- **Dont write a strategy that could apply to any company.** "We will provide excellent customer service, build great products, and grow our user base" is not a strategy.
- **Dont conflate goals with strategy.** "Reach $10M ARR" is a goal. The strategy explains how.
- **Dont include a comprehensive roadmap in the strategy.** The strategy identifies which capabilities to build. The roadmap specifies what to build and when.

---

## Output Format

```
1. STRATEGY HEADER
   Time period, version, author, last reviewed, status.

2. VISION ANCHOR
   One-sentence reminder of the vision this strategy serves.

3. STRATEGIC DIAGNOSIS
   The specific challenge or opportunity that strategy must address.
   What is the crux of the problem?
   What changes in the market, competitive landscape, or customer behavior
   make this the right moment for these choices?

4. WHERE WE PLAY
   Which customer segments we are pursuing in this period.
   Which geographies or verticals.
   Which use cases.
   EXPLICITLY: who we are not pursuing and why.

5. HOW WE WIN
   The basis of competition: what we must do better than any alternative.
   Why customers will choose us over alternatives.
   Our durable source of advantage.

6. STRATEGIC BETS (the key investments)
   For each bet (3 to 5):
   - The bet: what we are committing to build or do
   - The hypothesis: what must be true for this bet to pay off
   - The investment required: team, time, resources
   - The evidence that would confirm or invalidate it
   - Connection to where-to-play and how-to-win

7. WHAT WE ARE DEPRIORITIZING
   Explicit list of things we are choosing NOT to do in this period.
   Brief rationale for each.
   This section is as important as the bets section.

8. REQUIRED CAPABILITIES
   What we must build or acquire to execute this strategy.
   Which capabilities we have vs. which we need to develop.

9. KEY RISKS AND MITIGATIONS
   The 3 to 5 most important risks to this strategy.
   What could make the strategy wrong?
   How we are monitoring and mitigating each risk.

10. SUCCESS METRICS
    How we will know the strategy is working.
    Leading indicators that confirm strategic direction.
    Timeline for reviewing and adjusting.
```

---

## Starter Prompt

```
You are a product leader writing a product strategy document.

Vision anchor: [the vision this strategy serves]
Time period: [annual / bi-annual / other]
Strategic context: [current market situation, competitive dynamics, company stage]
Where we play choices: [which segments, markets, or use cases to focus on]
How we win: [the basis of competition]
Strategic bets: [the 3 to 5 key investments being made]
Explicit deprioritizations: [what is being set aside]
Key risks: [what could make this strategy wrong]

Please produce a complete product strategy document including:
1. Strategic diagnosis with specific crux of the challenge
2. Where-to-play with explicit exclusions
3. How-to-win with durable advantage articulation
4. Strategic bets with hypotheses and success criteria
5. Explicit deprioritization list with rationale
6. Required capabilities assessment
7. Key risks and mitigations
8. Success metrics with leading indicators

Every bet should connect to the vision.
The deprioritization section should be as specific as the bets section.
Flag any section that reads as a goal rather than a strategic choice.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `product-roadmap.md` | Strategy translates into roadmap priorities |
| `product-vision-doc.md` | Vision is the anchor this strategy serves |
| `okr-framework.md` | Strategy goals become the basis for OKRs |
| `feature-prioritization.md` | Strategy provides criteria for feature prioritization |

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
