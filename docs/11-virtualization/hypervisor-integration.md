# Hypervisor Integration

**STATUS: RESEARCH.** No hypervisor API/provider has been selected.

An integration proposal must compare Windows Hyper-V management interfaces and other supported providers for API stability, licensing, edition constraints, privilege model, automation, virtual networking and update compatibility. Webster should use provider adapters, least privilege, explicit VM operation consent, strict path validation and status polling with cancellation. It must not install or enable a hypervisor without explicit user/admin action or override corporate policy. Integration errors remain distinguishable from guest errors.
