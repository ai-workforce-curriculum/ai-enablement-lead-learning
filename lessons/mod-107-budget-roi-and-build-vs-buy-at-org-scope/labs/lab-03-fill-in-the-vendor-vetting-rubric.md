# Lab 03 — Fill in the One-Page Vendor-Vetting Rubric for One Specific Vendor

**Duration:** 45–60 minutes
**Format:** guided hands-on — rubric scoring across six dimensions + concentration check + failure-mode red-team
**Grounding chapters:** [06 — The Vendor Vetting Rubric](../06-the-vendor-vetting-rubric.md), [03 — The Build-vs-Buy Matrix at Enterprise Scope](../03-the-build-vs-buy-matrix-at-enterprise-scope.md), [04 — Partnering with Procurement, Finance, and IT](../04-partnering-with-procurement-finance-and-it.md)

## Objective

Fill in the **one-page vendor-vetting rubric** from [Chapter 06](../06-the-vendor-vetting-rubric.md) for one specific vendor your organization is about to pilot, renew, or consolidate with. The rubric scores six dimensions (capability trajectory, data and model posture, security and compliance, commercial resilience, operating and admin surface, switching and exit), produces a summary posture, and routes into a portfolio-level concentration check. By the end of the lab, the vendor has a dated rubric that will travel with it to its next decision moment and will refresh on the four Chapter 06 triggers (pre-pilot, pre-renewal, signal event, annual portfolio sweep).

## Prerequisites

- [Chapter 06](../06-the-vendor-vetting-rubric.md) read, with the six dimensions, the four triggers, the three failure modes, and the portfolio-level concentration view close enough to cite without the chapter open.
- [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md) read; the vendor-concentration and capability-ceiling dimensions in the build-vs-buy matrix operationalize into this rubric.
- [Chapter 04](../04-partnering-with-procurement-finance-and-it.md) read; the contract-term vocabulary (DPA, AI addenda, SOC 2 Type I vs II, data residency, model provenance / sub-processor flow-down) is what Dimensions 2 and 3 of the rubric score against.
- One specific vendor. Current-market examples that work well for the lab: GitHub Copilot, Cursor, Claude Code, Microsoft Copilot (M365), Google Gemini for Workspace, Zoom AI Companion, Glean, Harvey, Nuance DAX, Ada, Gong, ChatGPT Enterprise. Pick a vendor your chosen organization (from [Exercise 03](../exercises/exercise-03-org-scope-build-vs-buy-matrix.md) or [Exercise 05](../exercises/exercise-05-tool-stack-consolidation-worked-example.md), if applicable) is realistically deciding about.
- A blank working file — `vendor-rubric-<slug>.md`.

## Why a lab, not an exercise

Chapters 01 through 05 each anchor an exercise ([Exercise 01](../exercises/exercise-01-enablement-cost-model-drill.md) through [Exercise 05](../exercises/exercise-05-tool-stack-consolidation-worked-example.md)). [Chapter 06](../06-the-vendor-vetting-rubric.md) has no exercise, in keeping with R17 at 0.23 — the module carries just enough vendor-vetting discipline to make the role a credible counterparty and no more. In practice, the rubric is a *running* artifact: a one-page document per vendor, filled in at decision time, refreshed at the four triggers. The first time the rubric gets filled in is where it stops being a chapter and starts being an operating instrument. This lab is that first fill-in. The rubric you produce here lands into [Exercise 03](../exercises/exercise-03-org-scope-build-vs-buy-matrix.md)'s vendor-concentration dimension, [Exercise 05](../exercises/exercise-05-tool-stack-consolidation-worked-example.md)'s vendor-concentration check, and [Exercise 04](../exercises/exercise-04-procurement-and-finance-partnership-contract.md)'s renewal-plus-90 interface — the rubric is the shape of the information that flows through those downstream artifacts.

## Setup

Open `vendor-rubric-<slug>.md` and paste the Chapter 06 skeleton:

```markdown
# Vendor Vetting — <vendor-name> — <YYYY-MM-DD> — <reviewer>

## Context

- **Use case:** <Stage 1 problem statement summary>
- **Current deployment scope:** <BU, cohort size, horizon>
- **Decision pending:** <new rollout / renewal / consolidation case / pilot>
- **Trigger:** <which of the four triggers fired — pre-pilot / pre-renewal / signal event / annual sweep>

## Scores (1–5, 1 = strong concern, 5 = strong confidence)

### 1. Capability trajectory — <score>
<note>

### 2. Data and model posture — <score>
<note>

### 3. Security and compliance — <score>
<note>

### 4. Commercial resilience — <score>
<note>

### 5. Operating / admin surface — <score>
<note>

### 6. Switching and exit — <score>
<note>

## Summary

- **Overall posture:** <one sentence>
- **Red flags:** <what would trigger a stop>
- **Open items:** <what is being verified>
- **Next review date:** <renewal-minus-90 or sooner if signal changes>

## Portfolio concentration note

<one short paragraph on how this vendor sits in the portfolio-level concentration view>
```

