# User Management

**STATUS: PROPOSED.** During Windows-integrated phases, Windows authenticates identities and controls tokens and permissions. Webster maintains application preferences and may present authorized Windows-backed account information.

```mermaid
stateDiagram-v2
  [*] --> WindowsAuthenticated
  WindowsAuthenticated --> WebsterSessionStarting: launch / sign-in context
  WebsterSessionStarting --> Active: profile loaded
  WebsterSessionStarting --> Degraded: optional dependency unavailable
  Active --> Locked: host lock / policy event
  Locked --> Active: host unlock
  Active --> Ending: logout / shutdown
  Degraded --> Ending
  Ending --> [*]: release resources
```

Account creation, removal, lockout, recovery, group membership and password lifecycle remain Windows/domain responsibilities in Phase 1. Webster must not create a conflicting password store. Application-level roles are separate and cannot confer host privileges. See [accounts](accounts.md), [sessions](sessions.md), [profiles](profiles.md), [groups](groups.md).
