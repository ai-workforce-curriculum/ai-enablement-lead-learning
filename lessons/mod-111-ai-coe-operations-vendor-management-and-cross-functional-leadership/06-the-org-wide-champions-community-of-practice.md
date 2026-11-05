# The Org-Wide Champions Community of Practice

> [mod-105](../mod-105-champion-networks-and-change-management/README.md) authored the champion network as a two-way feedback loop at the rollout and function level. That network — recruit, train, recognise, retire — is already running. The piece [mod-105](../mod-105-champion-networks-and-change-management/README.md) did not finish is the *community* layer that sits above the individual team-manager-owned networks and binds them into an organisation-wide practice. The team-scope network is owned by `ai-augmented-team-manager` (level 40); the community-of-practice layer is owned by this role (level 45). This chapter authors that layer at operating depth — the charter, the activities, the health metrics, and the two drifts that collapse the community back into a newsletter list.

## Why the community layer exists

The champion networks at team and function scope (owned by `ai-augmented-team-manager`) solve a specific problem: carry the centre's content outward inside *one* team and surface *that* team's field signal back inward. The function works. What it does not do:

- **Cross-team lessons do not flow.** A champion in the customer-service function who has built a strong verification pattern for policy-grounded Q&A has no standing channel to share that pattern with the champion in the sales-operations function who is about to build the same pattern. The team-level network loops within the team.
- **Cross-BU peer learning does not flow.** A rollout that worked well in the Americas commercial organisation does not reach the regulated BUs in Europe through the team-level networks. The networks respect their own boundaries.
- **The champions themselves do not have a peer community.** Being a champion is a demanding role ([mod-105 Chapter 02](../mod-105-champion-networks-and-change-management/02-the-four-phase-lifecycle-recruit-train-recognise-retire.md)); without a community of other champions, the role is isolating. Retention ([mod-105 Chapter 07](../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md)) suffers.
- **The CoE loses a cross-cutting signal surface.** The team-level reports already route through [mod-105 Chapter 03](../mod-105-champion-networks-and-change-management/03-routing-field-signal-back-to-policy-tooling-and-training.md); what the CoE does not see without a community layer is the *pattern across teams* — the same resistance signal appearing in five teams simultaneously, the same vendor shortfall reported in three BUs, the same cross-functional confusion in legal, HR, and operations about a new policy edit.

The community of practice is the layer that handles these four. It is not a replacement for the team-level network; it is the sibling layer that makes the aggregate network operate as more than a sum of parts.

## The charter — what the community is and is not

A community of practice benefits from being named explicitly. Silent CoPs become newsletter lists. The charter is a short written document — one page — that answers four questions.

### Question 1 — Who is in it?

The default membership:

- **All currently active champions** across the organisation's team-level networks. Membership is automatic with active status; it ends when the retirement phase completes.
- **The enablement lead and the operations analyst** as the CoE's standing seats.
- **Embedded enablement partners** where the pattern family calls for them.
- **Rotating observers** from the AI council (Chapter 05) — typically `ai-governance-analyst` on a one-quarter rotation, with the option for `ai-risk-engineer` or `senior-ai-governance-architect` to join a specific session when the content calls for it.
- **The CAIO as a standing observer** if one is in place. The observation surface is passive — the CAIO reads the community's artefacts and attends summits but does not facilitate.
- **Team managers** (`ai-augmented-team-manager`, level 40) at the semi-annual summit (below) in a listening-and-contributing capacity. The community is primarily the champions', not the managers'; managers appear for the summit's cross-team-lesson sessions but not for the weekly surfaces.

The charter does not include *all employees interested in AI*. That is the enablement program's audience, not the CoP's membership. A CoP whose membership blurs into general interest collapses into a newsletter list within a quarter.

### Question 2 — What is it for?

Three stated purposes:

1. **Cross-team lesson transfer.** Patterns, prompts, verification techniques, vendor-usage tricks that work in one function travelling to another function's champions deliberately, not by accident.
2. **Peer support for the champion role.** Champions read other champions' retrospectives, ask each other how to handle specific resistance signals ([mod-105 Chapter 06](../mod-105-champion-networks-and-change-management/06-ai-specific-resistance-patterns-adkar-and-kotter.md)), and share recognition.
3. **Cross-team pattern signal.** The CoE picks up patterns that live in the community but do not appear in any single team's field report — the five-team resistance echo, the three-BU vendor shortfall, the cross-functional policy confusion.

