# Audience Segmentation and Fluency Targets

> Fluency is not uniform. A board chair, a service representative, a senior legal reviewer, and an engineer configuring a RAG pipeline all need "AI fluency" — but the content, the depth, and the measurable target for each are different. The audience-segmentation decision is the one that saves you from spending the biggest line item in your budget on a course nobody is well-served by.

## The four tiers

Chapter 01 named them. This chapter is the definition.

| Tier | Who's in it | What fluency looks like | Headcount share (typical) |
|---|---|---|---|
| **Leadership** | Executives, VPs, senior people managers with budget authority | Can govern. Reads the scorecard. Decides on risk posture. Knows what to escalate. | 2–5% |
| **Operators** | Every employee or contractor using an approved AI tool in their day work | Can do named tasks fluently with AI assistance. Verifies. Escalates when the signal says to. | 80–92% |
| **Specialists** | Senior ICs whose function is being materially reshaped by AI: legal reviewers, senior analysts, L&D designers, enablement partners, champions, auditors | Carries pattern libraries for their function. Coaches peers. Feeds the champion network. | 5–12% |
| **Builders** | People commissioning, configuring, administering, red-teaming, or building AI systems | Technical AI depth. Mostly served by the AI Engineering and AI Governance curricula, not yours. | 0.3–2% |

The ranges are starting figures based on how most mid-size enterprises end up distributed after the first literacy cycle. Your organization's distribution depends on its industry, its automation posture, and how far the toolset has been pushed into regulated work. <!-- needs-research: refresh these ranges against the most recent McKinsey State of AI and Deloitte State of Generative AI in the Enterprise cycles, 2026 editions. -->

The design error to avoid: splitting the budget evenly across the tiers. Operators are the largest audience by an order of magnitude — most of the budget, most of the delivery capacity, most of the measurement effort belongs there. Leadership gets a small, high-signal program. Builders are mostly a *routing* line item, not a teaching line item.

## What each tier needs — the content shape

The content shape differs by tier. Name the intent per tier before picking any specific course or workshop format.

### Leadership tier — literacy to govern

Content is short, high-density, and framed around decisions the tier actually makes. The leadership tier is the one most often *over-taught* on technical depth and *under-taught* on governance literacy. Fix the direction.

Covers:

- What the technology is and is not (one honest page; no demos that imply more than the tech does).
- The organization's own AI posture — what was approved, what was deferred, what was prohibited and why.
- How to read the executive scorecard ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md)).
- The three or four decisions the tier is uniquely responsible for (approving a tool for the envelope, approving a rollout, signing a policy, pulling a kill switch on a program).
- The escalation path — who they call when something smells wrong.

Format: 60–90 minutes live (a workshop or executive briefing) plus a two-page reference card. Not an LMS course.

### Operators tier — literacy to do real work

This is the biggest tier and the hardest one to get right. The common failure is teaching operators "how to prompt an LLM" when what they need is "how to do the three tasks I do every day with AI assistance, and how to notice when I shouldn't."

Covers:

- The approved-tool envelope for *their* role — not the full org catalog.
- The data-handling SOP in operator voice — what they can paste, what they cannot, where to escalate.
- Role-specific prompt patterns and verification habits (Chapter 04 is where this is built out).
- The two or three escalation signals most relevant to their function.
- A short "working with AI without becoming dependent on it" module — the habits that protect skill-atrophy on the IC side.

Format: a 60–90 minute foundational module (synchronous or self-paced), followed by role-based playbook content delivered in 15–45 minute chunks, with office hours and a prompt-coaching clinic as the in-the-flow support.

### Specialists tier — literacy to coach and extend

Specialists are the force-multiplier tier — the champion network draws from here. The content assumes operator fluency already and adds:

- Deeper pattern libraries for their function, including failure modes.
- A function-specific use-case backlog with worked examples.
- How to coach peers through a prompt (you are training the trainers here).
- Signal interpretation: when a prompt isn't working, what to change.
- The routing playbook: when to send a colleague to the builder tier instead of helping yourself.

Format: cohort-based. A bootcamp (half-day or two-day) is appropriate for this tier. Recurring community of practice meetings hold them together after.

### Builders tier — literacy to build responsibly

This tier mostly *defers out* of your curriculum. You are not teaching them to build — you are making sure the handoff to the AI Engineering and AI Governance tracks happens cleanly.

What you own for this tier:

- Enrollment routing to the right external / internal curriculum (`applied-ai-engineer`, `agentic-ai-engineer`, `ai-risk-engineer`, etc.).
- The organization's commissioning process from [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md) — builders need to know how to accept and interpret a commissioning brief.
- The governance obligations builders inherit by virtue of operating inside your org (policy, data classes, incident pathway).

