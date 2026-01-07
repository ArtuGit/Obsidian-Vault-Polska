# Change: Add A1 subpages for learning plan

## Why
The A1 learning plan ([content/Plan nauki A1.md](../../content/Plan%20nauki%20A1.md)) links to many lesson pages under `content/A1/`, but those pages are currently empty. This creates a broken learning flow (blank pages) and a low-quality published Quartz site output.

## What Changes
- Add a consistent, minimal structure for A1 lesson pages that follows the project’s content rules (see `.ai-context/general.rule.md`).
- Populate every A1 page referenced by the learning plan with starter content (non-empty) that includes:
  - a translated subtitle (H1) in Ukrainian/Russian/English (without duplicating the Polish system title)
  - translated section headers (Ukrainian + English)
  - key Polish terms with Ukrainian/Russian/English translations
  - Polish examples with Ukrainian + English translations
  - at least one Obsidian callout block (e.g., `[!NOTE]`, `[!TIP]`, …)
- Add an automated repo check to prevent future regressions (e.g., empty A1 pages or missing required structure).

## Impact
- Affected content: `content/A1/*.md` and potentially `content/Plan nauki A1.md` (only if we need to fix/standardize links).
- Affected tooling: a small validation script and/or CI wiring so `npm test`/`npm run check` can catch empty pages.
- Quartz output: improved HTML generation for A1 pages (no blank pages).

## Non-goals
- Adding new UI, navigation concepts, or Quartz theme changes.
- Creating new lesson topics beyond the ones already listed in the A1 plan.
