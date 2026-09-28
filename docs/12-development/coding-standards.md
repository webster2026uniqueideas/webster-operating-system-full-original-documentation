# Coding Standards

**STATUS: PROPOSED.** Standards become normative when source implementation begins.

Use small cohesive components, explicit ownership, meaningful types and stable error categories. Keep UI responsive and platform calls behind adapters. Validate untrusted input at every boundary; use bounded operations and cancellation. Document non-obvious invariants and public contracts, not line-by-line narration. Avoid global mutable state, hidden side effects, unsafe command construction and silent catch-all failures. All changes include focused tests and review of failure/permission behavior. Formatting, static analysis and warning policy must be automated in CI once the toolchain is selected.
