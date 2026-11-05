# Prompt Coaching for Non-Engineers

> "Prompt engineering" as a job title mostly evaporated in 2024–2025. What remained is quieter and more durable: a coaching posture that gets non-engineers unstuck when the tool is not doing what their job needs. This is coaching, not teaching — and the distinction is the one most enterprise programs still get wrong. This chapter is the coaching framing the enablement lead's team runs, and the explicit handoff to the engineering and analyst tracks for the depth your program should not try to carry.

## Why "coaching" and not "training"

Training transfers content. Coaching improves performance on a task the coachee is actually doing. The distinction matters because the enablement lead's team is not going to make a sales rep into a prompt engineer, and should not try. What the team *can* do is get a stuck sales rep from "the AI isn't doing what I want" to "I have a working prompt for the task" — repeatedly, reliably, across functions — and in the process improve the playbook's prompt library for everyone else.

Three practical differences in posture:

- **A trainer prepares a session; a coach shows up to the operator's problem.** The coach has frameworks in their head; they do not have slides.
- **A trainer's success is attendance; a coach's success is a shipped artifact.** The coachee walked out with a working prompt or a working workflow.
- **A trainer owns the content; a coach owns the *loop* between the coachee's work and the shared prompt library.** A good coaching session does not die with the coachee — it feeds the library.

If your prompt-engineering program is structured as a course, you are teaching. If it is structured as a set of 1:1s and small-group clinics with real problems in the room, you are coaching. The second is what this chapter treats.

## The two hard deferrals

Before the coaching program is designed, two groups are deliberately out of scope.

### IC software engineers → `ai-assisted-software-engineer` (level 20)

Engineers using AI inside their IDE and in code review do not need prompt coaching from the enablement lead's team. They need the level-20 curriculum: pair-programming patterns, test-and-verify loops, repo-scoped templates, context-window management for codebases, the engineering-specific failure modes.

Your program's role for this audience is:

- Enroll them in the level-20 curriculum.
- Publish the engineering playbook ([Chapter 04](04-role-based-playbooks-and-use-case-libraries.md)) that names the approved tools, the data-handling rules for code and secrets, and the org-specific patterns.
- Route engineers who ask for prompt coaching into the level-20 track.

What your program does not do: write prompt-engineering material for engineers. If an engineer cannot get what they need from the level-20 curriculum plus their playbook, the correct response is to improve the level-20 curriculum's intake or pair them with a senior engineer, not to have your enablement team write engineering-flavored prompt coaching.

### IC analysts → `ai-augmented-analyst` (level 20)

Analysts writing SQL, exploring data, building charts, and producing reports have the parallel track at level 20. Same deferral logic. The analyst playbook names the approved tools and patterns; the depth lives in the level-20 track.

The deferral is load-bearing because without it, the enablement lead's team grows a shadow engineering curriculum that is worse than the real one and distracts from the broader fluency work. Hold the line.

## The coaching surface — four formats

The coaching program offers four formats. They are listed from highest-touch to lowest-touch. Most of the demand comes from the lower-touch formats; the higher-touch formats cost more per operator but produce the material the lower-touch formats run on.

### Format 1 — 1:1 coaching (highest touch)

A single operator with a stuck problem meets one coach for 30–60 minutes. The session has a defined outcome: a working prompt, a working workflow, or a clear "this isn't a prompt problem; it's a data-handling problem / tool-selection problem / process problem" determination.

The 1:1 is reserved for:

- Senior operators where fluency gains have outsized multiplier effects (champions, specialists, high-leverage individual contributors).
- Problems that cannot be solved in group coaching because the data in the room is too sensitive to share.
- Patterns that are likely to generalize — the coach writes a playbook entry after the session.

Volume: budget 1–2 1:1 slots per coach per week. Enablement leads typically run some of these themselves; champions run others. More than 2 per week per coach and the coach is doing little else.

### Format 2 — Small-group clinics (the main vehicle)

Five to ten operators from the same function, meeting for 60–90 minutes, each bringing a specific problem. The clinic runs through the problems in sequence. Operators learn as much from each other's problems as from their own.

The clinic is the main vehicle because:

- The coach's time scales — one hour of coach time yields seven operator outcomes.
- The community effect — operators see peers getting unstuck and learn the moves.
- The prompt library feeds itself — several library entries typically emerge per clinic.

Cadence: one clinic per week per major function in the first year; biweekly in steady state. Hosted by a specialist-tier contributor (often a champion) or by the CoE's dedicated prompt coach.

### Format 3 — Walk-up office hours (the open slot)

Treated in [Chapter 05](05-the-delivery-mix.md) as the office hours vehicle; mentioned here because much of what happens inside office hours *is* prompt coaching. The operator walks in, says "my prompt isn't working," the coach sits with them for 10–20 minutes, they leave with a working version.

Office hours are the lightest-weight coaching format. They are also the one where coaches should be most ready to redirect — "this isn't a prompt problem, this is in your playbook already" or "you need the role workshop, not a 10-minute fix."

### Format 4 — The prompt library as asynchronous coaching

A good prompt library *is* a form of coaching at scale. Each entry is a frozen coaching conversation: when to use this, what goes in the placeholders, what to watch for.

The library is maintained by the coaching program. Every clinic and every 1:1 produces library updates. The library is itself the artifact that lets the coaching program scale past the capacity of the live formats.

