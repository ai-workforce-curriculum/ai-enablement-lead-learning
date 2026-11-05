# Exercise 05 — Rollout Artifact Set Dry Run

**Estimated effort:** 4 hours
**Format:** a bundle of seven short Markdown artifacts plus a one-page pre-mortem, delivered as a single folder or a single Markdown file with clear H2 dividers
**Grounding chapters:** [03 — The Rollout Artifact Set](../03-the-rollout-artifact-set.md), [05 — Failure Modes and the Pre-Mortem](../05-failure-modes-and-the-pre-mortem.md)

## Objective

Produce the full seven-artifact rollout bundle, at outline depth, for one concrete tool rollout at one concrete organization. The point of the exercise is that the *set* exists end-to-end, each piece has a named co-author, and the whole thing has been stress-tested by a pre-mortem — not that any single artifact is publication-ready. A rough artifact is fine. A missing artifact is a failure.

## Prerequisites

- Chapters 03 and 05 read. Chapter 02 (bounded pilots) is helpful background.
- A chosen organization and a chosen tool. If you have carried a pair through earlier exercises (the scope contract from mod-101 Exercise 01, the selection worked example in Exercise 01 of this module, and the use-policy draft in Exercise 02), reuse them. If you have not, pick one organization/tool pair now and stay with it for the full bundle:
  - a 3,000-person US bank rolling out a general-purpose code assistant to engineering
  - a 12,000-person global pharma rolling out a document-summarisation assistant to medical affairs
  - a 500-person SaaS company rolling out an enterprise chat assistant to the whole company

## Problem statement

Your executive sponsor has approved the pilot. The security review is in flight. Procurement is close to signing. You have two weeks before access is turned on for the first cohort, and the question you will be asked in your next steering review is simple: *are we ready to turn this on?*

"Ready" at this level does not mean the tool works. "Ready" means the seven rollout artifacts in Chapter 03 exist, each one has a co-author who will stand behind it, and you have already imagined — on paper — the three ways this rollout fails and what in the bundle catches each failure.

This exercise is that dry run. You will produce the seven artifacts at outline depth and the pre-mortem that interrogates them.

## Requirements

Produce **seven short artifacts**, each roughly half a page to a page. Depth is explicitly *not* the goal — coverage is. Each artifact must contain:

- A short description of its purpose (one or two sentences).
- Enough structure (bullets, a tiny table, a short list of sections) that a reader can see the shape of what the finished artifact would contain.
- **A visible "co-authored by / signed by" line** naming the roles involved. Use role titles, not real people. At minimum, name the owning role and one co-signer. Where Chapter 03 names a specific co-author for an artifact, use that one.

The seven artifacts, in order:

1. **Use policy stub.** If you carried the Exercise 02 draft, point at it by filename and add a one-paragraph note on what still needs to be true for this rollout. If you did not, sketch the stub — three or four bullets on what is allowed, what is not, and the carve-outs that apply to the chosen tool.
2. **Data-handling SOP.** What data classes can and cannot go into the tool, where inputs and outputs live, retention, and the one or two "do not paste this" rules that matter most for the chosen organization.
3. **Access & offboarding playbook.** How a user gets access (requestor, approver, SLA), how a user loses access on role change, and how a user loses access on termination. Name the owning system of record.
4. **Training package outline.** Role-segmented, with **at minimum three roles**: operator (daily end user), specialist (power user or domain owner), administrator (the people who run the tool and its guardrails). For each role: time-to-complete, three to five learning objectives, and the format (self-serve, live, mixed).
5. **Support & escalation path.** Tier 1 / Tier 2 / Tier 3 ownership, hours, response SLAs, and the two or three incident categories that bypass Tier 1 entirely (e.g. suspected data leak, model producing regulated-content violations).
6. **Champion list.** Named roles — not real individuals — with counts per business unit or function, and the three or four selection criteria you used. A line on time commitment and on what champions are *not* responsible for.
7. **Kill-switch & rollback plan.** The signal(s) that would trigger a halt, who can pull it, how fast it happens (SSO disable, license revoke, feature flag), and what the organization does for the users mid-session when it fires.

