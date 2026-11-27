# Lab 01 — Build the Cost-Model Sourcing Map and the Quarterly Attestation Form

**Duration:** 60–75 minutes
**Format:** guided hands-on — sourcing-map construction + attestation-form drafting + red-team pass
**Grounding chapters:** [01 — The Enablement Cost Model at Org Scope](../01-the-enablement-cost-model-at-org-scope.md), [04 — Partnering with Procurement, Finance, and IT](../04-partnering-with-procurement-finance-and-it.md)

## Objective

Produce the **sourcing map** and the **quarterly attestation form** that keep the six-family cost model from [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md) defensible across reorganizations, tool swaps, and staffing changes. The sourcing map names, per family, the authoritative source and the reconciliation cadence; the attestation form is the one-page instrument that collects the Family 3 SME-time, Family 4 shadow-enablement, Family 4 champion-time, and Family 6 manager-change-management lines that no system ledger reads for you. By the end of the lab, the model you built in [Exercise 01](../exercises/exercise-01-enablement-cost-model-drill.md) has the plumbing underneath it that a Finance auditor would sign off on in a working session.

## Prerequisites

- [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md) read, with the six-family taxonomy, the sourcing map, the three sourcing disciplines (cross-ledger reconciliation, attestation for partial time, dollar-threshold materiality), and the quarterly attestation cadence close enough to cite without the chapter open.
- [Chapter 04](../04-partnering-with-procurement-finance-and-it.md) read, with particular attention to the Procurement and Finance ownership splits and the monthly-invoice-reconciliation interface.
- A chosen organization. Fictional-but-realistic is fine; the organization must have an identifiable CoE cost center, at least two business units with named operators, and at least one AI tool live in production. Carrying the organization from Exercise 01 produces a coherent bundle.
- Two blank working files — `sourcing-map.md` and `attestation-form.md`.

## Why a lab, not an exercise

[Exercise 01](../exercises/exercise-01-enablement-cost-model-drill.md) builds the cost model itself — the six families populated, the methodology appendix, the five-undercount defence. It assumes the sourcing map and the attestation convention exist and can be referenced. In practice, the sourcing map and the attestation form are *authored artifacts* the enablement lead has to produce before the cost model is defensible — they are the plumbing Exercise 01's methodology appendix points at. This lab builds that plumbing. If you tried to populate Family 4 (embedded FTE) or Family 6 (downstream support) in Exercise 01 and felt you were estimating in the dark, this is the layer that fills the gap.

[Exercise 04](../exercises/exercise-04-procurement-and-finance-partnership-contract.md) writes the three-way partnership contract that the sourcing map depends on; this lab produces the two concrete artifacts the contract's Finance and Procurement sections will reference by name.

## Setup

Open `sourcing-map.md` and paste this skeleton. You will fill it in as you walk Steps 1–3.

```markdown
# Cost-Model Sourcing Map — <organization-name> — v0.1 (draft)

**Owner:** AI Enablement Lead — <your-name>
**Finance partner:** <name>
**HR / Workforce Planning partner:** <name>
**IT partner:** <name>
**Procurement partner:** <name>
**Review cadence:** refreshed annually at budget cycle; mid-year amendments logged.

## 1. Family-by-family sourcing

## 2. Cross-ledger reconciliation hooks

## 3. Materiality threshold

## 4. Fully-loaded FTE multiplier

## 5. AI-incremental cost rule
```

Open `attestation-form.md` and paste this skeleton:

```markdown
# Quarterly Enablement Attestation Form — Q<N> FY<YY>

**Contributor:** <name, role, cost center>
**Contributor's manager (sign-off):** <name>
**Attestation period:** <quarter start> through <quarter end>
**Instructions:** <one short paragraph>

## 1. Lines attested

## 2. Methodology notes

## 3. Sign-off
```

---

## Step 1 — Fill in the family-by-family sourcing block (15 min)

In `sourcing-map.md` Section 1, write six subsections — one per family — each naming (a) the family, (b) the authoritative source, (c) the reconciliation cadence, (d) the named owner on the source side. The chapter's sketch (Chapter 01, *The sourcing map*) is the starting point; the job here is to resolve it against your organization's specific partners and systems.

Three rules to apply as you write:

- The authoritative source is a **specific system or specific role**, not a category. "Workday" or "the CoE cost-center GL run by `ai-coe-ops-manager`" is specific; "HR" or "Finance" is not.
- The reconciliation cadence is a **specific interval**, aligned to a partner's existing cycle where possible. "Monthly, on the second business day of the following month, through the Finance close cycle" is specific; "regularly" is not.
- The owner is a **named role on the source side**, not the enablement lead. The enablement lead *consumes* the source; the owner is who runs it. (This matters because the lead's cost model inherits the source's data quality — if the source is unowned, the cost line is unreliable.)

