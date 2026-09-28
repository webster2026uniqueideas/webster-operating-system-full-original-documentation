# Performance Management

**STATUS: PROPOSED.** Performance views provide sampled, attributed observations, not guarantees or a new scheduler.

Track CPU, committed/working-set memory, disk activity, network throughput and process usage using supported APIs. Every metric states units, interval, timestamp, sampling source and known limitations. Avoid high-frequency polling; use bounded sampling, cancellation and back-pressure. Handle permissions, counter resets, multi-core normalization, sleep/resume and missing counters. Trends are local unless telemetry is explicitly consented to; default collection should remain on-device. Do not terminate or reprioritize workloads automatically without an explicit policy and user-visible rationale.
