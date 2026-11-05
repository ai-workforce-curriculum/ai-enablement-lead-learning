# Exercise 04 — EU AI Act Article 4 Literacy Floor Drill

**Estimated effort:** 2 hours
**Format:** audit-ready literacy-program outline + evidence catalog
**Grounding chapters:** [05 — EU AI Act Article 4 and the Literacy Floor](../05-eu-ai-act-article-4-and-the-literacy-floor.md)

## Objective

Produce the two artifacts that would survive an EU member-state market-surveillance authority showing up tomorrow and asking, "demonstrate that your deployer-side AI literacy obligations under Article 4 are met":

1. A **literacy-program outline** that is audience-segmented, proportionate, current, and auditable.
2. An **evidence catalog** naming every piece of evidence that backs the claim — what it is, where it lives, who maintains it, how fresh it is.

The drill is a self-audit. The goal is to find gaps *before* a regulator does.

## Prerequisites

- Chapter 05 read.
- Access to the [EU AI Act text](https://eur-lex.europa.eu/eli/reg/2024/1689/oj) (the official consolidated version — do not rely on a summary for the specific wording of Article 4).
- Your chosen organization. For this exercise, the organization **must** have some EU-touching activity: EU employees, EU contractors, EU customers, or EU data subjects. If your Exercises 01–03 organization has none, pick a variant.

## Problem statement

Your head of AI governance has asked for the literacy slice of a larger AI Act readiness drill. Legal counsel will read whatever you produce. You have two days. Produce the two artifacts above at the level where legal can either sign them or redline them — no further.

## Requirements

### Part A — Literacy-program outline

A short document (one to two pages) covering:

1. **Scope** — who is in scope? Employees, contractors, third-party operators, and the specific definition under Article 4 you're applying ("staff and other persons dealing with the operation and use of AI systems on their behalf"). Name the specific populations and headcount estimates.
2. **Audience tiers** — at least three (leadership, operator, specialist is a reasonable starting shape; your organization may need more). For each tier: who's in it, what the content covers, how long it takes, and *why the content is sufficient for the context* under Article 4's "sufficient level … taking into account … technical knowledge, experience, education and training and the context."
3. **Delivery mechanisms** — instructor-led, e-learning, assessment, performance-support, refresh cadence. State the refresh cadence explicitly and explain why.
4. **Updates when the toolset changes** — the written rule for how the program updates when the approved-tool envelope, risk posture, or policy changes.
5. **Non-completers** — the policy for someone in scope who does not complete their required tier within the window. This is the question regulators ask next.

### Part B — Evidence catalog

A table (or bulleted list) of every piece of evidence that backs the claims above. For each row:

- Evidence name (e.g., "Level 1 literacy curriculum, v2026.2").
- What it is (one line).
- Where it lives (system name, link, path).
- Who maintains it (role).
- How fresh it is (date of last review).
- Who can retrieve it without your help (role — critical: evidence an auditor can only get through you is not evidence yet).

At minimum, the catalog covers:

- The content library (modules, assessments, playbooks).
- The completion records (roster, dates, pass/fail).
- The non-completer handling records.
- The refresh/update records (change log for the content and for the policy that governs it).
- The scope-definition record (who's in scope and the dated decision that put them there).

## Starter guidance

- Read the Article 4 text once in the official source before you write. The exact wording of "sufficient level … to their best extent … taking into account …" matters; paraphrases drift.
- Do **not** write marketing copy. An auditor is reading for *claim → evidence → retrievability*. If a line of the program outline has no matching evidence row, the line is a liability.
- Proportionality is your friend if applied honestly and your enemy if inflated. A 50-person law firm does not need the same program as a 50,000-person bank; a 50,000-person bank does not get to point at the 50-person firm's program.
- For the specialist tier, do not duplicate work done by the AI Governance or AI Engineering curricula. Reference the specialist's own role-specific training (red-team, model-eval, agent-building) and name the handoff.
- The "non-completers" section is the one most programs skip and the one most auditors ask about. Have an answer that is neither punitive theater nor empty.

## Deliverables

- `article-4-literacy-program.md` — the program outline (Part A).
- `article-4-evidence-catalog.md` — the evidence catalog (Part B).
- A short cover note (3-5 sentences) summarizing the two biggest gaps you found while building the drill and what you would do in the next 30 days to close them.

## Acceptance criteria

- The scope definition names specific populations and headcount, not abstract categories.
- Each audience tier has a *written rationale* for proportionality, not a tier label with implied justification.
- Every claim in the program outline maps to at least one evidence row in the catalog.
- At least one evidence row names a retriever who is *not you*.
- The non-completer policy is specific and defensible.
- The cover-note gaps are honest — if the drill is perfect, you have not done it as a drill.

## Stretch goals

- Add a one-paragraph note on how the program extends to **contractors and third-party operators** who use AI on the organization's behalf. This is where most organizations have their biggest Article 4 exposure and least evidence.
- Add the **content-update trigger matrix** — a short table of "when `<thing>` changes, `<content>` is reviewed within `<window>`." Common triggers: approved-tool envelope change, policy revision, EU AI Office guidance release, incident retrospective finding, member-state enforcement action.
- Draft the **talking points** the head of governance would use with legal counsel in a 30-minute review. Not a formal brief — the three things you want legal to decide in that meeting.

## Why this exercise matters

Article 4 is the first deployer-side AI literacy obligation with teeth in a major jurisdiction. Most organizations' current "AI training" is marketing, not evidence. Running the self-audit as a drill — *before* a regulator does it to you — surfaces the gaps while they are still cheap to close. It also doubles as the backbone of [mod-104](../../mod-104-training-programs-and-ai-literacy-curriculum/README.md)'s full curriculum build.
