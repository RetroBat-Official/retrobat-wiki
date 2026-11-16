---
description: Doom3
---

# Doom III

<div align="left"><figure><img src="../../../.gitbook/assets/image (598).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**Doom 3** (id Software, 2004) brings Doom's Mars base back as a shooter and horror game, with dynamic lighting and real-time shadows. Its expansion **Resurrection of Evil** (2005) adds a new campaign and new weapons.

RetroBat runs these games with two modern ports of the engine: the **boom3** libretro core (default) and **dhewm3**.

The game files are not provided: use the ones from your own copy (CD, Steam, GOG).

{% embed url="https://docs.libretro.com/library/boom3/" %}

{% embed url="https://dhewm3.org/" %}

## At a glance

<table><thead><tr><th width="231.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\doom3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.boom3 .game</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: boom3</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

| Emulator                      | Strengths                                                                                                                 | Limitations                                                                      |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **libretro: boom3** (default) | RetroArch hotkeys, OpenGL or Vulkan rendering, frame rates above 60 fps, also accepts unpatched data (1.0, 1.1).          | No mods in RetroBat. The core's controller layouts are less handy than dhewm3's. |
| **dhewm3**                    | Engine the core is based on, mods, controller set up like Doom 3 BFG, many options (quality, brightness, surround sound). | Requires game data patched to 1.3.1.                                             |

To change the emulator, for the whole system or for a single game, see the **Configuration of systems and games** page.

## BIOS

No BIOS is needed. You need the game files (`.pk4`) instead:

| Game                 | Folder            | Files                        |
| -------------------- | ----------------- | ---------------------------- |
| Doom 3               | `roms\doom3\base` | `pak000.pk4` to `pak008.pk4` |
| Resurrection of Evil | `roms\doom3\d3xp` | `pak000.pk4`, `pak001.pk4`   |

Resurrection of Evil also needs the Doom 3 `base` folder.

These files are in the game installation folder: CD patched to 1.3.1, or Steam and GOG releases ("DOOM 3", not "DOOM 3: BFG Edition"). dhewm3 requires version 1.3.1; the boom3 core also accepts unpatched CDs (1.0, 1.1).

## Which game format should I use?

| Format                 | Description                                                                                                                           |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **.boom3** / **.game** | Launch text file: its first line gives the path to the game's `pak000.pk4` (see [**Guides**](doom-iii.md#creating-the-launch-files)). |

`roms\doom3` layout:

```
roms\doom3\
├── Doom 3.boom3
├── Doom 3 - Resurrection of Evil.boom3
├── base\
│   ├── pak000.pk4
│   ├── …
│   └── pak008.pk4
└── d3xp\
    ├── pak000.pk4
    └── pak001.pk4
```

## Controls

### Automatic configuration

**dhewm3**: RetroBat binds the controller buttons after the Doom 3 BFG layout (dhewm3 `gamepad.cfg` and `gamepad-d3xp.cfg` files), with the PDA on NORTH.

<table><thead><tr><th width="256.5">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Move forward, backward, strafe</td></tr><tr><td>Right stick</td><td>Turn, look up and down</td></tr><tr><td>R2</td><td>Fire</td></tr><tr><td>L2</td><td>Flashlight</td></tr><tr><td>SOUTH</td><td>Jump</td></tr><tr><td>EAST</td><td>Crouch</td></tr><tr><td>WEST</td><td>Reload</td></tr><tr><td>NORTH</td><td>PDA</td></tr><tr><td>L1 / R1</td><td>Previous weapon / next weapon</td></tr><tr><td>L3</td><td>Run (hold)</td></tr><tr><td>R3</td><td>Crouch</td></tr><tr><td>D-pad: up / down / left / right</td><td>Grenades / BFG / Soul Cube / fists</td></tr><tr><td>START</td><td>Menu</td></tr></tbody></table>

For Resurrection of Evil, the D-pad and L2 follow the dhewm3 `gamepad-d3xp.cfg` layout (expansion weapons). The controls can be changed in the dhewm3 menu (**Settings > Controls**), but RetroBat rewrites the controller buttons at each launch: to keep your settings, set **AUTOCONFIGURE CONTROLLERS** to OFF.

**boom3 core**: **CONTROLS > CONTROLLER TYPE** selects the layout, GAMEPAD CLASSIC (default), GAMEPAD CLASSIC ALT or GAMEPAD MODERN. KEYBOARD AND MOUSE plays with keyboard and mouse.

<table><thead><tr><th width="155.25">RetroBat controller</th><th>Gamepad classic</th><th>Gamepad classic alt</th><th>Gamepad modern</th></tr></thead><tbody><tr><td>Left stick</td><td>Move forward, backward, strafe</td><td>Move forward, backward, strafe</td><td>Move forward, backward, strafe</td></tr><tr><td>Right stick</td><td>Look</td><td>Look</td><td>Look</td></tr><tr><td>D-pad</td><td>Move forward, backward, strafe</td><td>Move forward, backward, strafe</td><td>Move forward, backward, strafe</td></tr><tr><td>SOUTH</td><td>Jump</td><td>Look down</td><td>Crouch</td></tr><tr><td>EAST</td><td>Next weapon</td><td>Turn right</td><td>Strafe right</td></tr><tr><td>WEST</td><td>Fire</td><td>Turn left</td><td>Jump</td></tr><tr><td>NORTH</td><td>Free look (hold)</td><td>Look up</td><td>Strafe left</td></tr><tr><td>L1 / R1</td><td>Strafe left / right</td><td>Jump / fire</td><td>Previous / next weapon</td></tr><tr><td>L2 / R2</td><td>—</td><td>Run / next weapon</td><td>Jump / fire</td></tr><tr><td>L3</td><td>Crouch</td><td>Crouch</td><td>—</td></tr><tr><td>R3</td><td>PDA</td><td>Previous weapon</td><td>—</td></tr><tr><td>START</td><td>Menu</td><td>Menu</td><td>Menu</td></tr><tr><td>SELECT</td><td>PDA</td><td>PDA</td><td>PDA</td></tr></tbody></table>

