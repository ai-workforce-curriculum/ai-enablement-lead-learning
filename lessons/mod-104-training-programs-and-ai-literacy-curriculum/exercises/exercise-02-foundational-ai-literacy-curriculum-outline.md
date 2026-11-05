# Exercise 02 — Foundational AI Literacy Curriculum Outline

**Estimated effort:** 3 hours
**Format:** a curriculum outline of 3–5 pages, Markdown or docx, plus a short assessment specification
**Grounding chapters:** [03 — The Foundational AI Literacy Curriculum](../03-the-foundational-ai-literacy-curriculum.md), [07 — Measuring Fluency Growth](../07-measuring-fluency-growth.md)

## Objective

Produce the **foundational curriculum outline** — the six-module artifact every in-scope operator will complete, authored to the organization you carried forward from Exercise 01. The outline is the artifact your L&D partner will turn into an LMS module set and the artifact an Article 4 auditor will read when asking *is this proportionate for your context*.

## Prerequisites

- Chapter 03 read; Chapter 07 skimmed.
- Fluency target map from Exercise 01 in hand (or a reasonable stand-in).
- Access to (or a reasonable facsimile of) your organization's acceptable-use policy and data-handling SOP. If you do not have these, use the templates from [mod-103](../../mod-103-policy-co-authoring-with-governance/README.md) Exercises 01–02 as stand-ins.

## Problem statement

Your L&D counterpart has asked for the "intake brief" on the foundational curriculum — enough detail that they can begin instructional design and LMS build-out. They want:

- The six-module breakdown with learning objectives, time budget, and format for each.
- The scenarios that will carry Modules 3 (acceptable-use) and 4 (data-handling).
- The assessment specification — what the knowledge check looks like and what the artifact grading criteria are.
- A clear changelog mechanism so the curriculum stays current.

## Requirements

Deliver one outline with these components.

### 1. Opening scope paragraph (3–5 sentences)

Who this curriculum is for (the operator tier plus any sub-tiers you called out in Exercise 01), who it is not for (leadership, specialists, builders — with pointers to their curricula), and the Article 4 posture it answers to.

### 2. Module-by-module outline

Six modules per Chapter 03. For each module, specify:

- **Title** — short and task-shaped.
- **Learning objectives** — 2–3 bullets per module. Objectives are observable ("the operator can identify three escalation signals relevant to their function"), not aspirational ("the operator understands AI").
- **Format** — live cohort, self-paced, scenario workshop, reference card. Justify the choice in one sentence.
- **Time budget** — minutes of operator time.
- **Content outline** — 3–6 bullets of what the module covers. Not the full slide deck — the skeleton.
- **Example or scenario** — one concrete example or scenario the module uses.

Modules 3 (acceptable-use in operator voice) and 4 (data-handling in scenarios) must each include at least **three named scenarios** specific to your organization — e.g., for a bank: "A branch employee uses a chatbot to summarize a customer complaint." The scenarios are the thing that makes the curriculum organization-specific rather than generic.

### 3. Assessment specification

Separately from the module outlines:

- **Knowledge check:** 10–15 item specification. Not the full items — a description of the item types, the policy sources items will be drawn from, the pass bar, retake rules, and item-pool rotation policy.
- **Artifact:** the end-of-curriculum open-book artifact (e.g., a one-paragraph operator-voice summary of the acceptable-use policy). Grading rubric sketched in 3–5 criteria.

### 4. Freshness and changelog mechanism

A short section specifying:

- Which modules refresh on which triggers (policy change, envelope change, incident).
- Where the changelog lives (document header, wiki page, LMS note).
- Who owns the refresh and the cadence for a "no-trigger" annual review.

### 5. The shadow AI call-out

One paragraph on how the curriculum names shadow AI explicitly in Module 2 and where the amnesty / intake path is. This is not optional — see Chapter 03.

## Starter guidance

- Modules 1 and 2 are allowed to be short. Do not over-engineer them. Module 1 is 20 minutes; if you've written an hour's worth of content, you are drifting into technical-literacy territory that does not belong here.
- Scenarios for Modules 3 and 4 should be *operator-voice* — a line manager could read them aloud in a team meeting and they would sound like real situations, not training vignettes. If a scenario starts "Imagine a user named John who...", rewrite it.
- The assessment specification is the thing an auditor checks for proportionality. A 10-item quiz drawn from your actual policy is defensible; a 10-item quiz on generic AI trivia is not.
- Reference [mod-103](../../mod-103-policy-co-authoring-with-governance/README.md) for the acceptable-use policy and data-handling SOP shape your scenarios should draw from. If those artifacts do not exist yet in your organization, note it as a prerequisite that must be resolved before this curriculum can go live.
- Do not write the full slide decks. Your artifact is a curriculum outline — the skeleton L&D turns into courseware. If you are drafting slides, you are over-building the exercise.

## Deliverables

- `foundational-curriculum-outline.md` (or `.docx`): the outline described above.
- A short *instructional-design intake note* (3–5 sentences) you would hand to your L&D partner summarizing what you need from them to turn this into LMS-live content.

## Acceptance criteria

- The outline covers all six modules with all five required elements per module.
- Modules 3 and 4 each include at least three named, organization-specific scenarios.
- The assessment specification is grounded in the organization's actual policy artifacts (or clearly flagged stand-ins).
- Freshness mechanism is explicit — a reader can tell when and why modules refresh.
- The shadow AI amnesty / intake path is named explicitly.
- Total length 3–5 pages. If it is longer, you have drifted into slide-authoring; cut to the skeleton.

## Stretch goals

- Author one of the Module 4 scenarios in full — the scenario text, the correct operator action, the common failure mode, and a scoring criterion. This is the kind of artifact you would test on your champion network before taking the curriculum live.
- Design a 5-item knowledge-check pool derived from your organization's acceptable-use policy. Check the items against the policy text to confirm each item has a defensible, text-supported answer.
- Draft the "line-manager one-pager" — a single-page summary your team managers (`ai-augmented-team-manager`) would use to introduce the curriculum to their teams. This is the kind of deferral artifact from [Chapter 08](../08-partnering-with-hr-ld-and-internal-comms.md).

## Why this exercise matters

The foundational curriculum is the single artifact most likely to be audited and the one most likely to go stale within 12 months if it isn't designed with refresh in mind. Producing the outline once, correctly, and with the freshness mechanism baked in, saves the next 12 months of firefighting as policy and tools change underneath.
