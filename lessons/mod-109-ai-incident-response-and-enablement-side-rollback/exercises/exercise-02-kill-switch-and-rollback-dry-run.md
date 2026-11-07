# Exercise 02 — Kill-Switch and Rollback Dry Run

**Estimated effort:** 2.5 hours
**Format:** runbook + user-visible state plan + dry-run script + evidence-preservation sequence, Markdown
**Grounding chapters:** [02 — The Kill-Switch as an Operating Artifact](../02-the-kill-switch-as-an-operating-artifact.md); [04 — The First Ten Minutes to the First Hour](../04-the-first-ten-minutes-to-the-first-hour.md). Prior reading: [mod-102 Chapter 03 Artifact 7](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md).

## Objective

Operationalise the mod-102 Artifact 7 kill-switch and rollback plan for the rollout you chose in Exercise 01. Turn the one-page runbook into a live operating artifact — authorisation criteria written legibly, revocation sequence specified and ready to drill, user-visible state designed, evidence preservation sequenced ahead of revocation, communications templated against the three internal channels, and the standing-cadence obligations named. Produce a dry-run script that IT identity and the ai-risk-engineer can execute together to pressure-test the runbook before the next GA cohort opens.

## Prerequisites

- Chapters 02 and 04 read.
- [mod-102 Chapter 03 Artifact 7](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) read.
- Exercise 01 complete; carry the same rollout and the gap memo from Exercise 01's stretch goal (if you wrote it) into this drill.
- Access to (or plausible reconstruction of) the rollout's SSO identity provider, licence pool, DLP pipeline, and vendor admin console. Where you do not have access, flag the gap inline with a `needs-research` marker and reason about the plausible shape.

## Problem statement

Your rollout is approaching its next GA expansion cohort. Your head of AI governance has asked to see the kill-switch runbook as a live operating artefact — not the one-page launch gate from mod-102, but the version that would be executed in the first fifteen minutes of a confirmed incident. The IT identity lead has agreed to run a dry-run with the ai-risk-engineer and you in the next two weeks. Produce the deliverables below at the depth where the three of you can execute the dry-run against a test group and where the governance co-sign would read as a defensible operating control.

## Requirements

### Part A — The operating runbook

Expand the mod-102 one-page launch-gate runbook into an operating runbook with the following sections. Keep each section tight; the runbook is still read under pressure.

1. **Authorising role and authorisation criteria.** Name the authorising role (the role, not a person). Pick one of the two legible shapes from Chapter 02 (named-signal-shapes OR severity-matrix) and write it out at specificity. If the organisation uses a delegated-authority shape, write the delegation in the form the governance side would sign.
2. **Revocation sequence.** The order-sensitive steps for revoking access. Name:
   - Which SSO group(s) are emptied, in what order, by what system call or admin action.
   - Which licence pool or seat pool is deprovisioned.
   - Which vendor-side admin-console action is taken (if any).
   - Which API-key pool or integration token is rotated (if the tool has an API surface).
   - Which organisational system feeds depend on the tool and must be paused.
   - The order dependencies among the above.
3. **User-visible state.** Three specific messages:
   - **In-tool message** (if the vendor supports a tenant banner or maintenance mode).
   - **Post-SSO-revocation message** from the identity provider's side.
   - **In-channel message** (Slack/Teams/email) for the operator population in the first hour.
   Each message is written in full; the governance side approves the words before incident.
4. **Evidence preservation sequence.** The specific list of what gets preserved before revocation, with ownership:
   - Vendor audit logs pulled to the evidence store (named location).
   - Organisational log pipeline snapshot (DLP, SSO, egress) — named systems and who executes.
   - Operator-side evidence capture (the exact prompt/output, the field report, timestamps).
   - Communication-surface preservation (Slack threads, help tickets, email threads).
   - Who confirms the preservation step is complete before revocation proceeds.
5. **Communications template.** The three internal channels — champion network, help channel, exec informational — each with a pre-approved template message for the first hour. Templates are blanks the governance-side owner fills in during the incident.
6. **Partial-pull shapes.** The specific partial shapes the runbook supports (scope-narrow, feature-disable, rate-limit/supervisor-mode) with each shape's own revocation sequence and user-visible state.
7. **Standing-cadence obligations.** The specific review cadence for the runbook:
   - Per-rollout-change review trigger.
   - Six-monthly dry-run calendar entry.
   - Named-role-change trigger (what changes in the ladder; who re-signs).
   - Per-confirmed-incident revision trigger.

### Part B — The user-visible state plan

A one-page plan that tells an operator reading the three messages what the organisation is doing. Required:

- The three messages (from Part A section 3) in sequence as the operator would experience them.
- A short paragraph explaining what each message is designed to accomplish and what it is explicitly designed *not* to characterise (severity, cause, external posture).
- One sentence per message naming the approver of its content.

