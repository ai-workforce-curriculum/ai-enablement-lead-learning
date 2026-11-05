# Reconciling the Tool Stack Across BUs

> Most enterprise AI tool stacks are not the result of a tool-selection strategy; they are the sedimentary record of twenty-four months of BU-level procurement decisions, each locally rational, globally overlapping. The enablement lead inherits the stack after it has already settled; the job is not to tear it up but to surface consolidation opportunities to leadership — in a form that does not strip teams of tools that are actually working. This chapter is the discipline that keeps the enablement program from funding five overlapping copilots without becoming the role that is remembered as the one who shut down the thing people liked.

## Why the stack sprawls

Four structural causes. Naming them is the first move; the remediation is matched to the cause.

- **Local-optimum procurement.** Each BU faces a specific workflow, finds a vendor that fits, and buys it. The procurement decision is locally correct; globally, the three BUs buy three different tools for overlapping work. The enablement lead who did not exist at the time of the decisions inherits the result.
- **Vendor land-and-expand into the platform.** The organization already runs M365 or Google Workspace or Salesforce. The vendor releases an AI add-on into that surface. BU adoption of the add-on is frictionless because it is already licensed; the add-on ships before the enablement program evaluates it, and overlaps a tool already chosen through formal selection.
- **Pilot sprawl.** The Stage 2 POCs from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) expand into informal rollouts without a Stage 3 commit. Two BUs pilot adjacent tools in the same category; both pilots quietly convert to running tools; no one consolidates.
- **The rip-out cost deterrent.** A BU with an operating tool that works will not give it up for a theoretical consolidation benefit. The tool is not switchable because switching has a real cost (operator relearning, workflow redesign, data migration) that the consolidation analysis has to internalize.

A reconciliation effort that does not name which of these four causes produced a specific overlap will produce the wrong remediation. The chapter's method opens with naming the cause, then moves to the economics.

## The reconciliation inventory

The inventory is the discipline that makes overlap visible. Three dimensions produce a stack map.

- **Task-category axis.** Across the organization, what task families are being addressed by AI tools? Drafting, summarization, meeting-notes, retrieval, code assistance, support-ticket handling, analyst / research, sales-call intelligence, incident response, clinical documentation, legal research — the list that [mod-106 Chapter 01](../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md) uses for scorecard category rollups applies here.
- **BU axis.** What business units are running tools in each category.
- **Tool axis.** What specific tools are in production, in pilot, in POC.

The intersection is the inventory cell: *for each (task-category × BU) cell, what tool(s) are in use?*

A sketch (illustrative only):

```
Task category     | BU A        | BU B         | BU C      | BU D
------------------+-------------+--------------+-----------+---------------
Drafting          | M365 Copilot| ChatGPT Ent  | Copilot + | M365 Copilot
                  |             |              | Claude    |
Meeting-notes     | M365 Copilot| Zoom AI Comp.| Otter.ai  | M365 Copilot
                  |             |              |           |
Code assistance   | GitHub Copi.| Cursor       | GitHub +  | — (no eng)
                  |             |              | Claude    |
Support copilot   | —           | —            | Ada       | Decagon
                  |             |              |           |
Internal search   | Glean (POC) | M365 Copilot | Glean     | ServiceNow
                  |             | search       |           | AI Search
Sales-call intel  | Gong        | Chorus       | —         | Gong
```

The inventory is deliberately named with concrete current-market tools (which will change) because the readability matters; the reader of the inventory should be able to see the overlap in seconds. A sanitized inventory with "Tool A" and "Tool B" labels is not readable in a steering meeting.

## Reading the inventory — four overlap patterns

The inventory reveals four patterns, each with a specific remediation.

### Pattern 1 — Platform add-on duplicates a standalone tool

Example in the sketch: BU B uses Microsoft Copilot search while also piloting Glean in BU A and BU C. Both do internal retrieval; the platform add-on may or may not match the standalone tool's quality on the specific internal-corpus task.

- **Remediation.** Run a bounded comparison using the matrix from [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md), weighted toward capability-fit on the specific internal corpus and TCO at scale. The platform add-on wins on TCO; the standalone wins on capability where it does. The consolidation case is for a decision at the task-category level, not a BU-level rip-out.

### Pattern 2 — Same vendor, different BUs, no shared contract

Example: BU A and BU D both run M365 Copilot through separate purchasing arrangements. The organization is paying retail across two contracts instead of an enterprise agreement.

