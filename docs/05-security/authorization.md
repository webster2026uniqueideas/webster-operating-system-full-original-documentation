# Authorization

**STATUS: PROPOSED.** Windows access checks are authoritative for Windows resources. Webster authorization gates Webster-defined operations and must not weaken platform policy.

Define capabilities such as `system.read`, `process.inspect`, `service.control`, `storage.modify`, `account.manage` and `security.configure`; map these to Windows permissions and explicit operation policy rather than relying on UI visibility. Evaluate caller identity, role, target, requested action, current host state and policy at the broker/API boundary. Default deny; re-check at execution time to prevent stale-selection/TOCTOU errors. A successful UI check is not authorization. Record denied and completed sensitive actions without logging credentials. Domain policy and UAC remain in force.
