# Sprint Zero: The Agent-Ready Project

*(Also called stage zero. Not to be confused with Stage 0 in the [org maturity model](01-maturity-model.md), which describes an organization's overall adoption posture. Sprint zero is per-project: the setup phase before the real work starts.)*

## What sprint zero means now

Traditionally, sprint zero was plumbing: create the repo, wire up CI, provision environments, seed the backlog. Necessary, mechanical, mostly forgettable.

In an AI-era project, sprint zero has a second job that is neither mechanical nor forgettable: **onboarding the agents.** A project team now includes AI agents as working members, and agents are only as good as the context, instructions, and skills they're given. A project isn't set up when the humans can start working; it's set up when *both humans and agents* can act with full context.

The core claim: **project setup should be a predefined, repeatable process, not an improvisation.** Every project in the org starts from the same scaffold, the same way every deployment draws on the same platform. This is the [third-time rule](../GLOSSARY.md) applied to project inception: you've set up enough projects that the setup itself should be an extracted, versioned asset.

Consistency here isn't bureaucratic tidiness. It's what makes everything downstream cheaper:

- **Agents thrive on convention.** An agent that knows every project keeps decisions in `decisions/`, meeting records in `meetings/`, and its operating instructions at the root can work in any project on day one. Bespoke layouts mean re-teaching context per project, forever.
- **Skills become portable.** A skill written against a standard structure works across the whole portfolio. A skill written against one project's quirks works once.
- **Improvements propagate.** Fix the template once and every future project inherits the fix. Improvise per project and every lesson stays local, which is the same [feedback-loop failure](03-failure-modes.md) this repo catalogs at org scale.

## The four layers of the setup process

A predefined sprint-zero process has four layers, from generic to project-specific:

### 1. Setup instructions
The bootstrap layer: how to instantiate the project itself. Repo creation from the template, directory scaffold, access and permissions, tool provisioning, environment configuration. Written so that an agent can execute most of it, with a human approving the irreversible steps. If setup takes more than a session, the template needs work.

### 2. Instructions for the AI
The context layer: what every agent working in this project needs to know. Typically a root-level context file (the project's standing brief) covering:

- what the project is, for whom, and what done looks like
- scope boundaries: what this project explicitly is not
- conventions: naming, structure, tone, definitions specific to this project
- constraints: compliance, security, stakeholders, deadlines that shape decisions
- pointers: where the knowledge base, decision log, backlog, and meeting records live

Instructions are layered, like configuration: **org-global instructions** (how we work everywhere) are inherited, **project instructions** override and extend them, and **task-level instructions** ride on individual pieces of work. Write each fact at the highest layer it's true at, so it's maintained once.

### 3. Global skills
The capability layer: the organization's shared library of skills, inherited by every project. A skill is a packaged, versioned procedure an agent can apply: how we summarize a research document, how we extract action items from a transcript, how we draft a status update, how we run a security pass. Global skills are the project-level face of the [platform](../GLOSSARY.md): maintained centrally, improved from field experience, and available everywhere so no project rebuilds them. A project may add its own local skills, but a local skill that a second and third project wants is a graduation candidate for the global library.

### 4. Defined processes
The wiring layer, and the part that makes the project genuinely agent-ready: standing pipelines that connect *types of information* to *the skills that process them*. The two workhorses are below.

## Process one: the knowledge intake pipeline

Every project accumulates supporting material: requirements documents, research, vendor specs, prior art, reference designs, background reading. In most projects this lands wherever it lands (email, chat, someone's drive) and its contents live only in the heads of whoever read it.

The agent-ready version: the project has a **designated intake location** (an inbox directory, a watched folder, a channel), and an agent processes everything that arrives:

1. **Classify.** What kind of document is this? Requirements, research, reference, contract, data dictionary, something else?
2. **Route to the associated skill(s).** Each document type maps to one or more skills that define what "processed" means for that type. A research paper gets summarized with findings-relevant-to-this-project extracted. A requirements doc gets decomposed into candidate backlog items and constraints. A vendor spec gets its integration-relevant details indexed. The type-to-skill mapping is part of the project template and extended per project.
3. **File and link.** The processed output lands in the project knowledge base: summarized, indexed, cross-linked to the tasks and decisions it touches, with the original preserved alongside.

The result is a **living knowledge base** instead of a document graveyard: any agent (or human) joining the project can query what's known, and nothing important is trapped in an unread PDF. The intake agent runs assistive-first, consistent with the repo's [default posture](../GLOSSARY.md): it proposes summaries, extracted requirements, and links, and a human accepts them cheaply.

## Process two: the meeting record pipeline

Meetings are where projects actually change course, and meeting knowledge is the most perishable knowledge there is. The agent-ready project treats meeting records as first-class input:

- **A standing repository** for meeting notes and transcriptions, populated as a habit (or automatically, where transcription is in place).
- **An agent with meeting-processing skills** that runs over each new record and produces three kinds of output:
  1. **Action items.** Commitments and asks detected in the discussion, drafted as backlog items with proposed owners and due dates, routed to a human for confirmation.
  2. **Decisions.** Determinations that affect the project: scope changes, approach choices, priority calls. Each is appended to the **decision log** with date, deciders, and rationale, and, critically, checked against existing work: which open tasks, documents, or assumptions does this decision affect? Flag them.
  3. **Task refinement.** Discussion that adds detail to existing work: acceptance criteria mentioned in passing, constraints surfaced, estimates revised. The agent attaches the refinement to the relevant backlog items rather than letting it evaporate.

The quiet payoff is the decision log. Most projects cannot answer "when did we decide X, and why?" six weeks later. A project where every meeting is swept for decisions can, and agents working in the project can consult the log before proposing something that was already ruled out.

## What sprint zero must leave behind

By the end of sprint zero, these artifacts exist and are wired together:

| Artifact | What it is |
|---|---|
| Project scaffold | Standard structure, instantiated from the org template |
| AI instructions | Root context file, inheriting org-global instructions |
| Skills manifest | Which global skills are active, plus any project-local ones |
| Knowledge base + intake | The inbox, the type-to-skill mapping, the processed store |
| Meeting repository + pipeline | The record store and the extraction agent behind it |
| Decision log | Empty but standing, fed by the meeting pipeline |
| Backlog | Seeded, and connected so intake and meetings can propose into it |

**The definition of done is a test, not a checklist review:** drop a real document into the intake and watch it get classified, processed, and filed. Feed in a real meeting transcript and watch action items, decisions, and refinements come out as proposals. A new member, human or agent, can onboard from the repository alone, with no oral tradition required. If those three things work, sprint zero is done.

The operational checklist version of this doc lives at [playbooks/sprint-zero-checklist.md](../playbooks/sprint-zero-checklist.md).

## Anti-patterns

- **Improvised setup.** Every project laid out differently, so every skill and every agent needs per-project adaptation. The whole point is the standing template; if a project deviates, the deviation should be an argued exception, not a default.
- **Write-once instructions.** The context file is written at kickoff and never touched again, drifting from reality until agents are working from fiction. Instructions are living artifacts; the meeting pipeline's decision log is one natural trigger for updating them.
- **Local skill sprawl.** Each project rebuilds its own meeting summarizer, its own document processor. Same disease as the org-level [platform-before-proof failure mode](03-failure-modes.md) in reverse: proof exists everywhere, and nothing gets extracted.
- **Unbounded intake autonomy.** The pipelines write directly into the backlog and decision log with no human gate. Wrong action items and phantom decisions poison trust in the whole system fast. Proposals in, human confirmation, then commitment: autonomy is widened later, on track record.
- **Sprint zero as a fortnight of ceremony.** With a real template, sprint zero is measured in hours or days. If it's taking weeks, you're building the template inside the project (do it once, outside) or gold-plating scaffolding the project hasn't earned yet.
