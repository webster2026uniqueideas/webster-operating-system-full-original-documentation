# Volumes

**STATUS: PROPOSED.** A volume is modeled independently from physical disk and partition; mount points and drive letters are associations that can change.

Report volume identity, filesystem, labels, capacity/free space, mount paths, online/read-only state and encryption metadata when accessible. Validate mount targets and permissions. Format, dismount, assign-letter and repair operations require scoped authorization, clear destructive warning, fresh target verification and Windows-confirmed completion. Handle system/boot, network, virtual, encrypted and removable volumes as special cases; unsupported actions remain disabled with explanation.
