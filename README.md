# SkillForge

**Reusable AI workflows, skills, playbooks, and quality gates for disciplined AI agents.**

SkillForge is MiamiCreme’s agent operating system for turning AI from a loose chat assistant into a repeatable delivery machine. It combines engineering skills, workflow recipes, reusable playbooks, productized service packs, and verification gates so agents can clarify requirements, plan work, build in slices, test behavior, review quality, and ship safely.

SkillForge is built on the excellent [`addyosmani/agent-skills`](https://github.com/addyosmani/agent-skills) foundation and extends it with MiamiCreme-specific workflow packs for repo audits, AI consulting, MVP building, business operations, SignalBrief-powered research, and FrameBrief-powered video intelligence.

---

## MiamiCreme AI Workflow Stack

SkillForge is the playbook and quality layer. SignalBrief is the market-signal layer. FrameBrief is the video-evidence layer. Together they create a practical operating system for AI-assisted consulting, product building, and client delivery.

| Product | Role | Primary Output |
|---|---|---|
| [`SkillForge`](https://github.com/miamicreme/SkillForge) | Agent workflow system | Specs, plans, implementation tasks, QA gates, audits, proposals |
| [`SignalBrief`](https://github.com/miamicreme/signalbrief) | Social and market intelligence layer | Company, founder, competitor, buyer-pain, deal, and trend briefs |
| [`FrameBrief`](https://github.com/miamicreme/FrameBrief) | Video intelligence layer | Creative teardowns, demo briefs, bug repro briefs, launch notes, walkthrough briefs |

The intended workflow is:

1. **SignalBrief finds the conversation** — what people are saying, sharing, building, betting on, and complaining about.
2. **FrameBrief watches the evidence** — what is visible and spoken inside videos, demos, walkthroughs, ads, and screen recordings.
3. **SkillForge turns that intelligence into action** — specs, plans, branches, implementation prompts, outreach, proposals, and delivery gates.

---

## The Forge Loop

The Forge Loop is SkillForge’s core methodology:

> Research what matters. Forge the plan. Ship the work.

| Stage | Purpose | Artifact |
|---|---|---|
| Signal | Gather outside evidence and context | SignalBrief, FrameBrief, or research notes |
| Scope | Clarify the real objective and constraints | Problem statement and acceptance criteria |
| Spec | Define what should exist when done | Spec, brief, or requirements doc |
| Plan | Break the work into small verified slices | Task plan, branch plan, or recipe |
| Build | Execute one useful slice at a time | Implementation or deliverable |
| Prove | Verify before claiming completion | Tests, checks, citations, timestamps, or review notes |
| Ship | Deliver with risks and next steps visible | PR, summary, proposal, report, or handoff |

See [`docs/forge-loop.md`](docs/forge-loop.md) for the full methodology and [`skills/using-skillforge/SKILL.md`](skills/using-skillforge/SKILL.md) for the bootstrap behavior agents should follow.

---

## What SkillForge Adds

The upstream skill foundation already covers the engineering lifecycle: define, plan, build, verify, review, and ship. SkillForge keeps that discipline and adds a product layer around it.

| Layer | Purpose |
|---|---|
| `skills/` | Core agent skills and SkillForge bootstrap workflows |
| `recipes/` | End-to-end workflows that combine multiple skills into repeatable outcomes |
| `packs/` | Productized bundles for specific use cases, audiences, and paid services |
| `references/` | Checklists and supporting quality bars used by skills and recipes |
| `docs/` | Attribution, roadmap, comparison notes, brand positioning, and SkillForge-specific guidance |

---

## SkillForge Packs

| Pack | What it does | Best customer |
|---|---|---|
| [Repo Audit Pack](packs/repo-audit/README.md) | Rates a repository, finds risks, and creates a branch-by-branch improvement plan | Founders, developers, agencies, AI app builders |
| [AI Consultant Pack](packs/ai-consultant/README.md) | Guides discovery, assessment, scope control, proposals, and follow-up | AI consultants and automation agencies |
| [MVP Builder Pack](packs/mvp-builder/README.md) | Turns a product idea into a spec, plan, build slices, tests, and launch checklist | Founders and product builders |
| [Business Ops Pack](packs/business-ops/README.md) | Maps internal workflows, SOPs, reports, automations, and AI assistant opportunities | Small businesses and operations teams |
| [SignalBrief Research Pack](packs/signalbrief-research/README.md) | Converts market/social intelligence into briefs, discovery notes, opportunity maps, and outreach angles | Consultants, founders, sales teams, recruiters, dealmakers |

---

## Workflow Recipes

Recipes are higher-level playbooks that combine skills into a complete operating pattern.

| Recipe | Use when |
|---|---|
| [Repo Audit](recipes/repo-audit.md) | You need to evaluate a repository and produce a production-readiness plan |
| [Client Discovery](recipes/client-discovery.md) | You need to run an AI consulting or automation discovery process |
| [MVP Builder](recipes/mvp-builder.md) | You need to turn an idea into a buildable MVP plan |
| [Business Ops](recipes/business-ops.md) | You need to assess a company’s workflows and automation opportunities |
| [SignalBrief to Proposal](recipes/signalbrief-to-proposal.md) | You need to turn market intelligence into a client-ready proposal or pitch |
| [SignalBrief to MVP](recipes/signalbrief-to-mvp.md) | You need to turn user pain and competitor research into a buildable product spec |
| [Video to Brief](recipes/video-to-brief.md) | You need to turn video evidence into a timestamped brief, bug report, teardown, or walkthrough note |

---

## Quick Start

Install the full SkillForge skill foundation with the open skills CLI:

```bash
npx skills add miamicreme/SkillForge
npx skills add miamicreme/SkillForge --list
```

Install individual skills:

```bash
npx skills add miamicreme/SkillForge --skill using-skillforge
npx skills add miamicreme/SkillForge --skill code-review-and-quality
npx skills add miamicreme/SkillForge --skill test-driven-development
npx skills add miamicreme/SkillForge --skill planning-and-task-breakdown
```

Use the repo directly during development:

```bash
git clone https://github.com/miamicreme/SkillForge.git
cd SkillForge
```

---

## Core Commands

The inherited command layer maps to the development lifecycle.

| What you're doing | Command | Principle |
|---|---|---|
| Define what to build | `/spec` | Spec before code |
| Plan how to build it | `/plan` | Small, atomic tasks |
| Build incrementally | `/build` | One slice at a time |
| Prove it works | `/test` | Tests are proof |
| Review before merge | `/review` | Improve code health |
| Audit web performance | `/webperf` | Measure before optimizing |
| Simplify the code | `/code-simplify` | Clarity over cleverness |
| Ship to production | `/ship` | Safer launches through gates |

SignalBrief currently keeps its inherited `/last30days` command while the branded `/signalbrief` command is planned. FrameBrief currently keeps its inherited `/watch` command while the branded `/framebrief` command is planned.

---

## Positioning

SkillForge is not just a prompt pack. It is a workflow system for making agents behave like disciplined operators.

SignalBrief is not just a search tool. It is a market-intelligence layer for grounding decisions in real public signals.

FrameBrief is not just a video summarizer. It is a video-intelligence layer for grounding decisions in what was actually seen and heard.

Together, the MiamiCreme AI workflow stack should help agents:

- find what matters before building or pitching,
- watch the evidence before summarizing or deciding,
- ask better discovery questions,
- break work into small verifiable tasks,
- avoid skipping tests and quality gates,
- surface risk instead of hiding it,
- produce reusable plans, docs, implementation prompts, and briefs,
- support productized services like audits, client discovery, MVP buildouts, video teardowns, and market-intelligence reports.

---

## Development Roadmap

See [docs/roadmap.md](docs/roadmap.md).

Near-term priorities:

1. Finish SkillForge branding and attribution.
2. Make the Forge Loop the mandatory workflow pattern.
3. Align SignalBrief as the research/briefing layer in the MiamiCreme workflow stack.
4. Align FrameBrief as the video-evidence layer in the MiamiCreme workflow stack.
5. Add install and reference verification.
6. Expand the starter packs.
7. Add recipe validation.
8. Create demo audits, sample briefs, and sample outputs.
9. Package paid/professional workflow templates later.

---

## Competitive Analysis

See [`docs/superpowers-competitive-analysis.md`](docs/superpowers-competitive-analysis.md) for the Superpowers benchmark and SkillForge differentiation strategy.

See [`docs/claude-video-companion-analysis.md`](docs/claude-video-companion-analysis.md) for the FrameBrief / Claude Video companion strategy.

---

## Attribution

SkillForge is based on [`addyosmani/agent-skills`](https://github.com/addyosmani/agent-skills), used under the MIT License. See [docs/attribution.md](docs/attribution.md) for details.

The original project provides the core engineering skill foundation. SkillForge adds workflow recipes, productized packs, and business-oriented agent operating patterns.

SignalBrief is based on [`mvanhorn/last30days-skill`](https://github.com/mvanhorn/last30days-skill), used under the MIT License, and is maintained separately in [`miamicreme/signalbrief`](https://github.com/miamicreme/signalbrief).

FrameBrief is based on [`bradautomates/claude-video`](https://github.com/bradautomates/claude-video), used under the MIT License, and is maintained separately in [`miamicreme/FrameBrief`](https://github.com/miamicreme/FrameBrief).

---

## License

MIT. See [`LICENSE`](LICENSE).
