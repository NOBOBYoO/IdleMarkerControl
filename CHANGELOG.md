# Changelog

## [1.0.0] - 2026-10-26

### ✨ Additions

- Paint, sink, dish-washing, map lean/stand, refugee, couple, radio-listen, screwdriver and primping markers, plus the Nuka-World paint-ghoul and fence-cheer markers, now use pose holograms instead of the generic beacon.
- Those markers now show clear prompt labels, even when their names are not available.

### 🔄 Changes

- Hologram colour (green enabled, red disabled) is now applied in-game per marker.
- Separate disabled meshes are gone, so the download is about half the size.
- Laser cutter markers now use the welding poses.
- Hologram meshes are cleaned up to a single shape each.
- PrismaUI views now wait until the runtime is ready, and the marker label no longer shows the cursor.

### 🛠️ Fixes

- Spouse wall-lean, prisoner floor-sit and radio floor-sit markers no longer show the wrong pose.
- Kneel-sit, praying, mortar and noodle holograms no longer render fainter than the rest.

## [0.2.0] - 2026-10-04

### ✨ Additions

- Hologram shown / hidden state is remembered between sessions (`bRememberHologramState`, also a switch in the settings panel).
- New ini key `sExtraAllowedMenus` for other mods' menus that block **E**.

### 🔄 Changes

- **E** and **H** are ignored while any other input menu is open (message boxes, scrap confirmation, Pip-Boy, terminals, crafting). HUD overlays from other mods don't count.
- The marker label hides while another menu is open on top of workshop mode.

### 🛠️ Fixes

- Fixed crashes when opening menus such as workbench crafting, terminals and the Pip-Boy.
- Fixed IMC overriding the game's input lock during crafting, terminal use and furniture use.
- Fixed holograms being built twice on entering workshop mode.
- Fixed the settings panel not opening with **Use PrismaUI for labels** turned off.

## [0.1.0] - 2026-09-26

- Initial release
