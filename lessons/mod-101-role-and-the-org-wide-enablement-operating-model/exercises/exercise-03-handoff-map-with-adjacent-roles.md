# Exercise 03 — Handoff Map with Adjacent Roles

**Estimated effort:** 2 hours
**Format:** one diagram + one accompanying page of labeled handoffs
**Grounding chapters:** [04 — Handoffs with Adjacent Roles](../04-handoffs-with-adjacent-roles.md)

## Objective

Draw the handoff map for the AI Enablement Lead role at your chosen organization — the four load-bearing handoffs from Chapter 04 (down to `ai-augmented-team-manager`, sideways to `ai-governance-analyst` and `ai-risk-engineer`, up to `head-of-ai-governance`) — and label every arrow with the specific artifact, metric, or decision that crosses it this quarter.

The failure mode this exercise defends against: handoff lines that exist on the org chart but carry nothing real, and therefore degrade into "collaboration meetings."

## Prerequisites

- Chapter 04 read.
- The chosen organization from Exercises 01 and 02 (consistency matters — the handoffs change with the CoE shape).
- A rough sense of whether the organization actually has each of the four adjacent roles today. If it does not, you will name a proxy (e.g., "no `head-of-ai-governance` exists yet; the privacy officer is acting in the role").

## Problem statement

You are joining a cross-functional working group in week 4 of the role. The group has agreed that "we need better handoffs with governance." Everyone has a different idea of what that means. You have been asked to bring a diagram to the next meeting that makes the handoffs concrete.

## Requirements

### Part A — The diagram

A single diagram (whiteboard photo, ASCII, Mermaid, or your preferred drawing tool). It shows, at minimum:

- You at the center.
- The four adjacent roles from Chapter 04 — `ai-augmented-team-manager` (down), `ai-governance-analyst` (sideways-down), `ai-risk-engineer` (sideways-peer), `head-of-ai-governance` (up). If the organization uses different internal titles, use the internal titles and note the mapping.
- Bidirectional arrows between you and each adjacent role.
- A separate "plug-in" area with the arrows that exist but are not load-bearing (legal, security/IAM, finance, applied-AI engineers, executive sponsor). These can be stylized differently (dashed arrows, faded lines) so the four load-bearing handoffs stand out.

### Part B — The label sheet

For each of the four load-bearing handoffs, write a two-column list:

- **You hand them** — at least three specific artifacts, metrics, or decisions.
- **They hand you** — at least three specific artifacts, metrics, or decisions.

Each line should be *nameable*. "Draft acceptable-use policy v2026.3 for redline" is nameable. "Policy input" is not. If you cannot name a specific artifact, write `<!-- needs-definition: ... -->` rather than a vague placeholder, and flag it for the working group.

### Part C — The failure walk-through

Pick one of the four handoffs. Write a short (5–8 sentences) walk-through of one realistic failure scenario — what breaks if this handoff is only an org-chart line — and the specific change that would prevent it.

## Starter guidance

- Use the sketch in Chapter 04 as the *shape*, not the content. Your organization's handoffs will differ in which artifacts actually cross.
- For organizations without a formal `head-of-ai-governance`, pick the role that acts in that chair today (often the Chief Privacy Officer, General Counsel's AI delegate, or the CISO wearing a second hat). Note it on the diagram.
- The `ai-risk-engineer` handoff is the one most often missing in less-mature organizations. If your organization does not have one, write what the handoff *would* look like once it exists, and flag the dependency.
- For the "they hand you" column on the `ai-augmented-team-manager` handoff, make sure you name *field signal* — the thing most team managers forget they owe you, and the thing you cannot run the operating model without.
- A labeled arrow with no artifact this quarter is not a handoff yet; mark it as an aspiration and plan to backfill in a later quarter.

## Deliverables

- `handoff-map.*` — the diagram.
- `handoff-labels.md` — the four handoffs with "you hand them / they hand you" pairs, three specific items each direction.
- `handoff-failure-walkthrough.md` — the 5-8 sentence failure scenario and the specific preventive change.

## Acceptance criteria

- The diagram distinguishes the four load-bearing handoffs from the plug-in arrows visually.
- Every "you hand them" / "they hand you" item is a concrete artifact, metric, or decision — not a verb-of-collaboration.
- At least one handoff has a visible gap (an arrow that is aspirational or an adjacent role that does not yet exist) and that gap is flagged, not hidden.
- The failure walk-through is specific enough that a reader could predict the symptom in advance (e.g., "a champion-reported prompt-injection surfaces in week 6, we have no red-team evidence to cite, the governance council pulls the rollout because we cannot defend it").
- The diagram makes sense to a cross-functional colleague who did *not* read Chapter 04.

## Stretch goals

- Add a *second* diagram showing the handoffs as they'll look at **month 12** — what new roles are hired, which aspirational arrows have gone live, which plug-in arrows have been formalized.
- For each of the four handoffs, name the single **cadence** (weekly triage? monthly review? quarterly operating ritual?) that keeps it alive. A handoff without a cadence is a handoff that decays.
- For the `ai-risk-engineer` handoff, write the short "one-page red-team evidence request" template you would send them before the next rollout decision. (This is a preview of [mod-109](../../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) and [mod-102](../../mod-102-selecting-and-rolling-out-ai-tools/README.md); even a rough first cut is useful.)

## Why this exercise matters

Most AI enablement programs stall at the handoffs, not at the delivery. The team manager doesn't feed field signal back. The governance analyst becomes a courier instead of a partner. The risk engineer is called after a rollout decision instead of before. Drawing the map — with specific labels — is how you turn org-chart lines into real plumbing.
