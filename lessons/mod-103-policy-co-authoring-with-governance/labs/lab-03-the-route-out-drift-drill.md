# Lab 03 — The Route-Out Drift Drill

**Duration:** 60–75 minutes
**Format:** guided solo drill — classify a corpus of enablement-side sentences and actions against the three drifts, rewrite the drifted ones to stay on the enablement side, and build the handoff-mechanics artifact Chapter 07 names
**Grounding chapters:** [07 — What You Route Out — Counsel, SOC, Architect](../07-what-you-route-out-counsel-soc-architect.md), [01 — The Co-Author Posture and the Redline Log](../01-the-co-author-posture-and-the-redline-log.md), [04 — The One-Page Acceptable-Use Policy](../04-the-one-page-acceptable-use-policy.md), [05 — The Data-Handling SOP](../05-the-data-handling-sop.md), [06 — The Intake Questionnaire](../06-the-intake-questionnaire.md)

## Objective

Work a corpus of **twelve enablement-side sentences and actions** against the three Chapter 07 drifts — legal opinion, SOC-side incident handling, control-library architecture — and (a) classify each as *stay* or *drift*, (b) for every drift, rewrite the sentence or action into the enablement-side move that keeps the owner on the right side of the line, (c) build the **handoff-mechanics artifact** Chapter 07 names (named owner, named trigger, thing you keep) for each of the three drifts in your own organization.

This lab is not any of the five exercises. The exercises produce the three policy artifacts, the council pre-read, and the standards-mapping memo; this lab sits on top of all of them and drills the discipline that keeps the whole module's output from collapsing into one person's job. Chapter 07 calls the drifts "quiet role collapse"; the drill is the cheap practice that keeps the collapse from happening under the pressure of the first incident, the first contested legal clause, the first intake pattern that cries out for a redesigned field.

## Prerequisites

- Chapter 07 read end to end.
- Chapters 01, 04, 05, 06 read — each drift maps to artifacts from these chapters.
- A chosen organization (carry forward from Exercises 01–04 if you have one; otherwise pick one of the three archetypes from Exercise 01).
- A single markdown file.
- Optional: the AUP, SOP, intake submission, council pre-read, or standards-mapping memo artifacts from the exercises, if you have them. The drill works without them, but having them lets you point real sentences at the corpus.

## Why a lab, not an exercise

Exercises produce *artifacts*. This lab produces *reflexes*. Chapter 07 is explicit that the three drifts "feel like upgrade and read like competence" — which is to say, when you make one, you will not notice at the moment. The reflex you need is the one that catches the drift sentence *before* it lands in the signed policy, the triage Slack, or the memo to the architect. You cannot build that reflex by writing more artifacts; you build it by practicing the classification until it is automatic.

A solo drill, worked against a deliberately mixed corpus, is the cheapest way to build that reflex.

## Setup

Create `route-out-drift-drill.md` with this skeleton:

```markdown
# Route-Out Drift Drill — <organization>

**Date:** <today>
**Drilled by:** AI Enablement Lead (me)

## Part 1 — Classify the corpus (25 min)

<entries>

## Part 2 — Rewrite the drifts (20 min)

<entries>

## Part 3 — Build the three handoff-mechanics artifacts (20 min)

<entries>

## Debrief — what the drill taught me (10 min)

<entries>
```

Set a timer per part — the time pressure is part of the drill.

---

## Part 1 — Classify the twelve items (25 min on the timer)

Copy this corpus into your file as a table. Work it top to bottom — for each item, write a one-letter classification (`S` = stay on the enablement side; `L` = drift to legal/counsel; `C` = drift to SOC/security operations; `A` = drift to architect/control library) and a one-sentence rationale. Do not look ahead; work in order.

