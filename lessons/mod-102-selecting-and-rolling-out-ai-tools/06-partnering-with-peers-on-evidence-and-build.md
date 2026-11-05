# Partnering with `applied-ai-engineer` and `ai-risk-engineer`

> You are not the builder and you are not the red-teamer. You are the person whose brief makes both of them useful. The quality of this chapter's two artifacts — the commissioning brief and the red-team ask — is what separates a rollout that holds up in front of a governance council from one that doesn't.

## Positioning — commissioner and evidence consumer

Two of your most load-bearing partnerships on a rollout do not report to you and never will. They sit on different ladders.

- `applied-ai-engineer` (peer, level 30) sits in the AI Engineering family. They (and their siblings `agentic-ai-engineer` and `agentic-systems-architect`) build. You do not.
- `ai-risk-engineer` (peer, level 25) sits in the AI Governance family. They run red-team exercises, model evals, and guardrail design. You do not.

Your scope contract (Chapter 01) is explicit: the build of internal agents defers to the AI Engineering family, and engineered risk / red-team evidence defers to the AI Governance family. That means your authority with these peers is not positional — it is *brief-shaped*. You get work out of them the same way: by handing them a sharply named problem (the artifact this role is good at) and consuming the artifact they return.

The implication is uncomfortable the first time you see it. If the problem you hand the engineer is vague, you get a vague agent. If the red-team ask you hand the risk engineer is late, you get red-team evidence that lands after the rollout has already gone sideways. Both failures are yours, not theirs.

## With `applied-ai-engineer` (peer, level 30, AI Engineering family)

When the three-stage selection decision from Chapter 01 lands on neither "use the approved-tool envelope as-is" nor "buy a commercial point tool," you are in **commission** territory. The deliverable is not a tool choice; it is a written brief handed to an `applied-ai-engineer` (or to `agentic-ai-engineer` / `agentic-systems-architect` when the problem is a multi-step agent or a platform, not a point tool).

The commissioning brief is this role's artifact. It is also the artifact you are most likely to short-change. Treat it with the same weight as the scope contract. At minimum it contains:

- **Problem statement.** One paragraph. The business problem, not the AI technique. "Service agents spend 40% of a ticket searching four systems for the same answer" — not "we want a RAG agent."
- **Target task.** The specific workflow step the tool is replacing, augmenting, or inserting into. Named from the user's point of view.
- **User cohort.** Who, how many, what their current baseline looks like, whether they are opt-in or mandated, and what training they have had.
- **Non-negotiable guardrails.** The behaviors the tool must not exhibit, phrased in terms the engineer can test against — data classes it must not touch, actions it must not take, surfaces it must not reach. These come out of policy (mod-103) and out of the red-team ask you will write in parallel.
- **Success criterion.** A measurable statement of what "this worked" means — outcome metric, workflow metric, or both (mod-106). Not usage, except as a sanity check.
- **Budget.** Both build and run. Steady-state cost matters as much as build cost; a tool that is cheap to build and expensive to operate is a landmine.
- **Timeline.** Pilot date, rollout date, and the decision gates in between.
- **Maintenance commitment.** Who owns the tool after handoff. If you do not have an owner named before the engineer starts, the tool is already dying.

### What the engineer needs from you at kickoff

A signed brief. Access to the user cohort for discovery and evaluation. The approved-tool envelope and policy references the tool has to respect. A clear statement that *you* are the single decision-maker on scope changes, not a committee.

### What you need from the engineer at acceptance

A working tool against the success criterion. An eval harness and a result on it. A runbook that your support path (part of the rollout artifact set — the chapter on the rollout artifact set covers this in depth) can actually operate. A maintenance plan and a named owner.

The full commissioning depth — productionize-worthiness assessment on inherited prototypes, the honest no-go call, scoring commissioned tools on the same outcome framework as any other rollout — is covered in **mod-110**. This chapter is the interface; mod-110 is the method.

## With `ai-risk-engineer` (peer, level 25, AI Governance family)

Before a rollout crosses a risk threshold, you ask for red-team evidence. The threshold is not subtle: sensitive data in the loop, customer-facing deployment, high-stakes decision support, or a regulator-touching workflow. If any of those conditions hold, the rollout does not go to general availability until red-team evidence is in the rollout artifact set.