- **Remediation.** Procurement-driven consolidation (see [Chapter 04](04-partnering-with-procurement-finance-and-it.md)). The Procurement renewal-plus-90 interface is the lever; consolidation to a single enterprise agreement is typically a 10-25% price improvement and does not require any tool change at the BU level.

### Pattern 3 — Overlapping tools in the same category across BUs

Example: BU A on Gong, BU B on Chorus, both doing sales-call intelligence. Two vendors, two integrations, two training surfaces, two sets of champions, two contracts.

- **Remediation.** This is the hardest case because both tools are usually operational. The consolidation case runs the matrix from [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) with switching cost explicitly weighted; it may conclude that the overlap is justified (meaningful capability differentiation, high switching cost) or that one tool should become the standard with a migration runway.

### Pattern 4 — Pilot sprawl inside a single BU

Example: BU C running GitHub Copilot and Claude in the same engineering org, with no decision between them. Pilots that did not close.

- **Remediation.** Close the Stage 3 decision from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md). One tool becomes the standard; the other closes or converts to a bounded experiment with a named end state. A BU with two competing coding copilots has an unresolved selection, not a diversified portfolio.

## The consolidation economics

A consolidation case is an ROI case ([Chapter 02](02-projecting-roi-with-confidence-bands.md)) with specific numerator and denominator shapes.

### Numerator — the value of consolidation

Three sources of value, each separately defended.

- **License-cost reduction.** Volume pricing at the consolidated contract typically improves per-seat pricing by 10-25% versus fragmented pricing. The savings are the delta between fragmented list price and consolidated contract price, net of any contractual complexities (true-ups, mid-term uplifts).
- **Operating-cost reduction.** Fewer vendors to manage, fewer integrations to maintain, fewer training surfaces, fewer champion networks. Family 2, 3, 4, 5, and 6 lines from [Chapter 01](01-the-enablement-cost-model-at-org-scope.md) all reduce; the reductions are harder to quantify than license-cost reduction and should be reported with wider bands.
- **Standardization benefits.** Shared playbooks, cross-BU mobility of operator skills, centralized policy enforcement, fewer surfaces for governance review. Qualitative; reported as narrative rather than a number unless specific instances are attributable.

### Denominator — the cost of consolidation

Three sources of cost, each separately defended. The denominator discipline from [Chapter 01](01-the-enablement-cost-model-at-org-scope.md) applies.

- **Switching cost.** Operator relearning, workflow redesign, data migration, integration rebuild, lost-productivity dip during transition. Model as a one-time cost spread across the transition period. The literature on technology transitions suggests the productivity dip is typically 3-6 months for non-trivial workflow tools; model honestly.
- **Reduced optionality.** A consolidated stack has fewer options to pull if the chosen vendor fails to deliver. Price as the expected cost of vendor-swap-under-duress, weighted by the probability of needing to swap.
- **Local-optimum sacrifice.** If a BU was on a tool that genuinely fit its workflow better than the consolidation target, the difference in workflow fit is a real cost. Measure through workflow interviews ([mod-106 Chapter 01](../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md)) before and after; carry the delta on the honest side of the ledger.

### The crossover point

A consolidation case is economically positive when the net value exceeds the switching cost over a reasonable horizon (typically two years; some organizations use three). A consolidation case that is only positive on year-five math is a case where the organization is making a long bet; name the horizon.

The two-year crossover is the honest default. Shorter horizons are available but harder to defend against the productivity-dip pattern.

## Surfacing consolidation without stripping teams

The hardest part of the chapter — and of the role. Consolidation that reads to the operators as "the central team is taking away my tool" fails even when the economics are favourable.

### The surfacing move

Five principles that keep the consolidation move credible.

- **Surface to leadership, not to the operators first.** The consolidation case goes to the executive sponsor, Finance, and Procurement first. The decision is at the altitude of the budget conversation; it is not an operator-level change until the decision is made.
- **Carry the local-optimum sacrifice on the writeup.** If consolidation sacrifices a tool that is genuinely working well in BU B, write that on the case — "BU B operators report high workflow fit on Chorus; consolidation to Gong trades local fit for standardization and X in net savings." The reviewer should not have to find this; the enablement lead should put it there.
- **Timeline the transition deliberately.** A consolidation move is not a one-quarter cut-over. 6-12 months is typical; longer for complex tools. The transition plan is part of the case.
- **Protect the champion network across the transition.** The champions who became expert on the retired tool are the first to feel undermined by consolidation. Explicitly re-skill them on the consolidation target and carry them forward; the champions who feel abandoned become resistance nodes ([mod-105 Chapter 06](../mod-105-champion-networks-and-change-management/06-ai-specific-resistance-patterns-adkar-and-kotter.md)).
- **Leave exceptions where they are earned.** A consolidation case that forces a BU to abandon a differentiated tool that is producing measurable value is a weaker case than one that permits a documented exception. Exceptions are specific, time-bound, and reviewed at the next cycle — not a rejection of the consolidation discipline.

