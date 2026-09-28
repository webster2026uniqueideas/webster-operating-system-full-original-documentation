# System API

**STATUS: PROPOSED.** System API provides read-only host capability, health and inventory snapshots plus separately authorized operations.

**Purpose/consumers:** consistent interface for desktop, WCM and Webster services. **Inputs/outputs:** scoped query, filters, paging and freshness preference -> typed snapshot/job with source and timestamp. **Errors:** denied, unsupported, partial, stale, timeout, policy and platform error. **Security:** explicit capabilities, least privilege, bounded queries, authorization at mutation boundary, no arbitrary command API. **Versioning:** major/minor schema; additive optional fields; clients negotiate capabilities. **Compatibility:** Windows adapters implement per-version support and map platform differences without claiming unavailable data. Storage/process/network/device sub-APIs follow the same envelope; see [API architecture](api-architecture.md).
