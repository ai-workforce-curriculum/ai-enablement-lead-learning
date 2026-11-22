# Quiz 01 — Selection, Pilots, Rollout Artifacts, Measurement, and the Pre-Mortem

**Format:** multiple choice · **Questions:** 12 · **Estimated effort:** 20–25 minutes
**Grounding:** [Chapter 01](../01-the-three-stage-selection-decision.md), [Chapter 02](../02-designing-bounded-pilots.md), [Chapter 03](../03-the-rollout-artifact-set.md), [Chapter 04](../04-measuring-whether-the-rollout-changed-anything.md), [Chapter 05](../05-failure-modes-and-the-pre-mortem.md), [Chapter 06](../06-partnering-with-peers-on-evidence-and-build.md)

## How to take this quiz

Pick the single best answer for each question. Each question tests whether you can *apply* a chapter idea — paraphrasing the chapter is not enough. The answer key with short explanations is at the bottom; resist reading it until you have your own answers written down.

---

### Q1. A BU head emails: *"We want a tool that does AI for sales — can you kick off evaluation?"* Based on Chapter 01, the correct Stage 1 move is to:

- **A.** Open Stage 2 immediately and ask three vendors for demos; sales is a well-understood domain.
- **B.** Push back to the five-field problem statement — target task, current baseline, pain measurement, user cohort — before any candidate evaluation starts, usually through a short working session with the people who own the work, not the budget.
- **C.** Treat the email itself as the Stage 1 artifact and route it to procurement for a RFP.
- **D.** Decline the request; "AI for sales" is out of scope for a level-45 enablement lead.

### Q2. Chapter 01 says *every* Stage 2 writeup must contain an explicit build-vs-buy line. In which of the following should the line still appear?

- **A.** When three vendors already in the approved envelope cover the capability — the honest answer is a one-sentence "no, buy — commodity capability already in the envelope."
- **B.** Only when an internal engineering team has raised a hand to build.
- **C.** Only when the capability touches sensitive data.
- **D.** Only when the POC is projected to run longer than six weeks.

### Q3. A Stage 2 POC has been running for seven weeks on the same candidate and the team is asking for a four-week extension to "really see what the tool can do." Chapter 01's framing of POCs says:

- **A.** Extend by four weeks; a POC's natural length is whatever the team needs to feel confident.
- **B.** Extend indefinitely but demote the POC's priority.
- **C.** Call it — a POC that keeps getting extended is Stage 2 failing; a scoped-and-timeboxed exercise longer than six weeks has become a pilot in disguise. Decide, write the decision, and move on.
- **D.** Convert the POC into a rollout on the strength of the elapsed effort.

### Q4. A BU head says: *"The tool is low risk, this is obvious — let's skip the pilot and roll out to 2,000 people."* Chapter 01 names four conditions that all must hold to earn a direct-to-rollout skip. Which of the following is **not** one of them?

- **A.** Low risk surface — no regulated data, no external customers, no safety-of-life decisions.
- **B.** Prior evidence from another BU, a peer organization, or a credible case study.
- **C.** The tool is inside the approved-tool envelope with no open items.
- **D.** The sponsoring executive is at level 60 or above.

### Q5. A pilot charter draft lists the cohort as *"five AI-curious engineers who already pay for a personal subscription to the tool."* Under Chapter 02, the most grounded objection is:

- **A.** The cohort is too small; pilots should be at least twenty people.
- **B.** The cohort is *representative of champions, not of the rollout population* — you will learn that your friends like the tool, not whether the broader organization will adopt it. A defensible cohort mixes skill levels, includes sceptics, and matches the eventual rollout shape.
- **C.** The cohort is fine as long as the charter also names a baseline.
- **D.** The cohort is fine; self-funded users prove intrinsic motivation and that is the signal that matters.

### Q6. At the end-of-pilot decision meeting, the numbers land *between* the pre-written adopt threshold and the kill threshold. What does Chapter 02 say should happen?

- **A.** Default to adopt — the signal is directionally positive and the sponsor is watching.
- **B.** Rewrite the adopt threshold to match the result, so the pilot can be called a success.
- **C.** Move to *extend* **only** if a specific, testable hypothesis explains the shortfall *and* the extension has a named ceiling; otherwise default to kill. The one thing the charter forbids is drifting without a decision.
- **D.** Roll over for another full pilot cycle of equal length.

