# Lab 03 — Red-Team Three Executive Paragraphs Against the Theatre Patterns and the Structural Moves

**Duration:** 60–75 minutes
**Format:** guided hands-on — diagnosis drill + rewrite + self-red-team pass
**Grounding chapters:** [03 — Writing for Executives — Board Updates, LT Briefings, Strategic Memos](../03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md), [02 — Authoring the Executive Scorecard — Weekly, Monthly, Quarterly](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md)

## Objective

Drill the diagnosis-and-rewrite reflex on three short executive-facing paragraphs. Each is a draft that landed on your desk from the exec sponsor's EA (or from a previous version of you in a hurry) ahead of a board update, an LT briefing, and a strategic memo. The lab is to name which Chapter 03 **theatre failure mode** each paragraph carries (engagement lede, strategy abstraction, vendor voice), which of the three **structural moves** is broken (BLUF, misses-in-the-lead, confidence bands), and to rewrite each paragraph into one that would read as a program operating with its eyes open. The repeated small-unit drill is how the Chapter 03 moves stop being a checklist you reach for and start being a reflex that catches drift as you draft.

## Prerequisites

- [Chapter 03](../03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) read, with the three executive artifacts, the three structural moves, and the three theatre failure modes close enough to name without the chapter in hand.
- [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) read, with the five-part miss narrative structure and the misses-first discipline available.
- A blank working file — `exec-paragraph-redteam.md`.

## Why a lab, not an exercise

[Exercise 03](../exercises/exercise-03-quarterly-board-ready-review-outline.md) produces the one-page executive summary that opens the quarterly review — positive output, roughly 350–500 words, written under the BLUF discipline. [Exercise 04](../exercises/exercise-04-metric-miss-narrative-drill.md) drills the miss narrative at scorecard altitude (Section 3 of the deep-dive), not at executive-communication altitude. Neither exercise drills the diagnostic reflex on *drafts that have already failed* — paragraphs that have slid into one or more of Chapter 03's theatre patterns and need to be caught before they ship. This lab is that drill. The failure case is where the structural moves and the theatre pattern names earn their keep; drilling it three times across three different draft shapes is how the reflex gets wired. By the end of the lab, a thin BLUF in your own next draft reads to you the same way a type error reads to a compiler.

## Setup

Open `exec-paragraph-redteam.md` and paste this skeleton. You will fill it in as you walk Steps 2 through 5.

```markdown
# Executive Paragraph Red-Team — v0.1

**Reviewer:** AI Enablement Lead — <your-name>
**Review cadence:** on every executive-facing draft before co-authoring with the sponsor.

## 1. The three drafts (verbatim, as received)

<paste Draft A, Draft B, Draft C from Step 1>

## 2. Draft A — board update opening
### 2.1 Diagnosis
### 2.2 Rewrite
### 2.3 Self-red-team

## 3. Draft B — LT briefing BLUF
### 3.1 Diagnosis
### 3.2 Rewrite
### 3.3 Self-red-team

## 4. Draft C — strategic memo to the CFO
### 4.1 Diagnosis
### 4.2 Rewrite
### 4.3 Self-red-team

## 5. Reflection
```

---

## Step 1 — Read the three drafts (5 min)

Copy the three drafts verbatim into Section 1 of your working file. Read them once through without annotating. Ask yourself, after each: *what would a VP who has run programs before notice in the first sentence?* Note the answer in one line under each draft; do not yet diagnose.

### Draft A — the opening paragraph of a board update

> The AI-powered productivity tools we have deployed this year have now reached 78% of the workforce, representing a transformative milestone in our organization's digital transformation journey. Our generative AI platform has driven meaningful adoption across every business unit, and vendor benchmarks suggest we are tracking ahead of the industry average on time-to-value. We remain confident in the strategic trajectory and look forward to continuing to drive AI-powered productivity across the enterprise.

### Draft B — the BLUF paragraph of an LT briefing

