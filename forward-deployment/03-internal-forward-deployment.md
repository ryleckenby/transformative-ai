# Internal Forward Deployment

Running the FDE motion inside your own organization: a small team of embedded engineers, deployed to business teams, producing workflow wins and feeding a shared platform. This is the strongest known implementation of [AI enablement](../enablement/00-overview.md); it replaces the center of excellence that advises with a center that ships.

## Why internal FDEs beat the alternatives

| Alternative | Why it underperforms |
|---|---|
| Center of excellence (advisory) | Produces guidance, not deployments; becomes a [slide factory](../enablement/03-failure-modes.md) |
| Every team fends for itself | Enthusiast teams win, everyone else stalls; no pattern reuse; tools sprawl |
| Big-bang vendor rollout | Tool-first thinking; nobody redesigns the workflows; adoption theater |
| External consultants | Can genuinely help, but learning walks out the door and unit economics never improve |
| **Internal FDEs + platform** | Ships workflow wins *and* compounds them into shared capability |

The internal arena is also *easier* than the vendor arena in key ways (no procurement wall, shared incentives on paper, one badge) but harder in one: the "customer" didn't pay, so their commitment is softer. This makes [qualification](02-engagement-lifecycle.md) *more* important internally, not less. Only engage where there's pull.

## Minimum viable shape

You don't need a department. The smallest real version:

- **2 to 3 FDE-profile engineers** (see [skill profile](01-the-fde-model.md)): product-minded, full-stack-pragmatic, comfortable in other people's domains
- **1 platform-inclined engineer** curating what deployments produce into reusable patterns (shared prompts/agents, connectors, eval harness, deployment templates)
- **An executive sponsor** who clears access blockages and protects the team from being reassigned to whatever's on fire
- **A funnel and a queue**: teams request engagements; the FDE group qualifies hard and runs 1 to 2 concurrent engagements per FDE, max

Run each engagement by the [lifecycle](02-engagement-lifecycle.md). Measure the program by the [scorecard discipline](../enablement/04-measuring-impact.md): stacked one-page workflow wins, time-to-value trending down, pattern reuse trending up.

## Design decisions that matter

**Where it reports.** Under a CTO/CIO it risks tool-first drift; under a COO or business unit it risks becoming one unit's private team. Either works *if* the charter is explicit: the team's product is *workflow wins across the org plus the platform they feed*, and its scorecard says so.

**Funding.** Central funding for the first year; chargebacks at the start create a sales motion before there's a track record. Introduce partial chargeback later as demand exceeds supply. By then teams are bidding with real problems, which is itself a qualification mechanism.

**Rotation as a feature.** Internal FDE is a phenomenal development role; engineers learn the business end to end. Deliberately rotate high-potential engineers through 6-to-12-month FDE tours and back into product and platform teams. Every alum becomes an embedded champion where they land, and the org's overall AI fluency compounds. (This also mitigates burnout, the role's chronic hazard.)

**The champion interface.** Each engagement recruits and trains a champion inside the host team ([playbook phase 6](../enablement/02-adoption-playbook.md)). The FDE leaves; the champion stays; the champions network becomes the org's distributed enablement layer. Internal FDEs without champion-building scale linearly (bad); with it, they scale like a network (good).

**The platform discipline.** Same rule as the vendor arena: platform components are extracted from deployments (third-time rule), never speculated. The internal platform's backlog *is* the stack of field reports.

## A realistic first-year arc

- **Q1:** Recruit the seed team (internally; the profiles usually exist and are bored). Qualify hard; run 2 engagements in pull-heavy teams with frequent, measurable workflows. Capture baselines religiously.
- **Q2:** Ship the first two wins; publish before/after numbers internally, champion-fronted. Start the pattern library from what got hand-rolled. Queue forms.
- **Q3:** 3 to 4 engagements, at least one reusing patterns from the first half (time-to-value should visibly drop). First clean kill; publicize it too, because it buys enormous credibility. First rotation begins.
- **Q4:** The scorecard stack goes to leadership; funding conversation is about *rate of expansion*, not existence. First Stage-3 signs: teams self-serving on patterns without an engagement.

The failure version of this arc: the team gets pulled onto an executive pet demo in Q1, produces impressive theater, captures no baselines, and by Q4 is defending its existence with activity metrics. Every element of the discipline above exists to prevent that specific movie.
