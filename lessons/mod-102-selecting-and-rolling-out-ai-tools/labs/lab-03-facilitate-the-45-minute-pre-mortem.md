# Lab 03 — Facilitate the 45-Minute Pre-Mortem (Solo Dry-Run)

**Duration:** 60 minutes (the 45-minute meeting plus a 15-minute debrief)
**Format:** guided solo dry-run — you play facilitator *and* all five attendees; produces a signed one-page pre-mortem
**Grounding chapters:** [05 — Failure Modes and the Pre-Mortem That Preempts Them](../05-failure-modes-and-the-pre-mortem.md), [03 — The Rollout Artifact Set](../03-the-rollout-artifact-set.md), [01 — The Three-Stage Tool Selection Decision](../01-the-three-stage-selection-decision.md)

## Objective

Walk through the **45-minute pre-mortem meeting** end-to-end, as the facilitator *and* as each of the five attendees whose roles Chapter 05 names. Produce the signed one-page pre-mortem that Chapter 01 names as the prerequisite for the Stage 3 pilot-vs-rollout commit.

This lab is not Exercise 05's pre-mortem — that exercise asks you to *write three failure sentences and map them to artifacts*. This lab runs the *meeting* those sentences come out of, with the facilitator mechanics intact: silent writing before group discussion, verbatim capture, clustering by failure mode, and the artifact-owner assignment at the close. Running the meeting badly produces the same three sentences on the page and a rollout that still fails for the reason nobody could articulate.

## Prerequisites

- Chapter 05 read end to end, including the "How to run the pre-mortem meeting in 45 minutes" section.
- Chapter 03 skimmed far enough to name the seven rollout artifacts without looking.
- Chapter 01 skimmed to the Stage 3 gate — you will produce the pre-mortem that Stage 3 depends on.
- A chosen rollout. Carry forward from Exercises 01–05 if you have the pair. If not, pick:
  - 3,000-person US bank rolling out a code assistant to its 180-engineer platform team
  - 12,000-person global pharma rolling out a document-summarization tool to the 60-person medical-affairs writing team
  - 500-person SaaS company rolling out a meeting-notes tool to a 220-person go-to-market org
- A timer (phone, watch, kitchen timer). You will hold yourself to the Chapter 05 minute budget.
- A single markdown file.

## Why a lab, not an exercise

Exercise 05's pre-mortem is the *output artifact* — three sentences and a mapping. This lab is the *process that produces a defensible version of that artifact*. Most pre-mortems fail not at the sentence level but at the process level: the quiet skeptic's view gets absorbed into the sponsor's optimism in the first five minutes of discussion, and the meeting ends with a cheerful consensus the room already had before it started. Chapter 05 names the specific countermeasure — individual silent writing before group discussion — and that countermeasure is the whole technique.

A solo dry-run with the timer on is the cheapest way to build the facilitator muscle before the real meeting, where stopping to re-read the chapter is not an option.

## Setup

Create `pre-mortem-dry-run.md` with this skeleton:

```markdown
# Pre-Mortem Dry-Run — <organization> / <rollout>

**Date of dry-run:** <today>
**Facilitator:** AI Enablement Lead (me)
**Simulated attendees (five roles, played by me):**
1. AI Enablement Lead (facilitator — same role)
2. Sponsoring BU owner — <specific role title for your org>
3. Champion lead for that BU — <specific role title>
4. Governance representative — <specific role title, per the handoff map>
5. Known skeptic — <specific role title; someone known to have reservations about the rollout>

**The pre-mortem prompt (verbatim):**
> Imagine it is six months from now and this rollout has quietly failed. Write the three sentences that explain why.

## Round 1 — Silent writing (minutes 5–20)

<entries>

## Round 2 — Read-aloud + clustering (minutes 20–40)

<entries>

## Round 3 — Artifact + owner assignment (minutes 40–45)

<entries>

## The signed one-page pre-mortem

<entries>

## 15-minute debrief — what I learned about the meeting

<entries>
```

Start your timer.

---

## Step 1 — Minutes 0–5: the open (5 min on your timer)

Write the open, as the facilitator would say it:

```markdown
**Open:** "We have 45 minutes. The prompt is on the agenda. I will read it once. Then we will each — silently, individually — write three sentences that explain why this rollout has quietly failed six months from now. No discussion yet. Pens down at 20 minutes past the hour. Any questions?"
```

Chapter 05: "The lead reads the prompt. No discussion." Not a discussion of the prompt, not a clarification round. The point of the silence that follows is that it is actually silent.

**Checkpoint 1:**

