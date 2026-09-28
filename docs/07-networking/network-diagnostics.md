# Network Diagnostics

**STATUS: PROPOSED.** Diagnostics collect the minimum evidence needed to distinguish local interface, DHCP, routing, DNS, proxy, firewall and remote endpoint failures.

Each check is bounded, cancelable and labeled with target/method/time. Provide local-only mode by default; exporting diagnostics requires user consent and previews included identifiers. Redact SSIDs, addresses, domains and tokens where feasible. Do not silently packet-capture or upload telemetry. Probe outcomes are evidence, not proof of root cause. Results are stored with retention limits and can be deleted.
