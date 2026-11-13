---
description: Commodore
---

# Commodore Plus/4

<div align="left"><figure><img src="../../../../.gitbook/assets/image (551).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Commodore Plus/4** was released in 1984, at the same time as the Commodore 16, its little brother. It has 64 KB of memory, BASIC 3.5 and the **TED** chip (121 colours). Its name comes from the four applications built into its ROM (word processor, spreadsheet, database and graphics), grouped under the name "3-plus-1".

Designed for business and home use, it is not compatible with the Commodore 64 and sold poorly in the United States. In Europe it found its audience, like the C16, with many budget games on tape. It runs C16 games, and some games were written for its 64 KB.

RetroBat emulates the Plus/4 with **VICE**, the reference emulator for Commodore computers.

{% embed url="https://en.wikipedia.org/wiki/Commodore_Plus/4" %}

## At a glance

|                              |                                             |
| ---------------------------- | ------------------------------------------- |
| **Games folder**             | `roms\cplus4`                               |
| **Extensions**               | .d64 .prg .tap .t64 .crt .bin .m3u .zip .7z |
| **Default emulator**         | libretro: vice\_xplus4                      |
| **BIOS**                     | None                                        |
| **Controller configuration** | Automatic                                   |
| **Save states**              | libretro cores                              |
| **RetroAchievements**        | No                                          |
| **Netplay**                  | No                                          |

## Which emulator should I choose?

The Plus/4 has only one emulator in RetroBat.

| Emulator                             | Strengths                                                                                                                     | Limitations                                                                                                 |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **libretro: vice\_xplus4** (default) | Very accurate emulation of the C16 / C116 / Plus/4 family, emulated disk drive and tape drive, virtual keyboard, save states. | Tape games load slowly, as on the real machine (see [Guides](commodore-plus4.md#speeding-up-tape-loading)). |

The same core is used by the Commodore 16 system (`roms\c16` folder, see the [**Commodore 16**](commodore-16.md) page). For the Plus/4, RetroBat sets the model to Plus/4 PAL.

## BIOS

No BIOS is needed: the Plus/4 ROMs, built-in software included, are built into VICE.

## Which game format should I use?

| Format     | Notes                                                                                                    |
| ---------- | -------------------------------------------------------------------------------------------------------- |
| **.d64**   | Disk image (1541 / 1551 drives). The most practical format.                                              |
| **.prg**   | Program only, loaded directly in memory. The fastest to start.                                           |
| **.tap**   | Tape image. Loading is slow (see [Guides](commodore-plus4.md#speeding-up-tape-loading)).                 |
| .t64       | Tape archive, rare on the Plus/4.                                                                        |
| .crt, .bin | Cartridge.                                                                                               |
| .m3u       | List of the disks or tapes of a game (see [Guides](commodore-plus4.md#games-on-several-disks-or-tapes)). |
| .zip, .7z  | Archive containing one of the formats above.                                                             |

VICE starts the game by itself: there is no need to type the load command.

## Controls

### Automatic configuration

RetroBat configures the controllers automatically. The joystick is plugged into **port 2**, used by most games.

| RetroBat controller | Commodore Plus/4          |
| ------------------- | ------------------------- |
| D-pad               | Joystick                  |
| SOUTH               | Fire                      |
| EAST                | Second fire (rarely used) |
| NORTH               | Space bar                 |
| L2                  | ESC                       |
| R2                  | RETURN (Enter)            |
| SELECT              | Virtual keyboard          |

Many games ask you to press the space bar or RETURN to start: use NORTH or R2.

### Virtual keyboard

**SELECT** shows or hides the virtual keyboard. Move with the D-pad and press a key with **SOUTH**. In the virtual keyboard, **START** types RETURN, **NORTH** the space bar, **WEST** toggles SHIFT LOCK and **EAST** makes the keyboard transparent.

### Keyboard

A keyboard plugged into the PC works as a Plus/4 keyboard. Enable **CONTROLS > KEYBOARD FOCUS** so that the keys do not trigger RetroArch hotkeys. The **Scroll Lock** key turns this mode on or off in game.

The **Right CTRL** key swaps joystick ports 1 and 2 in game.

### Control options

| Option                                                 | Effect                                                                            |
| ------------------------------------------------------ | --------------------------------------------------------------------------------- |
| **CONTROLS > JOYSTICK PORT**                           | Port 2 (default) or port 1, for the few games that expect the joystick in port 1. |
| **CONTROLS > RETROPAD FACE BUTTON OPTIONS**            | Changes the fire button, or puts "up" (jump) on a button.                         |
| **CONTROLS > PLAYER 1 CONTROLLER TYPE** / **PLAYER 2** | RETROPAD (default), JOYSTICK or KEYBOARD.                                         |

### Hotkeys

vice\_xplus4 uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="276.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Save states</td><td><code>saves\cplus4\libretro.vice_xplus4</code></td></tr><tr><td>Save disks created by VICE</td><td><code>saves\cplus4</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Speeding up tape loading

A tape game takes several minutes to load, as on the real machine. The **EMULATION > FAST LOAD** option runs the emulation at maximum speed during loading, as long as no sound is played. It also works with disks, if **EMULATION > TRUE DRIVE EMULATION** is enabled.

When possible, prefer the `.prg` or `.d64` version of a game: it starts much faster.

### Games on several disks or tapes

Create an `.m3u` file that lists the files in order, one per line:

```
My game (Disk 1).d64
My game (Disk 2).d64
```

Place the `.m3u` and the files in `roms\cplus4`. Change disk in game with the [RetroArch hotkeys](../../../../navigation/hotkeys.md) for multi-disk games.

### Choosing the model

The **EMULATION > MODEL TYPE** option selects the emulated machine: Plus/4 PAL (default for this system), Plus/4 NTSC, C16 PAL or NTSC, V364 and C232.

* Keep a **PAL** model for European games, which are the vast majority. In NTSC, they run too fast or display incorrectly.
* A C16 game that has issues on the Plus/4 can be run with a **C16 PAL** model, or placed in the Commodore 16 system.

### Other useful options

| Option                                    | Effect                                                      |
| ----------------------------------------- | ----------------------------------------------------------- |
| **VISUAL RENDERING > COLOR PALETTE**      | Colodore (default), VICE internal palette or Yape palettes. |
| **VISUAL RENDERING > CROP**               | Hides the border around the picture.                        |
| **VISUAL RENDERING > PIXEL ASPECT RATIO** | Shape of the pixels: automatic, PAL, NTSC or square.        |

## Known issues

<table><thead><tr><th width="345.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game stays on a loading screen</td><td>This is normal with a tape: loading takes several minutes. Enable <strong>FAST LOAD</strong> or use a <code>.prg</code> / <code>.d64</code> version.</td></tr><tr><td>The joystick does not respond</td><td>The game expects the joystick in the other port: change <strong>JOYSTICK PORT</strong>, or press <strong>Right CTRL</strong> on the keyboard.</td></tr><tr><td>The game runs too fast or the picture jumps</td><td>It is a European game run in NTSC: select a <strong>PAL</strong> model.</td></tr><tr><td>A C16 game does not work correctly</td><td>Select the <strong>C16 PAL</strong> model, or place the game in the Commodore 16 system.</td></tr><tr><td>The game asks you to press a key</td><td>Use NORTH (space bar), R2 (RETURN) or the virtual keyboard (SELECT).</td></tr></tbody></table>
