# Connectivity

**STATUS: PROPOSED.** Connectivity diagnostics separate physical/link, address assignment, routing, name resolution and application reachability.

Ethernet and Wi-Fi are surfaced through Windows network state; DHCP and DNS are Windows-provided in Phase 1. Diagnostics should use bounded, consented probes to known targets and avoid collecting payloads. Report each stage separately with timestamps and likely scope, not a single false “internet” verdict. VPNs, captive portals, proxies, sleep/resume and managed policies alter results. Avoid automatic network resets or credential prompts; provide supported Windows settings links and explicit recovery steps.
