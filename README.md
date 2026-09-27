<div align="center">

  <h1>Idle Marker Control</h1>

  <p>
    <strong>Choose which idle markers your settlers use.</strong><br>
    A small F4SE plugin for Fallout 4 settlements.
  </p>

  <p>
    <a href="https://github.com/NOBOBYoO/IdleMarkerControl/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/NOBOBYoO/IdleMarkerControl?style=for-the-badge&label=LATEST_RELEASE&labelColor=0C2306&color=5EEF84"></a>
    <a href="https://github.com/NOBOBYoO/IdleMarkerControl/releases"><img alt="Release downloads" src="https://img.shields.io/github/downloads/NOBOBYoO/IdleMarkerControl/total?style=for-the-badge&label=DOWNLOADS&labelColor=0C2306&color=33B450"></a>
  </p>

  <p>
    <a href="#overview">Overview</a> ·
    <a href="#features">Features</a> ·
    <a href="#controls">Controls</a> ·
    <a href="#settings-panel">Settings panel</a> ·
    <a href="#requirements">Requirements</a> ·
    <a href="#installation">Installation</a> ·
    <a href="#support-and-troubleshooting">Support</a>
  </p>
</div>

---

## Overview

Idle Marker Control identifies the idle markers in a settlement and lets you toggle their state, so NPCs don't use the ones you turn off.

It is non-intrusive:

- No plugin (.esp).
- Markers are toggled with the game's own enable/disable on the existing marker references. No objects are moved, deleted, or permanently added; the only change saved is each marker's enabled/disabled state.
- Precombines and previs are not touched.
- Holograms are temporary and exist only in workshop mode.

## Features

- **Holograms in workshop mode**: a pose figure where a pose mesh exists, otherwise a generic beacon with a facing arrow. **Green** = enabled, **red** = disabled.
- **Toggle**: aim at a hologram and press **Interact** (**E** by default).
- **Hotkey**: tap **H** in workshop mode to hide or show all holograms.
- **Status label**: a small Enabled/Disabled label near the top right of the screen in workshop mode.
- **Settings panel**: hold **H** for 1 second (PrismaUI F4, optional but recommended).

## Controls

| Action | Where | Result |
| --- | --- | --- |
| Aim + **Interact** (E) | Workshop mode | Enable or disable the marker |
| Tap **H** | Workshop mode | Hide or show all holograms |
| Hold **H** for 1 second | In or out of workshop mode | Open the settings panel |
| Tap **H**, **Esc**, or **Close** | Settings panel | Close the settings panel |

## Settings panel

Requires [PrismaUI F4](https://www.nexusmods.com/fallout4/mods/105454) (optional but recommended). Changes apply immediately and are saved to `IdleMarkerControl.ini`.

- Marker count for the current settlement, and a Show/Hide holograms button.
- Hotkey rebinding and hold time.
- Status label on/off, position and alignment.
- Interface scale 75–200%, for large and 4K screens.
- Reset to defaults.

Without PrismaUI F4, all settings are in `Data\F4SE\Plugins\IdleMarkerControl.ini`.

## Requirements

- [Fallout 4 Script Extender (F4SE)](https://f4se.silverlock.org/)
- [Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327)
- Fallout 4 **1.10.163** (Old-Gen), **1.10.984** (Next-Gen), or **1.11.191+** (Anniversary Edition)
- [PrismaUI F4](https://www.nexusmods.com/fallout4/mods/105454) – **optional but recommended** (settings panel and PrismaUI labels)

Use the file matching your game version for each requirement. No .esp is needed.

## Installation

1. Install F4SE and Address Library for your game version. PrismaUI F4 is optional but recommended.
2. Download `IdleMarkerControl-<version>.zip` from [Releases](https://github.com/NOBOBYoO/IdleMarkerControl/releases/latest).
3. Install it with Mod Organizer 2 or Vortex, or copy its `Data` folder into the Fallout 4 folder.
4. Launch the game through F4SE and enter workshop mode in a settlement.

## Known limitations

- Some markers use the generic beacon because no pose mesh ships for them.
- The settings panel needs PrismaUI F4; otherwise use `IdleMarkerControl.ini`.
- Disabled markers are stored in your save. Re-enable them before uninstalling if you want them back.

## Support and troubleshooting

- **No holograms:** check that the game was launched through F4SE, Address Library matches your game version, and holograms aren't hidden (tap **H**).
- **Holding H does nothing:** PrismaUI F4 is missing or `bUsePrismaUI=0`.
- **Log:** `Documents\My Games\Fallout4\F4SE\IdleMarkerControl.log`

When reporting a problem, include your game version, mod version, `IdleMarkerControl.log`, `f4se.log`, load order, and steps to reproduce.

## AI usage disclosure

AI tools are used during Idle Marker Control's development for **code, documentation, and artwork**, including automation, debugging, and implementation support. **The logo was AI-generated.**

Design decisions, feature direction, review, testing, and release responsibility remain under the author's supervision.

## Credits

- [Fallout 4 Script Extender (F4SE)](https://f4se.silverlock.org/) – Ian Patterson, Stephen Abel, and Brendan Borthwick
- [Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327) – meh321
- [PrismaUI F4](https://www.nexusmods.com/fallout4/mods/105454) – StarkMP; Fallout 4 port by NomadsReach / Fallen World
- [CommonLibF4 AV](https://github.com/LucaDotGit/CommonLibF4) – LucaDotGit; based on alandtse's CommonLibF4 NG and Ryan McKenzie's original CommonLibF4

## License

Copyright (c) 2026 NOBODY. All Rights Reserved. See [LICENSE](LICENSE).