---
name: repo-productization
description: Turns a technical repository into a credible portfolio or commercial product. Use when a working project needs positioning, onboarding, proof, packaging, deployment clarity, or buyer-ready presentation.
---

# Repository Productization

## Objective

Transform a repository from “code that exists” into a product that a developer, employer, client, or customer can understand, run, trust, and evaluate.

## Process

### 1. Define the product truth

Document:

- target user;
- expensive or painful problem solved;
- primary workflow;
- measurable outcome;
- current maturity;
- what is real, partial, simulated, or planned.

Never market planned functionality as implemented.

### 2. Establish the golden path

Choose one workflow that demonstrates the product's value. It must have:

- a clear starting state;
- realistic inputs;
- observable processing;
- a useful output;
- a repeatable demo path;
- failure handling.

### 3. Improve first-run experience

Require:

- concise product-first README;
- prerequisites and supported versions;
- one canonical setup path;
- `.env.example` without secrets;
- seed or sample data where appropriate;
- screenshots, diagrams, or a short demo;
- troubleshooting for common failures.

### 4. Add trust signals

Evaluate and improve:

- automated tests and CI status;
- architecture and key tradeoffs;
- security posture;
- observability and system health;
- license and attribution;
- roadmap and known limitations;
- changelog or release notes.

### 5. Package the story

Create messaging at three levels:

- **one sentence** — user, problem, outcome;
- **one paragraph** — workflow, differentiation, proof;
- **case study** — context, constraints, architecture, decisions, results, lessons.

### 6. Separate audiences

Tailor the repository experience for:

- developers who need to run and extend it;
- employers who need evidence of engineering judgment;
- clients who need confidence in delivery and risk control;
- users who need a clear outcome and simple workflow.

### 7. Grade readiness

Score 0–5 for:

- product clarity;
- setup reproducibility;
- demonstrated value;
- technical credibility;
- operational readiness;
- security and privacy;
- visual presentation;
- commercial positioning.

Prioritize the lowest scores that block adoption or trust.

## Required Output

1. Current product assessment
2. Product positioning statement
3. Golden-path definition
4. Missing trust signals
5. Repository changes by priority
6. Demo and case-study plan
7. Release checklist

## Anti-Rationalization

| Excuse | Response |
|---|---|
| “The code speaks for itself.” | Evaluators cannot value what they cannot quickly understand. |
| “It is only a portfolio project.” | Portfolio projects are judged by clarity, decisions, and proof. |
| “Screenshots are enough.” | Visual proof does not replace reproducible behavior. |
| “We can call unfinished features beta.” | Maturity labels do not excuse inaccurate claims. |

## Exit Criteria

The repository is productized when a new evaluator can understand the value, reproduce the golden path, inspect credible engineering evidence, and distinguish shipped capability from roadmap.
