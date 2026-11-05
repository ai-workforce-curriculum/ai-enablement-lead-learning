# The Data-Handling SOP

> The acceptable-use policy tells operators what the tool is for. The data-handling SOP tells them what to do in the ten minutes after they realize sensitive data was pasted into it by mistake. The first ten minutes decide whether this becomes an operational note or an incident.

## What this SOP is — and is not

The data-handling standard operating procedure is artifact 2 of the rollout artifact set ([mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md)). It is the **operational procedure** for data moving into and out of an AI tool. It sits on top of two things it does not re-author:

- The organization's **data classification scheme** — privacy owns it; the SOP references it.
- The organization's **technical controls** (DLP policies, tenancy settings, logging configuration, output monitoring) — information security owns them; the SOP references them.

The SOP is the operator-facing procedure that makes the scheme and the controls usable in day-to-day work. Its audience is the person at the keyboard, not the auditor and not the architect.

## Why security and privacy are the critical co-authors

For the AUP ([Chapter 04](04-the-one-page-acceptable-use-policy.md)), the heaviest redliners are legal and governance. For the data-handling SOP, the heaviest redliners are **security and privacy** — and the two signatures that are a launch gate are theirs. Legal and governance are read-only collaborators on this artifact; they ratify at the end.

- **Security** owns the technical controls that sit under the SOP. If the SOP says "DLP will flag the data class," security must have actually configured DLP to flag it. The security redline is where a plausible-sounding SOP sentence is caught because the control that would enforce it does not exist yet.
- **Privacy** owns the data-class mapping and the retention statement. If the SOP says "customer PII must not be pasted in," privacy must have agreed what "customer PII" covers in the organization's scheme, what the vendor's retention does with that data, and what the data-subject-rights implications are if a user does paste it in.

Without both signatures, the tool is **not** approved for GA. This is a hard launch gate — not a soft conversation at the governance council.

## The five sections

### 1 — In-scope data classes with examples

Map to the organization's data classification scheme by name. For each class touched by this tool, write two or three **concrete examples** of what is and isn't in it:

- "Customer name in a support transcript" is PII.
- "Product SKU" is not.
- "Draft employment-termination memo" is sensitive personnel data.
- "Published marketing collateral" is not.

The examples are what make the class usable at the keyboard. Operators do not parse a classification taxonomy in a moment of decision; they pattern-match against examples. Pick examples drawn from the real work the cohort does, not from a privacy textbook.

### 2 — Retention

What the vendor keeps, for how long. Whether prompts are used for training. Whether the organization's tenant has retention controls different from the vendor default. Whether abuse-monitoring logs retained by the vendor have a different lifecycle than product telemetry.

**Reference the vendor Data Processing Agreement — do not restate it.** The DPA is the authoritative source; the SOP points at it and surfaces the facts operators need to know. Restating the DPA in the SOP creates two sources of truth and the two drift apart within a quarter.

### 3 — Egress behavior

What leaves the organization's trust boundary when a user prompts the tool. Which jurisdictions the request and response cross. The distinction between model-training egress (the vendor uses the data to improve a model) and abuse-monitoring egress (the vendor retains the data for security review of its own platform). The two are often confused by operators; the SOP is where they are separated in plain language.

Call out any model-provider-of-last-resort fallback. If the primary provider is unavailable and the tool fails over to a different model, the egress behavior may differ. Operators should know.

### 4 — The accident path

The crown-jewel section. What a user does in the first ten minutes after they realize sensitive data was pasted in by mistake. Operator voice. Step by step. Minimum five steps. Must include:

1. **Immediate action the user takes** — and does not take. "Do not delete the prompt" is usually the right line because the deleted prompt still exists in the tool's retention and logs, and deleting it destroys the evidence the organization needs to measure what happened.
2. **Who the user contacts first** — a named role (not a named person) with a channel (Slack group, ticket queue) and an SLA expectation.
3. **What information to preserve** — the exact prompt text, the output, the timestamp, the user's browser or client context. A short list.
4. **What happens next on the enablement side** — the first-line triager's first move, who else gets looped in, when the user gets an update.
5. **Handoff to security operations** — the point at which this stops being an enablement conversation and becomes a SOC-side investigation. The SOC decides retention-forensic questions, notification-clock questions, external-coordination questions. [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) covers the routing discipline; the full incident mechanics live in [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).