A worked opening for Family 1 (fictional, mid-sized organization):

> *Family 1 — Tool licenses. Authoritative source: `procurement-system.ap-ledger` plus vendor invoice archive in `/finance/vendors/ai/`, owned by the `vendor-ops-manager` on the Procurement side. Reconciliation cadence: monthly, on the second business day of the month, through the Finance close cycle. Variable charges (usage-based inference, API consumption) are recognized to the quarter the usage occurred (not the quarter the invoice landed); true-ups are reconciled at renewal and allocated back to the originating quarters per the organization's variable-cost recognition rule. Pilot and POC licenses are tagged `pilot-poc` and carry a separate line until the rollout crosses the Stage 3 gate from [mod-102 Chapter 01](../../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md), at which point they collapse into the enterprise-seat line.*

Repeat this shape for Families 2 through 6. Expect Family 4 and Family 6 to be the hardest to populate — they rely on attestation plus cross-ledger reads rather than a single invoice stream.

### Checkpoint 1 — before Step 2

- [ ] Section 1 has six subsections, one per family, each with authoritative source, cadence, and named owner.
- [ ] Every source names a specific system or specific role (not a category).
- [ ] Family 1 states the variable-charge recognition rule; Family 4 and Family 6 flag that they run on attestation plus system data.
- [ ] No family is left as "TBD" — if the source is genuinely unresolved, the subsection names what has to be true for it to resolve and who owns the resolution.

---

## Step 2 — Write the cross-ledger reconciliation hooks (10 min)

Chapter 01's first sourcing discipline is cross-ledger reconciliation. The hooks are what let the cost model aggregate across ledgers that sit inside different organizational units. Setting them up is one-time work; running them is cheap — once they exist.

In Section 2, name each hook explicitly. Three hooks are usually load-bearing:

- **The AI-tag on IT support tickets.** How the IT ticketing system identifies tickets generated by AI-tool support (account provisioning, licensing, integration, "it stopped working"). State: the tag name, who owns the tag taxonomy, when it was added (or when it will be added), and the sampled-estimate fallback for the period before the tag was live. A ticketing system without the tag is a ticketing system from which Family 6 cannot be read; the fallback until the tag lands is a sampled estimate signed by the IT director.
- **The AI-project code on legal / privacy / security timesheets.** How governance partners (legal, privacy, security) attribute their AI-related review time to the enablement program. State: the project code, who owns the attestation, and whether the code is required at time-entry (strong) or self-reported quarterly (weaker — reduces to attestation).
- **The enablement-program allocation on HR records.** How embedded enablement partners (BU-embedded partners, named champions) are flagged in the HR system with the percentage-of-time allocated to the enablement program. State: the HR field name (or the attestation fallback), the annual ratification working group ([mod-106 Chapter 05](../../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)'s FTE-attribution group), and the refresh cadence.

Four if applicable: a DLP integration hook that measures AI-tool-driven DLP alerts for Family 6. Usually smaller, often skipped on first draft; note its absence rather than pretending it exists.

### Checkpoint 2 — before Step 3

- [ ] Section 2 names at least three hooks with specific system / field / tag names.
- [ ] Each hook names its owner on the source side.
- [ ] Any hook that does not yet exist is named with its fallback (typically a sampled estimate) and the condition under which it will be stood up.

---

## Step 3 — State the materiality threshold, FTE multiplier, and AI-incremental rule (10 min)

Sections 3, 4, and 5 are the three methodology-footnote lines the Finance partner will sign off on in the annual working session. Each is short — one paragraph — but each is load-bearing because it pre-resolves a conversation that would otherwise re-open every quarter.

### Section 3 — Materiality threshold

Chapter 01 names a typical bar of 0.5% of total denominator. Write Section 3 as: the specific percentage, the dollar equivalent at the current total, the roll-up rule ("items under $X are collapsed into an 'other / small lines' bucket inside their family; the bucket is itemized in a supplemental exhibit on request"), and the refresh cadence (annual, with the budget cycle).

### Section 4 — Fully-loaded FTE multiplier

Chapter 01's rule: the multiplier is Finance's, not enablement's. Write Section 4 as: the specific multiplier (e.g., 1.35x base salary), the components it covers (benefits, facilities, overhead allocation, per the organization's standard), who owns it on the Finance side, and the refresh cadence. If the organization's multiplier is not yet confirmed, state so and name the partner who will confirm it in the first working session — do not invent one.

### Section 5 — AI-incremental cost rule

