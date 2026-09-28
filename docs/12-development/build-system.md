# Build System

**STATUS: PROPOSED.** CMake with Visual Studio/MSVC integration is a candidate, not an existing project setup.

Pin compiler, Windows SDK, CMake and dependency versions. Provide reproducible Debug/Release configurations, explicit architecture targets, generated version metadata, code signing only in controlled release pipeline, and deterministic packaging where feasible. CI should build from clean checkout, run unit/static analysis/security checks, produce test artifacts and verify package signatures. Never commit secrets or private signing keys. Build configuration must state minimum Windows/API targets and fail clearly when prerequisites are missing.