## The coaching curriculum for the coaches

The coaches need their own curriculum. Not everyone who can prompt well can coach well.

Three capabilities make a coach credible:

- **The diagnostic repertoire** — five or six recognizable prompt-failure patterns the coach can name when they see them (the model is ignoring an instruction; the context is overloaded; the output format is under-specified; the model is being asked a question that is actually a data-handling question; the model is being asked a question that is out of its knowledge). Naming the pattern gets 70% of the way to the fix.
- **The prompt-adjustment moves** — the handful of techniques that fix the most common failures (add explicit output format; move critical instructions to the top and the bottom; break the task into steps; provide a worked example; shorten the context; switch tools entirely).
- **The *refusal to over-engineer* reflex** — the coach's most important skill is recognizing when the problem is not solved by a better prompt (data is wrong; task is poorly framed; tool is wrong; process is wrong). A coach who always has a prompt answer is a bad coach.

The coach curriculum is a specialist-tier bootcamp ([Chapter 05](05-the-delivery-mix.md)). The CoE runs it; champions and specialists who want to coach graduate from it. The bootcamp is also the entry criterion for coaching 1:1s — un-trained coaches burn credibility quickly in sensitive sessions.

## The anti-patterns the coaching program avoids

Three anti-patterns burn coaching programs. Name them, avoid them.

### "Prompt engineering 101" courses for everyone

A multi-hour course on prompt engineering, generic, delivered to every operator. Outcome: operators remember 10% of it two weeks later, cannot apply what they remember to their specific work, and the organization has invested dozens of hours per operator for a measurable effect close to zero. Teach grounded coaching inside role-based playbooks instead.

### "Prompt library as the whole program"

A static list of prompts, published once, treated as the program. Outcome: prompts work for the examples they were written for and fail silently when applied to adjacent cases. Operators use them for a week, hit failures, give up. The library needs the *loop* — coaching sessions that update it — to stay alive.

### "The CoE will prompt it for you"

Operators submit tickets asking the CoE to write their prompts. The CoE grows a backlog of prompt-writing requests and does the work *for* operators instead of coaching them to do it. Outcome: no fluency transfer; the CoE scales linearly with demand. The right response to most of these tickets is a coaching session, not a written prompt.

## The incident angle

Coaching sits next to incident response. A prompt that reliably produces output that violates the data-handling SOP, or that reliably produces output that causes an incident downstream, is not a coaching problem — it is a signal to pull the prompt from the library, pause the workflow, and route the issue through the incident pathway in [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).

The coaching program trains its coaches to recognize these signals. "I keep trying to get the model to help me with X" where X is in the restricted list is an escalation, not a prompt iteration.

## The coaching metric

The coaching program's metric is **artifact completion**, not session volume.

- How many operators came in with a stuck task and left with a working artifact?
- How many playbook entries were produced from the week's coaching sessions?
- What share of 1:1 requests are from first-time versus repeat operators (a healthy mix says the program is generating repeat value; all first-timers says one-shot help with no lasting fluency)?

Session count is a cost metric, not a value metric. Do not report it as the headline.

## The scoping line — what prompt coaching is not

Four things prompt coaching is *not*, and this line is worth stating directly to prevent scope creep.

- **Not a service for generating marketing copy.** If an operator comes in asking the coach to write their newsletter copy, that is production work, not coaching. Redirect.
- **Not a free consulting line for a department's roadmap.** Coaching helps individuals get unstuck; it does not design departments' AI strategies. That is a BU-level conversation routed through the pilot pipeline ([mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md)).
- **Not an engineering service.** Engineering-depth work routes to the level-20 track, not to the coaching program.
- **Not a therapy slot.** Operators sometimes bring frustrations with AI that are really frustrations with their work, their manager, or their tools. The coach's job is to recognize this and help the operator get to the right support — not to absorb the frustration in an infinite 1:1.

## Where this chapter feeds

- [Chapter 04](04-role-based-playbooks-and-use-case-libraries.md) is where the prompt-library artifacts coaching produces live.
- [Chapter 05](05-the-delivery-mix.md) is where the group-format clinics and office hours slot into the delivery mix.
- [Chapter 07](07-measuring-fluency-growth.md) treats the measurement side — what to count and what not to.
- [mod-105](../mod-105-champion-networks-and-change-management/README.md) is the source of most coaches outside the CoE team.
- Exercise 04 asks you to design one coaching session format end-to-end.

## Summary

- Coaching, not teaching. The unit of success is a shipped artifact, not an attended session.
- IC engineering and IC analyst depth defers to the level-20 tracks (`ai-assisted-software-engineer`, `ai-augmented-analyst`). Hold the line.
- Four formats — 1:1, small-group clinic, walk-up office hours, prompt library as async coaching — in a mix tuned to the organization's size and demand.
- Coaches need their own curriculum: a diagnostic repertoire, a prompt-adjustment move set, and the refusal-to-over-engineer reflex.
- Three recognizable anti-patterns to avoid: generic prompt-engineering 101, prompt library as the whole program, CoE as a prompt-writing service.
- Measure artifacts produced and repeat-visitor mix; do not report session volume as the headline metric.
- The scoping line is worth stating: coaching is not marketing production, department strategy consulting, engineering work, or therapy.
