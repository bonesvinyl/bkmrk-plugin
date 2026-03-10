# bkmrk vs keep.md — Competitive Analysis

**Date:** 2026-03-10

## What They Share

Both products occupy the same niche: turning saved bookmarks (especially X/Twitter bookmarks) into useful, AI-accessible content.

| Capability | bkmrk | keep.md |
|---|---|---|
| X/Twitter bookmark sync | Yes | Yes |
| API access to bookmarks | Yes (REST API) | Yes (REST API + CLI) |
| AI agent integration | Yes (Claude Code skill) | Yes (agent skill) |
| Web app / dashboard | Yes (bkmrkapp.com) | Yes (keep.md web app) |
| Content enrichment | Yes (article extraction) | Yes (markdown extraction) |
| Search bookmarks | Yes | Yes |

## Where They Diverge

**keep.md is a bookmark *storage* tool. bkmrk is a bookmark *execution* engine.**

### keep.md: "Save and Search"

- **Primary value**: Clean markdown extraction and retrieval
- **Workflow**: Save → Store as markdown → Search/retrieve later → Feed to AI as context
- **The AI reads your bookmarks** — agents consume bookmarks as passive reference material
- **Output**: Organized, searchable markdown content
- **Broad capture**: RSS feeds, YouTube, any URL, Chrome bookmarks, X bookmarks
- **Platform agnostic**: Works with any AI agent via skill.md standard, CLI, API
- **Mobile**: iOS/Android share sheet support
- **Privacy focused**: No analytics, no trackers

### bkmrk: "Stage and Execute"

- **Primary value**: Turning bookmarks into completed dev tasks
- **Workflow**: Bookmark → Enrich → Analyze → Stage → Execute via Claude Code agents → Mark done
- **The AI acts on your bookmarks** — agents execute tasks derived from bookmark content
- **Output**: Actual code changes, implementations, and development work
- **Narrow focus**: X/Twitter bookmarks specifically, developer-oriented content
- **Claude Code native**: Deep integration as a Claude Code plugin, uses Task tool for agent swarms
- **Project mapping**: Bookmarks are matched to local dev projects with path resolution
- **Execution intelligence**: Generated prompts, relevance scoring, success criteria, parallel/sequential execution modes

## Strengths of keep.md (relative to bkmrk)

1. **Broader capture surface** — RSS, YouTube transcripts, any URL, Chrome bookmarks, not just X
2. **Platform agnostic** — Works with any AI agent via open skill.md standard, not locked to Claude Code
3. **Mobile support** — Native share sheets on iOS/Android
4. **Simpler mental model** — "Save and search" is easy to understand
5. **CLI tool** — Command-line access for power users
6. **Markdown-first storage** — Content is portable, readable, and standardized
7. **Privacy stance** — Explicit no-tracking commitment

## Strengths of bkmrk (relative to keep.md)

1. **Execution, not just retrieval** — Bookmarks become completed tasks, not just reference material
2. **Intelligence layer** — Analysis, relevance scoring, project matching, generated prompts
3. **Agent orchestration** — Parallel/sequential execution of multiple bookmark tasks via agent swarms
4. **Developer workflow integration** — Bookmarks map to specific local projects with tech stack awareness
5. **Status management** — Staged → Done → Trashed lifecycle gives bookmarks a clear progression
6. **Verification** — Tasks are only marked done if actually accomplished
7. **Richer enrichment** — Full article content + thread context + implementation suggestions, not just markdown extraction

## Competitive Positioning

```
                    Passive (Reference)          Active (Execution)
                    ←─────────────────────────────────────────────→

  Broad capture     keep.md
  (any URL)         Raindrop.io
                    Pocket

  X/Twitter         keep.md (twitter sync)       bkmrk
  focused                                        (bookmark → code)
```

**keep.md** competes horizontally with bookmark managers (Raindrop, Pocket, Pinboard) but differentiates with its markdown-first, AI-agent-friendly approach.

**bkmrk** competes vertically — it's not really a bookmark manager at all. It's a task execution pipeline that happens to use bookmarks as input. There's no real direct competitor doing this.

## Opportunities for bkmrk

1. **Broader input sources** — Consider supporting RSS, YouTube, or arbitrary URLs beyond just X bookmarks
2. **CLI access** — A `bkmrk` CLI could complement the Claude Code skill
3. **Markdown export** — Let users access enriched content as portable markdown
4. **Mobile capture** — Share sheet integration for quick staging from mobile
5. **Multi-agent support** — Consider skill.md standard adoption for agent-agnostic access
6. **Hybrid mode** — Some bookmarks are reference, some are tasks — let users choose per bookmark

## Threats from keep.md

- **Low**: keep.md could theoretically add execution features, but their architecture is storage-oriented
- **Medium**: If keep.md's agent skill becomes the default way developers feed bookmarks to Claude Code, bkmrk loses the "input" step
- **Worth watching**: keep.md could become an upstream data source that feeds into bkmrk, rather than a competitor — a potential integration partner

## Summary

**keep.md** = "Your bookmarks, as clean markdown, accessible everywhere"
**bkmrk** = "Your bookmarks, analyzed and executed as dev tasks"

They solve different problems. keep.md answers "how do I find that thing I saved?" while bkmrk answers "how do I actually do the thing I bookmarked?"
