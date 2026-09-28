# Integration Testing

**STATUS: PROPOSED.** Verify Windows adapter behavior on a supported Windows matrix and under standard-user and authorized-admin contexts.

Test SCM/WMI/device/storage/network APIs where available; API absence and access denial are expected scenarios. Use temporary test services/devices or controlled VMs, clean up even after failure, and assert host state is restored. Validate IPC identity, ACLs, protocol versions, timeouts, client disconnects and operation audit. Record OS edition/build and policy state; do not use live user secrets.
