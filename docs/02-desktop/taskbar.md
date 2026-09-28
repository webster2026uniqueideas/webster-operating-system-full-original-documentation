# Taskbar

**STATUS: PROPOSED.** A Webster taskbar may expose launch, pinned items, running Webster apps and an optional status/tray region.

Requirements: keyboard navigation and accessible names; visible focus; stable layout; clear running/attention state; context actions scoped to the selected app; avoid duplicate or misleading status when Windows already presents the same system function. Pinning and ordering are per-user preferences. Launch uses registered application identity and safe argument handling, never concatenated shell commands.

Window activation and application lifecycle remain Windows-controlled. If the host taskbar is active, Webster must define coexistence rather than silently hide or replace it. Tray icons are limited, discoverable and have accessible alternatives.
