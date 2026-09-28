# Known Limitations

**STATUS: CURRENT DOCUMENTATION LIMITATIONS.** These are consequences of the project being unimplemented, not defects in shipped software.

- No source implementation, builds, tests, packages or release support matrix exists in this repository.
- Windows API choices, exact Windows versions/editions, UI framework, IPC transport, installer, persistence and telemetry policy remain unvalidated decisions.
- Management capabilities depend on Windows API availability, permissions, edition and device policy; full access cannot be promised.
- A Windows-integrated desktop does not own kernel, boot, scheduler, filesystem, drivers, accounts or network stack.
- Standalone privileged broker design is proposed and needs detailed threat review before implementation.
- Independent boot/kernel/HAL and driver support are future research only.
