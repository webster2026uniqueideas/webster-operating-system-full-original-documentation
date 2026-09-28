# Device Management

**STATUS: PROPOSED.** This system-level view defines device service boundaries; the user-facing inventory workflow is in [Computer Management device management](../03-computer-management/device-management.md).

A device adapter enumerates through supported Windows PnP/configuration APIs, normalizes properties without discarding source, and emits add/remove/change events where available. It must tolerate duplicate, stale, inaccessible and surprise-removal conditions. Webster does not install arbitrary kernel drivers or own device arbitration in Phase 1. Long-running queries are cancellable and do not block the UI. Any future device-control service needs explicit capability, API, driver trust and rollback design.
