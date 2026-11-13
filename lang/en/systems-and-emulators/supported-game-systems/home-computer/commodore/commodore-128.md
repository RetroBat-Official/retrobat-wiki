---
description: Commodore
---

# Commodore 128

<div align="left"><figure><img src="../../../../.gitbook/assets/image (553).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Commodore 128** was released in 1985. It succeeded the Commodore 64 and remained compatible with it. It actually combines three computers: a **C128** mode with 128 KB of memory and BASIC 7.0, a **C64** mode that runs almost the whole Commodore 64 library, and a **CP/M** mode thanks to a second processor, the Z80. It can display 40 columns on a TV or 80 columns on a monitor.

Most players used it in C64 mode: few games were written for the C128 mode. The C128D, with a built-in disk drive, was released in 1986.

RetroBat emulates the C128 with **VICE**, the reference emulator for Commodore computers.

{% embed url="https://en.wikipedia.org/wiki/Commodore_128" %}

## At a glance

<table><thead><tr><th width="216.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\c128</code></td></tr><tr><td><strong>Extensions</strong></td><td>.d64 .d71 .d81 .g64 .prg .t64 .tap .crt .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: vice_x128</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (vice_x128)</td></tr></tbody></table>

## Which emulator should I choose?

The C128 has only one emulator in RetroBat.

<table><thead><tr><th width="169.5">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: vice_x128</strong> (default)</td><td>Emulates the C128 and C64 modes, the 40 and 80 column displays, the 1571 and 1581 drives, the virtual keyboard and save states.</td><td>For Commodore 64 games, the Commodore 64 system is easier to use.</td></tr></tbody></table>

Commodore 64 games are best placed in the **Commodore 64** system (see the **Commodore 64** page). The C128 system is for programs written for the C128.

## BIOS

No BIOS is needed: the C128 and disk drive ROMs are built into VICE.

## Which game format should I use?

<table><thead><tr><th width="164">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.d64</strong></td><td>1541 disk image.</td></tr><tr><td><strong>.d71</strong></td><td>Double-sided disk image of the 1571 drive, the C128 drive.</td></tr><tr><td>.d81</td><td>3.5-inch disk image of the 1581 drive.</td></tr><tr><td>.g64</td><td>Exact image of a copy-protected disk.</td></tr><tr><td><strong>.prg</strong></td><td>Program only, loaded directly in memory.</td></tr><tr><td>.t64, .tap</td><td>Tape. Loading a <code>.tap</code> is slow (see <a href="commodore-128.md#speeding-up-loading">Guides</a>).</td></tr><tr><td>.crt</td><td>Cartridge.</td></tr><tr><td>.m3u</td><td>List of the disks of a game (see <a href="commodore-128.md#games-on-several-disks">Guides</a>).</td></tr><tr><td>.zip, .7z</td><td>Archive containing one of the formats above.</td></tr></tbody></table>

VICE starts the program by itself: there is no need to type the load command.

## Controls

### Automatic configuration

RetroBat configures the controllers automatically. The joystick is plugged into **port 2**, used by most games.

<table><thead><tr><th width="202.75">RetroBat controller</th><th>Commodore 128</th></tr></thead><tbody><tr><td>D-pad</td><td>Joystick</td></tr><tr><td>SOUTH</td><td>Fire</td></tr><tr><td>EAST</td><td>Second fire (rarely used)</td></tr><tr><td>NORTH</td><td>Space bar</td></tr><tr><td>L2</td><td>RUN/STOP (Escape key)</td></tr><tr><td>R2</td><td>RETURN (Enter)</td></tr><tr><td>SELECT</td><td>Virtual keyboard</td></tr></tbody></table>

### Virtual keyboard

**SELECT** shows or hides the virtual keyboard. Move with the D-pad and press a key with **SOUTH**. In the virtual keyboard, **START** types RETURN, **NORTH** the space bar, **WEST** toggles SHIFT LOCK and **EAST** makes the keyboard transparent.

### Keyboard

A keyboard plugged into the PC works as a C128 keyboard. Enable **CONTROLS > KEYBOARD FOCUS** so that the keys do not trigger RetroArch hotkeys. The **Scroll Lock** key turns this mode on or off in game.

