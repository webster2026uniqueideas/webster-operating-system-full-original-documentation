# Unit Testing

**STATUS: PROPOSED.** Pure domain logic, schema validation, state transitions and error mapping should be unit-testable without Windows privileges or external services.

Use deterministic inputs, fake clocks/providers and no ambient network/disk dependencies. Cover boundary values, overflow, malformed configuration, cancellation, partial results and all public error categories. Tests must not rely on user profile or machine-specific registry state. Keep test doubles behaviorally explicit; they do not establish platform compatibility.
