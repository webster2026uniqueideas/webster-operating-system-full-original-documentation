# Permissions

**STATUS: PROPOSED.** Webster configuration/data permissions use Windows ACLs and least-privilege installation defaults in the integrated phases.

Protect machine-wide binaries and policy from standard-user modification; separate machine-wide immutable assets from per-user writable settings/cache/log data. Validate effective access during installation and update. Do not create world-writable directories on executable search paths. Honor inherited ACLs and managed-device policy; report access denied without instructing users to weaken security. File APIs must avoid path traversal, reparse-point/symlink surprises and unsafe temporary-file races. See [filesystem security](filesystem-security.md).
