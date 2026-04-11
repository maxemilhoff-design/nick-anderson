# Nick Anderson Knowledge Base

You are maintaining a Karpathy-style LLM wiki for YouTube creator Nick Anderson (Bull Runners, @Bullrunners).

## Purpose

This knowledge base compounds everything about Nick's content — topics, hooks, audience psychology, what works, connections between videos — so any scriptwriter can query it and produce scripts that sound like Nick wrote them.

## Architecture

Three layers:

1. **raw/** — Immutable source documents. Transcripts, articles, research. Never modify these.
2. **wiki/** — LLM-maintained knowledge pages. You own this entirely. Create, update, cross-reference, keep consistent.
3. **outputs/** — Generated reports, analyses, query results worth keeping.

## Directory Structure

```
raw/
  transcripts/    ← Video transcripts (one .md per video)
  articles/       ← Web-clipped research, competitor analysis
  assets/         ← Screenshots, thumbnails, reference images

wiki/
  index.md        ← Master catalog of all wiki pages
  concepts/       ← Topics Nick covers (XRP, gematria, NESARA, conspiracies, etc.)
  entities/       ← People, companies, coins, orgs Nick references
  patterns/       ← Recurring content patterns, structures, and formats that work
  hooks/          ← Proven hooks extracted from Nick's videos, tagged by type
  sources/        ← One summary page per ingested raw source
  hot.md          ← Hot cache: most recent/relevant context (under 500 words)

outputs/          ← Query results, analyses, comparisons worth keeping
log.md            ← Chronological operation history
```

## Wiki Page Format

Every wiki page uses this frontmatter:

```yaml
---
title: Page Title
type: concept | entity | pattern | hook | source | analysis
tags: [relevant, tags]
sources: [list of source pages that inform this page]
updated: YYYY-MM-DD
---
```

Use `[[wikilinks]]` for all cross-references between pages. This enables Obsidian's graph view and backlinks.

## Operations

### Ingest

When told to ingest a source from `raw/`:

1. Read the source document fully
2. Create a summary page in `wiki/sources/` with key takeaways
3. Extract and create/update pages for:
   - **Concepts**: Topics, themes, narratives (→ `wiki/concepts/`)
   - **Entities**: People, companies, coins, organizations (→ `wiki/entities/`)
   - **Patterns**: Content structures, formats, pacing approaches that work (→ `wiki/patterns/`)
   - **Hooks**: Opening lines/sequences, tagged by type (→ `wiki/hooks/`)
4. Update cross-references on all affected pages
5. Update `wiki/index.md`
6. Append entry to `log.md`
7. Update `wiki/hot.md` if this is recent/high-priority

A single source may touch 10-15 wiki pages. That's normal.

### Query

When asked a question:

1. Read `wiki/index.md` to find relevant pages
2. Read those pages
3. Synthesize an answer with `[[wikilink]]` citations
4. If the answer is valuable and reusable, offer to save it as a page in `outputs/`

### Lint

When asked to health-check:

1. Scan for contradictions between pages
2. Find orphan pages with no inbound links
3. Identify concepts mentioned but lacking their own page
4. Check for stale claims superseded by newer sources
5. Suggest new sources or research to fill gaps
6. Report findings and fix what you can

## Hook Tagging Schema

Every hook in `wiki/hooks/` should be tagged with:

- **hook_type**: curiosity-gap | bold-claim | pattern-interrupt | story | controversy | proof | authority | urgency
- **topic**: what the video is about
- **format**: long-form | short-form
- **strength**: strong | medium | weak (based on view performance if known)
- **text**: the actual hook verbatim

## Indexing

`wiki/index.md` is organized by category:

```markdown
## Sources
- [[source-name]] — one-line summary

## Concepts
- [[concept-name]] — one-line summary

## Entities
- [[entity-name]] — one-line summary

## Patterns
- [[pattern-name]] — one-line summary

## Hooks
- [[hook-name]] — hook type, topic
```

Update the index on every ingest. Keep entries under 120 characters.

## Logging

`log.md` uses this format:

```markdown
## [YYYY-MM-DD] operation | Subject
Details of what was done.
Pages created: [[page1]], [[page2]]
Pages updated: [[page3]], [[page4]]
```

## Rules

- Never modify files in `raw/` — they are immutable source of truth
- Always use `[[wikilinks]]` for cross-references
- Keep wiki pages focused — one concept/entity/pattern per page
- When in doubt about categorization, check the index for existing pages first to avoid duplicates
- Prefer updating an existing page over creating a new one when the topic overlaps
- Every claim should trace back to a source via `[[wikilinks]]`
