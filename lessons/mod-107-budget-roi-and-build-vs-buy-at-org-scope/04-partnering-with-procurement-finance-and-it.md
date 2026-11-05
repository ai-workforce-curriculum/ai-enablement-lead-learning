# Partnering with Procurement, Finance, and IT

> [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) built the Finance partnership at scorecard depth. [Chapter 01](01-the-enablement-cost-model-at-org-scope.md) and [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) of this module raised the surface area to budget and build-vs-buy depth; those decisions require a *three-way* partnership — Procurement on contract terms, Finance on budgeting and cost recovery, IT on licensing and identity. This chapter is the operating contract with the three partners and the vocabulary the role needs to be a credible counterparty. Contract execution — the redline cycle, the signature, the counter-party relationship — remains with Procurement and Legal; the enablement lead carries the use-case authority and the technical / data posture inputs.

## Why the three-way partnership exists as its own surface

Three structural reasons.

- **Each partner owns a column the others cannot sign off.** Procurement owns the paper; Finance owns the ledger; IT owns the admin and identity surface. A decision that skips any partner produces a tool that lands but does not operate — the contract that security did not see, the invoice that Finance did not forecast, the admin surface that IT cannot manage.
- **The partners move on different clocks.** Procurement runs on negotiation cycles (weeks). Finance runs on budget cycles (months to quarters). IT runs on release and change-management cycles (continuous). The enablement lead orchestrates across the three clocks so none of them becomes the bottleneck.
- **The partners each read the same vendor through different lenses.** Procurement reads price, terms, and risk allocation. Finance reads budget fit, cost-recovery mechanism, and the invoice stream. IT reads SSO integration, licensing structure, and operational load. The role's job is to carry the full picture so the three lenses compose rather than fight.

The chapter maps each partnership — what the role owns, what the partner owns, what is co-owned — and the vocabulary that makes the role a credible counterparty in each conversation.

## The Procurement partnership

Procurement owns contract execution: redlines, negotiation, signature, counter-party management. The enablement lead carries the use case, the data posture, and the technical requirements that shape the contract terms; the contract itself is Procurement's artifact.

### The contract-term vocabulary the role must carry

The enablement lead reads contracts, does not draft them. Reading requires vocabulary across six surfaces.

- **The DPA (Data Processing Addendum).** The agreement governing how the vendor processes the organization's data. The standard shape is a GDPR-style DPA (relevant whether or not the organization is EU-regulated; GDPR language is now baseline across enterprise contracts). Read for: data categories processed, processing purposes, sub-processors (and their locations), data-breach notification timelines, audit rights, data-return/deletion obligations at termination.
- **AI-specific addenda.** Most enterprise contracts for AI tools now carry an AI addendum on top of the base DPA. Read for: training-use posture (does the vendor use customer prompts/outputs for model training? default answer at enterprise tier should be *no*, and the contract should say so), model-provenance attestations (what models the vendor uses, where they are hosted, under what sub-processor relationships), output-rights allocation (who owns what the model produces), human-in-the-loop obligations where applicable.
- **Security attestations.** SOC 2 Type II is table stakes. ISO 27001 adds breadth. Industry-specific attestations (HIPAA BAA, PCI-DSS, FedRAMP level, specific sector attestations) matter where regulated workflows are in scope. SOC 2 Type I is *not* SOC 2 Type II — Type I is design-only; Type II includes operating-effectiveness evidence over a period. Learn to tell them apart on the vendor's trust page in ten seconds.
- **Data-residency terms.** Where the data is stored at rest and processed in transit, with contractual commitments rather than best-effort claims. For regulated organizations and cross-border data flows, this is the most frequent redline surface.
- **Model provenance and sub-processor flow-down.** Many AI vendors run on sub-processor model providers (OpenAI, Anthropic, Google, AWS Bedrock, Azure OpenAI). The vendor's contract should name the current model sub-processors and flow down the DPA obligations to them. Opaque sub-processor chains are the risk; the contract term is the control.
- **Commercial terms.** License counts, metering definitions, true-up provisions, renewal uplift caps, termination for convenience, usage overage pricing, SLA credits. Each is a Procurement redline target; the role contributes by providing the use-case elasticity (what growth to expect, what metering will cost at scale).

### The standing Procurement partnership

The running contract — four interfaces that keep the partnership alive.

- **Pre-negotiation briefing.** 30-60 minutes per vendor, before Procurement opens negotiation. Enablement lead carries: use case, cohort size and growth, data categories touched, integration surface, required attestations, regulatory jurisdictions. Procurement carries: term precedent from other contracts with this vendor, known negotiation surfaces, redline patterns. Output: a one-page negotiation brief that Procurement runs with.
- **Redline review (as called).** Procurement escalates specific redlines to the enablement lead when the redline touches use-case shape — metering definition, acceptable-use scope, data-category boundary, output-rights allocation. The enablement lead answers in business terms; Procurement writes the clause.
- **Standing vendor review cadence.** Quarterly review of the vendor portfolio with Procurement — upcoming renewals, open redlines, counterparty-health signals, sub-processor changes. Short meeting, large hazard-avoidance value.
- **Renewal-plus-90 review.** Ninety days before renewal, Procurement and enablement open the renewal case — usage trajectory, price trajectory, what the business case has delivered. This is the moment to reopen terms; if it slips, the renewal lands with the vendor's standard uplift and no negotiation window.

