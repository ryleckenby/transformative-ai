# The Adoption Playbook

A step-by-step guide for running an AI enablement effort with a real team. This is written for the person doing the enabling — an enablement lead, a forward-deployed engineer, a champion inside the team. It assumes tool access and policy already exist (Stage 1 in the [maturity model](01-maturity-model.md)); the goal is to get one team a genuine workflow win (Stage 2), the repeatable unit of transformation.

## Phase 1 — Pick the right team and the right workflow

The single highest-leverage decision. You are choosing a proof, and proofs need favorable conditions.

**Pick a team that:**
- has a leader who *wants* this (pull, not push — never start with a conscripted team)
- feels real pain in a recurring workflow
- can spare a genuine champion a few hours a week

**Pick a workflow that:**
- recurs frequently (daily/weekly, not quarterly) — frequency is what compounds
- has painful, acknowledged friction
- has *checkable output* — someone can quickly verify whether the AI-assisted result is right. Workflows where verification is cheap and production is expensive are the sweet spot.
- is low blast-radius if it goes wrong during the pilot

**Anti-patterns at this phase:** picking the CEO's pet use case, picking the most skeptical team "to prove it works anywhere," picking a workflow that runs twice a year, or picking an open-ended creative task where quality is unfalsifiable.

Use the [discovery question bank](../playbooks/discovery-questions.md) to run this conversation.

## Phase 2 — Map the workflow as it actually is

Sit with the people who do the work. Not the manager's description — the real thing, with all the workarounds, tribal knowledge, and "oh, and then I check this other spreadsheet" steps.

For each step, capture:
- **Input** — what arrives, in what form, from where
- **Judgment** — what decision is actually made here, and what knowledge does it require?
- **Output** — what leaves, to whom
- **Time & pain** — how long, how hated
- **Failure cost** — what happens if this step is wrong

Then classify each step: **mechanical** (transform/route/summarize — automate), **judgment-with-pattern** (expert applies learnable patterns — AI drafts, human verifies), or **true judgment** (accountability, taste, relationships — human leads, AI briefs). Most workflows turn out to be 70% mechanical and judgment-with-pattern; the humans just never had the option to shed them before.

## Phase 3 — Build the thin version

Build the smallest thing that changes the workflow *this week*. Resist the platform temptation.

- Prefer **assistive before autonomous**: AI drafts, human approves. Autonomy is earned by track record, not granted by architecture.
- Put the AI **where the work already happens** (the ticket system, the doc, the IDE) — every context switch halves usage.
- Make the human verification step explicit and cheap: show sources, show reasoning, make "reject and fix" one click.
- Write down the **evaluation criteria** now, however crude — even ten golden examples with expected outputs. You'll thank yourself in Phase 5.

## Phase 4 — Run it side-by-side

For 2–4 weeks, run the new path alongside the old one with the champion and 2–3 volunteers.

- **Measure before/after** on the metrics chosen in Phase 1 (cycle time, throughput, error rate, satisfaction). The [pilot scorecard](../playbooks/pilot-scorecard.md) is the template.
- **Hold a weekly 30-minute retro**: what did the AI get wrong this week? What did people route around? What manual step survived that shouldn't have?
- Expect the dip: weeks 1–2 are often *slower* as habits rewire. Tell everyone this in advance so nobody calls the pilot dead at day 10.

## Phase 5 — Harden or kill

At the end of the pilot window, make an explicit call:

- **Harden:** the win is real → productionize. Add monitoring, expand the eval set, document the workflow, train the rest of the team, and *retire the old path* (a new path that coexists indefinitely with the old one will lose — the old path is muscle memory).
- **Kill:** the win isn't there → say so loudly and in writing. A clean, documented kill builds more credibility than a zombie pilot. Capture *why* (model capability? data access? verification too expensive?) — today's kill is often next year's win when capability improves.

## Phase 6 — Extract and propagate

The pilot's value is only half in the team it helped. The other half:

- **Extract the pattern**, not the artifact: "triage flow: classify → enrich → draft → human gate" transfers; the specific prompt doesn't.
- **Publish the before/after numbers** internally. Nothing recruits the next team like a peer's measured win.
- **Promote the champion** — visibly. The org watches what happens to early movers. If enabling AI is career-positive, you get more champions; if it's invisible extra work, you get none.
- **Feed the platform backlog**: everything the pilot had to hand-roll (data access, evals, deployment) is a candidate for shared infrastructure. This is the enablement version of the [FDE feedback loop](../forward-deployment/01-the-fde-model.md).

Then pick the next team, and run it again. Transformation is this loop, executed relentlessly, with each iteration cheaper than the last.
