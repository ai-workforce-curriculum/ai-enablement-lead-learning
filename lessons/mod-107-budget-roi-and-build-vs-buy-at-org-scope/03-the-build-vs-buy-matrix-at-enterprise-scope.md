# The Build-vs-Buy Matrix at Enterprise Scope

> [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) required that every Stage 2 writeup carry an explicit build-vs-buy line, even when the answer is trivial. This chapter is the *depth* behind that line: the full enterprise matrix across the four live tool categories (coding / knowledge-work copilots, platform add-ons, industry-specific tools, internal build), the comparison frame that composes with the cost model from [Chapter 01](01-the-enablement-cost-model-at-org-scope.md) and the projection from [Chapter 02](02-projecting-roi-with-confidence-bands.md), and the common failure modes that turn a defensible decision into a vendor-captured one or a sunk-cost build. The chapter is deliberately concrete about current-market tools; the tools will change, the matrix will not.

## Why build-vs-buy is a distinct discipline at enterprise scope

At one rollout, build-vs-buy fits in a paragraph. At enterprise scope with ten-plus rollouts across six BUs, three things make it a distinct discipline.

- **The matrix has four columns, not two.** The enterprise choice is not build-versus-buy as a binary; it is a selection across (a) a coding / knowledge-work copilot, (b) a platform add-on from a SaaS the organization already runs, (c) an industry-specific tool, and (d) an internal build. Each column has a different cost shape, a different data posture, and a different maintenance commitment.
- **Candidate families overlap on capability but diverge on surface.** A general-purpose copilot and the Microsoft Copilot add-on both do meeting-summary work; they differ on data boundary, admin surface, data residency, and procurement cost. The naive matrix compares them on capability alone and gets the decision wrong.
- **The decision composes with the stack, not in isolation.** A buy decision on a vendor the organization already has three tools from is a different decision than the same buy from a new vendor. The consolidation discipline in [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) is what composes with the matrix; running the matrix alone and the consolidation alone produces inconsistent decisions.

The role of this chapter is to make the four-column matrix the standard shape of a build-vs-buy writeup and to make the vocabulary portable across cases.

## The four columns — what each is and what it is not

### Column 1 — Coding / knowledge-work copilots

General-purpose AI assistants deployed into developer, writer, analyst, or support workflows as standalone tools. Current-market examples: GitHub Copilot, Cursor, Claude Code, Windsurf, Amazon CodeWhisperer-adjacent offerings, JetBrains AI Assistant.

- **Where the capability lives.** The vendor hosts the model and the tool; the organization integrates via plugins, IDEs, or desktop apps. The vendor controls the model roadmap, the capability ceiling, and the pricing.
- **Where the data boundary is.** Prompts, completions, and sometimes context from the user's files travel to the vendor. The vendor's enterprise tier typically offers a "no-training-on-your-data" commitment ([Chapter 04](04-partnering-with-procurement-finance-and-it.md) treats the contract term); verify it, do not assume it.
- **What you are buying.** Access to the vendor's model and tool surface, the vendor's model-update rhythm, the vendor's admin and audit surfaces. Not: ownership, the underlying model weights, control over roadmap.
- **What you are committing to.** The vendor's pricing elasticity, the vendor's product decisions, and the integration surface. Switching costs scale with how deeply the tool is woven into the daily workflow.

### Column 2 — Platform add-ons

AI features added to SaaS platforms the organization already runs. Current-market examples: Microsoft Copilot (across M365, Teams, Dynamics), Google Gemini for Workspace, Zoom AI Companion, Salesforce Einstein, Atlassian Rovo, ServiceNow Now Assist, Notion AI.

- **Where the capability lives.** Inside a platform the organization is already contracted with, running against the organization's data already in that platform. The vendor hosts; the data is already under the vendor's existing data-processing addendum.
- **Where the data boundary is.** Often the same data boundary as the parent SaaS, with explicit AI-feature addenda (see [Chapter 04](04-partnering-with-procurement-finance-and-it.md) on the DPA / AI addendum structure). Data residency usually inherits from the parent SaaS; verify per-add-on.
- **What you are buying.** The add-on tier, usually priced per-user per-month on top of the base platform. Integration work is often minimal because the add-on sits inside the admin surface already in use.
- **What you are committing to.** Deeper lock-in to the platform SaaS; the add-on increases the switching cost of the platform itself. Add-ons often ship AI features earlier than the capability-ceiling vendors in Column 1 reach parity, and often with less admin control.