> In Q3 we continued to execute on our AI enablement roadmap, delivering against a majority of our commitments and advancing our strategic priorities across the portfolio. The program has driven productivity improvements on the order of 22% in core workflows and is positioned well heading into Q4. We are requesting leadership support to continue the current trajectory.

### Draft C — the second paragraph of a strategic memo to the CFO on the drafting-workflow rollout

> The Legal drafting rollout faced some headwinds this quarter but we remain on track to deliver value. Early feedback has been positive overall and the team is working through implementation refinements. Vendor data shows a 55.8% median reduction in task completion time for coding workflows, which gives us confidence that drafting workflows will see similar impact as the rollout matures. We anticipate full return on investment within the next few quarters.

### Checkpoint 1 — before Step 2

- [ ] All three drafts are pasted verbatim into Section 1 of your working file.
- [ ] You have one line of first-impression notes under each draft (what a VP who has run programs before would notice in the first sentence).
- [ ] You have *not* yet applied the Chapter 03 vocabulary — the diagnosis happens in Step 2.

---

## Step 2 — Draft A — board update opening: diagnose, rewrite, self-red-team (15 min)

### 2.1 Diagnosis

In Section 2.1 of your file, walk Draft A through three diagnosis questions:

1. **Which of the three Chapter 03 theatre failure modes does it carry?** Name every pattern that applies; a paragraph can carry more than one. For each, cite the specific phrase that triggered the diagnosis.
   - *Engagement lede* — does the first sentence open with a usage number or an adoption percentage? Chapter 03: "The first paragraph of the board update … opens with a usage number. 'The AI tools we deployed this year have reached 78% of the workforce.' This is the mod-102 Chapter 04 adoption-percentage failure in executive-communication dress."
   - *Strategy abstraction* — does the paragraph end with a non-falsifiable commitment ("continue to drive … across the enterprise")? Chapter 03: "No specific commitment is made. 'We will continue to drive AI-powered productivity across the enterprise.' This is not a sentence an executive can act on."
   - *Vendor voice* — do phrases from vendor marketing appear ("AI-powered," "generative AI platform," "transformative milestone," "digital transformation journey")? Chapter 03: "Phrases from vendor marketing material appear … 'generative AI platform,' 'transformative productivity gains.' The sentences are indistinguishable from a vendor whitepaper."
2. **Which of the three Chapter 03 structural moves is broken?**
   - *BLUF* — does the first paragraph state the finding, the ask, and the confidence? If no number against target, no ask, and no confidence appears in the lead, BLUF is broken.
   - *Misses-in-the-lead* — if Q3 had a miss (and most quarters have one), is it in the lead or buried?
   - *Confidence bands* — do the quantitative claims carry a band or appear as point estimates with no methodology?
3. **Which Chapter 02 miss-section failure mode shows up (if any)?** Euphemism ("headwinds"), scope-swap (re-targeting silently as success), attribution flight ("the BU's lack of readiness").

Write the diagnosis as a short paragraph, three to six sentences, that names each pattern and cites the phrase. A diagnosis that says "this is bad" without naming the pattern is not the drill.

### 2.2 Rewrite

In Section 2.2, rewrite the opening paragraph. The rewrite must:

