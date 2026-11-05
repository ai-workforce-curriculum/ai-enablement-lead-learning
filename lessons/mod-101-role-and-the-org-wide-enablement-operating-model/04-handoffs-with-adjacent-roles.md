# Handoffs with Adjacent Roles

> The scope contract from Chapter 01 draws your boundary. This chapter draws the arrows that cross it. For each arrow, name what crosses — an artifact, a metric, a decision — and the role on the other side. Without that specificity, "collaboration" degrades into recurring meetings that produce nothing.

## The handoff map, at a glance

Four handoffs do most of the real work in a running enablement program:

- **Down** to `ai-augmented-team-manager` (level 40, AI Workforce family — one level below you)
- **Sideways** to `ai-governance-analyst` (level 15, AI Governance family — operational legwork you consume)
- **Sideways** to `ai-risk-engineer` (level 25, AI Governance family — peer, engineered risk and red-team)
- **Up** to `head-of-ai-governance` (level 60, AI Governance family — program leadership)

There are more arrows (to legal, to security, to finance, to the applied-AI and agentic engineers you commission), but the four above are the arrows that structure the job. The rest plug in around them.

## Handoff 1 — down to `ai-augmented-team-manager` (level 40)

**They own:** one team's AI adoption — 5–30 people, one function. They write the team's playbook, run the weekly standup, measure the team's productivity delta, and hire against AI fluency on their roster.

