# Claude Skills Competitive Analysis

This note captures what SkillForge should learn from [`alirezarezvani/claude-skills`](https://github.com/alirezarezvani/claude-skills) without becoming a bloated clone.

## High-Level Takeaway

`claude-skills` wins on breadth. It is positioned as a massive cross-tool library with hundreds of skills, agents, personas, commands, Python tools, references, domain folders, and multi-platform install support.

SkillForge should not try to beat that by adding more skills.

SkillForge should own a different lane:

> SkillForge is the workflow and delivery layer that turns evidence into client-ready work.

## What Claude Skills Does Well

| Strength | Why It Works | SkillForge Move |
|---|---|---|
| Large catalog | The repo feels comprehensive and useful for many domains | Keep a curated catalog, but organize around outcomes instead of volume |
| Multi-tool support | It speaks to Claude Code, Codex, Gemini, Cursor, Windsurf, Aider, OpenCode, and more | Add explicit install docs per supported host when SkillForge matures |
| Domain organization | Engineering, product, marketing, compliance, finance, research, and C-level advisory are easy to scan | Keep packs grouped by use case: repo audit, AI consulting, MVP, business ops, research, video |
| Skills / agents / personas distinction | It explains the difference between how to execute, what to do, and who is thinking | Add a SkillForge equivalent: skills, recipes, packs, briefs, personas later |
| Orchestration examples | Shows how skills/personas can chain across work phases | Make the Forge Loop the central orchestration model |
| Security auditor concept | Makes the library feel safer to install and evaluate | Add a future SkillForge Pack Auditor / Skill Auditor recipe |
| Conversion/install scripts | Reduces manual adoption friction | Add an install doctor and host compatibility checks later |
| Social proof | Stars, contributors, tests, and releases build trust | SkillForge needs demos, sample outputs, and case studies before heavy promotion |

## What SkillForge Should Not Copy

Do not copy the "everything library" strategy.

Large catalogs create discoverability, but they also create problems:

- unclear primary use case,
- skill overlap,
- inconsistent quality,
- hard-to-verify claims,
- maintenance burden,
- README number drift,
- weak product positioning.

SkillForge should avoid becoming a directory of random prompts.

## Positioning Difference

| Dimension | Claude Skills | SkillForge |
|---|---|---|
| Primary strategy | Breadth and catalog size | Workflow clarity and business outcomes |
| Main promise | Hundreds of skills across many tools/domains | Turn signal, evidence, repo context, and client needs into deliverables |
| User mental model | Skill library | Delivery methodology |
| Best buyer/user | Power users looking for many ready-made skills | Consultants, founders, operators, and builders who need repeatable outcomes |
| Differentiator | Volume and platform coverage | Forge Loop, packs, recipes, SignalBrief, FrameBrief, client-ready artifacts |
| Risk | Bloat and inconsistent quality | Too narrow if demos are weak |

## Strategic Lesson

SkillForge should be smaller but sharper.

The winning claim should be:

> We do not have the most skills. We have the clearest path from evidence to shipped work.

## Recommended SkillForge Improvements

### 1. Add a Skills / Recipes / Packs / Briefs explanation

SkillForge should explain its primitives clearly:

| Primitive | Meaning |
|---|---|
| Skill | A focused operating instruction for an agent |
| Recipe | A step-by-step workflow that composes skills into an outcome |
| Pack | A productized bundle for a specific customer/use case |
| Brief | A client-ready research, video, repo, or business artifact |
| Forge Loop | The central methodology: Signal, Scope, Spec, Plan, Build, Prove, Ship |

### 2. Add install clarity later

SkillForge should eventually document support for:

- Claude Code,
- OpenAI Codex,
- Cursor,
- Gemini CLI,
- Windsurf,
- OpenCode,
- manual Markdown use.

Do this only after the repo structure and metadata are stable.

### 3. Add a Pack Auditor

A future SkillForge auditor should verify:

- every pack has a README,
- every recipe has a goal, inputs, workflow, outputs, and quality gate,
- internal links resolve,
- no upstream attribution is missing,
- every claim maps to an artifact or validation step.

### 4. Add sample outputs

The fastest way to build trust is not more skills. It is examples.

Add sample deliverables for:

- repo audit,
- AI automation assessment,
- MVP blueprint,
- SignalBrief-to-proposal,
- video-to-brief,
- business operations roadmap.

## Recommended Commit Path

1. Add `docs/claude-skills-competitive-analysis.md`.
2. Link it from the README competitive analysis section.
3. Add a `docs/primitives.md` page explaining skills, recipes, packs, briefs, and the Forge Loop.
4. Add `scripts/validate-skillforge-content.js` or equivalent later.
5. Add sample outputs before expanding the pack catalog.

## Product Principle

Claude Skills proves there is demand for large skill libraries.

SkillForge should prove there is demand for a disciplined workflow stack that turns research, video, code, and client context into work people can use, sell, test, ship, or hand to a team.