The accident path is the section that gets skipped and shouldn't. Most users who paste the wrong thing in know within minutes — their stomach drops. The question is whether the SOP tells them exactly what to do, or whether they Slack a manager who Slacks a director who finds this role on a Friday afternoon. By the time that chain resolves, the window for a clean remediation is gone.

### 5 — Access and revocation touchpoint

A **pointer**, not a re-authoring. The access and offboarding playbook is artifact 3 of the rollout artifact set (operated by IT identity); the SOP references it and names the specific conditions under which SOP-side handling triggers an access-review request (for example, repeated accident-path triggers from one user cohort may indicate a training gap or a revocation need).

## Three accident paths worth naming by shape

Operators and triagers both benefit from recognizing which shape is in front of them. The three shapes most SOPs end up operating against:

- **The paste-mistake path.** The common one. A user pastes a data class that was on the forbidden list. The SOP's accident-path section is primarily for this.
- **The subtly-wrong-output path.** The tool returned an output the user cannot tell is right. This often does not feel like an incident at the moment; it feels like a judgment call. The SOP should name this shape and route it — usually to the champion network for workflow interviews and to [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md)-side prompt-coaching material, occasionally to the risk engineer if the pattern recurs.
- **The tool-malfunction path.** The tool outputs something out of policy on its own — hallucinated personal data, refused to answer a routine request, produced content the organization's brand would not sign off on. This routes to [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) incident handling and to `ai-risk-engineer` (L25) for engineered-risk assessment.

Each shape has a different first-line response. Naming them in the SOP lets the first-line triager pattern-match in seconds instead of minutes.

## Where the SOP ends and SOC-side handling begins

A clean boundary makes the handoff fast under pressure:

- **Enablement side:** the first ten minutes. User-facing accident-path script. First-line triage. Champion-network communication. Pause-rollout decision. Preservation of operator-side evidence.
- **SOC side:** forensic acquisition. Log analysis and model-forensics. Retention-window reconciliation. Regulator-notification-clock management (if a clock has been tripped). External coordination with the vendor and any data subjects. The `ai-risk-engineer` (L25) and the SOC run this workstream; `head-of-ai-governance` (L60) and counsel own the regulator-facing communications.

The enablement lead **convenes, triages, and hands off**. Does not run the forensic workstream. Does not speak to regulators. [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) has the discipline.

## Co-author tags on the SOP

As with the AUP, every section carries a co-author tag. The signing surface is different: privacy signs sections 1 and 2; security signs sections 2 and 3; both sign section 4 (the accident path); IT identity is referenced in section 5. `head-of-ai-governance` ratifies the whole document at the end of the cycle.

## Coupling with the AUP

The AUP and the SOP are a pair, not two separate documents. The AUP names the data classes that the SOP operationalizes; the AUP's "if-in-doubt default" points at the SOP's accident path for the cases where the user has already done the thing. Changes to one almost always require changes to the other within the same redline cycle.

If an AUP revision ships without the matching SOP update, operators learn an updated set of rules and a stale set of procedures in the same week — and they default to whichever is easier.

## Summary

- The data-handling SOP is the operator-facing procedure that sits on top of the data classification scheme (privacy's) and the technical controls (security's). It does not re-author either.
- Security and privacy are the co-authors whose signatures are a launch gate. Legal and governance are read-only ratifiers on this artifact.
- Five sections: in-scope data classes with examples, retention, egress behavior, the accident path, access/revocation touchpoint.
- The accident path has five minimum steps, operator voice, with "do not delete the prompt" named. It is the section that gets skipped and shouldn't.
- Three accident shapes to name: paste-mistake, subtly-wrong-output, tool-malfunction. Each has a different first-line response.
- Enablement handles the first ten minutes; SOC and `ai-risk-engineer` (L25) handle the forensics after. See [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) for the routing-out discipline and [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) for the full incident flow.
- The AUP and the SOP are a pair — co-redline them in the same cycle.
