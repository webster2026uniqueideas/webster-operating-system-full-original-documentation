# Development Phases

**STATUS: PROPOSED PLANNING GUIDANCE.** No phase is complete or underway based on this documentation alone.

| Phase | Goal | Exit evidence |
|---|---|---|
| 0 — Architecture | Approve scope, requirements, threat model, support matrix and decisions | Reviewed specs, feasibility spikes and acceptance criteria |
| 1 — Native foundation | Build C++ core, Windows adapters, packaging and CI | Reproducible builds, unit/adapter tests, least-privilege proof |
| 2 — Webster Desktop | Implement shell, taskbar, windows, menus and accessibility | End-to-end usability/accessibility on target Windows matrix |
| 3 — System management | Deliver Computer Management inventory and safe operations | Authorized workflows, error/recovery tests, audit evidence |
| 4 — Security | Harden identity, IPC, signing, auditing and update path | Threat review and security test gate |
| 5 — System services | Expand process/storage/network/device/service management | Capability-specific support and reliability acceptance |
| 6 — Developer platform | Version stable APIs/SDK and optionally extensions | Compatibility policy and conformance suite |
| 7 — Advanced native architecture | Evaluate deeper isolated services/platform integration | Documented benefit, permissions and maintenance cost |
| 8 — Independent OS research | Decide whether boot/kernel/HAL research is warranted | Separate approved charter, prototype and risk/funding plan |

Sequence and scope can change; exit evidence, not calendar dates, determines readiness. Phase 8 is optional and does not follow automatically from the earlier phases.
