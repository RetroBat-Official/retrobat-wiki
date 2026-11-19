---
description: bstone
---

# Blake Stone

<div align="left"><figure><img src="../../../.gitbook/assets/image (642).png" alt="" width="450"><figcaption></figcaption></figure></div>

## Overview

**Blake Stone** (Apogee / JAM Productions) is a first-person shooter series on an engine derived from Wolfenstein 3D: **Aliens of Gold** (1993) and **Planet Strike** (1994).

RetroBat uses **BStone**, a modern engine: high resolution, widescreen, Vulkan or OpenGL rendering.

The game files are not provided: use the ones from your own copies (Steam, GOG) or the Aliens of Gold shareware version.

{% embed url="https://github.com/bibendovsky/bstone" %}

## At a glance

<table><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\bstone</code></td></tr><tr><td><strong>Extensions</strong></td><td>.bstone</td></tr><tr><td><strong>Default emulator</strong></td><td>bstone</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (player 1 controller, turned into keyboard keys)</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves, quick save / load with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## BIOS

No BIOS is needed. RetroBat recognizes the game from its files:

| Game                          | File extension        |
| ----------------------------- | --------------------- |
| Aliens of Gold (full version) | `.BS6` (`VSWAP.BS6`…) |
| Aliens of Gold (shareware)    | `.BS1` (`VSWAP.BS1`…) |
| Planet Strike                 | `.VSI` (`VSWAP.VSI`…) |

## Which game format?

An empty `.bstone` file placed in the folder of the game files starts this game. If a folder holds several games, the file name selects the game: `aog` or `alien` for Aliens of Gold, `ps` or `planet` for Planet Strike.

## Controls

### Automatic configuration

BStone does not read controllers: RetroBat turns the controller into keyboard keys (file `system\padtokey\bstone.keys`) and assigns these keys to the game actions.

<table><thead><tr><th width="335.25">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>D-pad, left stick</td><td>Move forward / back, turn</td></tr><tr><td>Right stick left / right</td><td>Strafe</td></tr><tr><td>R2</td><td>Fire</td></tr><tr><td>L2</td><td>Run</td></tr><tr><td>SOUTH</td><td>Use (open), "yes" in questions</td></tr><tr><td>EAST, START</td><td>Menu (Escape)</td></tr><tr><td>L1 / R1</td><td>Previous / next weapon</td></tr><tr><td>L3</td><td>Statistics</td></tr></tbody></table>

### Hotkeys

<table><thead><tr><th width="306.5">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr><tr><td>HOTKEY + WEST</td><td>Quick save</td></tr><tr><td>HOTKEY + NORTH</td><td>Quick load</td></tr><tr><td>HOTKEY + R3</td><td>Screenshot</td></tr></tbody></table>

See the **Hotkeys** page for more details.

## Folders

| Content                           | Folder               |
| --------------------------------- | -------------------- |
| Games                             | `roms\bstone\<game>` |
| Configuration, saves, screenshots | `emulators\bstone`   |

## Guides

### File layout

```
roms\bstone\
├── aog\
│   ├── aog.bstone        (empty file created for RetroBat)
│   ├── AUDIOHED.BS1
│   ├── AUDIOT.BS1
│   ├── IANIM.BS1
│   ├── JAMERR.EXE
│   ├── MAPHEAD.BS1
│   ├── MAPTEMP.BS1
│   ├── SANIM.BS1
│   ├── VGADICT.BS1
│   ├── VGAGRAPH.BS1
│   ├── VGAHEAD.BS1
│   └── VSWAP.BS1
└── ps\
    ├── ps.bstone         (empty file created for RetroBat)
    ├── AUDIOHED.VSI
    ├── AUDIOT.VSI
    ├── EANIM.VSI
    ├── IANIM.VSI
    ├── MAPHEAD.VSI
    ├── MAPTEMP.VSI
    ├── VGADICT.VSI
    ├── VGAGRAPH.VSI
    ├── VGAHEAD.VSI
    └── VSWAP.VSI
```

Example with the Aliens of Gold shareware version (`.BS1`); the files of the full version have the `.BS6` extension.

### Options

* **WIDESCREEN** (enabled by default) adapts the 3D view to widescreen displays; **STRETCH UI** also stretches the menus.
* **UPSCALE FILTER** (xBRZ) smooths the textures, **ADLIB EMULATION** selects the music emulation.
* **DRIVERS > VIDEO** on AUTOMATIC tries Vulkan, then OpenGL, then the software renderer.

## Known issues

| Issue                                                | Solution                                                   |
| ---------------------------------------------------- | ---------------------------------------------------------- |
| BStone shows a game selection window                 | The `.bstone` file is not in the folder of the game files. |
| Wrong game started in a folder that holds both games | Name the file `aog.bstone` or `ps.bstone`.                 |
