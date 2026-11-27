# Lab 02 — Compose the ROI Confidence Band via Monte Carlo

**Duration:** 75–90 minutes
**Format:** guided hands-on — term-distribution authoring + Monte Carlo composition + sensitivity drill + theatre-pattern red-team
**Grounding chapters:** [02 — Projecting ROI with Confidence Bands](../02-projecting-roi-with-confidence-bands.md), [01 — The Enablement Cost Model at Org Scope](../01-the-enablement-cost-model-at-org-scope.md)

## Objective

Produce a working **ROI band-composition artifact** for one priority rollout: the four term distributions (magnitude, timing, attribution, cost) authored with explicit 10th / 50th / 90th percentiles, a thousand-draw Monte Carlo that composes them into a three-year ROI distribution, the central estimate and 90% band read off the sample, and a two-assumption sensitivity analysis that shows which term the ROI is most load-bearing on. The deliverable is the artifact the enablement lead carries into a Finance working session — not a slide, a *worksheet* the Finance partner can inspect and challenge term-by-term.

## Prerequisites

- [Chapter 02](../02-projecting-roi-with-confidence-bands.md) read, with the four-dimensional value-realisation framework, the J-curve regions, the four term bands, the two composition approaches (analytical propagation, Monte Carlo), and the three projection-specific theatre patterns close enough to cite without the chapter open.
- [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md) read; the denominator in the ROI calculation uses the six-family cost model, and Family 6's wider band is where the cost-band uncertainty mostly lives.
- One priority rollout. Carrying the rollout from [Exercise 02](../exercises/exercise-02-roi-projection-with-confidence-bands.md) is efficient — the J-curve from Exercise 02 is the integral this lab feeds into the Monte Carlo. If Exercise 02 is not done, a rollout with (a) a steady-state magnitude estimate, (b) a cohort size, (c) a rough ramp length, and (d) a Family 1-6 cost total is sufficient.
- A working environment: a spreadsheet that supports random-sample functions (Excel's `RAND()` or `NORMINV`, Google Sheets' equivalents) **or** a notebook environment with Python (`numpy.random`) or R. One blank worksheet file — `roi-band-monte-carlo.xlsx` or `.ipynb` — plus a short writeup file — `band-composition-notes.md`.

## Why a lab, not an exercise

[Exercise 02](../exercises/exercise-02-roi-projection-with-confidence-bands.md) builds the full projection worksheet — J-curve monthly for 36 months, magnitude / timing / attribution / cost bands, composed ROI band, sensitivity analysis, prioritisation-frame statement. The exercise requires that you *state the composition method* (analytical or Monte Carlo); it does not walk you through running it. In practice, the first time an enablement lead actually composes a confidence band — authoring four distributions, running the simulation, reading the percentiles — is where the method becomes real. If Exercise 02 asked you to compose the band and you reported "analytical propagation with ±20%" because you did not know how to run the Monte Carlo, this lab is where that gap closes.

The lab also sits upstream of [Exercise 03](../exercises/exercise-03-org-scope-build-vs-buy-matrix.md) and [Exercise 05](../exercises/exercise-05-tool-stack-consolidation-worked-example.md): the build-vs-buy matrix and the consolidation case both call for a composed-band ROI per candidate. Once you have composed one band, composing three more for a matrix is additive, not from scratch.

## Setup

Open the worksheet file. If using a spreadsheet, structure four sheets: `terms`, `draws`, `roi_distribution`, `sensitivity`. If using a notebook, structure four cells correspondingly. Open `band-composition-notes.md` and paste this skeleton:

```markdown
# ROI Band Composition — <rollout-slug> — v0.1 (draft)

**Owner:** AI Enablement Lead — <your-name>
**Finance partner:** <name>
**Composition method:** Monte Carlo, 1,000 draws
**Horizon:** 3 years (36 months)

## 1. The four term distributions

## 2. The composition — how the terms combine

## 3. The composed-band read

## 4. The sensitivity analysis

## 5. Theatre-pattern self-check
```

---

## Step 1 — Author the four term distributions (20 min)

