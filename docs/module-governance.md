# Module Governance

SkillForge should stay modular, testable, and reusable. This governance document defines the rules for adding modules, adapters, contracts, recipes, and packs.

## Governance Goals

1. Keep public products separate.
2. Make module outputs reusable in private EmpireOS.
3. Prevent SkillForge from becoming a random prompt library.
4. Preserve attribution and license clarity.
5. Require every workflow to produce a useful artifact.
6. Make quality gates visible before promotion.

## Module Acceptance Standard

A module is acceptable only when it has:

| Requirement | Meaning |
|---|---|
| Clear owner | The product/repo responsible for the module is obvious |
| Stable purpose | The module solves one category of problem |
| Input contract | The required inputs are documented |
| Output contract | The produced artifact shape is documented |
| Evidence model | Sources, assumptions, confidence, and timestamps are handled |
| Quality gate | There is a pass/warn/fail or equivalent completion check |
| Adapter surface | Other systems know how to consume the output |
| Safe examples | Sample outputs do not leak private data |

## Boundary Rules

### SkillForge Owns

- Forge Loop methodology
- recipes
- packs
- artifact contracts
- evidence contracts
- quality gates
- public-safe adapter documentation
- sample deliverables
- validators

### SkillForge Does Not Own

- SignalBrief search runtime
- FrameBrief video runtime
- private EmpireOS dashboards
- private personal memory
- DealFlow private underwriting logic
- client credentials, secrets, or private business data

## Public vs Private Rule

Public repos may contain:

- generic schemas,
- public-safe adapters,
- example artifacts,
- documentation,
- reusable methods,
- generic validation logic.

Private repos should contain:

- EmpireOS personal workflows,
- private dashboards,
- private financial or operational memory,
- client-specific implementations,
- DealFlow proprietary scoring logic,
- credentials and integrations.

## Dependency Direction

Dependencies must flow one way:

```text
SignalBrief  ┐
FrameBrief   ├──> SkillForge artifact contracts ──> EmpireOS private adapters
Repo Audit   ┘
```

SkillForge may define contracts for other systems to use, but it should not directly depend on EmpireOS.

EmpireOS may consume SkillForge, SignalBrief, FrameBrief, and DealFlow outputs, but public modules should not require EmpireOS to work.

## Versioning Rule

Contracts should be versioned before any consuming system depends on them.

Use semantic contract versions:

```text
artifact_contract_version: 0.1.0
```

Breaking changes require:

- new version number,
- migration notes,
- sample before/after artifact,
- compatibility note for EmpireOS/DealFlow adapters.

## Naming Rules

Use clear names:

| Type | Naming Pattern | Example |
|---|---|---|
| Skill | `using-name` or task name | `using-skillforge` |
| Recipe | outcome phrase | `signalbrief-to-proposal.md` |
| Pack | use-case folder | `packs/repo-audit/` |
| Contract | noun schema | `artifact.schema.json` |
| Adapter | source or target module | `adapters/empireos/` |
| Sample | artifact type + example | `samples/repo-audit/basic-saas-audit.md` |

## Quality Gate Rule

Every recipe, pack, and adapter must answer:

1. What input is required?
2. What output is produced?
3. What evidence supports the output?
4. What assumptions remain?
5. What makes the output pass, warn, or fail?
6. What should happen next?

## No Hidden Coupling Rule

A module should not secretly require another module unless it declares that dependency.

Use this pattern:

```yaml
requires:
  - artifact_contract: "0.1.0"
optional_inputs:
  - signalbrief
  - framebrief
outputs:
  - proposal
  - mvp_plan
```

## EmpireOS Reuse Rule

Before a module is reused in EmpireOS, it should have:

- stable artifact type,
- stable next-action format,
- priority/risk mapping,
- quality gate status,
- source links or evidence notes,
- no public/private boundary violation.

## Review Checklist

Before merging a module change, ask:

- Does this keep repos separate?
- Is this reusable without EmpireOS?
- Can EmpireOS consume the output later?
- Is there a clear contract?
- Are private details excluded?
- Is attribution preserved?
- Is the output useful enough to sell, ship, test, or hand to a team?

## Golden Rule

If a module cannot produce a reusable artifact with evidence and a quality gate, it is not ready for SkillForge.
