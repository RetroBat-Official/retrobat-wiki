---
description: tyrQuake
---

# Quake

<div align="left"><figure><img src="../../../.gitbook/assets/image (785).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**Quake** (id Software, 1996) is id Software's first fully 3D first-person shooter. It started online gaming and a very large mod scene, still active today.

This system runs **Quake**, its two official mission packs (**Scourge of Armagon** and **Dissolution of Eternity**), **Dimension of the Past** and mods (maps, episodes, conversions such as **Quoth**).

RetroBat offers the **tyrquake** libretro core (default) and **vkQuake**, a modern Vulkan engine.

Game files are not provided: use the ones from your own copy.

{% embed url="https://docs.libretro.com/library/tyrquake/" %}

{% embed url="https://github.com/Novum/vkQuake" %}

## At a glance

<table><thead><tr><th width="257.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\quake</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pak .quake</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: tyrquake</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (tyrquake core: 3 layouts; vkQuake: player 1 controller)</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves (vkQuake: quick save / load hotkeys)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="170.75">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: tyrquake</strong> (default)</td><td>Light, faithful rendering, three controller layouts, RetroArch hotkeys.</td><td>No save states. Rendering close to the original (internal resolution up to 1920x1200).</td></tr><tr><td><strong>vkquake</strong></td><td>Modern engine (Vulkan): high resolution, display refresh rate, improved effects, compatible with large recent mods. Quick save and load hotkeys.</td><td>One player only on the controller.</td></tr></tbody></table>

## BIOS

No BIOS is required. You need the game files instead:

<table><thead><tr><th width="328.25">Game</th><th width="133.25">Folder</th><th>Files</th></tr></thead><tbody><tr><td>Quake</td><td><code>id1</code></td><td><code>pak0.pak</code>, <code>pak1.pak</code> (<code>pak0.pak</code> alone = shareware version)</td></tr><tr><td>Scourge of Armagon (mission pack 1)</td><td><code>hipnotic</code></td><td><code>pak0.pak</code></td></tr><tr><td>Dissolution of Eternity (mission pack 2)</td><td><code>rogue</code></td><td><code>pak0.pak</code></td></tr><tr><td>Dimension of the Past</td><td><code>dopa</code></td><td><code>pak0.pak</code></td></tr></tbody></table>

The versions sold today (Steam, GOG) contain these files.

## Which game format?

<table><thead><tr><th width="175.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.pak</strong></td><td>Game data file. The game launched is the one of the file's folder (<code>id1</code>, <code>hipnotic</code>, <code>rogue</code>, mod…).</td></tr><tr><td><strong>.quake</strong></td><td>Launch file placed in <code>roms\quake</code>: it gives the folder of the game to launch (see <a href="quake.md#launch-files-.quake"><strong>Guides</strong></a>).</td></tr></tbody></table>

Recommended layout of `roms\quake`: the base game in `id1`, each mission pack or mod in its own folder, next to it.

```
roms\quake\
├── id1\
│   ├── pak0.pak
│   ├── pak1.pak
│   └── music\
│       ├── track02.ogg
│       └── ...
├── hipnotic\
│   ├── pak0.pak
│   └── music\
├── rogue\
│   ├── pak0.pak
│   └── music\
├── dopa\
│   └── pak0.pak
├── Quake.quake
└── Scourge of Armagon.quake
```

The music (CD tracks) goes as `.ogg` files in the `music` folder of each game (`track02.ogg`, `track03.ogg`…).

## Controls

### Automatic configuration

**tyrquake core**: **CONTROLS > CONTROLLER TYPE** selects the layout. In the three controller layouts, the left stick moves and the right stick looks around.

<table><thead><tr><th>Action</th><th width="170.25">CLASSIC GAMEPAD (default)</th><th width="186.25">ALT. CLASSIC GAMEPAD</th><th>MODERN GAMEPAD</th></tr></thead><tbody><tr><td>Fire</td><td>WEST</td><td>R1</td><td>R2</td></tr><tr><td>Jump</td><td>SOUTH</td><td>L1</td><td>L2</td></tr><tr><td>Next weapon</td><td>EAST</td><td>R2</td><td>R1</td></tr><tr><td>Previous weapon</td><td>—</td><td>R3</td><td>L1</td></tr><tr><td>D-pad left / right</td><td>Turn</td><td>Strafe</td><td>Strafe</td></tr><tr><td>D-pad up / down</td><td>Forward / back</td><td>Forward / back</td><td>Forward / back</td></tr><tr><td>Menu</td><td>START</td><td>START</td><td>START</td></tr></tbody></table>

