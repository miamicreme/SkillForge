# using-skillforge

Use this skill whenever the user asks an agent to build, fix, audit, plan, research, consult, propose, launch, or ship work that should become a reusable artifact.

## Purpose

This is the SkillForge bootstrap. It tells the agent to use the Forge Loop before jumping into output.

## Activation

Before starting meaningful work, check whether the task fits one of these categories:

- repo audit or code improvement,
- product/MVP planning,
- AI consulting or automation discovery,
- business operations assessment,
- market research or SignalBrief conversion,
- proposal, outreach, or client-ready deliverable,
- implementation plan, branch plan, or quality gate.

If yes, apply the Forge Loop.

## The Forge Loop

1. **Signal** — gather or summarize evidence.
2. **Scope** — clarify the real objective and constraints.
3. **Spec** — define what should exist when done.
4. **Plan** — break the work into small verifiable steps.
5. **Build** — execute one useful slice at a time.
6. **Prove** — verify with tests, checks, citations, or review.
7. **Ship** — summarize what changed, what is ready, and what remains.

## Operating Rules

- Do not skip evidence when a decision depends on current market, customer, repo, or business context.
- Do not jump from vague request to code or final deliverable.
- Do not claim completion without proof.
- Do not hide assumptions.
- Prefer reusable artifacts over one-off chat.
- Keep tasks small enough to verify.
- When research is needed, use SignalBrief-style framing: what people are saying, doing, buying, building, betting on, or complaining about.

## Output Expectations

A SkillForge response should usually include:

- the stage of the Forge Loop being applied,
- the artifact produced,
- evidence or assumptions used,
- verification or quality gate,
- next recommended action.

## Related Docs

- `docs/forge-loop.md`
- `docs/superpowers-competitive-analysis.md`
- `packs/signalbrief-research/README.md`
- `recipes/signalbrief-to-proposal.md`
- `recipes/signalbrief-to-mvp.md`
