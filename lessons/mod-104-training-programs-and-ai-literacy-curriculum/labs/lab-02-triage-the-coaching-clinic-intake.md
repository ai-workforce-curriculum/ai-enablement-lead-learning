# Lab 02 — Triage the Coaching Clinic Intake

**Duration:** 60–75 minutes
**Format:** guided hands-on — six pre-written intake tickets, pattern-cluster and route, time-box the live clinic, author the library updates
**Grounding chapters:** [06 — Prompt Coaching for Non-Engineers](../06-prompt-coaching-for-non-engineers.md), [04 — Role-Based Playbooks and Use-Case Libraries](../04-role-based-playbooks-and-use-case-libraries.md) (where library updates land)

## Objective

Dry-run the **pre-session triage** that a small-group prompt-coaching clinic lives or dies by — the 15-minute move Chapter 06's Format 2 names (and [Exercise 04](../exercises/exercise-04-prompt-coaching-session-design.md)'s facilitator guide specifies). You will cluster six incoming problems by failure pattern, decide which are coaching and which route out, time-box the live round-robin, and author the library updates that land after the session.

This lab operates one layer below [Exercise 04](../exercises/exercise-04-prompt-coaching-session-design.md). Exercise 04 asks you to *design* the clinic (session design + facilitator guide + diagnostic cheat-sheet). This lab is the live facilitator move inside a clinic once the design exists: the move that separates "this clinic produced a shipped artifact" from "this clinic was a nice conversation."

## Prerequisites

- Chapter 06 read, specifically *The coaching surface — four formats* (Format 2) and *The coaching curriculum for the coaches* (the diagnostic repertoire). Chapter 04 skimmed (prompt-library entry shape).
- A chosen function and organization. Carry forward the one from [Exercise 03](../exercises/exercise-03-role-based-playbook-for-one-function.md) if you did it. If none, pick customer service or sales — the tickets below are written to that pattern.
- Your organization's data-classification taxonomy (see [Lab 01](lab-01-author-the-module-4-data-handling-scenario-triad.md)'s shape).
- A blank markdown file.

## Why a lab, not an exercise

The design exists; the facilitator move has to be rehearsed. Chapter 06 names three anti-patterns — generic prompt-engineering 101, prompt library as the whole program, CoE as a prompt-writing service — and all three are the result of a coach who did not triage well. A coach who runs the full round-robin with no pre-cluster produces a Q&A session; a coach who writes prompts for every ticket produces a free prompt-writing service. This lab is the triage move practiced against a realistic ticket set.

## Setup

Open a file called `coaching-clinic-triage.md` with this header, then work through Steps 1–5 below.

```markdown
# Coaching Clinic Triage Dry-Run — <function>, <organization>

**Clinic format:** small-group (Format 2 per Chapter 06)
**Duration:** 75 minutes total (15 pre-session triage + 5 opening + 45 round-robin + 10 closing)
**Participant cap:** 6 (the triage set below)
**Coach credential:** graduate of the coach bootcamp (Chapter 06)
**Facilitator:** <you>
```

## The six intake tickets

Use these six pre-written intake artifacts as the clinic's incoming cohort. Each is deliberately typical of what a real clinic receives in its first six months.

Participants have filled the Exercise-04 intake form with five fields: `problem`, `task`, `what they tried`, `what failed`, `data classes involved`.

### Ticket 1 — Operator: senior support rep

- **problem:** "The chatbot keeps producing replies that cite a refund policy we retired six months ago."
- **task:** draft a tier-1 reply to a refund-request ticket.
- **what they tried:** two or three versions of the same prompt pattern they learned in the role workshop.
- **what failed:** every output repeats the retired policy text.
- **data classes involved:** customer identifiers, ticket content (restricted), policy citations (internal).

### Ticket 2 — Operator: new support rep (3 weeks in role)

- **problem:** "The AI won't write replies in our brand voice."
- **task:** draft a tier-1 reply.
- **what they tried:** "Please use our brand voice."
- **what failed:** outputs are generic.
- **data classes involved:** customer ticket content (restricted).

