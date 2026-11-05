# mod-103 — Policy Co-Authoring with Governance, Legal, Security, and Privacy

**Estimated effort:** 14 hours
**Role level:** 45 · **Family:** AI Workforce

This is the module where the role's writing meets its co-authors. Before you build the training curriculum (mod-104), run the champion network (mod-105), or stand up the exec scorecard (mod-106), you have to be able to co-author the three policy artifacts the enablement side authors first then redlines with governance — the acceptable-use policy, the data-handling SOP, and the intake questionnaire — and the redline log that proves the two sides negotiated. You also have to be able to attend the AI governance council as the enablement-side liaison without drifting into the chair's job, and to speak NIST AI RMF GOVERN and ISO/IEC 42001 clauses well enough to make the co-authoring conversation run at the right altitude. Those are the moves — and the three handoffs that stop you from accidentally owning counsel's, the SOC's, and the architect's work — are the whole module.

## Learning objectives

- Co-author the acceptable-use, data-handling, and intake policies for AI tools with legal, risk, compliance, and information security — producing documents that read as agreement between sides, not hand-off from one.
- Attend the AI governance council as the enablement-side liaison — feed intake workflows, provide risk-classification input, surface field signal from champions back into policy — co-owned with `head-of-ai-governance`.
- Read NIST AI RMF 1.0 GOVERN function and ISO/IEC 42001 clauses an enablement lead needs to speak fluently with governance partners — while leaving the architecture of the control library to `senior-ai-governance-architect` (L50) and program leadership to `head-of-ai-governance` (L60).
- Draft the three policy artifacts the enablement side authors first then redlines with governance — one-page acceptable-use policy, data-handling SOP, intake questionnaire — and the redline log that proves the two sides negotiated.
- Route legal opinion out to counsel; route SOC-side incident handling out to security operations; route control-library architecture out to `senior-ai-governance-architect` (L50).

## Lecture chapters

1. [The Co-Author Posture and the Redline Log](01-the-co-author-posture-and-the-redline-log.md) — the three failure postures (hand-off, abdication, no-artifact), the four partners, and the redline log as the artifact that proves co-authoring happened.
2. [The AI Governance Council Liaison Seat](02-the-governance-council-liaison-seat.md) — the three jobs at council (feed intake, risk-classification input, field signal), the pre-read and report-back discipline, and the co-ownership shape with `head-of-ai-governance`.
3. [NIST AI RMF GOVERN and ISO/IEC 42001 for the Enablement Seat](03-nist-ai-rmf-govern-and-iso-iec-42001-for-the-enablement-seat.md) — what to read, at what depth, and where the architect's work begins.
4. [The One-Page Acceptable-Use Policy](04-the-one-page-acceptable-use-policy.md) — the seven sections, the co-author tags, the if-in-doubt default, and the hard constraint of one page.
5. [The Data-Handling SOP](05-the-data-handling-sop.md) — the five sections, the ten-minute accident path, and the security + privacy launch gate.
6. [The Intake Questionnaire](06-the-intake-questionnaire.md) — the schema-vs-runner split, the pre-review session discipline, and the co-authoring beat on schema refinements.
7. [What You Route Out — Counsel, SOC, Architect](07-what-you-route-out-counsel-soc-architect.md) — the three drifts (legal opinion, SOC-side incident handling, control-library architecture) and the mechanics that stop each one.

## Exercises

Exercises 01–03 share a chosen tool and organization — carrying the same pairing across the three produces a coherent artifact bundle (AUP + SOP + intake submission) worth keeping. Exercise 04 uses the same organization for council context. Exercise 05 is a standalone standards-mapping drill that does not require a carried-forward tool.

1. [One-Page Acceptable-Use Policy Drill](exercises/exercise-01-one-page-acceptable-use-policy-drill.md) — the 1–2 page AUP draft with seven sections, co-author tags, and the one-sentence if-in-doubt default.
2. [Data-Handling SOP for an AI Tool](exercises/exercise-02-data-handling-sop-for-an-ai-tool.md) — the 2–3 page SOP with the five-step accident path and the security + privacy signing surface.
3. [Intake Questionnaire Co-Author](exercises/exercise-03-intake-questionnaire-co-author.md) — the completed questionnaire plus the 1-page schema-refinement memo to `senior-ai-governance-architect`.
4. [Governance Council Pre-Read Authoring](exercises/exercise-04-governance-council-pre-read-authoring.md) — the one-page three-section pre-read with named-ask-per-section discipline.
5. [NIST AI RMF GOVERN → Enablement Practice Map](exercises/exercise-05-nist-ai-rmf-govern-to-enablement-practice-map.md) — the eight-row mapping table plus the two-gap enablement-practice memo.

## Labs and quizzes

Lab and quiz prompts land in `labs/` and `quizzes/` on subsequent content cycles.

## Resources

External references: [`resources.md`](resources.md).

## How this module connects to the rest of the track

- Takes from [mod-101](../mod-101-role-and-the-org-wide-enablement-operating-model/README.md): the scope contract (Chapter 01) and the handoff map (Chapter 04) define the role boundaries this module's co-authoring posture operates inside; the EU AI Act Article 4 reading (Chapter 05) is the regulatory floor the AUP and training-roster evidence surfaces are built on.
- Takes from [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md): the use-policy and data-handling SOP *stubs* drafted in mod-102 Chapter 03 and Exercise 02 are the first drafts this module's walking-redline cycle redlines against; the approved-tooling envelope and Stage 2 candidate evaluation are what the intake questionnaire feeds.
- Feeds [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md): every policy change must couple to a training-package change in the same cycle, or operators learn two policies at once and default to whichever is easier.
- Feeds [mod-105](../mod-105-champion-networks-and-change-management/README.md): the champion network is the two-way field-signal interface — champions carry policy to operators and surface field signal back into the council pre-read (Chapter 02 Job 3).
- Feeds [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md): the executive scorecard's policy-compliance surfaces are evidenced by the redline log, the AUP ratification record, and the intake-queue status pipeline from this module.
- Feeds [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md): the data-handling SOP's ten-minute accident path hands off to incident response at the SOC-side boundary; Chapter 07's routing-out discipline is the shape of that handoff.
- Feeds [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md): the intake questionnaire from Chapter 06 is the same artifact that gates commissioned internal tools and custom agents, not only vendor tools.
- Feeds [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md): the AI governance council liaison seat (Chapter 02) and the walking-redline cadence (Chapter 01) are among the recurring operating-model rituals that run at CoE steady state.
