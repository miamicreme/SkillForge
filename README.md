# SkillForge

**Reusable AI workflows, skills, playbooks, and quality gates for disciplined AI agents.**

SkillForge helps AI agents work with structure instead of chaos. It combines engineering skills, workflow recipes, reusable playbooks, and verification gates so agents can clarify requirements, plan work, build in slices, test behavior, review quality, and ship safely.

SkillForge is built on the excellent [`addyosmani/agent-skills`](https://github.com/addyosmani/agent-skills) foundation and extends it with productized workflow packs for repo audits, AI consulting, MVP building, and business operations.

---

## What SkillForge Adds

The upstream skill foundation already covers the engineering lifecycle: define, plan, build, verify, review, and ship. SkillForge keeps that discipline and adds a product layer around it.

| Layer | Purpose |
|---|---|
| `skills/` | Core agent skills and engineering workflows inherited from the upstream foundation |
| `recipes/` | End-to-end workflows that combine multiple skills into repeatable outcomes |
| `packs/` | Productized bundles for specific use cases, audiences, and paid services |
| `references/` | Checklists and supporting quality bars used by skills and recipes |
| `docs/` | Attribution, roadmap, comparison notes, and SkillForge-specific guidance |

---

## First Four SkillForge Packs

| Pack | What it does | Best customer |
|---|---|---|
| [Repo Audit Pack](packs/repo-audit/README.md) | Rates a repository, finds risks, and creates a branch-by-branch improvement plan | Founders, developers, agencies, AI app builders |
| [AI Consultant Pack](packs/ai-consultant/README.md) | Guides discovery, assessment, scope control, proposals, and follow-up | AI consultants and automation agencies |
| [MVP Builder Pack](packs/mvp-builder/README.md) | Turns a product idea into a spec, plan, build slices, tests, and launch checklist | Founders and product builders |
| [Business Ops Pack](packs/business-ops/README.md) | Maps internal workflows, SOPs, reports, automations, and AI assistant opportunities | Small businesses and operations teams |

---

## Workflow Recipes

Recipes are higher-level playbooks that combine skills into a complete operating pattern.

| Recipe | Use when |
|---|---|
| [Repo Audit](recipes/repo-audit.md) | You need to evaluate a repository and produce a production-readiness plan |
| [Client Discovery](recipes/client-discovery.md) | You need to run an AI consulting or automation discovery process |
| [MVP Builder](recipes/mvp-builder.md) | You need to turn an idea into a buildable MVP plan |
| [Business Ops](recipes/business-ops.md) | You need to assess a company's workflows and automation opportunities |

---

## Quick Start

Install the full SkillForge skill foundation with the open skills CLI:

```bash
npx skills add miamicreme/SkillForge
npx skills add miamicreme/SkillForge --list
```

Install individual skills:

```bash
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

---

## SkillForge Positioning

SkillForge is not just a prompt pack. It is a workflow system for making agents behave like disciplined operators.

The goal is to make AI agents:

- ask better questions before building,
- break work into small verifiable tasks,
- avoid skipping tests and quality gates,
- surface risk instead of hiding it,
- produce reusable plans, docs, and implementation prompts,
- support productized services like audits, client discovery, and MVP buildouts.

---

## Development Roadmap

See [docs/roadmap.md](docs/roadmap.md).

Near-term priorities:

1. Finish SkillForge branding and attribution.
2. Add install and reference verification.
3. Expand the four starter packs.
4. Add recipe validation.
5. Create demo audits and sample outputs.
6. Package paid/professional workflow templates later.

---

## Attribution

SkillForge is based on [`addyosmani/agent-skills`](https://github.com/addyosmani/agent-skills), used under the MIT License. See [docs/attribution.md](docs/attribution.md) for details.

The original project provides the core engineering skill foundation. SkillForge adds workflow recipes, productized packs, and business-oriented agent operating patterns.

---

## License

MIT. See [`LICENSE`](LICENSE).
