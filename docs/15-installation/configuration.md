# Configuration

**STATUS: PROPOSED.** Configuration is versioned and scoped as defined in [configuration system](../06-system/configuration-system.md).

Installer defaults are secure and minimal. User preferences can be changed without admin; machine-wide policy is protected and may be managed externally. Imports are schema-validated, size-bounded and previewed. Secrets are never accepted in command-line arguments or plaintext configuration. Migrations are transactional or recoverable. Document defaults, precedence, policy lock, reset and export behavior in the future reference; no keys are defined as implemented here.
