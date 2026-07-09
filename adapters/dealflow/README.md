# DealFlow Adapter

The DealFlow Adapter converts SkillForge, SignalBrief, FrameBrief, and deal-related artifacts into DealFlow summaries, buyer-fit notes, risk analysis, outreach angles, and next actions.

## Target Module

DealFlow / Deal Intelligence

## Purpose

Let DealFlow consume reusable artifacts without coupling deal scoring, buyer matching, or proprietary underwriting logic into public SkillForge.

## Input Artifact Types

- `signal_brief`
- `frame_brief`
- `deal_brief`
- `proposal`
- `business_ops_assessment`
- `client_discovery_summary`

## Output Shape

A public-safe DealFlow adapter may produce:

```json
{
  "dealflow_summary": {
    "deal_name": "string",
    "deal_type": "real_estate | business | asset | partnership | unknown",
    "fit_summary": "string",
    "buyer_angle": "string",
    "risk_level": "low | medium | high",
    "next_best_action": "string",
    "linked_artifact_id": "string"
  }
}
```

Private DealFlow implementations may add proprietary scoring, probability models, underwriting calculations, or buyer-matching logic.

## Boundary Rule

Public SkillForge can define the adapter contract and generic flow.

Private DealFlow should own:

- scoring formulas,
- buyer lists,
- deal underwriting rules,
- financial assumptions,
- proprietary outreach strategy,
- CRM-specific integrations.

## Quality Gate

A DealFlow adapter output is usable only when it includes:

- deal type,
- fit summary,
- buyer or operator angle,
- risk level,
- next best action,
- linked artifact evidence.
