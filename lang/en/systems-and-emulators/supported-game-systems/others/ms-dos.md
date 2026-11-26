---
description: Microsoft
---

# DOS

<div align="left"><figure><img src="../../../.gitbook/assets/image (739).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**MS-DOS** is the operating system of IBM-compatible PCs from 1981 to the mid-1990s, before Windows 95. Thousands of games were released for DOS: **Doom**, **Prince of Persia**, **Lemmings**, **Monkey Island**, **Day of the Tentacle**, **X-COM**, **Commander Keen**, **Duke Nukem 3D**, **Dune II**, **Alone in the Dark**…

Every PC was different: processor, graphics card (CGA, EGA, VGA, SVGA), sound card (Sound Blaster, AdLib, Gravis Ultrasound, Roland MT-32). DOSBox emulators reproduce this hardware. Most games are played with the keyboard and mouse; some accept a joystick.

RetroBat offers four emulators, all based on DOSBox: the **dosbox\_pure** libretro core (default), standalone **DOSBox Pure**, **DOSBox Staging** and **DOSBox**.

{% embed url="https://en.wikipedia.org/wiki/MS-DOS" %}

## At a glance

<table><thead><tr><th width="221.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\dos</code></td></tr><tr><td><strong>Extensions</strong></td><td>.dosbox .pc .dos .dosz .zip .m3u8 .bat</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: dosbox_pure</td></tr><tr><td><strong>BIOS</strong></td><td>None (optional MT-32 ROMs)</td></tr><tr><td><strong>Controller setup</strong></td><td>DOSBox Pure automatic mapping (core and standalone); DOS joystick or pad2key with DOSBox Staging and DOSBox</td></tr><tr><td><strong>Save states</strong></td><td>dosbox_pure core; DOSBox Pure with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="197">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: dosbox_pure</strong> (default)</td><td>Reads <code>.zip</code> games without extracting them, start menu usable with a controller, automatic controller mapping for many games, on-screen keyboard, save states, RetroArch shaders and bezels.</td><td>—</td></tr><tr><td><strong>dosbox-pure</strong></td><td>The same engine as a standalone program, with its own menu.</td><td>Save states with hotkeys, not managed by RetroBat.</td></tr><tr><td><strong>dosbox-staging</strong></td><td>Modern and very accurate DOSBox: CRT shaders, 3dfx Voodoo, many sound cards, fine CPU settings.</td><td>No save states. No automatic controller mapping. Does not read <code>.dosz</code>.</td></tr><tr><td><strong>dosbox</strong></td><td>The original DOSBox 0.74.</td><td>Only starts game folders (see <a href="ms-dos.md#which-game-format-should-i-use"><strong>Which game format should I use?</strong></a>). Few settings.</td></tr></tbody></table>

**If in doubt, keep libretro: dosbox\_pure.**

## BIOS

No BIOS is needed.

For MIDI music, RetroBat provides the `Roland_SC-55.sf2` sound bank in `bios\scummvm\extra`. You can add to the same folder:

| File                               | Used for                                  | Checked by RetroBat |
| ---------------------------------- | ----------------------------------------- | ------------------- |
| `MT32_CONTROL.ROM`, `MT32_PCM.ROM` | Roland MT-32 (Sierra, LucasArts, Origin…) | Yes (optional)      |
| `Roland_SC-88.sf2`                 | Roland SC-88                              | No                  |

These files are shared with ScummVM. Choose the device with **AUDIO > MIDI OUTPUT**.

## Which game format should I use?

| Format                              | dosbox\_pure (core, standalone) | dosbox-staging                      | dosbox |
| ----------------------------------- | ------------------------------- | ----------------------------------- | ------ |
| **.zip**, **.dosz**                 | Yes, without extraction         | `.zip` only (extracted by RetroBat) | No     |
| **Folder** `.pc`, `.dos`, `.dosbox` | Yes                             | Yes                                 | Yes    |
| **.bat**                            | Yes                             | Yes                                 | No     |
| **.m3u8** (several discs)           | Yes                             | No                                  | No     |