### What Procurement owns, what enablement owns, what is co-owned

- **Procurement owns.** The contract text, the redline cycle, the counter-party relationship on commercial terms, the signature, the paper trail.
- **Enablement owns.** The use case, the cohort shape, the data posture, the integration surface, the acceptable-use language that the organization's operators will actually operate under, the connection between the contract and the operating artifacts (policy, rollout plan, enablement plan).
- **Co-owned.** The negotiation brief, the redline priorities on use-case-touching clauses, the renewal case, the vendor review rhythm.

## The Finance partnership

Finance's role in this module extends [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) from the scorecard ROI line to full budget and cost-recovery mechanics.

### Budgeting the enablement program

Four surfaces at this depth.

- **Annual budget construction.** The cost model from [Chapter 01](01-the-enablement-cost-model-at-org-scope.md) is the input. Build the annual budget with Finance as a joint artifact; publish the six families, the sourcing map, and the reconciliation cadence. The annual budget conversation is where materiality thresholds, FTE multipliers, and attribution conventions get resolved for the fiscal year.
- **In-year forecasts.** Variance tracking against plan — Family 1 against invoice schedule, Family 4 against staffing changes, Family 6 against incident-driven costs. The variance pattern is itself diagnostic; a consistent under-spend on Family 3 suggests under-investment in training production, not thrift.
- **Scenario modelling.** Finance partners on scenarios: what the budget looks like under adoption acceleration, under tool-stack consolidation (see [Chapter 05](05-reconciling-the-tool-stack-across-bus.md)), under a build-vs-buy shift ([Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md)). Projections from [Chapter 02](02-projecting-roi-with-confidence-bands.md) feed in.
- **The budget narrative.** The one-page budget narrative that lands in the annual leadership review — what the program will spend, what it is projected to produce, what the confidence band is. Co-authored; neither the enablement lead nor Finance owns the narrative alone.

### Cost recovery — how the money moves across BUs

A tension that shows up in every enterprise enablement program: the CoE funds enablement centrally, but the business units receive the value and (often) operate the licenses. Three recovery models, each with its own tradeoffs.

- **Central funding, no recovery.** The CoE's budget absorbs enablement cost; the BUs do not see a chargeback. Simplest; also the model that produces the most unused seats because the BU does not feel the cost. Appropriate for early-stage programs where adoption is the priority over efficiency.
- **Chargeback by usage.** The CoE funds enablement initially, then charges back to BUs based on active-usage metrics. Aligns incentives — BUs pay for what they use — but creates measurement overhead and can discourage experimentation at the BU level.
- **Shared-services allocation.** The CoE's cost is allocated across BUs through the organization's standard shared-services allocation model (often based on headcount, revenue, or a composite). Middle ground; most common at mature enablement programs.

The choice of recovery model is Finance's call, shaped by the organization's standard shared-services practice. The enablement lead's job is to make the implications visible: a chargeback model requires accurate active-usage reporting; an allocation model does not drive BU-level efficiency; central funding under-prices experimentation but does not price it out.

### The running Finance partnership

Extending the four interfaces from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md):

- **Annual budget cycle.** 4-8 weeks, aligned to the organization's fiscal calendar. The cost model, the projections, the scenario slate, the budget narrative — produced jointly.
- **Standing quarterly ROI review.** From [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md); unchanged.
- **Monthly invoice reconciliation.** From [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md); extended to carry the six-family taxonomy, not just the tool-license line.
- **Ad-hoc for contracts and build-vs-buy.** A new vendor contract or a Column 4 build case triggers a Finance review of the cost projection and the ROI band.
- **Semi-annual attribution working group.** Enablement, Finance, HR/Workforce Planning align on FTE-attribution conventions. Unchanged from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md).

## The IT partnership

IT owns licensing, SSO, identity, operational integration, and the ongoing admin surface of the AI tools. The partnership has three recurring surfaces.

### Licensing

Three structural licensing choices that IT shapes.

- **Centralized vs BU-distributed procurement.** Whether licenses are procured centrally and distributed to BUs, or BUs procure through their own purchasing authority. Centralized procurement enables volume pricing and the consolidation discipline from [Chapter 05](05-reconciling-the-tool-stack-across-bus.md); distributed procurement is faster for BU-specific needs but produces overlapping spend. The choice is often organizational and harder to change than the enablement lead can do alone — surface the tradeoff, let the CIO and CFO decide.
- **Entitlement provisioning.** How users are granted access — entitled roles, group-based provisioning, self-service with manager approval, deliberate assignment by the admin. IT runs this; enablement contributes the cohort shape (Stage 1 problem definition from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md)) and the policy requirements (from [mod-103](../mod-103-policy-co-authoring-with-governance/README.md)).
- **Seat lifecycle.** How unused seats are reclaimed, how leavers are offboarded, how inter-BU transfers are handled. The inactive-seat problem — contracted but unused licenses — lives here; a monthly seat-reclamation cadence with IT is the standard remediation.

