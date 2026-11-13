## Approach

Preserve each strategic history under a dated OpenSpec archive. Existing
task checkboxes are historical evidence, not a request to re-certify work.
Append the corresponding implementation commit without advancing task state.
Neutral wording replaces retired tooling references; Git history is untouched.

OpenSpec becomes the only active workflow. Keep all unrelated review gates,
concurrency limits, and runtime configuration unchanged.

## Product boundary

`internal/agentkit/content` is the embedded deployment source, walked by
`agentkit.Scaffold`. It contains no retired workflow files or references.
The repository's `.opencode/` guidance is not embedded or shipped by init.
Consequently a separate product-removal change, stale-file policy change,
and product changelog entry do not apply. Scaffold behavior remains unchanged.

## Validation

Run CI's vet, race-enabled tests, and binary build at final committed HEAD.
Validate all OpenSpec artifacts and search tracked contents and filenames
for retired tooling identifiers. Preserve all existing scenarios while
correcting the six flat delta-spec paths required by the installed validator.
