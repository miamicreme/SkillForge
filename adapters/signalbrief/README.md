# SignalBrief Adapter

The SignalBrief Adapter converts market, social, company, founder, competitor, buyer-pain, deal, and trend research into SkillForge artifacts.

## Source Module

`miamicreme/signalbrief`

## Purpose

Preserve SignalBrief as the evidence-gathering layer while allowing SkillForge, EmpireOS, DealFlow, or client reports to consume the findings.

## Inputs

- SignalBrief topic
- research timeframe
- source list or source summary
- cited claims
- confidence notes
- user decision being supported
- optional raw brief Markdown or HTML

## Output Artifact Types

- `signal_brief`
- `proposal`
- `mvp_plan`
- `deal_brief`
- `client_discovery_summary`

## Required Evidence Handling

The adapter must preserve:

- source URLs or source descriptions,
- claim summaries,
- source type,
- confidence level,
- assumptions and gaps,
- captured date/time if available.

## Quality Gate

A converted SignalBrief artifact should be `pass` only when:

- the decision supported is clear,
- at least one evidence item is present,
- assumptions are visible,
- next actions are specific,
- the artifact can be rendered into a client-ready brief or internal decision note.

Use `warn` when evidence is thin or the brief depends heavily on assumptions.

Use `fail` when there is no usable source evidence.

## Example Flow

```text
SignalBrief company research
  -> SignalBrief Adapter
  -> signal_brief artifact
  -> SkillForge signalbrief-to-proposal recipe
  -> proposal artifact
  -> EmpireOS follow-up mission
```

## Boundary Rule

Do not copy SignalBrief runtime code into SkillForge. This adapter is a contract layer, not the search engine.
