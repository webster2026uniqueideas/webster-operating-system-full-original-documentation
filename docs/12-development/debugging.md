# Debugging

**STATUS: PROPOSED.** Debugging practices must preserve user privacy and host integrity.

Use symbolized builds, structured logs with correlation IDs and opt-in diagnostic bundles. Redact credentials, tokens, private paths and network identifiers. Prefer synthetic data and isolated VMs for privileged workflows. Debug broker/service under least privilege; do not disable platform protections as a routine workaround. Capture dumps only with user/admin consent, access controls and retention policy. Record OS build, Webster version, configuration schema and reproduction steps without exposing secrets.
