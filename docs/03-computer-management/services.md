# Service Management

**STATUS: PROPOSED.** Windows Service Control Manager (SCM) owns Windows service lifecycle and dependency semantics. WCM is a client.

Discover services through supported SCM APIs; show service identity, display name, current state, start type, account (appropriately redacted), dependencies and last observed time. Start/stop/restart and startup changes require per-operation authorization, fresh state/dependency checks, clear impact, confirmation where interruption is likely, timeout and result verification. Do not force termination as routine stop behavior or alter protected services. Preserve recovery configuration when changing startup settings. Service dependencies can include services outside Webster; show those edges and handle partial data. Webster services, if introduced, must document owner, identity, recovery and upgrade policy separately.
