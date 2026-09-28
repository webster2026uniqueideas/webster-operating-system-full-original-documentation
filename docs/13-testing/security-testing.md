# Security Testing

**STATUS: REQUIRED** before privileged functionality or release.

Threat-led tests cover IPC spoofing/ACL bypass, authorization race/TOCTOU, malformed and oversized messages, path/reparse-point attacks, command injection, DLL search order, insecure defaults, privilege escalation, data/secret leakage, update tampering/downgrade, dependency vulnerabilities and audit failure. Use fuzzing for parsers and protocol boundaries, static analysis and supported runtime sanitizers. Verify standard-user denial and managed-policy behavior. Findings are triaged and tracked to closure; security tests do not replace design review or external assessment.
