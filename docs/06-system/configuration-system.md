# Configuration System

**STATUS: PROPOSED.** Configuration has explicit ownership, scope, schema and migration policy.

Separate machine policy, per-user preferences, runtime state and secrets. Use versioned structured formats with strict parsing, defaults and validation; write atomically and preserve a recoverable prior version. Honor managed Windows policy and do not silently overwrite unknown values. Registry use is limited to documented Windows integration settings; it is not Webster's general database or secret store. Secret values use supported OS cryptographic protection with access control. Configuration migrations are idempotent, logged and rollback-aware. See [configuration reference](../17-reference/configuration-reference.md).