### Q7. On launch day for a 4,000-seat rollout, the data-handling SOP has been drafted but is unsigned by security and privacy; the other six artifacts are all signed. Chapter 03's launch gate says:

- **A.** Launch — six of seven is a passing grade and the SOP can be countersigned in the first week.
- **B.** Launch to a subset of 400 users as a soft launch while the signatures land.
- **C.** Do not launch — the SOP without security *and* privacy signatures means the tool is not approved for GA. The artifact set is a gate, not a deliverable; a missing signature is not a judgment call.
- **D.** Launch; the SOP is an operational document and not formally part of the gate.

### Q8. A nine-month-old rollout reports *"95% of licensed users logged in last week, median prompts per user up 40% quarter over quarter, NPS at 72."* The CFO asks *"what changed on the target task?"* Under Chapter 04, the correct diagnosis and next move is:

- **A.** This is a model report; forward it to peer rollouts as a template.
- **B.** The readout is in metric-theatre territory — usage telemetry is being promoted into the outcome slot, the target-task outcome is missing or was never baselined, and the CFO's question cannot be answered from these numbers. Pull the pilot's target-task baseline, measure comparable work now, and lead the next readout with the outcome delta (even if it is flat); keep usage demoted to a sanity-check line.
- **C.** Reply that the 95% login rate itself is the change and no further measurement is needed.
- **D.** Escalate to governance for a policy review; the issue is compliance, not measurement.

### Q9. An enterprise rollout touched three BUs (legal, sales, engineering) and three roles per BU. The measurement plan commits to *"three workflow interviews with the loudest champions in the pilot cohort."* Under Chapter 04, the problem is:

- **A.** Three interviews is too few in total; the number should be at least twenty.
- **B.** Interviews should never be used — they are anecdotal.
- **C.** The minimum sample for an org-wide rollout is every role that touches the tool *and* every BU that adopted it — nine cells, not three total — and sampling only the loudest champions biases toward wins. The signal is often in the quiet users.
- **D.** Interviews should be scheduled only after the rollout ends, never during it.

### Q10. A rollout is approved and scheduled. One BU has nominated a single, unusually capable champion who is running every office hour, answering every Slack message, and building the internal prompt library alone. Under Chapter 05, the specific failure mode this is sliding into — and the preempting artifact — are:

- **A.** The ghost-user rollout, preempted by stronger launch comms.
- **B.** The metric-theatre pilot, preempted by a dashboard redesign.
- **C.** The champion-of-one, preempted by a champion list with strictly more than one champion per BU/function at launch, each with a written remit, manager-signed time allocation, and a retention plan — no rollout clears Stage 3 with a champion list of one.
- **D.** The policy-after-rollout retrofit, preempted by a security review.

### Q11. You have five minutes left in a 45-minute pre-mortem meeting and three attendees have written variations of *"adoption was slower than expected."* Under Chapter 05, the right move is:

- **A.** Accept it as a valid failure sentence and move to artifact mapping.
- **B.** Re-run the exercise — vague pre-mortem sentences are the single most reliable leading indicator of a rollout that fails for exactly the reason nobody could quite articulate in the room. The three sentences must be specific and named.
- **C.** Replace the sentences with the facilitator's own guesses to save time.
- **D.** Skip to the commit line; the pre-mortem is a courtesy step, not a gate.

### Q12. A customer-facing rollout is three weeks from its pilot-to-rollout commit. It handles sensitive customer data and is regulator-touching. The sponsoring VP says: *"Let's ship first and ask the risk engineer to red-team it in the first month post-launch — we can always adjust."* Under Chapter 06, your correct response is:

- **A.** Agree; red-team evidence is more useful once real traffic is running.
- **B.** Red-team evidence lands *before* the rollout commit, not after — the chapter is explicit that if the risk engineer cannot turn the work around in time, the rollout waits. Red-team after rollout turns every finding into an incident instead of a design input, and leaves you with no story for the governance council.
- **C.** Agree conditionally; a two-week post-launch red team is acceptable if the risk engineer signs off.
- **D.** Escalate to legal; this is a contract question, not an evidence question.

---

## Answer key

