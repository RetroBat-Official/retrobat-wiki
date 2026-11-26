---
description: eduke32
---

# Duke Nukem 3D

<div align="left"><figure><img src="../../../.gitbook/assets/image (741).png" alt=""><figcaption></figcaption></figure></div>

## Overview

**Duke Nukem 3D** (3D Realms, 1996) is a first-person shooter on the Build engine, famous for its humor and interactive levels.

This system runs Duke Nukem 3D, its add-ons (**Duke It Out in D.C.**, **Duke Caribbean: Life's a Beach**, **Duke: Nuclear Winter**, **Penthouse Paradise**) and mods.

RetroBat offers **eduke32** (default) and **Raze**, a modern engine that also runs the other Build games (see the [**Raze**](raze.md) page).

The game files are not provided: use the ones from your own copy (Steam, GOG, CD).

{% embed url="http://www.eduke32.com/" %}

## At a glance

<table><thead><tr><th width="236.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\eduke32</code></td></tr><tr><td><strong>Extensions</strong></td><td>.eduke32</td></tr><tr><td><strong>Default emulator</strong></td><td>eduke32</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (player 1 controller)</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves, quick save / load with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="185.75">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>eduke32</strong> (default)</td><td>Reference Duke Nukem 3D engine, original software renderer or OpenGL (HD packs), very compatible with mods.</td><td>Duke Nukem 3D only.</td></tr><tr><td><strong>raze</strong></td><td>Modern engine (OpenGL / Vulkan), same <code>.eduke32</code> launch files.</td><td>Fewer compatible mods.</td></tr></tbody></table>

## BIOS

No BIOS is needed. You need the files of your game, for example in `roms\eduke32\duke`:

| Game                            | Files                             |
| ------------------------------- | --------------------------------- |
| Duke Nukem 3D (Atomic Edition)  | `DUKE3D.GRP` (and `DUKE.RTS`)     |
| Duke It Out in D.C.             | `DUKEDC.GRP`                      |
| Duke Caribbean: Life's a Beach  | `VACATION.GRP`                    |
| Duke: Nuclear Winter            | `NWINTER.GRP`                     |
| Duke Nukem's Penthouse Paradise | `PENTHOUS.GRP` and its `GAME.CON` |

## Which game format?

A game is launched with a `.eduke32` text file placed in `roms\eduke32`. It lists the files to load, one parameter per line. A path starting with `/` or `\` starts from the folder of the `.eduke32` file.

<table><thead><tr><th width="135.75">Parameter</th><th>Role</th><th>Equivalent</th></tr></thead><tbody><tr><td><code>FILE</code></td><td>Main game file (<code>.grp</code>, <code>.zip</code>)</td><td><code>-gamegrp</code></td></tr><tr><td><code>FILE+</code></td><td>Added file (add-on, mod)</td><td><code>-g</code></td></tr><tr><td><code>CON</code></td><td>Main script</td><td><code>-x</code></td></tr><tr><td><code>CON+</code></td><td>Added script</td><td><code>-mx</code></td></tr><tr><td><code>DEF</code></td><td>Main definitions file</td><td><code>-h</code></td></tr><tr><td><code>DEF+</code></td><td>Added definitions file</td><td><code>-mh</code></td></tr><tr><td><code>DIR</code></td><td>Search folder</td><td><code>-j</code></td></tr><tr><td><code>MAP</code></td><td>Map to start</td><td><code>-map</code></td></tr></tbody></table>

`FILE`, `CON`, `DEF` and `MAP` are only read once; `FILE+`, `CON+`, `DEF+` and `DIR` can be repeated.

## Controls

### Automatic configuration

RetroBat configures the player 1 controller (eduke32 only uses one):

<table><thead><tr><th width="227.75">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Move forward / back, strafe</td></tr><tr><td>Right stick</td><td>Turn, look up / down</td></tr><tr><td>R2</td><td>Fire</td></tr><tr><td>L2</td><td>Jump</td></tr><tr><td>SOUTH</td><td>Open / use</td></tr><tr><td>EAST / WEST</td><td>Inventory (use item)</td></tr><tr><td>NORTH</td><td>Quick kick</td></tr><tr><td>L1</td><td>Crouch (hold)</td></tr><tr><td>R1</td><td>Alternate fire</td></tr><tr><td>L3</td><td>Run</td></tr><tr><td>R3</td><td>Crouch (toggle)</td></tr><tr><td>D-pad left / right</td><td>Previous / next inventory item</td></tr><tr><td>D-pad up / down</td><td>Previous / next weapon</td></tr><tr><td>START</td><td>Menu</td></tr></tbody></table>

SELECT stays free for the RetroBat hotkeys. Useful options: **CONTROLS > INVERT Y AXIS**, **STICK DEADZONE**, **ALWAYS RUN** (enabled by default), **AUTO AIM**.

### Hotkeys

<table><thead><tr><th width="225.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr><tr><td>HOTKEY + SOUTH</td><td>Menu (Escape)</td></tr><tr><td>HOTKEY + WEST</td><td>Quick save</td></tr><tr><td>HOTKEY + NORTH</td><td>Quick load</td></tr><tr><td>HOTKEY + R3</td><td>Screenshot</td></tr></tbody></table>

See the [**Hotkeys**](../../../navigation/hotkeys.md) page for more details.

## Folders

<table><thead><tr><th width="305.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games and launch files</td><td><code>roms\eduke32</code></td></tr><tr><td>HD packs, sounds and mods loaded automatically</td><td><code>roms\eduke32\autoload</code></td></tr><tr><td>Configuration</td><td><code>emulators\eduke32\eduke32.cfg</code>, <code>emulators\eduke32\settings.cfg</code></td></tr></tbody></table>

## Guides

### .eduke32 file examples

With this layout:

```
roms\eduke32\
├── duke\
│   ├── DUKE3D.GRP
│   ├── DUKE.RTS
│   ├── DUKEDC.GRP
│   ├── VACATION.GRP
│   ├── NWINTER.GRP
│   ├── PENTHOUS.GRP
│   └── GAME.CON      (the Penthouse Paradise one)
├── Duke Nukem 3D.eduke32
└── Duke It Out in D.C..eduke32
```

**Duke Nukem 3D**

```
FILE = /duke/DUKE3D.GRP
```

**Duke It Out in D.C.** (same with `VACATION.GRP` or `NWINTER.GRP`)

```
FILE = /duke/DUKE3D.GRP
FILE+ = /duke/DUKEDC.GRP
```

**Duke Nukem's Penthouse Paradise**

```
FILE = /duke/DUKE3D.GRP
FILE+ = /duke/PENTHOUS.GRP
CON = /duke/GAME.CON
```

### HD packs

Put the packs (HD textures, sounds, 3D models) in `roms\eduke32\autoload`, then enable **EMULATION > AUTOLOAD CONTENT**:

<div align="left"><figure><img src="../../../.gitbook/assets/image (743).png" alt=""><figcaption></figcaption></figure></div>

Example:

<div align="left"><figure><img src="../../../.gitbook/assets/image (742).png" alt=""><figcaption></figcaption></figure></div>

HD textures and 3D models need an OpenGL renderer: **VIDEO > RENDERER** on POLYMOST or POLYMER.

### Music

**AUDIO > MIDI OUTPUT** on SOUNDFONT uses the Roland SC-55 bank shipped with RetroBat (`bios\scummvm\extra\Roland_SC-55.sf2`). Without this file, the music goes back to OPL3 emulation.

## Known issues

<table><thead><tr><th width="326.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start or shows the game selection screen</td><td>Check the paths in the <code>.eduke32</code> file (they start from the file's folder).</td></tr><tr><td>HD packs are not displayed</td><td>Enable <strong>AUTOLOAD CONTENT</strong> and set the renderer to POLYMOST or POLYMER.</td></tr><tr><td>The bezel is not displayed</td><td>It is only displayed in borderless fullscreen, without a forced resolution.</td></tr></tbody></table>
