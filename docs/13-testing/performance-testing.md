# Performance Testing

**STATUS: PROPOSED.** Set measurable budgets after prototype baselines, not by assumption.

Measure cold/warm launch, UI input latency, steady-state CPU/memory, inventory latency, polling overhead, IPC throughput, cancellation, large event query behavior and shutdown time on documented hardware/OS configurations. Report percentiles, sample period and background workload. Test degraded/slow WMI/providers and large device/process counts. Avoid aggressive collection that itself distorts performance. Regression thresholds require repeatable environments and versioned baselines.