Then produce one additional document:

8. **One-page pre-mortem (Chapter 05).** Write **three sentences**, each of the form "Six months from now, this rollout failed because \_\_\_." For each sentence, name which of the seven artifacts above was supposed to preempt that failure, and — in one line — whether your current draft of that artifact actually would have.

## Starter guidance

- Seven artifacts in four hours means each one gets roughly twenty-five minutes. Set a timer. If you are still polishing artifact 2 at the ninety-minute mark, stop and move on. The dry run exists so you discover which artifact you cannot sketch in half an hour — that is the one you will need help with on the real rollout.
- The co-author lines are not decoration. If you cannot name the role that co-signs the data-handling SOP without checking, that is a finding. Write it down as a finding in the artifact itself ("co-author: TBD — I don't know who owns data classification at this org and will find out by \[date\]"). Honest gaps beat invented co-authors.
- The training outline is the one learners most often over-invest in. Keep it at outline depth. Three roles, learning objectives as bullets, no slide decks. Module 104 is where curriculum depth lives.
- The kill-switch plan is the one learners most often under-invest in. Spend the full twenty-five minutes on it. "Revoke SSO" is not a plan; "the IAM on-call revokes the SSO app, which drops all active sessions within 90 seconds, and the #ai-support channel pins a notice drafted by \[role\]" is.
- The pre-mortem is the whole point of the exercise, not an appendix. Treat the three failure sentences as the real deliverable and the seven artifacts as the surface area the pre-mortem is allowed to test. If one of your three sentences does not map cleanly to one of the seven artifacts, either your artifact set is incomplete or your failure is outside the scope of this rollout — say which.

## Deliverables

- A folder `rollout-bundle/` (or a single `rollout-bundle.md` file) containing the seven artifacts, in the order above, each with its own H2 and its own co-author line.
- `pre-mortem.md` — one page, three failure sentences, each mapped to one artifact, each with a one-line honesty check on whether the current draft actually catches it.
- A three-line header at the top of the bundle naming the organization, the tool, and the date you would plan to turn access on. These three lines anchor the whole set.

## Acceptance criteria

- All seven artifacts exist. A missing one fails the exercise regardless of how good the other six are.
- Each artifact has a visible co-author line naming at least two roles (owner plus co-signer). "TBD — reason" is acceptable; silence is not.
- The training outline covers at least three roles, and the roles are *different* (not three flavours of end user).
- The kill-switch plan names a specific mechanism (not just an intent), a specific role that pulls it, and a rough time-to-effect.
- The pre-mortem is three sentences, each mapped to exactly one artifact, each with an honest one-line check on whether the current draft would preempt it.
- No artifact is longer than a page. If one of them is, you are drafting the real artifact instead of the outline — cut.

## Stretch goals

- Pick the one artifact in your bundle that you feel least qualified to co-author alone, and sketch — three bullets — the conversation you would have with that co-author in the first thirty minutes. This is the practical bridge into Chapter 06 (partnering with peers).
- Add a **fourth** failure sentence to the pre-mortem that your current artifact set *cannot* preempt, and name the artifact (or the module) that would have to exist for the bundle to catch it. This is often where mod-109 (incident response) and mod-103 (policy depth) earn their place.
- Take your kill-switch plan and walk it through once in your head at 2am on a Saturday. Note the one step that quietly breaks when the named role is asleep, and amend the plan.

## Why this exercise matters

The rollout artifact set is the thing that distinguishes an AI Enablement Lead from a project manager running a tool launch. You are not shipping the tool; you are shipping the seven artifacts that let the organization absorb the tool. The first time you do this on a real rollout, the pressure is high, three of the seven co-authors are unresponsive, and you will discover which artifacts you have never actually drafted. Running the dry run once, under no pressure, means the first time is not the first time.

Depth of any single artifact is explicitly out of scope here — policy depth lives in mod-103, curriculum depth in mod-104, champion-network depth in mod-105, kill-switch operation in mod-109. The exercise is about the *set existing*, co-authored, and stress-tested by a pre-mortem. That is the altitude of the role.
