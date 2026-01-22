# Change: Fill empty A1 lesson pages

## Why
The A1 learning plan links to 49 lesson pages under `content/A1/`, but 46 of those pages are currently empty (0 bytes). This breaks the learning flow (blank pages) and violates the existing `a1-subpages` specification.

## What Changes
- Populate every empty `content/A1/*.md` lesson with learner-usable A1 content.
- Ensure each populated lesson follows `.ai-context/general.rule.md` (languages, headings, translations, links, callouts).
- Keep scope strictly to A1 lesson pages: no re-organization of the vault and no new topics.

## Out of Scope
- Expanding beyond A1 depth (A2+ material).
- Rewriting the A1 plan (`content/Plan nauki A1.md`) unless a broken link is discovered.
- Large Quartz/site architecture work.

## Impact
- Affected spec: `openspec/specs/a1-subpages/spec.md` (implementation of existing requirements; no spec change intended).
- Affected content: `content/A1/*.md` (46 currently-empty pages).

## Acceptance Criteria
- Every `content/A1/*.md` file is non-empty.
- Each A1 lesson page:
  - Starts with a subtitle H1 in Ukrainian/Russian/English (does not repeat the Polish system title).
  - Uses translated section headers (`## <PL> / <UA> / <EN>`).
  - Introduces key terms as: Polish + Ukrainian/Russian/English.
  - Includes examples as: Polish + Ukrainian + English.
  - Uses at least one proper Obsidian callout.
  - Includes a link back to `[[Plan nauki A1]]` with accompanying UA/RU/EN explanation text.
- A validation command exists and fails on empty A1 files (per spec).
