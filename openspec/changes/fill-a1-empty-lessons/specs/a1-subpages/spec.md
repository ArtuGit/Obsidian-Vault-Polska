# a1-subpages (delta)

## ADDED Requirements

### Requirement: A1 lesson pages follow a minimal learner template
For each A1 lesson page under `content/A1/`, the system SHALL include a minimal, consistent structure suitable for A1 learners.

#### Scenario: User opens any A1 lesson page
- **GIVEN** the user opens a lesson page under `content/A1/`
- **WHEN** the page renders
- **THEN** the first content line is an H1 subtitle in Ukrainian/Russian/English
- **AND** the page contains at least one translated section header in the format `## <PL> / <UA> / <EN>`
- **AND** the page includes a key terms block (Polish term + UA/RU/EN translations)
- **AND** the page includes examples (Polish + Ukrainian + English)
- **AND** the page links back to `[[Plan nauki A1]]` with accompanying UA/RU/EN explanation text

### Requirement: Obsidian callouts use valid syntax
For A1 lesson pages, the system SHALL use Obsidian callouts in proper blockquote form.

#### Scenario: Callouts render correctly in Obsidian/Quartz
- **GIVEN** an A1 lesson page contains a callout
- **WHEN** the callout is written
- **THEN** it uses the syntax `> [!NOTE]` (or other supported callout types)
- **AND** callout content lines are prefixed with `>`
