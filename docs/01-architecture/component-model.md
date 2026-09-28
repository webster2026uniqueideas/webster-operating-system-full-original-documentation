# Component Model

**STATUS: PROPOSED.** Components have explicit ownership, lifecycle, trust level, contract and failure behavior.

## Component Classes

- **UI process:** shell and applications, normally standard-user, responsible for presentation and user intent.
- **Domain library:** pure policy/model logic with no ambient platform authority where practical.
- **Platform adapter:** translates typed Webster operations to documented Windows APIs.
- **Background process/service:** only for work that needs independent lifecycle or a supported service identity; not a default deployment shape.
- **Privileged broker:** separately protected process for narrow administrative actions; validates caller, parameters, authorization and operation-specific policy.

## Contracts

Every component contract specifies API version, inputs, outputs, errors, identity requirements, timeout/cancellation, logging policy, compatibility and owner. Components avoid circular dependencies; UI depends on domain contracts, domain logic depends on abstractions, and adapters implement those abstractions.

## Lifecycle

Discover/install, start, health-check, serve, drain requests, stop, update and recover are explicit states. A crash must not corrupt host state; idempotent operations and bounded retries are preferred. State transitions and data ownership are recorded in the relevant service specification.
