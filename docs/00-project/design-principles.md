# Design Principles

**STATUS: REQUIRED** as guidance for future design decisions; implementation is **NOT YET IMPLEMENTED**.

1. **Truthful ownership:** distinguish Webster policy/UI from Windows-provided capabilities.
2. **Least privilege:** default to standard-user execution; broker only specific authorized actions.
3. **Explicit contracts:** version APIs, IPC messages, configuration and persisted formats.
4. **Secure by construction:** validate at boundaries, authenticate IPC peers, minimize secrets and audit sensitive operations.
5. **Failure is a state:** report partial results, platform errors and recovery options; never imply success prematurely.
6. **Accessible by default:** keyboard operation, screen-reader semantics, contrast, scaling and reduced-motion support are design constraints.
7. **Composable and testable:** separate UI, domain policy, platform adapters and privileged operations.
8. **Supported integration:** prefer documented Windows interfaces; isolate compatibility-sensitive adapters.
9. **Reversible administration:** destructive actions require clear scope, confirmation and recovery planning.
10. **Evidence before independence:** kernel, bootloader and hardware ownership require separate feasibility, threat and maintenance reviews.
