# SkillForge

**Kohron Burton's AI Engineering Operating System**

SkillForge is a production-focused collection of AI coding workflows, specialist agents, quality gates, and domain-specific delivery skills. It helps coding agents move from idea to verified production software without skipping requirements, tests, security, observability, or launch readiness.

```text
DEFINE → PLAN → BUILD → VERIFY → REVIEW → SHIP
```

## Why SkillForge

AI coding agents often optimize for speed and completion instead of evidence. SkillForge enforces a stronger standard:

- assumptions are surfaced before implementation;
- non-trivial work starts with a written specification;
- changes are delivered in small, verifiable slices;
- tests and runtime evidence are required;
- security, performance, and observability are reviewed before launch;
- work is not considered complete until the definition of done is satisfied.

## Core Commands

| Goal | Command |
|---|---|
| Define the product or feature | `/spec` |
| Break work into atomic tasks | `/plan` |
| Build incrementally | `/build` |
| Prove behavior | `/test` |
| Review code health | `/review` |
| Audit web performance | `/webperf` |
| Simplify implementation | `/code-simplify` |
| Ship safely | `/ship` |

## SkillForge Extensions

SkillForge adds domain-focused workflows on top of the core engineering pack:

- [`production-readiness-audit`](skills/production-readiness-audit/SKILL.md) — determine whether a repository truly runs and is safe to ship;
- [`make-it-run`](skills/make-it-run/SKILL.md) — reproduce failures, repair setup, and produce verified launch instructions;
- [`repo-productization`](skills/repo-productization/SKILL.md) — turn a technical repository into a credible portfolio or commercial product.

## Install

Install the complete pack with the Skills CLI:

```bash
npx skills add miamicreme/SkillForge
```

List available skills:

```bash
npx skills add miamicreme/SkillForge --list
```

Install one skill:

```bash
npx skills add miamicreme/SkillForge --skill production-readiness-audit
```

The skills are plain Markdown and can also be used with Claude Code, Cursor, Codex, Copilot, Gemini CLI, Windsurf, OpenCode, and other agents that support instruction files or system prompts.

## Operating Standard

Every non-trivial change should produce evidence for:

1. requirements and acceptance criteria;
2. implementation scope;
3. automated checks;
4. runtime verification;
5. security and dependency review;
6. documentation and rollback guidance.

A response such as “it should work” is not completion evidence.

## Project Structure

```text
SkillForge/
├── skills/                 # Core and SkillForge-specific workflows
├── agents/                 # Specialist reviewer personas
├── references/             # Reusable engineering checklists
├── commands/               # Agent command entry points
├── .claude/commands/       # Claude Code commands
├── .gemini/commands/       # Gemini CLI commands
├── docs/                   # Setup and operating documentation
├── ATTRIBUTION.md          # Upstream provenance and modification notice
├── plugin.json             # SkillForge package metadata
└── LICENSE                 # MIT license
```

## Intended Uses

SkillForge is designed for:

- production repository audits;
- MVP and SaaS delivery;
- API, frontend, and distributed-system implementation;
- client discovery and technical delivery;
- portfolio project hardening;
- repeatable AI-assisted software engineering.

## Attribution

SkillForge is based on and extends Addy Osmani's open-source `agent-skills` project. The upstream material remains available under the MIT License. See [ATTRIBUTION.md](ATTRIBUTION.md) and [LICENSE](LICENSE) for details.

## License

MIT. You may use, modify, distribute, sublicense, and sell copies subject to the license terms and preservation of required copyright notices.
