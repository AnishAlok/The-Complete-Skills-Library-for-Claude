# feature-announcement.md

> **Skill:** Produces feature release announcement copy for in-app notifications, customer emails, and changelog entries when shipping a new capability to existing users.

---

## TLDR

A feature announcement communicates a new capability to the users who will benefit from it: concise, benefit-led, and immediately actionable. Distinct from a product announcement in scope (one feature vs. a full product), audience (existing users who already understand the product vs. prospects who do not), and goal (adoption of something new vs. awareness and acquisition). This skill produces the in-app notification, the customer email, and the changelog entry.

---

## Topic Explanation

### Feature Announcements Are for Existing Users

Product announcements are for the market. Feature announcements are for people who already use the product.

This changes the writing entirely. You do not need to explain the product category, establish company credibility, or handle top-of-funnel objections. The user already bought. Now you need to answer three questions as efficiently as possible: what is new, does it help me specifically, and how do I use it?

### The Announcement Fatigue Problem

Existing users develop calibrated attention to feature announcements. They learn quickly whether a company's feature communications are worth opening. If a company announces every minor improvement with equal enthusiasm, users start filtering them out.

Reserve formal feature announcements for capabilities that meaningfully improve a workflow a significant portion of users depend on. Minor improvements belong in release notes and changelog entries, not email campaigns or in-app modals.

The goal: train users that when they receive a feature announcement from this product, it is worth opening.

### In-App vs. Email vs. Changelog

**In-app notification:** Appears in context when the user is in the product and would most benefit from knowing. Highest click-through rate because it appears at the moment of maximum relevance. Must be brief: 2 to 3 sentences maximum with one clear action. Never interrupt a critical workflow with a feature announcement.

**Customer email:** For significant features that justify proactive outreach. The email must give users a reason to leave whatever they are doing and go into the product. 150 to 200 words maximum. The CTA links directly to the feature, not to a blog post about it.

**Changelog entry:** The complete record for users who actively track changes. Technical detail is appropriate here. Also serves as searchable documentation for users who remember hearing about a feature but cannot find it.

---

## Output Format

```
IN-APP NOTIFICATION

Version A: Tooltip or popover (use for smaller, contextual features)
Headline: [5 to 7 words. Names the benefit, not the feature.]
Body: [1 to 2 sentences. What it does. Why it helps this user now.]
CTA: [Try it now / See how it works / Dismiss]

Version B: Modal (use for significant features that warrant deliberate attention)
Headline: [Benefit or new capability in 7 to 10 words]
Body: [2 to 3 sentences. The problem it solves. What is now possible.
How to access or enable it.]
Primary CTA: [Specific action — links directly to the feature]
Secondary: [Maybe later / Learn more]

Dismissal behavior: [closes permanently / reappears once / closes for this session]

---

CUSTOMER EMAIL

Subject A: [Feature name or direct benefit. Under 45 characters.]
Subject B: [Outcome or question angle. Under 45 characters.]
Preview text: [Adds information, does not repeat subject. Under 90 characters.]

[Salutation]

[Opening line: 1 sentence. The specific thing now possible that was not possible before.
Lead with the capability or outcome, not "We're excited to share..."]

[Body: 3 to 5 sentences.
Sentence 1-2: The problem it solves or the workflow it improves.
Sentence 3: What users can do now.
Sentence 4: How to find or enable it in the product.
Sentence 5 (optional): Any configuration, plan, or permission requirement.]

[CTA: Verb + specific destination. "See it in [Product Name]" with direct link.
Do not link to a blog post. Link to the feature itself.]

[Signature]

---

CHANGELOG ENTRY

Version: [X.X.X] | Released: [YYYY-MM-DD] | [Tier: Major / Minor / Patch]

[Feature Name]
[1 sentence summary of what it does and who it is for.]

[2 to 4 sentences of complete description:
What it does technically. How to access it. Any configuration required.
Any limitations, known edge cases, or rollout status (e.g., available to all plans / Pro and above).]

Documentation: [link]
Related entries: [links to related features or changelog entries if applicable]
```

---

## Starter Prompt

```
You are a product marketer writing a feature announcement for existing users.

Feature name: [name]
What it does: [plain-language description]
Problem it solves for existing users: [the specific workflow friction this addresses]
How to access or enable it: [where to find it in the product — be exact]
Target users: [which user types benefit most, and which plan or role it is available to]
Limitations or caveats: [what it does not yet do / known edge cases]
Rollout status: [available to all / rolling out to Pro+ / launching month/day]

Produce:
1. In-app notification in both tooltip and modal formats
2. Customer email with 2 subject line variations
3. Changelog entry

Lead every version with the benefit, not the feature name or "we're excited."
The email CTA must link directly to the feature, not to documentation or the blog.
The changelog entry must include any plan restriction or known limitation.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `product-announcement.md` | Use for full product launches; this skill is for individual feature releases |

| Use This Alongside | Why |
|---|---|
| `launch-plan.md` | Feature announcements may be a deliverable within a Tier 2 or 3 launch plan |

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