Chapter 01's fifth undercount. Write Section 5 as a one-sentence rule plus one worked example. A worked opening:

> *AI-incremental cost rule: for platform add-ons sitting on existing SaaS contracts (Microsoft 365, Google Workspace, Salesforce, ServiceNow), only the AI add-on per-user charge belongs in the AI denominator; the pre-existing base SaaS license is the non-AI operating baseline. Worked example: M365 E5 at $57/user/month is baseline (not in denominator); M365 Copilot at $30/user/month is incremental (in denominator). This rule is published so the conversation about whether the full $87/user/month belongs in the denominator does not re-open each quarter.*

### Checkpoint 3 — before Step 4

- [ ] Section 3 states the materiality threshold as a specific percentage with the dollar equivalent and the roll-up rule.
- [ ] Section 4 states the fully-loaded FTE multiplier with its components and its owner; "TBD" is replaced with a named resolution partner if the number is not confirmed.
- [ ] Section 5 states the AI-incremental cost rule with at least one worked example (pre-existing cost identified, AI-incremental cost identified).

---

## Step 4 — Draft the attestation form (15 min)

Switch to `attestation-form.md`. The attestation form is the instrument that collects Family 3 SME time, Family 4 champion / shadow / governance-partner time, and Family 6 manager change-management load. Chapter 01's third sourcing discipline is attestation for partial time; the form is its running shape.

Four design rules carry forward from Chapter 01:

- **One page.** A two-page attestation form will not be filled in. Keep it tight.
- **Structured, not narrative.** Named lines with hours, percentages, or dollar equivalents — not free-text descriptions.
- **Manager sign-off.** The contributor's manager signs off, not the contributor alone. Chapter 01's note on attestation: "This reduces self-report inflation."
- **Quarterly.** Monthly is too often; annual is too infrequent. The quarterly cadence matches Chapter 01's attestation rhythm.

### Section 1 — Lines attested

Provide a fixed list of attestation line-items with units. Four required:

| # | Line | Unit | Guidance |
|---|------|------|----------|
| 1.1 | Enablement SME time (Family 3) | hours per quarter | Time spent reviewing training content, recording role-specific modules, advising the CoE on domain curriculum. |
| 1.2 | Champion duties (Family 4) | % of role per quarter | Time spent on champion duties — office hours, peer coaching, rollout participation. Chapter 01's typical range: 10-20% of a role's time. |
| 1.3 | Shadow enablement (Family 4) | hours per quarter | Informal enablement work not attributed to a formal role — tip sheets, informal office hours, coaching through change. Count only material contributions. |
| 1.4 | Manager change-management load (Family 6) | hours per quarter | Rollout coordination, team-level measurement, 1:1 coaching through adoption, resistance management. |

Add a fifth line (1.5 — governance partner time, hours per quarter) if the contributor is in legal, privacy, security, or compliance.

Each line has three cells: **hours or %**, **the rollouts / programs the time was spent on** (free-text, two or three items max), and **a one-sentence note on anything unusual this quarter**.

### Section 2 — Methodology notes

Three short notes at the bottom of the form, anchored to the sourcing-map:

