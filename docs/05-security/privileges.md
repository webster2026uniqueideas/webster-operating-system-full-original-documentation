# Privileges

**STATUS: REQUIRED** design principle. Standard-user execution is the default.

Separate read-only inventory from state mutation. Do not elevate the whole desktop. Use supported Windows consent/elevation or a dedicated restricted service only for operations that require it. Privilege requests name the exact operation and target; authorization is checked server-side and platform access checks still apply. Do not run as LocalSystem without a documented necessity, threat analysis and review. Privilege is never inferred from group labels or caller parameters alone. Revoke handles and temporary elevation promptly; audit grant/use/failure while minimizing personal data.
