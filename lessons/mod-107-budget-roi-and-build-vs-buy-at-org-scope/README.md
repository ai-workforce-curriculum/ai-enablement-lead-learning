# mod-107 — Budget, ROI, and Build-vs-Buy at Organization Scope

**Estimated effort:** 14 hours
**Role level:** 45 · **Family:** AI Workforce

This is the module where the enablement program defends its economics. Before the industry-specific flavouring in mod-108, before the incident path in mod-109, before commissioning internal tools in mod-110, the role has to be able to *build a complete cost model*, *project ROI with defensible confidence bands*, *run a build-vs-buy matrix at enterprise scope*, *operate a three-way partnership with Procurement, Finance, and IT*, *consolidate overlapping tool spend without stripping teams of working tools*, and *keep a lightweight vendor-vetting rubric current*. The scorecard-facing ROI slice from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) is the input; the annual budget, the build-vs-buy decisions, the consolidation cases, and the vendor-portfolio view are the operating output. Six chapters, five exercises.

## Learning objectives

- Build the cost model for enablement — tool licenses, enablement-program spend, embedded enablement partner FTE, training production, champion-network operating cost, support — grounded in R14 (0.35, 9/26 postings).
- Project ROI on priority use cases with a defensible value-realisation framework — magnitude, timing, attribution, confidence — and refuse point estimates that don't carry a confidence band.
- Run the build-vs-buy matrix at enterprise scope — AI coding / knowledge-work copilots (Cursor, Copilot, Claude Code, Windsurf), platform add-ons (Microsoft Copilot, Google Gemini for Workspace, Zoom AI Companion), industry-specific tools, and the internal-build option.
- Partner with procurement on contracts (DPA, SOC 2, model-provenance, data-residency terms), with finance on budgeting and cost recovery, and with IT on licensing — handing contract execution out of scope.
- Reconcile the tool stack across BUs so the enablement program does not fund five overlapping copilots; surface the consolidation opportunity to leadership without stripping teams of working tools.
- Monitor R17 (vendor / external-partner management, 0.23 — below-threshold but one cycle from clearing the bar) with a lightweight vendor-vetting rubric.

## Lecture chapters

1. [The Enablement Cost Model at Org Scope](01-the-enablement-cost-model-at-org-scope.md) — the six-family taxonomy (tool licenses, enablement-program direct spend, training production, embedded FTE, champion-network operating cost, downstream support/risk/operating), the sourcing map that assigns each family an authoritative source and a reconciliation cadence, a worked numerical example, five named undercounts, and the monthly/quarterly/annual cadences that keep the denominator current.
2. [Projecting ROI with Confidence Bands](02-projecting-roi-with-confidence-bands.md) — the four-dimensional value-realisation framework (magnitude, timing, attribution, confidence), the J-curve shape of rollout value, composing confidence bands analytically or via Monte Carlo, refusing point estimates in three recurring forms, three prioritisation frames, three projection-specific theatre patterns.
3. [The Build-vs-Buy Matrix at Enterprise Scope](03-the-build-vs-buy-matrix-at-enterprise-scope.md) — the four-column matrix (coding / knowledge-work copilots, platform add-ons, industry-specific tools, internal build), the ten-dimension comparison frame, TCO shape per column, reusable column-wins patterns, three failure modes (vendor capture, build hubris, capability-only scoring), and the signed-artifact shape.
4. [Partnering with Procurement, Finance, and IT](04-partnering-with-procurement-finance-and-it.md) — six contract-term surfaces (DPA, AI addenda, security attestations, data residency, model provenance / sub-processor flow-down, commercial terms) and four Procurement interfaces; the Finance partnership extended to annual budget, scenario modelling, and three cost-recovery models; the IT partnership on licensing, SSO/SCIM/admin, and operational load; explicit out-of-scope lines on contract execution, budget authority, and IT operational decisions.
5. [Reconciling the Tool Stack Across BUs](05-reconciling-the-tool-stack-across-bus.md) — four structural causes of stack sprawl, the task-category × BU × tool inventory grid, four overlap patterns with matched remediations, consolidation economics with switching-cost discipline, five surfacing principles for leadership-facing consolidation cases, three failure patterns, annual/mid-year/renewal-plus-90 cadence.
6. [The Vendor Vetting Rubric](06-the-vendor-vetting-rubric.md) — the lightweight six-dimension rubric (capability trajectory, data and model posture, security and compliance, commercial resilience, operating / admin surface, switching and exit) proportional to R17 at 0.23, four trigger types, portfolio-level concentration view, three named failure modes, written to carry heavier weight if R17 clears the threshold next cycle.