### Ticket 3 — Operator: team lead

- **problem:** "I need the AI to help me plan our team's AI rollout for the next quarter."
- **task:** write a department roadmap.
- **what they tried:** asked the chatbot to "write a roadmap for our team's AI adoption."
- **what failed:** outputs are shallow and generic.
- **data classes involved:** internal (team names, roadmap draft).

### Ticket 4 — Operator: support rep

- **problem:** "The AI keeps hedging in replies and customers call us out for sounding evasive."
- **task:** draft a tier-1 reply where the answer is a clear no.
- **what they tried:** adding "be direct" to the prompt.
- **what failed:** outputs still hedge.
- **data classes involved:** customer ticket content (restricted).

### Ticket 5 — Operator: support rep

- **problem:** "I want the AI to generate a workaround so customers can get refunds outside our policy window when they really need it."
- **task:** draft replies offering a workaround.
- **what they tried:** several prompt rewordings framing the workaround as a goodwill gesture.
- **what failed:** the model does it, but the operator's manager pulled two such replies in QA.
- **data classes involved:** customer identifiers, refund amount (restricted).

### Ticket 6 — Operator: support specialist

- **problem:** "I want to write a newsletter for our team covering the last quarter's AI wins."
- **task:** produce the newsletter.
- **what they tried:** a single prompt describing the audience.
- **what failed:** outputs are fine but generic.
- **data classes involved:** internal.

Add each ticket verbatim as a numbered block in your lab file before Step 1.

---

## Step 1 — Pre-session pattern-cluster (15 min)

Chapter 06's "coaching curriculum for the coaches" names the diagnostic repertoire: five or six recognizable prompt-failure patterns the coach can name when they see them (the model is ignoring an instruction; the context is overloaded; the output format is under-specified; the model is being asked a question that is actually a data-handling question; the model is being asked a question that is out of its knowledge; and the recurring sixth — the shortening-the-context / switch-tools move).

For each of the six tickets, write a one-sentence **pattern diagnosis** using one of these names. If a ticket does not fit one of the named patterns, name the mismatch explicitly — this is usually the signal that the ticket is a route-out, not a coaching case.

Then, in a `cluster` note at the bottom of Step 1, group the tickets by pattern. Example clustering (your own may differ based on your reading):

