# product-announcement.md

> **Skill:** Produces a product announcement for publishing as a blog post and sending as a launch email, written in a customer-facing voice that builds understanding, generates excitement, and drives initial adoption.

---

## TLDR

A product announcement translates the press release into a customer-facing narrative: warmer in tone, deeper in benefit explanation, and focused entirely on what the product means for the reader. This skill produces both the blog post and the launch email: two distinct documents for the same news event, each written for its specific channel and reading context.

---

## Topic Explanation

### Three Documents, Three Audiences

Press release: journalists and analysts. Formal, AP style, inverted pyramid, executive quotes.

Blog post announcement: existing customers, prospects, SEO audience, social media sharers. Narrative-led, problem-first, benefit-focused, conversational.

Launch email: current subscribers and customers. Short, personal, one CTA, directly actionable.

All three reference the same product launch. None of them should read like the others.

### Why "Today We Are Excited to Announce" Fails

Announcements that open with the company's excitement ask the reader to do cognitive work: connect a product they know nothing about to their own situation and decide whether to care.

Announcements that open with the reader's situation create immediate recognition. The reader identifies themselves in the description and is already invested before the product is named.

The structural principle: earn the right to introduce the product by first demonstrating that you understand the problem it solves.

### Blog Post Length and SEO

Product announcement blog posts serve two purposes: customer communication and long-term SEO. The combination means they benefit from more depth than a press release but must remain readable for humans scrolling casually.

Target 600 to 900 words for a feature announcement, 900 to 1,400 words for a major product launch. Use headers for skimmers. Lead every section with the most important sentence in case the reader stops there.

---

## Dos

- **Do lead with the problem, not the product name.** The product name should appear for the first time in paragraph two, after the problem has been established.
- **Do frame every capability as a customer outcome.** "You can now [do X]" not "Feature Y enables users to [do X]."
- **Do include one CTA only.** Multiple CTAs dilute each other. Decide whether this launch is driving trial, demo bookings, or documentation reads, and optimize everything for that one action.

---

## Donts

- **Dont write the blog post as a press release.** Different structure, different voice, different purpose. A blog post can have a point of view. A press release cannot.
- **Dont send the same copy to customers and prospects.** Customers know the product and need to understand what has changed. Prospects need the broader context of what the product is.

---

## Output Format

```
BLOG POST ANNOUNCEMENT

Headline: [Problem-led or outcome-led. Not "Introducing [Product]."
Not "We're excited to announce." A headline that makes the target reader
want to read because it describes their situation or a result they want.]

Subhead: [One supporting sentence. Adds information rather than repeating the headline.]

[Opening paragraph: the problem. 2 to 3 sentences. Write about the reader's experience.
Be specific and accurate. Create recognition before creating interest.
Do not mention the product. Do not mention the company. Just the problem.]

[Paragraph 2: the product arrives as the answer.
"Today we're launching [Product Name] to solve exactly that."
Or: "That's what [Product Name] is built for."
The transition from problem to product should feel earned, not abrupt.]

[Paragraphs 3 to 4: what it does. 3 key capabilities described as customer outcomes.
Structure: "With [Product Name], you can now [outcome]."
Not: "The [Feature] module provides [functionality]."]

[Customer or beta user quote: in their natural voice. 2 to 3 sentences.
Describes the specific impact on their work, not the product's features.]

[Paragraphs 5 to 6 (optional depth section): integration details, configuration options,
which plan it is available in, or what makes it technically interesting.
Reward the reader who wants more without punishing the one who skims.]

[Availability and pricing paragraph: when it is available, where to find it,
what it costs or which plan it is in. Specific and complete.]

[CTA paragraph: one action. Make it specific.
Not "Learn more." Specify what happens when they click:
"Start your free 14-day trial," "Book a 20-minute demo,"
"Read the documentation and try it today."]

---

LAUNCH EMAIL

Subject line A: [Direct benefit. Under 50 characters.]
Subject line B: [Curiosity gap or question. Under 50 characters.]
Subject line C: [Social proof or urgency angle. Under 50 characters.]
Preview text: [Adds new information, does not restate subject. Under 90 characters.]

[Salutation — personalized by first name where list allows]

[Opening: 1 sentence. The news and its direct relevance to this reader.
If the list can be segmented, this sentence should reference what they already use or do.]

[Body: 3 to 4 sentences. What it does, what it means for them,
how to get to it. Short sentences. One idea per sentence.]

[CTA: action verb plus specific outcome. Linked. Not described as a button.
"Start your free trial →" / "See it in [Product Name] →"]

[Closing line: warm, first-name sign-off. Not corporate.]

[First name]

P.S. [Optional: one additional piece of information for the most engaged readers.
A secondary feature, a piece of social proof, or a time-limited offer.]
```

---

## Starter Prompt

```
You are a product marketer writing a product announcement.

Product name: [name]
What it does: [plain-language description]
Target audience: [who this announcement is for — be specific]
The problem it solves: [the specific pain this addresses, in the reader's language]
Key capabilities (3): [the most important things it does, stated as customer outcomes]
Customer result or quote: [early evidence of value if available]
Pricing and availability: [when and how to get it, what it costs]
Primary CTA: [the single action this announcement should drive]
List segmentation available: [can the email be personalized or targeted by segment?]

Write both a blog post announcement and an email announcement.
The blog post headline must lead with problem or outcome, not the product name.
Every capability must be stated as what the reader can now do, not what the feature does.
The email must include 3 subject line variations with distinct angles.
One CTA only in each document.
```

---

## Related Skills

| Use This Alongside | Why |
|---|---|
| `press-release.md` | Press release is the formal record; this is the customer narrative |
| `feature-announcement.md` | Use for individual feature announcements within an existing product |
| `launch-plan.md` | Blog post and email are deliverables in the Content and Email workstreams |

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
