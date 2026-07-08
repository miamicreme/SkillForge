---
name: using-skillforge
description: Applies the SkillForge Forge Loop before meaningful agent work. Use when the user asks an agent to build, fix, audit, plan, research, consult, propose, launch, or ship work that should become a reusable artifact.
---

# using-skillforge

Use this skill whenever the user asks an agent to build, fix, audit, plan, research, consult, propose, launch, or ship work that should become a reusable artifact.

## Overview

This is the SkillForge bootstrap. It tells the agent to use the Forge Loop before jumping into output.

## When to Use

Use this skill before starting meaningful work that fits one of these categories:

- repo audit or code improvement,
- product/MVP planning,
- AI consulting or automation discovery,
- business operations assessment,
- market research or SignalBrief conversion,
- video evidence or FrameBrief conversion,
- proposal, outreach, or client-ready deliverable,
- implementation plan, branch plan, or quality gate.

## The Forge Loop

1. **Signal** — gather or summarize evidence.
2. **Scope** — clarify the real objective and constraints.
3. **Spec** — define what should exist when done.
4. **Plan** — break the work into small verifiable steps.
5. **Build** — execute one useful slice at a time.
6. **Prove** — verify with tests, checks, citations, timestamps, or review.
7. **Ship** — summarize what changed, what is ready, and what remains.

## Operating Rules

- Do not skip evidence when a decision depends on current market, customer, repo, video, or business context.
- Do not jump from vague request to code or final deliverable.
- Do not claim completion without proof.
- Do not hide assumptions.
- Prefer reusable artifacts over one-off chat.
- Keep tasks small enough to verify.
- When research is needed, use SignalBrief-style framing: what people are saying, doing, buying, building, betting on, or complaining about.
- When video evidence is needed, use FrameBrief-style framing: what was seen, heard, timestamped, or visually proven.

## Output Expectations

A SkillForge response should usually include:

- the stage of the Forge Loop being applied,
- the artifact produced,
- evidence or assumptions used,
- verification or quality gate,
- next recommended action.

## Common Rationalizations

| Rationalization | Response |
|---|---|
| "The user wants speed, so skip scope." | Fast work still needs a clear target. Scope first, then move fast. |
| "This is just a quick answer." | If the output will be reused, sold, shipped, or handed to a client, apply the loop. |
| "I can fill in the gaps." | Assumptions must be visible. Do not quietly invent missing facts. |

## Red Flags

- The output has no evidence, assumption list, or quality gate.
- The task jumps from idea directly to implementation.
- The response produces advice but no reusable artifact.
- The agent claims something is done without showing proof.

## Verification

Before finishing, confirm that the response has:

- a clear artifact,
- a stated scope,
- evidence or assumptions,
- a plan or deliverable structure,
- a proof/quality gate,
- a next action.

## Related Docs

- `docs/forge-loop.md`
- `docs/superpowers-competitive-analysis.md`
- `packs/signalbrief-research/README.md`
- `recipes/signalbrief-to-proposal.md`
- `recipes/signalbrief-to-mvp.md`
- `recipes/video-to-brief.md`
