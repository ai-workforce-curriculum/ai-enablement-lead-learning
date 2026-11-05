# The AI Center of Excellence Pattern Family

> Centers of Excellence are an old shape — enterprises have organized data, analytics, cloud, DevOps, lean, and security around them for decades. The AI CoE is not a new invention; it is an existing operating-model pattern pointed at a new capability. Your job is to pick the variant of that pattern that fits your organization, not to invent one.

## Why "pattern family" and not "the AI CoE"

There is no single AI Center of Excellence. There are four recurring shapes in how enterprises organize a cross-cutting capability, and the AI CoE is the latest thing to be arranged into one of them. Each shape has a different center of gravity, a different funding model, and a different failure mode. The four shapes:

1. **Hub (centralized)** — one central team does the work on behalf of the business.
2. **Hub-and-spoke** — a central team sets standards and runs a service catalog; embedded people in each BU execute against it.
3. **Federated** — BUs own AI work; a thin coordination layer aligns standards, surfaces reuse, and runs shared services (procurement, licensing, policy).
4. **Embedded** — AI responsibility is inside existing teams, with no central group — the "CoE" is a community of practice, not a budget line.

These are not named standards in a published spec; they are the recurring patterns consulting firms and enterprise architecture groups describe when documenting how shared-capability groups are organized. Treat them as a map, not a taxonomy.

## Shape 1 — Hub (centralized)

**Center of gravity:** one central team does the AI work. Business units bring problems; the central team scopes, builds (or commissions), rolls out, trains, and measures.

**When it fits:**
- The organization is small enough (or AI maturity is early enough) that one team can realistically serve all BUs.
- Regulatory posture requires tight control over who touches models with what data — centralization is the simplest audit story.
- The BUs do not yet have anyone technical enough to own adoption locally.

**When it breaks:**
- The hub becomes the bottleneck. The intake queue grows faster than the team ships.
- The hub loses touch with BU context; recommendations feel generic.
- Shadow AI thrives in the gap between what the hub can deliver and what people need this week.

**Funding shape:** central budget line, often reporting to CIO, COO, or CAIO. BUs do not pay per use; demand is unbounded, which is the central weakness.

**Staffing shape:** central enablement leads, central training production, central policy co-authors, central champion program manager. Small team — usually 4–12 FTE even at large enterprises.

## Shape 2 — Hub-and-spoke

**Center of gravity:** a central hub sets the standards and runs the shared services (policy, approved-tool envelope, training content, measurement framework, licensing). Each BU has a named "spoke" — an embedded enablement partner, an AI champion lead, or an AI product manager — who runs adoption inside their BU against the hub's standards.

**When it fits:**
- The organization is big enough that one hub cannot know each BU's workflows.
- BUs are distinct enough (manufacturing + retail + banking under one corporate roof) that a single playbook does not transfer.
- You can staff the spoke roles — they're hard to hire, and promoting from within is usually better than external recruitment.

**When it breaks:**
- Spokes drift. Without a strong hub cadence, each BU ends up with a parallel operating model and the "hub standards" are honored in the breach.
- The hub overspecifies and the spokes become ticket-takers; adoption slows because every decision escalates.
- The reporting line is fuzzy — spokes report to the BU, dotted-line to the hub, and the dotted line is where accountability lives, which means it doesn't.

**Funding shape:** hub funded centrally; spokes funded by their BU (which signals BU commitment and prevents the hub from becoming a free resource).

**Staffing shape:** hub keeps the central enablement leads, policy co-authors, training producers; each BU funds a spoke (embedded enablement partner or equivalent). This is the most common shape for large enterprises that have moved past the first wave of AI adoption.

## Shape 3 — Federated

**Center of gravity:** BUs own their AI work. A thin layer at the center does only what has to be done once — vendor contracts, enterprise-license arbitrage, policy alignment with legal / security / privacy, cross-BU reuse, regulator-facing evidence.

