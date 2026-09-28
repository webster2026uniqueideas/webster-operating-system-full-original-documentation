# Storage System

**STATUS: PROPOSED.** Webster storage services model and orchestrate Windows storage information; Windows owns block I/O, volume management, caches and filesystems in Phase 1.

Represent physical device, partition, volume, mount point and filesystem as distinct linked entities with stable-scoped identifiers and observation timestamps. Read queries are separated from mutation commands. Track capacity, free space and supported health/encryption metadata without asserting unsupported precision. Mutations use Windows facilities, revalidate selected device/volume identity, expose progress and preserve recovery options. Handle removable/offline/network volumes, permissions and encryption. See [storage architecture](../09-storage/storage-architecture.md).
