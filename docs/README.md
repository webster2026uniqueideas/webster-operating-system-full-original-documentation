# Webster Documentation

**STATUS: PROPOSED.** This is the navigation page for Webster's initial engineering specification. Nothing described here is represented as implemented.

## Start Here

- [Project overview](00-project/project-overview.md) | [Vision](00-project/vision.md) | [Scope](00-project/project-scope.md)
- [Master architecture](01-architecture/master-architecture.md) | [System layers](01-architecture/system-layers.md) | [Communication and IPC](01-architecture/communication-model.md)
- [Master specification](../specifications/WEBSTER-MASTER-SPECIFICATION.md) | [System requirements](../specifications/system-specification.md)

## Documentation Areas

| Area | Coverage |
|---|---|
| [00 Project](00-project/project-overview.md) | Definition, vision, mission, principles, terminology and scope |
| [01 Architecture](01-architecture/master-architecture.md) | Layers, components, process model, communication, IPC and dependencies |
| [02 Desktop](02-desktop/desktop-environment.md) | Shell, windows, taskbar, menus, notifications and interaction |
| [03 Computer Management](03-computer-management/computer-management.md) | System tools, storage, devices, services, users, performance and administration |
| [04 Native](04-native/native-architecture.md) | C++ design, Windows integration, services and standalone components |
| [05 Security](05-security/security-architecture.md) | Identity, authorization, privilege, isolation, secure IPC and threat model |
| [06 System](06-system/system-services.md) | Services, processes, memory, hardware, storage, filesystems and configuration |
| [07 Networking](07-networking/networking-architecture.md) | Connectivity, network configuration, firewall and diagnostics |
| [08 Users](08-users/user-management.md) | Accounts, sessions, profiles and groups |
| [09 Storage](09-storage/storage-architecture.md) | Drives, partitions, volumes, files and storage security |
| [10 Boot](10-boot/boot-architecture.md) | Windows-hosted startup, future boot research, recovery and shutdown |
| [11 Virtualization](11-virtualization/virtualization.md) | VMs, virtual hardware and hypervisor integration |
| [12 Development](12-development/development-guide.md) | Repository, code standards, build, debugging and contribution practices |
| [13 Testing](13-testing/testing-strategy.md) | Unit, integration, system, security and performance validation |
| [14 API](14-api/api-architecture.md) | System, native, IPC and extension contracts |
| [15 Installation](15-installation/system-requirements.md) | Requirements, installation, deployment, configuration and recovery |
| [16 Roadmap](16-roadmap/development-phases.md) | Planning phases, current state, milestones, limitations and future architecture |
| [17 Reference](17-reference/glossary.md) | Glossary and configuration, command and architecture references |

## Complete Index