---

## Step 1 — Fill in the Context block (5 min)

Chapter 06's rubric is *decision-shaped* — the scores change depending on what decision is pending. Write the Context block first so the rest of the rubric is grounded.

- **Use case.** Quote the Stage 1 problem statement from [mod-102 Chapter 01](../../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) in one sentence, workflow-first, not tool-first. "Software engineers producing pull-request-sized code changes across the Platform Engineering group" is a use case; "deploying an AI coding tool" is not.
- **Current deployment scope.** If the vendor is already live, name the BU(s), cohort size, and the horizon the current deployment has been running for. If this is a pre-pilot rubric, state "not yet deployed" and name the candidate scope.
- **Decision pending.** One of: new rollout, renewal, consolidation case, pilot. Each shifts the rubric's weight (a renewal is weighted toward Dimensions 4 and 5; a consolidation case is weighted toward Dimensions 1, 4, and 6; a pre-pilot is weighted toward Dimensions 1 and 2).
- **Trigger.** One of the four Chapter 06 triggers: pre-pilot, pre-renewal (renewal-minus-90), signal event, annual portfolio sweep. If a signal event triggered the review, name the event (acquisition, pricing change, public incident, sub-processor shift, significant capability release or regression).

### Checkpoint 1 — before Step 2

- [ ] Use case is written workflow-first.
- [ ] Decision pending is named as one of the four types.
- [ ] Trigger is named as one of the four Chapter 06 triggers; if a signal event, the specific event is named.

---

## Step 2 — Score Dimensions 1 and 2 — capability trajectory, data and model posture (10 min)

### Dimension 1 — Capability trajectory

Three sub-questions from Chapter 06. Write a short note that answers each; set a 1-5 score.

- **Current capability.** Does the vendor's tool do the Stage 1 target task at a measured quality bar? Draw from the Stage 2 POC from [mod-102 Chapter 01](../../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md). Score the fit, not the vendor's brand.
- **Roadmap credibility.** Has the vendor shipped what they said they would ship over the last two to four quarters? Roadmap-versus-delivery is a durable signal. If you cannot answer this, mark the sub-question as an open item and route it to the standing vendor review ([Chapter 04](../04-partnering-with-procurement-finance-and-it.md)).
- **Capability ceiling.** Where does the tool plateau? A tool at the frontier of the task carries a different risk than one in a capability race with alternatives; score the risk shape, not the absolute capability.

Chapter 06's warning on this dimension: distrust scores supported only by pitch collateral. The polished-pitch illusion lives here; weight verifiable evidence (POC outputs, reference-customer conversations) over marketing material.

### Dimension 2 — Data and model posture

Four sub-questions, each a specific contract-term read against the vendor's current contract or published trust page.

- **Training-use posture.** Does the vendor train on customer data? Default at enterprise tier should be **no**. If yes: under what conditions, with what opt-out, with what evidence the opt-out is honored? ([Chapter 04](../04-partnering-with-procurement-finance-and-it.md) names this as the first contract term to read.)
- **Model provenance.** What underlying models does the vendor use? First-party (vendor-trained), third-party (OpenAI, Anthropic, Google, Bedrock, Azure OpenAI), or hybrid? What is the sub-processor chain? Opaque provenance is a flag.
- **Data residency and jurisdiction.** Where is customer data stored at rest and processed in transit? Does the vendor operate in the jurisdictions your organization requires?
- **Retention and deletion.** How long is customer data retained; how is deletion verified at termination? Vendor practices vary widely; verify, do not assume.

Score Dimensions 1 and 2 with scores and 2-3 sentence notes each. Anywhere you cannot answer a sub-question from available evidence, name the sub-question as an **open item** in the Summary block — do not score around a gap.

### Checkpoint 2 — before Step 3

- [ ] Dimension 1 and Dimension 2 each have a score and a 2-3 sentence note.
- [ ] Every sub-question that could not be answered is listed in Open items.
- [ ] Dimension 2's training-use posture is scored against evidence (contract language, trust page citation), not against vendor sales statements alone.

---

## Step 3 — Score Dimension 3 — security and compliance (10 min)

Five sub-questions. Each is a specific attestation or posture check.

