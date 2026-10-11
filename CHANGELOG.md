# Changelog

## 3.0.1 (2026-10-11)

- Tail-call the stock `EA_ChatWindow.OnKeyEnter` for unregistered slash commands.
  Without this, LibSlash stays on the Lua stack and the client silently ignores
  `/assist` (and similar) when typed in chat.
- Maintained fork for Return of Reckoning; original LibSlash by Aiiane.

## 3.0.0 (2010-05-19)

- Upstream v3.0-release (Aiiane).
