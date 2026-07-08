# Superpowers Competitive Analysis

This note captures what SkillForge should learn from `obra/superpowers` without becoming a generic clone.

## High-Level Takeaway

Superpowers wins because it is not presented as a prompt pack. It is presented as a complete software development methodology for coding agents.

SkillForge should take the same strategic lesson and apply it to MiamiCreme's lane:

> SkillForge is a business and product delivery methodology for AI operators.

## What Superpowers Does Well

| Strength | Why It Works | SkillForge Move |
|---|---|---|
| Methodology-first positioning | It tells users how the agent behaves, not just what files exist | Lead with the Forge Loop, not only packs |
| Automatic workflow behavior | The agent is expected to check skills before acting | Add `using-skillforge` bootstrap guidance |
| Clear basic workflow | Brainstorm, worktree, plan, execute, test, review, finish | Map to Signal, Scope, Spec, Plan, Build, Prove, Ship |
| Multi-harness support | Claude Code, Codex, Cursor, Copilot, Kimi, OpenCode, Pi, etc. | Keep installation docs explicit per host as SkillForge matures |
| Testing philosophy | TDD, verification, and review are core values | Require proof gates in every SkillForge pack |
| Commercial services path | Enterprise support is visible | Position SkillForge packs as paid consulting/service assets |
| Community and contribution clarity | Contribution boundaries are explicit | Add contribution rules before accepting random skills |

## What SkillForge Should Not Copy

SkillForge should not try to own the exact same message as Superpowers:

> A software development methodology for coding agents.

That lane is already strong and crowded.

SkillForge should own:

> A business, product, research, and delivery methodology for AI operators.

## SkillForge Differentiation

| Dimension | Superpowers | SkillForge |
|---|---|---|
| Primary audience | Coding-agent users and software teams | AI consultants, founders, operators, product builders, dealmakers |
| Primary promise | Better coding-agent discipline | Better research-to-delivery execution |
| Core loop | Brainstorm, plan, subagents, TDD, review | Signal, scope, spec, plan, build, prove, ship |
| Research layer | Not the main product | SignalBrief is first-class |
| Business output | Mostly development-focused | Audits, proposals, discovery notes, MVP plans, SOP maps, implementation branches |
| Commercial angle | Enterprise support and tooling | MiamiCreme service packs and implementation workflows |

## Recommended SkillForge Commit Path

1. Add the Forge Loop as the central methodology.
2. Add a `using-skillforge` bootstrap skill that tells agents when to activate the methodology.
3. Link SignalBrief as the first stage of the loop.
4. Turn the README from a repo overview into a workflow story.
5. Add recipes that convert SignalBrief outputs into proposals and MVP specs.
6. Add validation/eval tasks so packs are testable, not just docs.
7. Add commercial service packaging later.

## Strategic Positioning

### SkillForge

Agent workflow system for building, auditing, consulting, and shipping with discipline.

### SignalBrief

Market intelligence briefs from real public signals.

### MiamiCreme Stack

Research what matters. Forge the plan. Ship the work.

## Product Principle

Every SkillForge feature should answer at least one of these questions:

- Does it help the agent ask better questions?
- Does it turn research into action?
- Does it reduce delivery risk?
- Does it produce a reusable artifact?
- Does it help a consultant, founder, or operator get paid?
- Does it make the final work more verifiable?

If the answer is no, it probably belongs outside SkillForge.
