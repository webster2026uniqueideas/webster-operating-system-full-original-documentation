# Virtualization

**STATUS: PROPOSED.** Virtualization is a development, testing and optional user capability hosted by Windows; Webster does not implement a hypervisor in Phase 1.

Use supported Hyper-V, Windows virtualization APIs or other approved hypervisors subject to edition, firmware, policy and licensing. Isolate test guests from production networks and secrets. Record host/guest versions and resource allocation for reproducibility. Virtualization is useful for snapshots and destructive management tests, but cannot fully validate physical device, firmware, timing or secure-boot behavior. See [VMs](virtual-machines.md), [virtual hardware](virtual-hardware.md) and [hypervisor integration](hypervisor-integration.md).
