# The Vendor Vetting Rubric

> R17 (vendor / external-partner management) sits at 0.23 in the posting signal — below the 0.25 threshold at which it would be a first-class learning objective, but one cycle from clearing the bar. The lightweight rubric here is the role's answer: a running vetting discipline that is proportional to the current evidence, that composes with the contract-term work from [Chapter 04](04-partnering-with-procurement-finance-and-it.md) and the build-vs-buy matrix from [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md), and that is ready to carry heavier weight if the signal strengthens in the next cycle. This is not a procurement-grade vendor assessment; it is the enablement lead's lens on the vendors that become counterparties in the enablement program.

## Why the role needs its own rubric

The organization already has vendor-vetting infrastructure: Procurement runs supplier assessments, Security runs vendor security reviews, Legal runs counter-party checks. The enablement lead's rubric is not a replacement — it is the lens the other reviews do not carry.

- **The vetting question is use-case-shaped, not generic.** A Security assessment asks whether a vendor meets the organization's controls baseline; it does not ask whether the vendor will still exist, deliver, and price fairly across a three-year enablement rollout. The enablement lead's rubric is the one that asks the use-case question.
- **The rubric runs across the portfolio, not per-contract.** Procurement reviews a vendor at contract signing and at renewal. Enablement reviews vendors continuously — every rollout decision, every consolidation case, every pilot that asks whether to commit. The cadence is different.
- **The rubric composes with the build-vs-buy matrix.** The vendor-concentration and capability-ceiling dimensions in [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) are exactly the questions the vetting rubric operationalizes.

The chapter's claim is modest: a one-page rubric, a running cadence, a few failure modes. R17 at 0.23 does not justify a full vendor-management curriculum; the role carries enough to be a credible counterparty and no more.

## The rubric — six dimensions

Each dimension produces a score and a written note. The score is 1-5 where 1 is the strongest concern; the note is what a reviewer cares about. The rubric is deliberately short — a one-page artifact per vendor, filled in at decision time and at renewal.

### Dimension 1 — Capability trajectory

Where is the vendor's capability relative to the task, and where is it going?

- **Current capability.** Does the vendor's tool do the Stage 1 target task at a measured quality bar? Draw from the Stage 2 POC from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md). A score; not a go/no-go.
- **Roadmap credibility.** Has the vendor shipped what they said they would ship over the last two to four quarters? Roadmap-versus-delivery is a durable signal; vendors that ship consistently are a different risk than vendors whose roadmaps are aspirational.
- **Capability ceiling.** Where does the tool plateau? A tool that has reached the frontier of what the task requires is a different risk than a tool that is still in a capability race with alternatives; both can be good investments, but the risk shape is different.

### Dimension 2 — Data and model posture

- **Training-use posture.** Does the vendor train on customer data? Default at enterprise tier should be no. If yes, under what conditions, with what opt-out, and what evidence that the opt-out is honored? This is the first contract term to read ([Chapter 04](04-partnering-with-procurement-finance-and-it.md)).
- **Model provenance.** What underlying models does the vendor use? Are they first-party (vendor-trained), third-party (hosted via API, e.g., OpenAI, Anthropic, Google), or hybrid? What is the sub-processor chain? Opaque provenance is a flag.
- **Data residency and jurisdiction.** Where is customer data stored at rest and processed in transit? Does the vendor operate in the jurisdictions the organization requires? Jurisdictional fit is table stakes in regulated contexts.
- **Retention and deletion.** How long is customer data retained; how is deletion verified at termination? Vendor practices here vary widely; verify, do not assume.

### Dimension 3 — Security and compliance posture

- **SOC 2 Type II.** Present, current, and in scope for the service being bought? (Service-scope mismatches are common — the vendor has SOC 2 Type II on their core platform but not on the AI add-on.)
- **ISO 27001.** Nice-to-have at most tiers; required at some regulated organizations.
- **Industry-specific attestations where applicable.** HIPAA BAA for healthcare, PCI-DSS for payment, FedRAMP level for public-sector, specific sector attestations. Required where the use case touches regulated data.
- **Model-provenance attestations.** Emerging category; not standardized across the industry. Where the vendor has model-origin or supply-chain attestations, record them; where they do not, note the absence without penalizing the absence until the industry standard matures. See [resources](resources.md) for current standards work.
- **Incident response posture.** Does the vendor have a documented incident-response process, a breach-notification SLA, a public incident history? Composes with [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).

