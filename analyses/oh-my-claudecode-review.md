# oh-my-claudecode — Review

**Source:** https://x.com/hasantoxr/status/2037963932204445836
**Reviewed:** 2026-03-29

Multi-agent orchestration layer on top of Claude Code. 3.6K GitHub stars, open source.

## Modes
- Autopilot, Ultrapilot (parallel), Swarm, Pipeline, Ecomode (30-50% cost reduction claim)
- 32 specialized agents, smart Haiku→Opus model routing, auto-resume on rate limits

## Pros
- Zero switching cost — layers on Claude Code directly
- Auto-resume on rate limits eliminates babysitting
- Ecomode/model routing could cut costs
- Open source, 3.6K stars, auditable

## Cons
- Marketing numbers with no methodology
- Overlaps heavily with MSAP
- 32 agents is a marketing number until audited
- Magic keyword triggers fragile vs explicit skills/hooks
- Unknown compatibility with our protocol stack

## Recommendation
Investigate, don't adopt wholesale. Evaluate Ecomode logic and auto-resume implementation — extract what's useful for MSAP.
