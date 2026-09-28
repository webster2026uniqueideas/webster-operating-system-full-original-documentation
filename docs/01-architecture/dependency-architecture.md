# Dependency Architecture

**STATUS: PROPOSED.** External dependencies are explicit and replaceable at adapter boundaries where practical.

## Direction

UI -> Webster domain contracts -> platform abstraction -> Windows adapter -> documented Windows API. Privileged calls additionally traverse an authenticated broker. Domain logic must not depend on UI frameworks or global mutable platform state.

## Dependency Register (Initial)

| Dependency | Purpose | Constraint / validation |
|---|---|---|
| Supported Windows versions and editions | Host OS and APIs | Establish support matrix; test policy, privilege and API availability. |
| MSVC and Windows SDK | Native build and headers/toolchain | Pin supported versions; CI must reproduce builds. |
| Windows security/SCM/WMI/storage/network APIs | System integration | Use least-privilege APIs; classify optional features and errors. |
| UI framework (selection pending) | Desktop rendering/accessibility | **RESEARCH:** select based on Windows integration, accessibility, licensing and deployment. |
| Test framework (selection pending) | Native tests | Select after repository implementation begins; support deterministic unit and integration tests. |

Record each dependency's version, license, update policy, attack surface, fallback and owner before use. Avoid undocumented APIs, bundled drivers and dependencies that require unnecessary elevation.
