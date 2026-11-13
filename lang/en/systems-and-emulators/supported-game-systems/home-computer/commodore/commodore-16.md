---
description: Commodore
---

# Commodore 16

<div align="left"><figure><img src="../../../../.gitbook/assets/image (549).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Commodore 16** was released in 1984. Commodore designed it as a low-cost home computer to replace the VIC-20. It has 16 KB of memory, BASIC 3.5 (more complete than the Commodore 64 one) and a new graphics and sound chip, the **TED**, which displays 121 colours.

It is not compatible with the Commodore 64, which held back its success in the United States. In Europe it sold better thanks to its price: in the United Kingdom, Germany or Hungary, it received many budget games sold on tape. The same family includes the **C116**, with a rubber keyboard, and the **Plus/4**, with 64 KB and built-in software. C16 games run on the Plus/4.

RetroBat emulates the C16 with **VICE**, the reference emulator for Commodore computers.

{% embed url="https://en.wikipedia.org/wiki/Commodore_16" %}

## At a glance

<table><thead><tr><th width="239"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\c16</code></td></tr><tr><td><strong>Extensions</strong></td><td>.d64 .prg .tap .t64 .crt .bin .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: vice_xplus4</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

The C16 has only one emulator in RetroBat.

| Emulator                             | Strengths                                                                                                                     | Limitations                                                                                              |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **libretro: vice\_xplus4** (default) | Very accurate emulation of the C16 / C116 / Plus/4 family, emulated disk drive and tape drive, virtual keyboard, save states. | Tape games load slowly, as on the real machine (see [Guides](commodore-16.md#speeding-up-tape-loading)). |

The same core is used by the Commodore Plus/4 system (`roms\cplus4` folder). For the C16, RetroBat automatically sets the model to C16.

## BIOS

No BIOS is needed: the C16 ROMs are built into VICE.

## Which game format should I use?

<table><thead><tr><th width="130.25">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.d64</strong></td><td>Disk image (1541 / 1551 drives). The most practical format.</td></tr><tr><td><strong>.prg</strong></td><td>Program only, loaded directly in memory. The fastest to start.</td></tr><tr><td><strong>.tap</strong></td><td>Tape image. Loading is slow (see <a href="commodore-16.md#speeding-up-tape-loading">Guides</a>).</td></tr><tr><td>.t64</td><td>Tape archive, rare on the C16.</td></tr><tr><td>.crt, .bin</td><td>Cartridge.</td></tr><tr><td>.m3u</td><td>List of the disks or tapes of a game (see <a href="commodore-16.md#games-on-several-disks-or-tapes">Guides</a>).</td></tr><tr><td>.zip, .7z</td><td>Archive containing one of the formats above.</td></tr></tbody></table>

VICE starts the game by itself: there is no need to type the load command.

## Controls

### Automatic configuration

RetroBat configures the controllers automatically. The joystick is plugged into **port 2**, used by most games.

<table><thead><tr><th width="217.75">RetroBat controller</th><th>Commodore 16</th></tr></thead><tbody><tr><td>D-pad</td><td>Joystick</td></tr><tr><td>SOUTH</td><td>Fire</td></tr><tr><td>EAST</td><td>Second fire (rarely used)</td></tr><tr><td>NORTH</td><td>Space bar</td></tr><tr><td>L2</td><td>ESC</td></tr><tr><td>R2</td><td>RETURN (Enter)</td></tr><tr><td>SELECT</td><td>Virtual keyboard</td></tr></tbody></table>

Many games ask you to press the space bar or RETURN to start: use NORTH or R2.

### Virtual keyboard

**SELECT** shows or hides the virtual keyboard. Move with the D-pad and press a key with **SOUTH**. In the virtual keyboard, **START** types RETURN, **NORTH** the space bar, **WEST** toggles SHIFT LOCK and **EAST** makes the keyboard transparent.

### Keyboard

A keyboard plugged into the PC works as a C16 keyboard. Enable **CONTROLS > KEYBOARD FOCUS** so that the keys do not trigger RetroArch hotkeys. The **Scroll Lock** key turns this mode on or off in game.

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

<table><thead><tr><th width="266.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Save states</td><td><code>saves\c16\libretro.vice_xplus4</code></td></tr><tr><td>Save disks created by VICE</td><td><code>saves\c16</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr></tbody></table>

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

Place the `.m3u` and the files in `roms\c16`. Change disk in game with the RetroArch hotkeys for multi-disk games.

### Choosing the model

The **EMULATION > MODEL TYPE** option selects the emulated machine: C16 PAL (default for this system), C16 NTSC, Plus/4 PAL or NTSC, V364 and C232.

* Keep a **PAL** model for European games, which are the vast majority. In NTSC, they run too fast or display incorrectly.
* A game that needs more than 16 KB of memory does not start on a C16: select **PLUS4 PAL**, or place the game in the Commodore Plus/4 system.

### Other useful options

| Option                                    | Effect                                                      |
| ----------------------------------------- | ----------------------------------------------------------- |
| **VISUAL RENDERING > COLOR PALETTE**      | Colodore (default), VICE internal palette or Yape palettes. |
| **VISUAL RENDERING > CROP**               | Hides the border around the picture.                        |
| **VISUAL RENDERING > PIXEL ASPECT RATIO** | Shape of the pixels: automatic, PAL, NTSC or square.        |

## Known issues

| Issue                                           | Solution                                                                                                          |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| The game stays on a loading screen              | This is normal with a tape: loading takes several minutes. Enable **FAST LOAD** or use a `.prg` / `.d64` version. |
| The joystick does not respond                   | The game expects the joystick in the other port: change **JOYSTICK PORT**.                                        |
| The game runs too fast or the picture jumps     | It is a European game run in NTSC: select a **PAL** model.                                                        |
| The game does not start or shows a memory error | It is made for the Plus/4: select the **PLUS4 PAL** model.                                                        |
| The game asks you to press a key                | Use NORTH (space bar), R2 (RETURN) or the virtual keyboard (SELECT).                                              |
