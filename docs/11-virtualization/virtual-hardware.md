# Virtual Hardware

**STATUS: PROPOSED.** Test guests use hypervisor-defined virtual CPU, memory, disks, NICs and firmware. The virtual profile is not equivalent to physical hardware support.

Define deterministic reference profiles for CI/manual testing, version guest additions/tools, constrain resource use and test absent devices/low memory/network loss. Keep test credentials and signing keys out of guest images. For any future independent OS prototype, document emulated devices separately from supported physical hardware and test both paths before claims of compatibility.
