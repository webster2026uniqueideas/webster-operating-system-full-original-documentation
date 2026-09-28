# Development Guide

**STATUS: PROPOSED.** This guide establishes future contributor practices; there is no source build yet.

Before coding, agree on supported Windows versions, toolchain, UI framework, dependency policy, component boundaries and installer/signing plan. Keep domain logic testable off the UI thread. Every privileged operation needs requirement IDs, API contract, threat analysis and tests. Changes update docs, error behavior, compatibility notes and test evidence. No real administrative actions should run against a developer's daily machine without an isolated test plan.

Build and CI setup are proposed in [build system](build-system.md); standards are in [coding](coding-standards.md) and [C++](cpp-standards.md).
