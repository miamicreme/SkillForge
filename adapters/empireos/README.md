# EmpireOS Adapter

The EmpireOS Adapter converts SkillForge artifacts into private EmpireOS missions, priorities, next actions, dashboards, and AI-team work items.

## Target Module

Private `EmpireOS`

## Purpose

Let EmpireOS reuse SkillForge, SignalBrief, FrameBrief, Repo Audit, Business Ops, and DealFlow artifacts without putting private EmpireOS logic into public repos.

## Input

Any valid SkillForge artifact:

- `repo_audit`
- `signal_brief`
- `frame_brief`
- `proposal`
- `mvp_plan`
- `business_ops_assessment`
- `deal_brief`
- `branch_plan`
- `implementation_handoff`
- `client_discovery_summary`

## Output Shape

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

## Mapping Rules

| Artifact Type | EmpireOS Mission Type |
|---|---|
| `repo_audit` | `fix` or `build` |
| `signal_brief` | `research` or `decide` |
| `frame_brief` | `research`, `fix`, or `build` |
| `proposal` | `sell` or `follow_up` |
| `mvp_plan` | `build` |
| `business_ops_assessment` | `build` or `decide` |
| `deal_brief` | `sell`, `follow_up`, or `decide` |

## Public Boundary

This public adapter doc may define the interface. The actual EmpireOS implementation should remain private.

Never include:

- private user memory,
- financial data,
- client credentials,
- personal dashboards,
- private daily routines,
- personal decision logs.

## Quality Gate

An EmpireOS adapter output is usable only when it produces:

- one clear next best action,
- priority,
- mission type,
- risk level,
- linked source artifact,
- enough context for a private AI team member to act.