### Part C — The dry-run script

A step-by-step script for the dry-run session. Required:

- **Pre-session prep** — who confirms what in advance (ladder freshness, test group, access to test SSO group, vendor's test tenant, evidence store access, communication-channel-test access).
- **Session agenda** — timed, step by step; typical dry-run is 60 to 90 minutes.
- **Observation protocol** — who observes what. At minimum:
  - The enablement lead observes the user-visible state at each step and times the step.
  - IT identity executes and reports system-side status per step.
  - The ai-risk-engineer observes vendor-side effects (session termination, token invalidation).
- **Pass criteria and known-failure handling** — what counts as a successful dry-run; what the runbook amendment looks like if the dry-run surfaces an order-dependency or a user-visible-state problem.
- **Post-session artefact** — the amended runbook sections with date, signatures, and the specific changes made.

### Part D — The evidence-preservation sequence memo

A one-page memo to the ai-risk-engineer and the SOC describing the specific preservation surfaces the enablement side captures, the preservation standard the organisation holds to, and the escalation path if a preservation step fails during a live incident. This memo is co-input to Exercise 03.

## Starter guidance

- The hardest Part A section is the revocation sequence. Spend the first thirty minutes just enumerating every system the tool touches (SSO, licence pool, API, vendor admin, dependent organisational systems) and drawing the dependency order. The sequence is almost always surprising the first time.
- The user-visible state messages are often written in a hurry at launch and then not revisited. Write them deliberately; the operator reading the Slack message is the person whose trust the organisation is working hardest to keep in the first hour.
- The partial-pull shapes are often skipped. At minimum, draft the scope-narrow shape — the one most likely to be useful when the signal attributes to a specific function.
- Where a vendor-side action depends on vendor capability (does the vendor support a tenant banner? does the vendor support feature-toggles?), check the vendor's current documentation. Flag the gap inline with a `needs-research` marker if the answer requires a vendor conversation you have not had.
- The dry-run script's pass criteria should include *timing*. A revocation sequence that takes 90 seconds is different from one that takes 25 minutes; the operator's experience of the kill-switch depends on the time.
- The preservation sequence memo is the artefact that most directly supports Article 73 and parallel reporting obligations (Chapter 07). Write it as if general counsel will read it.
- For organisational facts you do not know (specific SSO group names, specific licence pool names, specific admin-console steps for your vendor), flag the gap inline with a `needs-research` marker. Do not invent.

## Deliverables

- `kill-switch-runbook.md` — the expanded operating runbook with all seven sections.
- `user-visible-state-plan.md` — the three-message plan.
- `dry-run-script.md` — the step-by-step dry-run script.
- `evidence-preservation-memo.md` — the one-page memo.
- A short cover note (3-5 sentences) naming the two hardest judgment calls in the runbook and the one place the dry-run is most likely to surface a weakness.

## Acceptance criteria

- The runbook names the authorising role explicitly (role name, not a person; delegation in writing if delegated).
- The revocation sequence enumerates every system the tool touches, with the order dependencies named.
- All three user-visible state messages are written in full; each has a named approver.
- The evidence preservation sequence is sequenced ahead of revocation; preservation ownership is named per surface.
- Communications templates exist for all three internal channels; no external channel template.
- At least one partial-pull shape is specified with its own revocation sequence and user-visible state.
- The standing-cadence obligations include all four Chapter 02 Property 6 triggers.
- The dry-run script has pre-session prep, agenda with timings, observation protocol, pass criteria, and post-session artefact.
- The evidence-preservation memo names the preservation standard the organisation holds to (not a vague description).
- A `needs-research` marker is used inline throughout wherever vendor- or organisation-specific facts are unknown.

## Stretch goals

- Author the **"cleanup-after-false-alarm"** section of the runbook: what the organisation does when a pulled tool turns out to not have been incident-worthy, how operators are brought back online, how the champion network and help channel communicate the un-pull, how the post-incident log is closed cleanly.
- Draft the **vendor-coordination-checklist** for a vendor-side incident where the kill-switch is pulled on the organisation's side independently of the vendor's own response: what you say to the vendor, by what channel, in what order, with the DPA references.
- Produce a **"runbook diff table"** comparing your current runbook to the launch-gate version from mod-102 Chapter 03 — specifically what changed from launch-gate to operating artifact and why. The diff is the artefact that teaches the next rollout how to make the same move.

## Why this exercise matters

The kill-switch is the enablement side's single most important operating control during an incident. A one-page launch-gate runbook does not pull a tool cleanly; a live operating artifact does. The gap between the two is six specific operating properties (Chapter 02) and a dry-run cadence. Producing the live operating artifact under a 2.5-hour budget is calibration for producing it against each new tool in the approved envelope, where the production cadence is ongoing and the dry-run is the tax the role pays twice a year to keep the control live.