| Area | Documents |
|---|---|
| Project | [Overview](00-project/project-overview.md), [Vision](00-project/vision.md), [Mission](00-project/mission.md), [Design principles](00-project/design-principles.md), [Terminology](00-project/terminology.md), [Scope](00-project/project-scope.md) |
| Architecture | [Master architecture](01-architecture/master-architecture.md), [System layers](01-architecture/system-layers.md), [Component model](01-architecture/component-model.md), [Process model](01-architecture/process-model.md), [Communication model](01-architecture/communication-model.md), [IPC](01-architecture/ipc.md), [Dependency architecture](01-architecture/dependency-architecture.md) |
| Desktop | [Environment](02-desktop/desktop-environment.md), [Shell](02-desktop/desktop-shell.md), [Window management](02-desktop/window-management.md), [Taskbar](02-desktop/taskbar.md), [Context menu](02-desktop/context-menu.md), [Notifications](02-desktop/notifications.md), [UI system](02-desktop/user-interface-system.md) |
| Computer Management | [Overview](03-computer-management/computer-management.md), [System tools](03-computer-management/system-tools.md), [Device management](03-computer-management/device-management.md), [Disk management](03-computer-management/disk-management.md), [Storage management](03-computer-management/storage-management.md), [Services](03-computer-management/services.md), [Event management](03-computer-management/event-management.md), [Users and groups](03-computer-management/users-and-groups.md), [Performance](03-computer-management/performance.md), [Administrative tools](03-computer-management/administrative-tools.md) |
| Native | [Architecture](04-native/native-architecture.md), [C++ architecture](04-native/cpp-architecture.md), [Components](04-native/native-components.md), [Windows API integration](04-native/windows-api-integration.md), [Native services](04-native/native-services.md), [Standalone components](04-native/standalone-native-components.md) |
| Security | [Architecture](05-security/security-architecture.md), [Authentication](05-security/authentication.md), [Authorization](05-security/authorization.md), [Privileges](05-security/privileges.md), [Permissions](05-security/permissions.md), [Process isolation](05-security/process-isolation.md), [Filesystem security](05-security/filesystem-security.md), [Network security](05-security/network-security.md), [Secure IPC](05-security/secure-ipc.md), [Auditing](05-security/auditing.md), [Threat model](05-security/threat-model.md) |
| System | [Services](06-system/system-services.md), [Process management](06-system/process-management.md), [Memory management](06-system/memory-management.md), [Hardware management](06-system/hardware-management.md), [Device management](06-system/device-management.md), [Storage system](06-system/storage-system.md), [Filesystem](06-system/filesystem.md), [Configuration](06-system/configuration-system.md) |
| Networking | [Architecture](07-networking/networking-architecture.md), [Management](07-networking/network-management.md), [Connectivity](07-networking/connectivity.md), [Firewall integration](07-networking/firewall-integration.md), [Diagnostics](07-networking/network-diagnostics.md) |
| Users | [Management](08-users/user-management.md), [Accounts](08-users/accounts.md), [Sessions](08-users/sessions.md), [Profiles](08-users/profiles.md), [Groups](08-users/groups.md) |
| Storage | [Architecture](09-storage/storage-architecture.md), [Drives](09-storage/drives.md), [Partitions](09-storage/partitions.md), [Volumes](09-storage/volumes.md), [Files](09-storage/files.md), [Storage security](09-storage/storage-security.md) |
| Boot | [Architecture](10-boot/boot-architecture.md), [Startup sequence](10-boot/startup-sequence.md), [System initialization](10-boot/system-initialization.md), [Recovery](10-boot/recovery.md), [Shutdown](10-boot/shutdown.md) |
| Virtualization | [Strategy](11-virtualization/virtualization.md), [Virtual machines](11-virtualization/virtual-machines.md), [Virtual hardware](11-virtualization/virtual-hardware.md), [Hypervisor integration](11-virtualization/hypervisor-integration.md) |
| Development | [Guide](12-development/development-guide.md), [Repository architecture](12-development/repository-architecture.md), [Coding standards](12-development/coding-standards.md), [C++ standards](12-development/cpp-standards.md), [Build system](12-development/build-system.md), [Debugging](12-development/debugging.md), [Contribution guide](12-development/contribution-guide.md) |
| Testing | [Strategy](13-testing/testing-strategy.md), [Unit testing](13-testing/unit-testing.md), [Integration testing](13-testing/integration-testing.md), [System testing](13-testing/system-testing.md), [Security testing](13-testing/security-testing.md), [Performance testing](13-testing/performance-testing.md) |
| APIs | [Architecture](14-api/api-architecture.md), [Native API](14-api/native-api.md), [System API](14-api/system-api.md), [IPC API](14-api/ipc-api.md), [Extension API](14-api/extension-api.md) |
| Installation | [Requirements](15-installation/system-requirements.md), [Installation](15-installation/installation.md), [Deployment](15-installation/deployment.md), [Configuration](15-installation/configuration.md), [Recovery](15-installation/recovery.md) |
| Roadmap | [Phases](16-roadmap/development-phases.md), [Current state](16-roadmap/current-state.md), [Milestones](16-roadmap/milestones.md), [Future architecture](16-roadmap/future-architecture.md), [Limitations](16-roadmap/known-limitations.md) |
| Reference | [Glossary](17-reference/glossary.md), [Configuration reference](17-reference/configuration-reference.md), [Command reference](17-reference/command-reference.md), [Architecture reference](17-reference/architecture-reference.md) |

## Engineering Specifications

- [Master specification](../specifications/WEBSTER-MASTER-SPECIFICATION.md)
- [System specification and requirements](../specifications/system-specification.md)
- [Desktop specification](../specifications/desktop-specification.md)
- [Computer Management specification](../specifications/computer-management-specification.md)
- [Security specification](../specifications/security-specification.md)
- [Native component specification](../specifications/native-component-specification.md)

## Status Language

Every document distinguishes **PROPOSED** design from **REQUIRED** constraints, **FUTURE** direction, **RESEARCH** questions, **DEPENDENCY** on Windows or another component, and **NOT YET IMPLEMENTED** status. Phase 1 is a Windows-integrated environment; it is not a Webster kernel or independent OS.