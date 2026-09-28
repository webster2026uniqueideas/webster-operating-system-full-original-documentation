# System Tools

**STATUS: PROPOSED.** WCM system tools provide inventory and controlled entry points, while Windows remains the authority for host state.

- **System information:** OS edition/build, architecture, device identifiers as policy allows, uptime and Webster component versions; distinguish host-reported from Webster-derived fields.
- **Task/process management:** enumerate available processes and resource counters; expose terminate/priority operations only with permissions, confirmation and Windows success result.
- **Event management:** search/filter accessible Windows event sources plus Webster events; protect logs and label source/provider/time.
- **Diagnostics:** collect minimal, consented bundles, redact secrets and support export/deletion policies.
- **System configuration:** link to Webster settings and approved Windows settings surfaces; explain scope and restart requirements.

Each tool has read/write capability declarations, error states and an audit policy. See [performance](performance.md), [events](event-management.md) and [administration](administrative-tools.md).
