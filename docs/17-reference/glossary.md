# Webster Glossary

**STATUS: PROPOSED.** These definitions are canonical across the initial specification.

| Term | Definition |
|---|---|
| Broker | Separate, narrowly privileged process that validates and executes allow-listed requests. |
| Computer Management (WCM) | Proposed Webster console for inspection and authorized host-management workflows. |
| Dependency | Windows API, toolchain, policy, service or component Webster relies on but does not own. |
| Independent OS | Future bootable Webster architecture with separately designed kernel and boot chain; not Phase 1. |
| IPC | Inter-process communication using authenticated, versioned, bounded messages. |
| Native core | Proposed user-mode C++ domain/integration layer; not kernel code. |
| Platform adapter | Component mapping Webster contracts to supported Windows interfaces. |
| Proposed target architecture | Intended design described for planning; not implementation evidence. |
| Session | In Phase 1, Windows interactive user context plus Webster application state scoped to it. |
| Standalone native component | Separately packaged executable/process communicating over explicit API/IPC, not embedded in main program. |
| Webster-owned | UI, policy, contracts, orchestration or code controlled by Webster when implemented. |
| Windows-provided | Capability enforced/implemented by Windows during the integrated phases. |
| Windows-integrated environment | Webster apps/services hosted by Windows and using its supported OS facilities. |
| Requirement | Testable constraint identified by a unique `WEB-*` identifier. |

See [project terminology](../00-project/terminology.md) for the short form.
