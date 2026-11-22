---
description: ECWolf
---

# Wolfenstein 3D

<div align="left"><figure><img src="../../../.gitbook/assets/image (677).png" alt="" width="479"><figcaption></figcaption></figure></div>

## Overview

**Wolfenstein 3D** (id Software, 1992) is the founding game of the first-person shooter. RetroBat runs it with the **ECWolf** libretro core, which also runs **Spear of Destiny** and its missions, and the shareware version.

ECWolf brings high resolution, widescreen and play with a controller or keyboard and mouse.

The game files are not provided: use the ones from your own copies (Steam, GOG) or the shareware version.

{% embed url="https://docs.libretro.com/library/ecwolf/" %}

## At a glance

<table><thead><tr><th width="241.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\ecwolf</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pk3 .exe</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: ecwolf</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (controller, or keyboard and mouse)</td></tr><tr><td><strong>Save states</strong></td><td>Yes</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## BIOS

No BIOS is needed: the engine data (`ecwolf.pk3`) is built into the core.

You need the game files:

<table><thead><tr><th width="287.75">Game</th><th>File extension</th></tr></thead><tbody><tr><td>Wolfenstein 3D</td><td><code>.WL6</code></td></tr><tr><td>Wolfenstein 3D (shareware)</td><td><code>.WL1</code></td></tr><tr><td>Spear of Destiny</td><td><code>.SOD</code></td></tr><tr><td>Spear of Destiny (demo)</td><td><code>.SDM</code></td></tr><tr><td>Super 3-D Noah's Ark</td><td><code>.N3D</code></td></tr></tbody></table>

## Which game format?

<table><thead><tr><th width="112.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.exe</strong></td><td>DOS executable of the game (<code>WOLF3D.EXE</code>, <code>SPEAR.EXE</code>): the core runs the game of the file's folder.</td></tr><tr><td><strong>.pk3</strong></td><td>Mod in ECWolf format.</td></tr></tbody></table>

Put each game in its own folder of `roms\ecwolf`.

## Controls

### Automatic configuration

<table><thead><tr><th width="206.5">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Move forward / back, strafe</td></tr><tr><td>Right stick</td><td>Turn</td></tr><tr><td>D-pad</td><td>Move forward / back, turn</td></tr><tr><td>EAST</td><td>Fire</td></tr><tr><td>SOUTH</td><td>Use (open doors)</td></tr><tr><td>NORTH</td><td>Run (hold)</td></tr><tr><td>WEST</td><td>Show the status bar</td></tr><tr><td>L1 / R1</td><td>Strafe left / right</td></tr><tr><td>L2 / R2</td><td>Previous / next weapon</td></tr><tr><td>SELECT</td><td>Map</td></tr><tr><td>START</td><td>Menu</td></tr></tbody></table>

Useful options: **CONTROLS > ALWAYS RUN** (NORTH then walks), **ANALOG DEADZONE(CORE)**, **ANALOG SENSITIVITY(CORE)**.

### Keyboard and mouse

Keyboard and mouse work together with the controller. **CONTROLS > KEYBOARD AND MOUSE** gives the whole keyboard to the game and grabs the mouse: the `Scroll Lock` key gives the keyboard back to the RetroArch hotkeys. **CONTROLS > MOUSE SENSITIVITY** sets the turn speed (10 by default).

<table><thead><tr><th width="264">Keyboard / mouse</th><th>Action</th></tr></thead><tbody><tr><td>Up / down arrows, W / S</td><td>Move forward / back</td></tr><tr><td>Left / right arrows</td><td>Turn</td></tr><tr><td>A / D (or <code>,</code> / <code>.</code>)</td><td>Strafe</td></tr><tr><td>Mouse</td><td>Turn</td></tr><tr><td>Ctrl, Enter, left click</td><td>Fire</td></tr><tr><td>Space, right click</td><td>Use (open doors)</td></tr><tr><td>Shift</td><td>Run</td></tr><tr><td><code>[</code> / <code>]</code></td><td>Previous / next weapon</td></tr><tr><td>Tab</td><td>Map</td></tr><tr><td>Escape</td><td>Menu</td></tr></tbody></table>

### Hotkeys

RetroArch hotkeys, save states included. See the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="294">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\ecwolf\&#x3C;game></code></td></tr><tr><td>In-game saves and save states</td><td><code>saves\ecwolf</code></td></tr></tbody></table>

## Guides

### File layout

```
roms\ecwolf\
├── Wolfenstein 3D\
│   ├── WOLF3D.EXE
│   ├── AUDIOHED.WL6
│   ├── AUDIOT.WL6
│   ├── GAMEMAPS.WL6
│   ├── MAPHEAD.WL6
│   ├── VGADICT.WL6
│   ├── VGAGRAPH.WL6
│   ├── VGAHEAD.WL6
│   └── VSWAP.WL6
└── Spear of Destiny\
    ├── SPEAR.EXE
    └── *.SOD
```

### Options

* **INTERNAL RESOLUTION** up to 2560x1600, **VIDEO > REFRESH RATE (FPS)** up to 240 frames per second.
* **VIDEO > GAME ASPECT RATIO (CORE)** sets the picture when **GAME ASPECT RATIO** is on AUTO.

## Known issues

<table><thead><tr><th width="296.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The core does not find the game</td><td>The <code>.WL6</code> / <code>.SOD</code> files must be in the same folder as the launched file.</td></tr></tbody></table>