**What you hand them:**
- The approved-tool envelope (so they don't pilot a tool that fails governance).
- The role-based playbook for their function (so they don't start from scratch).
- The training curriculum and cohort schedule (so their people have a path to fluency).
- The champion program and the slot for their team's champion (so they're plugged into the network).
- The acceptable-use policy and data-handling SOP (so they don't negotiate policy per team).
- The team-level scorecard template (so their team-level metrics roll into the org scorecard).

**What they hand you:**
- Field signal: use cases that worked, use cases that didn't, the tools their team tried off-envelope.
- Champion nominations from their team.
- Team-level adoption and outcome metrics (fed through the scorecard template, so you aggregate without editing).
- Early warning on their team's AI incidents (so the enablement-side incident path fires before it becomes a governance incident).

**The failure mode:** a team manager stops using your artifacts because they are too generic. The fix is almost always in the role-based playbook — too few examples from the function, too much generality. Treat team-manager feedback as the highest-priority signal on curriculum and playbook quality.

## Handoff 2 — sideways to `ai-governance-analyst` (level 15)

**They own:** the operational legwork of governance — intake-questionnaire follow-ups, control-evidence collection, model-inventory maintenance, policy-change bookkeeping, audit prep. They live inside the governance program, not inside the CoE.

**What you hand them:**
- Completed intake questionnaires from your pilot pipeline (so the model inventory stays current).
- Rollout artifact sets for each tool you take to general availability (policy reference, access / offboarding playbook, support path, kill-switch procedure).
- Champion field reports that look like policy-relevant signal (so they can file them against the right control).
- Training-completion rosters (so the Article 4 literacy evidence has a provenance trail — see [Chapter 05](05-eu-ai-act-article-4-and-the-literacy-floor.md)).

**What they hand you:**
- The current model inventory — what's approved, what's in review, what's withdrawn.
- Policy-change notices with enough lead time that you can brief champions and update training before the policy drops.
- Evidence requests for upcoming audits (so you prepare the enablement-side evidence instead of scrambling).
- Status on intake tickets that have stalled at governance (so you can escalate instead of letting pilots die in queue).

**The failure mode:** the analyst becomes a human API between you and the governance program head. Cultivate the direct relationship and treat the analyst as a partner, not a courier.

## Handoff 3 — sideways to `ai-risk-engineer` (level 25, peer)

**They own:** engineered risk — red-team exercises, model-eval harness, guardrail design, incident forensics. They sit in the AI Governance family at level 25 but their counterpart-of-choice on the enablement side is you.

**What you hand them:**
- The list of tools in the approved-tool envelope so they know what to red-team first.
- The rollout rank-order (which rollouts are large or politically sensitive) so their eval coverage matches the exposure.
- Champion field reports that look like red-team signal — unexpected outputs, prompt-injection attempts, data-exfiltration-shaped behavior.
- The incident fact pattern when an enablement-side incident needs engineered root-cause.

**What they hand you:**
- Red-team evidence you can cite in the pilot-to-rollout decision (did the tool break under adversarial use? what was the mitigation?).
- Guardrail configurations that constrain known failure modes (so your rollout artifact set includes the guardrail, not just the tool).
- Incident forensics write-ups (so the training content, the champion briefing, and the policy update are grounded in what actually happened).
- Model-evaluation reports on the tools you are considering — real benchmarks, not vendor marketing.

**The failure mode:** you ship a rollout without red-team evidence. The first time the tool gets prompt-injected in the wild, you have no story for the governance council. Build the handoff into the pilot-to-rollout checklist.

## Handoff 4 — up to `head-of-ai-governance` (level 60)

**They own:** the governance program at enterprise scope — board-facing governance reporting, regulator engagement, the AI governance council chair seat, enterprise AI risk posture. They own policy; you co-author.

**What you hand them:**
- Draft acceptable-use policy and data-handling SOPs for their redline and ratification (see [mod-103](../mod-103-policy-co-authoring-with-governance/README.md)).
- Monthly / quarterly executive scorecard inputs (your rollout evidence feeds their board narrative).
- Incidents that meet escalation criteria from Chapter 03 (see [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) for the full path).
- The aggregated Article 4 literacy-evidence packet (see Chapter 05) for regulator-facing claims.

**What they hand you:**
- Ratified policy you can enforce (not a draft you have to defend).
- Regulator-facing decisions that change the enablement operating model (e.g., a new high-risk use-case category requires a new intake sub-process).
- Program-level priorities for the quarter (so your rollout backlog aligns with the governance program's milestones).
- Air cover when a BU tries to ignore policy (your authority ends at co-author; theirs ends at owner).

**The failure mode:** you start speaking as policy owner. The head of governance is now unclear whether they are being briefed or bypassed; your legal and regulator-facing stakeholders stop trusting the line. Co-author means co-author.

## A sketch diagram you can draw on a whiteboard

Not a literal diagram here — you're drawing this on a whiteboard in the first week of the job — but here is the mental picture:

```
                   [head-of-ai-governance (L60)]
                           ^   policy / incident escalation / regulator
                           |
                           |  evidence / draft policy / scorecard inputs
                           v
[ai-risk-engineer (L25)] <----> [AI ENABLEMENT LEAD (L45)] <----> [ai-governance-analyst (L15)]
   red-team / guardrails /        operating model / rollout /       intake / model inventory /
   incident forensics             champions / exec scorecard         training evidence / audit prep
                           ^
                           |  playbook / training / policy /
                           |  champion slot / scorecard template
                           |
                           |  field signal / team metrics /
                           |  champion nominations / incident flags
                           v
                   [ai-augmented-team-manager (L40)]
                            (one per team; many of them)
```

Four arrows. Each one labeled with concrete artifacts and signals. If you cannot label each arrow with at least one *specific* artifact that crosses it this quarter, the handoff isn't real yet — it is an org-chart line.

## The arrows that are not drawn

These exist and are important, but they do not structure the role; they plug into it:

- To **legal counsel** — you consume legal opinion through governance; you do not have a direct legal opinion relationship.
- To **security / IAM** — SSO, DLP configuration, DFIR; you feed signal, they execute.
- To **finance / procurement** — budget narrative, contract execution; you build the business case, they do contracts.
- To **applied-AI / agentic engineers** — commissioned internal tools (see [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md)); you commission, they build.
- To **the CAIO or executive sponsor** — the scorecard and the budget ask; they decide, you deliver.

All of these are real; none of them are the four load-bearing handoffs above.

## Summary

- Four handoffs structure the role: team manager (down), governance analyst (sideways, down), risk engineer (sideways, peer), head of governance (up).
- Every arrow carries specific artifacts in each direction; label them or they aren't real.
- The co-author / owner distinction with `head-of-ai-governance` is the one you are most likely to blur. Don't.
- Draw the map in your first week and revisit it quarterly — arrows change as the program matures.
