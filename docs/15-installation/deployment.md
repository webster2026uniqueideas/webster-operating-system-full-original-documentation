# Deployment

**STATUS: PROPOSED.** Distribution requires a signed release pipeline, provenance and support policy.

Package only required components; generate SBOM and dependency/license inventory; sign binaries and installer with controlled keys; publish checksums and release notes; protect update metadata against tampering and downgrade; stage rollout and provide rollback. Enterprise deployment must support silent install only with administrator-controlled flags and documented policy, not hidden consent. Separate development/test certificates from production. Key custody, update service, release channels and support lifecycle remain decisions before shipping.
