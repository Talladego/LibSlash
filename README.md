# LibSlash 3.0.2 (RoR assist fix)

Fork of **LibSlash** (Aiiane) for [Return of Reckoning](https://www.returnofreckoning.com/).

## Why this fork

Stock LibSlash wraps `EA_ChatWindow.OnKeyEnter`. If it does not **tail-call** the
original handler for unregistered commands, the client ignores typed `/assist`
(portrait Assist still works). Nearly every RoR UI stack loads LibSlash.

## Fix

For commands that are not registered with LibSlash:

```lua
return origOnKeyEnter(...)
```

Registered slash handlers still run as before.

## Install

1. Copy the `LibSlash` folder into `Interface\AddOns\`.
2. Enable **LibSlash** in the addon list (many addons depend on it).
3. `/reloadui` and test typed `/assist PlayerName`.

## Related

- Hotbar `/assist` can still fail if other addons call Lua during the click
  (e.g. older GCDsaver / CustomUI / StockPiler3 click wrappers).
- Upstream listing: https://tools.idrinth.de/addons/libslash/
- Community reports: https://forums.returnofreckoning.com/viewtopic.php?t=60710

## Credits

Original author: **Aiiane**. Assist tail-call maintenance: Talladego.
