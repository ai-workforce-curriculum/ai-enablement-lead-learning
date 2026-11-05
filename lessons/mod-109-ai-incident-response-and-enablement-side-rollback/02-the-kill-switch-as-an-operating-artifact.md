# The Kill-Switch as an Operating Artifact

> [mod-102 Chapter 03 artifact 7](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) authored a one-page kill-switch and rollback plan as a launch-gate artifact. Chapter 03 noted that "kill-switch operation — live incident mechanics, forensic hand-off, regulator-notification clock — lives in mod-109. This chapter authors the runbook; mod-109 runs it." This is the running. A kill-switch is not a paper artefact and it is not an engineering control — it is an **operating artifact** owned by a named role, drilled on a cadence, kept current as a standing responsibility. This chapter operationalises it.

## What the mod-102 artefact gave us

The kill-switch runbook from mod-102 names:

- **Who authorises** the pull (a role, not a committee — the authorising role name on the runbook).
- **How access is revoked** (which SSO group is emptied, which license pool is deprovisioned, in what order).
- **What users see mid-rollback** (the message surface and the error state).
- **What communications go out** (to whom, on what channel).
- **What preserved-evidence surface the post-mortem inherits**.

The runbook is signed by the enablement lead, `head-of-ai-governance` (L60), and the IT identity lead. It is pressure-tested by `ai-risk-engineer` (L25) on the revocation sequence.

That artefact is necessary and insufficient. A signed one-pager does not pull a tool cleanly. What makes the runbook load-bearing on the day of an incident is six operating properties that must be true *before* the incident arrives.

## The six operating properties of a live kill-switch

### Property 1 — Authorisation is a role, not a committee

The authorising role must be reachable in minutes, not hours. The role named on the runbook has standing to pull the tool without further sign-off — either by delegation from `head-of-ai-governance` (L60) in advance, or because the role *is* `head-of-ai-governance` (L60). The enablement lead is the operator of the kill-switch, not the authoriser — the role separation prevents the enablement lead from pulling the tool unilaterally and then owning the consequence.

Three common variants, depending on organisational shape:

- **Governance-authored authority.** `head-of-ai-governance` authorises; enablement lead operates; IT identity executes. The most common shape and the default in this track.
- **Split-authority shape.** `head-of-ai-governance` authorises for program-level and policy-triggered pulls; `ai-risk-engineer` (L25) authorises for engineered-root-cause pulls; SOC authorises for security-incident pulls. Common in larger organisations with a mature governance apparatus.
- **Delegated-authority shape.** `head-of-ai-governance` pre-delegates the enablement lead to pull the tool under specific written criteria (for example, "any champion field report tagged `incident-shaped` with a confirmed operator-visible data exposure"), with a notification obligation back to `head-of-ai-governance` within a defined window. Used where governance leadership is not continuously reachable and the enablement lead carries a formal operating authority. The delegation must be in writing in the runbook; a verbal delegation collapses under scrutiny.

The authorisation criteria themselves need to be legible. "Serious incident" is not a criterion; a list of specific signal shapes that trigger a pull is.

### Property 2 — Revocation sequence is drilled, not described

The runbook lists the revocation steps. The enablement lead and IT identity have rehearsed the sequence in a dry-run against the real IdP and the real licence pool at least once before launch, and at least once on a six-month cadence after. The dry-run is a specific drill: IT identity executes the revocation against a test group; the enablement lead observes the user-visible state at each step; the ai-risk-engineer checks that the vendor's sessions terminate as expected; the enablement lead times each step.

The reason the drill is non-optional: the revocation sequence contains order-sensitive steps that are not visible from the runbook. If the SSO group is emptied before the vendor's API-key pool is rotated, users may retain working API access even without SSO. If the licence pool is deprovisioned before SSO is revoked, users may see billing-side error messages that are confusing and worrying. The order matters, and the organisation discovers the order by running it.

### Property 3 — User-visible state is designed, not defaulted

Mid-rollback, users will see something. By default, that something is a vendor error page in the vendor's language, which is almost always wrong for the moment. The runbook specifies the user-visible state as a deliberate design decision.

- **The in-tool message** (if the vendor supports a tenant-level banner or maintenance mode): one sentence saying the tool is paused, directing the user to the help channel for details.
- **The post-SSO-revocation message** (if users attempt to log in after revocation): a short message from the identity provider's side rather than the vendor's. The IT identity team configures this; the enablement lead specifies the message content.
- **The in-channel message** (Slack, Teams, email) that users receive in the first hour: approved in advance as a template; the specific words are chosen in the incident thread with `head-of-ai-governance`.