* **Archive**: put the game in a `.zip` (or `.dosz`, same format), named after the game (`Lemmings.zip`).
* **Folder**: create a folder with the `.pc`, `.dos` or `.dosbox` extension (`Lemmings.pc`) and put the game files in it. A `dosbox.bat` file in the folder starts the game (for DOSBox Staging: `dosbox.bat`, `run.bat` or `autoexec.bat`). A `dosbox.conf` in the folder holds the game settings (DOSBox Staging; dosbox\_pure core with **EMULATION > LOAD DOSBOX.CONF**).
* **.bat**: a batch file that starts the game.

```
roms\
└─ dos\
   ├─ Lemmings.zip
   └─ Prince of Persia.pc\
      ├─ dosbox.bat
      └─ (game files)
```

### Zip games

DOSBox Pure can load games directly from **ZIP** files without the need to extract them. Changes (saved games, installation) are stored in a separate file (see [**Folders**](ms-dos.md#folders)): the original archive is not modified.

### Mount ZIP as A or D drive (DOSBox Pure) <a href="#mount-zip-as-a-or-d-drive" id="mount-zip-as-a-or-d-drive"></a>

If you have a ZIP file you want to load as a fake floppy disk or fake CD-ROM, there are multiple options, rename the file from `.ZIP` to e.g., `.D.ZIP` (to use the D: drive).

### Multi-disc

Use a `.m3u8` file (DOSBox Pure), all files listed in it will be added to the disc swap hotkeys.

The first image will automatically get mounted as the A: or D: drive depending on whether it is a CD or floppy disk image.

## Controls

DOS games are mostly played with the keyboard and mouse. The PC keyboard and mouse work with every emulator.

### dosbox\_pure core and DOSBox Pure

DOSBox Pure recognizes many games and maps the keys to the controller by itself (**CONTROLS > GAMEPAD AUTO MAPPING**, on by default).

* **L3** opens the on-screen keyboard (core, set with **USER INTERFACE > L3 BUTTON USAGE**: ON-SCREEN KEYBOARD, ON-SCREEN KEYBOARD ONLY (IN GAME), CORE MENU or disabled). With standalone DOSBox Pure, L3 opens the menu.
* **CONTROLS > PLAYER 1 CONTROLLER TYPE** (core) chooses what the controller emulates: keyboard keys, mouse, DOS joystick, Gravis gamepad, flight stick…
* **CONTROLS > KEYBOARD LAYOUT** matches the DOS keyboard to yours (FRANCE for an AZERTY keyboard).
* **CONTROLS > KEYBOARD FOCUS** (core) gives the whole keyboard to the game: RetroArch hotkeys are disabled. The **Scroll Lock** key toggles it.

Some games show the buttons of the official Gravis gamepad by colour. Mapping: Blue = NORTH, Red = WEST, Yellow = SOUTH, Green = EAST.

### DOSBox Staging and DOSBox

The game sees the controller as a DOS joystick (**CONTROLS > JOYSTICK TYPE** with DOSBox Staging). To play with a controller a game that only supports the keyboard, use pad2key , or the DOSBox mapper (**Ctrl + F1**).

### Hotkeys

The dosbox\_pure core uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../navigation/hotkeys.md) page).

**DOSBox Pure (standalone)**

| Hotkey             | Action                       | Keyboard   |
| ------------------ | ---------------------------- | ---------- |
| **HOTKEY + START** | Quit                         |            |
| HOTKEY + WEST      | Save state                   | Ctrl + F5  |
| HOTKEY + NORTH     | Load state                   | Ctrl + F9  |
| L3                 | DOSBox Pure menu             | Ctrl + F12 |
| —                  | Pause                        | Ctrl + F1  |
| —                  | Fast forward (hold)          | Ctrl + F3  |
| —                  | Fullscreen / window          | Ctrl + F7  |
| —                  | Lock the mouse to the window | Ctrl + F11 |

The save slot is chosen in the DOSBox Pure menu (**Saving & Loading**). These save states do not show up in the save state manager.

**DOSBox Staging and DOSBox**

| Hotkey             | Action                    | Keyboard    |
| ------------------ | ------------------------- | ----------- |
| **HOTKEY + START** | Quit                      |             |
| —                  | Key and controller mapper | Ctrl + F1   |
| —                  | Fullscreen / window       | Alt + Enter |

## Folders

