# Native Components

**STATUS: PROPOSED.** Candidate components are classified by trust and deployment rather than bundled by default.

- **Core library:** platform-neutral models, validation and stable error categories.
- **Windows adapter library:** process, service, device, storage, event, identity, networking and power adapters; each feature declares supported APIs and privileges.
- **Desktop host:** UI process, standard user by default.
- **Management client:** WCM UI and non-privileged query orchestration.
- **Optional management broker:** standalone executable only if isolation/privilege needs justify it; exact API allow-list, service identity and installer reviewed separately.
- **Test/support utilities:** development-only tools must not ship accidentally.

Libraries are not security boundaries inside one process. Components that need different trust/privileges must use OS-enforced process boundaries and authenticated IPC. Dynamic loading is disabled unless a signed, constrained extension mechanism is specified. See [standalone components](standalone-native-components.md).
