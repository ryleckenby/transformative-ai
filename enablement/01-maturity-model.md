# An AI Adoption Maturity Model

Maturity models are easy to abuse; they can become vanity ladders. Use this one diagnostically: identify where each *team* (not the org as a whole) sits, and apply the tactics for the next stage. Different teams in the same org are almost always at different stages, and that's fine.

## The five stages

### Stage 0: Latent
**Signature:** AI use is individual, unsanctioned, or absent. Maybe a policy exists; maybe it's a ban.

- **What it looks like:** A few people quietly use consumer chatbots. Leadership is either unaware or anxious. No shared tooling.
- **The trap:** Staying here out of risk aversion while competitors compound.
- **Next step:** Sanctioned access to a capable tool, a clear acceptable-use policy that says *yes* more than *no*, and visible executive use.

### Stage 1: Access
**Signature:** Tools are provisioned; usage is shallow and individual.

- **What it looks like:** Licenses everywhere, prompting 101 sessions, usage concentrated in drafting and summarization. Metrics tracked: seats, weekly active users.
- **The trap:** Declaring victory on activity metrics. This is the "adoption theater" stage: lots of motion, little change in how work gets done.
- **Next step:** Pick 2 to 3 high-friction workflows in willing teams and go deep (Stage 2 tactics). Stop measuring seats; start measuring workflow outcomes.

### Stage 2: Workflow wins
**Signature:** A handful of redesigned workflows show measurable, attributable improvement.

- **What it looks like:** Support triage cut from hours to minutes; contract review first-pass done by AI with human verification; engineering teams with agentic coding integrated into their loop. Each win has a named owner and a before/after measurement.
- **The trap:** Wins stay local. The team that built the support-triage flow never shares the pattern; five other teams rebuild it badly or not at all.
- **Next step:** Extract patterns into shared infrastructure. Stand up the champions network. This is where an internal forward-deployment motion earns its keep.

### Stage 3: Platform
**Signature:** Reusable capability (patterns, agents, evaluation harnesses, data access) lets each new workflow win cost less than the last.

- **What it looks like:** A small platform/enablement group maintains shared components; embedded engineers rotate through business teams; time-to-value for a new AI workflow drops from months to weeks. Governance is built into the platform (audit, evals, access control) instead of bolted on as review meetings.
- **The trap:** The platform team drifts inward, building what's interesting instead of what embedded work reveals is needed. The antidote is the [forward-deployment feedback loop](../forward-deployment/00-overview.md): platform priorities set by what deployments repeatedly hit.
- **Next step:** Leadership starts asking Stage 4 questions: which handoffs, roles, and services should be restructured now that the economics have changed?

### Stage 4: Operating model
**Signature:** Org structure and business model reflect AI-era economics, not pre-AI economics with AI sprinkled on.

- **What it looks like:** Teams sized around AI-augmented throughput. Services offered that were previously uneconomical. Roles redefined around judgment, taste, and accountability rather than production. Continuous re-evaluation as capability improves, because the frontier moves, and a Stage 4 org re-plans against it routinely.
- **The trap:** Believing you've "finished." Model capability doubles on a fast clock; a Stage 4 posture is a *process* of continuous restructuring, not an end state.

## How to use this honestly

1. **Assess per team.** "We're at Stage 3" is usually false globally and true for exactly one team.
2. **Don't skip Stage 2.** Orgs love jumping from Stage 1 to platform-building (Stage 3) because platforms feel strategic. A platform built before workflow wins exist is a solution in search of problems, one of the classic [failure modes](03-failure-modes.md).
3. **Expect stage-appropriate metrics.** Activity metrics are fine at Stage 1 and embarrassing at Stage 3. See [04-measuring-impact.md](04-measuring-impact.md).
4. **The transitions are people problems.** 0 to 1 is a permission problem. 1 to 2 is a skills-and-embedding problem. 2 to 3 is an infrastructure-and-incentives problem. 3 to 4 is an executive-courage problem.