Chapter 02's four terms each carry their own uncertainty. Each is characterized by a 10th-percentile, a 50th-percentile (central), and a 90th-percentile. Three questions per term:

- What is the central estimate?
- What is the 10th-percentile (the pessimistic draw that reflects the range of plausible downside)?
- What is the 90th-percentile (the optimistic draw that reflects the range of plausible upside)?

Two shape rules:

- **The 10th and 90th are plausible, not extreme.** They are the 80th-percentile-width band, not the worst-and-best possible outcomes. A 90th-percentile magnitude that assumes the rollout works for every single operator at the vendor's published ceiling is extreme, not plausible.
- **Asymmetry is allowed.** Terms do not have to be symmetric around the central estimate. Attribution-by-fraction is often skewed lower (40% central, 25% at the 10th, 55% at the 90th); timing is often skewed longer (7-month central, 5-month at the 10th, 14-month at the 90th — the right tail is longer than the left).

### Term 1 — Magnitude distribution

In the worksheet `terms` sheet (or notebook cell), author a row for Magnitude with three columns: `p10`, `p50`, `p90`. Units: dollar-equivalent monthly realised value *per operator at steady state*.

Grounding — Chapter 02 names three sources in order of preference:

1. **Trailing measurement** from a prior rollout of the same tool in a comparable cohort. If available, the trailing six-month distribution of value-per-operator gives you `p10` / `p50` / `p90` directly.
2. **Literature-informed distributions** (Peng, Ziegler, Noy & Zhang, Brynjolfsson/Li/Raymond, Dell'Acqua from [mod-106 Chapter 04](../../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md)), transferred as *shape* not *number*. The literature gives a 15–55% productivity-gain distribution on comparable tasks; your cohort is unobserved, so your band is *wider*, not narrower.
3. **Vendor-reported ranges** as the upper bound only. Never as `p50`.

In `band-composition-notes.md` Section 1, record one sentence naming which source grounds the distribution.

### Term 2 — Timing distribution

Author a row for Timing. Unit: crossover month (integer or fractional).

The dominant uncertainty sources are adoption curve shape, workflow-fit lag, and change-management load ([Chapter 02](../02-projecting-roi-with-confidence-bands.md)). A well-run knowledge-work rollout's crossover month sits in the 3–9 range per Chapter 02; a `p50` in month 2 is almost always optimistic. The `p90` (the pessimistic draw) can be in the 12–15 month range — some rollouts just take longer to cross.

### Term 3 — Attribution distribution

Author a row for Attribution. Unit: fraction between 0 and 1.

Pick the attribution frame first (fraction, cohort comparison, staggered rollout per Chapter 02). The frame sets the shape:

- **Attribution by fraction.** Central 40%, 10th-percentile 25%, 90th-percentile 55% is a defensible baseline when workflow-interview evidence distributes causal factors across AI, training, and operational changes. Wider is appropriate when the evidence is thin.
- **Attribution by cohort comparison.** The band is set by the uncertainty in the cohort match; typically narrower than fraction when cohorts are well-matched.
- **Attribution by staggered rollout.** The band is the standard error of the difference-in-differences estimate; narrowest when the staggering was designed in.

### Term 4 — Cost distribution

Author a row for Cost. Unit: total three-year dollar cost (the Family 1-6 TCO projected across the horizon, from [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md)).

Chapter 02 names Family 6 (downstream) as the widest band because it is the most attested rather than invoiced. Your `p10` cost (low cost) reflects a scenario where Family 6 lines (operator learning time, help-desk load, incident-response cost) run lower than planned; your `p90` cost (high cost) reflects a scenario where they run higher. Family 1 (tool licenses) has the narrowest contribution to the cost band.

### Checkpoint 1 — before Step 2

- [ ] Four rows exist in the `terms` sheet, each with `p10`, `p50`, `p90`.
- [ ] Each term's grounding (trailing data, literature, vendor-upper-bound, attestation) is named in `band-composition-notes.md` Section 1.
- [ ] No `p50` is at the ceiling of the vendor-published range.
- [ ] Timing `p50` is not in month 1 or month 2 unless the rationale is explicit.
- [ ] Attribution frame is named; the band width matches the frame's typical shape.

---

## Step 2 — Run the Monte Carlo composition (20 min)

The mechanics of Monte Carlo on four terms are simple. The chapter's note stands: "A thousand-draw Monte Carlo runs in under a second in a spreadsheet or a short notebook; the mechanics are not the hard part."

### Sample 1,000 draws per term

In the `draws` sheet (or notebook cell), build a 1,000-row × 4-column table. Each row is one Monte Carlo draw; each column is one term.

For the distribution per term, the simplest defensible choice is a **triangular distribution** anchored at `p10`, `p50`, `p90`. A triangular draw matches the three-point summary without assuming normality — appropriate for terms with modest asymmetry. If a term is near-symmetric, a normal distribution with a standard-deviation calibrated to the 10th-90th range (roughly `(p90 - p10) / 2.56` for a normal) is also acceptable.

Pseudocode for one draw (works in a notebook; the spreadsheet equivalent uses `RAND()` + inverse-CDF or a dedicated `TRIANG.INV`-style add-in):

```python
import numpy as np
rng = np.random.default_rng(seed=42)  # seed for reproducibility

def tri(p10, p50, p90, n):
    # map the p10/p50/p90 three-point summary to a triangular distribution
    # with mode p50 and tails extended to cover p10 and p90 approximately
    lo = p10 - 0.1 * (p50 - p10)
    hi = p90 + 0.1 * (p90 - p50)
    return rng.triangular(lo, p50, hi, n)

n = 1000
mag    = tri(p10=MAG_P10,  p50=MAG_P50,  p90=MAG_P90,  n=n)   # $/operator/month
cross  = tri(p10=T_P10,    p50=T_P50,    p90=T_P90,    n=n)   # months
attr   = tri(p10=A_P10,    p50=A_P50,    p90=A_P90,    n=n)   # fraction
cost   = tri(p10=C_P10,    p50=C_P50,    p90=C_P90,    n=n)   # $ total 3yr
```

Set a seed. The lab's output should be reproducible — a Monte Carlo you cannot re-run is not an artifact a Finance partner will trust.

### Compose each draw into a three-year ROI

For each of the 1,000 draws, compute the three-year ROI:

```python
cohort_size = 1800     # operators (from Exercise 02 rollout definition)
horizon_mo  = 36       # months

# gross realised value across horizon, accounting for ramp
# simplest honest model: zero value until crossover, linear ramp over 3 months, then steady state
def gross_value(mag_per_month, cross_month):
    months_steady = max(0, horizon_mo - cross_month - 3)
    months_ramp   = min(3, max(0, horizon_mo - cross_month))
    # ramp contribution: mean value during ramp is half the steady-state value
    ramp_contrib    = months_ramp * (mag_per_month / 2) * cohort_size
    steady_contrib  = months_steady * mag_per_month * cohort_size
    return ramp_contrib + steady_contrib

gross = np.array([gross_value(mag[i], cross[i]) for i in range(n)])
attributed = gross * attr
roi = attributed / cost  # ratio; subtract 1 for net-ROI if your convention requires
```

If your ROI convention is net-ROI (benefit / cost - 1 rather than benefit / cost), apply it uniformly — state the convention in `band-composition-notes.md` Section 2 either way.

The gross-value model above is deliberately simple. A richer model (the full J-curve from Chapter 02, with explicit plateau) is strictly better; this simple form is a floor, not a ceiling. If you built the J-curve in Exercise 02, substitute the J-curve integral for `gross_value` above.

### Checkpoint 2 — before Step 3

- [ ] 1,000 draws per term exist in the `draws` sheet / notebook cell.
- [ ] The seed is set and recorded (so the run is reproducible).
- [ ] Each draw produces a three-year ROI.
- [ ] The ROI convention (gross-ratio vs. net-ROI) is stated in `band-composition-notes.md` Section 2.

---

## Step 3 — Read the composed band and record it (10 min)

In the `roi_distribution` sheet / notebook cell, compute:

- The 10th-percentile of the ROI distribution — `np.percentile(roi, 10)`.
- The 50th-percentile (central / median) — `np.percentile(roi, 50)`.
- The 90th-percentile — `np.percentile(roi, 90)`.

A quick textual histogram helps the Finance partner read the shape — most notebook plotting libraries will do a 20-bin histogram in one line; a spreadsheet frequency-chart over 20 bins works equivalently.

Record in `band-composition-notes.md` Section 3, in the Chapter 02 canonical three-sentence form:

> *The point estimate is <p50>x. The 90% band is <p10>x–<p90>x. The band is wide because <the term that contributes most to spread — see Step 4>; a <specific narrowing event> will narrow the band.*

Chapter 02's remark on band width: "The composed-band width is almost always wider than feels comfortable. A 10th-to-90th-percentile ROI range spanning 50% of the central estimate is normal." If your composed band is tight (say, 15% of the central), re-check your term distributions — the `p10`/`p90` are almost certainly too close together and you have composed a point estimate wearing a band for cover.

### Checkpoint 3 — before Step 4

- [ ] `band-composition-notes.md` Section 3 carries the three-sentence form with `p10`, `p50`, `p90` ROI numbers substituted in.
- [ ] A histogram or frequency chart of the 1,000 ROI samples is attached or referenced.
- [ ] If the band spans less than 25% of the central estimate, Step 1 has been re-checked — tight bands on projected ROI are usually authorial under-statement of uncertainty, not real evidence.

---

## Step 4 — Sensitivity analysis — which term is the ROI most load-bearing on? (15 min)

Chapter 02's sensitivity-analysis discipline: "Sensitivity analysis on the two or three most impactful assumptions shows how ROI moves inside that band and which assumption the ROI is most load-bearing on."

In the `sensitivity` sheet / notebook cell, re-run the Monte Carlo four times — once per term, fixing that term at its `p50` while letting the other three vary. Compare the composed-band width in each run against the full-four-term run.

```python
def recompose_fixing(fixed_term_name):
    terms = {'mag': mag, 'cross': cross, 'attr': attr, 'cost': cost}
    # overwrite the fixed term with its p50 (constant across all draws)
    if fixed_term_name == 'mag':   mag_f   = np.full(n, MAG_P50)   ; return _compose(mag_f, cross, attr, cost)
    if fixed_term_name == 'cross': cross_f = np.full(n, T_P50)     ; return _compose(mag, cross_f, attr, cost)
    if fixed_term_name == 'attr':  attr_f  = np.full(n, A_P50)     ; return _compose(mag, cross, attr_f, cost)
    if fixed_term_name == 'cost':  cost_f  = np.full(n, C_P50)     ; return _compose(mag, cross, attr, cost_f)

for term in ['mag', 'cross', 'attr', 'cost']:
    roi_fixed = recompose_fixing(term)
    p10, p90 = np.percentile(roi_fixed, [10, 90])
    print(f"Fixing {term}: band width = {p90 - p10:.2f}x (vs. full band {FULL_P90 - FULL_P10:.2f}x)")
```

The term whose fixing most *reduces* the band width is the term the ROI is most load-bearing on. For most rollouts, the ranking is: **attribution** > **magnitude** > **timing** > **cost** (cost is often the narrowest contributor because Family 1 is well-sourced and Families 2-6 have smaller dollar weight on the band even when they have larger relative uncertainty).

Record in `band-composition-notes.md` Section 4:

- The ranking of the four terms by contribution to band width.
- The two or three terms the ROI is most load-bearing on.
- One sentence per load-bearing term naming the specific evidence source that would narrow its distribution (e.g., "A cohort-comparison analysis at the end of the first operating quarter will narrow the attribution band from 25%-55% to roughly 35%-50%").

### Checkpoint 4 — before Step 5

- [ ] Section 4 ranks the four terms by contribution to the band width.
- [ ] The two or three most-impactful terms are named explicitly.
- [ ] For each load-bearing term, the specific narrowing evidence source is named.

---

## Step 5 — Red-team against the three Chapter 02 theatre patterns (5 min)

Read `band-composition-notes.md` aloud and check against Chapter 02's three projection-specific theatre patterns:

1. **The hockey-stick projection.** Does the gross-value model (in Step 2) assume steady-state value starts in month 1? If yes, the J-curve has no ramp and the band is understated. Fix: re-insert the ramp region into the gross-value function.
2. **The band that walks.** Does `band-composition-notes.md` Section 3 report a narrower band than the raw 10th/90th percentiles would say? Does the summary slide (if one exists) narrow further? Fix: the narrative must match the computed numbers. If the composed band is 1.2x–3.1x, the summary line is 1.2x–3.1x, not "roughly 2.0x."
3. **Attribution by assertion.** Does Section 1's attribution distribution name its evidence source? "Attribution = 40%, no source" is the pattern. Fix: either cite workflow-interview evidence, cite a cohort-comparison analysis, cite a staggered-rollout design, or widen the distribution dramatically until honest sources are available.

For any pattern present, revise Sections 1-4 before shipping.

### Checkpoint 5 — before Step 6

- [ ] Section 5 addresses each of the three patterns.
- [ ] Any pattern that was present on first pass has been fixed.
- [ ] The three-sentence form in Section 3 reads cleanly: point estimate, band, reason the band is wide, narrowing plan.

---

## Step 6 — Version and route (5 min)

Add a version footer to `band-composition-notes.md`:

```
Version: v0.1 — draft for Finance working session.
Random seed: <recorded above>
Next revision: after the Finance partner's review (expected within 2 weeks).
Changes between versions are logged with date, author, and one-sentence reason.

## Change log

- v0.1 (YYYY-MM-DD) — <your-name> — initial Monte Carlo composition.
```

The worksheet file (`roi-band-monte-carlo.xlsx` or `.ipynb`) ships alongside the notes; the Finance partner should be able to open the worksheet, see the four term distributions, re-run the Monte Carlo against the recorded seed, and arrive at the same percentiles the notes carry. Reproducibility is the trust signal.

## Deliverables

- `roi-band-monte-carlo.xlsx` or `roi-band-monte-carlo.ipynb` — the worksheet / notebook with the four term distributions, 1,000 draws, the composed ROI distribution, and the sensitivity re-runs.
- `band-composition-notes.md` — the five-section writeup covering the term distributions, the composition method, the composed-band read, the sensitivity analysis, and the theatre-pattern self-check.

## Checkpoint — self-evaluation

- [ ] The worksheet / notebook runs reproducibly against the recorded seed.
- [ ] Each of the four term distributions has a `p10`, `p50`, `p90` and a named grounding source.
- [ ] The composed-band Section 3 states the point estimate and the 90% band in the Chapter 02 canonical three-sentence form.
- [ ] The band spans at least 25% of the central estimate (or if narrower, the term distributions have been re-checked and the narrowness is defended).
- [ ] The sensitivity analysis names the two or three terms the ROI is most load-bearing on and specifies the narrowing evidence source for each.
- [ ] None of the three Chapter 02 theatre patterns (hockey-stick, walking band, attribution by assertion) survived the red-team pass.
- [ ] A Finance partner reading `band-composition-notes.md` alone could decide whether to accept, challenge, or counter-propose on each term's distribution without needing the lab author in the room.

## What this lab prepares you for

Exercise 02's narrative Part B leads with a central ROI and composed band in a specific three-sentence form — this lab is where that form has computed numbers behind it. Exercise 03's build-vs-buy matrix requires a composed ROI band per candidate; the composition pattern you ran once here runs three or four times for the matrix. Exercise 05's consolidation economics case requires a composed ROI band on the consolidation move versus the status quo; the same Monte Carlo pattern applies with different term distributions. The lab also exercises the Chapter 02 refusing-the-point-estimate discipline: once you have a composed band, the pressure to ship a point estimate ("just one number for the slide") becomes something you can respond to directly — "the point estimate is Xx; the band is Y-Z; here is the term the band is most load-bearing on" — which is the rhythm Chapter 02 names as the one that makes projected ROI defensible in a budget conversation.
