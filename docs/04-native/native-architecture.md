# Native Architecture

**STATUS: PROPOSED.** Webster native code is user-mode C++ integration, not a kernel layer in Phase 1.

The native architecture separates stable domain contracts, platform-neutral logic, Windows adapters and optional out-of-process brokers. Public ABI surfaces should be narrow and versioned; do not expose STL types, exceptions or compiler-specific ownership across a binary boundary. Internal interfaces use RAII, value types and explicit error results. Windows handles use scoped wrappers; conversions and lifetime are explicit.

## Toolchain Direction

Target **C++20** initially with MSVC and a pinned Windows SDK; validate minimum compiler/OS support before committing. CMake plus Visual Studio integration is a proposed build direction. Use `/W4` or stricter warning policy, treat selected warnings as errors, enable supported static analysis, ASan for compatible test configurations, and CFG/modern linker protections for release. Dependency and runtime choices require a recorded review.

No global mutable service registry. Threading uses owned executors, cancellation and bounded queues; synchronization primitives protect documented invariants only. Exceptions do not cross ABI, C, IPC or plugin boundaries. See [C++ architecture](cpp-architecture.md) and [native component specification](../../specifications/native-component-specification.md).