- **SOC 2 Type II.** Present, current, and *in scope for the service being bought*? Chapter 06 warns that service-scope mismatches are common — the vendor has SOC 2 Type II on their core platform but not on the AI add-on. Check the report's scope paragraph, not just the attestation badge. ([Chapter 04](../04-partnering-with-procurement-finance-and-it.md) is direct: SOC 2 Type I is design-only; Type II includes operating-effectiveness evidence over a period — they are not equivalent.)
- **ISO 27001.** Nice-to-have at most tiers; required at some regulated organizations. Note presence or absence.
- **Industry-specific attestations where applicable.** HIPAA BAA for healthcare, PCI-DSS for payment, FedRAMP level for public-sector, specific sector attestations. Score against your use case's regulated-workflow surface, not generically.
- **Model-provenance attestations.** Emerging category, not standardized across the industry. Record where present; note the absence without penalizing until the industry standard matures. See [`resources.md`](../resources.md) for current standards work.
- **Incident-response posture.** Does the vendor have a documented incident-response process, a breach-notification SLA, a public incident history? This composes with [mod-109](../../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).

A score note for Dimension 3 should name the specific attestations present, the specific attestations missing where applicable, and the specific scope mismatches you noticed. "SOC 2 Type II present, dated 2026-04, scope covers the core platform but explicitly excludes the Copilot add-on — gap routed to Security for review" is a defensible note; "SOC 2 certified" is not.

### Checkpoint 3 — before Step 4

- [ ] Dimension 3 has a score and a note that names specific attestations present and missing.
- [ ] Any service-scope mismatch between the attestation and the service being bought is flagged in the note and in Open items.
- [ ] Where no model-provenance attestation exists, the absence is noted but not penalized in the score.

---

## Step 4 — Score Dimensions 4, 5, 6 — commercial resilience, operating surface, switching (10 min)

### Dimension 4 — Commercial resilience

Four sub-questions.

- **Company stage and funding.** Early-stage (seed/A) vs established. Not disqualifying either way; know which you are committing to.
- **Customer concentration.** Does the vendor depend on a handful of large customers? Is your organization among the first enterprise adopters?
- **Pricing stability.** Has the vendor changed its pricing model in the last 18 months? Vendors that change pricing twice in 18 months will likely change it again — price the renewal uplift accordingly.
- **Acquisition exposure.** Is the vendor a plausible acquisition target? Low-probability but worth naming — acquisitions change the counterparty relationship, the roadmap, and sometimes the data posture.

### Dimension 5 — Operating / admin surface

Four sub-questions.

- **SSO / SCIM maturity.** SAML or OIDC, SCIM provisioning, group-based entitlement. Table stakes. Verify in POC — do not take the vendor sales team's word for it. ([Chapter 04](../04-partnering-with-procurement-finance-and-it.md) is direct: "AI tools without SSO integration are not enterprise-ready.")
- **Admin and audit surfaces.** Usage reporting, audit logs, policy configuration, retention controls, DLP integration. Enterprise-grade or not?
- **Support posture.** SLA tiers, dedicated support, response times, escalation paths.
- **API and integration surface.** If the organization will integrate the tool into internal systems, the API surface is load-bearing.

### Dimension 6 — Switching and exit

Three sub-questions.

- **Data portability on exit.** Is there a tested export path? A vendor with no documented export path is a vendor the organization cannot reasonably exit.
- **Alternatives in market.** Three or more viable alternatives is comfortable; one or zero is concentration risk the organization has to accept explicitly.
- **Transition cost estimate.** From the switching-cost model in [Chapter 05](../05-reconciling-the-tool-stack-across-bus.md)'s consolidation economics. Order-of-magnitude is fine; the point is that the renewal conversation is grounded.

Score each dimension with a 1-5 and a 2-3 sentence note.

### Checkpoint 4 — before Step 5

- [ ] Dimensions 4, 5, 6 each have a score and a 2-3 sentence note.
- [ ] Dimension 5's SSO / SCIM claim is based on POC evidence or an explicit "verified / pending verification" flag — not vendor-sales attestation alone.
- [ ] Dimension 6's data-portability finding names either a tested export path or the absence of one.

---

## Step 5 — Fill in Summary and Portfolio concentration (10 min)

### Summary block

- **Overall posture.** One sentence that lets a reader read the shape of the vendor without reading the six scores. Chapter 06's rule: "the score is a shape, not a ranking. A vendor with 3s across the board and a vendor with 5s and 1s have different risk shapes; averaging them loses the shape." Write the posture sentence to convey the shape — "Strong on capability (Dim 1), strong on operating surface (Dim 5), weak on commercial resilience (Dim 4, early-stage vendor), unverified on service-scope of SOC 2 Type II (Dim 3)."
- **Red flags.** What would trigger a stop. Specific — "If the Series B does not close by Q2, the commercial-resilience concern escalates to a go/no-go" — not generic ("vendor health concerns").
- **Open items.** Everything you could not resolve from available evidence. Each item has a named owner on the resolution side (Procurement, Security, IT, or the enablement lead).
- **Next review date.** Chapter 06's rule: renewal-minus-90 or sooner if a signal changes. State the specific date, not "in six months."