### Hotkeys

* **dhewm3**:

<table><thead><tr><th width="255.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td><strong>HOTKEY + SOUTH</strong></td><td>Menu</td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Quick save</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Quick load</td></tr><tr><td><strong>HOTKEY + R3</strong></td><td>Screenshot</td></tr></tbody></table>

* **boom3 core**: RetroArch hotkeys (menu, fast forward, screenshot…), without save states. Saves go through the game menu, or the Doom 3 keys: `F5` quick save, `F9` quick load.

For more details, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="291.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\doom3</code></td></tr><tr><td>dhewm3: saves</td><td><code>saves\doom3\dhewm3\base\savegames</code> (Resurrection of Evil: <code>d3xp\savegames</code>)</td></tr><tr><td>dhewm3: screenshots (TGA format)</td><td><code>saves\doom3\dhewm3\base\screenshots</code></td></tr><tr><td>dhewm3: configuration</td><td><code>emulators\dhewm3\base\dhewm.cfg</code> (Resurrection of Evil: <code>d3xp\dhewm.cfg</code>)</td></tr><tr><td>boom3 core: saves</td><td><code>roms\doom3\base\savegames</code> (Resurrection of Evil: <code>d3xp\savegames</code>)</td></tr><tr><td>boom3 core: configuration</td><td><code>roms\doom3\base\dhewm.cfg</code></td></tr></tbody></table>

## Guides

### Creating the launch files

1. Copy the `base` and `d3xp` folders from the game installation folder to `roms\doom3`.
2. In `roms\doom3`, create a text file and rename it `Doom 3.boom3` (the `.txt` extension must go away).
3. Open it with Notepad and write on the first line: `base\pak000.pk4`.
4. For Resurrection of Evil, create `Doom 3 - Resurrection of Evil.boom3` the same way, with the line `d3xp\pak000.pk4`.

The file name is the one shown in the game list.

<div align="left"><figure><img src="../../../.gitbook/assets/image (599).png" alt=""><figcaption></figcaption></figure></div>

### Running a mod (dhewm3)

1. Put the mod folder in `roms\doom3`, next to `base` (for example `roms\doom3\sikkmod`).
2. Create a `.boom3` file whose first line starts with this folder name, for example `sikkmod\pak000.pk4`: RetroBat starts dhewm3 with this folder as the game (`fs_game`).
3. The next lines are added to the dhewm3 command line. For a Resurrection of Evil mod, add for example:

```
+set fs_game_base d3xp
```

Another example, to open the console and tune the mod:

```
+set com_allowconsole 1 +set g_gib_power 100
```

List of compatible mods: [dhewm3 mods](https://dhewm3.org/mods.html). Select **dhewm3** as the emulator for these games: with the boom3 core, RetroBat does not handle mods.

### Options worth knowing

* **dhewm3**: **SCREEN RESOLUTION** (desktop resolution by default), **VERTICAL SYNC**, **VIDEO > QUALITY**, **VISUAL RENDERING > ANTI-ALIASING (MSAA)**, **VISUAL RENDERING > BRIGHTNESS** (Doom 3 is a very dark game), **AUDIO > AUDIO CHANNELS** (STEREO or SURROUND), **AUDIO > ENABLE EAX**, **USER INTERFACE > HIDE HUD**, **USER INTERFACE > SHOW FPS**, **CONTROLS > ALWAYS RUN**, **CONTROLS > INVERT Y AXIS**, **CONTROLS > STICK DEADZONE**.
* **boom3 core**: **INTERNAL RESOLUTION** (1920x1080 by default), **VIDEO > QUALITY**, **VIDEO > FRAME RATE** (above 60, frames are interpolated), **CONTROLS > CONTROLLER TYPE**, **CONTROLS > INVERT Y AXIS**.

## Known issues

<table><thead><tr><th width="300.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start</td><td>Check the line of the <code>.boom3</code> file (<code>base\pak000.pk4</code> or <code>d3xp\pak000.pk4</code>) and where the <code>base</code> and <code>d3xp</code> folders are in <code>roms\doom3</code>.</td></tr><tr><td>Resurrection of Evil does not start</td><td>The Doom 3 <code>base</code> folder must be next to <code>d3xp</code>.</td></tr><tr><td>dhewm3 does not start with the files from a CD</td><td>dhewm3 requires version 1.3.1: install the official patch, or use the boom3 core.</td></tr><tr><td>Doom 3 BFG Edition does not work</td><td>This release is not supported: use the original one ("DOOM 3" on Steam, GOG).</td></tr><tr><td>The game is too dark</td><td>dhewm3: increase <strong>VISUAL RENDERING > BRIGHTNESS</strong>.</td></tr><tr><td>No save states</td><td>Save from the game menu, or with the quick save (see <a href="../../../navigation/hotkeys.md"><strong>Hotkeys</strong></a>).</td></tr><tr><td>A mod does not start</td><td>Use dhewm3; for a Resurrection of Evil mod, add <code>+set fs_game_base d3xp</code> to the <code>.boom3</code> file.</td></tr></tbody></table>
