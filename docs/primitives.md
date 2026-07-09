# SkillForge Primitives

SkillForge should use a small set of clear primitives. These primitives keep the system understandable, modular, and reusable in EmpireOS later.

## Primitive Map

| Primitive | Meaning | Example |
|---|---|---|
| Skill | A focused operating instruction for an agent | `using-skillforge` |
| Recipe | A repeatable workflow that turns inputs into an output | `repo-audit.md` |
| Pack | A productized bundle for a specific customer or use case | `packs/repo-audit/` |
| Artifact | A reusable output produced by a recipe, pack, or adapter | repo audit, proposal, MVP plan |
| Evidence | Facts, sources, assumptions, timestamps, and confidence notes | URL, repo finding, transcript, frame |
| Quality Gate | A pass/warn/fail check before claiming completion | launch gate, audit gate, proposal gate |
| Adapter | A boundary layer that converts one module output into another module input | SignalBrief to SkillForge, SkillForge to EmpireOS |
| Renderer | A presentation layer that turns artifact data into Markdown, HTML, proposal, report, or task list | brief renderer, proposal renderer |
| Contract | A stable schema for exchanging data between modules | `artifact.schema.json` |

## Skill

A skill tells an agent how to behave in a focused situation.

Good skills are:

- narrow,
- actionable,
- triggerable,
- verifiable,
- written so the agent can follow them without guessing.

A skill should not become a full business plan or large application spec.

## Recipe

A recipe combines skills and steps into a complete workflow.

A recipe should include:

- goal,
- inputs,
- workflow steps,
- recommended skills,
- output format,
- quality gate.

Example: `recipes/repo-audit.md` turns a repository into a score, risk matrix, and branch plan.

## Pack

A pack is a productized bundle for a specific customer and use case.

A pack should include:

- target customer,
- promise,
- deliverables,
- suggested offer,
- related recipes,
- quality gates,
- sample output later.

Example: `packs/ai-consultant/` turns discovery into scope, proposal, and roadmap.

## Artifact

An artifact is the thing SkillForge produces that can be reused, sold, shipped, tested, handed off, or consumed by EmpireOS.

Examples:

- repo audit,
- signal brief,
- frame brief,
- proposal,
- MVP plan,
- business operations assessment,
- deal brief,
- branch plan,
- implementation handoff.

Artifacts should follow the shared artifact contract where possible.

## Evidence

Evidence is what prevents SkillForge from becoming vague advice.

Evidence can come from:

- a repository,
- a URL,
- a file,
- a transcript,
- a video frame,
- a user statement,
- a test result,
- an explicit assumption.

Every serious artifact should separate facts from assumptions.

## Quality Gate

A quality gate says whether the output is ready.

Use:

- `pass` when the artifact is ready to use,
- `warn` when usable but incomplete or assumption-heavy,
- `fail` when the output should not be trusted yet.

## Adapter

Adapters keep products separate.

Examples:

- SignalBrief Adapter converts market research into a SkillForge artifact.
- FrameBrief Adapter converts video evidence into a SkillForge artifact.
- EmpireOS Adapter converts a SkillForge artifact into a mission, priority, or next action.

Adapters should not mix private product logic into public modules.

## Renderer

Renderers convert structured artifacts into human-facing outputs.

Possible render targets:

- Markdown,
- HTML,
- client proposal,
- repo audit report,
- EmpireOS mission card,
- DealFlow summary,
- task list,
- branch plan.

## Contract

Contracts define the stable exchange shape between modules.

A contract should be versioned, documented, and validated before multiple products depend on it.

## Best-Practice Rule

Do not add a new primitive unless the existing primitives cannot represent the work.

SkillForge should be simple enough to explain in one sentence:

> Skills teach behavior, recipes run workflows, packs sell outcomes, artifacts carry evidence, adapters connect modules, and quality gates prove readiness.
