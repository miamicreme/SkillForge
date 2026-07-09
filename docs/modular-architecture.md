# SkillForge Modular Architecture

This plan keeps SkillForge, SignalBrief, FrameBrief, and future MiamiCreme tools separate while making their best parts reusable inside private EmpireOS.

## Core Principle

Do not build one giant repo that mixes every idea together.

Build small modules with stable contracts:

> Public products stay independent. Private EmpireOS consumes their outputs through adapters.

That means SkillForge should not directly own SignalBrief, FrameBrief, DealFlow, or EmpireOS logic. SkillForge should define the delivery method, recipes, packs, quality gates, and artifact contracts that other systems can use.

## Product Boundaries

| Product | Ownership Boundary | What It Produces | What It Should Not Own |
|---|---|---|---|
| SkillForge | Workflow, delivery, recipes, packs, quality gates | Specs, plans, tasks, audits, proposals, quality gates, reusable artifacts | Social search engine runtime, video runtime, EmpireOS private data, DealFlow business logic |
| SignalBrief | Social, market, company, founder, competitor, buyer-pain, deal, and trend research | Evidence-driven market briefs and signal summaries | Delivery project management, EmpireOS UI, video-frame analysis |
| FrameBrief | Video, visual, transcript, timestamp, and screen-recording intelligence | Timestamped video briefs, bug repro notes, creative teardowns, demo notes | Social search, product delivery orchestration, EmpireOS UI |
| EmpireOS | Private personal command center and AI team operating system | Daily priorities, missions, decisions, AI team workspaces, private memory, dashboards | Public skill-pack branding, upstream fork logic, external product identity |
| DealFlow / Deal Intelligence | Deal-specific research, scoring, buyer fit, follow-up strategy | Deal score, buyer fit, probability, risks, next best action | Generic agent-skill runtime or public SkillForge branding |

## Module Layers

SkillForge should evolve into modules that can be reused without forcing every product into the same repo.

| Layer | Module | Purpose | Reusable In EmpireOS? |
|---|---|---|---|
| Core Method | Forge Loop | Signal, Scope, Spec, Plan, Build, Prove, Ship | Yes |
| Core Contract | Artifact Contract | Shared JSON/Markdown shape for briefs, plans, audits, proposals | Yes |
| Core Contract | Evidence Contract | Shared shape for facts, sources, confidence, assumptions, timestamps | Yes |
| Input Module | SignalBrief Adapter | Converts market/social research into SkillForge artifacts | Yes |
| Input Module | FrameBrief Adapter | Converts video/transcript/frame evidence into SkillForge artifacts | Yes |
| Input Module | Repo Audit Adapter | Converts repo scan findings into audit artifacts | Yes |
| Workflow Module | Recipe Runner | Executes recipes like repo audit, client discovery, MVP builder | Yes |
| Pack Module | Pack Registry | Lists available packs, inputs, outputs, and gates | Yes |
| Output Module | Brief Renderer | Converts artifact data into Markdown, HTML, proposal, report, or handoff | Yes |
| Output Module | Task Planner | Converts artifacts into branch plans, tickets, missions, or AI-team tasks | Yes |
| Integration Module | EmpireOS Adapter | Converts SkillForge artifacts into EmpireOS missions, priorities, and dashboards | Private only |
| Integration Module | DealFlow Adapter | Converts deal artifacts into DealFlow summaries, buyer fit, and follow-ups | Private or separate product |

## Recommended Repo Strategy

Keep the public repos focused:

```text
miamicreme/SkillForge      # workflow layer, recipes, packs, contracts, quality gates
miamicreme/signalbrief     # market/social intelligence module
miamicreme/FrameBrief      # video intelligence module
private/EmpireOS           # private command center that consumes module outputs
private/DealFlow           # deal intelligence and buyer-matching system
```

Do not make SkillForge depend on EmpireOS.

Do make EmpireOS capable of importing or calling SkillForge modules.

## Recommended Folder Strategy Inside SkillForge

SkillForge can stay documentation-first for now, but the long-term structure should be:

```text
SkillForge/
  skills/                  # agent skills and bootstrap behavior
  recipes/                 # workflow playbooks
  packs/                   # productized service bundles
  contracts/               # shared artifact/evidence schemas
  adapters/                # optional adapters for external modules
    signalbrief/
    framebrief/
    repo-audit/
    empireos/              # documentation only in public repo; implementation stays private
    dealflow/              # documentation only unless public-safe
  renderers/               # markdown/html/report/proposal render contracts
  validators/              # validation scripts and quality gates
  samples/                 # safe sample outputs
  docs/                    # strategy, roadmap, attribution, comparisons
```

## Contract-First Rule

Every module should define:

1. **Inputs** — what the module requires.
2. **Outputs** — what artifact it produces.
3. **Evidence** — sources, confidence, timestamps, and assumptions.
4. **Quality Gate** — how to know the output is usable.
5. **Adapter Surface** — how another product can consume it.

A module is not ready for EmpireOS until it has a stable output contract.

## Shared Artifact Contract

Use one common artifact shape across SkillForge, SignalBrief, FrameBrief, DealFlow, and EmpireOS.

```json
{
  "artifact_id": "string",
  "artifact_type": "repo_audit | signal_brief | frame_brief | proposal | mvp_plan | business_ops_assessment | deal_brief",
  "source_module": "skillforge | signalbrief | framebrief | dealflow | empireos",
  "title": "string",
  "summary": "string",
  "decision_supported": "string",
  "evidence": [
    {
      "source_type": "url | repo | file | transcript | frame | user_context | assumption",
      "source": "string",
      "claim": "string",
      "confidence": "low | medium | high",
      "timestamp": "optional string"
    }
  ],
  "risks": ["string"],
  "next_actions": ["string"],
  "quality_gate": {
    "status": "pass | warn | fail",
    "notes": "string"
  },
  "render_targets": ["markdown", "html", "empireos", "dealflow", "proposal"]
}
```

## EmpireOS Consumption Model

EmpireOS should not care where the artifact came from. It should care what the artifact means.

EmpireOS can consume:

| Artifact Type | EmpireOS Use |
|---|---|
| `repo_audit` | Create engineering mission, branch plan, and task queue |
| `signal_brief` | Add market context to daily command center or opportunity board |
| `frame_brief` | Create video-derived tasks, bug reports, creative notes, or deal notes |
| `proposal` | Track client opportunity and next follow-up |
| `mvp_plan` | Create product mission and build roadmap |
| `business_ops_assessment` | Create automation roadmap and client delivery plan |
| `deal_brief` | Create deal score, follow-up plan, buyer target, and daily action |

## EmpireOS Adapter Contract

The public SkillForge repo can document this adapter, but the implementation should live privately in EmpireOS.

```json
{
  "empireos_summary": {
    "priority": "low | medium | high | urgent",
    "mission_type": "build | sell | research | fix | follow_up | decide",
    "recommended_team": "string",
    "next_best_action": "string",
    "due_today": true,
    "probability_of_success": 0.0,
    "risk_level": "low | medium | high",
    "linked_artifact_id": "string"
  }
}
```

## Build Order

1. Keep the repos separate.
2. Add shared contracts to SkillForge.
3. Add adapters as docs first, not heavy code.
4. Add sample artifacts for each module.
5. Add validators that check every pack and recipe has inputs, outputs, evidence, and gates.
6. Let EmpireOS privately import or call the modules later.
7. Only extract a shared package when two or more products need the same code.

## What To Avoid

- Do not put EmpireOS private workflows in public repos.
- Do not make SkillForge a dumping ground for every skill idea.
- Do not make SignalBrief or FrameBrief depend on EmpireOS.
- Do not merge repos just because they work together.
- Do not create shared code until the contract is proven by real sample outputs.

## Decision Rule

If a feature answers **how agents work**, it belongs in SkillForge.

If it answers **what the market is saying**, it belongs in SignalBrief.

If it answers **what happened in a video**, it belongs in FrameBrief.

If it answers **what Kohron should do today**, it belongs in private EmpireOS.

If it answers **whether a deal is good and what to do next**, it belongs in DealFlow / Deal Intelligence.
