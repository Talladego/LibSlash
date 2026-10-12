# Changelog

## 3.0.3 (2026-10-12)

- `RegisterWSlashCmd` illegal-character debug message now matches `RegisterSlashCmd`
  (a-z, Russian alphabet, and 0-9), consistent with the shared pattern.

## 3.0.2 (2026-10-11)

- Run the upstream `_G` conflict scan once at init (not on every RegisterSlashCmd).
- Keep hash/scan helpers local; stop exposing a global `c`.
- `UnregisterSlashCmd` / `IsSlashCmdRegistered` lowercase input; unregister also clears `wslashCommands`.

## 3.0.1 (2026-10-11)

- Tail-call the stock `EA_ChatWindow.OnKeyEnter` for unregistered slash commands.
  Without this, LibSlash stays on the Lua stack and the client silently ignores
  `/assist` (and similar) when typed in chat.
- Maintained fork for Return of Reckoning; original LibSlash by Aiiane.

## 3.0.0 (2010-05-19)

- Upstream v3.0-release (Aiiane).
