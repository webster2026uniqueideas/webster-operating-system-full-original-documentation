# Sessions

**STATUS: PROPOSED.** Windows manages interactive logon, token, lock and desktop session boundaries. Webster creates an application session scoped to the host user session.

At launch, read only the required identity/profile context, initialize non-sensitive per-user state, and start UI without elevation. On lock, disconnect, logoff or shutdown, pause sensitive surfaces, cancel work, release handles and avoid persisting secrets. Multi-user/RDP sessions must not share mutable UI state or privileged IPC identity. Recover from partial initialization without blocking host logon. Do not emulate the Windows secure logon desktop. Session event detection uses supported notifications and handles missed events by revalidation.
