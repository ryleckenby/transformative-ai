# Pilot Scorecard (Template)

The one-page record of a workflow pilot's result. Written at the verdict meeting, kept forever. A stack of these is an enablement program's real balance sheet — including the kills. Everything in `[brackets]` gets filled in.

---

## Workflow: [name, team, team size]

**Pilot window:** [dates] · **Verdict:** ✅ Hardened / ❌ Killed / ⏸ Extended to [date] (extend once, max)
**Charter:** [link] · **Owner going forward:** [name — must be on the host team]

### Results vs. baseline

| Metric | Baseline ([dates], [n] units) | Pilot ([dates], [n] units) | Δ |
|---|---|---|---|
| [primary — e.g., median cycle time] | [3.1 h] | [24 min] | [−87%] |
| [paired quality — e.g., error/rework rate] | [22%] | [9%] | [−13 pts] |
| [coverage — work now done that wasn't] | [—] | [value] | |
| [human experience — pilot-group pulse] | [x/5] | [y/5] | |

**Caveats (mandatory, minimum one):** [pilot group was volunteers / case mix skewed easy / n is small / measurement instrument changed — whatever is true. A scorecard with no caveats is advertising.]

### Costs, all-in

| Item | Amount |
|---|---|
| FDE/enablement time | [0.4 FTE × 6 wks] |
| Champion + team time | [hrs] |
| Inference/tooling | [$ /mo run-rate] |
| Platform work drawn on | [what was reused — note it; reuse is a program metric] |

### The design that shipped

[3–5 lines: the workflow shape (e.g., classify → enrich → draft → human gate), where the human verification sits, what autonomy level, where it lives in their tools. Enough that another team could recognize whether the pattern fits them.]

### Eval & quality gate going forward

- Eval set: [n golden cases, where it lives] · Re-run cadence: [when / on model updates]
- Production quality monitor: [metric, alert threshold, who's paged]
- Autonomy review: [conditions under which the human gate loosens or tightens]

### If killed: why, exactly

[Capability gap / data access / verification too expensive / trust / economics — be specific. Then:]
- Eval set preserved at: [location]
- Re-test trigger: [next major model release / date / capability milestone]
- What would have to be true for this to work: [1–2 lines]

### Pattern extraction (the dividend)

- Reusable pattern: [name + 1 line, or "none — genuinely bespoke because X"]
- Hand-rolled pieces → platform backlog: [list, linked to backlog items]
- Next teams this pattern likely fits: [names]

### Retirement of the old path

Old path retired on: [date] / Not yet, because: [reason + date]. *(Dual paths decay into the old one. This line item exists because everyone skips it.)*