### Column 3 — Industry-specific tools

AI tools designed for a specific function, industry, or regulated workflow. Examples (not exhaustive, not an endorsement): legal research (Harvey, Spellbook, legal-tech category), clinical documentation (Nuance DAX, Abridge, Suki), customer support (Ada, Decagon, Forethought, vendor-specific CS copilots), sales-call intelligence (Gong, Chorus, Clari AI), financial-services advisory tools, cybersecurity co-pilots (Microsoft Security Copilot, SentinelOne Purple AI, CrowdStrike Charlotte AI).

- **Where the capability lives.** Vendor-hosted, tuned on domain-specific data, often with domain-specific compliance posture (HIPAA BAA, SOC 2 Type II, specific industry standards).
- **Where the data boundary is.** Varies widely; the industry-specific tool usually has the most domain-specific data terms and the most variation in data-residency posture across vendors.
- **What you are buying.** Domain-specific capability that general-purpose tools (Columns 1 and 2) do not match. Also: domain-specific accuracy, domain-specific compliance posture, domain-specific vocabulary and workflow integration.
- **What you are committing to.** Narrower addressable surface; the industry-specific tool often serves one function (legal, clinical, support) and is not reusable across the stack. Vendor concentration risk is higher — fewer alternatives if the vendor goes down, pivots, or is acquired.

### Column 4 — Internal build

Custom tools built by internal engineering against hosted or self-hosted models. Scope ranges from a thin wrapper around a hosted model API, to a RAG-based internal knowledge assistant, to a domain-specific agent commissioned under [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md).

- **Where the capability lives.** Inside the organization's engineering function. The organization owns the code; the model is usually hosted (API-based) and sometimes self-hosted.
- **Where the data boundary is.** The organization defines it. This is the column's strongest advantage: the data boundary can be tighter than any vendor's, assuming the engineering function is competent to run it.
- **What you are buying.** Workflow fit, data-boundary control, the option to internalize logic that no vendor captures.
- **What you are committing to.** Forever maintenance. An internal build is an operating responsibility of the engineering function for the life of the tool. The maintenance commitment is the line most often undercounted at build-decision time.

## The comparison frame — ten dimensions

Every build-vs-buy case compares the live candidates across the same ten dimensions. The uniformity is what makes the matrix readable at enterprise scale.

- **Capability fit for the target task.** Does the tool do the Stage 1 target task from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md)? Measured in the Stage 2 POC. A score; do not collapse to a go/no-go.
- **Total cost of ownership over the projection horizon.** Not the subscription cost — the full denominator from [Chapter 01](01-the-enablement-cost-model-at-org-scope.md) applied to this candidate: licenses or compute, enablement spend specific to this rollout, embedded FTE, training production, champion program share, downstream support. See the TCO section below.
- **Projected ROI with band.** From [Chapter 02](02-projecting-roi-with-confidence-bands.md). Report central estimate and band; a candidate with a narrower band at a lower central estimate may win against a candidate with a higher central estimate and a wide band.
- **Data boundary.** What data crosses to the vendor, under what terms, with what training-use posture and retention. See [Chapter 04](04-partnering-with-procurement-finance-and-it.md).
- **Data residency.** Where the data is stored and processed; regulatory fit for the organization's jurisdictions.
- **Security and compliance posture.** SOC 2 Type II, ISO 27001, industry-specific (HIPAA BAA, PCI-DSS attestation, FedRAMP level if applicable), model-provenance attestations where available. See [Chapter 04](04-partnering-with-procurement-finance-and-it.md) and [Chapter 06](06-the-vendor-vetting-rubric.md).
- **Switching cost.** Lock-in depth. Platform add-ons (Column 2) increase parent-SaaS switching cost; industry tools (Column 3) are narrowly swappable within the same category; coding copilots (Column 1) are relatively swappable at the IDE-plugin layer; internal builds (Column 4) are not swappable.
- **Vendor concentration and resilience.** How many alternatives exist if the vendor fails, pivots, or is acquired. See [Chapter 06](06-the-vendor-vetting-rubric.md).
- **Capability ceiling and roadmap.** How fast the vendor is adding capability; whether the roadmap aligns with the organization's needs. Column 1 and Column 2 vendors often have the fastest capability-add rate; Column 3 vendors sometimes lag behind general-purpose tools inside twelve months.
- **Operating complexity.** How much the enablement, security, and IT operating load the tool adds. Platform add-ons (Column 2) often add the least; internal builds (Column 4) add the most.