The charter does *not* say "the community is a decision-making body." Decisions belong at the AI council (Chapter 05) and at the CoE. The community is a practice layer, not a governance layer. A CoP that starts to vote on policy is a CoP that is drifting into the council's job.

### Question 3 — What does participation look like?

A member of the CoP contributes in three ways, in roughly decreasing frequency:

- **Reading the weekly cross-team post** (below). Low-touch, low-commitment.
- **Posting a cross-team lesson** when their work surfaces a pattern they think other champions could use. Expected cadence: once per quarter per champion on average, with heavier contributors and lighter contributors around that mean.
- **Attending the quarterly summit** (below). Two hours per quarter, in the champion's work calendar, covered by the manager-release commitment made at recruitment ([mod-105 Chapter 02](../mod-105-champion-networks-and-change-management/02-the-four-phase-lifecycle-recruit-train-recognise-retire.md)).

The participation shape is light deliberately. A CoP that demands heavy participation hollows out — champions already carry 10–20% of their time in their team role. The CoP has to fit *inside* that allocation, not demand additional time.

### Question 4 — What does the community produce?

The community's own artefact set:

- **The weekly cross-team lesson post.** One per week; usually curated by the operations analyst from the week's field reports and summit material.
- **The quarterly summit summary.** Two pages; shared across the CoE, the AI council, and the BU reviews.
- **The semi-annual community health report.** The four metrics below (membership, contribution, cross-team reach, retention) with the trend and the lead's reading.
- **The annual pattern library.** A publicly-visible internal artefact aggregating the year's cross-team lessons into a reusable resource. The library is the champion community's visible gift to the organisation.

## The weekly cross-team post

The lightweight engine of the community. The operations analyst drafts; the enablement lead reviews; the post ships on Fridays as part of the week's "external face" ([Chapter 01](01-the-coe-at-steady-state.md)).

### Content

Each post has three sections:

1. **One cross-team lesson.** A single champion-sourced pattern — a prompt, a verification step, a workflow adjustment, a resistance response — specific enough to be re-usable. 150–300 words. The lesson is sourced from field reports, summit material, or a direct ping from a champion. Attribution is explicit (unless the champion requests anonymity, which is honoured).
2. **One cross-team question.** A specific question an open field report has surfaced that the community might have an answer to. "How are champions in healthcare functions handling the new HIPAA-specific guardrails against policy-grounded Q&A on PHI-adjacent data?" is the shape. Responses go to the operations analyst and feed next week's lesson slot.
3. **One operating-loop signal.** A short note on what the CoE is tracking this week that the champions should know about — an incident the community should be alert to, a service-catalog slot change, a vendor certification lapse that affects what the champions can recommend. 50–100 words.

The format is tight; the post reads in three to five minutes. A champion who skims it in a work break has got what they needed.

### What the post is not

- **A comms channel for the enablement program.** The rollout communications cadence from [mod-105 Chapter 04](../mod-105-champion-networks-and-change-management/04-the-rollout-communications-cadence.md) runs the comms stream to the whole organisation. The CoP post is a peer surface for champions, not a comms broadcast.
- **A newsletter.** It carries no editorialising, no "lessons we learned," no padding. If the cross-team lesson slot has no lesson this week, the slot is empty with a one-line note; it is not filled with filler.

## The quarterly summit

A two-hour cross-team working session once per quarter. The community's standing operational cadence.

### Attendees

- All active champions (mandatory, release-committed).
- Enablement lead and operations analyst.
- One rotating AI council observer.
- Team managers (`ai-augmented-team-manager`) invited as listening-and-contributing attendees for the second half.
- Industry-flavour observers ([mod-108](../mod-108-industry-and-regulatory-flavours-of-enablement/README.md)) when the agenda calls for them.

### Standing agenda (120 minutes)