### Dimension 4 — Commercial resilience

- **Company stage and funding.** Early-stage (seed/A) vendors with great technology are a different risk than established vendors with 10-year track records. Neither is disqualifying; the enablement lead should know which they are committing to.
- **Customer concentration.** Does the vendor depend on a handful of large customers? A vendor where the organization would be among the first enterprise adopters bears concentration risk in the other direction.
- **Pricing stability.** Is the vendor still iterating on its pricing model? Vendors that have changed pricing structure twice in 18 months will likely change it again; price the renewal uplift accordingly.
- **Acquisition exposure.** Is the vendor a plausible acquisition target? Acquisitions are not inherently bad; they do change the counter-party relationship, the roadmap, and sometimes the data posture. Low-probability events but worth naming.

### Dimension 5 — Operating and admin surface

- **SSO / SCIM maturity.** SAML or OIDC, SCIM provisioning, group-based entitlement. Table stakes for enterprise. Verify in POC, do not take the vendor sales team's word for it.
- **Admin and audit surfaces.** Usage reporting, audit logs, policy configuration, retention controls, DLP integration. Enterprise-grade or not?
- **Support posture.** SLA tiers, dedicated support, response times, escalation paths. Composes with [Chapter 04](04-partnering-with-procurement-finance-and-it.md) commercial-terms work.
- **API and integration surface.** If the organization will integrate the tool into internal systems (and most non-trivial deployments will), the API surface is a load-bearing dimension.

### Dimension 6 — Switching and exit

- **Data portability on exit.** How is customer data returned at termination? Is there a tested export path? A vendor with no documented export path is a vendor the organization cannot reasonably exit.
- **Alternatives in market.** How many viable alternatives exist if the vendor has to be swapped? Three or more is comfortable; one or zero is concentration risk that the organization has to accept explicitly.
- **Transition cost estimate.** From the switching cost in the consolidation economics in [Chapter 05](05-reconciling-the-tool-stack-across-bus.md). Rough order of magnitude — not precise, but recorded so the renewal conversation is grounded.

## The rubric artifact

A one-page artifact per vendor. Example skeleton:

```
Vendor vetting — <vendor name> — <date> — <reviewer>

Context
  Use case: <Stage 1 problem statement summary>
  Current deployment scope: <BU, cohort size, horizon>
  Decision pending: <new rollout / renewal / consolidation case / pilot>

Scores (1-5, 1 = strong concern, 5 = strong confidence)
  1. Capability trajectory: X (note)
  2. Data and model posture: X (note)
  3. Security and compliance: X (note)
  4. Commercial resilience: X (note)
  5. Operating / admin surface: X (note)
  6. Switching / exit: X (note)

Summary
  Overall posture: <one sentence>
  Red flags: <what would trigger a stop>
  Open items: <what is being verified>
  Next review date: <renewal-minus-90 or sooner if signal changes>
```

The rubric is intentionally compact. A rubric that takes four hours per vendor will not be filled in; a rubric that takes thirty minutes will. The compactness is the design.

## When to run the rubric

Four triggers, each tied to a decision moment.

- **Pre-pilot.** Before the Stage 3 commit from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md). The rubric is one of the inputs to the Stage 3 gate.
- **Pre-renewal (renewal-minus-90).** Composes with the Procurement renewal-plus-90 review from [Chapter 04](04-partnering-with-procurement-finance-and-it.md). The rubric refresh is what feeds the renewal negotiation brief.
- **Signal event.** A material event — vendor acquisition, pricing model change, public incident, major sub-processor shift, significant capability release or regression. The rubric is re-run at the material event, not waited on to renewal.
- **Annual portfolio sweep.** Once a year, as part of the stack reconciliation from [Chapter 05](05-reconciling-the-tool-stack-across-bus.md). Every live vendor gets a rubric refresh; vendors that have not been looked at in twelve months are flagged.

## Vendor concentration — the composite view

Individual vendors score on the rubric; the portfolio scores on *concentration*. Three concentration questions the enablement lead reviews quarterly.

