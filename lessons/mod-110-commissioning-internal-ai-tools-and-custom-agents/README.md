# mod-110 — Commissioning Internal AI Tools and Custom Agents

**Estimated effort:** 12 hours
**Role level:** 45 · **Family:** AI Workforce

This is the module where the enablement lead buys a build. Across the preceding modules the role has been running a rollout artefact set over commercial tools: a vendor product, a platform add-on, an envelope-approved point tool. In mod-110 the rollout is still enablement-shaped — the same policy stack, the same training curriculum, the same champion network, the same scorecard — but the thing being rolled out does not exist until somebody builds it. That somebody is not the enablement lead. It is an `applied-ai-engineer` (peer, level 30), an `agentic-ai-engineer` (peer, AI Engineering family), or — when the problem is a platform rather than a point tool — an `agentic-systems-architect` (peer, AI Engineering family). The role's job is to **commission**: to author the brief the engineer builds against, to inherit prototypes from the consultants and business users who built the demo that triggered the project, to keep the measurement on the mod-106 framework rather than on a separate internal-build scorecard, and to make the honest no-go call when a prototype should not graduate.

The commissioning interface was named at a surface level in [mod-102 Chapter 06](../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md). This module is the depth. The build-vs-buy decision from [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) is upstream: when the matrix picks Column 4 — internal build — the commissioning brief in this module's Chapter 02 is what the engineer receives. Everything else flows from that artefact.

## Learning objectives

- Act as the commissioner — not the builder — of internal AI tools and custom agents the organization needs; grounded in R16 (0.38, 10/26 postings; co-owned with `applied-ai-engineer`).
- Author the commissioning brief — problem, audience, success criterion, non-negotiable guardrails, budget, timeline, maintenance commitment — that an `applied-ai-engineer` (peer, level 30) or `agentic-ai-engineer` (peer, AI Engineering family) can build against.
- Inherit prototypes from billable consultants or business users (R16 evidence: p-019 ClearView Healthcare Partners) — productionize-worthiness assessment, documentation requirement, support commitment, and the honest no-go call when a prototype should not graduate.
- Hand architectural depth to `agentic-systems-architect` (peer, AI Engineering family) — agent control planes, knowledge gateways, context layers (R20 below-threshold, 0.19) — this role does not build the agent platform, but understands what it is buying or building into.
- Measure commissioned tools on the same outcome / workflow / usage framework from [mod-102 Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md) and [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) — not on a separate internal-build scorecard.

## Lecture chapters

1. [The Commissioner Stance — Not the Builder](01-the-commissioner-stance-not-the-builder.md) — the brief-shaped authority the role carries with four peers (`applied-ai-engineer`, `agentic-ai-engineer`, `agentic-systems-architect`, `ai-risk-engineer`), the three postures that collapse the role on contact with an engineering team, and the one-paragraph test a request has to pass before it becomes a commission.
2. [The Commissioning Brief as the Load-Bearing Artifact](02-the-commissioning-brief-as-the-load-bearing-artifact.md) — the eight-section brief in operational depth, the questions each section answers, what engineers cannot work without, and the stage-gate review the brief passes through before a build starts.
3. [Inheriting Prototypes and the Honest No-Go](03-inheriting-prototypes-and-the-honest-no-go.md) — the ClearView-pattern inheritance of consultant-built and business-user-built prototypes, the productionize-worthiness assessment, the documentation and support-commitment requirements, and the honest no-go call when a prototype should not graduate.
4. [Handing Architectural Depth to the Agentic Systems Architect](04-handing-architectural-depth-to-the-agentic-systems-architect.md) — agent control planes, knowledge gateways, context layers; the vocabulary the commissioner understands without pretending to design at architectural depth; the three recurring architectural choices the commissioner is consulted on but does not own.
5. [Measuring Commissioned Tools on the Rollout Framework](05-measuring-commissioned-tools-on-the-rollout-framework.md) — the outcome / workflow / usage stack from mod-102 Chapter 04 and mod-106 applied to internal builds, the two temptations that collapse into an internal-build scorecard, the eval-harness surface the engineer owns and the outcome surface the commissioner owns, and the three cadences the measurement plan runs on.
6. [Signing Surfaces, Maintenance Commitments, and the Hand-Off Calendar](06-signing-surfaces-maintenance-and-handoff-calendar.md) — the signed brief, the maintenance owner, the hand-off calendar, the three tenure phases of a commissioned tool (acceptance, steady state, graduation or retirement), and when a commissioned tool becomes a vendor-shaped tool inside the mod-107 vendor portfolio.