1. **Opening — recognition** (10 minutes). The lead reads the quarter's recognition — champions who have carried specific lessons across teams, champions who have completed their term and are retiring, champions who have moved into new roles that carry the community's work with them. Recognition precedes work, deliberately.
2. **Cross-team lesson showcase** (45 minutes). Three to five champions each present a 5–8 minute lesson sourced from the quarter's field reports or summit nominations. The format is deliberate: a specific problem, the pattern that worked, the evidence that it worked, the shape in which it could be transferred to other teams. Q&A with the full community afterwards.
3. **Pattern-signal reading** (20 minutes). The operations analyst presents the cross-team patterns the CoE has picked up over the quarter — the resistance echo, the vendor shortfall, the policy confusion. The community reads the patterns back, confirming or adjusting them. Patterns confirmed by the community rise to the AI council's next quarterly agenda.
4. **Peer surgery** (30 minutes). Champions pose specific open problems they are stuck on; the community works the problem in small groups of 3–5, with each group reporting back. The problems vary: a specific resistance signal that is not yielding to the standard ADKAR / Kotter interventions, a vendor-training session that is not landing, a policy edge case the champion cannot route.
5. **Closing — next quarter's focus and the summer / annual summit preview** (15 minutes). The lead names the theme for the next quarter's cross-team lesson emphasis (e.g., "measurement discipline," "escalation recognition," "industry-flavour handoffs") and previews any upcoming full-day summit.

The 120 minutes is rigid. A summit that routinely exceeds its scheduled time has an agenda problem, not a content problem. The lead protects the time.

### The annual summit

Once a year, the quarterly summit expands into a full-day format — typically 5–6 hours, with lunch — that includes the training managers and the functional partners ([Chapter 05](05-the-quarterly-cross-functional-operating-ritual.md)). The agenda compresses the four quarterly sections but adds:

- **The year's pattern library release.** The annual artefact of cross-team lessons, published internally.
- **Rotating champion-led deep dives.** Two or three hour-long sessions led by senior-tenure champions on patterns they have carried in depth.
- **Industry-flavour panels.** Cross-industry conversation on what the regulated BUs and the unregulated BUs have learned from each other.
- **The retiring champions' farewell.** The semi-annual retirement cohort presents what they are handing off to successors.

The annual summit is a community-visibility event. The CoE's executive sponsor appears; the CAIO appears; the head-of-ai-governance appears. The annual summit is both a working session and a public demonstration that the community exists and is operating.

## Measuring community health

Four metrics carry the community's health signal. They line up with — but are distinct from — the champion network health measurement from [mod-105 Chapter 07](../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md).

### Metric 1 — Membership

The count of active champions in the community, by function and BU. Baseline from the semi-annual intake cycle; movement from retirements and new recruits.

**Signal:** steady or growing membership with a distribution that matches the service-catalog's slot demand is healthy. Shrinking membership in a function where catalog demand is growing is a signal the team-level network is not recruiting adequately; shrinking membership overall is a program-wide health signal that routes to the risk register.

### Metric 2 — Contribution rate

The percentage of champions who have contributed to the community in the trailing quarter — posted a cross-team lesson, responded to a cross-team question, presented at a summit, participated in peer surgery. Target: 60–80% per quarter.

**Signal:** contribution below 40% for two consecutive quarters is a signal that participation is passive — champions are reading but not contributing. Contribution above 90% is also a signal — the community has become dependent on the same small cadre of contributors and is not distributed. Both deviations have specific interventions (below).

### Metric 3 — Cross-team reach

The number of distinct teams a champion's lesson has been applied by, measured through follow-on field reports. A lesson that is cited in subsequent field reports by three other teams has cross-team reach of 3.

**Signal:** median cross-team reach of 1 or below means lessons are not travelling. Signals a community format problem (the lesson showcase is not landing, the post is not read, or the pattern-signal reading is not connected to downstream slot work). Median reach of 3 or above is healthy.

### Metric 4 — Retention

The percentage of champions who complete their full one-year term versus the percentage who retire early. Target: ≥85% completion. Early retirement is a lagging indicator of a community (and network) health problem — either the role is more demanding than the brief commits to, or the CoP is not providing the peer support that makes the role sustainable.

**Signal:** retention below 70% is a program-level risk that routes to the AI council. Retention above 95% can also be a signal — champions may be staying past the point where their learning has stabilised, which blocks intake for new voices.

The four metrics are published in the semi-annual community health report, visible to the champion community, the AI council, and the exec sponsor. The transparency is deliberate: the community's accountability is to its members first.

## Interventions when health signals move

### Membership shrinking without catalog demand changing

Likely cause: the team-level networks are not recruiting on cadence. The semi-annual intake cycle from [mod-105 Chapter 02](../mod-105-champion-networks-and-change-management/02-the-four-phase-lifecycle-recruit-train-recognise-retire.md) is sliding.

Intervention: the lead reviews the semi-annual intake calendar at the BU reviews (Chapter 05). Specific BUs behind on intake are named; the lead and the BU head co-author the next cycle's recruit plan. Not in the community's purview — the community can surface the signal but cannot fix the intake slip.

