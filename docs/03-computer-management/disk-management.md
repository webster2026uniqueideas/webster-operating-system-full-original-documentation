# Disk Management

**STATUS: PROPOSED.** Disk management is a high-risk Windows integration surface.

Inventory physical disks, partition tables, partitions, volumes, capacity and health indicators when supported, identifying unavailable or stale data. Read operations are default. Any partition, format, initialize, mount, offline or destructive operation requires capability checks, exact target identity, impact preview, explicit confirmation, fresh revalidation, platform authorization, progress and final verification. Never infer that a disk is safe to modify from a drive letter or stale selection. Webster delegates partitioning and filesystem operations to Windows-supported APIs/tools and never bypasses locks, encryption or policy. See [drives](../09-storage/drives.md), [partitions](../09-storage/partitions.md) and [storage security](../09-storage/storage-security.md).