- [ ] The open script is in your file verbatim.
- [ ] The prompt itself is quoted verbatim from Chapter 05 — not paraphrased.
- [ ] You did not spend more than five minutes on this step. If you did, your facilitator muscle is drafting into prose. The open is a paragraph, not an essay.

---

## Step 2 — Minutes 5–20: silent writing as all five attendees (15 min)

Chapter 05's technique, verbatim: "Everyone writes their three sentences *in silence*, individually. No whiteboard. No talking. Individual writing before group discussion is the whole technique — it is what keeps the quiet skeptic's view from being absorbed into the sponsor's optimism."

In the dry-run, you play all five roles. The discipline is that you write *as the role*, not as yourself. The point of the lab is to feel the difference. Set three minutes per attendee on the timer. No peeking at the others' sentences until you have finished all five.

For each attendee, fill in:

```markdown
### Attendee: <role title>

**Three sentences (first-person, in character):**

1. "Six months from now, this rollout failed because <specific, named reason>."
2. "Six months from now, this rollout failed because <specific, named reason>."
3. "Six months from now, this rollout failed because <specific, named reason>."
```

Guidance on writing in character for each role:

1. **AI Enablement Lead (facilitator — me).** Your job is to name the artifact-level failure the rest of the room would miss. Which of the seven Chapter 03 artifacts, in this specific rollout, do you suspect does not actually exist in the shape it needs to? Write from that intuition.
2. **Sponsoring BU owner.** They see the business problem. Their failure sentences will be about outcome — the thing the tool was bought to change not changing — and about their team's experience. They are least likely to name a governance-side failure and most likely to name a time-pressure one.
3. **Champion lead for that BU.** They see the field. Their failure sentences will often be the champion-of-one from Chapter 05, or a specific use-case that the training package didn't actually cover, or a Slack channel that went silent in week five.
4. **Governance representative.** They see the policy and incident surface. Their failure sentences will often be the policy-after-rollout retrofit — the SOP that was signed but was wrong on the specific data class that mattered, the escalation ladder that pointed at someone on long leave, the regulator inquiry that landed against an unsigned artifact.
5. **Known skeptic.** The skeptic's job in the room is exactly the one the technique is built to protect. Their sentences are often the most specific — write them accordingly. If your skeptic's sentences come out the same shape as the sponsor's, you have not written in character; re-write.

Chapter 05's refusal: "Vague pre-mortem sentences — 'adoption was slower than expected,' 'the vendor underdelivered,' 'the business was not ready' — are the single most reliable leading indicator of a rollout that will fail for exactly the reason nobody could quite articulate in the room." If any of your fifteen sentences comes out in that shape, strike it and re-write. The point is to feel what the strike-out costs you.

**Checkpoint 2:**

- [ ] Five sections, three sentences each — fifteen sentences total.
- [ ] Each sentence names a specific thing, not a mood. "Adoption was slower than expected" is a mood; "the only champion in the EU BU took a new role in month four and no second champion had been named" is a specific.
- [ ] The skeptic's three sentences sound meaningfully different from the sponsor's three. If they do not, the dry-run has not yet caught the failure mode the technique is designed to prevent.
- [ ] You stopped the timer at 20 minutes. If you ran over, note by how much — this is signal for the real meeting.

---

## Step 3 — Minutes 20–40: read-aloud + clustering (20 min)

Chapter 05: "Each attendee reads their three sentences aloud. The lead captures them verbatim. Cluster by named failure mode as you go."

In the dry-run, read each attendee's three sentences aloud (yes, out loud) and capture them *verbatim* in the file. Do not paraphrase into "cleaner" language; the verbatim capture is a facilitator discipline, and the cost of re-writing live is specifically what the chapter is refusing.

Then cluster. Chapter 05's four named failure modes are the starting taxonomy:

- **Ghost-user rollout** — licenses provisioned, usage near-zero; training+champions thin.
- **Metric-theatre pilot** — adoption up, outcome flat or unbaselined.
- **Champion-of-one** — one person carrying the program; no named second.
- **Policy-after-rollout retrofit** — artifact set thin on day one, written under incident pressure later.

A fifth, open cluster — "**Other — name it specifically**" — captures sentences that do not fit the four. Chapter 05: "The four named patterns in this chapter are a starting set, not a closed list."

Build the clustering table:

```markdown
| Cluster | Sentences assigned (verbatim) | Dominant failure mode |
|---------|-------------------------------|-----------------------|
| 1       |                               |                       |
| 2       |                               |                       |
| 3       |                               |                       |
| 4       |                               |                       |
| 5 (other, named) |                      |                       |
```

