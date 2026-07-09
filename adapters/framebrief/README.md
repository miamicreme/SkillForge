# FrameBrief Adapter

The FrameBrief Adapter converts video, transcript, timestamp, frame, demo, walkthrough, ad, course, webinar, and screen-recording evidence into SkillForge artifacts.

## Source Module

`miamicreme/FrameBrief`

## Purpose

Preserve FrameBrief as the video-evidence layer while allowing SkillForge, EmpireOS, DealFlow, QA workflows, and client reports to consume timestamped findings.

## Inputs

- video URL or file reference
- user question or viewing goal
- timestamped transcript notes
- frame or scene notes
- visible claims or UI observations
- uncertainty/gap notes
- optional `/watch` output

## Output Artifact Types

- `frame_brief`
- `repo_audit`
- `proposal`
- `mvp_plan`
- `deal_brief`
- `implementation_handoff`

## Required Evidence Handling

The adapter must preserve:

- timestamps,
- visible evidence,
- spoken claims,
- transcript-derived evidence,
- frame-derived evidence,
- assumptions and unknowns.

Spoken claims and visual proof should be separated when possible.

## Quality Gate

A converted FrameBrief artifact should be `pass` only when:

- the viewing goal is clear,
- timestamps are preserved,
- visible evidence and spoken claims are not mixed together,
- unknowns are explicit,
- the next action is specific.

Use `warn` when the video was only partially reviewed, transcript-only, or frame evidence is sparse.

Use `fail` when the output lacks timestamps or evidence.

## Example Flow

```text
FrameBrief product demo review
  -> FrameBrief Adapter
  -> frame_brief artifact
  -> SkillForge video-to-brief recipe
  -> MVP feature gap summary
  -> EmpireOS product mission
```

## Boundary Rule

Do not copy FrameBrief runtime code into SkillForge. This adapter is a contract layer, not the video analysis runtime.
