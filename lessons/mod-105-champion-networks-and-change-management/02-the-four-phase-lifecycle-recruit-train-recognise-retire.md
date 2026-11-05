# The Four-Phase Lifecycle — Recruit, Train, Recognise, Retire

> A champion network without a lifecycle is a roster with a date stamp. Over time, the roster accretes — the original cohort is still listed, new names get added, nothing is removed — and the field signal degrades to whatever the two or three still-active members happen to notice. The four-phase lifecycle is what stops the accretion. Treat each phase as a standing operation on the CoE's quarterly calendar, not a one-time project.

## Why "lifecycle" and not "program"

A program suggests a launch and a steady state. A lifecycle suggests a loop that every member goes around. The difference matters because the single most common failure mode of champion networks is **the stuck cohort** — the original 2024 champions still carry the title in 2026, half have changed role, two have left the company, and no one has been replaced. The lifecycle naming prevents that by making *retire* a visible phase on the same calendar as *recruit*.

The four phases, in order:

1. **Recruit** — sourcing the next intake of champions against a specific function and the next rollout cycle.
2. **Train** — bringing the intake to GA-day fluency on tool, policy, use cases, and escalation.
3. **Recognise** — the ongoing operations that keep active champions engaged and visible.
4. **Retire** — the planned exit from the role, with the knowledge transfer and the manager-release that make the exit clean.

Each phase has an owner on the CoE team (usually the operations analyst), a cadence, an artifact set, and a measurable outcome. The rest of the chapter treats each in turn.

## Phase 1 — Recruit

The recruit phase answers *who comes in next*. It runs on a cadence — typically once per quarter, aligned to the quarterly rollout plan from [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md).

### The intake question

Every recruit cycle starts with a sized intake:

- **How many seats are open this cycle?** Equal to (retirements this quarter) + (functions currently un-championed) + (business-unit expansion).
- **Against which functions?** A function without a champion has no field-signal interface; those seats recruit first.
- **Against which rollouts?** Champions are trained *ahead of* the rollout, not after. The quarterly rollout plan sets the recruit calendar.

The sizing question is a budget conversation with the exec sponsor. A rough starting shape: one champion per 50–150 operators in a function, plus one per business unit touching regulated workflow. A 3,000-person enterprise usually ends up with 25–45 active champions at any time; a 12,000-person global organization with 100–180. The numbers move; the ratio is defensible across the role evidence.

### Sourcing — four channels, in priority order

In roughly decreasing order of signal quality:

1. **Team-manager nomination.** [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) names team-manager nominations as a standing handoff; this is where it lands. Managers know who in their team is already helping peers with AI; the signal is high-quality because it reflects observed behaviour, not self-selection.
2. **Field signal from existing champions.** Active champions see talent in adjacent functions. "The analyst in supply chain who comes to every office hour and has already built two agent workflows" is a champion-shaped observation that another champion is positioned to make.
3. **Self-nomination with a manager co-signature.** Applications can be open but the manager must co-sign at submission time. Self-nomination alone produces an enthusiasm-selected cohort that burns out; the manager signature filters for operators whose actual work can accommodate the role.
4. **HR / L&D data.** Completion of the foundational curriculum, high engagement with office hours, prompt-library contributions. Use this as a shortlist against which nominations are checked, not as the primary channel.

The order matters because the signal quality degrades as you move down the list. A network sourced primarily through self-nomination skews enthusiast; a network sourced primarily through HR data skews compliance-completer. Nominations surface operators who are *already* doing the work informally.

### Selection criteria

Five criteria filter the candidate pool:

- **Local credibility.** When this person says "we tried that; here's what happened," their peers listen. Credibility usually comes from tenure or demonstrated competence in the function, not from title.
- **Manager release confirmed in writing.** Not a verbal "sure, go ahead" — a written commitment to the 10–20% time allocation for the duration of the term. The absence of a written release is the single best predictor of a cricket-network outcome ([Chapter 01](01-the-champion-network-as-a-change-management-asset.md)).
- **Already using approved tooling.** Candidates who have not used the approved envelope cannot be first-line answers on day one. Train them separately; do not recruit them into the champion role.
- **Communication capacity.** Not necessarily eloquence, but the capacity to write a two-paragraph field report that is actionable. This can be assessed with a short written exercise in the application.
- **Disposition toward escalation.** A champion who hides issues because they want to look competent is a liability. The selection conversation should probe how the candidate responded to an ambiguous situation in a prior role — looking for a disposition that escalates early, not late.

The criteria are deliberately not "most enthusiastic about AI." The goal is not to find the most excited users; it is to find the operators whose peers already turn to them.

### The term

Default term: **one year**, with the option of a second year. Two consecutive terms is common; a third is rare and should require a conversation with the exec sponsor about what structural problem it is covering for.

A finite term is important for three reasons:

