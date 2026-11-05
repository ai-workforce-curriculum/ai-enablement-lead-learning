# The Three-Stage Tool Selection Decision

> Most "we picked the wrong tool" stories are not tool stories. They are stories about a team that collapsed three decisions into one meeting and never noticed which one they were actually making.

## Why three stages, not one meeting

Tool selection at organization scope is three different judgements, each asking a different question, each capable of failing differently. Collapse them and the failure modes hide inside each other.

- **Stage 1 — Problem naming** asks *is there a real problem here, named precisely enough to be solved?* Fails as scope drift — "AI for sales" instead of a target task.
- **Stage 2 — Candidate evaluation** asks *which solution survives build-vs-buy, a scoped POC, and our approved-tooling envelope?* Fails as vendor capture or a six-month procurement loop on what should have been a two-week POC.
- **Stage 3 — Pilot-vs-rollout commit** asks *do we run a bounded pilot, or skip to rollout?* Fails as a rollout dressed up as a pilot, or a pilot that never converges.

The three-stage decision is R1 — the most-cited selection theme in the posting sample — and build-vs-buy / POC / approved-tooling envelope live inside Stage 2 (R2). This is your work. If you are not running it, procurement, a BU head, or a vendor AE is — and they are optimizing for something other than enterprise fit.

## Stage 1 — Problem naming

The forced artifact is a one-page problem statement with five fields. If any are missing, Stage 2 does not start.

1. **Problem statement.** One or two sentences, in the voice of the affected user. Not "we need AI." A problem.
2. **Target task.** The specific unit of work the tool would touch. A task, not a function. "Drafting first-pass responses to tier-one support tickets," not "customer support."
3. **Current baseline.** How the task is done today, by whom, at what cadence, at what quality bar. If you cannot describe the baseline in two paragraphs, you cannot measure whether the tool changed anything.
4. **Pain measurement.** A number, even a rough one — hours per week, backlog depth, error rate, cycle time, CSAT. "It feels slow" is not pain measurement. If no number exists, Stage 1's job is to instrument for one.
5. **User cohort.** Named group, sized. "Approximately 180 tier-one support reps across three regions," not "our support team." Cohort shape determines pilot design in Chapter 02.

The forbidden shortcut is *"We want a tool that does AI for sales."* That is not a problem; it is a budget line looking for a justification. The Stage 1 move is to push back to the five fields — usually through a thirty-minute working session with whoever owns the work, not whoever owns the budget.

A good problem statement reads like *"Tier-one support reps spend an estimated 11 hours per week drafting first-pass ticket responses from a 400-article knowledge base; cohort is 180 reps across three regions; current baseline is manual search plus copy-paste; backlog depth has grown over two quarters."* A bad one: *"We want to use GenAI to improve support."* The first names something; the second names nothing.

Stage 1 gate: thirty-minute review. Attendees: problem owner (often a function lead or an `ai-augmented-team-manager` L40 for the affected team), enablement lead, security / data partner on read-only. Go/no-go: *is this problem named well enough to evaluate candidates against it?* If no, iterate. Do not open Stage 2.

## Stage 2 — Candidate evaluation

Stage 2 answers *how do we solve the problem Stage 1 named?* It has three sub-decisions, in order.

### Build vs. buy — the one-line answer is required

Every Stage 2 writeup must contain an explicit build-vs-buy line, even when the answer is trivial. *"No, buy — commodity capability available from three vendors already in the envelope"* is a valid answer and must be written down. The alternative — *silently assuming buy* — is how organizations commission a custom agent they did not need, or miss an obvious internal-build opportunity an `applied-ai-engineer` L30 peer could have scoped in a week.

Short criteria (deep ROI math lives in mod-107): is the capability differentiated in the vendor market or about to commoditize; does the problem need internal data or workflow context no vendor can see; is there a maintenance commitment nobody will carry (build means carrying it forever); is there an `applied-ai-engineer` L30 bench available in the window the problem needs?

Most Stage 2 reviews land on buy. When the answer is build, mod-110 picks up the commissioning brief.

### POCs — explicit scope and timebox

