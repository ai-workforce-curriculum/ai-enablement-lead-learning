# The Rollout Artifact Set — What Must Exist Before Anyone Opens the Tool

> If the artifact set does not exist on launch day, it will be written in the dark, under incident pressure, three weeks later — by a different author, with a smaller signing surface, and with a user base already building muscle memory around the wrong pattern.

## Why the set has to exist *before* launch, not after

The most common rollout failure in this role is not a bad tool choice. It is a tool that goes live with a login URL and nothing else — no written answer to "what is this for," no SOP for sensitive data, no revocation path when the first leaver happens, no named human to call when it misbehaves. That shape is the **policy-after-rollout retrofit**, a named failure mode covered in Chapter 05. This chapter preempts it.

The retrofit fails mechanically. Once users are in the tool, every subsequent policy decision is also a *change* decision — you are not writing a rule, you are breaking an existing habit. Signing surface shrinks. Governance co-signs more reluctantly. Security pushes harder.

Operating rule: **the artifact set is a gate on rollout, not a deliverable of rollout**. Seven artifacts, in writing, co-signed, before the first non-pilot account is provisioned. The role is accountable for *the set existing and co-signed* — not for authoring every line.

## The seven artifacts

### 1. Use policy

A short written answer to "what is this tool for, and what is it not for," with examples of both. Two pages, not twenty. Approved data classes, approved task categories, and a non-exhaustive "don't do this with it" list — the part users actually read.

Co-authored: this role drafts; `head-of-ai-governance` L60 ratifies; legal and privacy review anything touching regulated data or external disclosure. Signed by: `head-of-ai-governance` L60, this role, legal, privacy.

Deep co-authoring workflow — intake, draft cycles, dissent capture, ratification — lives in mod-103. Launch-day requirement is lighter: the artifact exists and is signed.

### 2. Data-handling SOP

The operational procedure for data going into and coming out of the tool. In-scope data classes with examples. Retention (what the vendor keeps, for how long, whether prompts train the model). Egress behavior. The accident path — what a user does in the first ten minutes after they realize sensitive data was pasted in by mistake, and who they tell.

Co-authored: this role drafts the user-facing procedure; security owns the technical controls (DLP, logging, tenancy); privacy owns the data-class mapping and retention statement. Signed by: security and privacy. Without both signatures the tool is not approved for GA.

The accident path gets skipped and shouldn't. Users will paste the wrong thing in. The question is whether the SOP tells them exactly what to do, or whether they Slack a manager who Slacks a director who finds this role on a Friday afternoon.

### 3. Access & offboarding playbook

The identity lifecycle for the tool. SSO wiring (IdP, group, claims). License provisioning (auto on group membership, or request-based). Revocation on leaver *and* on internal transfer — the internal-transfer case is the one most rollouts miss and the one regulators care about. Periodic access review, quarterly at minimum for anything touching regulated data.

Executed by IT identity under their existing joiner-mover-leaver process. This role does not operate the IdP — this role owns that the playbook *exists*, is written against the actual tool, and has been accepted by IT identity. Signed by: IT identity lead, this role, and security if the tool crosses a security review gate.

If the leaver case is not scripted, a terminated employee retains a working login on day one post-exit, and the incident write-up will name this role.

### 4. Training package

Role-based training. Minimum three roles: **operator** (day-to-day users), **specialist** (power users, prompt-library maintainers, the people other users ask), **administrator** (the IT and governance side — configure, audit, revoke). Short and concrete. Not a sixty-slide deck. A one-hour operator session anchored on two or three live use cases, a two-hour specialist session, a focused administrator walkthrough of the admin console plus the audit log shape.

Co-authored: this role owns the shape; pilot-cohort SMEs author the use-case material; `ai-augmented-team-manager` L40 contacts validate that the operator session matches real team work. Signed by: this role and pilot team manager(s).

Full curriculum design — modality, assessment, Article 4 evidence — lives in mod-104.

### 5. Support & escalation path

