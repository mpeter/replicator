## ADDED Requirements

### Requirement: Single requirements authority
The repository MUST use OpenSpec as its only active requirements pipeline.
Repository workflow guidance MUST reference `openspec/constitution.md`,
canonical requirements under `openspec/specs/`, and active change artifacts
under `openspec/changes/`.

#### Scenario: Beginning a change
- **GIVEN** a contributor is planning non-trivial work
- **WHEN** they follow repository workflow guidance
- **THEN** they use an OpenSpec change and an `opsx/<name>` branch
- **AND** no second requirements pipeline is offered

### Requirement: Historical preservation
Completed strategic histories MUST live under dated directories in
`openspec/changes/archive/`. Migration MUST preserve their requirements and
task states, append implementation evidence, and use neutral terminology.

#### Scenario: Reading migrated history
- **GIVEN** a previously completed strategic specification
- **WHEN** its archive is read after migration
- **THEN** its requirements and recorded task completion states remain available
- **AND** appended evidence identifies the implementation commit

### Requirement: Retired infrastructure removal
The repository MUST remove the retired workflow infrastructure and its
references from tracked content and filenames without rewriting Git history.

#### Scenario: Inspecting the repository
- **GIVEN** the retirement is complete
- **WHEN** tracked files and their names are inspected
- **THEN** only OpenSpec requirements infrastructure remains
- **AND** unrelated embedded deployment assets are unchanged
