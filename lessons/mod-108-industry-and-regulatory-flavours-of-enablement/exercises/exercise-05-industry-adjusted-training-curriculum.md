# Exercise 05 — Industry-Adjusted Training Curriculum

**Estimated effort:** 4 hours
**Format:** curriculum outline across the three tiers + role-specific sub-tier + assessment and evidence design, Markdown
**Grounding chapters:** [02 — EU AI Act Article 4 — Training Content at Depth](../02-eu-ai-act-article-4-training-content-at-depth.md); the chosen industry chapter among [03](../03-healthcare-flavour-hipaa-and-phi.md) / [04](../04-finance-flavour-sr-11-7-and-finra.md) / [05](../05-legal-engineering-flavour.md) / [06](../06-education-flavour-ferpa-coppa-and-ed-tech.md); [07](../07-enablement-vs-governance-responsibility-split.md). Required prior reading: [mod-104](../../mod-104-training-programs-and-ai-literacy-curriculum/README.md) for the industry-neutral curriculum skeleton.

## Objective

Produce the industry-adjusted version of the mod-104 training curriculum for the same industry and organization you used in Exercise 04. The curriculum is not the full module build — it is the outline-level design an instructional-design partner would build from and an industry counterpart would redline. Specifically:

1. **Industry-adjusted leadership tier outline** — the content the industry adds on top of the Article 4 leadership shape.
2. **Industry-adjusted operator tier outline** — including at least one role-specific sub-tier that the industry's regulatory surface forces.
3. **Industry-adjusted specialist tier outline** — with explicit hand-offs to the adjacent curricula.
4. **Assessment design** — what is measured, how, with thresholds, including the industry-specific scenario-based component.
5. **Evidence catalog** — what gets stored, where, who retrieves it, including the industry-specific evidence an auditor will read.

## Prerequisites

- Chapter 02 read; the industry chapter read; Chapter 07 read.
- mod-104 read.
- Exercise 04 of this module completed (or an equivalent policy artifact set to teach against) — the curriculum teaches people how to operate *the policies in Exercise 04*, so the two are a pair.
- The same organization and industry used in Exercise 04.

## Problem statement

The policy package from Exercise 04 is in walking-redline cycle with the industry counterpart. In parallel, the head of learning and development (the instructional-design owner) has asked for the curriculum outline that the policy package will be taught with. The industry counterpart will co-sign the curriculum shape before instructional design builds it out. You have four hours. Produce the five artifacts above at the level where instructional design can scope the build (hours, content-production-labor estimate, delivery-mechanism mix) and the industry counterpart can read the outline and either sign or redline it.

## Requirements

### Part A — Three tier-level curriculum outlines

For each tier, provide:

1. **Audience definition.** Named populations with headcount estimates, including the role-specific operator sub-tier required by the industry.
2. **Content outline.** For each tier, six to ten topic areas, each with two-to-three concrete bullets. At least four of the topic areas must be industry-specific — would not appear in the generic mod-104 shape. The Article 4 foundation is assumed; focus the content outline on the industry overlay.
3. **Duration envelope.** Initial-training minutes, annual-refresh minutes, trigger-driven update minutes (when the policy changes, when regulator guidance updates, when a peer-organization enforcement action lands).
4. **Delivery mechanism.** E-learning vs. instructor-led vs. role-play vs. scenario-walkthrough — the mechanism matched to the content type.
5. **The written proportionality rationale.** One to two sentences in the regulator's own language naming the tier and its audience; flavoured for the industry — "appropriate to the [role]'s context as a [industry-specific role description] under [specific regulatory obligation]."

Operator-tier role-specific sub-tier: pick one role from the industry that has a regulated role-sub-tier (credit analyst at a bank; registered representative at a broker-dealer; clinician at a healthcare organization; attorney in the legal function; teacher at an institution). The sub-tier outline is materially distinct from the general operator tier — at least three content items are specific to the role's regulatory surface.

### Part B — Assessment design

A short document covering:

- **What is measured, by tier.** Knowledge, judgment, operational competence — at the specific altitude each tier requires.
- **How it is measured.** Multiple-choice, scenario-based attestation, prompt-and-review exercise, simulation.
- **Passing thresholds.** Stated numerically with rationale; higher thresholds for regulated-role sub-tiers than for the general operator tier.
- **Industry-specific scenario-based component.** At least three scenarios flavoured to the industry's regulatory surface — a clinician considering whether to paste a patient note into a tool; a credit analyst asked to use AI output in an adverse-action rationale; an attorney considering whether a specific tool preserves privilege; a teacher considering whether to use a tool on student work. Each scenario has an evaluation rubric.
- **Non-completer handling.** The specific policy on operators (including industry-specific roles) who have not completed required training within the window.

