# Users and Groups Management

**STATUS: PROPOSED.** During Windows-integrated phases, Windows accounts, tokens, groups and access-control checks remain authoritative.

WCM may inspect local/domain identity data within caller permissions and present Webster application preferences/roles separately. Account creation, deletion, enable/disable, membership, password reset and privilege changes are distinct high-impact operations; require platform authorization, exact identity confirmation, policy compliance, audit and recovery considerations. Do not store Windows passwords or claim Webster can override domain policy. Avoid exposing credential material or sensitive identifiers unnecessarily. For account architecture see [users](../08-users/user-management.md) and [security](../05-security/authorization.md).
