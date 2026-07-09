# SkillForge Roadmap

SkillForge starts as a branded fork of a strong agent-skills foundation and grows into a productized workflow layer for AI agents, consultants, founders, operators, and builders.

The MiamiCreme stack now has three coordinated but separate public layers:

1. **SignalBrief** — social and market intelligence.
2. **FrameBrief** — video and visual evidence intelligence.
3. **SkillForge** — workflow, delivery, quality gates, and client-ready artifacts.

Private **EmpireOS** should consume these modules through stable contracts. It should not be mixed into the public repos.

## Phase 1: Identity and Structure

- Replace upstream-facing branding with SkillForge positioning.
- Add clear attribution to the original MIT-licensed project.
- Add `recipes/` for end-to-end workflows.
- Add `packs/` for productized use cases.
- Keep the original engineering skills intact until the SkillForge layer is stable.
- Position the Forge Loop as the central methodology.

## Phase 2: Module Boundaries

Keep the stack modular before adding more features.

- Document product boundaries in `docs/modular-architecture.md`.
- Keep SkillForge, SignalBrief, FrameBrief, EmpireOS, and DealFlow as separate products.
- Define shared artifact and evidence contracts.
- Treat EmpireOS and DealFlow adapters as private integrations unless a public-safe contract is useful.
- Avoid shared code until two or more products have proven they need the same module.

## Phase 3: Starter Packs

The starter packs are:

1. Repo Audit Pack
2. AI Consultant Pack
3. MVP Builder Pack
4. Business Ops Pack
5. SignalBrief Research Pack

Each pack should include:

- purpose,
- target customer,
- input checklist,
- output format,
- agent workflow,
- quality gates,
- sample deliverable,
- module contract if it needs to be consumed by EmpireOS later.

## Phase 4: Evidence Layers

Integrate evidence sources into the Forge Loop:

- SignalBrief for market/social/company/founder/competitor evidence.
- FrameBrief for video/demo/screen-recording/ad/course/walkthrough evidence.
- Plain uploaded docs/files for internal source-of-truth evidence.
- Repo scans for code evidence.

The goal is to make every recommendation traceable to a signal, source, frame, timestamp, file, test, or explicit assumption.

## Phase 5: Recipes

Core recipes:

- Repo Audit
- Client Discovery
- MVP Builder
- Business Ops
- SignalBrief to Proposal
- SignalBrief to MVP
- Video to Brief

Near-term recipe additions:

- Video to Bug Report
- Video to Creative Teardown
- Company Brief to Discovery Questions
- Deal Brief to Buyer Outreach
- Repo Audit to Branch Plan
- Artifact to EmpireOS Mission
- Artifact to DealFlow Summary

## Phase 6: Contracts and Adapters

Add contract-first module documentation before implementation:

- `contracts/artifact.schema.json`
- `contracts/evidence.schema.json`
- `contracts/quality-gate.schema.json`
- `adapters/signalbrief/README.md`
- `adapters/framebrief/README.md`
- `adapters/empireos/README.md`
- `adapters/dealflow/README.md`

The public adapter docs should describe the interface. Private logic stays in EmpireOS or DealFlow.

## Phase 7: Validation

Add validation scripts for SkillForge-specific content:

- recipe schema checks,
- pack README checks,
- broken internal link detection,
- reference-file packaging checks,
- install doctor command,
- sample-output checks,
- skill activation checks,
- artifact contract validation,
- evidence contract validation,
- adapter contract validation.

## Phase 8: Demonstrations

Create public demos showing:

- a messy repo audit,
- a 30-day MVP plan,
- an AI consulting discovery workflow,
- a business operations automation assessment,
- a SignalBrief-to-proposal workflow,
- a FrameBrief video teardown,
- a video bug-repro-to-fix-plan workflow,
- an artifact moving into an EmpireOS-style mission summary without exposing private EmpireOS code.

## Phase 9: Productization

Possible paid/professional layers:

- premium packs,
- client-ready templates,
- repo audit report generator,
- AI automation assessment kit,
- SignalBrief market intelligence reports,
- FrameBrief video intelligence reports,
- team-specific private skill packs,
- custom implementation services.

## Guiding Principle

SkillForge should not become a pile of prompts. Every addition must be actionable, verifiable, and useful inside a real workflow.

Evidence should flow into the Forge Loop. The Forge Loop should produce work people can use, sell, test, ship, or hand to a team.

Module outputs should be clean enough that EmpireOS can consume them later without needing to know which public product produced them.
