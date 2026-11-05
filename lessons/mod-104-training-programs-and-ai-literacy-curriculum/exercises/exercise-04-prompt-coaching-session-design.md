# Exercise 04 — Prompt Coaching Session Design

**Estimated effort:** 2 hours
**Format:** a session design document of 2–4 pages plus a facilitator guide, Markdown or docx
**Grounding chapters:** [06 — Prompt Coaching for Non-Engineers](../06-prompt-coaching-for-non-engineers.md), [04 — Role-Based Playbooks and Use-Case Libraries](../04-role-based-playbooks-and-use-case-libraries.md)

## Objective

Design, end-to-end, a repeatable **small-group prompt-coaching clinic** — the Format 2 coaching vehicle from Chapter 06 — that your champions can run inside a single function without you in the room. The deliverable is the artifact you would hand to a newly-certified coach and expect them to run this week.

## Prerequisites

- Chapter 06 read; Chapter 04 skimmed.
- Role-based playbook from Exercise 03 (or equivalent for a chosen function) in hand.
- A chosen function to design the clinic for.

## Problem statement

A specialist-tier contributor has graduated from the coach bootcamp and is ready to host their first small-group clinic. They need a repeatable session design: how to prepare, how to run the 60–90 minutes, how to document the output, how to send the right follow-ups. The design has to be reusable — a coach should be able to run the same clinic structure next month with a different set of participants and different problems.

## Requirements

Deliver one artifact with two parts: the **session design** (what the clinic is) and the **facilitator guide** (how a coach runs it).

### Part A — Session design (1–2 pages)

#### 1. Clinic metadata

- Function the clinic serves.
- Participant profile (role level, pre-requisite completion of foundational curriculum, max size — 5–10 recommended).
- Cadence (weekly / biweekly / monthly).
- Duration.
- Required coaching credential.

#### 2. Entry criterion

What participants bring to the clinic. Specify:

- The expectation that each participant arrives with a specific, concrete stuck problem (not a theoretical question).
- The intake artifact — a short form (5 fields: problem, task, what they tried, what failed, data classes involved) submitted before the clinic.
- What happens when a participant arrives without the intake artifact.

#### 3. Clinic outcome

Name the artifact each participant leaves with. Should be one of: a working prompt from the library (improved / confirmed / newly authored), a workflow rework, or a routed-out determination (this isn't a prompt problem — here is where to take it).

#### 4. Follow-through

- What the coach captures from the session (which prompts worked, which failed, which library entries need updating).
- How the capture feeds the prompt library ([Chapter 04](../04-role-based-playbooks-and-use-case-libraries.md)).
- The follow-up to each participant within 48 hours.

### Part B — Facilitator guide (1–2 pages)

A runbook a coach follows to run the session. Specify:

#### 1. Pre-session (15 minutes)

- Review intake artifacts.
- Cluster problems by pattern (e.g., three participants have output-format failures; two have context-overload failures).
- Note which problems look like they need routing out rather than coaching.

#### 2. Opening (5 minutes)

- Scope-setter and scope-boundary statement (what this clinic is for; what it is not).
- The verification norm — the coach will not improve a prompt that produces output the operator has not committed to verifying.

#### 3. The round-robin (45–70 minutes)

- Each participant presents their problem (90 seconds max).
- The coach names the failure pattern (the diagnostic repertoire from Chapter 06).
- Group practices the fix in 5–8 minutes per problem.
- The coach writes the "before/after" to the shared clinic document in real time.
- A participant without a viable prompt problem gets a short redirection.

#### 4. Closing (10 minutes)

- The three or four library-ready improvements that will be written up after the session.
- The routed-out items — participants who need a different vehicle instead.
- The ask back to participants: use the new prompts this week; bring back failures to the next clinic.

#### 5. Post-session

- Library updates authored and submitted (within 24 hours).
- Short follow-up to each participant (within 48 hours).
- Incident signals routed to the incident fast lane ([mod-109](../../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)) if any surfaced.

### Part C — The diagnostic repertoire cheat-sheet

A one-page coach cheat-sheet listing 5–7 recognizable prompt-failure patterns with:

- The pattern name.
- The symptom the coach would notice.
- The one-sentence fix.
- A short example.

Drawn from Chapter 06's "diagnostic repertoire" treatment. Shape it in your own words — do not paraphrase the chapter.

## Starter guidance

- Keep the clinic to 60–90 minutes. Longer sessions burn out coaches and dilute output quality. If you design a two-hour clinic, you are over-building.
- The intake artifact is load-bearing. Participants who arrive without a specific problem turn the clinic into a Q&A session and dilute the time of participants who prepared. Enforce the intake.
- The coach's refusal-to-over-engineer reflex (Chapter 06) is the hardest thing to encode in a facilitator guide. Write an explicit step in the runbook: "before working on a prompt, ask whether the problem is actually a data-handling problem, a tool-selection problem, or a process problem. If yes, route out." This is the move that separates good coaches from ones who end up as free prompt-writing services.
- Reference the library update loop concretely. A clinic that produces insights but no library updates is a clinic that does not scale. The capture-and-update step is in the facilitator guide for a reason.
- Match the function you chose in Exercise 03 so the clinic output feeds directly into that playbook's library.

## Deliverables

- `coaching-clinic-design-<function>.md` (or `.docx`): the three parts above (Session design, Facilitator guide, Diagnostic cheat-sheet).
- A short *coach-onboarding note* (3–5 sentences) you would read to a newly-certified coach before handing them the artifact. This is the trust-building moment of the handover.

## Acceptance criteria

- The session design specifies cadence, duration, participant profile, intake, outcome, and follow-through.
- The facilitator guide is detailed enough that a coach new to the format could run it in their first session without needing you in the room.
- The diagnostic cheat-sheet has at least five named patterns with symptom + fix + example for each.
- The intake artifact and library-update loop are specified concretely, not aspirationally.
- Scope boundaries are stated explicitly — the clinic is not an engineering service, a prompt-writing service, or an open Q&A session.

## Stretch goals

- Author the intake-form template verbatim — the exact 5 fields a participant fills in before the clinic.
- Design the first three clinics' *anchor topics* — the topic the coach surfaces when participants do not bring enough intake problems. Grounded in the role-based playbook from Exercise 03.
- Write a short post-mortem template a coach fills out after each clinic — what landed, what did not, what the next session should do differently. This is the coaching program's own iteration loop.
- Design the escalation path for when a participant's "prompt problem" is actually an incident signal. Route to the incident fast lane; specify the handshake.

## Why this exercise matters

Coaching is the vehicle that produces the most *recurring* fluency growth per hour of CoE time. A clinic design that scales (ten clinics per week across the org, run by trained champions) can outweigh a dozen set-piece workshops. Designing the clinic properly once produces a repeatable asset the champion network runs on for years.
