# Webster Operating System

**Webster is a proposed Windows-integrated operating-system environment and systems platform.** Its initial engineering direction is a native Windows application suite with a coherent desktop, Computer Management environment, and carefully bounded native C++ components. It is not currently an independent operating system.

> **CURRENT STATE: NOT YET IMPLEMENTED IN THIS REPOSITORY.** This repository contains the initial engineering documentation and target specifications only. No Webster desktop, kernel, bootloader, system service, native component, or management tool is claimed to exist.

## Vision

Build a dependable, understandable computing environment that brings a consistent Webster experience to Windows first, establishes explicit service and security boundaries, and leaves room for deeper native system work only when supported by a deliberate engineering decision.

## Architecture

The **proposed target architecture** layers Webster applications and desktop experiences over Webster system services and a native C++ integration layer, which in turn uses supported Windows platform services. Windows remains responsible for the kernel, scheduling, virtual memory, drivers, hardware abstraction, filesystems, accounts and core networking during Phase 1. Hardware and firmware are reached through Windows, not directly by Webster.

## Major Components

- **Desktop:** proposed shell, window/taskbar experience, launch surface, menus, notifications and accessibility behavior.
- **Computer Management:** proposed console for system information, processes, events, devices, storage, services, accounts, performance and diagnostics.
- **Native C++:** proposed separately testable integration libraries and, where privilege boundaries require it, standalone processes.
- **Security:** identity-aware authorization, least privilege, authenticated IPC, auditing, secure updates and threat-driven design.
- **System services:** Webster-owned orchestration and presentation over Windows-owned operating-system capabilities.

## Development Roadmap

The roadmap progresses from requirements and architecture through a Windows-native foundation, desktop, management tools, security, services, developer APIs and advanced native research. An independent bootable OS is an optional future research direction, not a Phase 1 commitment.

## Documentation Index

Start at [docs/README.md](docs/README.md). The central documents are the [master specification](specifications/WEBSTER-MASTER-SPECIFICATION.md), [master architecture](docs/01-architecture/master-architecture.md), [requirements](specifications/system-specification.md), [desktop specification](specifications/desktop-specification.md), [Computer Management specification](specifications/computer-management-specification.md), [security specification](specifications/security-specification.md), and [native component specification](specifications/native-component-specification.md).

The `docs/` tree organizes project, architecture, desktop, administration, native engineering, security, system services, networking, users, storage, boot, virtualization, development, testing, APIs, installation, roadmap and reference material. `architecture/` is reserved for diagram and decision records.

## Status

**STATUS: PROPOSED.** The architecture, interfaces, requirements and roadmap in this repository are plans. They must be reviewed, validated and revised as implementation decisions are made. The existing repository license is GPL-3.0; future component and dependency licensing requires review before distribution.
