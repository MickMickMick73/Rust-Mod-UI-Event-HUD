# Rust Mod UI — Event HUD

Compact in-game overlay for Mix / Oxide. Same layout as a slim top-left info bar: menu well, five event wells, then players / scrap / time / grid.

Each event has a real **on** glyph (lit, on the map) and **off** glyph (cold, idle). Wells light rust-orange when armed.

Fan-made. No Facepunch IP. No letters baked into sprites.

## Layout

```
[☰]  [heli] [brad] [cargo] [drop] [ch47]   1   scrap   1:01 PM  H9
                                           MiX Server
```

- Inactive wells: `sprites/wells/off.png` + `icons/{id}-off.png`
- Active wells: `sprites/wells/on.png` + `icons/{id}-on.png`
- Hover: `sprites/wells/hover.png`
- Menu: `icons/burger.png` in an off well
- Optional framed tray: `sprites/frames/tray.png` (9-slice) if you want a metal rim instead of the slim CSS bar

## Drop-in

Unzip as `mix-event-hud/` next to `rust-ui.css`.

```html
<link rel="stylesheet" href="mix-event-hud.css" />
```

Swap ImageLibrary PNGs 1:1. CUI text sits beside the wells — never inside the sprites.

## Pack

| Asset | Path |
| --- | --- |
| On / off / hover wells | `sprites/wells/{on,off,hover,disabled}.png` |
| Event glyphs | `sprites/icons/{heli,brad,cargo,drop,ch47}-{on,off}.png` |
| Menu bars | `sprites/icons/burger.png` |
| Players / scrap / RP | `sprites/icons/{players,scrap,rp}.png` |
| Slim tray frame | `sprites/frames/tray.png` |
| Square plates (optional) | `sprites/tiles/{on,off,hover,disabled}.png` |
| Menu bar plate | `sprites/bar/menu.png` |
| World plate (catalog) | `textures/world.jpg` |

Repo: https://github.com/MickMickMick73/Rust-Mod-UI-Event-HUD
