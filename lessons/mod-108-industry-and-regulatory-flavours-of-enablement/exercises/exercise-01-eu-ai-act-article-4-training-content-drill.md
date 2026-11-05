# Exercise 01 — EU AI Act Article 4 Training Content Drill

**Estimated effort:** 3 hours
**Format:** three tier-level content outlines + content-update trigger matrix + scope-definition record, Markdown
**Grounding chapters:** [02 — EU AI Act Article 4 — Training Content at Depth](../02-eu-ai-act-article-4-training-content-at-depth.md); references [mod-101 Chapter 05](../../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md).

## Objective

Produce the four artifacts that together operationalize Article 4 training content for an EU-touching organization at the depth an instructional-design partner can build against and an auditor can read.

1. A **leadership-tier content outline** at the altitude the role actually teaches.
2. An **operator-tier content outline** with a role-specific sub-tier picked by the learner.
3. A **specialist-tier content outline** with the explicit hand-off to the adjacent AI Engineering curriculum.
4. A **content-update trigger matrix** with named owners and review windows.
5. A **scope-definition record** as a dated, signable artifact.

The drill is not the full curriculum — it is the drill that gets the curriculum structure right before instructional design builds it out.

## Prerequisites

- Chapter 02 read.
- [mod-101 Chapter 05](../../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md) read as the floor.
- Access to the [EU AI Act text](https://eur-lex.europa.eu/eli/reg/2024/1689/oj). Article 4 is short; read it in the official source.
- A chosen organization that has some EU-touching activity. If you don't have one in mind, pick one of:
  - A 6,000-person US-headquartered SaaS company with a 400-person EU engineering and sales presence across Dublin, Berlin, and Barcelona, no EU consumer customers but EU B2B customers and EU employees.
  - A 15,000-person US-headquartered financial services company with a 1,800-person London office post-Brexit and sales relationships with EU corporate clients.
  - A 3,500-person US-headquartered pharma / medical-device company with EU operations in Switzerland, Germany, and Belgium and EU clinical trials.

## Problem statement

Your head of AI governance has asked for the AI literacy slice of the organization's AI Act readiness program. Legal counsel will read; the organization's EU subsidiary leadership will read; the head of learning and development will read (they are the instructional-design owner). You have three hours. Produce the five artifacts above at the level where the instructional-design team can scope the build and legal can either sign the scope-definition record or redline it. The audience is competent readers, not an AI Act novice; do not pad.

## Requirements

### Part A — Three tier-level content outlines

For **each** of leadership, operator (with a role-specific sub-tier), and specialist, produce an outline that includes:

1. **Audience definition.** Named populations and headcount estimates; the operator role-sub-tier picks one specific role (customer-support representative, field sales, HR business partner, software engineer, financial analyst — pick one).
2. **Content outline.** Topic-by-topic, at the depth of two-to-three short bullets per topic. Not full modules — outlines.
3. **Duration envelope.** Initial-training minutes, annual-refresh minutes.
4. **Assessment shape.** What is measured, how, at what passing threshold.
5. **The written proportionality rationale.** One to two sentences in the regulator's own language — "the [tier] equips [audience] with [capability appropriate to context]." The sentence an auditor would read. Write it well.

### Part B — Content-update trigger matrix

A short table following the shape in Chapter 02. Rows cover at minimum:

- Approved-tool envelope change
- AUP or SOP revision
- EU AI Office or member-state authority guidance
- Serious-incident retrospective finding
- Member-state enforcement action (any deployer)
- Vendor model or capability change (material)
- Annual methodology review

Each row names: **trigger event**, **content reviewed**, **named owner of the trigger**, **review window** (calendar-day deadline).

### Part C — Scope-definition record

A signed, dated artifact that answers:

1. Which populations are in scope? (named, with headcount estimates and their location by country.)
2. The specific decisions on the four hard questions in Chapter 02 — contractors, outsourced operators, US-only employees whose output can reach EU data subjects, new-hire onboarding timing.
3. The signers: enablement lead, head of AI governance, general counsel, chief people officer or HR partner, head of the EU subsidiary (if the organization has one).
4. The dated-review clause — when this record reopens.

## Starter guidance

- The written proportionality rationale is the hardest sentence to write and the sentence an auditor will read most carefully. Spend five to ten minutes per tier on just the rationale. Avoid passive voice; avoid "comprehensive" and "robust" as filler.
- The operator role-sub-tier is the content-heavy portion of the drill. The sub-tier content is where the proportionality judgment lands — a customer-support representative handling EU customer inquiries has a different literacy obligation than a US-based software engineer. Make the content differ accordingly.
- The specialist tier should defer substantial content to the adjacent AI Engineering curriculum (applied-ai-engineer-learning, ai-risk-engineer-learning). Do not re-produce content that already lives in those tracks; reference and point.
- The trigger matrix's named-owner column is the one most programs leave blank. Fill it with role names (not person names) so the matrix survives staffing changes.
- The scope-definition record's hardest row is "US-only employees whose output can reach EU data subjects." The default from Chapter 02 is "scope wider." Document the specific reasoning your organization applies.
- Where a fact about the organization is load-bearing and you do not know it (headcount by country, the specific role titles in each BU, the existing training infrastructure), mark `<!-- needs-research: ... -->` inline. Do not invent.

## Deliverables

- `article-4-leadership-tier-outline.md`
- `article-4-operator-tier-outline.md` — explicitly naming the operator role-sub-tier.
- `article-4-specialist-tier-outline.md`
- `article-4-content-update-trigger-matrix.md`
- `article-4-scope-definition-record.md`
- A short cover note (3-5 sentences) summarizing the two hardest judgement calls you made in the drill and why.

## Acceptance criteria

- Each tier's outline has all five required sections.
- Each proportionality rationale is one to two sentences in the regulator's own language — not corporate-tone filler.
- The operator sub-tier content is materially different from the general operator tier; the sub-tier has at least three role-specific content lines.
- The specialist tier defers at least two content areas to the adjacent AI Engineering curricula with specific pointers.
- The trigger matrix has every required row with a named role-owner (not a person name) and a calendar-day review window.
- The scope-definition record answers all four hard questions with specific decisions; all signer roles are named (not left as "TBD").
- `<!-- needs-research: ... -->` is used wherever an organization-specific fact is missing.

## Stretch goals

- Write the three-sentence version of the leadership-tier proportionality rationale in the language of the EU AI Office's public communications, as if reading it in an enforcement letter. This sharpens the regulator-facing tone.
- Add a sixth artifact: a **non-completer policy** — what happens to a person in scope who has not completed the relevant tier within the required window. Access revocation? Manager escalation? Business-visibility-level reporting? This is the artifact most organizations skip and most regulators ask about.
- Add a **state-of-the-world one-pager** on the EU AI Office and member-state market-surveillance authority landscape at the time of drill — which authorities are active, what guidance they have published, what enforcement actions (if any) have landed. Mark the unknowns with `<!-- needs-research: ... -->` liberally; the one-pager is the live map, not the final answer.

## Why this exercise matters

Article 4 is the first deployer-side AI literacy obligation with teeth in a major jurisdiction. Most organizations' current AI training is marketing, not literacy. This drill runs the self-audit at the content-structure level — the level where the gaps become expensive to close later. The artifact set is also the foundation for the mod-104 curriculum build at the enterprise scale, and for Exercise 05 of this module's industry-adjusted curriculum.
