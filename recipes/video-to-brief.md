# Recipe: Video to Brief

Use this recipe when a video, screen recording, product demo, ad, webinar, course, TikTok, YouTube video, Loom, or local clip needs to become a useful business artifact.

This recipe is designed to work with Claude Video `/watch` output, but it can also use any timestamped transcript/frame notes.

## Goal

Turn video evidence into a concise, timestamped brief with decisions, insights, risks, and next actions.

## Inputs

- Video URL or local file path
- User question or decision to support
- `/watch` output or equivalent notes
- Target audience
- Desired artifact type: summary, teardown, bug report, proposal notes, MVP spec, content plan, or due diligence brief

## Steps

### 1. Define the Viewing Goal

Ask what the video needs to answer:

- What happened?
- What is actually new?
- What broke?
- What is the hook/offer/CTA?
- What does the demo reveal?
- What should we build, fix, pitch, or avoid?

### 2. Capture Evidence

Use Claude Video or equivalent tooling to capture:

- transcript highlights,
- key frames,
- timestamps,
- visible UI/product states,
- claims made by the speaker,
- moments of confusion, friction, or value.

### 3. Separate Signal from Noise

Classify findings:

| Type | Meaning |
|---|---|
| Claim | What the speaker says is true |
| Visual proof | What appears on screen |
| Workflow | Sequence of actions or steps |
| Problem | Bug, friction, gap, risk, or confusion |
| Opportunity | Feature, offer, positioning, or content angle |
| Unknown | Something unclear or not visible enough |

### 4. Pick the Output Shape

Choose one:

- **Video Summary** — key points and timestamps.
- **Creative Teardown** — hook, structure, pacing, offer, CTA, visuals.
- **Bug Repro Brief** — observed issue, steps, expected vs actual, likely cause, fix path.
- **Product Demo Brief** — features, workflow, UX notes, gaps, opportunities.
- **Training Notes** — process, checklist, SOP, action items.
- **Deal/Walkthrough Notes** — visible condition, risks, questions, buyer angles.

### 5. Write the Brief

Use this structure:

```markdown
# Video Brief: <Title / Source>

## Viewing Goal

## Executive Summary

## Key Moments

| Timestamp | What Happened | Why It Matters |
|---|---|---|

## Evidence Notes

## Risks / Gaps / Unknowns

## Recommended Next Action

## Follow-Up Questions
```

### 6. Convert to a SkillForge Artifact

Depending on the goal, route the brief into:

- `signalbrief-to-proposal.md`,
- `signalbrief-to-mvp.md`,
- `repo-audit.md`,
- `client-discovery.md`,
- `business-ops.md`,
- a custom implementation plan.

## Quality Gates

The brief is not done until:

- timestamps are preserved,
- visible evidence and spoken claims are separated,
- unknowns are explicit,
- the next action is clear,
- the output supports a real decision.

## Example Prompts

```text
/watch <competitor-launch-video> what is actually new, skip the hype
/watch <bug-repro.mov> when does the UI break and what likely caused it?
/watch <ad-video> break down the hook, offer, proof, and CTA
/watch <webinar> summarize this into implementation notes
```
