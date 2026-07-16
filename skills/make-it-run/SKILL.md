---
name: make-it-run
description: Reproduces and repairs repository setup or runtime failures. Use when asked to make a project run correctly, fix broken startup, or produce reliable local execution instructions.
---

# Make It Run

## Objective

Take a repository from an unverified or broken state to a reproducible working state with evidence.

## Process

### 1. Inspect before changing

Identify the stack, package manager, runtime versions, entry points, environment variables, services, and documented commands. Compare README claims with actual configuration.

### 2. Reproduce the failure

Start from the cleanest available state. Capture:

- exact command;
- exact failure output;
- environment and versions;
- first failing boundary.

Do not patch symptoms before reproducing the problem.

### 3. Localize the root cause

Reduce the failure to one category:

- dependency or version mismatch;
- missing configuration or secret;
- database or migration failure;
- incorrect command or file path;
- compile or type failure;
- runtime logic defect;
- external service dependency;
- operating-system assumption.

### 4. Apply the smallest durable fix

Prefer fixes that improve the repository for every future user:

- pin or document supported versions;
- repair scripts and defaults;
- add `.env.example` values without secrets;
- make migrations deterministic;
- improve error messages;
- add a regression test;
- remove undocumented manual steps.

Do not disable tests, validation, authentication, or security controls merely to make startup succeed.

### 5. Verify in layers

Run the applicable sequence:

1. dependency installation;
2. static analysis or type checking;
3. unit and integration tests;
4. production build;
5. local startup;
6. health endpoint or equivalent;
7. primary user workflow.

Record commands and results.

### 6. Repair the developer experience

Update setup instructions so a new developer can reproduce the result. Include prerequisites, environment variables, service startup order, migrations, launch command, and known limitations.

## Required Output

- root cause;
- files changed;
- verification evidence;
- exact run commands;
- unresolved external dependencies;
- rollback guidance where behavior changed.

## Anti-Rationalization

| Excuse | Response |
|---|---|
| “It works on my machine.” | Reproducibility requires documented versions and commands. |
| “Skipping the test makes it green.” | Removing evidence does not repair behavior. |
| “The missing secret is the user's problem.” | Required configuration must be clearly declared and validated. |
| “A large refactor is cleaner.” | Fix the failure with the smallest durable change first. |

## Exit Criteria

The task is complete only when the repository starts through documented commands and the primary workflow has been verified, or when an external blocker is precisely identified with reproduction evidence.
