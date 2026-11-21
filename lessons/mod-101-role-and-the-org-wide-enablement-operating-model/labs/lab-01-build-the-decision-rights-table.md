# Lab 01 — Build the Decision-Rights Table, Row by Row

**Duration:** 60–75 minutes
**Format:** guided hands-on — worked example + independent build + red-team pass
**Grounding chapters:** [03 — Authoring the Enablement Operating Model](../03-authoring-the-enablement-operating-model.md), [01 — The Level-45 Role and Its Scope Contract](../01-the-level-45-role-and-its-scope-contract.md)

## Objective

Produce a signed-ready **decision-rights table** across CoE / BU / Governance / Security — ten to fifteen rows, one letter per cell (**D**ecide / **A**pprove / **C**onsult / **I**nform), with exactly one decider per row. This lab walks you through three rows as a worked example, then has you build and stress-test the rest on your own.

This is not Exercise 02 (CoE shape memo) and not Exercise 01 (one-page scope contract). Exercises write the big-picture artifacts. This lab operates one layer below — the per-decision plumbing the artifacts depend on.

## Prerequisites

- Chapter 03 read (the decision-rights section in particular).
- Chapter 01 read (so you know which decisions are *your* unilateral calls vs. escalations).
- A chosen organization. The same organization you used in the exercises works well; pick a plausible mid-size enterprise if you have none in mind.
- A blank table (markdown, spreadsheet, or whiteboard).

## Why a lab, not an exercise

Exercise 02 asks you to *choose a CoE shape*. This lab asks you to *make the operating model survive a hard meeting*. Hard meetings fail on specific rows — "wait, who actually approves adding a tool to the envelope for general use?" — not on shape. You cannot cold-write a defensible table; you have to walk a few rows carefully before the rest fall out.

## Setup

Open a single file called `decision-rights-table.md` and paste this skeleton:

```markdown
# Decision Rights — <organization-name>

CoE = AI Enablement Lead and immediate team
BU  = requesting business unit (leader or delegate)
Gov = AI governance program (head of AI governance or governance analyst)
Sec = security / IAM / DLP

Legend: D = Decides · A = Approves · C = Consulted · I = Informed

| # | Decision | CoE | BU | Gov | Sec | Notes |
|---|----------|-----|----|-----|-----|-------|
```

You will fill in rows below.

---

## Step 1 — Walk the three worked rows (15 min)

Add these three rows verbatim from Chapter 03's starter table. For each, read the chapter's rationale and write a one-line **Notes** entry in your own words — *why* the letters land where they do.

### Row 1 — "Add tool to approved-tool envelope for pilot"

| # | Decision | CoE | BU | Gov | Sec | Notes |
|---|---|---|---|---|---|---|
| 1 | Add tool to approved-tool envelope for pilot | **D** | C | **A** | **A** | |

**Why the letters:** the CoE runs the pilot pipeline, so the CoE decides to add. But a pilot touches data and policy, so Governance and Security both hold an **Approve** — they can block. The BU is Consulted because they usually requested the pilot; they are not the decider or the approver.

**Your note to write:** one line in Notes. Example: "CoE drives velocity; Gov and Sec hold a joint veto on data/policy fit; BU asked for it but does not decide for the organization."

### Row 2 — "Add tool to approved-tool envelope for general use"

| # | Decision | CoE | BU | Gov | Sec | Notes |
|---|---|---|---|---|---|---|
| 2 | Add tool to approved-tool envelope for general use | C | I | **D** | **A** | |

**Why the letters:** general availability is an enterprise commitment. Governance decides (they own policy and the model inventory); Security approves (they must sign off on access and DLP posture); the CoE is Consulted (we bring the evidence and the readiness check but do not decide at this horizon); BUs are Informed.

**Contrast with Row 1:** same decision shape, one scope step up — and the **D** moves from CoE to Gov. The scope contract from Chapter 01 names exactly this transition: you co-author at enterprise scope, you do not own.

### Row 3 — "Pull kill switch on a rollout"

| # | Decision | CoE | BU | Gov | Sec | Notes |
|---|---|---|---|---|---|---|
| 3 | Pull kill switch on a rollout | **D** | I | I | I | Speed over consensus. Notify same-day; do not pre-consult. |

**Why the letters:** kill-switch authority sits on the CoE unilaterally (Chapter 01 names it among "decisions this role makes unilaterally"). The other three are **Informed**, not **Consulted** — pre-consulting a kill switch defeats its purpose. The Notes column is the right place to make that intent explicit.

**Checkpoint 1 — do not proceed until all three are true:**

- [ ] Every row has exactly one **D**.
- [ ] You can state in one sentence why the **D** is where it is.
- [ ] Row 2's Notes field explicitly names the "co-author vs. owner" boundary.

---

## Step 2 — Build the next five rows yourself (20 min)

Add rows 4–8. Use the Chapter 03 starter set (below) *or* pick five decisions you expect to be contested in your organization's first quarter. Fill the letters and write one-line Notes for each.

Candidate rows from Chapter 03's starter table (pick five, in any order):