- **How many vendors in the portfolio?** A portfolio with three vendors is a different risk than a portfolio with twenty. Both have failure modes; name where the portfolio sits.
- **How much spend on the top one, three, five vendors?** A portfolio where 80% of spend is on one vendor is concentration risk. A portfolio where no vendor exceeds 15% of spend is concentration risk in the other direction — operating complexity may be unsustainable.
- **How many tools are single-sourced (no alternative in market)?** Single-sourced tools are acceptable, in small numbers, with explicit acknowledgment. A portfolio where more than 20% of spend is single-sourced is carrying an unacknowledged concentration risk.

The concentration view is not an optimization target; it is a dashboard the role reads so concentration drift does not surprise anyone.

## Failure modes — three patterns the rubric catches

- **The polished-pitch illusion.** The vendor's sales motion is excellent; the rubric scores are high; the operating experience six months later is poor. Tell: strong Dimension 1 and Dimension 5 scores from pitch material, weak scores from production evidence six months later. Remediation: weight the rubric toward verifiable evidence (POC outputs, SOC 2 reports, API tests, reference-customer conversations) over vendor marketing material; distrust Dimensions 1 and 5 that are supported only by pitch collateral.
- **The security-only review.** The vendor passed Security review and so is deemed vetted. Dimensions 1, 4, and 6 were never scored. Tell: a rubric with only Dimensions 2 and 3 filled in. Remediation: a complete rubric is the artifact; partial rubrics do not pass the enablement lead's sign-off.
- **The stale score.** The rubric was run at pilot-commit and never refreshed. The vendor is now 18 months into operation; the scores reflect 18-month-old evidence. Tell: a rubric date more than 12 months old on a live vendor. Remediation: the annual portfolio sweep, with the signal-event trigger for major changes.

## What the rubric is not

Three things the rubric explicitly does not do.

- **It does not replace Procurement, Security, or Legal review.** Those reviews run on their own cadence with their own depth. The rubric is enablement-lens; the organization carries the other lenses.
- **It does not produce a numerical vendor rank.** The score is a shape, not a ranking. A vendor with 3s across the board and a vendor with 5s and 1s have different risk shapes; averaging them loses the shape.
- **It does not commit to vendor removal on a score threshold.** A low-scoring vendor may still be the right tool in the stack, with explicit acknowledgment of the concerns. The rubric informs the decision; the decision is made with the sponsor, Finance, and Procurement.

## What crossing the R17 threshold would change

At 0.23 this is a lightweight rubric with a running cadence. At 0.30+ in a future cycle, the module would expand into a dedicated vendor-management curriculum — deeper contract-term coverage, formal counter-party relationship management, structured vendor performance scoring, formal exit-planning drills. The chapter is written to carry that expansion gracefully: the rubric's six dimensions map directly onto the depth categories a heavier curriculum would develop.

Until then: run the rubric, refresh on cadence, read concentration quarterly, trust Procurement and Security for the lenses this chapter does not carry.

## Where this chapter feeds

- Composes with [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) — the vendor-concentration and capability-ceiling dimensions there operationalize into this rubric.
- Composes with [Chapter 04](04-partnering-with-procurement-finance-and-it.md) at the renewal-minus-90 interface.
- Composes with [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) in the annual portfolio sweep.
- Feeds [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) when a vendor event produces an incident-adjacent signal.
- Feeds [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md) when vendor management becomes a first-class CoE operating surface.

## Summary

- The rubric is proportional to R17 at 0.23 — a one-page artifact per vendor, six dimensions, filled in at decision time and at renewal.
- Six dimensions: capability trajectory, data and model posture, security and compliance, commercial resilience, operating / admin surface, switching and exit.
- Four triggers: pre-pilot (feeds Stage 3), pre-renewal (feeds Procurement at renewal-minus-90), signal event (vendor acquisition, pricing change, major incident), annual portfolio sweep.
- Portfolio-level concentration view runs quarterly: vendor count, spend concentration on top one / three / five, single-sourced-tool fraction.
- Three named failure modes: polished-pitch illusion, security-only review, stale score; each has a specific tell and remediation.
- The rubric is the enablement-lens only; Procurement, Security, and Legal carry the lenses this rubric does not.
- Written so that R17 strengthening in a future cycle expands the module gracefully — the six dimensions map onto the depth categories a heavier curriculum would develop.
