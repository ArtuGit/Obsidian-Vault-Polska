# Design: A1 lesson subpages

## Constraints (content rules)
These pages MUST follow `.ai-context/general.rule.md`:
- System/Obsidian title stays Polish (file name / Quartz title).
- The first content H1 is a *subtitle* in **Ukrainian/Russian/English** (no Polish there), to avoid duplicating the system title.
- Each grammar term is provided as: Polish + Ukrainian/Russian/English translations.
- Examples are: Polish with Ukrainian + English translations.
- Headers should be translated into Ukrainian and English.
- Each internal link is accompanied by Ukrainian/Russian/English translation text (not part of the link).
- Use Obsidian callouts like `[!NOTE]`, `[!TIP]`, `[!IMPORTANT]`, `[!WARNING]`, `[!CAUTION]` where appropriate.

## Minimal page template
Each `content/A1/<topic>.md` page should follow this minimal structure.

1) Subtitle (H1)

- Format: `# <UA> — <RU> — <EN>`
- Example for `Alfabet i wymowa.md`:
  - `# Алфавіт і вимова — алфавит и произношение — alphabet & pronunciation`

2) Short intro paragraph (Ukrainian as primary, optionally a short English sentence if helpful)

3) Sections with translated headers

- Header format: `## <PL> / <UA> / <EN>`
- Keep the number of sections small (3–6) to stay “A1 minimal”.

4) Key terms block

- Use a compact list, e.g.
  - `**wymowa** — вимова / произношение / pronunciation`

5) Examples block

- Use a consistent line pattern, e.g.
  - `- To jest A. — Це A. — This is A.`

6) At least one callout

- E.g. a warning about common mistakes, or a tip for memorization.

7) Cross-links

- Link back to the plan:
  - `[[Plan nauki A1]] — план A1 / план A1 / A1 plan`

## Validation strategy
To keep quality high and prevent regressions:
- Add an automated check that fails if any `content/A1/*.md` file is empty.
- Optionally enforce basic structure:
  - first non-empty line is an H1
  - at least one “examples” section exists
  - at least N example lines containing two `—` separators

The check should be runnable locally and in CI (via an npm script).
