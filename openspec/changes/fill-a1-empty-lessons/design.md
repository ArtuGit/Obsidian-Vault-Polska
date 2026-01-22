# Design: Filling A1 lesson content

## Constraints (authoritative)
Follow `.ai-context/general.rule.md`.

Key points:
- Polish remains the system/Obsidian title (the file name).
- The first content H1 is a subtitle in **Ukrainian/Russian/English** (no Polish in that H1).
- Headers are translated into Ukrainian and English.
- Terms: Polish with Ukrainian/Russian/English translations.
- Examples: Polish with Ukrainian and English translations.
- Each internal link is accompanied by UA/RU/EN explanation text that is **not** part of the link.

## Minimal page template (A1)
Each `content/A1/<topic>.md` SHOULD follow this minimal structure:

1) Subtitle (H1)
- Format: `# <UA> — <RU> — <EN>`

2) Short intro paragraph
- Ukrainian as primary.

3) 3–6 sections with translated headers
- Header format: `## <PL> / <UA> / <EN>`

4) Key terms block
- Format: `**<PL-term>** — <UA> / <RU> / <EN>`

5) Examples block
- Format: `- <PL>. — <UA>. — <EN>.`

6) At least one Obsidian callout
- IMPORTANT: use correct callout syntax:
  - `> [!NOTE]`
  - `> [!TIP]`
  - `> [!IMPORTANT]`
  - `> [!WARNING]`
  - `> [!CAUTION]`

7) Cross-links
- Always include:
  - `[[Plan nauki A1]] — план A1 / план A1 / A1 plan`

## Validation strategy
Implement a simple local/CI check (per `a1-subpages` spec):
- Fail if any `content/A1/*.md` is empty.
- Optional (recommended) structure checks:
  - First non-empty line is `# ...`.
  - At least one section header `## ... / ... / ...` exists.
  - At least 3 example lines containing two `—` separators.
