# API Architecture

**STATUS: PROPOSED.** APIs are versioned contracts; no Webster API is implemented in this repository.

| API | Purpose | Consumers | Inputs / outputs | Errors | Security | Version / compatibility |
|---|---|---|---|---|---|---|
| System | Capability discovery, system identity and health | Desktop, WCM | Query/filter -> typed snapshots with source/time | Unsupported, denied, partial, stale, unavailable | Read-only by default; minimize identifiers | Major/minor contract; additive fields; unknown capability tolerated |
| Native | C++ domain/platform adapter boundary | Webster components | Typed operation -> typed result | Stable Webster category + platform context | No privilege implied by library call | ABI not exposed unless separately versioned; avoid STL across ABI |
| Desktop | Launch, shell state, settings and notifications | Shell/apps/extensions | App identity/events/actions -> state/result | Invalid target, policy, timeout, unavailable | User-session scope; validated registered identities | Versioned app contract; compatibility checked at registration |
| Storage | Inventory and explicit volume/file operations | WCM, apps with permission | Resource ID/action/options -> inventory/job result | Busy, denied, stale, unsupported, partial, IO failure | Read/mutate capability separation; confirm high-risk actions | Stable IDs scoped to host/session; schema versioned |
| Process | Enumerate/inspect and authorized actions | WCM, diagnostics | filters/PID-scoped request -> snapshot/action result | Protected, exited, denied, stale, unsupported | Windows token checks; no injection/arbitrary memory | IDs are ephemeral; additive schema |
| Network | Interface/connectivity diagnostics and approved config | WCM, settings | interface/probe config -> state/diagnostic | Policy, timeout, disconnected, denied | No secrets in logs; explicit consent for probes | Versioned provider capabilities |
| Security | Identity/capability query and authorization request | Broker, WCM | operation/target/context -> decision/reason | Denied, policy, identity unavailable | Default deny; enforcement-side decision | Versioned capability IDs; no privilege escalation on unknown values |
| Device | Inventory and eligible supported actions | WCM | device identity/filter -> properties/action state | Removed, denied, unavailable, stale | Windows PnP authorization; no driver loading shortcut | Properties optional and source-tagged |
| IPC | Cross-process request/reply/events | UI, broker, services | bounded versioned message -> structured reply | protocol, auth, timeout, cancellation, remote failure | Authenticated OS peer, ACL, allow-list | Explicit negotiation; fail closed on unsupported major |
| Extension | Optional constrained UI/application integration | Approved extensions | manifest + capability request -> scoped events/actions | invalid, incompatible, denied, unavailable | Untrusted by default; no direct privileged API | Signed/versioned manifest; compatibility gate |

Common envelope: request/correlation ID, contract version and deadline; result has status, typed payload, source/freshness and stable error. APIs do not expose generic command execution. See specialized contracts in this section.
