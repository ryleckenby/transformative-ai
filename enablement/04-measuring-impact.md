# Measuring Impact

Measurement is where enablement programs are won or lost, because what you measure determines what the program optimizes for. Measure activity and you'll get activity. This doc lays out a metric hierarchy, how to attribute honestly, and the traps.

## The metric hierarchy

Think of metrics in four tiers. Each tier is more meaningful and harder to measure than the one below it. A healthy program reports mostly on tiers 2 and 3 and uses tier 1 only for early-stage plumbing checks.

### Tier 0: Provisioning (necessary, meaningless)
Seats, access grants, policy sign-offs. Only interesting when they're broken.

### Tier 1: Activity
Weekly/daily active users, queries per user, feature usage, retention of usage over time.

- **What it's good for:** detecting Stage 0 to 1 problems (nobody's using it means an access, permission, or fear issue), and *retention* is a weak proxy for value (people abandon tools that don't help).
- **What it can't tell you:** whether any work is better. High activity is compatible with pure novelty use.

### Tier 2: Workflow outcomes
Per redesigned workflow, before/after on:

- **Cycle time**: request-to-done for one unit of work
- **Throughput**: units per person-week
- **Quality**: error/rework/escalation rate, first-pass acceptance rate
- **Coverage**: work that now gets done that previously didn't (the invisible backlog: tests never written, follow-ups never sent, analyses never run)
- **Human experience**: satisfaction of the people in the workflow; watch for "AI does the fun part, I do the residue" resentment

This is the tier that matters most. It requires a *baseline captured before the change*, the single most commonly skipped step in the field. No baseline, no claim.

### Tier 3: Business outcomes
Unit cost, revenue per employee, customer NPS/resolution time, time-to-market. Moves slowly, is confounded by everything, and is what executives actually care about. The honest posture: tier 3 claims are built by *aggregating audited tier 2 wins*, not by regression against the stock price.

## Attribution without self-deception

- **Baseline first.** Capture 2 to 4 weeks of the old workflow's numbers before touching it. Retrospective baselines are fiction.
- **Compare like with like.** Pilot volunteers are enthusiasts working on favorable cases. Report pilot numbers as pilot numbers; re-measure after full-team rollout.
- **Count the total cost.** Include the enablement engineer's time, the champion's time, tooling, and review overhead, not just license cost.
- **Watch for displaced work.** If cycle time fell because verification got skipped, quality metrics will pay the bill later. Always pair a speed metric with a quality metric; never report one without the other.
- **Self-report with care.** "Hours saved" surveys overestimate reliably (people report best-case, and saved time is partly reabsorbed). Use them as directional color, never as the headline number.

## An honest scorecard shape

For each workflow win, one page (template: [pilot scorecard](../playbooks/pilot-scorecard.md)):

```
Workflow:            Support ticket triage, Team X (14 people)
Baseline (4 wks):    median 3.1h to first response; 22% misroutes
After (4 wks, full team): median 24m; 9% misroutes
Quality gate:        human approves every routing; spot-audit weekly
Costs:               0.4 FTE enablement x 6 wks; $Y/mo inference
Owner:               [named person on the team, not on the enablement team]
Verdict:             Hardened, old path retired [date]
```

A program that produces a stack of these is unkillable at budget time. A program that produces dashboards of tier 1 metrics is one reorg away from deletion.

## Program-level metrics

Beyond individual workflows, track the *enablement engine* itself:

- **Time-to-value per engagement**: should fall as the platform matures (Stage 3 signature)
- **Pattern reuse rate**: how often a new deployment starts from an extracted pattern vs. from scratch
- **Kill rate and kill honesty**: a program with zero kills is either not trying hard things or not reporting honestly; a healthy portfolio kills a third of its pilots cleanly
- **Champion pipeline**: new champions per quarter, and champion retention (see [failure mode #6](03-failure-modes.md))
- **Re-evaluation cadence**: how stale are your "AI can't do this" conclusions? (see [failure mode #9](03-failure-modes.md))
