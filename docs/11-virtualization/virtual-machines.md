# Virtual Machines

**STATUS: PROPOSED.** Webster may provide a VM inventory/control UI only if a supported hypervisor API and product scope are selected.

The VM model includes identity, state, virtual CPU/memory allocation, virtual disks, network attachment, checkpoint/snapshot metadata and host ownership. Lifecycle states cover create/configure, start, running, pause/resume, graceful shutdown, forced stop, checkpoint/restore and removal where the chosen provider supports them. Operations are delegated to the hypervisor, authorized and confirmed; Webster must not imply guest isolation makes all host resources safe. VM files and snapshots are sensitive, storage-consuming assets. Initial use is developer/test automation, not a promise of a Webster virtualization product.
