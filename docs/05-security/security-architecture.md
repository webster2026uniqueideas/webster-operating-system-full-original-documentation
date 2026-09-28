# Security Architecture

**STATUS: REQUIRED** as a design constraint; Webster security implementation is **NOT YET IMPLEMENTED**.

## Security Goals

Protect users and host integrity; prevent unauthorized administrative changes; minimize exposure of credentials and personal data; preserve trusted updates; and provide diagnosable, privacy-conscious evidence of security-sensitive operations.

## Architecture

Webster inherits Windows identity, token, ACL, process and kernel enforcement during Phases 1 and 2. Webster adds application authorization, input validation, secure IPC, safe configuration, auditing and signed distribution. It must not claim to replace Windows authentication or security authority. Use standard-user processes by default; isolate privileged functionality in a separately protected, narrow broker only when required.

## Controls

Authentication uses Windows session identity in Phase 1; never collect Windows passwords. Authorization checks identity, role, operation, target, policy and current state at the enforcement boundary. Secrets use supported OS cryptographic protection and minimal lifetime. Files and executables have restrictive ACLs. IPC authenticates peer identity and rejects malformed/oversized input. Network features use secure defaults and Windows firewall policy. Native code follows memory-safe practices, secure loading and static analysis. Updates require authenticated signature verification, rollback protection and recovery. Sensitive operations generate protected, redacted audit events.

## Threat Model

Assets include host integrity, accounts/tokens, user data, IPC authority, update signing keys, configuration and audit records. Attackers include unprivileged local users, compromised Webster apps, malicious extensions/dependencies, remote peers and supply-chain compromise. See [threat model](threat-model.md), [authorization](authorization.md), and [security specification](../../specifications/security-specification.md).