**Q1 — B.** Chapter 01 names *"We want a tool that does AI for sales"* as the forbidden shortcut and says the Stage 1 move is to push back to the five-field problem statement through a working session with whoever owns the work, not the budget. (Chapter 01 — *Stage 1 — Problem naming*.)

**Q2 — A.** Chapter 01 is explicit that the build-vs-buy line must appear in every Stage 2 writeup even when trivial — *"No, buy — commodity capability available from three vendors already in the envelope"* is a valid answer and must be written down. The alternative is silently assuming buy and missing the commission call. (Chapter 01 — *Stage 2 — Build vs. buy*.)

**Q3 — C.** Chapter 01 says a POC's timebox is two to four weeks typical and that "longer than six weeks means it's secretly a pilot." A POC that keeps getting extended is Stage 2 failing — the move is to call it and move on, not to keep adding time. (Chapter 01 — *Stage 2 — POCs*.)

**Q4 — D.** Chapter 01 names the four direct-to-rollout conditions: low risk surface, prior evidence, inside the envelope, small cohort that a kill switch can absorb. Executive seniority is explicitly not one of them — "miss one, pilot first." (Chapter 01 — *Stage 3 — The pilot-vs-rollout commit*.)

**Q5 — B.** Chapter 02's first cohort rule is that defensible pilots look like the population you intend to roll out to — a mix of skill levels, at least one sceptic, named participants. Piloting with self-funded enthusiasts teaches you nothing about broader adoption. (Chapter 02 — *Cohort — representative, not friendly*.)

**Q6 — C.** Chapter 02 names drift as the thing the charter exists to refuse: "If the data does not clearly fall into one of the three buckets, the charter was not specific enough — fix that next time and default to kill or extend-once, never to drift." Extend is "a narrow lane, not an escape hatch," requires a testable hypothesis, and happens *once*. (Chapter 02 — *Pre-written decision criteria*.)

**Q7 — C.** Chapter 03 names the artifact set as a launch *gate*, not a launch deliverable — "if any signature is missing on launch day, the rollout is not ready. Not a judgment call — the gate." The data-handling SOP specifically names security *and* privacy as both required: "Without both signatures the tool is not approved for GA." (Chapter 03 — *Data-handling SOP* and *The signing surface*.)

**Q8 — B.** Chapter 04's three-layer order — outcome first, workflow interviews second, telemetry as sanity check — is the exact contrast to the readout in the vignette. The chapter names this pattern by name: metric theatre. Fix is to recover the pilot's target-task baseline, measure comparable work, and lead the next readout with the outcome delta (even if flat), demoting usage to a sanity-check line. (Chapter 04 — *The metric-theatre pilot*; Chapter 05 — *The metric-theatre pilot*.)

**Q9 — C.** Chapter 04 is explicit: "Minimum sample for an org-wide rollout: every role that touches the tool, every BU that adopted it. If the tool rolled into legal, sales, and engineering across three BUs, you need coverage in each of the nine cells, not three interviews total from the loudest users. Loud users bias toward wins; the signal is often in the quiet ones." (Chapter 04 — *Layer 2 — workflow interviews*.)

**Q10 — C.** Chapter 05 names the champion-of-one pattern specifically — one person absorbing all the load, no named second, no written playbook, no retention plan — and names the preempting artifact as a champion list with strictly more than one champion per BU/function at launch, each with written remit, manager-signed time allocation, and a retention plan. The chapter's hard gate: no rollout clears Stage 3 with a champion list of one. (Chapter 05 — *The champion-of-one*.)

**Q11 — B.** Chapter 05 names vague pre-mortem sentences — "adoption was slower than expected," "the vendor underdelivered," "the business was not ready" — as "the single most reliable leading indicator of a rollout that will fail for exactly the reason nobody could quite articulate in the room." Re-run the exercise; do not paper over. (Chapter 05 — *The pre-mortem as a one-page artifact*.)

**Q12 — B.** Chapter 06 names "red-team after rollout" as a common anti-pattern and states explicitly that red-team evidence lands "before the rollout commit. Not alongside it. Not shortly after. If the risk engineer cannot turn the work around in time, the rollout waits." Sensitive-data, customer-facing, and regulator-touching deployments all cross the threshold the chapter sets. (Chapter 06 — *With `ai-risk-engineer`* and *Common anti-patterns*.)
