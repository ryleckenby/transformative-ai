# Sprint Zero Checklist (Template)

The operational companion to [Sprint Zero: The Agent-Ready Project](../enablement/05-sprint-zero.md). Run this at project inception. With a mature org template most items are instantiation, not invention; if you're inventing here, that's a signal to improve the template after this project. Everything in `[brackets]` gets filled in.

## Scaffold

- [ ] Project instantiated from the org template, version [template version]
- [ ] Standard directory structure in place (knowledge base, intake, meetings, decisions, backlog locations all at their conventional paths)
- [ ] Access granted: [team members, agents, service accounts] with [read/write scopes]
- [ ] Tooling provisioned: [repo, tracker, transcription, agent runtime]
- [ ] Deviations from the template documented with rationale: [none / list]

## AI instructions

- [ ] Org-global instructions inherited and current (version: [x])
- [ ] Project context file written at the root, covering:
  - [ ] purpose, audience, and definition of done
  - [ ] explicit out-of-scope list
  - [ ] project conventions (naming, tone, structure, local definitions)
  - [ ] constraints (compliance, security, stakeholders, dates)
  - [ ] pointers to knowledge base, decision log, backlog, meeting repository
- [ ] Context file reviewed by [problem owner], not just its author
- [ ] Update trigger agreed: context file is revisited [cadence / on every logged decision]

## Skills

- [ ] Global skills manifest attached: [list of active org skills + versions]
- [ ] Project-local skills identified: [list, or "none"]
- [ ] For each local skill: a note on whether it's a candidate for the global library, and what would qualify it (the third project that wants it)

## Personas

- [ ] Delivery personas named to real people: sponsor, problem owner, champion, FDE/lead, platform support, with commitments stated
- [ ] Every standing agent written up as a delivery persona: mandate, write boundaries, escalation triggers, reviewing human and cadence
- [ ] Target personas documented from discovery: goal, pain, protected judgment, verification behavior, and what "better" measurably means to them
- [ ] Target personas wired in: eval criteria reference them, and pipeline outputs tag which persona a proposal or decision affects
- [ ] Personas stored in the project tree (versioned), not in a slide deck

## Knowledge intake pipeline

- [ ] Intake location live: [path/channel]
- [ ] Document type list defined for this project: [requirements, research, reference, contract, ...]
- [ ] Type-to-skill mapping written: each type names the skill(s) that process it
- [ ] Processed-output convention set: where summaries, extractions, and indexes land, and how originals are preserved
- [ ] Human confirmation gate in place for extracted requirements and backlog proposals
- [ ] **Smoke test passed:** a real document dropped in intake came out classified, processed, and filed

## Meeting record pipeline

- [ ] Meeting repository live: [path], and the team knows records go there (or transcription lands automatically)
- [ ] Extraction agent configured with skills for:
  - [ ] action items (proposed as backlog items with owner and date, human-confirmed)
  - [ ] decisions (appended to the decision log with date, deciders, rationale; affected tasks flagged)
  - [ ] task refinement (details attached to existing backlog items)
- [ ] Decision log standing at [path], empty but wired
- [ ] **Smoke test passed:** a real transcript produced action items, decisions, and refinements as proposals

## Backlog

- [ ] Backlog seeded from [charter / intake-processed requirements]
- [ ] Intake and meeting pipelines connected: both can propose items into it
- [ ] Proposal-to-committed flow defined: who confirms, how often

## Definition of done

- [ ] All three smoke tests pass (intake, meeting, onboarding)
- [ ] **Onboarding test:** someone uninvolved in setup (human or agent) can orient in the project from the repository alone and correctly answer: what is this project, what's been decided, what's in flight?
- [ ] Template feedback filed: anything invented or fixed during this sprint zero is reported back to the template owner

---

**Sprint zero completed:** [date] · **By:** [name] · **Template feedback filed:** [link / n/a]