A sentence can land in only one cluster; pick the dominant failure mode even when the sentence touches two. The clustering is a facilitator judgment call — the discipline is to make the call, not to leave it ambiguous.

**Checkpoint 3:**

- [ ] Every sentence captured in Step 2 appears, verbatim, in one of the cluster rows.
- [ ] At least three of the four named failure modes from Chapter 05 have at least one sentence each. If one failure mode has fifteen sentences and the others are empty, your attendees were not in character — strike out the overweighted cluster and rewrite Step 2.
- [ ] The "other — name it specifically" row either is empty or contains a *specifically named* new failure pattern, not "miscellaneous."

---

## Step 4 — Minutes 40–45: artifact + owner assignment (5 min)

Chapter 05: "For every cluster, name the preempting artifact and its owner. If the artifact does not exist, the rollout does not clear Stage 3."

Build the artifact-and-owner table:

```markdown
| Cluster / dominant failure mode | Preempting artifact (Chapter 03 or beyond) | Current state (exists / stub / absent) | Owner (role) | By when |
|---------------------------------|---------------------------------------------|-----------------------------------------|---------------|---------|
| Ghost-user rollout              | Training package tied to real use case + champion list (Chapter 03 artifacts 4 + 6) |                                         |               |         |
| Metric-theatre pilot            | Pilot charter with pre-written adopt/extend/kill (Chapter 02) + measurement plan (Chapter 04 / Lab 02) |         |               |         |
| Champion-of-one                 | Champion list with strictly more than one per BU, written remits, manager-signed time allocation (Chapter 03 artifact 6; deeper in mod-105) |  |               |         |
| Policy-after-rollout retrofit   | Full seven-artifact set co-signed before launch (Chapter 03); strictly, the use policy, data-handling SOP, and escalation path |     |               |         |
| Other — <name>                  | <name artifact or module that would have preempted it> |                              |               |         |
```

Fill in the three right-hand columns for each row. Specific moves:

1. **"Current state" is honest.** If the artifact is a stub drafted by you but not co-signed by governance, say "stub — not co-signed." If it does not exist, say "absent." The whole point of Chapter 05 is to make the absence visible before Stage 3 closes, not to let it slide.
2. **"Owner" is a named role, not "the CoE".** Chapter 05's attendee list names the governance representative, the champion lead, and the sponsoring BU owner — any of them may be the right owner for a given preempting artifact.
3. **"By when" is dated against the rollout calendar.** If the artifact is absent and the rollout launches in three weeks, "by when" is not "soon." Chapter 05: "If the artifact does not exist yet, Stage 3 has not cleared."

**Checkpoint 4:**

- [ ] Every cluster has a preempting artifact named; the Chapter 03 artifact set is referenced by name for the four Chapter 05 failure modes.
- [ ] "Current state" is honest — stubs are called stubs, absences are called absent.
- [ ] Every "by when" is a date against the rollout calendar, not an aspirational "soon."

---

## Step 5 — Produce and sign the one-page pre-mortem (write-up)

Chapter 05's write-up format: one page, three sections — *what we think will kill it*, *the preempting artifacts and owners*, *the commit*. Sign it. File it next to the service-catalog entry.

Build the signed one-page pre-mortem in a dedicated section of the file:

```markdown
## The signed one-page pre-mortem

**Rollout:** <org / tool / cohort>
**Stage 3 gate target date:** <date>

### What we think will kill it

Three sentences, each the most specific exemplar from its cluster (selected by the facilitator from the Step 3 captures):

1. "Six months from now, this rollout failed because <sentence from cluster 1>."
2. "Six months from now, this rollout failed because <sentence from cluster 2>."
3. "Six months from now, this rollout failed because <sentence from cluster 3>."

### The preempting artifacts and owners

| Failure | Preempting artifact | Owner | By when |
|---------|---------------------|-------|---------|

(Copy the matching rows from Step 4. One row per sentence above.)

### The commit

Signed by:
- AI Enablement Lead (facilitator)
- Sponsoring BU owner
- Champion lead
- Governance representative
- Skeptic (named — required; the skeptic signing is the whole point)

**Stage 3 gate status after this pre-mortem:**
- [ ] Cleared — all preempting artifacts exist and are signed by their named owners.
- [ ] Not cleared — <artifact name> is absent or unsigned; Stage 3 does not open until <by-when date>.

**Filed at:** `<path next to the service-catalog entry for this rollout>`
```

