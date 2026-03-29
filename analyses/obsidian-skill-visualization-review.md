# Obsidian Skill Visualization — Review

**Source:** https://x.com/raillyhugo/status/2037786612147331157
**Reviewed:** 2026-03-29

Using Obsidian as a visual browser/management interface for Claude Code skills, commands, and agents.

## What It Shows
- Obsidian vault structured to mirror Claude Code skill library
- Browsable categories: Skills, Commands, Agents
- Detail views with token counts, trigger conditions, priority tables
- 60+ items catalogued with metadata

## Pros
- Discoverability at scale (search, tags, graph view)
- Token-aware cataloguing (~1.3k per skill visible at a glance)
- Structured trigger conditions enable better routing
- Naming prefix conventions (async-, bundle-, server-) aid parsing
- 671 bookmarks — strong community validation

## Cons
- Documentation only, not runtime — vault can drift from actual skills
- Dual maintenance if skills live in .claude/ and Obsidian
- Local tool by default, sharing requires sync setup
- No dependency/conflict tracking between skills

## Recommendation
Adopt the concept. Add YAML frontmatter (token count, triggers) to skill files. Extend existing Obsidian vault to browse skills. Don't treat vault as source of truth — .claude/ stays authoritative. Priority: Medium-High, payoff grows with library size.
