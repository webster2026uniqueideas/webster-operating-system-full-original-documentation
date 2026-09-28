# Partitions

**STATUS: PROPOSED.** Partition inventory is Windows-backed; mutation is high risk and may be unsupported or blocked.

Display partition style/identifier, offset, size, type, associated disk and any mounted volume when APIs provide them. Partition creation/deletion/resizing/initialization is never performed from stale display state; require exact disk identity, capacity/impact preview, confirmation, elevated supported API, progress, post-operation enumeration and interruption/recovery guidance. Do not promise lossless resize or bypass encryption, open handles or system protections. See [disk management](../03-computer-management/disk-management.md).
