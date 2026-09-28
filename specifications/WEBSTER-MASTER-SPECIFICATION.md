# WEBSTER Master Specification

**STATUS: PROPOSED.** This document is the central engineering blueprint. It describes intended architecture and behavior, not shipped software. **Webster implementation status: NOT YET IMPLEMENTED IN THIS REPOSITORY.**

## 1. Project Definition

Webster is a proposed operating-system environment/platform. Phase 1 is a Windows-integrated desktop and system-management product; the current repository has no implementation. The phrase “operating system” describes the project ambition and coherent user environment, not a claim that Webster currently owns a kernel or boot process.

## 2. Vision

Provide an understandable, secure and consistent computing experience, starting on Windows, with clear ownership, observable system state and safer administration. See [vision](../docs/00-project/vision.md).

## 3. Scope

Phase 1 includes Webster user-mode applications, a desktop, native C++ integration, Computer Management, APIs, packaging and security controls. Phase 2 may isolate additional Webster services while Windows remains host authority. Kernel, bootloader, HAL/drivers, scheduler, filesystem and independent account/security stack are **FUTURE / RESEARCH**, requiring explicit approval.

## 4. Architecture

**Proposed target:** Webster applications -> Webster desktop -> Webster system services -> Webster native C++ adapters -> Windows/platform services -> hardware/firmware. Windows provides the Phase 1 kernel, scheduler, virtual memory, drivers, PnP, filesystems, identity/token/access checks, TCP/IP and window compositor. Webster owns its code, UI, policy and contracts. Hardware is accessed through Windows. See [master architecture](../docs/01-architecture/master-architecture.md).

## 5. Desktop

The proposed shell provides launch/navigation, taskbar, windows, system status, notifications, context menus and settings. It runs in the Windows user session and uses host window/input/accessibility facilities. Keyboard, screen-reader, scaling, high contrast and reduced motion are required. Context actions are target-aware, permission-checked and report actual outcomes. See [desktop specification](desktop-specification.md).

## 6. Computer Management

WCM unifies system inventory and authorized management of processes, events, devices, disks/volumes, services, users/groups, performance and diagnostics. Read-only observation is separate from mutation. High-risk changes preview target/impact, revalidate current state, use Windows APIs, require appropriate authorization/confirmation and verify result. See [Computer Management specification](computer-management-specification.md).

## 7. Native Architecture

Target C++20/MSVC/Windows SDK, subject to supported-version validation. Use RAII, smart ownership, bounded concurrency, explicit errors, safe handle wrappers and platform adapters. Exceptions do not cross ABI/IPC boundaries. CMake is a candidate build system. Native core is user mode, not a kernel. See [native specification](native-component-specification.md).

## 8. Security

Security is a design constraint. Standard-user execution is default; Windows identity and enforcement remain authoritative. Separate UI from narrowly privileged brokers; authenticate and authorize IPC operations; validate inputs; protect configuration/data; audit sensitive changes; sign updates; threat-model each privileged feature. See [security specification](security-specification.md).

## 9. Users

Windows performs logon, authentication and token creation. Webster session state and preferences are application-scoped. Webster must not store Windows passwords or override Windows/domain policy. Future independent identity is research only.

## 10. Processes

Windows creates/schedules/isolate processes and threads. Webster reports available metrics and submits supported authorized requests; it does not provide a Phase 1 scheduler or arbitrary process memory access.

## 11. Storage

Windows owns block I/O, volume manager, mounted filesystems, ACLs and encryption services. Webster models devices, partitions, volumes, paths and files distinctly, reports provenance/freshness, and delegates changes to supported Windows APIs with elevated safeguards.

## 12. Networking

Windows owns NIC drivers, TCP/IP, Winsock, DHCP/DNS and firewall enforcement. Webster offers status/configuration/diagnostics through supported interfaces, respects managed policy and avoids unsolicited listeners or hidden telemetry.

## 13. Devices

Windows PnP, drivers, device power and HAL own hardware access. Webster enumerates and manages only through documented APIs. No arbitrary driver loading or direct hardware access in Phase 1.

## 14. Services

SCM owns Windows service lifecycle. Webster service deployment is optional and requires least-privileged identity, narrow ACL-protected IPC, health/recovery policy and justified need. Do not run the desktop as LocalSystem.

## 15. APIs

Future System, Native, Desktop, Storage, Process, Network, Security, Device, IPC and Extension APIs are versioned and typed. No generic arbitrary command API. IPC identities come from Windows transport, not request data. Extension API is optional and untrusted by default. See [API architecture](../docs/14-api/api-architecture.md).

## 16. Boot Architecture

Current target: firmware -> Windows Boot Manager -> Windows kernel/session -> optional Webster startup. Webster failure must not prevent Windows boot/logon. Future independent flow (firmware -> Webster bootloader -> kernel -> services -> system manager -> desktop -> session) is **FUTURE / RESEARCH**, not implemented or yet specified in production detail.

## 17. Virtualization

Use supported hypervisors/VMs for isolated development and destructive tests. Hypervisor integration is unselected research. Virtual hardware coverage does not prove physical device or firmware support.

## 18. Development

Separate apps, contracts, domain core, platform adapters, optional broker, tests and packaging. Pin toolchain/SDK/dependencies, build reproducibly, review licensing and keep secrets out of source. See [development guide](../docs/12-development/development-guide.md).

## 19. Testing

Map every requirement to unit, adapter, integration, system, accessibility, security and performance tests as applicable. Use clean Windows environments and disposable VMs for dangerous operations. Test standard-user denial, policy/API absence, cancellation, partial data and recovery. No destructive host tests without a controlled plan.

## 20. Deployment

A future signed package must use restrictive ACLs, explicit installation scope, consent-based optional services/startup, authenticated updates, rollback and clean uninstall. Installer, release channels, key custody and Windows support matrix remain decisions.

## 21. Roadmap

Phase 0 architecture; 1 native foundation; 2 desktop; 3 management; 4 security; 5 system services; 6 developer platform; 7 advanced native architecture; 8 optional independent OS research. Phases are planning guidance; none is claimed complete. See [roadmap](../docs/16-roadmap/development-phases.md).

## 22. Requirements

Normative requirements are cataloged in [system specification](system-specification.md) and feature specifications. Identifiers are unique and acceptance must be testable. Core themes: truthful ownership, least privilege, accessibility, compatibility, reliability, performance measurement and traceable development.

## 23. Risks

- Undefined target Windows support matrix or UI/installer/IPC choices.
- API availability and permissions vary by version, edition, policy and device.
- Privileged broker can become a confused deputy or escalation path.
- Management operations can damage data or interrupt host services.
- Signing/update/dependency supply chain may compromise trust.
- Native C++ memory, handle and concurrency defects.
- “OS” terminology can lead to false kernel/boot expectations.
- Long-term independent kernel/driver maintenance may exceed project capacity.

Mitigate through explicit scope, staged read-only-first delivery, threat modeling, supported APIs, isolated tests, signed releases and evidence-based phase gates.

## 24. Future Architecture

A separate decision may investigate a bootable Webster OS, kernel, scheduler, memory manager, security authority, HAL/drivers, storage/filesystem, network stack and recovery/installer. Each would need its own requirements, threat model, compatibility plan, prototype and approval. No Phase 1 component is evidence these future components exist.

## Status Vocabulary

**PROPOSED** design; **REQUIRED** acceptance constraint; **FUTURE** possible later direction; **RESEARCH** unresolved feasibility; **DEPENDENCY** externally owned capability; **NOT YET IMPLEMENTED** absent from this repository. Windows-owned functionality is not Webster-owned merely because Webster presents it.
