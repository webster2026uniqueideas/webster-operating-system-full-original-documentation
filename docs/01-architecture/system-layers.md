# System Layers

**STATUS: PROPOSED.** The table describes Phase 1 ownership and future boundaries.

| Layer | Examples | Owner / trust boundary |
|---|---|---|
| Experience | Desktop shell, Webster apps | Webster user-mode code; untrusted input and plugins remain isolated. |
| Application/domain | Launch, settings, system-management workflows | Webster; no direct assumption of administrator rights. |
| Service/API | Read-only inventory, job orchestration, notification/event adapters | Webster user-mode process or narrowly privileged broker as justified. |
| Native adapter | C++ wrappers for Windows APIs, serialization, validation | Webster; adapter is not a kernel or HAL. |
| Platform | Win32, SCM, WMI, Windows security, storage, networking, event APIs | Windows-provided, policy and permission constrained. |
| Kernel/device | Scheduler, VM, object manager, drivers, PnP | Windows-owned in Phases 1 and 2. |
| Hardware/firmware | CPUs, disks, NICs, firmware | Reached through Windows. |

A request flows downward through the smallest required interface. Results flow back with provenance, freshness and errors. UI must not call privileged APIs merely because its process happens to be elevated. The [master architecture](master-architecture.md) is canonical.
