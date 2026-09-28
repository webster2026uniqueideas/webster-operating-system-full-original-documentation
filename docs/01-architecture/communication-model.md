# Communication Model

**STATUS: PROPOSED.** Prefer in-process typed interfaces for non-privileged code and authenticated IPC when process isolation or independent lifecycle is needed.

## Rules

- Keep contracts transport-neutral; select a transport after Windows support, deployment and threat review.
- Treat every boundary as untrusted, including same-user processes; authenticate peer identity and authorize each operation.
- Use bounded messages, strict schemas, length limits, timeouts, cancellation and back-pressure.
- Return structured status and platform error context without leaking secrets or sensitive data.
- Make administrative actions explicit requests with operation IDs, audit outcomes and idempotency where possible.
- Version contracts and reject unsupported versions safely; never silently reinterpret a privileged request.

The diagram and protocol constraints live in [IPC](ipc.md) and [secure IPC](../05-security/secure-ipc.md). No IPC transport is selected as implemented; named pipes are a candidate on Windows and require ACL, impersonation and peer-validation review.
