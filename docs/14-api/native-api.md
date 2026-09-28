# Native API

**STATUS: PROPOSED.** Native API defines C++ interfaces between domain services and platform adapters.

**Purpose/consumers:** typed capabilities for Webster apps/services; consumers are internal components and separately versioned native processes. **Inputs/outputs:** value types, validated options, cancellation/deadline; results include status, provenance and stable error. **Errors:** unsupported, access denied, invalid input, stale, timeout, canceled, partial and platform failure. **Security:** interface invocation does not grant authority; adapter uses caller token or explicit broker contract. **Versioning:** source API follows C++20/toolchain; binary ABI is private unless explicitly stabilized, and no STL/exceptions cross a public ABI. **Compatibility:** adapters declare OS/API capabilities and tests; missing optional fields remain unavailable, not fabricated.
