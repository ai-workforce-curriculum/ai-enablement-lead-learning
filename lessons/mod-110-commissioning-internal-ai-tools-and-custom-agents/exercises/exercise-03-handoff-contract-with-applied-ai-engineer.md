# Exercise 03 — Handoff Contract with Applied AI Engineer

**Estimated effort:** 2 hours
**Format:** three-page handoff contract + acceptance-criteria table + running-cadence calendar, Markdown
**Grounding chapters:** [02 — The Commissioning Brief as the Load-Bearing Artifact](../02-the-commissioning-brief-as-the-load-bearing-artifact.md); [04 — Handing Architectural Depth to the Agentic Systems Architect](../04-handing-architectural-depth-to-the-agentic-systems-architect.md); [06 — Signing Surfaces, Maintenance Commitments, and the Hand-Off Calendar](../06-signing-surfaces-maintenance-and-handoff-calendar.md). Prior reading: [mod-102 Chapter 06](../../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md); [mod-109 Chapter 05](../../mod-109-ai-incident-response-and-enablement-side-rollback/05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md) for the handoff-contract shape.

## Objective

Author the three-page handoff contract between you and the `applied-ai-engineer` (or `agentic-ai-engineer`) who will build the commission from Exercise 01. The contract turns the signed brief into an operating agreement that runs from signature through acceptance. The acceptance-criteria table is the specific surface the acceptance hand-off (Chapter 06, Hand-Off 3) is walked line by line against; the running-cadence calendar is the schedule the brief lives on from signing through pilot-to-rollout.

The output is the contract itself, the acceptance-criteria table, and the running-cadence calendar through acceptance. The deliverable is what the two signatures (commissioner and `ai-engineering-manager`) are formally binding on — an unsigned contract is a conversation.

## Prerequisites

- Chapters 02, 04, and 06 read.
- Exercise 01 complete (signed brief in hand) or Exercise 02's rebuild-from-brief / productionise cover note ready (revised brief equivalent in hand).
- [mod-102 Chapter 06](../../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md) read as the mod-102-side framing of the commissioning interface.
- [mod-109 Chapter 05](../../mod-109-ai-incident-response-and-enablement-side-rollback/05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md) read as the handoff-contract-shape precedent in the preceding module.

## Problem statement

The brief is signed. The `ai-engineering-manager` has nominated an `applied-ai-engineer` (or `agentic-ai-engineer` for an agentic commission). Kickoff is tomorrow. The two of you need the operating agreement that will govern the build — who delivers what by when, who owns which decision surface, what counts as acceptance, how scope changes are processed, and how the eval harness / outcome metric split (Chapter 05) is honoured during the build phase. This exercise is that contract.

The contract is three pages: one page of positioning and decision-rights, one page of the acceptance-criteria table, one page of the running cadence and scope-change protocol. Each page is load-bearing; longer is not better.

## Requirements

### Part A — The three-page contract

**Page 1 — Positioning and decision-rights.**

