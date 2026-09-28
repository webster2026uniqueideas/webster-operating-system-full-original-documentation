# Hardware Management

**STATUS: PROPOSED.** Windows owns hardware abstraction, drivers, Plug and Play, interrupts and device power policy during integrated phases.

Webster obtains inventory and selected status through documented Windows APIs, never direct port/MMIO access. Device control requires a supported driver/API, authorization and compatibility review. Handle hot-plug and sleep/resume; identifiers may be privacy-sensitive. Missing/unknown properties are not errors to fabricate. Future HAL/driver architecture is **FUTURE / RESEARCH** only and needs a separate safety and signing strategy.