- **How the hours translate to dollars.** Hours × fully-loaded hourly rate (fully-loaded annual cost ÷ 2,080 hours). The sourcing map's Section 4 FTE multiplier is applied here.
- **What is in scope and what is not.** "Enablement" here means time attributable to the AI enablement program specifically, not all time spent adjacent to AI tools. Non-attributable time (operator's own tool-use, personal learning) is explicitly out of scope.
- **The sign-off chain.** Contributor fills; contributor's manager signs; the enablement program's measurement analyst compiles and reconciles against the HR allocation field from the sourcing map's Section 2.

### Section 3 — Sign-off

Two signatures — contributor and manager — with date fields and the quarter / fiscal year.

### Checkpoint 4 — before Step 5

- [ ] The form fits on one page. If it does not, cut a line, not expand the page.
- [ ] Every attested line has a unit (hours, %, dollars) and a short guidance string.
- [ ] Section 2 names the dollar-conversion formula and the sign-off chain.
- [ ] Section 3 carries both contributor and manager sign-off fields; no form ships with only contributor sign-off.

---

## Step 5 — Red-team against the three sourcing disciplines and the five undercounts (10 min)

Read the sourcing map and the attestation form aloud against six failure checks. Anywhere the artifacts fail a check, add a `<!-- fix: ... -->` note inline and fix before shipping.

Three Chapter 01 sourcing disciplines at the plumbing layer:

1. **Cross-ledger reconciliation hooks exist?** For each of the three load-bearing hooks (IT ticket AI-tag, legal/privacy/security AI-project code, HR enablement allocation), either the hook is live and named with its owner, or the fallback and the condition for standing it up are named. "The ticketing system does not AI-tag" without a sampled-estimate fallback is a Family 6 line the reviewer will call missing.
2. **Attestation runs on quarter, with manager sign-off?** Not monthly (too often, reduces to noise), not annual (too infrequent, reduces to guess), not contributor-only (self-report inflation). The form's Section 3 enforces this.
3. **Materiality threshold is a specific percentage, not a hand-wave?** "0.5% of total denominator with the dollar equivalent at the current total" is defensible; "small lines are rolled up" is not.

Three of the five Chapter 01 undercounts at the plumbing layer:

4. **Can champion time be read from the sourcing map?** The map should name HR allocation (preferred) or the attestation form (fallback) as the source, with the annual FTE-attribution working group as the ratification gate. If the map has no path to champion time, Family 4's largest line is unsourced.
5. **Can operator learning time be computed from the sourcing map?** The map should carry a formula hook — operator fully-loaded time × hours per adoption cycle × cohort size, with the cohort size pulled from the rollout's Stage 3 roster. Family 6 depends on this; if the formula is not named, operator learning time is invented at every quarterly review.
6. **Is the AI-incremental cost rule explicit with a worked example?** Section 5 should carry one. A sourcing map that is silent on the AI-incremental rule will have the entire M365 bill dragged into the AI denominator by the first skeptical CFO question.

Fix each `<!-- fix: ... -->` note before Step 6.

### Checkpoint 5 — before Step 6

- [ ] All six checks pass or carry a fix note.
- [ ] Any hook that does not yet exist names its fallback and the condition under which it will be stood up.
- [ ] No attested line in Section 1 of the form uses "estimate" where "attested" is the right word.

---

## Step 6 — Version both artifacts and route them to the partners (5 min)

Chapter 01 names the annual methodology refresh and the sourcing-map ratification as joint artifacts with Finance, HR, and IT. The lab produces the first draft; routing it is what converts it into an operating artifact.

Add a version footer to both files:

```
Version: v0.1 — draft for Finance / HR / IT review.
Next revision: at the first joint working session (expected within 2 weeks).
Changes between versions are logged below with date, author, and one-sentence reason.

## Change log

- v0.1 (YYYY-MM-DD) — <your-name> — initial draft.
```

Send `sourcing-map.md` to the Finance partner (primary), the HR/Workforce Planning partner, and the IT partner (for the cross-ledger hooks). Send `attestation-form.md` to the three partners plus a pilot cohort of champions, SMEs, and managers who will be asked to fill it in next quarter — ask them to flag any line that is unclear or any unit they would struggle to answer honestly.

## Deliverables

- `sourcing-map.md` — the five-section sourcing map, with every family sourced, every hook named, the materiality threshold stated, the FTE multiplier stated (or routed to the resolution partner), and the AI-incremental cost rule with one worked example.
- `attestation-form.md` — the one-page quarterly form with attested-line structure, methodology notes, and manager sign-off.

## Checkpoint — self-evaluation

- [ ] A Finance partner reading `sourcing-map.md` alone could reconcile the cost model from Exercise 01 against the organization's ledgers without asking the enablement lead for clarification.
- [ ] Every one of the six families in the sourcing map has a named source, named owner, and named cadence; no family is "TBD."
- [ ] The attestation form fits on one page and would plausibly be filled in by a manager in 10 minutes.
- [ ] The three sourcing disciplines (cross-ledger hooks, quarterly attestation with manager sign-off, stated materiality threshold) are each explicit in the sourcing map.
- [ ] The AI-incremental cost rule is published with one worked example — the pre-existing base cost and the AI-incremental cost are both identified.
- [ ] The red-team pass caught at least one `<!-- fix: ... -->` the first time; a draft that passes clean on first read was not red-teamed hard enough.

## What this lab prepares you for

Exercise 01's cost model treats the sourcing map and the attestation convention as inputs; this lab is where those inputs are authored. Exercise 04's three-way partnership contract references the sourcing map in its Section 5 (Finance interfaces, monthly invoice reconciliation and semi-annual FTE-attribution working group); the map is what the contract points at by name. The quarterly attestation cycle from [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md)'s *keeping the cost model current* reads this form once a quarter; the form you draft here is what gets sent out at the next quarter-end. The lab also exercises the Chapter 04 Finance-partnership and IT-partnership vocabulary: once the sourcing map exists, the standing monthly invoice reconciliation and the standing monthly licensing reconciliation both have a document to work against instead of an ad-hoc spreadsheet — which is the plumbing rhythm Chapter 01 names as the one that makes the denominator defensible at steady state.
