# Network Management

**STATUS: PROPOSED.** Management queries use documented Windows APIs and respect enterprise policy.

Show adapters, connection state, media type, addresses/routes where permitted, DNS configuration and per-adapter metrics with source/time. Wi-Fi profile/security details are sensitive and permission scoped. Configuration changes require preview, target-interface identity, policy check, confirmation, platform API success and connectivity recovery guidance. Never store shared Wi-Fi credentials in Webster plaintext. Network profile and firewall changes may require elevation and may be blocked by domain policy; explain this without suggesting policy bypass.