KEYBOARD AND MOUSE plays with the keyboard and mouse: RetroBat then gives the whole keyboard to the game and captures the mouse. The `Scroll Lock` key gives the keyboard back to the RetroArch hotkeys.



**vkQuake**: RetroBat gives player 1's controller to the game (vkQuake reads only one controller). Default controls:

<table><thead><tr><th width="211.5">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Forward, back, strafe</td></tr><tr><td>Right stick</td><td>Look around</td></tr><tr><td>R2</td><td>Fire</td></tr><tr><td>L2</td><td>Jump</td></tr><tr><td>L1 / R1</td><td>Previous weapon / next weapon</td></tr><tr><td>START</td><td>Menu</td></tr><tr><td>SELECT</td><td>Scores</td></tr><tr><td>SOUTH / EAST</td><td>Confirm / back (menus)</td></tr></tbody></table>

Controls can be changed in the options of the vkQuake menu. **CONTROLS > INVERT Y AXIS** inverts looking up and down.

### Hotkeys

* **tyrquake core**: RetroArch hotkeys (fast forward, screenshots…), without save states: save from the game menu.
* **vkQuake**:

<table><thead><tr><th width="257.75">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr><tr><td>HOTKEY + WEST</td><td>Quick save</td></tr><tr><td>HOTKEY + NORTH</td><td>Quick load</td></tr><tr><td>HOTKEY + R3</td><td>Screenshot</td></tr></tbody></table>

For more details, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

| Content                                            | Folder                                                                                              |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Games and mods                                     | `roms\quake`                                                                                        |
| tyrquake core: saves and configuration             | <p><code>saves\quake\&#x3C;game folder></code></p><p>(for example <code>saves\quake\id1</code>)</p> |
| vkQuake: saves, game configuration and screenshots | `roms\quake\<game folder>`                                                                          |
| vkQuake: video configuration                       | `roms\quake\vkQuake.cfg`                                                                            |

`roms\quake\id1\retrobat.cfg` is rewritten by RetroBat at each vkQuake launch: do not edit it.

## Guides

### Launch a mission pack or a mod

Launch a `.pak` file of the game folder (for example `hipnotic\pak0.pak`): RetroBat launches the game of that folder. `hipnotic`, `rogue` and `quoth` are launched as mission packs (matching status bar), any other folder as a mod, on top of Quake.

A mod without a `.pak` file (loose files) is launched with a `.quake` file.

### Launch files (.quake)

A `.quake` file is a text file placed in `roms\quake`. It shows in the game list with its name.

* Its first line gives the game folder, for example `hipnotic`.
* If the file is empty, RetroBat launches the folder with the same name as the file (`dopa.quake` launches `dopa`).
* Older RetroBat files still work (name containing `scourge` or `hipnotic`: Scourge of Armagon; `dissolution` or `rogue`: Dissolution of Eternity; otherwise Quake).

<div align="left"><figure><img src="../../../.gitbook/assets/image (784).png" alt=""><figcaption></figcaption></figure></div>

With `.quake` files, the `.pak` files of the subfolders also show in the list: you can hide them in ES.

## Known issues

<table><thead><tr><th width="331.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Keyboard keys do not respond with the tyrquake core</td><td>Select <strong>CONTROLS > CONTROLLER TYPE > KEYBOARD AND MOUSE</strong>.</td></tr><tr><td>vkQuake ignores some settings (resolution, VSync)</td><td>The engine limits its command line to 255 characters: install RetroBat in a folder with a shorter path.</td></tr><tr><td>No music</td><td>Put the tracks as <code>.ogg</code> files in the <code>music</code> folder of the game.</td></tr><tr><td>With several controllers, vkQuake takes the wrong one</td><td>Two controllers of the same model cannot be told apart: vkQuake takes the first one found.</td></tr></tbody></table>