### Portfolio concentration note

One short paragraph running the vendor through Chapter 06's three concentration questions:

- Where does this vendor sit in the portfolio by spend share (top one, top three, top five)?
- Does this vendor's presence make a tool category single-sourced, or does it add diversity?
- Does the vendor's direction (growth, consolidation, acquisition exposure) shift the concentration view meaningfully in the next 12 months?

Chapter 06's framing is that the concentration view is a dashboard, not an optimization target — the paragraph names what the view sees for this vendor and flags any drift that would move the composite portfolio toward or away from the Chapter 06 rough thresholds (top-one > 80% is concentration risk; single-sourced > 20% of spend is concentration risk).

### Checkpoint 5 — before Step 6

- [ ] The overall-posture sentence conveys the shape of the six scores, not an average.
- [ ] Red flags are specific and name the trigger conditions, not generic concerns.
- [ ] Every open item has a named resolution owner.
- [ ] The next review date is a specific date aligned to a Chapter 06 trigger (renewal-minus-90, annual portfolio sweep, or a named signal-event horizon).
- [ ] The portfolio concentration paragraph names the vendor's current position and the concentration drift in the next 12 months.

---

## Step 6 — Red-team against the three Chapter 06 failure modes (5 min)

Read the rubric aloud and check against three failure patterns.

1. **The polished-pitch illusion.** Are Dimensions 1 and 5 scored high based on vendor pitch material alone? Tell: the strongest scores are on dimensions where the only evidence is sales collateral. Fix: either re-score with production evidence (POC outputs, SOC 2 reports, API tests, reference-customer conversations) or mark Dimensions 1 and 5 as "pending verification" open items.
2. **The security-only review.** Are Dimensions 1, 4, and 6 scored, or only 2 and 3? A rubric with only Dimensions 2 and 3 filled in is Chapter 06's named failure. Fix: complete the rubric — partial rubrics do not pass the enablement lead's sign-off.
3. **The stale score.** Is the date at the top of the rubric current? Will the next review date (set in Step 5) actually be honoured? Set a calendar reminder for the next review date before closing the lab; a stale rubric is a rubric with no refresh cadence.

For any failure present, revise before shipping.

### Checkpoint 6 — self-evaluation

- [ ] None of the three failure modes survived the red-team pass.
- [ ] The rubric fits on one page.
- [ ] A reviewer (Procurement, Security, or the executive sponsor) could read the rubric alone and understand the shape of the vendor — the overall posture sentence carries the shape, the scores carry the detail, the open items carry what is still being verified.
- [ ] The next review date is on a calendar — the lab does not end with the file but with the reminder set.

---

## Deliverables

- `vendor-rubric-<slug>.md` — the one-page vendor-vetting rubric for one specific vendor, with scores across six dimensions, a shape-conveying summary, specific red flags, named open items, a scheduled next review date, and a portfolio concentration paragraph.

## Checkpoint — self-evaluation

- [ ] The rubric fits on one page.
- [ ] All six dimensions have a score (1-5) and a 2-3 sentence note.
- [ ] The overall-posture sentence conveys the *shape* of the scores; no averaging.
- [ ] Every sub-question that could not be answered is listed as an open item with a named resolution owner.
- [ ] The next review date is scheduled on a calendar and aligned to one of the four Chapter 06 triggers.
- [ ] The portfolio concentration paragraph places this vendor in the composite view.
- [ ] None of Chapter 06's three failure modes (polished-pitch illusion, security-only review, stale score) survived the red-team pass.

## What this lab prepares you for

Exercise 03's build-vs-buy matrix scores vendor concentration and capability ceiling as two of its ten dimensions — this rubric is the source of those scores. Exercise 05's consolidation case runs a vendor-concentration check that reads the rubric portfolio-paragraph. Exercise 04's three-way partnership contract names the renewal-minus-90 interface; the rubric refresh at that trigger is the artifact the interface produces. More broadly, the rubric is the first-class output of the role's R17 (vendor / external-partner management, 0.23) posture — the role carries enough vendor-vetting discipline to be a credible counterparty to Procurement and Security, and the rubric is the one-page artifact that makes that discipline running rather than aspirational. If R17 strengthens in a future cycle, Chapter 06's six dimensions map directly onto the depth categories a heavier curriculum would expand into; the rubric you filled in today is the shape of what the role would own at larger scale.