```markdown
## Part 1 — Classify the corpus

Classification legend:
- **S** — stays on the enablement side (the sentence or action is appropriate for the enablement seat)
- **L** — drift to legal/counsel (writes a legal opinion where only a legal hook belongs)
- **C** — drift to SOC-side incident handling (runs forensic workstream, decides notification clock, speaks to regulators)
- **A** — drift to control-library architecture (redesigns schema, taxonomy, or control mapping)

| # | Candidate sentence or action | Classification | One-sentence rationale |
|---|------------------------------|----------------|------------------------|
| 1 | AUP draft contains the sentence: *"Pasting customer PII into prompts would violate GDPR Article 5."* |  |  |
| 2 | AUP draft contains the sentence: *"Users must not paste customer PII into prompts."* |  |  |
| 3 | SOP accident-path step 5 reads: *"The first-line triager packages the operator-side evidence (prompt text, output, timestamp, user context) and hands off to the SOC within the defined SLA."* |  |  |
| 4 | Triage Slack message during a live incident: *"I've reviewed the vendor's retention logs and I don't think the notification clock has started yet — let's hold off on telling counsel for 24 hours."* |  |  |
| 5 | Quarterly memo to `senior-ai-governance-architect`: *"Over the last cycle, five of twelve submissions in regulated-domain tasks could not be classified without asking the requester for clarification on human-review gating."* |  |  |
| 6 | Quarterly memo to `senior-ai-governance-architect`: *"Here is the redesigned field — the human-review-gating slot should become a required sub-field with four enumerated values, mapping to the existing control-library entries C-012 and C-015."* |  |  |
| 7 | Council pre-read Section 1 contains: *"INT-2026-087 — status: `awaiting-council-decision`. Ask: decision."* |  |  |
| 8 | Council pre-read Section 2 contains: *"Recommend the council move <tool> from Tier 2 to Tier 3 given the field-level usage expansion."* |  |  |
| 9 | AUP draft contains: *"This tool processes data in the US East region."* |  |  |
| 10 | Data-handling SOP retention section contains: *"The vendor's retention of abuse-monitoring logs is incompatible with our EU data-subject-rights obligations and must be renegotiated in the next DPA cycle."* |  |  |
| 11 | Enablement lead to the security partner during the walking redline: *"Can you confirm whether DLP has actually been configured to flag the PII class for this tool before we ship the SOP sentence that says DLP will flag it?"* |  |  |
| 12 | Enablement lead at council: *"I'd like to propose a new GOVERN sub-category covering champion-network field signal, since the current sub-categories don't have a clean home for it."* |  |  |
```

**Expected classification distribution (self-check — do not look until you have finished):** roughly three or four `S`, three drifts to `L`, two drifts to `C`, three or four drifts to `A`. If your distribution is wildly off that shape, re-read Chapter 07 and re-work the items where you diverged.

**Checkpoint 1:**

- [ ] All twelve items have a classification letter and a one-sentence rationale.
- [ ] You did not look at the rewrite section before finishing classification.
- [ ] Your rationale for each drift names *which* chapter line the sentence violates — Chapter 07's hook-vs-opinion distinction, the enablement-vs-SOC boundary, or the architect-redesign rule.

---

## Part 2 — Rewrite each drifted item (20 min on the timer)

For every item you classified as a drift (`L`, `C`, or `A`), write the enablement-side rewrite — the sentence or action that keeps the owner on the right side of the line while preserving the operational knowledge that made the original sentence tempting.

Use this template per rewrite:

```markdown
### Rewrite — Item <N>

**Original (drift type <L/C/A>):**
> <quote the original>

**Rewrite (enablement-side):**
> <the rewritten sentence or action>

**What the rewrite keeps (per Chapter 07's "what you keep" framing):**
- <the observation, the convening role, the operational knowledge that survives>

**What the rewrite routes out:**
- <the opinion, the forensic finding, the proposed redesign — with the named owner the artifact now points at>
```

Guidance per drift type:

- **`L` rewrites (legal opinion → legal hook).** Cut the opinion ("this would violate X," "this is acceptable under Y," "this exceeds Z"). Leave the hook — the named data class, named jurisdiction, named counterparty relationship. Add a line routing the opinion out: *"Counsel: please attach obligation language to this hook."* Chapter 07's test: does the sentence describe a fact the operator should know (hook), or does it assert what the law or contract says (opinion)?
- **`C` rewrites (SOC-side incident handling → convene/triage/handoff).** Cut the forensic verb (reviewed logs, analyzed retention, decided notification timing). Leave the triage move — the accident-shape recognition, the preserved-evidence packaging, the handoff to SOC and `ai-risk-engineer`. If the sentence tried to decide a notification clock, route the clock decision to `head-of-ai-governance` and counsel explicitly.
- **`A` rewrites (control-library redesign → field evidence).** Cut the proposed field, the proposed enumeration, the proposed control mapping. Leave the specific submissions and the shape of refinement framed as architect-decides. Chapter 06: "Propose adding a sub-field for human-review gating, because over the last cycle, five of twelve submissions in regulated-domain tasks could not be classified without asking the requester for clarification." Not: "Here is the redesigned field."

Work at least six rewrites in the twenty minutes — one per drifted item. If you have fewer than six drifts, re-check your Part 1 classifications; the corpus is intentionally weighted toward drifts because drift-recognition is the drill's point.

**Checkpoint 2:**

