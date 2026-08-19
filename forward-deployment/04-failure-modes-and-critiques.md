# Failure Modes and the Honest Case Against

Forward deployment has a distinguished record and a well-documented shadow. This doc takes the critiques seriously — a knowledge base that only sells the pattern isn't one.

## The structural critiques

### 1. "It's just consulting with better branding"

**The critique:** Bespoke work per customer, senior humans on planes, revenue that scales with headcount — that's a services firm, whatever the pitch deck says. Public-market skeptics leveled exactly this at Palantir for years.

**When it's true:** When the feedback loop is dead — engagements don't generalize into product, per-customer custom surface area grows, and engagement N costs the same as engagement 1.

**The test:** Plot custom-code-per-deployment and time-to-value over successive engagements. Falling → platform company with an embedded motion. Flat or rising → consultancy. There is no third reading, and the honest answer changes what you should do next (a deliberate consultancy is a fine thing to be — an accidental one is not).

### 2. Human duct tape over product gaps

**The critique:** FDEs make weak products look strong. Because a skilled human quietly bridges every gap, the product never receives the pressure that would force it to improve — and the company's unit economics quietly depend on heroics forever.

**When it's true:** When FDE effort isn't measured or fed back. The gap the FDE bridges is invisible to product leadership precisely because it's being bridged so competently.

**Counter-move:** Make the duct tape visible: field reports itemize every manual bridge, the graduation ledger tracks whether they're being absorbed into product, and product roadmaps are reviewed against deployment evidence. FDE pain is the product backlog, or the model is failing.

### 3. Doesn't scale / hides the real margin

**The critique:** You cannot hire ten thousand excellent FDEs; the model caps growth at the rate you can grow rare hybrid humans, and it flatters gross margins by booking services-ish work as product.

**When it's true:** Always, partially — the constraint is real. The strategic response is that the model is *designed to shrink its own necessity per deployment*: each generalization moves work from humans to product. AI tooling accelerates this sharply (an FDE with agentic tools does the work of several), and self-serve maturity should absorb the simpler deployments over time, reserving FDEs for the frontier. If FDE-hours-per-dollar-of-value isn't falling year over year, the critique is winning.

### 4. Two-tier engineering culture

**The critique:** Platform engineers come to see FDEs as cowboys shipping unmaintainable hacks; FDEs see platform as slow and detached from reality. Status accrues to one side (varies by company which), and the other side's talent leaks out.

**Counter-move:** Rotations in both directions, deployment evidence as the shared currency of roadmap decisions, promotion criteria that explicitly value both kinds of excellence, and shared wins (the connector that graduated is celebrated as *both* teams' shipping).

## The engagement-level failure modes

(These complement the [lifecycle anti-patterns](02-engagement-lifecycle.md); those are tactical, these are systemic.)

### 5. The permanent embed
The FDE becomes de facto staff at one customer — indispensable, beloved, and no longer forward-deployed in any meaningful sense. Learning stops flowing; one account consumes a rare human. **Fix:** charters with end states, tenure caps per engagement, and managers who treat "they can't function without our FDE" as a red flag, not a retention win.

### 6. Going native
Softer than #5: the FDE starts optimizing purely for the host's happiness — accepting scope that teaches the platform nothing, avoiding hard conversations about what the customer should change. Embedded empathy is the job; embedded capture is the failure. **Fix:** field-report cadence, FDE peer review across engagements, rotation.

### 7. The demo-industrial complex
Engagements repeatedly scoped around executive demos rather than daily users — impressive quarterly reviews, no operational adoption. Common when the sponsor is senior and the problem owner is absent. **Fix:** qualification requires a named daily-user problem owner; "who uses this every day, and did we baseline their workflow?" is the standing question.

### 8. Trust debt with the hosts' workforce
The embedded team is read as "the people automating us," and the workflow's actual experts quietly withhold the tribal knowledge that discovery depends on. The engagement then automates the *documented* workflow, which is not the *real* workflow, and fails in production. **Fix:** the FDE's explicit stance is augmenting the experts' judgment and shedding their drudgery — communicated by the sponsor, demonstrated in what gets built first (kill the hated task, not the valued one), and reflected in whose name is on the win.

## When not to use the model at all

- **Uniform, self-serve-able workflows** — build product; embedding humans adds cost without insight.
- **No platform to feed** — you're choosing consulting; fine, but price and staff it as consulting.
- **Engagements too small to carry a human** — the motion's floor cost is real; below it, use champions + patterns + office hours (the lightweight end of [enablement](../enablement/02-adoption-playbook.md)) instead.
- **As a substitute for fixing a broken product** — see #2; duct tape is a bridge, not a business model.

## The steelman, restated

Every critique above is a corruption of the same loop, and the model's defense is the same loop working: **embed → learn → generalize → shrink the bespoke**. Forward deployment is not "services vs. product" — it's a mechanism for *converting* services-shaped learning into product-shaped leverage, in domains where the learning is only available on the ground. Run with the loop intact, it's the fastest known way to deploy general capability into specific reality. Run without it, it's an expensive way to postpone finding that out.
