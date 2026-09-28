# Filesystem

**STATUS: PROPOSED.** Webster does not define or implement a Phase 1 filesystem. Windows-mounted filesystems and their semantics remain authoritative.

Webster file APIs operate on Windows paths/handles, preserve ACLs and filesystem behavior, avoid assumptions about case sensitivity, path length, reparse points and removable/network storage, and communicate sharing/permission failures. Any Webster-managed metadata is versioned, namespaced and recoverable; do not make hidden sidecar state authoritative. Temporary files use secure creation and cleanup. A future Webster filesystem requires a separate format, crash consistency, integrity, recovery, encryption and migration design.
