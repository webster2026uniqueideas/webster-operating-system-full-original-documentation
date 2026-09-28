# Windows API Integration

**STATUS: PROPOSED.** Webster integrates using supported documented APIs and reports Windows as capability provider.

| Capability | Candidate interface | Ownership / caveat |
|---|---|---|
| Process/thread | Win32 process and performance APIs, Tool Help/PSAPI as appropriate | Windows schedules and enforces process security; protected data may be inaccessible. |
| Services | Service Control Manager APIs | Windows owns lifecycle, account and dependency behavior. |
| Management inventory | WMI/CIM where appropriate | Optional, permissions/provider/latency vary; avoid as sole source. |
| Security | Windows access tokens, ACLs, UAC/elevation, DPAPI/CNG as suitable | Windows identity and access checks remain authoritative in Phase 1. |
| Devices | SetupAPI/Configuration Manager/device property APIs | Windows PnP and drivers own enumeration and driver state. |
| Storage | Volume management, file, storage and supported management APIs | Windows owns filesystem, mount and I/O stack; destructive operations need revalidation. |
| Networking | IP Helper, Winsock, Network List Manager and documented policy APIs | Windows owns TCP/IP and interface configuration. |
| Firewall | Windows Firewall with Advanced Security management APIs | Respect policy/domain management; do not disable protections. |
| Events | Windows Event Log APIs | Access is permission-scoped; preserve source and timestamps. |
| Configuration | Registry APIs only for documented settings; supported settings APIs preferred | No undocumented keys, secret storage in plaintext, or registry-as-database. |
| Power/system info | documented power, system information and notification interfaces | Handle sleep/resume and unsupported capability. |

At startup, detect supported OS/API capabilities rather than relying on marketing version strings. Isolate API-version differences in adapters, check every return code and resource lifetime, and test least-privileged behavior. Availability and exact API selections remain a **DEPENDENCY** to validate against the final Windows support matrix.
