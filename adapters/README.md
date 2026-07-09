# Adapters

Adapters are boundary modules. They convert outputs from one system into inputs another system can understand.

The goal is reuse without coupling.

## Adapter Rules

1. An adapter must not own the source module's runtime.
2. An adapter must not own the target module's private logic.
3. An adapter should transform artifacts, not hide assumptions.
4. An adapter should preserve evidence, confidence, risks, and quality gates.
5. Public adapters should describe contracts only when private implementation details would leak.

## Current Adapter Targets

| Adapter | Purpose | Public or Private? |
|---|---|---|
| `signalbrief/` | Convert market/social research into SkillForge artifacts | Public-safe |
| `framebrief/` | Convert video evidence into SkillForge artifacts | Public-safe |
| `repo-audit/` | Convert repo findings into audit artifacts and branch plans | Public-safe |
| `empireos/` | Convert artifacts into private EmpireOS missions/priorities | Public docs only; implementation private |
| `dealflow/` | Convert artifacts into DealFlow summaries and buyer actions | Public docs unless scoring logic is private |

## Adapter Output Standard

Every adapter should output a valid SkillForge artifact using:

- `contracts/artifact.schema.json`
- `contracts/evidence.schema.json`
- `contracts/quality-gate.schema.json`

## Best-Practice Pattern

```text
source runtime -> source output -> adapter -> SkillForge artifact -> renderer or private consumer
```

Example:

```text
SignalBrief research -> signalbrief adapter -> signal_brief artifact -> SkillForge proposal recipe -> EmpireOS follow-up mission
```
