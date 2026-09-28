# Firewall Integration

**STATUS: PROPOSED.** Windows Firewall remains authoritative. Webster may inspect status and request narrowly scoped rules through documented management interfaces when the user/admin authorizes it.

No feature disables the firewall or creates broad inbound access. A rule proposal specifies executable/service identity, direction, protocol, ports, profiles, interfaces, rationale and expiry/removal policy. Check existing/managed rules and conflict results; report blocked/unsupported states. Rule changes are privileged, audited and reversible. Do not treat “firewall on” as proof all traffic is protected or expose hidden policy. See [network security](../05-security/network-security.md).