The **Right CTRL** key swaps joystick ports 1 and 2 in game. The **F7** key switches the display between 40 and 80 columns.

### Control options

<table><thead><tr><th width="342.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>CONTROLS > JOYSTICK PORT</strong></td><td>Port 2 (default) or port 1, for the games that expect the joystick in port 1.</td></tr><tr><td><strong>CONTROLS > JOYSTICK PORT TYPE</strong></td><td>Joystick (default), paddles, mouse, KoalaPad, light pen or light gun.</td></tr><tr><td><strong>CONTROLS > RETROPAD FACE BUTTON OPTIONS</strong></td><td>Changes the fire button, or puts "up" (jump) on a button.</td></tr><tr><td><strong>CONTROLS > PLAYER 1 CONTROLLER TYPE</strong> / <strong>PLAYER 2</strong></td><td>RETROPAD (default), JOYSTICK or KEYBOARD.</td></tr></tbody></table>

### Light guns

The **GUNS > ENABLE GUN** option plugs a light pen into port 1, the only C128 port that accepts them. The **JOYSTICK PORT TYPE** option selects another light pen or light gun model.

For more details, see the [**Lightguns**](../../../../controllers/supported-controllers/lightguns/) page.

### Hotkeys

vice\_x128 uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="314">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Save states</td><td><code>saves\c128\libretro.vice_x128</code></td></tr><tr><td>Save disks created by VICE</td><td><code>saves\c128</code></td></tr><tr><td>Optional VICE files (JiffyDOS, <code>vicerc</code> configuration)</td><td><code>bios\vice</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### C64 mode and 80 column display

* The **EMULATION > C64 MODE** option starts the machine directly in Commodore 64 mode, for a C64 game placed in this system.
* The **EMULATION > VIDEO OUTPUT** option selects the display at startup: 40 columns (VIC-II, default) or 80 columns (VDC). Some C128 programs and the CP/M mode use the 80 column display. In game, **F7** switches from one to the other.

### Games on several disks

Create an `.m3u` file that lists the disks in order, one per line:

```
My game (Disk 1).d71
My game (Disk 2).d71
```

Place the `.m3u` and the disks in `roms\c128`. Change disk in game with the [RetroArch hotkeys](../../../../navigation/hotkeys.md) for multi-disk games.

### Speeding up loading

The **EMULATION > FAST LOAD** option runs the emulation at maximum speed while a disk or a tape is loading, as long as no sound is played. **TRUE DRIVE EMULATION** must be enabled for disks. The **EMULATION > WARP BOOST** option makes this mode even faster.

### Choosing the model and region

The **EMULATION > MODEL TYPE** option selects the emulated machine: C128, C128D or C128DCR, PAL or NTSC.

The **Auto** models choose the region from the file name: `NTSC`, `(USA)` or `(Japan)` start the game in NTSC, `PAL` or `(Europe)` in PAL. Without a tag, the region of the selected model is used. The default setting is **C128 PAL Auto**.

### Other useful options

<table><thead><tr><th width="340.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > MEMORY EXPANSION</strong></td><td>Adds a RAM Expansion Unit (REU) from 128 KB to 16 MB.</td></tr><tr><td><strong>VISUAL RENDERING > COLOR PALETTE</strong></td><td>Colodore (default), Pepto, VICE internal palette…</td></tr><tr><td><strong>VISUAL RENDERING > CROP</strong></td><td>Hides the border around the picture.</td></tr><tr><td><strong>VISUAL RENDERING > PIXEL ASPECT RATIO</strong></td><td>Shape of the pixels: automatic, PAL, NTSC or square.</td></tr></tbody></table>

## Known issues

| Issue                                         | Solution                                                                                                            |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| A Commodore 64 game does not start            | Place it in the Commodore 64 system, or enable **C64 MODE**.                                                        |
| The screen stays empty or only shows a cursor | The program uses the 80 column display: press **F7** or set **VIDEO OUTPUT** to 80 columns.                         |
| The joystick does not respond                 | The game expects the joystick in the other port: change **JOYSTICK PORT**, or press **Right CTRL** on the keyboard. |
| The game runs too fast or the music is wrong  | It is a European game run in NTSC: select a **PAL** model.                                                          |
