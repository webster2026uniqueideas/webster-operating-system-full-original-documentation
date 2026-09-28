# Process Isolation

**STATUS: PROPOSED.** Use process boundaries when components have materially different trust or privilege, not as decoration.

UI and extension-capable components run unprivileged and isolated from management authority. A broker is small, separately packaged, restricted, authenticated over IPC and limited to an allow-list. Windows owns process, token, job and memory isolation in Phase 1. Apply supported mitigations (DEP, ASLR, CFG and appropriate child-process/dynamic-code restrictions) after compatibility testing. Avoid code injection, shared writable executable memory and unsafe plugin loading. A compromised UI must not gain arbitrary host administration. See [process model](../01-architecture/process-model.md).