- Approve a pilot use case
- Approve rollout of a piloted use case
- Revise acceptable-use policy
- Revise data-handling SOP for AI
- Approve a new champion
- Revise the training curriculum
- Publish the executive scorecard
- Open an AI incident ticket
- Escalate an incident to legal / regulator

Do **not** copy the chapter's letters mechanically. For each row, say to yourself: *at this organization, who really decides?* If the honest answer differs from Chapter 03's starter, the chapter is a starting set — your table beats the generic one.

**Expected output after Step 2:** eight rows, each with:

- one **D**,
- the right mix of **A / C / I** for your organization,
- a one-line Notes entry naming the rationale.

**Checkpoint 2:**

- [ ] You have exactly one **D** per row.
- [ ] You have at least one row where a **D** differs from Chapter 03's starter table, and the Notes column explains why.
- [ ] Reading the table out loud takes under four minutes — if it is slower, your Notes column has grown into prose; cut.

---

## Step 3 — Add the two organization-specific rows (10 min)

Chapter 03 says the starter table is not the right table for your organization. Add two rows that are specific to your context and *not* in the starter set. Examples by organization type:

- **Regulated bank:** "Approve use of model output in a customer-facing credit decision" — likely CoE=C, BU=C, Gov=**D**, Sec=A; in some banks, model risk management sits above governance and owns the D.
- **Hospital system:** "Approve use of an AI scribe on protected health information" — likely CoE=C, BU=C, Gov=A, Sec=**D** (because PHI handling is the binding constraint), with the Chief Medical Information Officer as a real additional role to add.
- **SaaS company:** "Approve use of a vendor copilot on production-customer data" — CoE=C, BU=A, Gov=C, Sec=**D**.
- **Global holding company (federated CoE):** "Approve a BU-specific vendor copilot that cannot be enterprise-licensed" — CoE=C, BU=**D**, Gov=A, Sec=A — because the federated shape pushes the decide down to the BU.

Add your two rows. Name them specifically, not generically.

**Checkpoint 3:**

- [ ] Both rows name an organization-specific condition (a regulator, a data type, a system of record, a shape of contract).
- [ ] At least one of the two rows has the **D** somewhere other than CoE or Gov — surface roles your table was quietly ignoring (Sec, Risk, Legal-delegate, CMIO, model-risk, CDO).

---

## Step 4 — Red-team the table (15 min)

Read every row aloud against these four questions. Any row that fails one of them gets a `<!-- fix: ... -->` comment in the Notes column — do not silently paper over.

1. **Single decider check.** Does the row have exactly one **D**? Two **D**s is a meeting; zero is a vacuum.
2. **Scope creep check.** Does the row's **D** match the scope contract from Chapter 01? If a row quietly makes the CoE decide something the contract routes to Governance (policy, regulator-facing posture) or vice versa, flag it.
3. **Hard-case check.** Imagine the first hard version of this decision — the one where the parties disagree. With the current letters, does the hard case resolve, or does it still produce a six-person meeting? If it still produces a meeting, the table is ceremonial. Add a note on who breaks the tie.
4. **Audit readability check.** If a Governance auditor read only this table (no chapter, no contract), would they understand what the enablement lead is accountable for? If the table is unreadable without you in the room, it is not evidence yet.

**Expected output of Step 4:** a short list — three to six items — of the rows you want to revisit with your governance partner. These are the real agenda items for the first quarterly operating-model review.

---

## Step 5 — Publish and route for signature (5 min)

Chapter 03 names the table as something "signed by all four parties before the first real decision tests it." Finalize the lab artifact:

1. Add a header note: "Table version: v0.1 — draft for signature by CoE / BU rep / Gov / Sec, target date `<day-55>`."
2. Add a change-log footer: "v0.1 — initial draft (today). Next revision: after first hard case."
3. Save the file. In the real role you would route for signature; in the lab, the saved artifact is your deliverable.

## Deliverable

- `decision-rights-table.md` — 10–15 rows, each with exactly one **D**, Notes column populated, red-team flags visible, version header and change-log footer.

## Checkpoint — self-evaluation

- [ ] 10–15 rows total, no fewer, no more. If you wrote twenty, you over-specified; cut.
- [ ] Row 2 explicitly names the co-author vs. owner transition (matches Chapter 01 → Chapter 04's Handoff 4).
- [ ] Row 3's Notes column states that kill-switch pre-consultation defeats the purpose.
- [ ] At least one row diverges from Chapter 03's starter set because of an organization-specific fact, and the divergence is named.
- [ ] Red-team Step 4 produced at least three items to revisit — a table that passes red-team on first draft either is unusually complete or has not been red-teamed hard enough.

## What this lab prepares you for

The decision-rights table is one of the four plumbing pieces of the operating-model doc you build in Exercise 02's broader context and in [mod-111](../../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md). The lab exists because this specific artifact is almost always written vaguely on the first pass and expensively re-written after the first hard case. Writing it carefully once, with a red-team pass, is the cheapest version of that lesson.
