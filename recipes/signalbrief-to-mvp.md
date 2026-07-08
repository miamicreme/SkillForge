# Recipe: SignalBrief to MVP

Use this recipe when public market signal, buyer pain, competitor movement, or community chatter needs to become a buildable MVP plan.

## Goal

Turn research into a focused MVP spec that solves one painful problem well.

## Inputs

- SignalBrief or equivalent research notes
- Target customer
- Problem category
- Desired product direction
- Constraints: budget, timeline, stack, team, compliance, integrations
- Existing assets or repo if any

## Steps

### 1. Extract Pain Signals

Look for repeated signals:

- complaints,
- workarounds,
- high-engagement questions,
- competitor shortcomings,
- manual processes,
- willingness to pay,
- urgent events,
- repeated language from buyers/users.

### 2. Cluster the Pain

Group evidence into themes:

| Pain Theme | Evidence | User Type | Severity | Opportunity |
|---|---|---|---|---|
| Manual workflow | Repeated complaints | Operators | High | Automation MVP |
| Poor visibility | Users ask for reports | Managers | Medium | Dashboard MVP |
| Slow research | People compare tools manually | Consultants | High | Briefing assistant |

### 3. Pick One Wedge

Choose the smallest wedge that can win:

- one user,
- one painful workflow,
- one clear outcome,
- one measurable improvement.

Avoid combining every idea into the MVP.

### 4. Define the MVP Promise

Write the promise in this format:

> For `<target user>` who struggle with `<pain>`, this MVP helps them `<outcome>` by `<mechanism>`.

### 5. Create the MVP Spec

The MVP spec must include:

- target user,
- problem statement,
- user stories,
- core workflow,
- data model outline,
- integrations,
- non-goals,
- success metrics,
- risks,
- testing plan,
- launch checklist.

### 6. Create Build Slices

Break implementation into small slices:

1. Data model and seed path
2. Core create/read/update/delete flow
3. Main workflow screen or CLI action
4. AI/research integration
5. Export/share output
6. Quality gates and error handling
7. Demo data and onboarding

### 7. Validate Against the Signal

Before building, check:

- Does this MVP solve the strongest repeated pain?
- Is the buyer/user obvious?
- Can the first version be demoed quickly?
- Is the output valuable without perfect automation?
- Is the scope small enough to ship?

## Output Template

```markdown
# MVP Spec: <Name>

## Research Basis

## Target User

## Problem Statement

## MVP Promise

## Core Workflow

## User Stories

## Data Model Outline

## Integrations

## Non-Goals

## Build Slices

## Success Metrics

## Risks

## Test Plan

## Launch Checklist
```

## Quality Gates

The MVP plan is not ready until:

- one wedge is selected,
- non-goals are explicit,
- the plan has verifiable build slices,
- research signals support the chosen pain,
- the first demo path is clear.
