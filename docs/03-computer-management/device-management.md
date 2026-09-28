# Device Management

**STATUS: PROPOSED.** Device views are Windows-backed inventory and supported configuration workflows; Webster does not own PnP, drivers or a HAL in Phase 1.

Enumerate devices using supported Windows device/property APIs. Show stable identifiers only when needed, friendly name, class, present/removed state, status/problem code, provider/version, driver signing/status where available, and source/refresh time. Distinguish unknown, inaccessible and absent values. Driver installation/removal or enable/disable operations require platform authorization, compatibility checks, confirmation and recovery guidance; no arbitrary driver loading. WMI may supplement discovery but is not the sole source or guaranteed available. See [hardware management](../06-system/hardware-management.md).