### Contribution rate below 40%

Likely cause: the community format is not inviting enough contribution, or contribution is not being recognised.

Intervention: two moves. First, the operations analyst's curation of the weekly post actively solicits — reaching out to specific champions whose recent field reports surface lesson-shaped material, asking if they'd like to anchor the next post. Second, the quarterly summit's opening-recognition section explicitly names contributors from the prior quarter — making visible that contribution is visible. A CoP that recognises its contributors retains more of them.

### Cross-team reach median ≤ 1

Likely cause: the lesson format is not actionable. Champions are reading lessons but not using them.

Intervention: refactor the lesson format. Specific-problem-and-specific-pattern (as named in the summit section above) is the format; "we tried AI for X and here are our reflections" is not. The operations analyst's curation standard is tightened. The quarterly summit's showcase section is used as a format calibration — the strongest lessons shown at the summit are the model the weekly posts aim at.

### Retention below 70%

Likely cause: the champion role is overloading champions, or the CoP is not providing peer support.

Intervention: the lead routes the signal to both the team-level network (via the BU reviews) and the CoP's own operational cadence. On the network side, the team managers may need to confirm the release commitment is actually being honoured. On the CoP side, the peer surgery section of the quarterly summit may need to expand. Early retirement is an escalation surface — individual exits are discussed one-on-one with the champion and their manager; if the pattern is systemic, it rises to the AI council.

## Two drifts that collapse the community

### Drift 1 — The CoP becomes a newsletter list

Symptom: the weekly post ships, but contribution is flat. The quarterly summit becomes an attendance obligation. The community is nominally running but is not producing patterns that move across teams.

Diagnosis: the community has slid from practice into consumption. Members read; they do not contribute. Their membership feels like obligation, not peer belonging.

Correction: three moves, in order. First, the lead meets with the strongest contributors to understand what makes the community valuable to them, and amplifies those surfaces. Second, the summit's peer-surgery section is expanded relative to the lesson showcase — peer work is what makes a CoP a CoP; showcase alone can run as a newsletter. Third, the lead reviews the charter's "what participation looks like" statement against reality. If the real participation shape does not match the charter, one or the other has to change.

### Drift 2 — The CoP absorbs team-level work

Symptom: champions are coming to the community with problems that properly belong at the team level, with their own manager. The community is doing the work the team manager should be doing. The team-level networks are hollowing out.

Diagnosis: the ownership boundary between the team-manager-owned network and the community-of-practice layer has blurred. The level-40 role's authority is being undermined, and the level-45 role is absorbing the work that belongs there.

Correction: the enablement lead re-reads the handoff map from [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md), specifically the downward handoff to `ai-augmented-team-manager`. The community's weekly post explicitly refers team-scope issues back to the champion's team manager; the summit's agenda is calibrated against cross-team concerns only. A CoP that is doing team-scope work is a CoP that is breaking the scope contract.

## The relationship to the chapters ahead

- [Chapter 07](07-the-credentials-portfolio-as-shared-vocabulary.md) treats the credentials portfolio. The CoP's cross-functional surface is one of the places the shared vocabulary from AIGP / ATD / Prosci / ISO/IEC 42001 is used in practice — champions from governance-adjacent functions bring AIGP vocabulary, champions from HR-adjacent functions bring ATD / Prosci vocabulary; the community is a surface where the shared vocabulary is exercised.

## Summary

- **The community-of-practice layer sits above the team-level champion networks owned by `ai-augmented-team-manager`.** It is owned by this role (level 45) and solves four problems the team-level networks cannot: cross-team lessons, cross-BU peer learning, peer community for the champion role, and cross-cutting signal for the CoE.
- **The charter is explicit** on who is in the community, what it is for, what participation looks like, and what it produces. A silent CoP becomes a newsletter list within a quarter.
- **Light-weight cadence:** a weekly cross-team post (3–5 minute read), a quarterly 2-hour summit, a semi-annual community health report, and an annual day-long summit with an internal pattern library.
- **Four health metrics track the community:** membership, contribution rate, cross-team reach, and retention. Each has intervention patterns when it moves off target, routed through the BU reviews or the AI council as the scale calls for.
- **Two drifts to prevent:** the CoP collapsing into a newsletter, and the CoP absorbing team-scope work. The corrections live in the charter's clarity and in the handoff map discipline with the team-manager role.
