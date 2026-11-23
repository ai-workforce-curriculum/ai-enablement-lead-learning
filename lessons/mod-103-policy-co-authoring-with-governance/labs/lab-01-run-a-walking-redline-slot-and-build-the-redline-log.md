# Lab 01 — Run a Walking-Redline Slot and Build the Redline Log

**Duration:** 60–75 minutes
**Format:** guided solo dry-run — you play the enablement drafter *and* one named governance partner across a 30-minute walking-redline slot, producing the redline-log rows the slot generates
**Grounding chapters:** [01 — The Co-Author Posture and the Redline Log](../01-the-co-author-posture-and-the-redline-log.md), [04 — The One-Page Acceptable-Use Policy](../04-the-one-page-acceptable-use-policy.md), [05 — The Data-Handling SOP](../05-the-data-handling-sop.md)

## Objective

Simulate a single 30-minute **walking-redline slot** end-to-end and produce the **three to eight redline-log rows** Chapter 01 names as the per-slot output. The redline log — not the signed PDF — is the artifact that proves co-authoring happened; this lab builds the muscle for producing those rows under the time constraint of a real slot, before you sit one with a real partner.

This lab is not Exercise 01 (which produces the AUP draft) or Exercise 02 (which produces the SOP draft). Those exercises produce the document the slot redlines *against*. This lab operates one layer out — the thirty minutes in which the document becomes co-authored and the log that proves it.

## Prerequisites

- Chapter 01 read end to end, especially the *Cadence — the walking redline* and *The redline log* sections.
- Chapter 04 or Chapter 05 read, depending on which draft you choose to redline against.
- A draft to redline. In order of preference:
  - Your Exercise 01 AUP draft, if you have one.
  - Your Exercise 02 SOP draft, if you have one.
  - A short stub (6–8 sentences) you write before starting, naming the tool, three approved uses, two prohibited uses, and one data-class rule. The lab works at this scale; the slot cares about the flow, not the length of the input.
- A chosen partner persona to play. Pick exactly one for this slot:
  - **Counsel (data-protection practice)** — redlines legal hooks vs. opinions, retention language, jurisdictional naming.
  - **CISO delegate** — redlines claims about technical controls (DLP, tenancy, logging), retention / egress language the controls have to actually enforce.
  - **DPO / privacy** — redlines data-class mappings, examples drawn from real cohort work, retention statements and data-subject-rights touchpoints.
- A timer (phone, watch). The 30-minute slot is the lab's frame; hold yourself to it.
- A single markdown file.

## Why a lab, not an exercise

Exercises 01 and 02 answer *what belongs on the page*. This lab answers *what happens in the thirty minutes when a governance partner redlines the page and the two of you negotiate language into the log in real time*. Those are different failure modes: the first fails as thin content; the second fails as a slot where the two sides arrive, chat for twenty-five minutes, and leave with a shared sense of alignment and nothing durable on paper — Chapter 01's **no-artifact** failure posture.

A solo dry-run with the timer on is the cheapest way to build the slot-facilitation muscle before the real meeting, where pausing to re-read the chapter is not an option.

## Setup

Create `walking-redline-slot.md` with this skeleton:

```markdown
# Walking-Redline Slot — <tool> / <organization>

**Date of dry-run:** <today>
**Document under redline:** <AUP draft | SOP draft | stub> — path or inline below
**Drafter:** AI Enablement Lead (me)
**Partner (persona played by me for this slot):** <counsel | CISO delegate | DPO>
**Slot length:** 30 minutes (Chapter 01 default)
**Walking-redline cycle this is in:** slot <N> of a 4–6-slot cycle

## Document (or inline stub)

<entries>

## Slot script — minute by minute

<entries>

## Redline log — rows produced in this slot

<entries>

## Debrief — what the slot taught me

<entries>
```

Set your timer and start.

---

## Step 1 — Minutes 0–3: the open (3 min on your timer)

Write the open you would say as the drafter at the start of the slot. Chapter 01 frames the walking redline as "the current draft on screen and the redline log open." The open names what the partner is being asked to do and what they are *not* being asked to do.

Add the open to your file:

```markdown
**Open (drafter says):** "We have 30 minutes. The draft is on screen; the redline log is open next to it. I am asking you to redline — your language on the parts you own; your questions on the parts you do not — and we land each change as a row in the log as we go. I am not asking for sign-off today; that lands at the end of the cycle after four to six of these."
```

Chapter 01: a walking-redline slot ends with "three to eight rows in the log"; four to six slots produce a ratification-ready draft. State the cycle math in the open so the partner is not pricing a one-shot approval.

**Checkpoint 1 — do not proceed until all three are true:**

