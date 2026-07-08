# The Forge Loop

The Forge Loop is SkillForge's core operating methodology. It turns loose AI work into a disciplined delivery cycle.

> Research what matters. Forge the plan. Ship the work.

## Why It Exists

Most agent workflows fail because they jump from a vague request straight into output. The Forge Loop forces the agent to slow down, ground the work, define success, plan in slices, verify results, and produce reusable artifacts.

SkillForge should treat this as a mandatory workflow pattern, not a suggestion.

## The Loop

| Stage | Question | Primary Artifact | Gate |
|---|---|---|---|
| 1. Signal | What is true outside the building? | SignalBrief or research notes | Evidence is cited or clearly marked as assumption |
| 2. Scope | What are we actually trying to accomplish? | Problem statement and acceptance criteria | User-visible scope is clear |
| 3. Spec | What should exist when this is done? | Spec or brief | Requirements are testable |
| 4. Plan | How will we do it safely? | Branch-by-branch or task-by-task plan | Tasks are small and verifiable |
| 5. Build | What is the next smallest useful slice? | Implementation change or deliverable | Work follows the approved plan |
| 6. Prove | How do we know it works? | Tests, checks, review notes, citations, or validation output | Evidence beats claims |
| 7. Ship | What gets delivered and what remains? | Final summary, PR, client deliverable, or next-task list | Risks and follow-ups are explicit |

## Default Agent Behavior

When a user asks SkillForge to build, fix, audit, research, plan, or consult, the agent should check which Forge Loop stage applies before acting.

- If the user lacks evidence, start at **Signal**.
- If the user has evidence but the ask is vague, start at **Scope**.
- If the scope is clear but not buildable, start at **Spec**.
- If the spec is approved, move to **Plan**.
- If the plan is approved, move to **Build**.
- After every meaningful output, run **Prove** before declaring success.
- End with **Ship** so the user knows what changed and what comes next.

## Hard Rules

1. Do not skip from vague idea to code.
2. Do not claim completion without evidence.
3. Do not hide uncertainty.
4. Do not create giant tasks when smaller verified slices are possible.
5. Do not treat research as complete unless sources, assumptions, and gaps are visible.
6. Do not merge or ship without a review/verification step.

## How SignalBrief Fits

SignalBrief owns the **Signal** stage. It discovers outside evidence from public conversation, market movement, competitor activity, buyer pain, community chatter, and other external signals.

SkillForge then converts that evidence into:

- discovery questions,
- consulting proposals,
- MVP specs,
- repo audit plans,
- branch tasks,
- outreach drafts,
- quality gates,
- client-ready deliverables.

## Output Standard

Every Forge Loop deliverable should answer:

1. What was requested?
2. What evidence or context was used?
3. What decision was made?
4. What changed or should change?
5. How was it verified?
6. What remains open?

## Philosophy

- **Evidence over claims** — prove the work.
- **Small slices over big swings** — reduce risk.
- **Workflow over vibes** — follow the method.
- **Reusable artifacts over one-off chat** — produce assets that compound.
- **Business outcomes over prompt tricks** — the point is delivery.
