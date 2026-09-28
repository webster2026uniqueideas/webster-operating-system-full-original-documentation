# Memory Management

**STATUS: PROPOSED.** Windows owns physical/virtual memory management, paging, address spaces and memory protection in Phases 1 and 2.

Webster may report supported process/system memory counters with clear units, timestamps and definitions. Webster applications should bound caches, allocations and queues; handle allocation failure; avoid retaining sensitive data; and use RAII. Do not claim deterministic physical-memory control or expose kernel memory manipulation. Future independent-OS memory manager work is **FUTURE / RESEARCH** and outside this platform specification.
