# Exercise 01 — Audience Segmentation and Fluency Target Map

**Estimated effort:** 2 hours
**Format:** one artifact of 1–2 pages (table-heavy), Markdown or docx
**Grounding chapters:** [01 — Literacy is the Frame; Training is the Vehicle](../01-literacy-is-the-frame-training-is-the-vehicle.md), [02 — Audience Segmentation and Fluency Targets](../02-audience-segmentation-and-fluency-targets.md)

## Objective

Produce the **fluency target map** — the one artifact that segments the in-scope population and names what fluency means for each segment. This is the first load-bearing artifact of the training program; the foundational curriculum, the role-based playbooks, the measurement stack, and the exec scorecard all cite it.

## Prerequisites

- Chapters 01 and 02 read.
- A specific, realistic organization to work against. If you don't have a real one, carry forward one of the three organizations used in [mod-101 Exercise 01](../../mod-101-role-and-the-org-wide-enablement-operating-model/exercises/exercise-01-the-one-page-role-scope-contract.md) so the artifacts stack:
  - a 3,000-person US bank with an existing head of AI governance and no CoE yet
  - a 12,000-person global pharma with an active CAIO and a mature governance program
  - a 500-person SaaS company with no governance function and a CAIO who is really the CTO wearing a second hat

## Problem statement

Your exec sponsor is about to sign off on the training program's budget for the year. Before they sign, they want "the map" — the segmentation decision, with numbers. Specifically: *who is in scope at what tier, what fluency target applies to each tier, and how will you know when they hit it.*

They have told you they are not signing off on a template. The artifact has to be about *this* organization and defensible to the auditor who will walk in after they sign.

## Requirements

Deliver one artifact with the following components. One page is ideal, two is acceptable; longer and you have drifted into a job description.

### 1. Population scoping (3–5 sentences)

A short preamble that answers:

- Who is in scope and who is not (contractors, offshore operators, board members, etc.).
- What the total in-scope population is (approximate numbers for your chosen organization).
- Any population-level caveats (e.g., a regulated subsidiary with a stricter standard).

### 2. The tier table

The core artifact. One row per tier (four rows for most organizations — leadership, operators, specialists, builders), with these columns:

| Column | What to put in it |
|---|---|
| Tier | Leadership / Operators / Specialists / Builders |
| Approximate headcount share | Percentage or absolute number for your org |
| Fluency intent | One sentence: *"an operator at this tier can ..."* |
| Named tasks | 3–6 tasks they should be able to perform fluently with AI assistance. Must be role-specific, not generic. |
| Assessment method | Knowledge check / rubric-scored artifact / behavioral indicator (which combination) |
| Pass bar | The explicit threshold |
| Refresh cadence | Annual + any triggering events |

### 3. Rationale paragraph (3–5 sentences)

One short paragraph that would satisfy an auditor asking *why* this segmentation is proportionate for your organization. Reference the regulatory floor from [mod-101 Chapter 05](../../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md) if your organization touches the EU.

### 4. One deliberate exception

Name at least one row where you have *deliberately* diverged from the generic four-tier template — for example, a sub-tier inside operators (regulated-workflow operators) because your bank has a materially different fluency expectation for them. The exception is proof you authored this for your organization, not from a template.

## Starter guidance

- The named-tasks column is the hardest. Fight the instinct to write generic tasks ("uses AI effectively in daily work"). A specific task for a service rep is "draft an on-brand reply to a tier-1 ticket in under 2 minutes with policy citations verified against the live SOP." That sentence is the start of a rubric.
- Headcount shares vary by organization. A 500-person SaaS company's distribution looks very different from a 12,000-person pharma. Do not import the illustrative percentages from Chapter 02 verbatim — reason about your own org.
- "Specialists" is the tier most organizations mis-scope. These are not senior ICs *generally* — they are senior ICs whose function is being *materially reshaped* by AI and who are expected to coach peers. If your map has 25% of the population as specialists, you have mis-scoped.
- The builder tier is mostly a *routing* row — small headcount share, entry criterion is "route into the AI Engineering or AI Governance curriculum," not "take our internal course."
- Use the deferral patterns from Chapter 01 and Chapter 06 explicitly: engineers and analysts at the IC level defer to the level-20 tracks, not your curriculum.

## Deliverables

- `fluency-target-map.md` (or `.docx`): the artifact above.
- A brief *exception note* at the bottom (3 sentences max) describing the deliberate divergence from the generic template and why.

## Acceptance criteria

- One or two pages at normal body-text size. Table-heavy, not paragraph-heavy.
- The population scoping names in-scope and out-of-scope explicitly.
- Every tier row has all seven columns filled in with content that would survive a director-level review.
- The named-tasks column is specific enough that you could author a rubric from it in Exercise 06.
- The rationale paragraph makes a defensible proportionality argument.
- At least one row shows a deliberate, organization-specific deviation from the generic template.

## Stretch goals

- Produce a second version of the map for a counter-factual organization (e.g., if you wrote it for the SaaS company, write a one-page version for the pharma) and compare the differences in a three-bullet note. This is good practice for the real moment when you join a new organization.
- Add a "transition" column showing how a person moves between tiers (operator to specialist, specialist to builder). Name at least one concrete progression path.
- Compare one tier's named-tasks list against a real job description from LinkedIn or a company careers page for that role. Note where the official job description underweights the AI tasks your map names.

## Why this exercise matters

Every downstream artifact in this module — the foundational curriculum (Exercise 02), the role-based playbook (Exercise 03), the measurement rubrics (Exercise 06) — references this map. If the map is wrong, the downstream artifacts inherit the error. Writing this one first and keeping it short pays compound returns.
