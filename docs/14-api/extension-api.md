# Extension API

**STATUS: FUTURE / PROPOSED.** An extension mechanism is not required for initial Webster releases and must not become a privileged plugin system.

**Purpose/consumers:** optional third-party UI/content integration. **Inputs/outputs:** signed/validated manifest requests declared capabilities; host returns approval and narrow events/actions. **Errors:** invalid signature/manifest, denied capability, incompatible version, timeout, crash or unavailable host. **Security:** extensions untrusted by default; isolate process, least privilege, explicit consent, resource limits and revocation. No native DLL loading into privileged processes. **Versioning:** manifest/API versioned independently; deprecated capabilities announced. **Compatibility:** compatibility ranges and conformance tests; fail closed when an extension requests unknown authority. Detailed sandbox and signing design is a prerequisite before implementation.
