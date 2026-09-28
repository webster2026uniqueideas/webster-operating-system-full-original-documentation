# C++ Standards

**STATUS: PROPOSED.** Target C++20 with a pinned, supported MSVC/Windows SDK toolchain, pending compatibility validation.

Use RAII, `std::unique_ptr` for exclusive ownership, value types, const-correctness, scoped enums and explicit thread/resource lifetimes. Avoid owning raw pointers, C-style casts, unchecked format strings and naked HANDLE management. Use Unicode Win32 APIs; isolate conversions. Prefer expected operational errors as values; exceptions never cross C ABI, IPC or module boundaries. Enable compiler warnings/static analysis, sanitizers where supported and secure release linker options. Use modules only after toolchain and build support is demonstrated. Third-party dependency/license review is mandatory.
