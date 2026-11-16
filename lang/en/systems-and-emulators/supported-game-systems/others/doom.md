# Doom

<div align="left"><figure><img src="../../../.gitbook/assets/image (593).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

**Doom** (id Software, 1993) launched the first-person shooter on PC. Its engine was used by many other games and by thousands of player-made mods, still active today.

This system runs the games of that engine with modern engines: **Doom**, **The Ultimate Doom**, **Doom II**, **Final Doom** (TNT: Evilution, The Plutonia Experiment), **Heretic**, **Hexen**, **Strife**, **Chex Quest**, **Freedoom**, and mods (maps, episodes, total conversions such as **SIGIL** or **Brutal Doom**).

RetroBat offers **UZDoom** (default, successor of GZDoom), **GZDoom** and the **prboom** libretro core.

Game files are not provided: use the ones from your own copy, or **Freedoom**, a free game compatible with Doom mods.

{% embed url="https://github.com/UZDoom/uzdoom" %}

{% embed url="https://zdoom.org/index" %}

## At a glance

<table><thead><tr><th width="231.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\doom</code></td></tr><tr><td><strong>Extensions</strong></td><td>.wad .iwad .pwad .pk3 .ipk3 .gzdoom .uzdoom</td></tr><tr><td><strong>Default emulator</strong></td><td>uzdoom</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files required)</td></tr><tr><td><strong>Controller setup</strong></td><td>UZDoom and GZDoom default controls; automatic with the prboom core</td></tr><tr><td><strong>Save states</strong></td><td>prboom core; UZDoom and GZDoom: in-game saves</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="172">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>uzdoom</strong> (default)</td><td>The most complete: OpenGL or Vulkan rendering, high resolution, almost every mod (ZDoom formats, <code>.pk3</code>), Heretic, Hexen and Strife, controller recognized directly.</td><td>No save states: in-game saves, from its menu.</td></tr><tr><td><strong>gzdoom</strong></td><td>Previous version of the same engine.</td><td>Same limitations as UZDoom.</td></tr><tr><td><strong>libretro: prboom</strong></td><td>Rendering faithful to the original Doom, save states, RetroArch hotkeys, Boom, MBF and MBF21 mods.</td><td>Fewer compatible ZDoom mods.</td></tr></tbody></table>

## BIOS

No BIOS is needed. The game files (**IWAD**) are required:

<table><thead><tr><th width="285.25">Game</th><th>File</th></tr></thead><tbody><tr><td>Doom, The Ultimate Doom</td><td><code>doom.wad</code></td></tr><tr><td>Doom (free shareware version)</td><td><code>doom1.wad</code></td></tr><tr><td>Doom II</td><td><code>doom2.wad</code></td></tr><tr><td>Final Doom</td><td><code>tnt.wad</code>, <code>plutonia.wad</code></td></tr><tr><td>Heretic</td><td><code>heretic.wad</code></td></tr><tr><td>Hexen</td><td><code>hexen.wad</code> (expansion: <code>hexdd.wad</code>)</td></tr><tr><td>Strife</td><td><code>strife1.wad</code></td></tr><tr><td>Chex Quest</td><td><code>chex.wad</code></td></tr><tr><td>Freedoom (free)</td><td><code>freedoom1.wad</code>, <code>freedoom2.wad</code></td></tr></tbody></table>

The versions sold today (Steam, GOG, **Doom + Doom II** re-release) contain these files.

## Which game format?

<table><thead><tr><th width="190.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.wad</strong> / <strong>.iwad</strong></td><td>Full game (IWAD) or mod (PWAD).</td></tr><tr><td><strong>.pwad</strong></td><td>Mod: it needs the IWAD of the game (see <a href="doom.md#launching-a-mod-pwad"><strong>Guides</strong></a>).</td></tr><tr><td><strong>.pk3</strong> / <strong>.ipk3</strong></td><td>ZDoom-format mod (<code>.pk3</code>) or full game (<code>.ipk3</code>).</td></tr><tr><td><strong>.uzdoom</strong> / <strong>.gzdoom</strong></td><td>Launch file or folder: game and mods loaded together (see <a href="doom.md#loading-several-files-.uzdoom-.gzdoom"><strong>Guides</strong></a>).</td></tr></tbody></table>

