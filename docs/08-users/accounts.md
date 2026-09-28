# Accounts

**STATUS: PROPOSED.** Webster integrates with Windows local, domain or managed identities through the current process token and supported APIs.

Webster may display accounts or request administrative actions only when allowed by Windows policy and authorization. It must not store Windows password hashes, perform silent password resets, bypass lockout or create a second identity authority. Account identifiers are minimized in logs/UI. Recovery and account unlocking follow Windows/domain administrator procedures. A future independent-Webster account system is **FUTURE / RESEARCH** and needs threat, credential, migration and recovery design.
