# Exercise 02 — Data-Handling SOP for an AI Tool

**Estimated effort:** 3 hours
**Format:** 2–3 page operating procedure, Markdown
**Grounding chapters:** [01 — The Co-Author Posture and the Redline Log](../01-the-co-author-posture-and-the-redline-log.md), [05 — The Data-Handling SOP](../05-the-data-handling-sop.md), [07 — What You Route Out](../07-what-you-route-out-counsel-soc-architect.md)

## Objective

Draft the enablement-side data-handling SOP for the same tool and organization you used in Exercise 01. The SOP must be operator-voice, must pair cleanly with the AUP from Exercise 01, and must give **security and privacy** the specific redline surface they need to sign — their signatures are the launch gate on this artifact.

## Prerequisites

- Chapters 01, 05, and 07 read.
- Exercise 01 completed — you will reference the AUP's data classes and escalation path from that draft. If you did not do Exercise 01, pick one of the three organization archetypes from that exercise and sketch a one-paragraph AUP-reading before you start this one.

## Problem statement

Your tool is six weeks from launch. The AUP from Exercise 01 is in the walking-redline cycle. The data-handling SOP is artifact 2 of the rollout artifact set ([mod-102 Chapter 03](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md)) and without security and privacy signatures the tool is not approved for GA — this is a hard launch gate.

You are in a Thursday walking-redline slot with security and privacy. The CISO delegate has 30 minutes. The DPO has 30 minutes after. You need a draft they can land redlines on, not one they have to rewrite.

Legal and governance are read-only collaborators on this artifact in this cycle; they ratify at the end.

## Requirements

Deliver a 2–3 page data-handling SOP with these five sections, in this order:

1. **In-scope data classes with examples.** Map to the data classification scheme named in Exercise 01's AUP. For each class touched by this tool, write **two or three concrete examples** of what is and isn't in it, drawn from the real work the cohort does (not from a privacy textbook).
2. **Retention.** What the vendor keeps, for how long. Whether prompts are used for training. Whether your tenant has retention controls different from vendor default. Whether abuse-monitoring logs have a different lifecycle than product telemetry. **Reference the vendor DPA — do not restate it.** If you do not know the vendor's terms, mark `<!-- needs-research: ... -->` with the specific DPA clause slot you would populate.
3. **Egress behavior.** What leaves the organization's trust boundary. Which jurisdictions the request and response cross. The distinction between model-training egress and abuse-monitoring egress. Any fallback-model behavior if the primary model is unavailable.
4. **The accident path.** The crown-jewel section. Operator-voice. Step by step. **Minimum 5 steps.** Must include:
   - The immediate action the user takes **and does not take** (name "do not delete the prompt" or your defensible alternative, with reason).
   - Who the user contacts first — a named role with a channel and an SLA expectation.
   - The exact information to preserve (prompt text, output, timestamp, user context, anything else).
   - What happens next on the enablement side — the first-line triager's first move, who else gets looped in, when the user gets an update.
   - The handoff to security operations — the point at which this stops being an enablement conversation. Route to the SOC and `ai-risk-engineer` (L25) per [Chapter 07](../07-what-you-route-out-counsel-soc-architect.md); full incident mechanics live in [mod-109](../../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).
5. **Access and revocation touchpoint.** A **pointer** (not a re-authoring) to the access & offboarding playbook (artifact 3 of the rollout artifact set, operated by IT identity). Name the conditions under which SOP-side handling would trigger an access-review request (for example, repeated accident-path triggers from one user cohort indicating a training gap or a revocation need).

Every section carries a **co-author tag** naming: drafter (this role), redliner, security signer (CISO or delegate), privacy signer (DPO). Privacy signs sections 1 and 2 primarily; security signs sections 2 and 3 primarily; both sign section 4; IT identity is referenced (not a signer) in section 5. `head-of-ai-governance` is the end-of-cycle ratifier.

## Starter guidance