- [ ] Every drifted item from Part 1 has a rewrite.
- [ ] Each rewrite has a "what the rewrite keeps" line and a "what the rewrite routes out" line — Chapter 07's thing-you-keep / named-owner shape.
- [ ] No rewrite reintroduces the drift under a softer verb ("I think X" is still an opinion; "maybe the redesign should be Y" is still a redesign proposal). Strike and rewrite.

---

## Part 3 — Build the three handoff-mechanics artifacts (20 min on the timer)

Chapter 07 names three sets of handoff mechanics — one per drift — and the discipline that stops each. Build the three artifacts for your organization, each as a short named block in your file.

### Artifact A — The legal review slot and question queue

```markdown
### Handoff mechanics — Drift 1 (legal opinion stays with counsel)

**Named owner:** counsel — <specific practice, e.g., "data-protection practice" or named firm/internal counsel role>
**Named trigger:** <when the slot runs — "weekly 30-min walking-redline slot" during drafting windows; otherwise on open-question>
**Named channel:** <where open questions queue — e.g., "intake-tagged legal-question channel in the shared tracker">
**Thing you keep:** the ability to ask hard legal questions and the operational knowledge that lets you draft sentences counsel can productively respond to.

**Open-question template (used between slots):**
> "Counsel: in the context of <artifact + section>, the draft currently states <hook, verbatim>. The specific legal question for your reading: <one specific question, e.g., 'is the vendor's abuse-monitoring retention compatible with our data-subject-rights obligations for EU employees?'>. Target: <date> walking-redline slot."

**Co-author tag entry:** counsel is named in the co-author tag on every section where a legal reading has been attached.
```

### Artifact B — The enablement-side evidence pack SLA

```markdown
### Handoff mechanics — Drift 2 (SOC-side incident handling stays with security operations)

**Named owner:** SOC — <specific role, e.g., "named SOC on-call contact"> and `ai-risk-engineer` (L25)
**Named trigger:** <"SOP accident-path step 5 fires" OR "notification obligation becomes a live question" — whichever comes first>
**Named channel:** <"SOC Slack group" / "SOC ticket queue" — with the AUP's escalation-path section pointing at the same channel>
**Thing you keep:** the convening role, the operational knowledge that lets you brief the SOC quickly and accurately, the first-ten-minutes accident-path script with the user.

**Evidence-pack SLA (what you hand off, by when):**
> Within <N> minutes of handoff trigger, the SOC receives:
> - the exact prompt text that triggered the accident path (verbatim)
> - the output (verbatim)
> - the timestamp (ISO-8601, with timezone)
> - the user's role, geography, and client context
> - the accident shape classification (paste-mistake / subtly-wrong-output / tool-malfunction)
> - the pause-rollout decision state (pulled / held / not-applicable)
> - the champion-network communication state (sent / queued / not-applicable)
> No drip-fed questions. The pack is complete at handoff or the handoff is early.
```

### Artifact C — The quarterly architect evidence memo

```markdown
### Handoff mechanics — Drift 3 (control-library architecture stays with `senior-ai-governance-architect`)

**Named owner:** `senior-ai-governance-architect` (L50), with `head-of-ai-governance` (L60) on cc
**Named trigger:** quarterly cycle close (or per-cycle if the organization runs a faster cadence)
**Named channel:** memo filed at `<repo-path>/governance/architect-memos/<yyyy-qN>.md`; standing 30-minute monthly bilateral on the calendar
**Thing you keep:** the operational knowledge that makes you the person surfacing the sharpest evidence; the ability to say the current design is not working.

**Memo shape (every quarter):**
> - **Field evidence:** specific submissions (by ID, not anonymized) where the current taxonomy produced a wrong, unstable, or missing classification.
> - **Control evidence:** specific controls in the library that are never evidenced in practice, with the period of observation.
> - **Policy-category evidence:** policy categories that see no use, or see use for something other than their intent, with the specific submissions.
> - **Shape of refinement (not redesign):** framed as the architect's decision — "propose adding …," "propose revisiting the mapping between…," never "here is the new field."
> - **Costs and benefits:** which training materials, policy clauses, existing classifications would need to flow through if the architect chose to act.
> - **The explicit frame:** "evidence for the architect's consideration," not "a redesign to approve."

**Disciplined refusal:** "no redesign proposals from this seat" — held under pressure from council "just fix it" asks.
```

**Checkpoint 3:**

- [ ] All three handoff-mechanics artifacts present.
- [ ] Each artifact names an owner, a trigger, a channel, and a thing-you-keep.
- [ ] The evidence-pack SLA in Artifact B names specific evidence types (prompt / output / timestamp / user context / accident shape / pause-rollout state / champion-comm state) and a specific SLA number.
- [ ] The architect memo in Artifact C frames every recommendation as architect-decides and does not include a proposed field, proposed enumeration, or proposed control mapping.