- It makes retirement a scheduled event, not an awkward conversation.
- It creates visible turnover, which gives new champions a path in.
- It protects the champion's own career trajectory — the role is a growth experience, not a permanent fixture.

## Phase 2 — Train

The train phase answers *how does the intake become GA-ready*. It converges on a specific calendar: every champion is fluent on the tool, the policy, the use cases, and the escalation path **before** they appear on any launch-gate champion list.

### The champion bootcamp

The standard vehicle is a specialist-tier bootcamp from [mod-104 Chapter 05](../mod-104-training-programs-and-ai-literacy-curriculum/05-the-delivery-mix.md). Two to three days, cohort-based, 15–25 people per cohort, running twice a year (aligned to the semi-annual intake cycle for the network).

Curriculum slots — the content, not the delivery design:

- **The approved-tool envelope.** What's in, what's out, why. Covered fluently enough that a champion can answer "can we use X for Y?" against the envelope, without escalating every question.
- **The policy stack.** Acceptable-use policy, data-handling SOP, the ten-minute accident path from [mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md). The champion must be able to walk an operator through the accident path on a Friday afternoon, not read it to them.
- **The function's role-based playbook.** The specific use cases, prompts, and verification patterns for the function the champion will serve ([mod-104 Chapter 04](../mod-104-training-programs-and-ai-literacy-curriculum/04-role-based-playbooks-and-use-case-libraries.md)).
- **The escalation ladder.** Who gets paged for what, with named humans not role titles, and the field-report channel back into the CoE (treated in detail in Chapter 03).
- **The incident shape.** Not the forensic depth — that routes out to `ai-risk-engineer` L25 — but enough to recognise when the signal they are holding needs to escalate to the governance-owned path ([Chapter 08](08-the-handoff-to-the-governance-incident-path.md)).
- **The communications artifacts.** The current cadence from [Chapter 04](04-the-rollout-communications-cadence.md): what's being built, what's available, what's working, what's next. The champion is carrying these outward; they need to know where they live and how to use them.

### The pairing with an outgoing champion

Every incoming champion pairs with a retiring one for the first quarter. The pairing is not a mentorship — it is an active handoff of relationships (which operators in the function come with recurring questions), context (which policy exceptions were litigated with which outcomes), and voice (how this specific function talks about AI).

The pairing produces an artifact: a one-page **function hand-off brief** that the new champion keeps and the CoE files. Functions without a retiring champion to pair with get their brief from the CoE directly, drawn from field reports to date.

### The post-bootcamp 30-60-90

Three checkpoints in the first quarter:

- **30 days.** First field report filed. Shadowed one office hour. CoE check-in confirms the role feels tractable.
- **60 days.** Hosted first function office hour. At least one field report has produced a backlog ticket in policy, tooling, or training.
- **90 days.** Full operating cadence. Monthly network call attended. CoE-manager three-way check-in: is the time allocation holding? Is the function responding? Any adjustment to the role scope?

If a champion is struggling at 60 days, the intervention is almost always *not training* — it is time allocation, scope, or manager signal. Catch it here, not at the annual review.

## Phase 3 — Recognise

Recognition is the phase that keeps active champions engaged. It is operational, not ceremonial; the error is to think of it as the annual awards dinner.

### The three recognition channels

Three channels, run continuously:

- **Visibility into the organization.** Champions are named publicly as the local answer for their function. Their names appear in launch comms. Their contributions show up in the quarterly scorecard for the exec sponsor ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md)). An operator in the function who could not find their champion is a failure mode of this channel.
- **Visibility into their own career.** The champion role appears on the champion's performance review — as a named accountability their manager accepts and the champion's own leadership chain sees. HR / L&D partnership from [mod-104 Chapter 08](../mod-104-training-programs-and-ai-literacy-curriculum/08-partnering-with-hr-ld-and-internal-comms.md) is where this is negotiated.
- **Visibility into the program's direction.** Champions see their own fingerprints on the artifacts they carry. "The acceptable-use policy was updated this quarter; the change on section 4 came from field reports filed by champions in supply chain and legal ops." Attribution is specific; the champions named know their work mattered.

The third channel is the one most programs underinvest in and is the one that actually retains champions beyond a first term.

### Material recognition — small, and only when it helps

A one-sentence rule: material recognition (bonuses, titles, swag) is a reinforcement of the other three channels, not a substitute. A champion who stayed for the swag is the shape of a "crickets network" ([Chapter 01](01-the-champion-network-as-a-change-management-asset.md)); a champion who stayed because they could see their fingerprints on the policy is the shape of a healthy one.

Where material recognition helps:

- A modest annual budget (CoE-funded) for a cohort dinner or offsite day, with a work agenda alongside — not a thank-you dinner, a working one.
- A "contributed to policy/training/tooling" certificate the champion can attach to their performance review, co-signed by this role and (for policy contributions) `head-of-ai-governance` L60.
- A visible champion badge in collaboration tooling — small, functional (so operators can find their champion), not vanity.