## Exercises

The four exercises carry one chosen organization and one chosen commissioning target from Exercise 01 through Exercise 04. The artefact bundle produced is a coherent commission that an `applied-ai-engineer` could begin building against on the day Exercise 03 is submitted.

1. [Commissioning Brief Drill](exercises/exercise-01-commissioning-brief-drill.md) — the eight-section brief at full depth for a chosen problem, with the stage-gate review summary and the two-paragraph scope contract the brief will be signed against.
2. [Prototype Inheritance and Productionise Decision](exercises/exercise-02-prototype-inheritance-and-productionise-decision.md) — the productionize-worthiness assessment against the five dimensions (problem fit, data posture, operational fit, cost shape, maintenance fit); a productionise / rebuild / no-go recommendation with the honest no-go memo if the recommendation is no-go.
3. [Handoff Contract with Applied AI Engineer](exercises/exercise-03-handoff-contract-with-applied-ai-engineer.md) — the three-page handoff contract against the signed brief from Exercise 01, including the acceptance-criteria table, the eval-harness ownership split, and the running cadence through acceptance.
4. [Commissioned Tool Measurement Plan](exercises/exercise-04-commissioned-tool-measurement-plan.md) — the measurement plan for the commissioned tool on the mod-102/mod-106 framework, the eval-harness-vs-outcome split, the three-cadence running plan, and the misses-first scorecard slot for the tool inside the portfolio view.

## Labs and quizzes

Lab and quiz prompts land in `labs/` and `quizzes/` on subsequent content cycles.

## Resources

External references: [`resources.md`](resources.md).

## How this module connects to the rest of the track

- Takes from [mod-101](../mod-101-role-and-the-org-wide-enablement-operating-model/README.md): the scope contract and the handoff map define the boundary the commissioner holds with the AI Engineering family and with `ai-risk-engineer`.
- Takes from [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md): [Chapter 06](../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md) is the surface-level commissioning interface; this module is its depth. The rollout artefact set from [Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) and the outcome measurement from [Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md) wrap the commissioned tool the same way they wrap a vendor tool.
- Takes from [mod-103](../mod-103-policy-co-authoring-with-governance/README.md): the policy stack bounds the non-negotiable guardrails section of the commissioning brief ([Chapter 02](02-the-commissioning-brief-as-the-load-bearing-artifact.md)); the routing-out discipline bounds what the commissioner writes versus what governance writes.
- Takes from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md): the outcome / workflow / usage framework is reused for commissioned tools ([Chapter 05](05-measuring-commissioned-tools-on-the-rollout-framework.md)); internal builds enter the portfolio scorecard on the same surface as vendor tools.
- Takes from [mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md): when [Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) picks Column 4 (internal build), the commissioning brief in this module's [Chapter 02](02-the-commissioning-brief-as-the-load-bearing-artifact.md) is the deliverable the matrix hands off to.
- Feeds [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md): commissioned tools run the same incident path as vendor tools, and the commissioner is closer to the engineering team on root-cause investigation than they are on a vendor incident.
- Feeds [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md): the commissioning cadence, the maintenance-owner review, and the portfolio-view slot for internal builds become recurring CoE operating rituals; R16 is the co-owned CoE responsibility with the `applied-ai-engineer` manager.
