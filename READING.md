# Reading List

Curated sources behind (and against) the ideas in this repo. Organized by what question you're chasing. Titles and authors are given so items stay findable even as URLs rot; links included only where stable.

## On forward deployment and the FDE model

- **Nabeel Qureshi — "Reflections on Palantir"** (nabeelqu.co). The best insider account of the FDE model in practice: what forward-deployed work actually feels like, why the "it's just consulting" critique misses, and where it doesn't. Start here.
- **Palantir's S-1 filing (2020)** — the primary-source articulation of the FDE/platform split and the strategic bet that bespoke deployment work compounds into product. Read the business-model section skeptically alongside the bear-case commentary it attracted.
- **Forward-Deployed Engineer job postings at frontier AI companies** (Anthropic, OpenAI, and others — see their careers pages). Job descriptions are underrated primary sources: they state, in operational terms, what the role is believed to require right now.

## On why adoption lags capability

- **Paul A. David — "The Dynamo and the Computer: An Historical Perspective on the Modern Productivity Paradox"** (American Economic Review, 1990). The canonical account of why general-purpose technologies transform slowly: the win requires reorganizing the factory, not swapping the engine. The intellectual backbone of this repo's Level 2/Level 3 distinction.
- **Erik Brynjolfsson, Daniel Rock, Chad Syverson — "The Productivity J-Curve"** (NBER). Why measured productivity *dips* during transformative-technology adoption while intangible reorganization investment accumulates — and why patience plus measurement beats either hype or dismissal.
- **Everett Rogers — *Diffusion of Innovations*.** The champions-network playbook is applied Rogers: adoption spreads through trusted local peers, not central announcements.
- **Geoffrey Moore — *Crossing the Chasm*.** Why enthusiast wins don't automatically become mainstream practice; the chasm is the gap between this repo's Stage 2 and Stage 3.

## On AI-and-work evidence

- **Fabrizio Dell'Acqua et al. — "Navigating the Jagged Technological Frontier"** (Harvard Business School working paper, 2023; the BCG consultant study). The essential empirical result: AI dramatically improves performance *inside* its capability frontier and degrades it just outside, and the frontier is jagged and unintuitive. This is why workflow-level discovery and eval sets matter more than org-wide rollouts.
- **Anthropic Economic Index** (anthropic.com/economic-index). Ongoing empirical mapping of what AI is actually used for across occupations — useful for grounding "where's the leverage" conversations in observed usage rather than speculation.
- **METR — "Measuring AI Ability to Complete Long Tasks"** (metr.org, 2025). The task-horizon doubling result; the quantitative case behind this repo's claim that "no" verdicts have a shelf life and eval sets from killed pilots should be re-run on a cadence.
- **MIT (NANDA initiative) — "The GenAI Divide: State of AI in Business"** (2025). The widely cited finding that the overwhelming majority of enterprise GenAI pilots produce no measurable P&L impact — read it as a field survey of the failure modes cataloged in this repo (pilot graveyards, tool-first thinking, missing workflow integration).

## On practice

- **Ethan Mollick — *Co-Intelligence* and the "One Useful Thing" newsletter.** The most consistently practical writing on working with AI's jagged frontier; his "always invite AI to the table" heuristic is Level-1 enablement in four words.
- **Anthropic — "Building Effective Agents"** (anthropic.com engineering blog, 2024). The workflow-vs-agent design vocabulary used implicitly throughout this repo's build phases: start with the simplest composition that works, add autonomy only when the task demands it.

## Reading posture

Two biases to guard against while reading in this space:

1. **Vendor gravity.** Most writing about AI adoption is produced by parties selling AI adoption. Prefer primary sources (S-1s, job postings, measured studies) and insider accounts with skin in the game.
2. **Vintage decay.** Anything empirical about AI capability has a shelf life measured in months. Note the date of every claim; treat pre-2024 "AI can't X" claims as historical documents. The organizational findings (David, Rogers, Moore) age far better than the capability findings.

*Suggest additions via PR — see [CONTRIBUTING.md](CONTRIBUTING.md). The bar: would a practitioner running a real engagement act differently for having read it?*
