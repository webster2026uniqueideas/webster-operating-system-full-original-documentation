# C++ Architecture

**STATUS: PROPOSED.** Use modern C++20, with the exact compiler and SDK support matrix decided before implementation.

## Rules

- Prefer value semantics, `std::unique_ptr` for exclusive ownership, and `std::shared_ptr` only for genuine shared lifetime.
- Use RAII for handles, locks, COM interfaces, memory, threads and temporary resources; never rely on manual cleanup paths.
- Prefer explicit error-return types for expected operational failures; exceptions may handle exceptional internal failures if consistently configured. Catch at process/API boundaries and translate to stable errors. Never throw across ABI or IPC.
- Avoid raw owning pointers, unsafe casts, unchecked arithmetic, unbounded allocation and global mutable state.
- Keep platform headers and Win32 types behind adapters where feasible. Use Unicode Windows APIs and explicit UTF conversions.
- Use `std::jthread`/stop tokens where toolchain support and lifecycle fit; never detach unmanaged work.
- Define lock ordering and cancellation semantics; no blocking I/O on UI thread.
- Log structured, redacted events with correlation IDs; no secrets or uncontrolled user data.

C++ modules may be evaluated after compiler/IDE support is confirmed; do not require modules solely for novelty. See [coding standards](../12-development/cpp-standards.md).
