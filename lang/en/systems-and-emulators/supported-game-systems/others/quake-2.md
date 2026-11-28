---
description: vitaQuake II
---

# Quake 2

<div align="left"><figure><img src="../../../.gitbook/assets/image (786).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**Quake II** (id Software, 1997) is the sequel to Quake: a science-fiction campaign against the Strogg, with interconnected levels and a multiplayer mode that became a reference.

This system runs **Quake II**, its mission packs (**The Reckoning**, **Ground Zero**), **Zaero**, **Capture The Flag** and mods.

RetroBat offers the **vitaquake2** libretro core (default) and **vkQuake2**, a Vulkan engine.

Game files are not provided: use the ones from your own copy.

{% embed url="https://github.com/libretro/vitaquake2" %}

{% embed url="https://github.com/kondrak/vkQuake2" %}

## At a glance

<table><thead><tr><th width="219"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\quake2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pak .quake2</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: vitaquake2</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic with the vitaquake2 core; vkQuake2: keyboard and mouse</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves (vkQuake2: quick save / load hotkeys)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="184.5">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: vitaquake2</strong> (default)</td><td>Controller configured, menus included; RetroArch hotkeys; RetroBat picks the mission pack core by itself (The Reckoning, Ground Zero, Zaero).</td><td>No save states. Base game and these three packs only: no Capture The Flag and no mods.</td></tr><tr><td><strong>vkquake2</strong></td><td>Vulkan rendering, every mission pack and mod. Quick save and load hotkeys.</td><td>Made for keyboard and mouse: the controller has no default controls and the menus cannot be used with the controller.</td></tr></tbody></table>

## BIOS

No BIOS is required. You need the game files instead:

<table><thead><tr><th>Game</th><th width="134.5">Folder</th><th>Files</th></tr></thead><tbody><tr><td>Quake II</td><td><code>baseq2</code></td><td><code>pak0.pak</code>, <code>pak1.pak</code>, <code>pak2.pak</code></td></tr><tr><td>The Reckoning (mission pack 1)</td><td><code>xatrix</code></td><td><code>pak0.pak</code></td></tr><tr><td>Ground Zero (mission pack 2)</td><td><code>rogue</code></td><td><code>pak0.pak</code></td></tr><tr><td>Zaero</td><td><code>zaero</code></td><td><code>pak0.pak</code></td></tr><tr><td>Capture The Flag</td><td><code>ctf</code></td><td><code>pak0.pak</code></td></tr></tbody></table>

The versions sold today (Steam, GOG) contain these files.

## Which game format?

<table><thead><tr><th width="161.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.pak</strong></td><td>Game data file. The game launched is the one of the file's folder (<code>baseq2</code>, <code>xatrix</code>, <code>rogue</code>, mod…).</td></tr><tr><td><strong>.quake2</strong></td><td>Launch file placed in <code>roms\quake2</code>: it gives the folder of the game to launch (see <a href="quake-2.md#launch-files-.quake2"><strong>Guides</strong></a>).</td></tr></tbody></table>

Recommended layout of `roms\quake2`: the base game in `baseq2`, each mission pack or mod in its own folder, next to it.

```
roms\quake2\
├── baseq2\
│   ├── pak0.pak
│   ├── pak1.pak
│   ├── pak2.pak
│   ├── music\
│   │   ├── track02.ogg
│   │   └── ...
│   ├── video\
│   └── players\
├── xatrix\
│   ├── pak0.pak
│   └── video\
├── rogue\
│   ├── pak0.pak
│   └── video\
├── zaero\
│   └── pak0.pak
├── ctf\
│   └── pak0.pak
└── Quake II.quake2
```

The music (CD tracks) goes as `.ogg` files in the `music` folder of each game (`track02.ogg`, `track03.ogg`…).

## Controls

### Automatic configuration

**vitaquake2 core**: the controller is configured automatically.

<table><thead><tr><th width="244">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Forward, back, strafe</td></tr><tr><td>Right stick</td><td>Look around</td></tr><tr><td>R2</td><td>Fire</td></tr><tr><td>L2</td><td>Jump, move up</td></tr><tr><td>R1</td><td>Crouch, move down</td></tr><tr><td>L1</td><td>Run</td></tr><tr><td>WEST</td><td>Next weapon</td></tr><tr><td>D-pad left / right</td><td>Open the inventory / use the item</td></tr><tr><td>D-pad up / down</td><td>Previous / next item</td></tr><tr><td>R3</td><td>Drop the item</td></tr><tr><td>SELECT</td><td>Help computer</td></tr><tr><td>START</td><td>Menu</td></tr><tr><td>EAST / SOUTH</td><td>Confirm / back (menus)</td></tr></tbody></table>

