# System Services

**STATUS: PROPOSED.** Webster system services are optional user-mode components; Windows services and kernel facilities remain distinct.

A Webster service has an owned contract, identity, lifecycle, health model, dependencies, configuration schema, log policy, version support and uninstall path. Prefer user-session processes. Persistent services require a necessity statement, privilege review and failure isolation. Use SCM only for services designed to run under Windows service semantics. No service may claim OS-wide authority beyond its Windows token. See [native services](../04-native/native-services.md).
