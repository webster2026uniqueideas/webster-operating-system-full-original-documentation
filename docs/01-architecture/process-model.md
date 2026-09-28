# Process Model

**STATUS: PROPOSED.** Webster process operations in the Windows-integrated phases are requests to Windows, not a Webster scheduler.

Webster UI, helpers and services run as Windows processes with Windows tokens, jobs, handles, threads and isolation. A process-management view may query supported process APIs and display best-effort metrics with timestamps and access-denied states. Creation, termination, priority changes and inspection are mediated by Windows and must be authorized; protected processes and other users' processes may be inaccessible.

Webster must not inject into unrelated processes, duplicate handles without need, weaken mitigations, or promise hard resource limits unless Windows provides and confirms them. Use cancellation, timeouts, bounded worker pools and RAII handle wrappers. Future independent-OS scheduling is **FUTURE / RESEARCH** only.

See [process management](../06-system/process-management.md), [process isolation](../05-security/process-isolation.md), and [system specification](../../specifications/system-specification.md).
