# Project Scope

**STATUS: PROPOSED.** This scope describes intended boundaries, not delivered functionality.

## Phase 1 In Scope

- Windows-hosted Webster desktop and applications.
- User-mode C++ libraries and optional separate processes.
- System inspection and management through supported APIs and Windows authorization.
- Documented APIs, secure IPC, packaging, update and test strategy.

## Phase 1 Out of Scope

- Replacing the Windows kernel, boot manager, shell, scheduler, filesystem, drivers, authentication authority or TCP/IP stack.
- Direct hardware control bypassing Windows or undocumented kernel interfaces.
- Claiming universal support for all Windows editions/devices.

## Phase 2

Potential decomposition into independently managed Webster processes/services while retaining Windows as host and resource authority. Each privileged service requires threat analysis and a narrowly scoped contract.

## Future / Research

A Webster bootloader, kernel, HAL, driver framework, filesystem, independent account/security model and installer are research topics only. They require approval, architecture, prototype evidence and separate requirements.

The [master architecture](../01-architecture/master-architecture.md) and [roadmap](../16-roadmap/development-phases.md) define these boundaries in detail.
