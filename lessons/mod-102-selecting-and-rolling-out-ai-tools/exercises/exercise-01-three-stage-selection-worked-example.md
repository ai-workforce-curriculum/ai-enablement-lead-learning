# Exercise 01 — Three-Stage Selection Worked Example

**Estimated effort:** 3 hours
**Format:** three one-page artifacts, Markdown
**Grounding chapters:** [01 — The Three-Stage Tool Selection Decision](../01-the-three-stage-selection-decision.md)

## Objective

Walk one concrete organization-scope tool-selection decision through all three stages and produce the one-page artifact each gate expects. The output is the artifact *set* you would carry into a Stage 3 review — three short pages, each one signable — not an essay about how three-stage selection works. The point is to feel where the stages catch you and where they don't.

## Prerequisites

- Chapter 01 read, including the five-field problem statement, the Stage 2 build-vs-buy rule, and the Stage 3 pilot-vs-rollout criteria.
- Chapter 03 skimmed far enough to know the names of the seven rollout artifacts — you will reference at least one by name in your Stage 3 output.
- A chosen organization and decision. Pick one of:
  - a summarization + draft assistant for a 1,200-person professional-services firm
  - a meeting-notes tool for a 6,000-person pharma
  - a coding assistant for a 400-engineer platform team at a 9,000-person retailer
  - a learner-chosen alternative of comparable org-wide scope (not a single-team experiment)

You will reuse this organization and tool choice in Exercises 02-05. Pick something you can live with for the whole module.

## Problem statement

The executive sponsor for your chosen organization has asked you — the AI Enablement Lead — to run the formal selection process on this tool decision. They do not care about your framework. They care that at the Stage 3 review they can read three signed one-pagers in ten minutes and know whether to approve a pilot, approve rollout, or send you back to Stage 2. You have the week to produce the set.

## Requirements

Produce three separate one-page artifacts, one per stage. Each must fit on one page at normal body-text size.

1. **Stage 1 — Problem statement one-pager.** All five fields from Chapter 01 (problem statement in user voice, target task, current baseline, pain measurement, user cohort). Plus one closing line answering the question Stage 1 exists to answer: *is this problem named well enough to evaluate candidates against it?*
2. **Stage 2 — Candidate evaluation one-pager.** Problem restatement in one sentence. An explicit build-vs-buy line — even if "build" is dismissed in one sentence, it must appear. A table or list of at least **three candidates** against the problem, including at least one explicit **"no"** (knocked out) and at least one **"defer"** (promising but out-of-envelope or needs more evidence). POC scope + timebox + exit criterion if a POC was run or is proposed. Envelope status per candidate. One recommended candidate. Plus the closing line: *is this candidate ready to commit to Stage 3?*
3. **Stage 3 — Pilot-vs-rollout commit one-pager.** Problem, candidate, envelope status (one line each). An explicit **pilot or rollout** decision with reasoning against the four Chapter 01 criteria (risk surface, prior evidence, envelope status, cohort size). Named kill-switch owner. **At least one artifact from the Chapter 03 rollout artifact set, named, that must exist before the chosen path starts.** Plus the closing line: *commit to pilot, commit to rollout, or return to Stage 2 — and why.*

## Starter guidance

- The hardest part of Stage 1 is the pain measurement. If you cannot name a number — even a rough one — your Stage 1 artifact fails on the "pain measurement" field. The honest move is to write the number you would instrument for in week one and mark it as a target, not an observation. Do not invent a measured number you did not measure.
- Stage 2 is where learners most often cheat by only listing candidates they want to win. Put a candidate on the list you expect to knock out, and knock it out in writing. The "no" line is the one that proves the evaluation happened.
- The "defer" line is the one most learners forget exists. A candidate can be the technically strongest option *and* not be Stage-3-ready because the envelope work has not happened. That is a defer, not a no. Chapter 01's warning — "running a pilot on an out-of-envelope tool and pretending the paperwork will catch up" — is what the defer line prevents.
- Build-vs-buy must appear even when the answer is trivially "buy." Writing *"No, buy — commodity capability already in the envelope from two vendors"* is a one-line answer and it is a valid Stage 2 output. Omitting the line is not.
- At Stage 3, if your reasoning against the four criteria has more than one "miss," the honest output is **pilot**, not rollout. Chapter 01 is explicit: miss one, pilot first. Do not talk yourself into the rollout.
- The Chapter 03 artifact you name at Stage 3 should be the one most likely to *not exist* on launch day for your specific organization. For a pharma, that is often the data-handling SOP. For a 400-engineer platform team, it is often the champion list. Pick the one that is actually your constraint.
- Do not invent vendor names, feature lists, incident histories, or peer-organization results. If your Stage 2 evaluation leans on a claim you cannot verify, mark it with `<!-- needs-research: ... -->` and move on. The exercise is the *shape* of the decision, not the fact base.

## Deliverables

- `stage-1-problem-statement.md`: one page, five fields, closing line.
- `stage-2-candidate-evaluation.md`: one page, three+ candidates, build-vs-buy line, one recommended candidate, closing line.
- `stage-3-pilot-vs-rollout.md`: one page, decision, reasoning against the four criteria, named kill-switch owner, named Chapter 03 artifact, closing line.

All three should share a header line naming the organization and the tool decision so a reader at Stage 3 review can orient in five seconds.

## Acceptance criteria

- Each artifact is one page at normal body-text size. If Stage 2 spills to two pages, you are writing an RFP response, not a gate artifact — cut.
- Stage 1 contains all five Chapter 01 fields. A missing field fails the gate; the exercise's gate is the same.
- Stage 2 contains an explicit build-vs-buy line, at least three candidates, at least one "no," and at least one "defer." Each candidate has an envelope-status line.
- Stage 3 names a specific Chapter 03 rollout artifact by name (e.g., "data-handling SOP," "kill-switch & rollback plan") that must exist before the chosen path can start.
- The organization-specific detail is visible across all three artifacts. A reader who knows your chosen organization should recognize it is written *for them*, not from a template.
- Every factual claim about a vendor, a regulator, a peer organization, or an incident is either something you can cite or is marked with `<!-- needs-research: ... -->`.

## Stretch goals

- Write the three-sentence **gate meeting agenda** for each stage: attendees, the one question the gate answers, the go/no-go outcome. Chapter 01 names the attendees for each gate; make them concrete for your organization (e.g., the actual `head-of-ai-governance` L60 delegate's team, not the abstract role).
- Pick the candidate you marked "defer" and sketch — three bullets — what envelope-admission work would move it from defer to ready for Stage 3. You will build on this in Exercise 02.
- Write the **one paragraph you would say out loud** at the Stage 3 gate if the executive sponsor pushes for rollout and your artifact says pilot. Three to five sentences. This is the muscle the role lives on.

## Why this exercise matters

Three-stage selection is the most-cited theme in the AI Enablement Lead posting sample, and the most common place the role is run over by a vendor AE, a procurement loop, or a BU head who skipped straight to rollout. Producing the three artifacts once, under no pressure, is how you build the reflex to ask for them when a decision is being made at speed. The artifact set you produce here is the shape of what you will carry into a real Stage 3 review — and the carry-forward into Exercises 02-05 means the pilot, the artifact set, and the measurement plan you build next all rest on this foundation.
