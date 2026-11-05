# mod-102 — Selecting and Rolling Out AI Tools at Organization Scale

**Estimated effort:** 22 hours
**Role level:** 45 · **Family:** AI Workforce

This module is where the role's judgement meets the calendar. Before you measure anything, co-author any policy, or run any champion network, you have to be able to *select* a tool at org scope and *roll it out* without quietly producing one of the four named failure modes. Those two moves — and the artifact set that flanks them — are the whole module.

## Learning objectives

- Run the three-stage tool-selection decision at enterprise scope — problem naming, candidate evaluation (build vs. buy, POCs, approved-tooling envelope), and pilot-vs-rollout commit — grounded in R1 (0.42, 11/26 postings) and R2 (0.31, 8/26 postings).
- Design bounded pilots with cohort, duration, baseline, and pre-written adopt / extend / kill decision criteria — refusing to let "the pilot went well" remain undefined.
- Produce the short artifact set a rollout needs before anyone opens the tool — use policy, data-handling SOP, access & offboarding playbook, training package, support & escalation path, champion list, kill-switch & rollback plan — grounded in R3 (0.65, 17/26 postings).
- Measure whether the rollout changed anything real — outcome metrics on the target task, workflow interviews as qualitative ground truth, usage telemetry only as sanity check — grounded in R4 (0.77, 20/26 postings).
- Recognise the common failure modes — the ghost-user rollout, the metric-theatre pilot, the champion-of-one, the policy-after-rollout retrofit — and author the pre-mortem that preempts each.
- Partner with `applied-ai-engineer` (peer, level 30) on commissioned internal agents and with `ai-risk-engineer` (peer, level 25) on the red-team evidence that flanks a rollout.

## Lecture chapters

1. [The Three-Stage Tool Selection Decision](01-the-three-stage-selection-decision.md) — problem naming, candidate evaluation (build vs. buy, scoped POC, approved-tooling envelope), pilot-vs-rollout commit, and the stage-gate review at each boundary.
2. [Designing Bounded Pilots with Pre-Written Decision Criteria](02-designing-bounded-pilots.md) — the five-section pilot charter: cohort, duration, baseline, adopt / extend / kill criteria written before launch, and kill switch. Why "the pilot went well" is not a sentence this role is allowed to say.
3. [The Rollout Artifact Set — What Must Exist Before Anyone Opens the Tool](03-the-rollout-artifact-set.md) — the seven artifacts (use policy, data-handling SOP, access & offboarding playbook, training package, support & escalation path, champion list, kill-switch & rollback plan), who co-authors each, who signs.
4. [Measuring Whether the Rollout Changed Anything Real](04-measuring-whether-the-rollout-changed-anything.md) — the three measurement layers in priority order: outcome metrics first, workflow interviews second, usage telemetry as sanity check.
5. [Failure Modes and the Pre-Mortem That Preempts Them](05-failure-modes-and-the-pre-mortem.md) — the four named failure modes (ghost-user, metric-theatre, champion-of-one, policy-after-rollout) and the one-page pre-mortem run at the end of Stage 3.
6. [Partnering with `applied-ai-engineer` and `ai-risk-engineer`](06-partnering-with-peers-on-evidence-and-build.md) — the commissioning brief, the red-team ask, what you hand off, and what you need back.

## Exercises

Carrying one chosen organization and one chosen tool across Exercises 01–05 will produce a coherent rollout bundle worth keeping. Exercise 06 is a sharper, standalone drill.

1. [Three-Stage Selection Worked Example](exercises/exercise-01-three-stage-selection-worked-example.md) — three one-pagers, one per stage, for a concrete organization.
2. [Co-Author the Use Policy with Governance](exercises/exercise-02-co-author-the-use-policy-with-governance.md) — the enablement-side draft the governance partner is happy to react to.
3. [The Weekly Executive Rollout Report](exercises/exercise-03-the-weekly-executive-rollout-report.md) — the one-page weekly, outcome first, usage demoted to a sanity check.
4. [Pilot Charter and Decision Criteria](exercises/exercise-04-pilot-charter-and-decision-criteria.md) — the five-section charter with concrete adopt / extend / kill triggers written before the pilot starts.
5. [Rollout Artifact Set Dry Run](exercises/exercise-05-rollout-artifact-set-dry-run.md) — all seven artifacts at outline depth with co-author signatures, plus a pre-mortem.
6. [Outcome Measurement vs. Usage Telemetry Drill](exercises/exercise-06-outcome-measurement-vs-usage-telemetry-drill.md) — three vignettes, three rewrites, three diagnoses.

## Labs and quizzes

Lab and quiz prompts land in `labs/` and `quizzes/` on subsequent content cycles.

## Resources

External references: [`resources.md`](resources.md).

## How this module connects to the rest of the track

- Takes from [mod-101](../mod-101-role-and-the-org-wide-enablement-operating-model/README.md): the operating model's intake path, decision-rights table, and scope contract are what you run selection and rollout *through*.
- Feeds [mod-103](../mod-103-policy-co-authoring-with-governance/README.md): the use policy stub drafted here (Chapter 03 artifact 1; Exercise 02) is the first draft the mod-103 co-authoring process redlines against.
- Feeds [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md): the training-package slot in the rollout artifact set (Chapter 03 artifact 4) is what mod-104 builds out at curriculum depth.
- Feeds [mod-105](../mod-105-champion-networks-and-change-management/README.md): the champion-list slot (Chapter 03 artifact 6) is what mod-105 designs as a two-way network.
- Feeds [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md): the rollout-level outcome measurement (Chapter 04) is what mod-106 aggregates into the org-wide executive scorecard.
- Feeds [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md): the kill-switch & rollback plan (Chapter 03 artifact 7) is what mod-109 *operates* when a rollout surfaces harm.
- Feeds [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md): the commissioning brief (Chapter 06) is the enablement-side interface mod-110 writes in depth.
