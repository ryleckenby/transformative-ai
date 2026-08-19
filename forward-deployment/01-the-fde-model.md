# The FDE Model in Detail

## The two-sided team

The classic structure pairs two complementary roles per engagement:

- **The forward-deployed engineer (FDE)** — lives in the customer's context. Owns discovery, integration, workflow design, user trust. Ships the specific.
- **The platform engineer (core/product engineering)** — lives in the product's context. Owns the shared capability: the platform, the primitives, the quality bar. Ships the general.

(Palantir's internal names for these were, memorably, "Delta" and "Dev" — the delta being what you add on top of the platform for one customer.)

The model works when these two sides *trade*: FDEs export requirements-with-evidence ("three customers hand-rolled the same retry logic against SAP — that's a connector"), and platform imports them as product. The trade needs active management; left alone, the two sides drift into mutual resentment — FDEs see platform as slow and precious, platform sees FDEs as hackers generating unmaintainable one-offs. Healthy orgs force the contact: rotations (FDEs do platform tours and vice versa), shared roadmap reviews where deployment evidence sets priorities, and a explicit "graduation" process for promoting deployment code into platform.

## The economic logic

Forward deployment is expensive per engagement — senior generalist engineers, travel, long cycles. It's justified by three compounding effects:

1. **Deal/engagement economics:** embedded engineers unlock deployments that would otherwise die in the gap between "bought the platform" and "changed the operation." The revenue (or internal value) carried by the engagement pays for the humans.
2. **Product compounding:** each engagement's generalized learnings reduce the marginal cost of the next. The strategic goal of every FDE org is to *shrink its own necessity per deployment* — more product, less bespoke labor, over time.
3. **Information advantage:** FDEs are the highest-bandwidth sensor an AI product company has. They see how work actually happens inside customers — what breaks, what's trusted, what's worth money. In a fast-moving capability landscape, that ground truth is worth more than any amount of market research.

The bear case and its management live in [04-failure-modes-and-critiques.md](04-failure-modes-and-critiques.md).

## Why AI made this model newly central

Pre-AI, forward deployment was a niche answer for heavyweight data platforms. Three things changed:

1. **The capability became general.** A frontier model can plausibly help with *most* knowledge work, which means the question "what should we do with it?" has too many answers. Discovery — the FDE's core skill — became the bottleneck.
2. **The last mile stayed stubbornly specific.** Context engineering, data access, evaluation against the customer's actual quality bar, workflow integration, trust-building with the humans in the loop — none of this ships in a box.
3. **The frontier moves quarterly.** What was impossible at engagement start may be easy by engagement end. Someone on the ground has to keep re-mapping capability to opportunity; a static integration calcifies in months. FDEs are the mechanism by which deployments track the frontier.

There's also a subtler shift: **AI tooling makes FDEs dramatically more productive.** An embedded engineer with agentic coding tools can produce in a week what took a quarter — which changes the economics of "bespoke" and lets a small embedded team credibly rebuild a workflow rather than just advise on it. The pattern's costs fall as the capability it deploys improves; forward deployment is one of the few org models that gets *cheaper* as AI gets better.

## The skill profile (hiring and growing FDEs)

What to look for, in rough priority order:

1. **Problem discovery in foreign domains.** Can they sit with an expert in a domain they've never seen and locate the leverage within days? Test in interviews with case walk-throughs of an unfamiliar workflow.
2. **Shipping bias under mess.** Comfort producing the thin working version against legacy systems, partial data, and shifting requirements. Portfolio question: "tell me about something you shipped in a place where shipping was hard."
3. **Trust-building.** The users an FDE serves are often skeptical, sometimes threatened. The job is partly to make *their* judgment more powerful, and to be seen to. Watch for ego-per-unit-competence; low is better.
4. **Full-stack pragmatism over depth.** Breadth (data plumbing, a bit of frontend, evals, prompting/agents, deployment) beats depth in one layer. Depth can be borrowed from platform; breadth can't be.
5. **Written communication.** The feedback loop runs on field reports. An FDE who ships but can't crystallize what they learned into transferable writing captures only half the role's value.

Common sourcing profiles: strong product engineers who are bored of pure feature work; ex-founders; solutions architects who want to build rather than demo; scientists/analysts who learned to ship. The role burns people out via travel and context-switching — plan rotations (a platform tour every few engagements) as retention infrastructure, not as a perk.

## Operating disciplines that keep the model healthy

- **Field reports as a first-class artifact.** Every engagement produces structured written learnings on a cadence — what worked, what the platform lacked, what surprised. These are read; roadmap reviews cite them.
- **The graduation path.** A named process by which deployment-specific code becomes platform capability (nomination → hardening → ownership transfer). Without it, generalization happens never.
- **Engagement ends are designed.** Every engagement has a handoff plan from day one ([lifecycle](02-engagement-lifecycle.md)). FDEs who become permanent fixtures at one customer have converted into expensive staff augmentation.
- **A "no bespoke forever" ledger.** Track per-customer custom surface area. It should trend down as the platform absorbs patterns; if it trends up, you're accreting a consultancy.