## Exercises

Carrying one chosen organization and one chosen portfolio across Exercises 01, 02, 03, and 05 will produce a coherent budget-and-ROI bundle worth keeping. Exercise 04 is a sharper, self-contained drill on the partnership contract.

1. [Enablement Cost Model Drill](exercises/exercise-01-enablement-cost-model-drill.md) — construct a full six-family cost model for one chosen organization, with the sourcing map, materiality threshold, methodology appendix, and the five-named-undercount defence.
2. [ROI Projection with Confidence Bands](exercises/exercise-02-roi-projection-with-confidence-bands.md) — project ROI on a priority rollout over a three-year horizon with a J-curve, composed confidence band, sensitivity analysis, and a prioritisation-frame statement.
3. [Org-Scope Build-vs-Buy Matrix](exercises/exercise-03-org-scope-build-vs-buy-matrix.md) — run the four-column matrix on a concrete target task with ten dimensions, TCO shapes, projected ROI bands, and a signed-artifact recommendation.
4. [Procurement and Finance Partnership Contract](exercises/exercise-04-procurement-and-finance-partnership-contract.md) — draft the standing operating contract across Procurement, Finance, and IT, including pre-negotiation briefing, redline review protocol, and the running cadence.
5. [Tool Stack Consolidation Worked Example](exercises/exercise-05-tool-stack-consolidation-worked-example.md) — build the inventory grid, surface overlap patterns, model the consolidation economics with switching cost, and draft the executive-sponsor surfacing memo.

## Labs and quizzes

Lab and quiz prompts land in `labs/` and `quizzes/` on subsequent content cycles.

## Resources

External references: [`resources.md`](resources.md).

## How this module connects to the rest of the track

- Takes from [mod-101](../mod-101-role-and-the-org-wide-enablement-operating-model/README.md): the scope contract and the handoff map define which partners the three-way partnership in [Chapter 04](04-partnering-with-procurement-finance-and-it.md) actually involves.
- Takes from [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md): [Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md)'s build-vs-buy line is operationalized at depth in [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md); the Stage 3 gate carries the four-column matrix.
- Takes from [mod-103](../mod-103-policy-co-authoring-with-governance/README.md): the policy and DPA work bounds the data-posture dimension in the vendor-vetting rubric ([Chapter 06](06-the-vendor-vetting-rubric.md)) and shapes the Procurement contract review ([Chapter 04](04-partnering-with-procurement-finance-and-it.md)).
- Takes from [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md): training-production spend is Family 3 in the cost model ([Chapter 01](01-the-enablement-cost-model-at-org-scope.md)).
- Takes from [mod-105](../mod-105-champion-networks-and-change-management/README.md): champion-network operating cost is Families 4 and 5 in the cost model; resistance patterns shape the surfacing discipline for consolidation moves ([Chapter 05](05-reconciling-the-tool-stack-across-bus.md)).
- Takes from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md): [Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) is the scorecard-facing ROI slice; this module is its depth.
- Feeds [mod-108](../mod-108-industry-and-regulatory-flavours-of-enablement/README.md): industry-specific regulatory contexts shape the compliance dimension in the vendor-vetting rubric and the industry-tool column in the build-vs-buy matrix.
- Feeds [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md): Family 6 of the cost model includes incident-response cost; vendor-vetting rubric signals feed incident-adjacent risk.
- Feeds [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md): when Column 4 wins in [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md), mod-110 picks up the commissioning brief.
- Feeds [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md): the three-way partnership cadence, the vendor portfolio view, and the annual budget cycle become standing CoE operating rituals.
- Feeds [mod-112](../mod-112-career-positioning-and-the-next-step-on-the-ladder/README.md): defending economics in front of a CFO and a board is among the capabilities that distinguish the enablement lead at level 45 from the next-step-up roles.