- Open with a one-paragraph recap of the commission (problem, cohort, outcome criterion from the brief's Section 3, acceptance date from Section 6).
- Name the three decision surfaces and which role owns each:
  - **Architecture decisions** — model choice, retrieval pattern, deployment surface, prompt structure, agent-architecture choices. Owner: the engineer, with the `ai-engineering-manager` as the escalation surface. The commissioner is consulted but does not own.
  - **Scope decisions** — which problem, which cohort, which success criterion, which guardrails. Owner: the commissioner, with `head-of-ai-governance` as the governance-side co-signer. The engineer is consulted but does not own.
  - **Build-calendar decisions** — dates, contingency, scope-change timing. Owner: the `ai-engineering-manager`, with the commissioner as the dependency-surface co-signer (the pilot cohort is cohort-ready on specific dates; the exec sponsor's informational cadence depends on the build calendar).
- Close with the one-paragraph statement of what the signatures are binding on — the commissioner's signature binds to scope; the engineering manager's signature binds to build.

**Page 2 — The acceptance-criteria table.**

A table with four columns — **Artefact**, **Owner**, **What "complete" means**, **How it is verified at acceptance**. Rows cover every artefact the Chapter 02 Section 8 binding requires at acceptance:

- The working tool against the success criterion from Section 3.
- The eval harness and the baseline score.
- The runbook (operable by the support path from [mod-102 Chapter 03](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) artefact 5).
- The observability surface (logging, tracing, dashboarding; the maintenance owner can read it, the incident path can read it under [mod-109 Chapter 02](../../mod-109-ai-incident-response-and-enablement-side-rollback/02-the-kill-switch-as-an-operating-artifact.md)).
- The kill-switch runbook (co-authored with the commissioner; signed by `head-of-ai-governance`, IT identity, and the engineer).
- The data-handling-SOP-binding artefact (the specific policy references the tool respects at runtime).
- The maintenance-owner acceptance signature.

Each row's "how it is verified" entry is specific — the exact walk-through the hand-off meeting will perform. Vague verification ("reviewed for completeness") is the Chapter 01 apologist posture written into the acceptance surface; write the specific, verifiable walk.

**Page 3 — Running cadence and scope-change protocol.**

- **Running cadence.** The specific meetings between brief-signing and acceptance. At minimum: a weekly build-progress check (engineer and commissioner), a bi-weekly stakeholder update (commissioner, `ai-engineering-manager`, exec sponsor at informational altitude), the pilot charter review (Chapter 06 Hand-Off 2), the red-team-evidence review ahead of the pilot-to-rollout gate, and the acceptance meeting. Each entry names the agenda shape, the participants, and the artefact it operates on.
- **Scope-change protocol.** The specific sequence for processing a scope change: raised by whom, written against what, reviewed at what cadence, co-signed by whom, filed where. A scope change is a brief revision and a re-signature — not a conversation. Name the specific document path and the re-signature process.
- **The eval-harness-vs-outcome split during build.** Chapter 05's two-surface measurement discipline applies from day one. Name which eval-harness runs the commissioner reads at what cadence, which outcome measurements are being pre-staged for pilot, and what the data-plumbing dependencies between the engineering team and the `ai-augmented-analyst` ([mod-106 Chapter 06](../../mod-106-outcome-measurement-and-executive-reporting/06-coordinating-with-the-analyst-and-the-team-manager.md)) look like.

### Part B — The acceptance-criteria table (standalone)

Page 2 of the contract, extracted as its own file for the acceptance hand-off meeting. Include the same four columns and the same rows; include one extra column — **At-acceptance status** — that will be filled in live during the Chapter 06 Hand-Off 3 meeting. Leave the column empty in the exercise deliverable (the fill-in happens at the real hand-off), but ensure the table is structured to accept it.

### Part C — The running-cadence calendar

A one-page Markdown calendar with dates (relative to the brief-signing date; `T+0` for signing, `T+N weeks` or specific dates if your Section 6 timeline allowed it) and events. Each event names the meeting, the participants, the artefact under review, and the decision expected. The calendar runs from T+0 through acceptance plus the first graduate-or-retire review at T+4 quarters — sketched at outline depth after acceptance, specific pre-acceptance.

## Starter guidance

- The decision-rights section on Page 1 is the discipline that prevents the Chapter 01 designer posture. If you catch yourself writing "the commissioner approves the architecture," pull it out — the commissioner is consulted, not approving. Rewrite as "the engineer makes architecture decisions in consultation with the commissioner on behaviour impact."
- The acceptance-criteria table is where the brief's Section 8 and the engineer's runbook commitments meet. If the table leaves a Chapter 02 Section 8 slot uncovered, the brief's binding is incomplete at the acceptance surface. Reconcile against the brief before signing the contract.
- The scope-change protocol on Page 3 is often under-specified. A scope change raised in Slack and resolved in a hallway conversation is a scope change that leaks into the build without a brief revision. Name the specific path — probably `scope-change-request-NN.md` filed in the evidence store, with a named reviewer rotation.
- The eval-harness-vs-outcome split during build is the hardest part of the running cadence. The outcome metric is often not measurable until the tool is in pilot; the pre-pilot proxy is a workflow interview against the user cohort or a baseline measurement on the current (non-AI) workflow. Name the proxy explicitly.
- For an agentic-tool commission, add a row to the acceptance-criteria table for the step-boundary verification — the specific agent-behaviour tests that confirm the tool escalates to a human at the step boundaries named in the brief's Section 2.
- Where an organisational fact you need is unknown (specific meeting room, specific reviewer names, specific evidence-store paths), use `<!-- needs-research: ... -->` inline.

## Deliverables

- `handoff-contract.md` — the three-page contract.
- `acceptance-criteria-table.md` — the extracted table with the five columns (fifth column empty, structured to accept at-acceptance status).
- `running-cadence-calendar.md` — the one-page calendar through acceptance plus a sketch of the first graduate-or-retire review.
- A short cover note (3–5 sentences) summarising the most-contested decision-rights question you expect the engineer or engineering manager to push back on at contract signing, and the specific argument you will make to defend the commissioner-side ownership.

## Acceptance criteria

- The contract is three pages (approximately — tight prose, no filler). Each page's purpose is named at the top.
- Page 1 names the three decision surfaces (architecture, scope, build calendar) with explicit ownership and escalation; the commissioner's binding and the engineering manager's binding are each named in one paragraph.
- Page 2's table has four columns, covers every Chapter 02 Section 8 slot, and every row's "how it is verified" entry is specific rather than vague.
- Page 3 names the running cadence (meetings, agendas, artefacts, decisions), the scope-change protocol (raised-by, written-against, reviewed, co-signed, filed), and the eval-harness-vs-outcome split during build.
- The acceptance-criteria table is structured to accept the at-acceptance status column fill-in at the real hand-off.
- The running-cadence calendar covers T+0 through acceptance plus a sketch of the four-quarter graduate-or-retire review, with dates grounded against the brief's Section 6 timeline.
- `<!-- needs-research: ... -->` is used wherever an organisational fact is missing.
- The contract has no architecture decisions — no model names, no retrieval-pattern names.

## Stretch goals

- Add a **"what I do if the engineer pushes back on scope"** memo — one page — rehearsing the three most-likely scope-push-back patterns (feature expansion, cohort expansion, success-criterion softening) and the specific commissioner-side move for each. This is the Chapter 01 product-manager-posture prevention rehearsed in advance.
- Draft a **red-team-evidence coordination plan** as an appendix to Page 3 — the specific interface between the engineer (who provides evidence inputs) and the `ai-risk-engineer` (who runs the exercise), including the dated evidence-return gate from the brief's Section 4 Appendix A.
- Draft a **"what the contract does not resolve"** memo — one page — naming the questions you flagged for the contract-signing hand-off meeting rather than resolving in the draft. These are the contract-defining questions the two signatories will discuss before signing.

## Why this exercise matters

The brief is the commission's specification; the handoff contract is the commission's operating agreement. Without the contract, the brief has to re-interpret itself at every weekly meeting, scope decisions happen in Slack, acceptance becomes an exercise in "I think we're done" rather than a walk-through of a signed artefact, and the maintenance owner inherits a tool whose operating discipline was never written down. The contract is what turns a signed brief into a build you can defend to the governance council — and at acceptance, the acceptance-criteria table is the specific surface the commissioner, the engineer, and the maintenance owner all read together to confirm the commission has landed.