- Open with the primary outcome against the Q3 target (not a usage percentage). If no primary outcome against target can be named, the program has a scorecard problem, not a writing problem; name that in the paragraph.
- Carry a confidence band on the headline number (Chapter 03's third structural move).
- If Q3 had a miss, put the miss in the lead or in the first body sentence (Chapter 03's misses-in-the-lead move).
- End with a specific, measurable, date-anchored commitment (Chapter 03's remediation for the strategy-abstraction pattern).
- Use the organization's own language — no vendor marketing phrases.

Keep the rewrite under 120 words. A board-update opening paragraph that is longer is drifting toward the body.

Example of what a rewritten Draft A opening *shape* looks like (the values are illustrative — your own portfolio produces different numbers):

> In Q3, the AI enablement program's primary productivity outcome — median time-to-first-draft across drafting rollouts — moved 11% against a 30% quarterly target (90% CI 6–17%, measured on the 180-operator pilot cohort). The shortfall is concentrated in new-matter drafting; retained-client advisory moved 24%. We are asking the board to endorse the Q4 re-scope of the drafting rollout to retained-client advisory and a Stage 2 selection re-examination for new-matter drafting, with a mid-quarter decision review at week 6. Confidence is high on the diagnosis; confidence is lower on the re-scope hitting target in Q4.

### 2.3 Self-red-team

In Section 2.3, read your rewrite aloud and check it against three questions:

- Does the first sentence state the primary outcome against target, with a confidence band?
- Is the miss in the lead, not buried?
- Is the closing commitment specific, measurable, and date-anchored?

Fix any `<!-- fix: ... -->` notes before moving on.

### Checkpoint 2 — before Step 3

- [ ] Section 2.1 names at least two Chapter 03 theatre patterns by name, each with the specific phrase that triggered the diagnosis.
- [ ] Section 2.2 is under 120 words, opens with an outcome-against-target, and ends with a specific commitment.
- [ ] Section 2.3 catches at least one `<!-- fix: ... -->` on first read-aloud; a rewrite that passes clean on the first self-red-team was not red-teamed hard enough.

---

## Step 3 — Draft B — LT briefing BLUF: diagnose, rewrite, self-red-team (15 min)

Draft B is subtler than Draft A — no vendor marketing phrases, no adoption percentage in the lead. The failure is quieter; it is Chapter 03's strategy-abstraction pattern operating at BLUF altitude, dressed up in competent-sounding language.

### 3.1 Diagnosis

Walk Draft B through the same three diagnosis questions as in Step 2.1. Specifically check:

- **Strategy abstraction.** "Continued to execute on our AI enablement roadmap," "delivering against a majority of our commitments," "advancing our strategic priorities." What specific commitment does this sentence state that a VP could approve, challenge, or track against? If none, this is the Chapter 03 pattern — abstraction protects the writer over one quarter and erodes credibility over four.
- **BLUF discipline.** Chapter 03's three-sentence BLUF: (1) finding, (2) ask, (3) confidence. Which of those three elements is actually in Draft B's three sentences? "Requesting leadership support to continue the current trajectory" — what decision, by when, from whom?
- **Confidence bands.** "Productivity improvements on the order of 22% in core workflows." Is there a confidence band on the 22%? Is "core workflows" an auditable cohort, or portfolio-aggregation sleight-of-hand ([Chapter 01](../01-the-measurement-stack-at-org-scope.md) category-error pattern)?
- **Misses-in-the-lead.** "Delivering against a majority of our commitments" — what is the shape of the minority that did not deliver? If any part of the portfolio missed, where is the miss?

### 3.2 Rewrite

Rewrite Draft B as a BLUF paragraph that carries the three sentences Chapter 03 names:

- *Finding* — the headline outcome(s) against target, named explicitly, with a confidence band and a named cohort/denominator.
- *Ask* — the specific decision or alignment being requested, with a decision owner and a decision-by date.
- *Confidence/caveat* — how certain you are, and the main risk or unknown.

If Q3 had a dominant miss, the miss belongs in the finding sentence or the one immediately after. Keep the rewrite to four sentences and under 150 words — an LT-briefing BLUF that is longer rewrites itself into talking points that lose the structure (Chapter 03's drafting-rhythm note on slide decks).

### 3.3 Self-red-team

In Section 3.3, check:

- Each of the BLUF's three sentences carries its named load — finding, ask, confidence.
- The 22% (or your equivalent portfolio number) carries a confidence band *and* a named cohort or denominator. "Core workflows" without a defined cohort is portfolio sleight-of-hand.
- The ask has a named decision owner and a decision-by date; "leadership support" without a name and a date is a missed ask.
- If a miss is in the portfolio, it appears in sentence 1 or 2.

### Checkpoint 3 — before Step 4

- [ ] Section 3.1 names the strategy-abstraction pattern explicitly and cites the phrase.
- [ ] Section 3.2 is four sentences or fewer, under 150 words, and carries all three BLUF loads.
- [ ] The ask sentence has a name and a date; vague leadership-support is flagged as a `<!-- fix: ... -->` and resolved before shipping.

---

## Step 4 — Draft C — strategic memo to the CFO: diagnose, rewrite, self-red-team (15 min)

Draft C is a memo to the CFO on the Legal drafting rollout's Q3 performance. The underlying situation, per the module's worked example: Q3 target 30% reduction in time-to-first-draft, actual 11% reduction, diagnosis workflow-fit issue in new-matter drafting confirmed in 6 of 8 interviews. The draft hides this behind euphemism and borrows a vendor-whitepaper number.

### 4.1 Diagnosis

Walk Draft C through the diagnosis. Expected findings — your own write-up should cite the phrases:

- **Euphemism.** "Faced some headwinds this quarter but we remain on track to deliver value" — Chapter 02's named miss-section failure mode. The metric missed by 19 percentage points against target; "headwinds" and "remain on track" together are the pattern.
- **Attribution flight.** If the draft reaches for external causes or omits the diagnosis, the Chapter 02 third failure mode is in play.
- **Vendor voice** and **vendor-number headline.** "Vendor data shows a 55.8% median reduction in task completion time for coding workflows, which gives us confidence that drafting workflows will see similar impact" — this is simultaneously the Chapter 03 vendor-voice pattern, the Chapter 01 vendor-number-headline pattern (transplanting a published number across task — coding to drafting — and across population), and the Chapter 05 reverse-engineered-ROI tell ("gives us confidence" is the authorial move that justifies a number not yet in evidence).
- **Strategy abstraction** on the forward-looking commitment. "Anticipate full return on investment within the next few quarters" — no specific number, no specific date, no confidence band. Chapter 03 names this as the pattern that erodes credibility across quarters; Chapter 05's compounding-ROI-forever pattern is in the neighbourhood.
- **BLUF, missing.** A memo to the CFO on a specific decision is a Chapter 03 strategic-memo artifact; its first paragraph is a BLUF. Draft C's first paragraph buries the actual miss.

### 4.2 Rewrite

Rewrite the paragraph as the second paragraph of a strategic memo to the CFO. The rewrite must:

- State the miss in plain numbers, in one sentence. "Q3 target was 30% median reduction in time-to-first-draft on retained-client advisory; actual was 11% (90% CI 6–17%, n=174 associates, 12 weeks)." This is the Chapter 02 five-part structure's *target* and *actual* lines compressed into one sentence for executive length.
- Name the diagnosis in the next sentence, with the qualitative evidence density ("confirmed in 6 of 8 interviews with senior associates in the new-matter cohort"). This is the Chapter 02 five-part structure's *why* line at executive altitude.
- Name the intervention — the re-scope to retained-client advisory for Q4 with a named owner and decision-by date. The Chapter 02 *what is being done* line.
- End with the program-level *learned* line — the one sentence that teaches at the program level, not the rollout level. Chapter 02 names this as the most important sentence in the miss narrative; a strategic memo to the CFO is the single place outside the deep-dive where it must appear.
- Remove the vendor-number borrow entirely. If the methodology reference belongs anywhere, it is a methodology-appendix line citing *method* (pre-registered primary outcome, longitudinal observation from [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md)), not a number.
- Carry a confidence band on any quantitative claim.

Keep the rewrite to 150–200 words. A memo to the CFO on a specific miss, if longer, is reaching for cover.

### 4.3 Self-red-team

In Section 4.3, check:

- No phrase from the original ("headwinds," "remain on track," "gives us confidence," "within the next few quarters") survives into the rewrite.
- No vendor-reported productivity number appears.
- The *learned* line names a program-level change — a new rule for pilot design, a new interview question, a new attribution check — not a rollout-level correction.
- The intervention has a named owner (role is fine; name is better) and a date.
- The miss is in the lead; the rewrite does not open with hits to cushion the miss.

### Checkpoint 4 — before Step 5

- [ ] Section 4.1 names euphemism, vendor voice, vendor-number headline, and strategy abstraction explicitly, each with the citing phrase.
- [ ] Section 4.2 is 150–200 words, opens with the miss in plain numbers, and ends with a program-level learned line.
- [ ] Section 4.3 confirms no vendor-reported productivity number and no original euphemism phrase survived.

---

## Step 5 — Reflection (5 min)

In Section 5, write five to seven sentences on the drill itself:

- Which of the three drafts was hardest to rewrite honestly, and why. Candidates: Draft A (the vendor-voice pull is strong when the source material is polished); Draft B (strategy abstraction is quiet, and "delivering against a majority" sounds competent); Draft C (the learned line is the single hardest sentence in the module and this is the drill where it lands).
- One Chapter 03 pattern you expect to catch yourself writing *first* in your own next draft. Chapter 03's point is that the patterns feel natural while you draft; naming your own drift pattern here is how it becomes visible.
- One Chapter 02 or Chapter 05 cross-reference you drew on during the rewrite. (Draft C's rewrite leans on Chapter 02's five-part miss narrative; Draft C's diagnosis leans on Chapter 05's reverse-engineered-ROI; Draft B's rewrite leans on Chapter 02's BLUF three-sentence structure.)
- One editorial move in your rewrites you expect the sponsor to push back on when the drafting-rhythm from Chapter 03 kicks in (week 12 edits). Candidates: the miss in the lead ("we should soften this"), the confidence band ("we don't need to show uncertainty to the CFO"), the removal of the vendor number ("but it's a real number"). Name the pushback and the Chapter 03 principle you would ground the push-back-to-the-pushback in.

### Checkpoint 5 — before shipping

- [ ] Section 5 names the hardest draft and why — a one-line "all three were hard" fails the reflection.
- [ ] Section 5 names your own expected drift pattern. The pattern is the one you expect to re-encounter in a real draft next month.
- [ ] Section 5 names one editorial move you expect sponsor pushback on, with the principle you would ground the defence in.

---

## Deliverables

- `exec-paragraph-redteam.md` — Sections 1 through 5 filled: the three drafts verbatim in Section 1; diagnosis, rewrite, and self-red-team for each draft in Sections 2, 3, 4; reflection in Section 5.

## Checkpoint — self-evaluation

- [ ] Each diagnosis names the Chapter 03 theatre patterns by name *and* cites the specific phrase that triggered the diagnosis.
- [ ] Each rewrite satisfies BLUF (where applicable), misses-in-the-lead (where applicable), and confidence bands (where a number appears).
- [ ] No vendor-reported productivity number appears in any rewrite.
- [ ] Draft C's rewrite ends with a program-level *learned* line, per Chapter 02's miss-narrative discipline.
- [ ] Section 5 names your own expected drift pattern and one expected sponsor pushback with a principled defence.

## What this lab prepares you for

Exercise 03's one-page executive summary and Exercise 04's miss narratives are the positive-output drills; this lab is the diagnostic one that catches the drafts those exercises would ship if you wrote them under calendar pressure without reading your own prose critically. The co-authoring rhythm from Chapter 03 (week 10 headline alignment, week 11 draft, week 12 sponsor edits) only works if the lead's first draft is already past the three theatre patterns; this lab is the drill that gets you to that first draft faster. Over time, re-running the lab with new drafts (your own, a peer's, a prior quarter's artifact for review) is one of the few repeatable mechanisms that keeps executive-writing craft from decaying between quarterly reviews.