The named path users follow when the tool misbehaves. Tier 1 is the help channel — Slack, Teams, or a ticket queue — with an SLA that is not "best effort." Tier 2 is enablement — this role's team or delegate. From tier 2, escalation forks: to **vendor** for product issues, to **governance** (`head-of-ai-governance` L60, `ai-governance-analyst` L15) for policy questions, to **security** (`ai-risk-engineer` L25 and the SOC) for incidents.

Co-authored: this role drafts the ladder; vendor relationship manager confirms vendor contact and SLA; security and governance confirm their own escalation contacts. Signed by: this role; each named escalation owner acknowledges in writing that their contact is current.

If the table is stale on day one, every incident starts with a scavenger hunt. The scavenger hunt *is* the incident.

### 6. Champion list

A written list of named humans — one per business unit or function at minimum — trained ahead of GA, who have agreed in writing to be the local first-line answer, whose managers have agreed in writing to let them spend the time. Named. Trained. Accountable. Not optional.

Co-authored: this role identifies candidates; `ai-augmented-team-manager` L40 contacts nominate; each champion's manager signs off on the time commitment. Signed by: this role and each champion's manager.

Champion *network* design — recognition, rotation, promotion paths, community of practice — lives in mod-105.

### 7. Kill-switch & rollback plan

A one-page runbook for pulling the tool cleanly. Who authorizes (name the role, not "leadership"). How access is revoked (which SSO group is emptied, which license pool is deprovisioned, in what order). What users see mid-rollback. What communications go out, to whom, on what channel. What preserved-evidence surface the post-mortem inherits.

Co-authored: this role drafts; `ai-risk-engineer` L25 pressure-tests the revocation sequence; `head-of-ai-governance` L60 signs on authorization criteria. Signed by: this role, `head-of-ai-governance` L60, IT identity lead.

Kill-switch *operation* — live incident mechanics, forensic hand-off, regulator-notification clock — lives in mod-109. This chapter authors the runbook; mod-109 runs it.

## The "ghost-user rollout" anti-pattern

A ghost-user rollout is the one where the tool is provisioned, the all-hands email goes out, the login works — and three weeks later the usage dashboard shows two hundred accounts and twelve weekly actives. A specific failure mode with a specific cause: no training package tied to a real use case, and no champion standing next to the user at their desk.

The wrong response is more marketing — a second launch email, a lunch-and-learn, an intranet banner. The right response, and the preempt that stops the ghost rollout happening in the first place, is two artifacts working together: the **training package** tied to a specific role and use case, and the **champion list** that puts a trained human in reach of every operator on day one. If those two are thin, the rollout is a ghost rollout no matter how good the tool is.

## The signing surface

The signing surface is the point. This role is the convener, not the sole author. Governance, security, privacy, legal, IT identity, and pilot team managers all sign pieces of it — which is how the rollout becomes *the organization's* rollout and not *this role's* rollout.

The seven as a launch checklist:

1. Use policy — governance, legal, privacy.
2. Data-handling SOP — security, privacy.
3. Access & offboarding playbook — IT identity.
4. Training package — this role and pilot team managers.
5. Support & escalation path — every named escalation owner.
6. Champion list — champions' managers.
7. Kill-switch & rollback plan — governance, IT identity, this role.

If any signature is missing on launch day, the rollout is not ready. Not a judgment call — the gate.

## Summary

- The seven-artifact set is a **launch gate**, not a launch deliverable — absent on day one, the rollout becomes a policy-after-rollout retrofit (Chapter 05).
- The seven: use policy, data-handling SOP, access & offboarding playbook, training package, support & escalation path, champion list, kill-switch & rollback plan.
- This role is accountable for the set *existing and being co-signed*, not for personally authoring every line — governance, security, privacy, IT identity, legal, and pilot team managers all sign surfaces of it.
- The ghost-user rollout is preempted by two artifacts working together: a role-based training package tied to a real use case, and a champion list with named, trained, manager-released humans one Slack message from every operator.
- Deeper treatments live elsewhere — mod-103 (policy), mod-104 (training), mod-105 (champion network), mod-109 (kill-switch operation) — but each assumes the launch-day artifact exists. This chapter is where it gets built.