A rollback that leaves users staring at a vendor 500 error with no organisational context is a rollback that generates a second wave of support traffic and speculation. The design preempts the wave.

### Property 4 — Evidence preservation is sequenced ahead of revocation

A kill-switch pull disrupts the vendor's session state, the organisation's log pipeline, and sometimes the vendor's retention windows for prompts and outputs. The runbook sequences evidence preservation **before** revocation where possible:

- **Vendor audit logs** pulled to the organisation's evidence store in their current state. Many vendors retain prompt-and-output history for a defined window (often 30 days); a retention-window clock may be ticking, and evidence captured before revocation is cleaner than evidence captured after a vendor-side support ticket.
- **Organisational log pipeline** (DLP alerts, SSO sign-in records, egress logs) snapshotted at the moment of the signal.
- **Operator-side evidence** (the full field report, the champion's narrative, the exact prompt and output if available, timestamps, user context, sensitive-data classification) captured in the hand-off packet treated in [Chapter 04](04-the-first-ten-minutes-to-the-first-hour.md).
- **Communication-surface preservation** — the Slack thread, the help-ticket exchange, the email thread — exported before any auto-retention cycle fires.

The ai-risk-engineer (L25) will tell the enablement lead what engineered evidence is needed from the vendor; the SOC will tell the enablement lead what security evidence is needed from the organisation's own stack. The enablement lead's job is to preserve the operator-side surface that only enablement can collect, and to sequence the pull so engineered and security evidence can be collected before the vendor's session is terminated.

For incidents that may qualify as EU AI Act serious incidents (Chapter 07), preservation is not optional and the retention window is not the organisation's choice — it is bounded by the Article 73 reporting obligation. The enablement lead does not run that clock; the runbook's preservation discipline is what keeps the clock runnable.

### Property 5 — Communications go out on prepared channels, not improvised ones

The first-hour communications surface uses channels that already exist and are already carrying the rollout's standing cadence from [mod-105 Chapter 04](../mod-105-champion-networks-and-change-management/04-the-rollout-communications-cadence.md). Three channels, pre-approved:

- **The champion network.** The champions for every affected function are briefed within 30 minutes of the pull. The brief is **what to say, what not to say, where to send questions**. The governance-side owner has approved the content.
- **The help channel.** Tier 1 support for the tool has the approved message and the escalation path for operator questions. Operators who ask "why" are told the enablement team is coordinating an investigation with governance and will send a follow-up on an approved cadence.
- **The exec informational channel.** The exec sponsor named in [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) and [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) is notified informationally — "a signal has crossed into incident territory; `head-of-ai-governance` is leading; here is what the enablement side is doing to support." Not substantive briefing; informational.

The communications surface does not include an external channel. If an external communication is required, `head-of-ai-governance` and general counsel author it; the enablement lead does not.

### Property 6 — The runbook has a standing owner and a standing cadence

The kill-switch artefact has a named standing owner (the enablement lead) and a cadence on which it is reviewed and kept current:

- **Every rollout change.** A new vendor, a new SSO group, a new licence pool, a new business unit onboarded, an approved-tool envelope change — the runbook is reviewed for correctness.
- **Every six months at minimum.** A dry-run and a ladder-freshness review.
- **Every escalation-ladder named role change.** When `head-of-ai-governance` changes, when the IT identity lead changes, when the ai-risk-engineer changes, when the SOC rotates on-call — the ladder updates and the runbook is re-signed.
- **Every confirmed incident.** The incident's close-the-loop ([Chapter 06](06-the-close-the-loop-discipline.md)) revises the runbook where the incident surfaced a weakness.

A runbook that has not been touched in 18 months is a runbook that will fail on the day of the incident. The standing cadence is what keeps the artefact live.

## The two authorisation-criteria shapes

Two legible shapes for the authorising criteria on the runbook. Pick one explicitly.

### Shape A — Named-signal-shapes trigger the pull

A short, enumerated list of signal shapes. If any item on the list is confirmed, the authorising role pulls the tool. Examples:

- Confirmed operator-visible exposure of in-scope regulated data (PHI, PCI, MNPI, student records, privileged legal content).
- Model output causing direct harm to an identifiable person.
- A guardrail bypass that produced a tool answer violating a regulatory prohibition.
- Credential exposure through the tool to an unauthorised party.
- A vendor-side security incident the vendor has notified under the DPA.

The signal-shape list is specific. "A serious incident" is not a shape; "confirmed operator-visible exposure of PHI" is.

The shape works well when the organisation has a mature governance partner who can co-author the list, and when the rollout's risk surface is well understood. It is less adaptive — an incident the list did not anticipate requires the authorising role's judgement, which is slower.

### Shape B — Severity-matrix triggers the pull

A short severity matrix with the authoriser mapped to severity. For example:

| Severity | Enablement authority | Governance authority | SOC authority |
|---|---|---|---|
| S4 — contained to one operator; no data exposure | — | — | — |
| S3 — confirmed small-scope impact (≤10 operators; no regulated data) | Pull with notification to governance within 4 hours | — | — |
| S2 — confirmed material impact or any regulated-data exposure | Recommend pull; governance authorises | Authorises | — |
| S1 — confirmed regulatory-notifiable or external-reaching | Recommend pull; governance authorises; SOC co-signs | Authorises | Co-signs |

The severity matrix is more adaptive but requires that the enablement lead and governance share a severity vocabulary, with worked examples. Severity classification itself is not the enablement lead's call at the moment of the incident — the enablement lead's provisional read goes in; the authoriser decides.

Hybrid shapes exist (a short named-signal list that triggers pre-delegated pulls, plus a severity matrix for everything else), but at the cost of complexity. Choose the simplest shape the organisation can run.

## When a partial kill-switch is appropriate

A full pull is not always the right move. Three partial shapes to have in the runbook:

- **Scope-narrow.** Revoke the tool from a specific function, region, or role while keeping it available to others. Appropriate when the signal is attributable to a specific user population and the broader population is not at risk.
- **Feature-disable.** Turn off a specific feature of the tool (plugins, specific model variants, file uploads, agentic workflows) while keeping the base tool available. Appropriate when the signal attributes to a specific feature and the vendor supports feature-level toggles.
- **Rate-limit or supervisor-mode.** Impose a usage ceiling or require manager approval for continued use. Appropriate when the signal suggests misuse rather than tool failure, and the organisation wants to preserve the tool while investigating.

Each partial shape has its own revocation sequence, user-visible state, and communications. The runbook should name the partial shapes it supports explicitly; an improvised partial pull in the middle of an incident is a source of error.

## The failure modes

Three operating failures that the properties above are meant to prevent.

- **The runbook is right, the ladder is stale.** The enablement lead goes to page `head-of-ai-governance` and discovers that the name on the runbook left the organisation three months ago. The pull is delayed by the time it takes to rediscover authority. **Prevention:** Property 6, standing cadence.
- **The revocation sequence has an undiscovered order dependency.** The enablement lead and IT identity execute the runbook, but the sequence is wrong, and operators retain working access through a side-channel the runbook did not consider. **Prevention:** Property 2, drilled revocation.
- **The pull succeeds and the post-mortem has nothing to work with.** The vendor retained prompts for 14 days; by the time the ai-risk-engineer asks the vendor for the data, the retention window has lapsed. **Prevention:** Property 4, evidence preservation sequenced ahead of revocation.

Each of the three has happened in the AI Incident Database's enablement-side cases or in analogous SaaS-rollout incidents outside AI. [Chapter 03](03-learning-from-the-ai-incident-database-and-oecd-ai.md) treats the precedent surface explicitly.

## Summary

- The kill-switch is not a paper artefact. It is a live operating artifact with six properties that must be true before the incident arrives.
- Property 1 — authorisation is a specific role (or delegated specific role), not a committee.
- Property 2 — the revocation sequence is drilled, not described; at least one dry-run before launch and at least one on a six-month cadence.
- Property 3 — the user-visible state during rollback is designed in advance (in-tool message, post-SSO message, in-channel message).
- Property 4 — evidence preservation is sequenced ahead of revocation; vendor logs, organisational logs, operator-side evidence, communication-surface preservation.
- Property 5 — communications go out on the champion network, help channel, and exec informational channel using pre-approved templates; no external channel.
- Property 6 — the runbook has a standing owner (enablement lead) and a standing cadence (per-change, six-monthly, per-role-change, per-confirmed-incident).
- Two legible authorisation shapes: named-signal-shapes or severity-matrix. Choose one; keep it simple.
- Three partial-pull shapes (scope-narrow, feature-disable, rate-limit/supervisor-mode) available as alternatives to a full pull when the signal attributes support them.
- Three operating failures the properties prevent: stale ladder, undiscovered order dependency, destroyed evidence.
