# Learning Plan Rule (Topic Index Only)

This rule is for AI agents generating learning “plans” like **A2 learning plan**.
In this vault, a learning plan means a **topic index** (a curated list of topics + links), not a study schedule.

## Hard Requirements

### 1) Output must be a topic index (not a schedule)
- Do **not** include timelines, week-by-week structure, durations, frequency, spaced repetition, “how to learn” advice, or recommendations.
- Do **not** include general learning tips, motivation, resources, apps, or methodologies.
- You may include a single short note explaining that the page is only an index of topics.

### 2) Topics must be specific and concrete
- Use explicit topic titles such as: Numbers 0–1000, Ordinal numbers, Months & seasons, Dates, Time & clock, Cases: Genitive, Verbs: Past tense, Imperative, Aspect (perfective/imperfective), Motion verbs, etc.
- Avoid vague buckets like “Grammar”, “Vocabulary”, “Speaking practice”. If a category exists, it must contain specific topic links.

### 3) Every topic must link to an EMPTY page
- Each topic item must link to a dedicated page that is **fully empty** (no frontmatter, no title, no headings, no text).
- Pages are placeholders; content will be written later.
- If a linked page already exists and has content, do not modify it; still link to it.

## File + Linking Conventions

### Target note for the plan
- Create (or update) the plan note at: `content/Plan nauki <LEVEL>.md`
	- Example: `content/Plan nauki A2.md`

### Topic pages location
- Topic pages must live under: `content/<LEVEL>/`
	- Example: `content/A2/`

### Link format
- Use Obsidian wiki-links that match the file path from `content/` without the `.md` extension:
	- `[[A2/Numbers 0-1000]]` links to `content/A2/Numbers 0-1000.md`

### Page creation rule (placeholders)
- For each topic link that does not yet exist, create the file **as empty**:
	- Correct: empty file (0 bytes or a single newline)
	- Incorrect: any content at all (frontmatter, `# Title`, notes, TODOs, etc.)

## Required Markdown Structure (match existing A1 index style)

### Title
- Start with a single H1 title in the same style as A1:
	- `# План тем <LEVEL> / План тем <LEVEL> / <LEVEL> Topic Index`

### Optional note block (allowed)
- If included, use exactly one short note block:
	- `[!NOTE]` with 1–2 sentences
	- It must NOT contain learning advice; only describe that this is a list of topics.

### Sections
- Group topics into clear sections similar to A1, using trilingual headings:
	- `## <Polish> / <Ukrainian> / <English>`
- Each section contains bullet points.

### Topic bullets
- Each bullet must follow this pattern:
	- `- [[<LEVEL>/<Topic Page Name>]] — <UA description> / <RU description> / <EN description>`
- The link text is Polish (as in the file name). Descriptions are short.
- Do not add extra nested lists or paragraphs.

## Content Restrictions Checklist
- No schedules, no calendars, no “study X minutes”, no “do exercises”.
- No generic “how to learn Polish” guidance.
- No prose explanations of grammar rules.
- Only headings + topic bullets (+ optional single NOTE).

## Alignment with General Vault Rules
- Follow language conventions from `general.rule.md`:
	- Polish in link/file names.
	- Ukrainian/Russian/English descriptions next to each link.
	- Do not duplicate system title with an extra H1 elsewhere (use a single H1 only).