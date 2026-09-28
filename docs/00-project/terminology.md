# Terminology

**STATUS: PROPOSED.** Definitions are normative where referenced by requirements.

- **Webster:** the proposed product/platform described by this repository, not a currently implemented OS.
- **Windows-integrated environment:** Webster applications and services running on Windows and using supported Windows facilities.
- **Webster-owned:** behavior, policy, UI, contract or process implemented by Webster when built.
- **Windows-provided:** operating-system capability whose authority and implementation remain with Windows.
- **Native core:** proposed C++ integration and domain layer; does not mean kernel code.
- **Broker:** a narrowly privileged process that validates and performs an explicitly permitted operation for a less-privileged client.
- **Computer Management:** proposed Webster administrative console and associated service interfaces.
- **Session:** authenticated interactive user context managed by Windows in Phase 1; Webster session state is application-level.
- **Standalone native component:** separately packaged process/module communicating with the main program through an explicit API; not embedded in the main executable.
- **Independent OS:** a future bootable Webster system with its own designed boot chain and kernel, not part of Phase 1.

See the [master glossary](../17-reference/glossary.md) for the canonical expanded list.
