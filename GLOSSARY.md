# Glossary

Shared vocabulary for this repo. Half the arguments in this space dissolve once terms are pinned down; here's where we pin them.

**Adoption theater**: Activity that resembles AI adoption (licenses, trainings, active-user dashboards) without change in how work is done. Detectable by asking for three named workflows with before/after numbers. See [failure modes](enablement/03-failure-modes.md).

**AI enablement**: The organizational function that converts AI access into changed workflows: embedded practice, champions, shared infrastructure, and outcome measurement. Not provisioning, not training, not governance; the connective tissue among them. See [enablement overview](enablement/00-overview.md).

**Assistive-before-autonomous**: The default deployment posture: AI drafts, a human approves, and autonomy is widened only as a measured track record accumulates. The cheapest known insurance against [trust collapse](enablement/03-failure-modes.md).

**Champion**: A member of the host team (not the enablement team) who carries the new workflow after the engagement ends, with allocated time and visible credit. The interface through which embedded wins become durable local practice.

**Coverage**: Work that gets done post-AI that simply didn't get done before (the tests never written, the follow-ups never sent). The most under-reported win category, and often the least politically fraught.

**Decision log**: The project's standing record of determinations that changed its course: what was decided, when, by whom, and why. Fed by the meeting record pipeline; consulted by agents and humans before re-litigating or contradicting settled questions. See [sprint zero](enablement/05-sprint-zero.md).

**Eval set / golden examples**: Real inputs with known-good outputs, collected from the actual workflow, used to test AI behavior before and after any change (model, prompt, agent, config). The unit of quality assurance for deployed AI; also the preserved seed that lets a killed pilot be cheaply re-tested when capability improves.

**FDE (forward-deployed engineer)**: An engineer embedded with the customer or team that owns a problem, who ships working software in that context and feeds learnings back to a platform. Roughly 60% engineer, 25% product manager, 15% diplomat. See [the FDE model](forward-deployment/01-the-fde-model.md).

**Field report**: The structured written learnings an FDE delivers at engagement end: platform gaps hit, components hand-rolled, surprises found. The document that makes the feedback loop real rather than aspirational.

**Forward deployment**: The pattern of embedding engineers where the problem lives, building with the problem's owners, and generalizing what's learned into shared capability. Distinguished from consulting by the feedback loop, not by the embedding. See [overview](forward-deployment/00-overview.md).

**Graduation**: The named process by which deployment-specific code or patterns are promoted into platform capability (nominate, harden, transfer ownership). Without a graduation path, generalization happens never.

**Human duct tape**: The pathology in which skilled embedded humans quietly bridge product gaps so competently that the product never feels the pressure to close them. See [critiques](forward-deployment/04-failure-modes-and-critiques.md).

**Internal forward deployment**: The FDE motion run inside one organization: platform/enablement engineers embedding with business teams. The strongest known implementation of AI enablement. See [internal forward deployment](forward-deployment/03-internal-forward-deployment.md).

**Invisible backlog**: The queue of work an organization has silently agreed not to do because it was uneconomical pre-AI. A prime discovery target: wins here add capacity without displacing anyone's current role.

**Judgment-with-pattern**: Work that feels like expertise but consists of applying learnable patterns (the thing a new hire "takes longest to get good at"). The center of the AI opportunity: AI drafts, the expert verifies.

**Kill (clean)**: Ending a pilot that didn't hit its target: explicitly, in writing, with reasons and a preserved eval set. A legitimate outcome that builds program credibility; distinguished from the zombie pilot, which ends never and proves nothing. "Not yet" and "no" are different verdicts.

**Knowledge intake pipeline**: A project's designated landing zone for supporting documents (requirements, research, specs, reference material) plus the agent that classifies each arrival by type and processes it with the skill(s) mapped to that type, filing the result into a living knowledge base. See [sprint zero](enablement/05-sprint-zero.md).

**Paved road**: Governance delivered as pre-approved patterns, tools, and data tiers that teams can use without asking, with review reserved for novel risk. The alternative to governance-as-veto.

**Personas (delivery / target)**: The two "who" definitions a project writes down in sprint zero. Delivery personas are who runs the project, humans and standing agents alike, each with a mandate, boundaries, and escalation rules; target personas are who the project serves, captured as design and evaluation inputs (goal, pain, protected judgment, verification behavior). See [sprint zero](enablement/05-sprint-zero.md).

**Pilot graveyard**: An org's accumulation of impressive demos that never reached production, usually because production constraints (access, compliance, ownership) were deferred past the point of confrontation.

**Platform (in this repo's sense)**: The shared, reusable layer that embedded engagements draw on and feed: patterns, connectors, eval harnesses, deployment templates. Legitimate only when extracted from real deployments (see *third-time rule*).

**Problem owner**: The person who does the workflow daily and answers for its output. Distinct from the sponsor; an engagement with a sponsor but no problem owner is a demo in progress.

**Skill**: A packaged, versioned procedure an agent can apply: how to summarize a research document, extract action items from a transcript, run a security pass. Global skills are maintained centrally and inherited by every project; a project-local skill wanted by a third project is a graduation candidate. See [sprint zero](enablement/05-sprint-zero.md).

**Sprint zero (stage zero)**: The per-project setup phase, expanded for the AI era: instantiate the standard scaffold, write the AI instructions, attach the skills manifest, and wire the standing pipelines (knowledge intake, meeting records) so agents are working project members from day one. Done when the smoke tests pass, not when the checklist is read. Distinct from Stage 0 of the org [maturity model](enablement/01-maturity-model.md). See [sprint zero](enablement/05-sprint-zero.md).

**Stage 2 / workflow win**: The repeatable unit of AI transformation: one recurring workflow, redesigned with AI in the loop, with a measured before/after. See the [maturity model](enablement/01-maturity-model.md).

**Third-time rule**: Build a shared component when the third deployment needs it. Not the first (speculation), not the tenth (waste).

**Thin path / thin version**: The smallest end-to-end version of a redesigned workflow that touches real data and real users. Ships in weeks; exists to start the learning loop, not to be the final architecture.

**Verification asymmetry**: The property that makes a workflow AI-suitable: producing the output is expensive, checking it is cheap. Workflows with cheap verification tolerate imperfect AI safely; workflows where checking costs as much as doing need much higher autonomy standards.

**Zombie pilot**: A pilot that neither hardens nor dies: no verdict, dwindling usage, standing agenda item. Worse than a clean kill because it consumes credibility and blocks the honest lesson.