- "The model is working on stale context." — Ticket 1 (retired policy lives in the prompt or in the tool's retrieval index).
- "The output format is under-specified / the instruction is too abstract." — Ticket 2 (brand voice), Ticket 4 (directness).
- "This isn't a prompt problem — it is a department-strategy conversation." — Ticket 3 (route-out per Chapter 06's scoping line).
- "This isn't a prompt problem — it is an incident signal." — Ticket 5 (the operator is trying to use the tool to bypass policy; Chapter 06's "incident angle" routes this through the incident pathway).
- "This isn't a prompt problem — it is production work, not coaching." — Ticket 6 (Chapter 06's scoping line: not a service for generating marketing copy).

**Checkpoint 1 — do not proceed until all three are true:**

- [ ] Every ticket has a one-sentence pattern diagnosis.
- [ ] Route-outs are named *before* the clinic starts — the coach does not discover them live.
- [ ] At least one ticket is identified as either an incident signal or a scoping-line violation (production, strategy, or engineering work) — if your diagnosis has all six in the "coachable" bucket, you have not applied the refusal-to-over-engineer reflex.

---

## Step 2 — Decide the live-session shape (10 min)

With the cluster in hand, author the live session's timeline in a short bulleted plan. Total live time is 60 minutes (75 total minus the 15-minute triage). A realistic shape:

- **Opening (5 min).** Scope-setter and scope-boundary statement; the verification norm; name the route-outs so those participants know what to expect in the Closing.
- **Round-robin (40–45 min).** 7–10 minutes per coachable ticket.
- **Route-out handling inside the live time (5 min).** Not a working session for the route-out tickets; a named routing with the participant present so they leave with the right next step. Not glossed over — Chapter 06 is explicit that the live acknowledgment is part of what makes the coaching program credible.
- **Closing (10 min).** Library-ready improvements; follow-up asks; the incident-pathway handshake if Ticket 5 was present.

For each coachable ticket, write a two-line **planned move** using the prompt-adjustment moves from Chapter 06:

- Ticket 1 — planned move: name the stale-context pattern; cycle the operator through verification (cite the live policy inside the prompt, not rely on the model's memory); if the retrieval index itself is stale, this becomes a workflow issue to route into the playbook refresh cycle.
- Ticket 2 — planned move: specify the output format and provide a worked example (two of the chapter's named moves) — brand voice is under-specified without an anchor sample.
- Ticket 4 — planned move: move the critical instruction to the top and bottom; provide a worked example of a clear-no reply in the brand voice.

**Checkpoint 2:**

- [ ] The 60 live minutes balance to within a five-minute tolerance.
- [ ] Each coachable ticket has a planned move that names a specific Chapter 06 adjustment (format, example, top-and-bottom, break-into-steps, shorten-context, or switch-tools).
- [ ] The route-outs have a named *destination* each — not "route out" alone — e.g., incident pathway per [mod-109](../../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) for Ticket 5, pilot pipeline per [mod-102](../../mod-102-selecting-and-rolling-out-ai-tools/README.md) for Ticket 3, production-work decline with no destination for Ticket 6.

---

## Step 3 — Dry-run the opening and one coaching pass (10 min)

Rehearse out loud (or in writing) two short moments.

### 3A — The 5-minute opening

Write the two or three sentences you will say at the top of the clinic. Include:

1. The scope-setter: what this clinic is for.
2. The scope-boundary statement: what this clinic is not — Chapter 06's scoping line (not a marketing-production service, not a department-strategy consulting line, not an engineering service, not a therapy slot).
3. The verification norm: the coach will not iterate a prompt that produces output the operator has not committed to verifying per Module 5 / the role-based playbook ([Chapter 04](../04-role-based-playbooks-and-use-case-libraries.md)).

Keep it under 120 words. If the opening runs over, the clinic opens late and the round-robin compresses.

### 3B — One coaching pass, written out

Pick one of the coachable tickets (2 is often the richest for a dry-run). Write the 7–10 minute pass in a mini-script:

- The 90-second participant presentation (what the participant says).
- The coach's diagnosis sentence (the pattern name, out loud to the group).
- The group practice step — what the group does in the 5–8 minutes of working time (write the before/after; the exact adjustment).
- The coach's close for this ticket — the library-entry fragment that will be written up after the session.

The point of this step is to catch, before the live clinic, the move a coach commonly fluffs: diagnosing the pattern out loud *to the group*, not just in the coach's head. The naming is where the pedagogy lives.

**Checkpoint 3:**

- [ ] Opening is under 120 words and names the scoping line explicitly.
- [ ] The written coaching pass names the pattern out loud before the fix starts.
- [ ] The before/after is a concrete prompt diff, not an abstraction.

---

## Step 4 — Author the post-session library updates (15 min)

Chapter 06's main loop: a good coaching session feeds the shared prompt library (Chapter 04). A clinic that produces insights but no library updates is a clinic that does not scale.

Draft two or three library-update entries from the coachable tickets. Each follows the Chapter 04 prompt-library entry shape:

- **Name** (task-shaped, not technology-shaped).
- **When to use it** (1–2 sentences).
- **Prompt template** (verbatim, `[[BRACKETED]]` placeholders named for content).
- **Data classes accepted** (per the SOP).
- **Example filled-in input and output** (anonymized).
- **Known failure modes** (2–3 sentences; include the pattern this entry closes out so the next clinic recognizes it faster).

The updates land in the role-based playbook's prompt library within 24 hours of the clinic per the [Exercise 04](../exercises/exercise-04-prompt-coaching-session-design.md) facilitator guide — the capture speed is part of what keeps the library alive.

**Checkpoint 4:**

- [ ] Two or three library-update entries authored. Entries that could not be written in draft form within 24 hours of a real clinic should not be claimed — write what you can write; backlog the rest.
- [ ] Each entry's `data classes accepted` line is specific (e.g., "Customer ticket content: restricted. Policy citations: internal.") — not "appropriate data."
- [ ] Each entry's `known failure modes` names the pattern from Step 1 that produced the entry, so a future coach recognizes it faster.

---

## Step 5 — Metric capture and incident handshake (5 min)

Chapter 06's coaching metric is *artifact completion*, not session volume. Close the lab file with a three-line metric capture for this clinic:

- **Coachable tickets with a shipped artifact:** `<count>` of `<coachable total>`.
- **Route-outs completed with a named destination:** `<count>` of `<route-out total>`.
- **Library updates authored within 24 hours:** `<count>`.
- **Repeat-visitor mix (first-time vs. returning):** not applicable in Lab 02 (first session); this row stays in the template for future clinics.

Then write the one-line **incident handshake** for Ticket 5 (if that ticket landed in your cluster). The handshake names the person to notify, the artifact to hand them (the intake form text with the operator's stated intent), and the retention step — the ticket stays with the coach's log but the operator's live prompt stops now. The incident pathway is specified in [mod-109](../../mod-109-ai-incident-response-and-enablement-side-rollback/README.md); Chapter 06 names the handshake as part of the coach's training.

---

## Deliverable

- `coaching-clinic-triage.md` — the six intake tickets, your Step 1 pattern diagnoses and cluster, Step 2 live-session plan, Step 3 opening script and one written coaching pass, Step 4 library updates (2–3 entries), Step 5 metric capture and incident handshake if applicable.

## Expected output shape

Roughly 3–4 pages at normal body-text size. The triage work is dense; the library entries each run roughly half a page. If your output is a single page, the diagnoses and library entries are thin; expand. If your output is six or more pages, you have drifted into writing full playbook pages; a library update is a short entry, not a treatise.

## Checkpoint — self-evaluation

- [ ] Each of the six tickets has a one-sentence pattern diagnosis.
- [ ] At least two of the six are correctly identified as route-outs rather than coaching cases — if all six are "coachable," re-read Chapter 06's scoping line and "incident angle" and revisit.
- [ ] The 60 live minutes balance; each coachable ticket has 7–10 minutes with a named prompt-adjustment move.
- [ ] The opening script is under 120 words and names the scoping-line boundaries explicitly.
- [ ] 2–3 library updates are authored with every Chapter 04 field populated.
- [ ] The incident-pathway handshake is specified if Ticket 5 was present in the cluster.

## Common failure modes

- **All six tickets diagnosed as coachable.** The refusal-to-over-engineer reflex is not yet trained; Chapter 06 names this as the worst coach failure mode — a coach who always has a prompt answer is a bad coach.
- **Route-outs dismissed in Opening without a named destination.** A route-out without a destination is a brush-off; the participant leaves with no next step and the program loses credibility.
- **Opening runs long.** The clinic opens late and the round-robin loses depth. Keep the opening under 120 words.
- **Library updates skipped because "we'll do them later."** Chapter 06 names this as the pattern that lets the library die; the 24-hour capture is load-bearing.
- **Metric capture reports session volume as the headline.** Chapter 06 is explicit: artifact completion and library updates are the metrics; session count is a cost metric, not a value metric.

## What this lab prepares you for

The pre-session triage is the move Chapter 06 names as the one that separates a credible coaching program from a drain on the CoE. A coach who triages well runs a 60-minute clinic that produces three library updates and two clean route-outs; a coach who does not runs a 60-minute Q&A session that produces nothing durable. Rehearsing the move against a realistic ticket set builds the reflex that makes the live clinic work. The output of this lab also plugs directly into the role-based playbook's prompt library from [Exercise 03](../exercises/exercise-03-role-based-playbook-for-one-function.md) — the library updates you draft here are the ones that will land in the next revision.