### Part C — Evidence catalog

A short table listing every piece of evidence the curriculum produces that an auditor can read. For each row:

- Evidence name (e.g., "Clinician-tier module, v1.0; attestation record").
- What it is (one line).
- Where it lives (system name, link, path).
- Who maintains it (role).
- Who retrieves it without the enablement lead in the room (role).
- The regulatory question it is the evidence for (HIPAA workforce-training obligation; SR 11-7 training expectations; FERPA professional-development evidence; Article 4 literacy obligation; ABA Rule 1.1 technological-competence demonstration).

At minimum, 10 rows. Each row names a specific regulator's expectation the evidence meets.

## Starter guidance

- Begin with the Article 4 shape from Chapter 02. The industry content is the overlay; do not re-derive the shape.
- The leadership tier is often where the industry overlay lands most visibly — regulatory posture, exam history, enforcement landscape. Write content at this altitude as if briefing an audit committee.
- The operator-tier content is the mass of the curriculum. The regulated-role sub-tier is the content-heavy part; spend at least a third of the drill time on it.
- The specialist tier should defer substantial content to the adjacent AI Engineering or governance curricula. The industry overlay is still present (SR 11-7 depth for the bank's risk engineer; HIPAA Security Rule depth for the healthcare specialist), but much of the technical content is in `ai-risk-engineer-learning` and should be referenced rather than duplicated.
- The scenario-based assessments are the hardest and most valuable part of Part B. Write scenarios that are realistic for the industry and that have ambiguous features — a good scenario has multiple plausible answers until the regulatory rule disambiguates.
- The evidence catalog is where exercises land the exercise-01 Article 4 shape in a regulated-industry context. Each row should name a specific regulatory question the evidence meets.
- Where an organizational fact is load-bearing and you do not know it (current curriculum investment, L&D partner capacity, LMS platform, existing industry-specific training programs), mark `<!-- needs-research: ... -->` inline. Do not invent.

## Deliverables

- `curriculum-leadership-tier.md`
- `curriculum-operator-tier.md` — including the regulated-role sub-tier.
- `curriculum-specialist-tier.md`
- `curriculum-assessment-design.md`
- `curriculum-evidence-catalog.md`
- A short cover note (3-5 sentences) summarizing the two hardest judgment calls in the industry overlay and why.

## Acceptance criteria

- Every tier has all five required sections.
- At least four content items per tier are industry-specific (would not appear in the generic mod-104 shape).
- The operator-tier regulated-role sub-tier has at least three content items that are specific to the role's regulatory surface.
- Proportionality rationales use the regulator's own language and are specific to the industry.
- Assessment design has at least three industry-specific scenario-based items with evaluation rubrics.
- Evidence catalog has at least 10 rows; each row names a specific regulator's expectation.
- Non-completer handling is specific, not abstract.
- `<!-- needs-research: ... -->` used where organizational facts are unknown.

## Stretch goals

- Write a **curriculum-coupling note** showing how the curriculum updates when the Exercise 04 policy package changes — specific trigger types, specific content areas that get re-reviewed, specific windows.
- Produce a **three-year curriculum calendar** for the industry showing the initial-build cadence, the first-year refresh, and the annual methodology review — with industry-specific triggers marked (regulator exam year, new state-law effective dates, etc.).
- Draft the **two-paragraph version** of the curriculum rationale that the head of AI governance would use with the audit committee to demonstrate Article 4 compliance *through* the industry's regulatory surface. The audience is competent regulators, not consumer-marketing readers.

## Why this exercise matters

Curriculum design is the content-depth half of the enablement role in a regulated industry. The policy package from Exercise 04 names what operators must do; this curriculum teaches them how to do it defensibly. The pair is what a regulator reads during a workforce-training inquiry: here is the policy, here is the training that teaches the policy, here is the evidence that the training happened. Producing the pair under a four-hour budget — enough to design well, not enough to over-produce — is calibration for the real role, where the pair is produced across weeks under the walking-redline cadence of the industry counterpart.