A proof-of-concept inside Stage 2 is not a pilot. It is narrower, shorter, and answers only *does this tool do the target task at a quality bar we can measure?* A POC has: **scope** (single task, nothing adjacent); **timebox** (two to four weeks typical; longer than six weeks means it's secretly a pilot); **participants** (a handful of power users, not the full cohort); **exit criterion** (one pre-written sentence describing what would qualify the vendor for Stage 3 and what would knock them out). A POC that keeps getting extended is Stage 2 failing. Call it and move on.

### The approved-tooling envelope

The envelope is the small, pre-cleared list of vendors and tool patterns that have already been through the policy, security, data-handling, and procurement work — SSO cleared with IT identity, DPA on file, data-residency terms resolved, acceptable-use language already drafted (mod-103). A Stage 2 candidate inside the envelope can go to pilot in days, not quarters.

A candidate outside the envelope is not disqualified; it is simply not ready for Stage 3. The Stage 2 output is a decision: (a) begin envelope-admission work in parallel with governance, security, and procurement, or (b) deprioritize until the envelope catches up. What is not acceptable is running a pilot on an out-of-envelope tool and pretending the paperwork will catch up. When the rollout stalls at month four, it will stall on the paperwork.

Stage 2 gate: one-hour review. Attendees: enablement lead, security / privacy partner, procurement partner, Stage 1 problem owner, an `ai-risk-engineer` L25 on read-only for anything touching sensitive data. One-page artifact: problem restatement, build-vs-buy line, POC results (if any), envelope status, recommended candidate. Go/no-go: *is this candidate ready to commit to Stage 3?*

## Stage 3 — The pilot-vs-rollout commit

Stage 3 is the deliberate pause before the money moves. You have a named problem (Stage 1) and a chosen candidate inside the envelope (Stage 2). The only question: *pilot, or straight to rollout?*

The default is pilot. Pilot design is the subject of Chapter 02; Stage 3 decides the binary.

A direct-to-rollout skip is earned, not assumed. All of these should be true:

- **Low risk surface.** The task does not touch regulated data, external customers, or safety-of-life decisions.
- **Prior evidence.** Another BU, a peer organization, or a case study you trust has already run the equivalent pilot and the results are available.
- **Inside the envelope.** The tool has cleared policy, security, and data-handling work. No open items.
- **Small cohort.** Sized so that if rollout goes badly, the kill-switch and rollback plan from mod-109 can absorb it without an incident.

Miss one, pilot first.

Stage 3 gate: forty-five-minute review. Attendees: enablement lead, problem owner, security / privacy partner, procurement, the executive sponsor (often a BU lead or a `chief-ai-officer` L70 delegate for enterprise-visible tools), a `head-of-ai-governance` L60 or delegate for anything that will show up in the governance council. One-page artifact: problem, candidate, envelope status, pilot-vs-rollout recommendation with reasoning, kill-switch owner. Go/no-go: *commit to pilot, commit to rollout, or return to Stage 2.* The third option is the one people forget; name it explicitly.

## The stage-gate reviews at a glance

Three reviews, three one-page artifacts, three explicit go/no-go decisions. The pattern is deliberately uniform — same shape of meeting, same shape of artifact, different question each time. That uniformity lets the gates run at enterprise cadence without turning into a governance program of their own — a trap your `senior-ai-governance-architect` L50 peer will flag. Keep the gates light, written, signed. The decision log is the artifact that survives the role, not the slide deck.

## Summary

- The three stages are three different questions — problem naming, candidate evaluation, pilot-vs-rollout commit — and must be run as separate gates so their failure modes stay separable.
- Stage 1 requires a five-field problem statement; "AI for sales" does not pass.
- Stage 2 requires an explicit build-vs-buy line (even when the answer is "no, buy"), a scoped and timeboxed POC when needed, and candidates that fit the approved-tooling envelope — or a decision on envelope-admission work before Stage 3 opens.
- Stage 3 defaults to pilot; direct-to-rollout is earned by low risk, prior evidence, envelope fit, and a cohort small enough to kill-switch cleanly.
- Each stage closes with a short review, a one-page artifact, and a written go/no-go — the decision log is the artifact that survives the role.