The **red-team ask** is this role's artifact. The risk engineer runs the red team; you specify the scope. At minimum the ask contains:

- **Scope.** Which tool, which deployment surface, which user cohort, which data classes are in play. What is in bounds for the exercise and what is explicitly out.
- **Threat model inputs.** Who you believe the adversaries are (external attacker, malicious insider, well-meaning user, prompt-injection via content), what you believe is at stake, and which of the non-negotiable guardrails from the commissioning brief (or the vendor contract, if "buy") have to hold.
- **Success criteria for the red-team itself.** Not "find vulnerabilities" — that is not a criterion. Something closer to "demonstrate whether the guardrails hold under the top three attack classes we have named, and document the mitigations if they don't."
- **When results are needed.** Before the pilot-to-rollout decision, not after. Dated against your rollout calendar.
- **How findings fold back in.** Whose job it is to turn a finding into a guardrail change, a policy update, a training module, a champion briefing, or a kill-switch condition — and where that appears in the rollout artifact set.

The depth of red-team methodology — attack taxonomy, eval harness design, guardrail engineering — belongs to the `ai-risk-engineer-learning` track. You do not need to run the exercise. You need to ask for it well, consume the evidence, and route the findings into the rollout.

Red-team evidence lands **before** the rollout commit. Not alongside it. Not shortly after. If the risk engineer cannot turn the work around in time, the rollout waits.

## Common anti-patterns

- **The half-named problem.** "Make us an AI thing for HR." The engineer either builds something that misses or spends a month doing your discovery work for you. If you cannot write the problem statement in one paragraph, you are not ready to commission. Go back to the three-stage decision.
- **Red-team after rollout.** The tool is already live when you ask. Now every finding is an incident, not a design input. The first time a prompt-injection lands in the wild without red-team coverage, you have no story for the governance council — this is the failure mode called out in the handoffs chapter and it is entirely preventable.
- **Treating the risk engineer as an approver.** The red-team ask is a commission, not a sign-off request. The risk engineer gives you evidence; you make the rollout decision with it. If you push the call to them, you have abdicated a decision your scope contract says is yours.
- **Letting the engineer's preferred stack overwrite a "buy".** An `applied-ai-engineer` with time on their hands will cheerfully build something the approved-tool envelope already covers. Your job in the three-stage decision is to catch this before it starts. The commissioning brief exists partly as a forcing function: if the brief can be satisfied by a tool already in the envelope, don't commission.

## Signing surface

Two signatures sit on top of the two artifacts in this chapter:

- **Commissioning brief** — co-signed by this role and the engineer's manager (typically an `ai-engineering-manager` or a product/engineering director, depending on the organization's shape). Your signature commits to the problem framing, the user cohort, the maintenance owner. Theirs commits to the build.
- **Red-team ask** — co-signed by this role and `head-of-ai-governance` (level 60). Your signature commits to the scope, the threat model inputs, and the rollout dependency on findings. Theirs ratifies the ask against the governance program's priorities and gives the risk engineer air cover to deliver real evidence rather than vendor-friendly evidence. <!-- needs-research: confirm whether the head-of-ai-governance sign-off is universal or whether some orgs route this co-signature through `senior-ai-governance-architect` instead. -->

Both signatures are prerequisites. An unsigned commissioning brief is a conversation, not a commitment. An unsigned red-team ask is a favor you are asking, which is a brittle way to run a program whose output a regulator may read.

## Summary

- You are the commissioner, not the builder; the evidence consumer, not the red-teamer. Your authority with both peers runs through the brief you hand them.
- The commissioning brief to `applied-ai-engineer` (peer, level 30) names the problem, cohort, guardrails, success criterion, budget, timeline, and maintenance owner — mod-110 covers the full commissioning depth.
- The red-team ask to `ai-risk-engineer` (peer, level 25) names scope, threat model, success criteria for the exercise, deadline relative to the rollout, and the fold-back route for findings. Evidence lands before rollout, not after.
- Common failure modes — half-named problems, late red-team evidence, treating the risk engineer as an approver, letting a preferred stack overwrite a legitimate "buy" — are preventable at the brief, not downstream.
- Commissioning briefs are co-signed with the engineer's manager; red-team asks are co-signed with `head-of-ai-governance`. Unsigned briefs are conversations; unsigned asks are favors.