---

## Part 4 — 10-minute debrief (after the timer)

Write the debrief answering these four prompts. One or two sentences each.

```markdown
## Debrief — what the drill taught me

1. **Which of the twelve corpus items did I classify as `S` but am now less sure about on second reading — and which Chapter 07 line resolves the doubt?**
   <answer>
2. **Of the three drifts, which one is my seat most at risk of making in the next 90 days — and which chapter cue will catch it?**
   <answer>
3. **Which rewrite felt most like "making the sentence weaker" — and why is the weaker sentence actually the correct one per Chapter 07's "observations not opinions" rule?**
   <answer>
4. **In production, which of the three handoff mechanics will break first if I don't hold the discipline — and what is the one Monday-morning move that would preempt the break?**
   <answer>
```

**Checkpoint 4:**

- [ ] All four prompts answered.
- [ ] Prompt 2 names a specific drift and a specific chapter cue, not a generic answer.
- [ ] Prompt 4 names a specific Monday-morning move, not an aspiration.

---

## Deliverable

- `route-out-drift-drill.md` — the twelve-item classification table (all rows filled), the drifted-item rewrites (at least six), the three handoff-mechanics artifacts, and the four-prompt debrief.

## Expected output shape

Roughly 2.5–3.5 pages of markdown. Twelve classified items; six or more rewrites with "keeps" and "routes out" lines; three handoff-mechanics artifacts, each with owner / trigger / channel / thing-you-keep and the artifact-specific template (open-question template, evidence-pack SLA, quarterly memo shape); four debrief answers.

## Checkpoint — self-evaluation

- [ ] Every corpus item has a classification letter (`S` / `L` / `C` / `A`) and a one-sentence rationale that names which Chapter 07 line it violates (or confirms).
- [ ] Every drift has a rewrite that keeps the operational knowledge and routes the opinion/finding/redesign to the named owner.
- [ ] No rewrite reintroduces the drift under softer language — "I think" is still an opinion; "maybe the redesign is" is still a redesign.
- [ ] Artifact B's evidence-pack SLA names a specific number of minutes, not "promptly."
- [ ] Artifact C's memo shape does not include a proposed field definition, a proposed value enumeration, or a proposed control mapping.
- [ ] The debrief names a specific drift the seat is at risk of making and a specific chapter cue that catches it.

## Common failure modes

- **Over-weighting the `S` classification.** The corpus is deliberately weighted toward drifts. If you classified eight or more items as `S`, you are reading the drifts past the chapter's line. Re-work from Chapter 07's *Why the drifts happen* section.
- **Rewriting a `L` drift as a quieter opinion.** "This *may* violate GDPR" is still an opinion. The rewrite is to cut the opinion verb entirely and leave the hook; counsel attaches the opinion.
- **Rewriting a `C` drift by moving it to a different enablement-side role.** "The CoE lead will decide the notification clock" is still SOC-side incident handling, just reassigned. The rewrite routes the clock decision to `head-of-ai-governance` and counsel explicitly, not to another enablement-side seat.
- **Rewriting an `A` drift by hedging the proposal.** "I'm not sure, but maybe the field should become…" is still a field proposal. The rewrite cuts the field proposal entirely and leaves the submissions + the shape of refinement, framed as architect-decides.
- **The evidence-pack SLA in Artifact B is unbounded.** "Prompt" and "quickly" are not SLAs. Pick a specific number (common choices: 15, 30, or 60 minutes, depending on organizational maturity) and own it. Chapter 07 is explicit that the handoff is "within a defined SLA, not drip-fed as questions arise."
- **The quarterly architect memo includes a field redesign anyway.** Chapter 07 names this as "the most insidious drift because it feels like upgrade." If the memo shape in Artifact C contains a proposed field, strike it; the architect proposes fields.

## What this lab prepares you for

The three drifts are the discipline that makes the whole module scale. The two policy artifacts (AUP, SOP), the intake questionnaire, the council pre-read, and the standards-mapping memo all look clean in isolation, and all collapse into one person's job if the drifts are not caught at the sentence level. Drilling the classifications until the recognition is automatic — and having the handoff-mechanics artifacts (slot, evidence pack, quarterly memo) built and filed in advance — is what makes the first incident, the first contested legal clause, and the first intake pattern that cries out for a redesign survivable. In production, you will touch all three drifts in a mature CoE every quarter; the lab is the cheap practice before the quarter where it matters.
