# Changelog

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