The anti-pattern is a swag budget that scales with the recognition work; if champions are chasing the swag, the signal they produce degrades correspondingly.

### The standing network cadence

A monthly or bi-monthly network call. Agenda is short and real:

- Field reports since last call — summarised by the CoE, with named attribution.
- One deep-dive from a champion on a function-specific problem they are working through.
- Centre updates — upcoming rollouts, upcoming policy changes, upcoming training rev.
- One open slot for dissent or concern raised by a champion. **This slot is the one you protect** — the first time a champion raises a concern and it is defused rather than engaged with, the slot is dead.

A healthy network call runs 45 minutes. One that regularly runs 90 minutes is either the social-club pattern setting in or a symptom that the field reports are being used as the primary surfacing channel instead of the standing intake (Chapter 03).

## Phase 4 — Retire

Retirement is scheduled, planned, and clean. It is also the phase most programs skip, which is why the network accretes.

### When a champion retires

Four triggers:

- **End of term.** The one-year or two-year term expires; the champion is not renewing. This is the default path and should be the most common.
- **Role change inside the organization.** The champion has moved to a role or team where the champion accountability no longer fits. A promotion, a reorg, a sideways move. Default: retire from the role at the new team; recruit a replacement in the vacated function.
- **Role change in the champion's capacity.** Workload, personal situation, or scope change makes 10–20% unsustainable. This should be a *conversation* with the champion and their manager, not a resignation moment. Make it easy to step down.
- **Non-performance.** The champion is listed but is not operating — the 90-day signal (Phase 2) was missed, interventions have been tried, and the role is not working. This is rare if the selection criteria held, and uncomfortable, but it is the phase that prevents the "stuck cohort" failure.

### The retirement artifact

Each retirement produces a short handoff — the mirror of the function hand-off brief from Phase 2:

- Named relationships in the function, with enough context that the incoming champion can pick up without starting cold.
- Open field-report items — things the champion was watching that the incoming one should pick up.
- Policy or tooling exceptions specific to the function, with a pointer to the governance ruling.
- One-paragraph reflection on what was hard and what worked — written for the incoming champion, filed for the CoE.

The retirement artifact is not a checkbox. It is the primary knowledge-transfer vehicle for the function's AI adoption, and the single artifact the CoE has that preserves institutional memory across champion turnover.

### The alumni surface — light, optional, bounded

Retiring champions often remain interested in the program. A lightweight alumni surface — a Slack channel, two annual updates from the CoE, an invitation to the annual network-wide gathering if one exists — is appropriate and cheap. Making the alumni surface a work surface is the mistake: alumni are not current field-signal interfaces, and the CoE should not route backlog items through them.

## The lifecycle calendar, at a glance

A sustainable network runs the four phases on a recognisable calendar:

| Cadence | Phase activity |
|---|---|
| Weekly | Office hours by function (hosted by champion); CoE Slack monitoring of field-report channel |
| Monthly | Standing network call; retirement check-ins for champions in their final quarter of term |
| Quarterly | Recruit cycle (sourcing against Q+1 rollouts); field-report synthesis into policy/tooling/training backlog; recognition review |
| Semi-annually | Champion bootcamp cohort; term-end reviews; cohort retirement wave |
| Annually | Scorecard inclusion of champion-sourced contributions; network scope review (functions and headcount); manager-release renewal |

The calendar is not hypothetical. Chapter 07's measurement stack tracks whether each cell is running; Exercises 01 and 02 ask you to lay it out against a specific organization.

## Where this chapter feeds

- [Chapter 03](03-routing-field-signal-back-to-policy-tooling-and-training.md) treats the inbound-signal mechanics that Phase 1's field-report channel points at.
- [Chapter 04](04-the-rollout-communications-cadence.md) treats the outbound communications that Phase 2's bootcamp and Phase 3's recognition carry.
- [Chapter 07](07-measuring-change-management-health.md) treats the metrics that tell you whether each phase is healthy, including champion retention as a primary signal.
- Exercise 01 asks you to design the recruit plan for a specific organization; Exercise 02 asks you to run a two-way feedback-loop drill grounded in Phase 3.

## Summary

- Four phases — recruit, train, recognise, retire — run as a lifecycle on a standing calendar, not as a one-time program.
- **Recruit** sizes against open seats and rollouts; sources through manager nomination first; applies five selection criteria; terms are one year, renewable once by default.
- **Train** converges on GA-day fluency through a semi-annual bootcamp, pairs incoming champions with retiring ones, and uses a 30-60-90 to catch role-fit problems early.
- **Recognise** operates in three channels — visibility into the organization, into the champion's career, and into the program's direction. The third is the one that retains beyond a first term.
- **Retire** is scheduled, planned, and documented. Skipping this phase is how networks accrete into a stuck cohort; running it is how new recruits get a path in.
- The calendar — weekly to annual — is the operating surface the CoE runs and [Chapter 07](07-measuring-change-management-health.md) measures.
