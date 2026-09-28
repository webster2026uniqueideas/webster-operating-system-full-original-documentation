# Auditing

**STATUS: PROPOSED.** Audit security-sensitive Webster operations using supported Windows event/log facilities or a documented protected local store.

Record actor identity reference, operation, target class/identifier as appropriate, request/correlation ID, authorization decision, start/end and outcome. Exclude passwords, tokens, private keys and unnecessary personal data. Protect access and integrity using OS controls; do not claim tamper-proof storage. Define retention, rotation, export and failure behavior. If audit recording is mandatory for a high-risk mutation and unavailable, fail closed or require an explicitly approved policy; ordinary diagnostics must not block unrelated work. Distinguish audit logs from debug telemetry and honor managed policy.
