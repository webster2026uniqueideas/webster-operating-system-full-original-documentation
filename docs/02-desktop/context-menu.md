# Context Menu

**STATUS: PROPOSED.** The Webster desktop context menu is a contextual operating-system-style command surface, not a copy of another shell.

## Target Categories

- **Open / Open with:** shown only for a recognized target; safe default action and explicit application choice.
- **New:** create only supported item types in the clicked location; report collisions and permission errors.
- **Refresh:** refresh Webster's displayed view/model, not a claim to reset Windows or hardware.
- **Personalization:** open Webster desktop appearance and layout settings.
- **Display:** open relevant display controls; Windows remains the display authority in Phase 1.
- **System tools / Computer Management:** launch the relevant Webster management view and show unavailable capabilities honestly.
- **Settings:** navigate to scoped Webster settings.
- **Terminal:** optional, policy-controlled launch of a configured terminal with safe working directory; never provide an implicit elevated shell.
- **Properties:** inspect the selected item, with platform-provided values identified as such.
- **Administrative actions:** only for eligible targets, clearly marked, authorization-checked, and confirmed for consequential changes.

## Interaction Contract

Right-click or the platform's equivalent opens a menu anchored to the target and constrained to the work area. Keyboard context-menu key and Shift+F10 are supported; focus enters the menu, arrows navigate, Enter invokes, Escape closes and focus returns to the target. Touch/pen uses an appropriate long-press where supported. Menus expose accessible role/name/state, respect reduced motion and high contrast, dismiss on outside click, and do not obscure critical confirmation text.

Items are context-sensitive, deterministic and disabled with an explanation if unavailable. Destructive or privileged actions are not hidden in ambiguous submenus. Every action routes through a documented API and reports completion or error. Windows-provided commands are labeled and invoked through supported integration. See [Computer Management](../03-computer-management/computer-management.md).
