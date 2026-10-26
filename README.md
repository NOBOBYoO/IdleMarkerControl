<p align="center">
  <img src="art/IdleMarkerControl.png" alt="Idle Marker Control" width="420">
</p>

<p align="center">
  <strong>Choose which idle markers your settlers use.</strong>
</p>

# Idle Marker Control

Idle Marker Control identifies the idle markers in a settlement and lets you toggle their state, so NPCs don't use the ones you turn off.

It is non-intrusive:

- No plugin (.esp).
- Markers are toggled with the game's own enable/disable on the existing marker references. No objects are moved, deleted, or permanently added; the only change saved is each marker's enabled/disabled state.
- Precombines and previs are not touched.
- Holograms are temporary display objects that exist only in workshop mode and are removed when you leave it.

Palette used by the Idle Marker Control UI and artwork:

| Role | Color | Hex |
| --- | --- | --- |
| Enabled / primary | Hologram Green | `#4CFF7A` |
| Accent | Signal Green | `#3DDC84` |
| Disabled | Red | `#FF4B4B` |
| Text | Light Grey | `#D6DDD9` |
| Secondary text | Grey | `#8A9490` |

## Features

- **Holograms in workshop mode**: a pose figure where a pose mesh exists, otherwise a generic beacon with a facing arrow. **Green** = enabled, **red** = disabled.
- **Toggle**: aim at a hologram and press **Interact** (**E** by default; the prompt follows your binding). **E** is left to the game while another menu that takes input is open (message boxes, scrap confirmation, Pip-Boy, terminals, crafting); HUD overlays from other mods don't count.
- **Hotkey**: tap **H** in workshop mode to hide or show all holograms. The shown / hidden state is remembered between sessions (can be turned off).
- **Status label**: a small Enabled/Disabled label near the top right of the screen in workshop mode. Position adjustable.
- **Settings panel** (PrismaUI F4, optional but recommended): hold **H** for 1 second, in or out of workshop mode. Marker count for the current settlement, hotkey rebinding, hold time, remembering the shown / hidden state, status label position, Interface scale (75–200%, for large and 4K screens), and reset to defaults. Changes apply immediately and are saved to `IdleMarkerControl.ini`.

## Requirements

- [Fallout 4 Script Extender (F4SE)](https://f4se.silverlock.org/)
- [Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327)
- Fallout 4 **1.10.163** (Old-Gen), **1.10.984** (Next-Gen), or **1.11.191+** (Anniversary Edition)
- [PrismaUI F4](https://www.nexusmods.com/fallout4/mods/105454) — **optional but recommended**. Adds the settings panel and PrismaUI labels. Without it, Idle Marker Control uses its own HUD labels and all settings are in `IdleMarkerControl.ini`.

## Installation

1. Install F4SE and Address Library for your game version. PrismaUI F4 is optional but recommended.
2. Install Idle Marker Control with Vortex or Mod Organizer 2 (or copy its `Data` folder into the game folder).
3. Launch the game through F4SE and enter workshop mode in a settlement.

## Usage

| Action | Where | Result |
| --- | --- | --- |
| Aim + **Interact** (E) | Workshop mode | Enable or disable the marker |
| Tap **H** | Workshop mode | Hide or show all holograms |
| Hold **H** 1 second | Anywhere (default) | Open the settings panel (PrismaUI F4) |
| Tap **H** / **Esc** / **Close** | Settings panel | Close it |

## Settings reference

`Data\F4SE\Plugins\IdleMarkerControl.ini`, section `[IdleMarkerControl]`. Keys are DirectInput scan codes (decimal or `0x` hex).

| Setting | Default | Meaning |
| --- | --- | --- |
| `FocusRadius` | `150` | Distance (game units) to focus a marker. |
| `ScanRadius` | `16384` | Scan distance from the workshop, for markers just outside the build area. |
| `ShowDisabled` | `true` | Keep a red hologram on disabled markers so they can be turned back on. |
| `OverlayScale` | `0.08` | Scale of the ground pad used when a pose mesh is missing. |
| `OverlayHeight` | `12` | Height offset of that pad. |
| `OverlayPoseScale` | `1.0` | Scale of pose holograms. |
| `OverlayPoseHeight` | `0` | Extra height offset for pose holograms. |
| `iToggleKey` | `0x23` (H) | Tap: show/hide holograms. Hold: settings panel. `0` = off. |
| `fSettingsHoldSeconds` | `1.0` | Hold time to open the settings panel (0.3–5). |
| `bSettingsAnywhere` | `1` | `1` = the hold also works outside workshop mode. |
| `bRememberHologramState` | `1` | Remember shown / hidden (the hotkey tap) between sessions, saved as `bHologramsVisible`. `0` = each session starts as `bShowOnStart` says. |
| `bShowOnStart` | `1` | Start state when not remembering, and on the first run: shown (`1`) or hidden (`0`). |
| `bShowStatusHud` | `1` | Show the status label in workshop mode. |
| `fStatusHudX` | `0.842` | Label horizontal position (fraction of screen width; right edge when right-aligned). |
| `fStatusHudY` | `0.080` | Label vertical position (fraction of screen height; top edge). |
| `bStatusHudRightAlign` | `1` | Right-align the label at `fStatusHudX`. |
| `UiScalePercent` | `100` | Interface scale, 75–200 in steps of 5. Scales the PrismaUI panel and label, and the built-in label's text. |
| `bUsePrismaUI` | `1` | Use PrismaUI F4 for the labels when installed. `0` = built-in labels; the settings panel still opens. |
| `sExtraAllowedMenus` | *(empty)* | Comma-separated menu names from other mods that should not block **E**. HUD overlays are already ignored. |
| `ShowNotification` | `false` | Unused. |
| `VerboseLogging` | `false` | Extra detail in `IdleMarkerControl.log` (each **E** press, menu checks, scan details). |

## Known limitations

- Some markers use the generic beacon because no pose mesh ships for them.
- The settings panel needs PrismaUI F4; otherwise use `IdleMarkerControl.ini`.
- Disabled markers are stored in your save. Re-enable them before uninstalling if you want them back.

## Troubleshooting

- No holograms: check that the game was launched through F4SE, Address Library matches your game version, and holograms aren't hidden (tap **H**).
- Holding **H** does nothing: PrismaUI F4 is missing.
- **E** does nothing while another mod's menu is open: add the menu name to `sExtraAllowedMenus`. With `VerboseLogging=true`, the log names the menu that blocked **E**.
- Log: `Documents\My Games\Fallout4\F4SE\IdleMarkerControl.log`. When reporting a problem, include your game version, mod version, this log, `f4se.log`, load order, and steps to reproduce.

## AI usage disclosure

AI tools are used during development for automation, debugging, image generation, and implementation support. Design decisions, feature direction, review, testing, and release responsibility remain under the author's supervision.

## Support

Support for continued development is welcome on Ko-fi.

<a href='https://ko-fi.com/Z7Z028MXCC' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi3.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

## Credits

- [Fallout 4 Script Extender (F4SE)](https://f4se.silverlock.org/) — Ian Patterson, Stephen Abel, and Brendan Borthwick
- [Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327) — meh321
- [PrismaUI F4](https://www.nexusmods.com/fallout4/mods/105454) — StarkMP; Fallout 4 port by NomadsReach / Fallen World
- [CommonLibF4 AV](https://github.com/LucaDotGit/CommonLibF4) — LucaDotGit; based on alandtse's CommonLibF4 NG and Ryan McKenzie's original CommonLibF4