<table><thead><tr><th width="345.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\dos</code></td></tr><tr><td>Sound banks and MT-32 ROMs</td><td><code>bios\scummvm\extra</code> (copied to the DOSBox Pure and DOSBox Staging folders)</td></tr><tr><td>dosbox_pure core: changes to <code>.zip</code> games</td><td><code>saves\dos</code></td></tr><tr><td>dosbox_pure core: save states</td><td><code>saves\dos\libretro.dosbox_pure</code></td></tr><tr><td>Standalone DOSBox Pure: saves and save states</td><td><code>saves\dos\dosbox-pure</code></td></tr><tr><td>Standalone DOSBox Pure: configuration</td><td><code>emulators\dosbox-pure\DOSBoxPure.cfg</code></td></tr><tr><td>DOSBox Staging: configuration</td><td><code>emulators\dosbox-staging\dosbox-staging.conf</code> (or <code>dosbox.conf</code> in the game folder)</td></tr><tr><td>DOSBox Staging, DOSBox: game saves</td><td>Game folder</td></tr></tbody></table>

## Guides

### Load Games

This is the first screen that appears when loading a game with DOSBox Pure. It offers a gamepad controllable list of all executable files for the loaded game. By pressing right an item can be selected as the default which will skip the menu on the next launch.

<div align="left"><figure><img src="../../../.gitbook/assets/image (740).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
If there is only a single executable, the menu will not show.
{% endhint %}

**USER INTERFACE > DOSBOX START MENU** (core) sets what happens when the game ends: immediate shutdown, after 3 or 5 seconds, or back to the menu.

### Install a game (DOSBox Staging)

With DOSBox Staging, **EMULATION > TRY TO RUN GAME SETUP** starts the game setup program (`SETUP.EXE`, or the one chosen with **EMULATION > SETUP EXECUTABLE**) to set the sound card. **EMULATION > FORCE EXE TO RUN** starts a specific executable.

### A game that runs too fast or too slow

* dosbox\_pure core, DOSBox Pure: **EMULATION > CPU CYCLES**.
* DOSBox Staging: **EMULATION > CPU CYCLES** for real-mode games, **EMULATION > CPU CYCLES(PROTECTED MODE)** for later games (Doom, Duke Nukem 3D…).

### Sound and music

* **AUDIO > SOUNDBLASTER TYPE** and **AUDIO > MIDI OUTPUT** set the sound card and the music. The sound card chosen in the game setup program must match.
* **AUDIO > GRAVIS ULTRASOUND** enables the Gravis card for the games that support it.

### Other useful options

| Emulator                        | Option                                    | Effect                                                          |
| ------------------------------- | ----------------------------------------- | --------------------------------------------------------------- |
| dosbox\_pure (core, standalone) | **VIDEO > 3DFX VOODOO ACCELERATOR**       | 3D card for compatible games (Tomb Raider, Carmageddon…).       |
| dosbox\_pure (core, standalone) | **VIDEO > ASPECT RATIO CORRECTION**       | Corrects the non-square pixels of DOS games.                    |
| dosbox\_pure (standalone)       | **VISUAL RENDERING > CRT FILTER**         | CRT screen effect.                                              |
| dosbox-staging                  | **SHADER SET**                            | CRT rendering (CRT AUTO by default), smoothing or sharp pixels. |
| dosbox-staging                  | **VOODOO > ENABLE 3DFX VOODOO EMULATION** | 3D card for compatible games.                                   |

## Known issues

<table><thead><tr><th width="364">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start with DOSBox</td><td>DOSBox 0.74 only starts game folders with a <code>dosbox.bat</code>. Use the dosbox_pure core.</td></tr><tr><td>A <code>.dosz</code> does not start with DOSBox Staging</td><td>Rename it to <code>.zip</code>, or use DOSBox Pure.</td></tr><tr><td>The executable selection screen comes back at every launch</td><td>Choose the executable with the d-pad RIGHT (see <a href="ms-dos.md#load-games"><strong>Guides</strong></a>).</td></tr><tr><td>No sound or no music</td><td>Set the sound card in the game setup program, the same as in <strong>AUDIO > SOUNDBLASTER TYPE</strong>. For the MT-32, add the ROMs to <code>bios\scummvm\extra</code>.</td></tr><tr><td>The keys do not match my keyboard</td><td>Set <strong>CONTROLS > KEYBOARD LAYOUT</strong>.</td></tr><tr><td>RetroArch hotkeys trigger while typing</td><td>Enable <strong>CONTROLS > KEYBOARD FOCUS</strong> (core).</td></tr></tbody></table>