### Scoring the matrix

Score each dimension 1-5 or weighted 0-100 against each candidate. Weights are chosen per-case with the problem owner from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md); typical weight pools concentrate on capability fit, TCO, projected ROI, data boundary, and compliance for regulated contexts. The remaining dimensions act as *disqualifiers* — a low score on switching cost or vendor concentration may not change the winner but is a line on the writeup that a reviewer can act on.

The matrix produces a *ranked recommendation with reasoning*, not a numerical winner that pretends the scoring is objective. Publish the weights alongside the ranking; the weight choice is part of the decision.

## TCO over the projection horizon

Total cost of ownership is the denominator from [Chapter 01](01-the-enablement-cost-model-at-org-scope.md) projected across the candidate-decision horizon (typically three years, matching the budget and build-vs-buy projection horizon from [Chapter 02](02-projecting-roi-with-confidence-bands.md)). Different columns have different TCO shapes.

### TCO shape for Column 1 (coding / knowledge-work copilots)

- **Front-loaded enablement, back-loaded license.** Year one is enablement-heavy (training, champions, rollout labor); year two and three are mostly license and support.
- **Price elasticity and renewal uplift.** Vendor contracts routinely include a 7-15% annual uplift; project it into years two and three unless the contract specifically locks the rate.
- **Add-on and tier creep.** Line items added across the horizon — enterprise security tier, admin add-ons, advanced features released after year one. Model a reasonable creep.

### TCO shape for Column 2 (platform add-ons)

- **Low integration cost; high license cost at scale.** Platform add-ons are cheap to integrate (they ride on existing admin) but expensive per-user at scale (M365 Copilot and equivalent are typically priced in the $360/user/year range or higher). The denominator is dominated by license.
- **Tightly coupled to platform contract.** A re-negotiation of the parent SaaS contract usually drags the AI add-on with it; check the contract shape with Procurement ([Chapter 04](04-partnering-with-procurement-finance-and-it.md)).

### TCO shape for Column 3 (industry-specific tools)

- **Higher per-seat cost, narrower addressable surface.** Industry tools often cost two to five times the per-seat rate of general-purpose copilots but deliver domain-specific value general-purpose tools cannot.
- **Compliance-posture cost is embedded.** The compliance attestation that makes the tool usable in the regulated workflow is part of what the per-seat price is buying; remember this when comparing to lower-priced general-purpose tools that would need the same posture built from scratch.

### TCO shape for Column 4 (internal build)

- **Front-loaded build cost; ongoing operating cost.** Year zero / year one is engineering-heavy; subsequent years are ongoing operating cost — model hosting or API usage, maintenance, iteration, incident response, security review.
- **The maintenance commitment is the long line.** 1-3 full-time engineering seats on an ongoing basis is typical for a non-trivial internal build; this cost persists for the life of the tool. The build case that forgets ongoing maintenance has typically understated TCO by 40-70% across the three-year horizon.
- **Build cost scales with ambition.** A thin wrapper over a hosted model may be 0.5 FTE for 2-3 months; a RAG-grounded internal copilot with role-based access and admin surface may be 4-8 FTE for 6-9 months; an agentic workflow with tool-calling and auditability may be 6-12 FTE for a year-plus. Scope honestly.

## When each column wins

Reusable patterns from the matrix across cases.

- **Column 2 wins on commodity workflow value inside an existing SaaS surface.** Meeting summaries in Teams or Zoom, document drafting inside M365 or Workspace, standard-feature use cases. The platform add-on is already integrated, already covered by a DPA, and does not require a new vendor relationship.
- **Column 1 wins on frontier capability and cross-tool reach.** Coding assistants with the strongest capability ceilings are usually Column 1; a Column 2 coding add-on typically lags by 6-18 months in capability. Also: knowledge-work tools that need to reach across multiple SaaS surfaces.
- **Column 3 wins on domain-specific accuracy, workflow fit, and compliance posture.** Clinical documentation, legal research, regulated customer-service workflows, specialized analyst work. The general-purpose alternative is almost always worse on the domain-specific quality bar, and the compliance posture is non-trivial to replicate.
- **Column 4 wins on data-boundary constraints no vendor can meet, differentiated workflow value no vendor sees, or forced build by regulation.** Rare; when it does win, [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md) carries the commissioning brief. Most internal-build decisions that are *not* driven by one of these three triggers are vendor-market-misread — the capability the team wants to build will arrive from a vendor inside twelve months.

