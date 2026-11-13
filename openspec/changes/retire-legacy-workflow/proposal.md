# OpenSpec as the sole requirements authority

## Why

Parallel requirements trees give reviewers conflicting sources of truth.
Keep one active workflow while preserving historical requirements and tasks.

## What Changes

- Archive three completed strategic histories with implementation evidence.
- Retire the previous workflow's scripts, templates, commands, and skill.
- Move the constitution to `openspec/constitution.md` and route repository
  agents, commands, and contributor guidance to OpenSpec only.
- Correct existing delta specification layout without changing requirements.

## Capabilities

### New Capabilities
- `repository-workflow`: one requirements authority and preserved history.

## Impact

Repository development guidance changes; the embedded agent kit has no
retired workflow assets or references and remains byte-for-byte unchanged.
No user file is removed and no product version changes.

## Constitution Alignment

- I. Autonomous Collaboration: PASS — requirements remain file artifacts.
- II. Composability First: PASS — runtime and shipped assets are unchanged.
- III. Observable Quality: PASS — validation and CI checks verify the result.
- IV. Testability: PASS — no runtime behavior or isolation contracts change.

The operator explicitly requires local commits only, overriding publication
and PR steps for this task. No review or merge approval is claimed.
