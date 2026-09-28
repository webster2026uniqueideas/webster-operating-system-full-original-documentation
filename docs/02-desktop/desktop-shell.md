# Desktop Shell

**STATUS: PROPOSED.** The shell is the Webster user-session entry point and navigation surface.

## Responsibilities

Provide application discovery/launch, desktop surface, taskbar, system tray/status area, notification presentation, context menu routing, settings navigation and session-aware behavior. It delegates window creation, input, rendering/composition and login/session security to Windows APIs/framework facilities.

## Behavior

- Start only after the Windows interactive session is available; show a recoverable error if required services are unavailable.
- Do not start elevated by default. Elevation occurs only through an explicit Windows consent flow or an approved broker.
- Maintain responsive input while work runs asynchronously; display progress, cancellation and stale/unavailable state.
- Respect Windows policies, multiple monitors, DPI, user settings and assistive technologies.
- Persist only documented per-user preferences; validate data and tolerate missing/corrupt optional state.

**DEPENDENCY:** UI framework and replacement-shell policy are not selected. Avoid assuming Webster owns the Windows logon or shell lifecycle.
