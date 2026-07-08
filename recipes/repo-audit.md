# Repo Audit Recipe

Use this recipe when a repository needs a senior-level quality review and a practical improvement plan.

## Goal

Produce a clear repo audit that answers:

- What is built?
- What works?
- What is incomplete?
- What is risky?
- What should be fixed first?
- What branches/tasks should be created?

## Inputs

- Repository URL or uploaded source archive
- Product goal or intended customer
- Known bugs or blockers
- Deployment target
- Time and budget constraints

## Workflow

1. **Inventory the repo**
   - Identify framework, language, package manager, deployment target, and architecture.
   - Locate app entry points, modules, tests, environment files, and CI/CD.

2. **Score the repo**
   - Architecture
   - Product completeness
   - Code quality
   - Test coverage
   - Security
   - Performance
   - Deployment readiness
   - UX/UI completeness

3. **Find blockers**
   - Broken install/build/run flow
   - Missing environment variables
   - Stubbed or mocked critical paths
   - Auth, payment, database, or API gaps
   - No tests or failing tests

4. **Create branch plan**
   - One branch per logical improvement.
   - Keep branches small enough to review.
   - Include acceptance criteria and proof required.

5. **Produce final audit**
   - 0-10 rating
   - Executive summary
   - Risk matrix
   - Prioritized issues
   - Branch/task plan
   - Suggested first pull request

## Recommended Skills

- `context-engineering`
- `planning-and-task-breakdown`
- `code-review-and-quality`
- `security-and-hardening`
- `performance-optimization`
- `documentation-and-adrs`
- `git-workflow-and-versioning`

## Output Format

```md
# Repo Audit

## Score

## Executive Summary

## What Works

## Major Issues

## Risk Matrix

## Branch Plan

## First 72 Hours

## Acceptance Criteria
```

## Quality Gate

Do not call the audit complete unless the repo has been inspected at the file/module level and each recommendation maps to a concrete task or branch.
