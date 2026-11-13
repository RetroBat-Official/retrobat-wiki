---
description: Commodore
---

# Commodore PET

<div align="left"><figure><img src="../../../../.gitbook/assets/image (550).png" alt="" width="240"><figcaption></figcaption></figure></div>

## Overview

The **Commodore PET** (Personal Electronic Transactor) was released in 1977. With the Apple II and the TRS-80, it is one of the very first personal computers sold ready to use. Everything is in the same case: monochrome screen, keyboard and, on the first model, tape drive.

It was mostly used in schools and businesses. Several series followed: 2001, 3000, 4000, then 8000 with an 80 column display. Its games are simple, often drawn with the PETSCII graphics characters and played with the keyboard: the PET has no joystick port.

RetroBat emulates the PET with **VICE**, the reference emulator for Commodore computers.

{% embed url="https://en.wikipedia.org/wiki/Commodore_PET" %}

## At a glance

<table><thead><tr><th width="234"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\pet</code></td></tr><tr><td><strong>Extensions</strong></td><td>.crt .d64 .d80 .d81 .d82 .prg .tap .t64 .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: vice_xpet</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic (keyboard keys on the controller)</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

The PET has only one emulator in RetroBat.

<table><thead><tr><th width="184.5">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: vice_xpet</strong> (default)</td><td>Emulates all PET models, the disk and tape drives, with virtual keyboard and save states.</td><td>Games are played with the keyboard.</td></tr></tbody></table>

## BIOS

No BIOS is needed: the ROMs of the various PET models are built into VICE.

## Which game format should I use?

<table><thead><tr><th width="224">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.prg</strong></td><td>Program only, loaded directly in memory. The most common format for PET games.</td></tr><tr><td><strong>.d64</strong>, .d80, .d81, .d82</td><td>Disk image (2040 / 4040, 8050, 1581, 8250 drives).</td></tr><tr><td>.tap, .t64</td><td>Tape. Loading a <code>.tap</code> is slow.</td></tr><tr><td>.crt</td><td>Cartridge.</td></tr><tr><td>.m3u</td><td>List of the disks of a program.</td></tr><tr><td>.zip, .7z</td><td>Archive containing one of the formats above.</td></tr></tbody></table>

VICE starts the program by itself: there is no need to type the load command.

## Controls

### Automatic configuration

The PET has no joystick port: games are played with the keyboard. A few keyboard keys are placed on the controller:

<table><thead><tr><th width="255.25">RetroBat controller</th><th>PET</th></tr></thead><tbody><tr><td>NORTH</td><td>Space bar</td></tr><tr><td>L2</td><td>RUN/STOP (Escape key)</td></tr><tr><td>R2</td><td>RETURN (Enter)</td></tr><tr><td>SELECT</td><td>Virtual keyboard</td></tr></tbody></table>

### Virtual keyboard

**SELECT** shows or hides the virtual keyboard. Move with the D-pad and press a key with **SOUTH**. In the virtual keyboard, **START** types RETURN, **NORTH** the space bar, **WEST** toggles SHIFT LOCK and **EAST** makes the keyboard transparent.

### Keyboard

A keyboard plugged into the PC works as a PET keyboard: it is the easiest way to play. Enable **CONTROLS > KEYBOARD FOCUS** so that the keys do not trigger RetroArch hotkeys. The **Scroll Lock** key turns this mode on or off in game.

To place other keys on the controller, create a PadToKey profile (see the [**PadToKey**](../../../../controllers/pad2key.md) page).

### Hotkeys

vice\_xpet uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="286.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Save states</td><td><code>saves\pet\libretro.vice_xpet</code></td></tr><tr><td>Save disks created by VICE</td><td><code>saves\pet</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Adding a game

1. Copy the game file (`.prg`, `.d64`…) to `roms\pet`.
2. Update the RetroBat game list.
3. Launch the game: VICE loads and starts it automatically.

### Choosing the model

The **EMULATION > MODEL TYPE** option selects the emulated PET. The default model is the **PET 8032** (80 columns, 32 KB).

Many games were written for the 40 column models: if they display incorrectly or do not start, select **PET 4032**, or **PET 2001** for the oldest ones.

### Other useful options

| Option                               | Effect                                                                 |
| ------------------------------------ | ---------------------------------------------------------------------- |
| **VISUAL RENDERING > COLOR PALETTE** | Monitor colour: internal (default), green, amber or white.             |
| **VISUAL RENDERING > CROP**          | Hides the border around the picture.                                   |
| **EMULATION > FAST LOAD**            | Runs the emulation at maximum speed while a disk or a tape is loading. |

> 📷 **Screenshot to add**: Commodore PET system options in RetroBat.

## Known issues

| Issue                                             | Solution                                                                                                                                    |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| The game displays incorrectly or does not start   | It is written for another model: select **PET 4032** or **PET 2001**.                                                                       |
| The controller does not move anything in the game | The PET has no joystick: play with the keyboard, the virtual keyboard (SELECT) or a [PadToKey](../../../../controllers/pad2key.md) profile. |