- [ ] The open script explicitly separates "what I am asking for" (redlines) from "what I am not asking for" (sign-off).
- [ ] The open names the slot as one of a 4–6-slot cycle — Chapter 01's cadence.
- [ ] Time on the clock is still under three minutes. Opens that stretch to five minutes eat the slot.

---

## Step 2 — Minutes 3–25: run the redlines in character (22 min)

For the next twenty-two minutes, play your chosen partner. The discipline is that you redline *as the partner*, not as yourself-dressed-as-partner. The point of the lab is to feel the specificity of each partner's language.

Work in this loop, repeating for each redline the partner would make. Target three to eight rows total — Chapter 01's slot-output count.

1. **Read a sentence of the draft out loud.** Not silently — the partner's redline reflex fires on how the sentence *sounds* against their vocabulary.
2. **Decide whether the partner would redline it.** If yes, what specifically — the data class is not quite right, the retention claim doesn't match the controls, the legal-opinion phrasing needs to become a hook, the jurisdictional naming is vague. If no, move on; the partner does not redline every sentence.
3. **Write the row in the log.** Use Chapter 01's minimum-viable structure — Date / Document / Section / Partner / Before / After / Rationale / Resolution.
4. **Move to the next sentence.**

Add rows to the log table:

```markdown
## Redline log — rows produced in this slot

| Date | Document | Section | Partner | Before | After | Rationale | Resolution |
|------|----------|---------|---------|--------|-------|-----------|------------|
|      |          |         |         |        |       |           |            |
```

Guidance on writing in character for each partner persona:

- **Counsel (data-protection practice).** Counsel redlines the *shape* of a sentence as much as its content. A sentence that reads "This would violate GDPR" — even in a hooks-only AUP — is a redline target, not because counsel disagrees with the claim but because the sentence is in counsel's voice, not yours; the fix is to cut the opinion and leave only the hook (the data class, the jurisdiction, the counterparty) that counsel attaches an opinion to. Chapter 04 and Chapter 07 both name this discipline.
- **CISO delegate.** Security redlines any sentence that implies a control exists when the control has not actually been configured. "DLP will flag the data class" is a redline target if DLP has not yet been scoped for this tool. The security redline also tightens retention language — vendor retention vs. internal retention, abuse-monitoring retention vs. model-training retention — because sloppy conflation here is what breaks the SOP in practice.
- **DPO / privacy.** Privacy redlines data-class language. "Customer PII" is a redline target without a named scheme; the fix is to pin the class to the organization's named classification scheme and name two or three concrete examples drawn from the cohort's real work. Privacy also redlines any retention statement that does not reference the vendor DPA or that restates the DPA inline (restatement is Chapter 05's warned-against double-source-of-truth pattern).

**Rationale is the row that teaches.** Chapter 01: the rationale column is "the partner's reason in their own language." Example: "Privacy: the current example (customer name in support transcript) is good, but add a counter-example (product SKU — not PII) so operators have the pattern-match surface for a class, not just the class itself." Future heads of governance read the rationale to understand *why* the clause ended up where it did; a rationale that reads "cleaned up" tells them nothing.

**Resolution is a tag, not prose.** One of `accepted`, `revised` (with a pointer to the final text), `escalated` (with who it escalated to — e.g., *"escalated to head-of-ai-governance for cycle-level call on legal-hook boundary"*), or `declined` (with reason). A row with no resolution becomes a stale redline that resurfaces every refresh cycle.

**Checkpoint 2:**

- [ ] Between three and eight rows produced — Chapter 01's slot output. Fewer than three usually means the partner was not in character; more than eight usually means the slot has stretched past 30 minutes.
- [ ] Every row's rationale is in the partner's voice, not a paraphrase of the before-and-after. "Cleaned up" is a disqualifying rationale.
- [ ] Every row has a resolution tag (`accepted` / `revised` / `escalated` / `declined`).
- [ ] At least one row is an `escalated` or `declined` resolution. A slot where every row is `accepted` was almost certainly a hand-off dressed up as a redline.

---

## Step 3 — Minutes 25–28: name the next slot (3 min)

The walking-redline cycle is 4–6 slots; the current slot's close names the next slot. Write a two-line close in your file:

```markdown
**Close (drafter says):** "That's seven rows in the log. Next slot I'd like <specific thing>. I'll send the updated draft by <date>; the log stays open as we go."
```

The "specific thing" names which partner is next (counsel after privacy, because the privacy redlines opened three new legal hooks; security after counsel, because the retention clause now carries legal language that security has to confirm maps to the actual controls), and names the section the next slot focuses on.

**Checkpoint 3:**

- [ ] The close names a specific next partner and a specific section — not "we'll keep working on it."
- [ ] The close is two lines or fewer. A long close means the slot overran.

---

## Step 4 — Minutes 28–30: file the log and the delta (2 min)

Chapter 01: "Keep the log in the same repository as the draft. Not in a separate ticketing system. Not in a shared drive the next head of governance cannot find."

Add a short filing line:

```markdown
**Filed at:** `<repo-path>/policies/<tool>/redline-log.md` — version `slot-<N>`
**Draft updated:** `<repo-path>/policies/<tool>/<aup|sop>.md` — the After-column text has been merged in; each merged redline carries a reference to its log row.
```

The two-sided discipline: the log row points at the draft section; the draft section points back at the log row. The pair is what makes the audit story readable in a year.

**Checkpoint 4:**

- [ ] The log and the draft live at parallel paths in the same repo.
- [ ] Each merged redline in the draft points back at its log row (even if only as a `<!-- redline-log: row 3 -->` comment inline for the lab).

---

## Step 5 — 15-minute debrief (after the timer)

Write a short debrief answering these four prompts. One or two sentences each. The debrief is the part of the lab that compounds.

```markdown
## Debrief — what the slot taught me

1. **Which redline was hardest to write in character — and why?**
   <answer>
2. **Which row's rationale came closest to the "cleaned up" trap, and what moved it off the trap?**
   <answer>
3. **Which failure posture from Chapter 01 (hand-off / abdication / no-artifact) was the slot most at risk of sliding into, and what prevented it?**
   <answer>
4. **In a real slot, where is this dry-run likely to break first?** (Common answers: the partner's rationale gets paraphrased into drafter voice, the resolution column is skipped, the slot overruns past 30 minutes, the log and the draft drift out of sync.)
   <answer>
```

**Checkpoint 5:**

- [ ] All four prompts answered.
- [ ] Prompt 3 names a specific failure posture and a specific thing that prevented it in the slot.

---

## Deliverable

- `walking-redline-slot.md` — the open script, the slot script (minute-by-minute), the redline log with 3–8 rows, the close script, the filing lines, and the four-prompt debrief.

## Expected output shape

Roughly 1.5–2 pages of markdown. 3–8 rows visible in the log; each row has a specific Before / After / Rationale / Resolution. At least one `escalated` or `declined` resolution. The slot fits in 30 minutes; the debrief adds another 15.

## Checkpoint — self-evaluation

- [ ] The open script separates "redlines" from "sign-off" and names the 4–6-slot cycle.
- [ ] 3–8 rows produced; each row has all eight log columns populated.
- [ ] Rationale column is in partner voice, not drafter voice. "Cleaned up" does not appear anywhere.
- [ ] At least one row is `escalated` or `declined`; not all rows are `accepted`.
- [ ] The close names a specific next partner and a specific section.
- [ ] Log and draft live at parallel paths in the same repo; each merged redline points back at its log row.
- [ ] The debrief names a specific failure posture (hand-off / abdication / no-artifact) the slot was at risk of sliding into.

## Common failure modes

- **Running the slot as one long monologue.** Chapter 01 names long-meeting co-authoring as low-hit-rate. The walking redline is 30 minutes, with the draft on screen and the log open; if the dry-run stretches past 45, you have fallen into the long-meeting shape the chapter is refusing.
- **Rationale paraphrased into drafter voice.** The log row's job is to carry the partner's reason in their language for the next head of governance who reads it. "Cleaned up the retention language" is drafter voice; "Privacy: the vendor retention statement needed the abuse-monitoring clock named separately from the model-training clock — the two drift by a quarter and operators conflate them" is partner voice.
- **Every resolution is `accepted`.** A slot without any `escalated` or `declined` row is almost always a hand-off wearing redline clothes. The partner that redlines a draft always finds at least one thing worth escalating or declining; a slot that produces only acceptances has probably not surfaced the hard questions.
- **Skipping the Before / After columns.** Chapter 01 is explicit: "Before / After capture the exact text that changed — not a summary." A row that says "revised retention section" is a stale row the next refresh cycle will start the same conversation against.
- **The log lives in the ticketing system; the draft lives in the repo.** Chapter 01 flags this as the specific anti-pattern that strands the log where the next head of governance cannot find it. Same repo, parallel paths.

## What this lab prepares you for

Walking redlines are the recurring cadence of the role — four to six slots per co-authoring cycle, several cycles per quarter at a mature CoE. The first time you sit one with a real partner, the pressure is on your facilitator discipline, not on your drafting; the row-shape and the rationale voice are what carry the log forward through personnel changes. Running one slot cold in this lab, with the timer on and one partner in character, is the cheapest version of that discovery. In production, this lab's output composes directly into the signing-ready draft Exercise 01 or Exercise 02 produces — the exercises write the document; this lab writes the evidence that the document was co-authored.
