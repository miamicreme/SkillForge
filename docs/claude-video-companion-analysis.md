# Claude Video Companion Analysis

This note explains how [`bradautomates/claude-video`](https://github.com/bradautomates/claude-video) can fit into the MiamiCreme AI workflow stack.

## Verdict

Yes — Claude Video is useful as a companion capability.

It should not replace SignalBrief. It should extend the evidence layer for cases where the signal lives inside video, screen recordings, demos, ads, webinars, podcasts, TikToks, YouTube videos, Looms, or local `.mp4/.mov` files.

## Where It Fits

| Layer | Tool | Role |
|---|---|---|
| Market/social research | SignalBrief | Searches public conversation, engagement, source clusters, and market chatter |
| Video/audio evidence | Claude Video `/watch` | Watches a video by combining captions/transcript, frames, and timestamps |
| Workflow/delivery | SkillForge | Turns evidence into specs, proposals, audits, MVP plans, and client deliverables |

## Best Use Cases

| Use Case | Why Claude Video Helps | SkillForge Output |
|---|---|---|
| Competitor launch video | Separates real product changes from hype | Competitive memo, feature gap list |
| YouTube/TikTok ad analysis | Captures hooks, visual structure, offer, pacing, and CTA | Creative teardown, ad script, content plan |
| Screen-recorded bug repro | Sees the UI state and timestamp where the issue happens | Bug report, reproduction steps, fix plan |
| Course or webinar | Converts long video into searchable notes and action items | SOP, training notes, implementation checklist |
| Product demo | Reads both spoken claims and visual workflow | MVP spec, UX notes, feature map |
| Real estate/business video walkthrough | Pulls condition notes, visible risks, and talking points | Deal notes, buyer brief, due diligence checklist |

## Integration Pattern

Do not make SkillForge depend on Claude Video at runtime yet.

Instead, treat `/watch` output as an optional evidence source:

1. Run `/watch <video-url-or-path> <question>`.
2. Capture the timestamped findings.
3. Feed the findings into a SkillForge recipe.
4. Convert them into a reusable artifact.
5. Cite assumptions and gaps.

## Suggested Recipe

Use `recipes/video-to-brief.md` when the user's source material is video-first.

## Guardrails

- Do not claim the video was reviewed unless `/watch` output or equivalent frame/transcript evidence is available.
- Prefer focused windows for long videos when the user asks about a specific moment.
- Use transcript-only mode when visuals do not matter.
- Use frames when the visual state, UI, body language, product demo, or on-screen text matters.
- Keep token cost visible when using many frames.
- Preserve timestamps in downstream briefs.

## Strategic Use

Claude Video gives MiamiCreme a practical edge because many buyers, founders, creators, and competitors communicate through video before anything is documented. SignalBrief finds the public conversation around the market. Claude Video watches the source material itself. SkillForge turns both into an action plan.

## Positioning Line

SignalBrief searches the conversation. Claude Video watches the evidence. SkillForge turns both into deliverables.