The chapter does not mandate a winner. It mandates that the writeup show the four columns, the ten dimensions, the weights, and the reasoning; the winner is a judgement call with defensible method underneath.

## Failure modes — three patterns to catch in your own writeup

- **Vendor capture.** The writeup ran the matrix against one column (usually Column 1 or Column 2) because a vendor conversation was already in motion. The other three columns are represented as single-line dismissals. Tell: the writeup has three columns effectively empty. Remediation: run the matrix with all four columns genuinely considered, even when the answer is obvious; the empty columns make the decision faster, not less rigorous.
- **Build hubris.** The writeup concludes "we should build" because the team wants to build. The capability-ceiling comparison is weak, the maintenance commitment is undercounted, the market scan is cursory. Tell: the year-three internal-build TCO is lower than any vendor's, on the assumption that maintenance is a small line. Remediation: require the write-up to pass a peer review with an engineering lead who will inherit the maintenance; the review usually reveals what was missed.
- **Capability-only scoring.** The matrix compared candidates only on capability fit; TCO, data boundary, switching cost, vendor concentration were weightless. Tell: the winner is the newest, most-hyped tool. Remediation: require weights on non-capability dimensions to sum to at least 40% of total weight for enterprise-scope decisions.

## The matrix output — what gets signed

A build-vs-buy writeup at enterprise scope produces one artifact.

```
Build-vs-Buy Decision — <problem name>

Stage 1 problem statement: <one sentence from mod-102 Chapter 01>
Target task and cohort: <summary from Stage 1>

Candidates considered
  Column 1 (copilot): <specific tool(s), or "not applicable because ...">
  Column 2 (add-on):  <specific add-on(s), or "not applicable because ...">
  Column 3 (industry): <specific tool(s), or "not applicable because ...">
  Column 4 (build):   <build scope, or "not applicable because ...">

Comparison (ten dimensions, weighted)
  Weights: <published, with rationale>
  Scores:  <table across candidates>

TCO (three-year horizon)
  Candidate A: $X.X M, with band
  Candidate B: $X.X M, with band
  ...

Projected ROI (three-year horizon, from Chapter 02 method)
  Candidate A: central Yx, 90% band Z-W
  Candidate B: ...

Recommendation: <candidate, with reasoning>
Disqualifiers acknowledged: <non-winning candidates' failure modes>
Dependencies: <what has to be true for the recommendation to hold>
Decision owner: <sponsor / Stage 3 attendee>
```

Sign-off travels with the artifact. For enterprise-scope decisions this is typically the executive sponsor, Finance, Procurement, Security/Privacy, and the Stage 1 problem owner. The gate review is the Stage 2 gate from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md), extended to carry the four-column depth.

## Where this chapter feeds

- [Chapter 04](04-partnering-with-procurement-finance-and-it.md) carries the contract-term comparison that this chapter's data-boundary and compliance dimensions produce.
- [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) composes: a build-vs-buy decision does not run in isolation; it runs against the stack the organization already has.
- [Chapter 06](06-the-vendor-vetting-rubric.md) operationalizes the vendor-concentration and compliance-posture dimensions into a running rubric.
- Feeds [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md) when Column 4 wins — the commissioning brief is what mod-110 operates on.
- Feeds [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md) when a recurring vendor-management rhythm is implied by the decision.

## Summary

- The build-vs-buy matrix at enterprise scope is a four-column comparison, not a binary — coding/knowledge-work copilots (Column 1), platform add-ons (Column 2), industry-specific tools (Column 3), internal build (Column 4) — each with a distinct cost shape, data posture, and maintenance commitment.
- Compare candidates across ten dimensions (capability fit, TCO, projected ROI, data boundary, residency, compliance, switching cost, vendor concentration, capability ceiling, operating complexity) with published weights.
- TCO shapes differ by column: enablement-front-loaded for Column 1, license-dominant at scale for Column 2, higher per-seat with embedded compliance for Column 3, maintenance-dominant for Column 4.
- Reusable column-wins patterns: Column 2 for commodity workflow value in existing SaaS; Column 1 for frontier capability and cross-tool reach; Column 3 for domain-specific accuracy and compliance; Column 4 only for data-boundary, differentiated workflow, or forced build.
- Three named failure modes: vendor capture, build hubris, capability-only scoring; each has a specific tell and a specific remediation.
- The matrix output is a signed artifact with candidates, weights, scores, TCO, projected ROI, recommendation, and acknowledged disqualifiers — reviewed at the Stage 2 gate from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md).