Format: a short "builder onboarding" artifact, usually 2–3 hours live, plus a routing table.

## Fluency targets — making "sufficient" measurable

"Sufficient" is the regulatory word (Article 4). "Measurable" is the enablement-lead word. For each tier, fluency targets have three layers.

### Layer 1 — knowledge check

The lowest layer. Can the person, after the content, answer a short set of questions? For leadership this looks like case-based scenarios ("a VP escalates X; what do you do?"). For operators it is a role-specific quiz grounded in the policy and the role's workflow. For specialists it is scored short-answer against a rubric. The threshold is published; typical pass bars are 80% on the knowledge check, with a retake if missed.

Limit: a knowledge check does not prove anyone can *do* anything with AI. It proves they completed the content and retained the propositional knowledge. It is necessary and insufficient.

### Layer 2 — task-level proficiency

The layer that matters. For each tier, name three to six *tasks* that the tier should be able to perform fluently with AI assistance, and define a rubric for each task. Chapter 07 treats the rubric design in full. The point to hold here: the fluency target is a sentence of the form "an operator at this tier can perform [named task] with AI assistance, produce output that meets [named rubric] at [named quality bar], within [named time]."

For the operator tier, the three-to-six tasks should come straight from the role-based playbook. For a customer service representative they might be: "draft an on-brand reply to a tier-1 ticket," "summarize a 14-day case history for handoff," "classify an inbound ticket into the correct queue." The literacy target is fluency on *those tasks*, not fluency on generic chat.

### Layer 3 — behavioral indicators

The layer that holds the program accountable to behavior change. Examples:

- Operators who complete the curriculum demonstrate a measurable shift in which tools they use for which tasks.
- Specialists who complete the bootcamp contribute to the use-case library within a defined window.
- Leadership who complete the briefing exercise their escalation path at least once per cycle (tabletop or real).

These indicators are read from the systems of record you already have (ticketing, LMS, the use-case library, the incident log). They are the bridge from literacy to outcome and the data the exec scorecard in [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) draws on.

## The segmentation artifact — the fluency target map

The output of Chapter 02 is one artifact: the **fluency target map**. It is a table with:

- One row per tier (four rows) or per role within a tier if your organization has enough variation to justify it.
- Columns for: in-scope population, fluency intent sentence, named tasks (3–6), rubric reference, assessment method, pass bar, refresh cadence.

Keep the map on one or two pages. If it is longer, you are describing jobs, not literacy targets. Exercise 01 asks you to draft this artifact.

Rev the map annually at minimum, or whenever a change in the approved-tool envelope or the data-handling SOP shifts what "fluency" means for a tier. The rev history is itself audit-relevant.

## Common segmentation mistakes

Three recurring mistakes, named so you can avoid them.

1. **Segment by department instead of by relationship to AI.** "Sales" and "service" are not useful literacy tiers. The *operator in sales* and the *specialist in sales* need different content. Segment by the tier definition first, then layer the role-based playbooks (Chapter 04) on top.
2. **Give the leadership tier the operator curriculum.** Executives who sit through a 90-minute operator workshop learn nothing they use. Design a tier-specific artifact; the time cost is part of what you are respecting.
3. **Treat "builder" as a title, not a function.** An analyst who wires up an internal agent for their team is doing builder work and inherits builder obligations, even if their job title is "senior analyst." Route them into the builder-onboarding artifact; do not rely on titles.

## Where this chapter feeds

- [Chapter 03](03-the-foundational-ai-literacy-curriculum.md) builds out the operator-tier foundational curriculum the map points at.
- [Chapter 04](04-role-based-playbooks-and-use-case-libraries.md) builds the role-level playbooks that sit on top of the foundational curriculum.
- [Chapter 07](07-measuring-fluency-growth.md) builds out the rubrics and assessments referenced in Layer 2 and Layer 3.
- Exercise 01 produces the fluency target map as a deliverable.

## Summary

- Four tiers — leadership, operators, specialists, builders — with a heavily skewed headcount distribution. Budget accordingly.
- Each tier has a distinct content shape, format, and set of decisions it needs to make.
- Fluency has three measurable layers: knowledge check, task-level proficiency, behavioral indicator. The second is the one that makes the program defensible.
- The artifact for this chapter is the **fluency target map** — one or two pages, one row per tier or role, revised annually or when the toolset changes.
- Segment by relationship to AI first, department second. A title is not a tier.
