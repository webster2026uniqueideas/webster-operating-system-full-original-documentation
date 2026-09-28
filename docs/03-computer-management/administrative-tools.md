# Administrative Tools

**STATUS: PROPOSED.** Administrative tools combine scoped settings, security posture, logs, diagnostics and recovery links.

Tools must clearly separate inspection from changes; identify whether the setting belongs to Webster or Windows; show required role, policy constraints and restart impact; request consent through supported elevation; and record operation outcome. No arbitrary command execution, hidden policy modification, credential capture or silent elevation. Recovery supports safe mode/degraded UI and verified rollback where technically possible. A failed operation reports whether state is unchanged, partially changed or unknown. See [recovery](../10-boot/recovery.md), [privileges](../05-security/privileges.md) and [installation recovery](../15-installation/recovery.md).
