# Capability: A1 lesson subpages

## ADDED Requirements

### Requirement: A1 plan links open meaningful lesson pages
The system SHALL ensure that each A1 lesson linked from the A1 learning plan provides non-empty, learner-usable content.

#### Scenario: User opens a lesson from the plan
- **GIVEN** the user is reading `content/Plan nauki A1.md`
- **WHEN** the user opens any `[[A1/<topic>]]` link
- **THEN** the destination page is not empty
- **AND** the page contains a clear structure suitable for A1 learners

### Requirement: A1 pages follow the project’s language and formatting rules
For each A1 lesson page under `content/A1/`, the system SHALL structure content according to `.ai-context/general.rule.md`.

#### Scenario: Subtitle does not duplicate the system title
- **GIVEN** an A1 page’s system title is the Polish file name
- **WHEN** the page content begins
- **THEN** the first content H1 is a subtitle in Ukrainian/Russian/English
- **AND** it does not repeat the Polish system title

#### Scenario: Section headers are translated
- **GIVEN** an A1 page has multiple sections
- **WHEN** section headers are rendered
- **THEN** each section header includes Ukrainian and English translations

#### Scenario: Terms and examples include translations
- **GIVEN** an A1 page introduces vocabulary or grammar
- **WHEN** key terms are presented
- **THEN** each key term is shown in Polish with Ukrainian/Russian/English translations
- **AND** examples are Polish sentences with Ukrainian and English translations

#### Scenario: Internal links are annotated
- **GIVEN** an A1 page contains internal Obsidian links
- **WHEN** those links appear in the content
- **THEN** each internal link is accompanied by Ukrainian/Russian/English explanation text that is not part of the link

### Requirement: Automated validation prevents empty A1 pages
The system SHALL provide an automated check that fails if A1 lesson pages are empty.

#### Scenario: CI/local check catches an empty A1 file
- **GIVEN** a `content/A1/*.md` file is empty
- **WHEN** the validation script runs
- **THEN** the command fails with a clear error listing the offending file(s)
