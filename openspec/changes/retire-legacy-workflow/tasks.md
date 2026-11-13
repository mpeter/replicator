## 1. Workflow retirement
- [x] 1.1 Archive strategic histories and append implementation evidence without advancing task states.
- [x] 1.2 Retire the previous workflow infrastructure and update constitution and repository guidance.
- [x] 1.3 Correct existing delta-spec layout while preserving requirements and scenarios.

## 2. Verification
- [x] 2.1 Verify constitution alignment and unchanged embedded deployment assets.
- [ ] 2.2 Run full CI-equivalent gates and OpenSpec validation at final committed HEAD; confirm zero retired-name matches.

CI vet, race tests, build, and OpenSpec validation passed during implementation.
Final-HEAD checks remain required. Additional environment checks are blocked:
`govulncheck` reports GO-2026-6859 in Go 1.27.3 (fixed in 1.27.4);
the installed linter was built with Go 1.25.10 and panics on newer Go sources.
No toolchain, dependency, or gate change is authorized by this retirement.