Pick the three sentences from the Step 3 captures that are the most specific exemplars of their clusters — not the three sentences you personally wrote in Step 2 as the facilitator. The facilitator's job is to let the sharpest sentence in the room land on the page; "my sentences made the cut" is a signal you have not actually let the quiet skeptic's view land.

**Checkpoint 5:**

- [ ] The three sentences are selected from Step 3's captures and are the most specific exemplars of their clusters — not your own facilitator sentences and not a paraphrase.
- [ ] The commit section has five signature slots and names the skeptic as one of them.
- [ ] The "Stage 3 gate status" line is explicit about cleared or not cleared; no soft-landing language.

---

## Step 6 — 15-minute debrief (after the timer)

Write a short debrief section answering these four prompts. Each is one or two sentences. The debrief is the part of the lab that compounds — the real meeting's quality is downstream of the facilitator reflexes you build in the debrief.

```markdown
## 15-minute debrief — what I learned about the meeting

1. **Which attendee was hardest to write in character for, and why?**
   <answer>
2. **Which sentence came closest to the "adoption was slower than expected" trap, and what moved it off the trap?**
   <answer>
3. **Which Chapter 03 artifact did I discover is weaker in my rollout than I thought — and what is the one thing I would do on Monday to shore it up?**
   <answer>
4. **In a real meeting, where is this dry-run likely to break first?** (Common answers: silent writing is cut short, verbatim capture becomes paraphrase, the skeptic is not actually in the room.)
   <answer>
```

**Checkpoint 6:**

- [ ] All four prompts answered.
- [ ] Prompt 3 names a specific artifact and a specific Monday action, not an abstraction.

---

## Deliverable

- `pre-mortem-dry-run.md` — the open script, the fifteen silent-writing sentences, the clustering table, the artifact-and-owner table, the signed one-page pre-mortem, and the four-prompt debrief.

## Expected output shape

Roughly 2–3 pages of markdown. Fifteen first-person sentences visible, four-mode clustering table filled, artifact-and-owner table filled, signed one-page pre-mortem at the bottom, debrief below it. The meeting fits in 45 minutes; the write-up and debrief together push to 60. If you went longer, note the overrun in the debrief as signal for the real meeting.

## Checkpoint — self-evaluation

- [ ] The prompt used is verbatim from Chapter 05.
- [ ] Fifteen sentences are written in five first-person voices; the skeptic's three sound meaningfully different from the sponsor's three.
- [ ] No sentence survives in a shape resembling "adoption was slower than expected," "the vendor underdelivered," or "the business was not ready." If one does, re-write.
- [ ] The clustering table has at least three of the four Chapter 05 failure modes populated.
- [ ] The artifact-and-owner table names an owner by role (not "the CoE") and a date against the rollout calendar (not "soon") for every cluster.
- [ ] The signed one-page pre-mortem selects the three sentences from Step 3 captures, has a five-signature commit block, and states Stage 3 gate status explicitly.
- [ ] The debrief names a specific artifact to shore up and a specific Monday action.

## Common failure modes

- **Skipping the silent writing.** Chapter 05's whole technique rests on it. In a solo dry-run the temptation is to write all five attendees' sentences in a batch. Resist — set the three-minute timer per attendee and write in character.
- **The skeptic sounds like the sponsor.** If this happens, you were not in character. The skeptic in a real meeting is often the quietest person in the room, with the sharpest sentence. Re-do Step 2 for that attendee.
- **Clustering before capture.** Chapter 05 is explicit: capture verbatim first, cluster as you go. In practice, novice facilitators paraphrase into cluster-friendly language in real time, and the specificity that makes the pre-mortem useful gets lost. Capture the sentence, then cluster.
- **Letting "by when" slide to "soon."** The whole point of Chapter 05 is to make Stage 3 gate status concrete. "Soon" is the shape of language that lets Stage 3 close with absent artifacts.
- **Making yourself the owner of every preempting artifact.** Chapter 03's signing surface is the point; this role convenes, does not solely author. If your artifact-and-owner table has you as owner of all five rows, the pre-mortem has quietly re-centralized the work and you have missed the chapter's central move.

## What this prepares you for

The pre-mortem is the single highest-leverage 45 minutes of the Stage 3 gate. In the real role, you will run one of these before every pilot-to-rollout commit, and the first time you do it you will discover how much of the technique lives in the facilitator discipline, not in the three-sentence prompt. Running the dry-run once with the timer on — against your own rollout, in character, signing the write-up — is the cheapest version of that discovery. In production, this lab's output composes directly into the Stage 3 one-pager (Exercise 01 / Lab 01) and into mod-109's incident-response priors.