* **CONTROLS > CONTROLLER TYPE > KEYBOARD/MOUSE** plays with the keyboard and mouse: RetroBat then gives the whole keyboard to the game and captures the mouse. The `Scroll Lock` key gives the keyboard back to the RetroArch hotkeys.
* **CONTROLS > INVERT VERTICAL AXIS** inverts looking up and down.
* **CONTROLS > MOUSE SENSITIVITY** sets the camera speed, with the right stick as with the mouse.

**vkQuake2**: play with the keyboard and mouse. **CONTROLS > USE JOYSTICK** enables the controller, but vkQuake2 only uses the first controller found by Windows, with no button assigned: buttons must be bound in the game menu (**Options > Customize Controls**), with the keyboard. In the game menus, every controller button confirms.

### Hotkeys

* **vitaquake2 core**: RetroArch hotkeys (fast forward, screenshots…), without save states: save from the game menu.
* **vkQuake2**:

<table><thead><tr><th width="221.5">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr><tr><td>HOTKEY + WEST</td><td>Quick save</td></tr><tr><td>HOTKEY + NORTH</td><td>Quick load</td></tr><tr><td>HOTKEY + R3</td><td>Screenshot</td></tr></tbody></table>

For more details, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="344">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games and mods</td><td><code>roms\quake2</code></td></tr><tr><td>vitaquake2 core: saves and configuration</td><td><p><code>saves\quake2\&#x3C;game folder></code></p><p>(for example <code>saves\quake2\baseq2</code>)</p></td></tr><tr><td>vkQuake2: saves</td><td><code>roms\quake2\&#x3C;game folder>\save</code></td></tr><tr><td>vkQuake2: configuration</td><td><code>roms\quake2\baseq2\config.cfg</code> (or the <code>config.cfg</code> of the mission pack folder, if it exists)</td></tr><tr><td>vkQuake2: screenshots</td><td><code>roms\quake2\&#x3C;game folder>\scrnshot</code></td></tr></tbody></table>

## Guides

### Launch a mission pack or a mod

Launch a `.pak` file of the game folder (for example `xatrix\pak0.pak`): RetroBat launches the game of that folder.

* **vitaquake2 core**: there is one core per game (vitaquake2, vitaquake2-xatrix, vitaquake2-rogue, vitaquake2-zaero). RetroBat picks the right one from the folder by itself: keep the **vitaquake2** core. Capture The Flag (`ctf`), other packs and mods are not supported: RetroBat shows a message, launch them with vkquake2.
* **vkQuake2**: every folder is accepted. Each game needs its library (`gamex64.dll`) in its folder: RetroBat copies the one provided with vkQuake2 when it is missing (base game and mission packs). A mod must provide its own.

### Launch files (.quake2)

A `.quake2` file is a text file placed in `roms\quake2`. It shows in the game list with its name.

* Its first line gives the game folder, for example `xatrix`.
* If the file is empty, RetroBat launches the folder with the same name as the file (`zaero.quake2` launches `zaero`).
* Older RetroBat files still work (name containing `rogue`, `xatrix` or `zaero`; otherwise Quake II).

<div align="left"><figure><img src="../../../.gitbook/assets/image (787).png" alt=""><figcaption></figcaption></figure></div>

### Useful options

* **vitaquake2 core**: **DRIVERS > VIDEO CORE RENDERER** (OPENGL by default, or SOFTWARE). The internal resolutions marked OPENGL ONLY need the OpenGL renderer.

## Known issues

<table><thead><tr><th width="340.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>"vitaQuake II does not support the game folder" message</td><td>This folder (Capture The Flag, mod) is not supported by the core: select the vkquake2 emulator for this game.</td></tr><tr><td>The controller does nothing with vkQuake2</td><td>Enable <strong>CONTROLS > USE JOYSTICK</strong> and bind the buttons in the game menu, or use the vitaquake2 core.</td></tr><tr><td>A mod does not start with vkQuake2</td><td>It needs its own <code>gamex64.dll</code> (64-bit version) in its folder.</td></tr><tr><td>No music</td><td>Put the tracks as <code>.ogg</code> files in the <code>music</code> folder of the game.</td></tr></tbody></table>
