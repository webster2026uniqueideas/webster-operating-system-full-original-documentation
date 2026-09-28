# Filesystem Security

**STATUS: PROPOSED.** Windows filesystems and ACL enforcement remain platform-owned in Phase 1.

Install machine binaries/configuration under protected locations and per-user data under the user's profile with appropriate ACLs. Separate executable, mutable data, cache, logs and secrets. Use canonicalized paths, handle-based operations where practical, reparse-point-aware validation, exclusive temporary creation and atomic replacement for configuration. Never assume a path stays unchanged between check and use. Apply encryption through supported Windows facilities and clearly report policy/availability; Webster must not implement ad hoc cryptography. Backups and diagnostics require privacy controls. See [storage security](../09-storage/storage-security.md).