### The failure patterns

Three ways the surfacing move fails, each with a specific tell.

- **The clear-the-decks reconciliation.** The enablement lead proposes a wholesale consolidation across every category. The case has aggressive savings numbers; the switching cost and local-optimum sacrifice lines are thin. Operators experience it as a mass tool removal. Tell: the case is framed around savings headline, with switching cost in a footnote. Remediation: force switching cost onto the first page.
- **The vendor-driven consolidation.** A vendor whose tool is winning across the comparison matrix proposes an enterprise agreement that locks the organization into a single-vendor stack. The consolidation case is correct but the lock-in is the un-named cost. Tell: the writeup names consolidation value but is silent on vendor concentration; cross-check with [Chapter 06](06-the-vendor-vetting-rubric.md).
- **The consolidation that never ships.** The consolidation case is correct, the executive sponsor agrees, and the decision is deferred for six quarters because the switching is too painful. Tell: the same consolidation opportunity appears on the stack map every cycle without movement. Remediation: scope the decision around a specific contract renewal date; renewal moments are when consolidation decisions actually land, not between them.

## The cadence

Reconciliation runs on an annual cycle, aligned to the budget cycle from [Chapter 04](04-partnering-with-procurement-finance-and-it.md), with a mid-year check.

- **Annual stack inventory.** 4-6 weeks of work, concurrent with the annual budget cycle. The inventory, the overlap pattern map, the consolidation cases.
- **Mid-year check.** Shorter; typically one meeting with Procurement and Finance. New tools that entered the stack since the annual inventory, upcoming contract renewals, early signals that consolidation targets are slipping.
- **Standing renewal-plus-90 reviews from [Chapter 04](04-partnering-with-procurement-finance-and-it.md).** Each renewal is a chance to re-open the consolidation question for that specific vendor.

## Where this chapter feeds

- [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) is the comparison frame used inside each consolidation case.
- [Chapter 04](04-partnering-with-procurement-finance-and-it.md) is the running partnership that converts a consolidation decision into contract terms.
- [Chapter 06](06-the-vendor-vetting-rubric.md) is what prevents consolidation from becoming unmanaged vendor concentration.
- Feeds [mod-105 Chapter 06](../mod-105-champion-networks-and-change-management/06-ai-specific-resistance-patterns-adkar-and-kotter.md) when transition triggers resistance patterns.
- Feeds [mod-106 Chapter 01](../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md) by producing cleaner category rollups once the stack has fewer within-category tools.

## Summary

- Four structural causes of stack sprawl: local-optimum procurement, platform add-on land-and-expand, pilot sprawl without Stage 3 commit, rip-out cost deterrent. Remediation is matched to cause.
- The reconciliation inventory is a (task-category × BU × tool) grid, named with concrete current-market tools, that makes overlap readable in seconds.
- Four overlap patterns: platform add-on duplicates standalone; same vendor across BUs with no shared contract; overlapping tools in same category across BUs; pilot sprawl inside a single BU. Each has its own remediation shape.
- The consolidation case is an ROI case ([Chapter 02](02-projecting-roi-with-confidence-bands.md)): numerator is license + operating + standardization value; denominator is switching + reduced-optionality + local-optimum-sacrifice cost. Two-year crossover is the honest default horizon.
- Five surfacing principles that keep consolidation credible: surface to leadership first, carry local-optimum sacrifice on the writeup, timeline the transition deliberately, protect champions across transitions, leave earned exceptions.
- Three failure patterns: clear-the-decks reconciliation, vendor-driven consolidation, consolidation that never ships. Each has a specific tell.
- Annual stack inventory aligned to the budget cycle, mid-year check, standing renewal-plus-90 reviews — the cadence that keeps consolidation a running discipline rather than a one-time event.
