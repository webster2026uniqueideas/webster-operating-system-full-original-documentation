# Event Management

**STATUS: PROPOSED.** Provide searchable, bounded access to Windows event logs and Webster operational/audit events.

Records should include provider/source, event identifier, severity, timestamp and timezone, correlation ID where available, message and structured fields. Query filters must be bounded and avoid untrusted query construction. Log access is permission-scoped; sensitive fields are redacted in UI/export where feasible. Preserve original event data and identify any normalization. Webster audit records should be integrity-protected by the host's supported mechanism and must not be presented as tamper-proof absent evidence. Export requires explicit destination and privacy notice. Failures or inaccessible channels are shown, not silently omitted.
