# IPC API

**STATUS: PROPOSED.** IPC API is the contract for separately installed Webster native processes.

**Purpose/consumers:** client/server request, reply and bounded event delivery. **Inputs/outputs:** protocol major/minor, operation ID, correlation ID, deadline and typed bounded payload -> completion status, result/error and correlation ID. **Errors:** unauthenticated, denied, malformed, unsupported version, rate-limited, canceled, timeout, disconnected and platform failure. **Security:** OS-authenticated peer, restrictive endpoint ACL, server-side authorization, operation allow-list, replay/idempotency rules, size limits and secret-free logs. **Versioning:** explicit handshake; incompatible major fails closed; additive optional fields within minor. **Compatibility:** old/new pairs tested in CI and updater coordinates client/server rollout.

Candidate Windows named-pipe transport requires security review; transport is not yet selected.
