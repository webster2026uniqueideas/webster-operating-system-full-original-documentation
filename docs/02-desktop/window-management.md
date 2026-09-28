# Window Management

**STATUS: PROPOSED.** Webster applications should use the host windowing system and follow a shared behavior contract.

Every top-level window provides a descriptive title, system-accessible controls, predictable focus order, resize/move/minimize/maximize/close behavior where applicable, keyboard shortcuts, DPI-aware layout and multi-monitor restoration. Dialogs are owned and modal only when necessary. Destructive confirmation identifies the affected resource and consequence.

Webster may provide app-level grouping, navigation and restore hints, but Windows owns compositor, window handles, desktop/session isolation and actual z-order. Persisted placement is advisory: clamp restored coordinates to current displays and avoid inaccessible windows. Remote-desktop, secure desktop and policy transitions must degrade safely.

No custom window manager is implied in Phase 1.