### SSO, identity, and admin integration

- **SSO integration.** AI tools without SSO integration are not enterprise-ready. Confirm SSO (SAML 2.0 or OIDC) in the Stage 2 POC from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md); it is a disqualifier for enterprise rollout if missing.
- **SCIM provisioning.** Automated user provisioning and deprovisioning via SCIM. Table stakes for enterprise; some vendors still charge extra for it. Verify before committing.
- **Admin surface fit.** The AI tool's admin surface — audit logs, usage reporting, policy configuration, data-retention controls — must integrate with the organization's existing admin and security tooling. IT reads this surface first.
- **DLP and data-boundary integration.** Data-loss-prevention integration, especially for tools that touch sensitive data categories. Depends on the vendor's admin surface and the organization's DLP stack.

### Operational load

AI tools generate ongoing IT operational load — support tickets (Family 6 in [Chapter 01](01-the-enablement-cost-model-at-org-scope.md)), integration maintenance, identity and access reviews, vendor change management. The IT partnership budgets for this load; the enablement program's cost model carries it.

### The running IT partnership

- **Pre-rollout integration review.** Before Stage 3 commit from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md). Confirm SSO, SCIM, admin surface, DLP integration. Output: a one-page IT-readiness check that attaches to the Stage 3 artifact.
- **Standing monthly licensing reconciliation.** Seat counts, utilization, reclamation targets. Composes with Finance's monthly invoice reconciliation.
- **Quarterly admin review.** Audit logs, usage patterns, policy-violation flags, identity reviews. Composes with the governance review cycle from [mod-103](../mod-103-policy-co-authoring-with-governance/README.md).

## What is out of scope for the enablement lead

The chapter's title promises partnership; the role's authority has limits. Three explicit out-of-scope lines.

- **Contract execution.** Redlines, negotiation, and signature belong to Procurement and Legal. The enablement lead *influences* term selection by carrying the use-case authority, but does not write clauses, does not run redlines, does not sign contracts.
- **Final budget authority.** The CFO and the executive sponsor own the budget decision. The enablement lead builds the case; the decision is made at an altitude above the role.
- **IT operational decisions.** SSO architecture, identity-store configuration, DLP policy configuration, admin-surface integration standards — these are IT's calls. The enablement lead carries the use case's requirements to the conversation and lets IT decide the implementation.

Carrying these boundaries explicitly is what keeps the partnerships functional. A role that steps across them produces artifacts the partners will not sign; a role that stays inside them produces artifacts the partners will co-sign.

## The three-way cadence

A compressed view of the running cadence across the three partners.

```
                        | Weekly | Monthly | Quarterly | Semi-annual | Annual
------------------------+--------+---------+-----------+-------------+--------
Procurement             |        |         |     ✓     |             |   ✓   
  (negotiation briefs)  |        |         |           |             |       
Finance                 |        |    ✓    |     ✓     |      ✓      |   ✓   
IT                      |        |    ✓    |     ✓     |             |   ✓   
```

Weekly: ad-hoc, not scheduled. Monthly: Finance invoice reconciliation, IT licensing reconciliation. Quarterly: Procurement vendor review, Finance ROI review, IT admin review. Semi-annual: Finance FTE-attribution working group. Annual: budget cycle, renewal planning across vendors.

## Where this chapter feeds

- [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) uses the Procurement renewal-plus-90 interface and the IT seat-lifecycle discipline to surface overlapping spend.
- [Chapter 06](06-the-vendor-vetting-rubric.md) uses the contract-term and attestation vocabulary to produce the running vendor-vetting rubric.
- Composes with [mod-103](../mod-103-policy-co-authoring-with-governance/README.md) on policy / AUP / DPA alignment.
- Composes with [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md) at steady state.

## Summary

- The three-way partnership — Procurement, Finance, IT — exists because each partner owns a column the others cannot sign off, moves on a different clock, and reads the vendor through a different lens.
- Procurement partnership: six contract-term surfaces (DPA, AI addenda, security attestations, data residency, model provenance / sub-processor flow-down, commercial terms); four interfaces (pre-negotiation brief, redline review as called, quarterly vendor review, renewal-plus-90).
- Finance partnership: annual budget construction, in-year forecast, scenario modelling, cost-recovery model (central / chargeback / shared-services allocation), extended from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md).
- IT partnership: licensing (centralized vs BU-distributed, entitlement, seat lifecycle), SSO / SCIM / admin surface, DLP integration, operational load.
- Explicit out-of-scope lines: contract execution, final budget authority, IT operational decisions — the enablement lead influences but does not own these.
- A compressed three-way cadence across weekly / monthly / quarterly / semi-annual / annual rhythms keeps the partnerships operating without becoming a governance program of their own.
