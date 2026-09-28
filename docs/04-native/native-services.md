# Native Services

**STATUS: PROPOSED.** A Webster Windows service is an optional Phase 2 deployment choice, not a default requirement.

A service must have a documented purpose unavailable to a user-mode client, least-privileged service identity, minimal ACL-protected IPC, explicit service dependencies, bounded startup/shutdown, SCM recovery policy, health reporting, update/rollback strategy and audit coverage. Prefer per-user standard processes for desktop behavior and read-only information. Never run the entire shell or management UI as LocalSystem. Avoid shared writable executable/configuration paths and unsafe service DLL search behavior.

Installation/removal requires signed packages and supported Windows service configuration. Operational failures must leave Windows services and host security settings intact. Service API/version changes follow the [IPC contract](../01-architecture/ipc.md).
