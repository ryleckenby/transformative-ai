# Forward Deployment: An Overview

## What it is

**Forward deployment** is the practice of sending engineers *to the problem*: embedding them with the customer or team that owns a real workflow, having them build working software in that context, and feeding what they learn back into a shared product or platform.

The name comes from the military notion of forward-deployed forces, stationed where the action is rather than at headquarters. In software, the term was popularized by **Palantir**, whose *forward-deployed engineers* (FDEs) embedded with customers (intelligence agencies, manufacturers, banks), configuring and extending the core platform against messy, real data and real operational pain. Whatever one thinks of any particular company, the organizational pattern proved something important: for problems where **the gap between capability and value lives inside the customer's context**, embedded engineers close that gap faster than any amount of documentation, sales engineering, or professional services at arm's length.

The AI era has made the pattern mainstream. Frontier labs and AI product companies now hire FDEs in volume, for a simple reason: **modern AI is a general-purpose capability whose value is realized only through workflow-specific integration.** The model can do the work; someone has to discover *which* work, wire it into the systems where the work lives, and earn the trust of the people whose work it is. That someone is the forward-deployed engineer.

## The defining feedback loop

What separates forward deployment from consulting is not the embedding; consultants embed too. It's the **loop**:

```
   platform / product
     │            ▲
     │ deploy     │ generalize
     ▼            │
   embedded engagement ──► customer/team value
```

- **Consulting:** value flows to the client; learning walks out the door with the consultant; every engagement starts near zero.
- **Forward deployment:** every engagement makes the *platform* better. The recurring pain becomes a product feature, the hand-rolled integration becomes a connector, the improvised eval becomes shared harness. Engagement N+1 is cheaper than engagement N. The economics compound.

This loop is the test. If your embedded engineers' learnings have no product or platform to flow back into, you are running a consultancy (which is a fine business, but a different one, with linear rather than compounding economics).

## Two arenas for the same pattern

This repo treats forward deployment as one pattern with two arenas:

1. **External (vendor to customer):** an AI company embeds FDEs with customers to turn a platform into deployed value. This is the classic Palantir-style motion, now standard across AI companies.
2. **Internal (platform team to business team):** an enterprise's own AI/platform/enablement group embeds engineers with business teams (finance, support, legal, ops) to produce the [workflow wins](../enablement/02-adoption-playbook.md) that drive adoption. Same loop, same skills, same failure modes; the "customer" just shares your badge. Covered in [03-internal-forward-deployment.md](03-internal-forward-deployment.md).

The internal arena is the bridge to this repo's other half: **internal forward deployment is the strongest known mechanism for AI enablement.** It replaces the slide-factory center of excellence with people who ship.

## What an FDE actually is

A hybrid role, roughly: 60% engineer, 25% product manager, 15% diplomat.

- **Engineer:** ships working software against ugly, real constraints (legacy systems, half-documented data, security regimes). Bias for the thin working version over the elegant architecture.
- **Product manager:** discovers what's actually valuable (not what was asked for), scopes ruthlessly, defines success measurably.
- **Diplomat:** builds trust with users who may be skeptical or threatened, navigates the org chart, manages stakeholders who control data, access, and budget.

The rarest and most load-bearing skill is **problem discovery in someone else's domain**: sitting with a claims adjuster or a compliance analyst and, within days, understanding their work well enough to see where the leverage is. Deep technical skill without this produces beautiful solutions to the wrong problems.

## When forward deployment is the right model

Strong fit when:
- value depends on **context that can't be shipped in a box**: proprietary data, idiosyncratic workflows, regulatory particulars
- the capability is **general but the last mile is specific** (this is the AI deployment problem in one line)
- engagements can **feed a platform**: there is somewhere for learning to compound
- deals/engagements are **large enough** to carry the cost of embedded humans

Weak fit when:
- the product is genuinely self-serve and the workflow is uniform (just build the product)
- there's no platform to feed (you're choosing consulting; choose it deliberately)
- it's being used to **paper over product gaps forever**: FDEs as permanent human duct tape is the pattern's best-known pathology (see [04-failure-modes-and-critiques.md](04-failure-modes-and-critiques.md))

## What this section covers

| Doc | Question it answers |
|---|---|
| [01-the-fde-model.md](01-the-fde-model.md) | How the role and the feedback loop work in detail |
| [02-engagement-lifecycle.md](02-engagement-lifecycle.md) | How a single engagement runs, kickoff to handoff |
| [03-internal-forward-deployment.md](03-internal-forward-deployment.md) | How to run this motion inside your own org |
| [04-failure-modes-and-critiques.md](04-failure-modes-and-critiques.md) | Where the model breaks, and the honest case against it |
