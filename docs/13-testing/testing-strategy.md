# Testing Strategy

**STATUS: REQUIRED** for implementation acceptance; no test suite exists yet.

Tests progress from deterministic domain unit tests, through mocked adapter contract tests and Windows integration tests, to isolated-VM system scenarios and hardware qualification. Every feature maps tests to requirement IDs, expected permissions, error states, compatibility matrix and recovery. Never validate destructive storage/account/service operations on an uncontrolled host. CI runs static analysis, dependency and secret checks, unit tests and reproducible builds. Security tests include malformed IPC and least-privilege denials; accessibility tests include keyboard/screen-reader checks. See the focused testing guides below.