**When it fits:**
- BUs are substantially autonomous (common in holding-company structures, in multi-brand groups, in financial services where each business line has its own regulator).
- The BUs already have strong product / engineering / analytics capability and do not need central delivery.
- The cost of central coordination would exceed the benefit — the organization cannot plausibly agree on a single training curriculum because the jobs are too different.

**When it breaks:**
- Five BUs each buy a different enterprise copilot; the organization pays five times and the BUs don't share champions, playbooks, or failures.
- Policy fragments. The acceptable-use policy says different things in different BUs and legal cannot reconcile them under audit.
- Executive reporting rolls up to a single board, but the underlying scorecards are not comparable — the board cannot tell whether AI investment is working.

**Funding shape:** BU-funded AI programs; a small central-coordination budget (often inside CIO or CAIO office).

**Staffing shape:** each BU has its own AI enablement lead; a tiny central team (1–3 FTE) runs vendor management, policy liaison, and the cross-BU operating ritual.

## Shape 4 — Embedded (community of practice)

**Center of gravity:** no central group. AI responsibility sits inside existing roles — team managers, L&D, legal, security. A community of practice (voluntary, cross-cutting) is the only "CoE" in the room.

**When it fits:**
- The organization is small (sometimes <500 people) and does not need a formal CoE.
- The organization is philosophically against central bureaucracy — flat, engineer-heavy, product-led cultures where a central group would be rejected.
- AI capability is already distributed and mature enough that centralizing would slow things down.

**When it breaks:**
- No one owns the intake. "Everyone" and "no one" are the same answer when a regulator asks who approved the use of a specific tool on specific data.
- Policy co-authoring has no home. Legal, security, and privacy each write their own thing; they don't line up.
- The role you are reading about — the AI Enablement Lead — does not formally exist in this shape. It is instead distributed across L&D, IT, and a couple of enthusiastic ICs.

**Funding shape:** no central AI budget; AI spend is absorbed into existing cost centers.

**Staffing shape:** none at the center. This is the shape many organizations *claim* to have before they realize they have an operating-model problem.

## Choosing a shape — the rough decision

Three factors matter more than the rest:

- **Organization size and BU autonomy.** Small + unified → hub. Big + unified → hub-and-spoke. Big + autonomous BUs → federated. Small + flat culture → embedded.
- **Regulatory posture.** Heavily regulated organizations (healthcare, finance, defense) tend toward hub or hub-and-spoke because a central audit story is cheaper than defending four of them. Lightly regulated organizations can afford federated.
- **AI maturity.** Early-stage adoption needs a hub to seed the capability. Mature adoption can shed the hub and move toward federated or embedded; most do not, because the hub becomes load-bearing for training and policy even after BUs run their own programs.

There is one trap. Executives with consulting backgrounds are biased toward **hub** (it is the cleanest to describe on a slide). Line-of-business leaders are biased toward **federated** (it preserves their autonomy). Neither bias is wrong, but neither is a rationale. A defensible rationale names the specific organizational facts the shape follows from.

## What the shape determines

Once you've chosen a shape, several downstream choices follow mechanically:

- Reporting line and the scope contract from Chapter 01.
- Whether the staffing plan funds spokes or not.
- The funding model (central vs. BU-paid vs. charge-back).
- The service catalog scope — a federated center publishes vendor contracts and policy; a hub publishes the entire enablement menu.
- Whether the champion network is one network or N federated networks that meet in the community of practice.

Chapter 03 picks up with the operating-model design that follows the shape choice.

## Summary

- The AI CoE is one of four long-standing shapes for shared capability: hub, hub-and-spoke, federated, embedded.
- Pick on size, BU autonomy, regulatory posture, and maturity — not on bias.
- The shape choice is the first *irreversible-ish* decision; the operating-model design flows from it.
- Hub-and-spoke is the modal choice at large enterprises in the current cycle; it is not therefore the right choice for *your* organization.
