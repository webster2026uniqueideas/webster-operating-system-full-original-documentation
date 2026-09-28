# Network Security

**STATUS: PROPOSED.** Networking uses the Windows stack and policy. Webster services should bind only when needed and restrict endpoints, interfaces and identities.

Use authenticated, encrypted protocols for remote communication; validate certificates and names; set timeouts and size limits; reject downgrade and malformed input; avoid storing tokens in logs/configuration. Default to no inbound listener. Firewall rules are explicit, minimal, documented and removable; never disable Windows Firewall. Respect managed policy and report when a rule cannot be applied. Diagnostics minimize packet/content capture and require consent. See [firewall integration](../07-networking/firewall-integration.md).
