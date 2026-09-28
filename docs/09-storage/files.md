# Files

**STATUS: PROPOSED.** Webster file workflows use Windows file APIs and preserve host filesystem semantics, metadata and ACLs.

Support safe browsing, launching through registered associations, properties and explicit file operations. Do not assume case sensitivity, local availability or path permanence. Revalidate selection, guard reparse points/path traversal, use atomic writes where applicable, report sharing/permission errors, and avoid following a link into unintended privileged locations. Metadata display identifies unavailable values. Application data is namespaced and versioned; no hidden system files are required for core OS behavior.

Temporary files use an OS-provided per-user temporary location, restrictive creation semantics, bounded lifetime and cleanup on normal exit, with stale-file cleanup that never follows an untrusted path. Webster application data has an explicit per-user or machine scope, schema version and backup/uninstall policy. User content is not silently moved into Webster-owned storage.
