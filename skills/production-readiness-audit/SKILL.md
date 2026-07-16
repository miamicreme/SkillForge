---
name: production-readiness-audit
description: Audits a repository for real production readiness. Use when asked whether a project runs, is deployable, is secure enough to ship, or is ready for customers.
---

# Production Readiness Audit

## Objective

Produce an evidence-backed answer to one question: **Can this repository be operated safely in production today?**

Do not confuse attractive code, extensive documentation, or a passing build with production readiness.

## Process

### 1. Establish the operating target

Identify:

- intended users and critical workflows;
- runtime, hosting, database, queues, storage, and external services;
- environments and deployment method;
- stated reliability, security, privacy, and performance expectations.

Record assumptions where the repository does not provide an answer.

### 2. Prove setup from a clean state

Inspect the documented setup and compare it to actual configuration files. Verify:

- prerequisites and supported versions;
- dependency installation;
- environment-variable documentation;
- database migrations and seed path;
- local start commands;
- production build commands.

A setup step that depends on tribal knowledge is a finding.

### 3. Verify the golden path

Run or inspect the most important end-to-end workflow. Capture evidence for:

- application startup;
- authentication and authorization;
- primary create/read/update behavior;
- persistence;
- background jobs or integrations;
- expected failure behavior.

### 4. Review production controls

Evaluate:

- input validation and permission boundaries;
- secret handling and dependency risk;
- structured logs and correlation identifiers;
- health, readiness, and liveness behavior;
- metrics, traces, and alertable symptoms;
- backups, migrations, rollback, and data recovery;
- rate limits, timeouts, retries, and idempotency;
- CI quality gates and deployment controls.

### 5. Grade findings

Use four levels:

- **Blocker** — unsafe or impossible to launch;
- **High** — likely customer, security, or data-impacting failure;
- **Medium** — meaningful operational weakness;
- **Low** — polish or maintainability improvement.

Every finding must include evidence, impact, and a concrete remediation.

### 6. Issue the verdict

Choose exactly one:

- **Ready** — launch evidence is complete and no blockers remain;
- **Conditionally ready** — limited rollout is acceptable with named controls;
- **Not ready** — one or more blockers prevent responsible launch;
- **Unable to verify** — required runtime access or evidence is unavailable.

## Required Output

1. Executive verdict
2. Evidence reviewed
3. Golden-path result
4. Findings ordered by severity
5. Seven-day remediation plan
6. Launch checklist
7. Remaining unknowns

## Anti-Rationalization

| Excuse | Response |
|---|---|
| “The build passes.” | A build does not prove runtime behavior or recoverability. |
| “It is only an MVP.” | MVP reduces scope, not the need to protect users and data. |
| “Monitoring can come later.” | Unobservable production systems fail silently. |
| “The README says it works.” | Documentation is a claim until reproduced. |

## Exit Criteria

The audit is complete only when the verdict is tied to reproducible evidence and every blocker has an owner-ready remediation.
