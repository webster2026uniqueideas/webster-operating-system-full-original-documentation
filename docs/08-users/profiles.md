# Profiles

**STATUS: PROPOSED.** Webster profile data is per-user application state stored under Windows-managed user profile locations.

Define schema/version, migration, size limits, backup/export behavior and privacy classification. Keep preferences, caches and logs separate; secrets use OS-protected storage, not ordinary profile files. Support redirected/roaming profiles by handling delayed, unavailable or read-only paths; avoid assuming local disk. Atomic writes and corruption recovery must preserve a safe default. Uninstall behavior for user data is explicit and consent-based.
