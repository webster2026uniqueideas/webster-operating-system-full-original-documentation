# Storage Security

**STATUS: PROPOSED.** Windows ACLs and supported encryption facilities remain authoritative.

Respect user/machine ACLs, BitLocker and policy; never weaken permissions or silently decrypt/format. Use OS-protected secret facilities and approved encryption APIs rather than custom cryptography. Treat device identifiers, filenames and health data as sensitive. Diagnostics/export are consent-based and redacted. Verify package/data ACLs and reject writable executable paths. Recovery documentation must distinguish data recovery from OS recovery and must not promise decryption without keys. See [filesystem security](../05-security/filesystem-security.md).