- Chapter 05 describes the five sections in depth. Spend your three hours on the accident path — it is the section that gets skipped and shouldn't, and the section the CISO delegate and DPO will spend the most redline minutes on.
- **The accident path is the make-or-break section.** Write it in operator voice. The person at the keyboard whose stomach just dropped needs to know, in seconds, what their next three clicks are. Abstract procedural language fails here; concrete step-by-step with named channels succeeds.
- "Do not delete the prompt" is usually the correct line because the deleted prompt still exists in the tool's retention and logs, and deletion destroys the evidence the organization needs. If you write a different first instruction, defend it in a redline-log entry.
- The **data classification scheme name must match the AUP** from Exercise 01. If the AUP proposed a minimum scheme, this SOP references the same proposed scheme.
- Retention must distinguish **vendor retention** (what the SaaS provider keeps) from **internal retention** (what your organization's logs capture). The two are almost always on different clocks and the SOP must make that visible.
- The egress section often falls over on the model-training vs. abuse-monitoring distinction. Draft each as a separate sentence; let privacy and security redline each independently.
- Where you do not know an organization-specific fact (the SOC's channel, the SLA, the specific jurisdictions the request crosses, the vendor's abuse-monitoring retention), mark `<!-- needs-research: ... -->` with enough specificity that a partner can close the gap. Do not invent.
- **Name the three accident shapes** from Chapter 05 — paste-mistake, subtly-wrong-output, tool-malfunction — somewhere in the SOP (section 4 is the right place). Each needs a different first-line response and naming them in the SOP lets the first-line triager pattern-match in seconds.

## Deliverables

- `data-handling-sop.md`: 2–3 pages, five sections in the required order, co-author tags per section, accident-path section with at least five numbered operator-voice steps.

## Acceptance criteria

- Fits in 2–3 pages at normal body-text size.
- All five sections present, in the required order.
- Data classes map to the named scheme from Exercise 01; at least two or three concrete examples per class.
- Retention section distinguishes vendor and internal retention and references (does not restate) the vendor DPA.
- Egress section separates model-training egress from abuse-monitoring egress.
- Accident-path section has at least five numbered operator-voice steps, includes a "do not" instruction with reason, names the role-level contact, lists the specific information to preserve, and names the handoff to security operations.
- Section 4 names the three accident shapes (paste-mistake, subtly-wrong-output, tool-malfunction).
- Section 5 is a pointer — not a re-authoring — to the access & offboarding playbook.
- Co-author tags per section; security and privacy are explicit signers on the sections they own; `head-of-ai-governance` named as end-of-cycle ratifier.
- No SOC-side forensic language (no log analysis, no notification-clock management, no vendor forensics) — those are routed out per Chapter 07.
- `<!-- needs-research: ... -->` used wherever organization-specific facts are missing. No invention.

## Stretch goals

- Write a one-paragraph **precedence rule** for cases where the SOP and the AUP appear to conflict. (For example: "When the AUP's approved-use list permits a use that the SOP's data-class table forbids, the SOP controls.") Pick a direction deliberately.
- Draft the **3-sentence Slack message** the first-line triager sends when the accident path fires — confirming receipt, naming the next step, giving the user an ETA for follow-up.
- Draft the **retention-table template** as a Markdown table with the slots counsel and privacy will populate (data class, vendor retention, internal retention, deletion trigger, DPA clause reference, needs-research marks on the slots you do not know).
- Sketch the **enablement-side evidence pack** (Chapter 07) that gets handed to the SOC when the accident path hits handoff — what artifacts, in what format, within what SLA.

## Why this exercise matters

The data-handling SOP is the artifact most responsible for whether a data-class accident becomes an operational note or an incident. Security and privacy will sign only a draft they can defend; counsel and governance will ratify only a document that gives counsel legal hooks and governance an evidence surface. Writing the SOP as a paired artifact with the AUP (not as a standalone document) is the move that makes the two sides of co-authoring actually meet — and that makes [mod-109](../../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) feasible when an incident does land.