Recommended layout of `roms\doom`: one folder per game, with its mods next to it or in a subfolder.

```
roms\doom\
├── Doom\
│   ├── doom.wad
│   └── SIGIL\
│       └── SIGIL.wad
└── Doom II\
    ├── doom2.wad
    └── Brutal Doom.uzdoom
```

## Controls

### Automatic setup

**UZDoom** recognizes the controller directly, with its default controls:

<table><thead><tr><th width="247.75">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Move forward, back, strafe</td></tr><tr><td>Right stick</td><td>Turn, look up and down</td></tr><tr><td>R2 / L2</td><td>Fire / alternate fire</td></tr><tr><td>SOUTH</td><td>Use (open a door, press a switch)</td></tr><tr><td>EAST</td><td>Crouch</td></tr><tr><td>WEST</td><td>Reload</td></tr><tr><td>NORTH</td><td>Jump</td></tr><tr><td>L1 / R1</td><td>Previous weapon / next weapon</td></tr><tr><td>R3</td><td>Zoom</td></tr><tr><td>D-pad: left / right / down</td><td>Previous item / next item / use item</td></tr><tr><td>START</td><td>Menu</td></tr><tr><td>SELECT</td><td>Map</td></tr></tbody></table>

Controls are changed in the UZDoom menu (**Options > Customize Controls**). With GZDoom, fewer buttons are mapped by default: complete them in the same menu.



**prboom core**: **CONTROLS > CONTROLLER TYPE** selects the layout, GAMEPAD CLASSIC (default, inspired by Doom on PlayStation) or GAMEPAD MODERN (sticks, inspired by Doom 3 on Xbox).

<table><thead><tr><th width="175.75">RetroBat controller</th><th width="216">Gamepad classic</th><th>Gamepad modern</th></tr></thead><tbody><tr><td>D-pad</td><td>Move</td><td>—</td></tr><tr><td>Left stick</td><td>—</td><td>Move forward, back, strafe</td></tr><tr><td>Right stick</td><td>—</td><td>Turn</td></tr><tr><td>NORTH</td><td>Fire</td><td>Previous weapon</td></tr><tr><td>EAST</td><td>Use</td><td>Next weapon</td></tr><tr><td>SOUTH</td><td>Strafe (hold)</td><td>Last message</td></tr><tr><td>WEST</td><td>Run</td><td>Use</td></tr><tr><td>L1 / R1</td><td>Strafe left / right</td><td>Quick load / quick save</td></tr><tr><td>L2 / R2</td><td>Previous / next weapon</td><td>Run / fire</td></tr><tr><td>L3</td><td>Run (toggle)</td><td>Run (toggle)</td></tr><tr><td>R3</td><td>180° turn</td><td>180° turn</td></tr><tr><td>START</td><td>Menu</td><td>Menu</td></tr><tr><td>SELECT</td><td>Map</td><td>Map</td></tr></tbody></table>

KEYBOARD/MOUSE plays with keyboard and mouse. **CONTROLS > ENABLE MOUSE** adds the mouse to the gamepad layouts.

### Hotkeys

* **UZDoom, GZDoom**: HOTKEY + START exits the game. Saves go through the game menu, or the Doom keys: `F2` save, `F3` load, `F6` quick save, `F9` quick load.
* **prboom core**: RetroArch hotkeys (save states, fast forward…).

For more details, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="307.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games and mods</td><td><code>roms\doom</code></td></tr><tr><td>UZDoom: saves</td><td><code>saves\uzdoom</code></td></tr><tr><td>GZDoom: saves</td><td><code>saves\gzdoom</code></td></tr><tr><td>prboom core: saves</td><td><code>saves\doom</code></td></tr><tr><td>prboom core: save states</td><td><code>saves\doom\libretro.prboom</code></td></tr><tr><td>UZDoom, GZDoom: screenshots</td><td><code>screenshots\uzdoom</code>, <code>screenshots\gzdoom</code></td></tr><tr><td>UZDoom, GZDoom: configuration</td><td><code>emulators\uzdoom\uzdoom_portable.ini</code>, <code>emulators\gzdoom\gzdoom_portable.ini</code></td></tr></tbody></table>

## Guides

### Launching a mod (PWAD)

Place the mod next to the game IWAD, or in a subfolder, then launch the mod from the game list. RetroBat looks for the IWAD from the mod maps (ExMy maps: Doom or Heretic; MAPxx: Doom II), in the mod folder then in the parent folders.

* **UZDoom, GZDoom**: when no IWAD is found, the emulator shows a window to choose it. Mods that name their own game (GAMEINFO lump) choose it by themselves.
* **prboom core**: it looks for the IWAD in the mod folder and its parent folders (**EMULATION > SEARCH IWAD IN PARENT FOLDERS**, on by default). For **SIGIL**, disable this option.

### Loading several files (.uzdoom, .gzdoom)

To launch a game with one or more mods, create a text file with the `.uzdoom` (or `.gzdoom`) extension in `roms\doom`. It shows up in the game list.

* One line: the game to launch, for example `doom2.wad`.
* Several lines: the UZDoom command line arguments, **one per line**. Paths are relative to the file folder. Lines starting with `#` are ignored.

```
-iwad
doom2.wad
-file
mods\brutalv22.pk3
-skill
3
```

Another option: a **folder** named with the `.uzdoom` extension (for example `Brutal Doom.uzdoom`), containing the IWAD and the mods. RetroBat loads the IWAD, then the mods in alphabetical order.

The prboom core also reads these files and folders: it only keeps the files (IWAD, WAD, PK3, DeHackEd patches) and ignores the other arguments.

<div align="left"><figure><img src="../../../.gitbook/assets/image (594).png" alt=""><figcaption></figcaption></figure></div>

### Useful options

* **UZDoom, GZDoom**: **DRIVERS > VIDEO** (OpenGL, Vulkan, OpenGL ES), **VISUAL RENDERING > RENDER MODE** (HARDWARE ACCELERATED, SOFTWARE), **EMULATION > COMPATIBILITY MODE** (for old mods and demos), **VISUAL RENDERING > VANILLA FRAMERATE** (35 frames per second), **CONTROLS > ALWAYS RUN** (on by default), **CONTROLS > SHOW CROSSHAIR**.
* **prboom core**: **INTERNAL RESOLUTION**, **EMULATION > COMPATIBILITY LEVEL** (MBF21 for mods that need it), **VISUAL RENDERING > COLOR DEPTH**, **EMULATION > WALL BULLET DECALS**.

## Known issues

<table><thead><tr><th width="354">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>UZDoom or GZDoom shows a window to choose the game</td><td>The IWAD was not found: place the mod next to the IWAD or in a subfolder, or use a <code>.uzdoom</code> file.</td></tr><tr><td>A mod does not work with the prboom core</td><td>It is made for ZDoom: use UZDoom.</td></tr><tr><td>SIGIL does not start with the prboom core</td><td>Disable <strong>EMULATION > SEARCH IWAD IN PARENT FOLDERS</strong> for that game.</td></tr><tr><td>A recent mod does not behave as expected with the prboom core</td><td>Set <strong>EMULATION > COMPATIBILITY LEVEL</strong> to MBF21.</td></tr><tr><td>An old mod or demo plays wrong with UZDoom</td><td>Try another <strong>EMULATION > COMPATIBILITY MODE</strong> (DOOM, BOOM, MBF).</td></tr></tbody></table>
