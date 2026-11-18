---
description: Atari
---

# Atari ST

<div align="left"><figure><img src="../../../../.gitbook/assets/image (617).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Atari ST** came out in 1985 (520 ST, then 1040 ST). It has a Motorola 68000 processor and the GEM graphical interface, with a mouse, and cost much less than its rivals. Its built-in MIDI ports made it the musicians' computer. In Europe, it was one of the most popular gaming computers of the late 1980s. Then came the Mega ST, the STE (1989: more colors, digital sound, enhanced joystick ports), the Mega STE, the TT and the Falcon.

Its library is huge: Dungeon Master, Xenon 2, Populous, Captain Blood, Carrier Command, Starglider, Another World, Lemmings, Kick Off… Most games came on floppy disk.

{% embed url="https://en.wikipedia.org/wiki/Atari_ST" %}

## At a glance

<table><thead><tr><th width="212.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\atarist</code></td></tr><tr><td><strong>Extensions</strong></td><td>.st .msa .stx .dim .ipf .ctr .gz .m3u .gem .gemdos .acsi .ahd .vhd .scsi .shd .ide .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: hatarib</td></tr><tr><td><strong>BIOS</strong></td><td>None (TOS optional; required for hatari2014)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; Hatari with hotkeys (one per game)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>libretro hatarib core</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="147.75">Emulator</th><th width="148">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: hatarib</strong> (default)</td><td>Everyone</td><td>hatariB, a recent libretro version of Hatari: built-in EmuTOS, on-screen keyboard, mouse on the right stick, hard disks, save states, netplay.</td><td>—</td></tr><tr><td><strong>libretro: hatari2014</strong></td><td>Troubleshooting</td><td>Old libretro version of Hatari (1.8).</td><td>Needs <code>tos.img</code>. No hard disks, no <code>.ctr</code> / <code>.gz</code>.</td></tr><tr><td><strong>hatari</strong> (standalone)</td><td>Purists</td><td>Hatari in its original version, with its full menu: ST, Mega ST, STE, Mega STE, STE Jaguar pads, video recording.</td><td>Needs a TOS (see <a href="atari-st.md#bios"><strong>BIOS</strong></a>). Only one save state per game, with hotkeys.</td></tr></tbody></table>

**If in doubt, keep libretro: hatarib.**

## BIOS

The Atari ST operating system, **TOS**, is in the machine's ROM. hatariB has **EmuTOS** built in, a free TOS compatible with most games: no file is needed. An original TOS is still more compatible with some games.

<table><thead><tr><th width="232.25">File</th><th width="165.75">Folder</th><th>Used by</th></tr></thead><tbody><tr><td><code>tos.img</code></td><td><code>bios</code></td><td>Default TOS: hatarib, hatari2014 (required), hatari</td></tr><tr><td><code>tos102.img</code>, <code>tos104.img</code>, <code>tos106.img</code>, <code>tos206.img</code></td><td><code>bios\hatari\tos</code></td><td><strong>EMULATION > TOS</strong> choice (hatarib, hatari2014, hatari)</td></tr><tr><td><code>emutos.img</code></td><td><code>bios\hatari\tos</code></td><td>hatari, hatari2014: EmuTOS</td></tr></tbody></table>

The RetroBat BIOS check lists them as optional. Each TOS exists in several versions (countries, revisions): RetroBat does not check the MD5. Files must have exactly these names.

* **hatarib**: `tos.img` when present, EmuTOS otherwise. A TOS chosen in **EMULATION > TOS** is copied automatically from `bios\hatari\tos` to `bios\hatarib`, the folder the core reads.
* **hatari**: `tos.img`, otherwise `emutos.img`. Without either, Hatari does not start (« Missing TOS file » message).
* **hatari2014**: `tos.img`, or the TOS chosen in **EMULATION > TOS**.

Which TOS should I choose?

<table><thead><tr><th width="143.25">TOS</th><th width="134.5">Machines</th><th>Notes</th></tr></thead><tbody><tr><td>1.00, 1.02, 1.04</td><td>ST, Mega ST</td><td>The most compatible with floppy disk games. 1.04 is recommended for games installed on hard disk.</td></tr><tr><td>1.06, 1.62</td><td>STE only</td><td>With Hatari, RetroBat then chooses the STE machine automatically.</td></tr><tr><td>2.06</td><td>ST and STE</td><td>Better hard disk support, less compatible with a few old games.</td></tr><tr><td>EmuTOS</td><td>All</td><td>Free, supports hard disks. Compatible with most games, not all.</td></tr></tbody></table>

RetroBat avoids combinations that do not work: autostart and GEMDOS hard disks need TOS 1.04 or later, hard disk images need a driver that only EmuTOS has built in. In these cases, RetroBat picks a compatible TOS (TOS 1.04, 2.06 or EmuTOS).

## Which game format?

| Type                       | Extensions                                       | Notes                                                                                                        |
| -------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| Floppy disk                | `.st`, `.msa`                                    | The most common formats.                                                                                     |
| Copy-protected floppy disk | `.stx`, `.ipf`, `.ctr`                           | Keep copy protections. `.ipf` and `.ctr` are read with the CAPS library, shipped with RetroBat.              |
| Floppy disk                | `.dim`, `.gz`                                    | `.gz`: compressed floppy disk.                                                                               |
| Several floppy disks       | `.m3u`                                           | List of a game's disks (see [**Guides**](atari-st.md#games-on-several-disks-the-m3u-file)).                  |
| Hard disk (image)          | `.acsi`, `.ahd`, `.vhd`, `.scsi`, `.shd`, `.ide` | The disk type depends on the extension. hatarib and hatari.                                                  |
| Hard disk (folder)         | `.gem`, `.gemdos`                                | A PC folder seen as a hard disk (GEMDOS, see [**Guides**](atari-st.md#games-installed-on-hard-disk-gemdos)). |

Files can be compressed as `.zip` or `.7z`. Hard disk formats, `.ctr` and `.gz` do not work with hatari2014.

## Controls

RetroBat configures controllers automatically. The Atari ST joystick has a single button. The PC mouse is the Atari mouse, and the PC keyboard the Atari keyboard.

| RetroBat controller | libretro: hatarib            | libretro: hatari2014    | hatari                                  |
| ------------------- | ---------------------------- | ----------------------- | --------------------------------------- |
| D-pad               | Joystick                     | Joystick                | Joystick                                |
| Left stick          | Joystick                     | —                       | Joystick                                |
| Right stick         | Mouse                        | —                       | —                                       |
| SOUTH               | Fire                         | —                       | Fire                                    |
| EAST                | Autofire                     | Fire                    | Space bar or jump (**BUTTON 2** option) |
| WEST                | Left click                   | Emulator menu           | Autofire                                |
| NORTH               | Right click                  | —                       | —                                       |
| SELECT              | Drive A or B choice          | Mouse / joystick toggle | —                                       |
| START               | Help screen                  | On-screen keyboard      | —                                       |
| L1                  | On-screen keyboard           | Joystick number         | —                                       |
| R1                  | On-screen keyboard (one key) | Mouse speed             | —                                       |
| L2                  | Slow mouse                   | Status display          | —                                       |
| R2                  | Fast mouse                   | —                       | —                                       |
| L3                  | Space                        | —                       | —                                       |
| R3                  | Return                       | —                       | —                                       |

The hatarib **on-screen keyboard**: L1 shows it, choose a key with the D-pad, L1 presses it, R1 closes the keyboard. R1 alone opens the keyboard in « one key » mode: the game is paused until the key press. NORTH moves the keyboard to the top or bottom.

With hatari2014, the WEST button opens the core menu and SELECT toggles the D-pad between mouse and joystick.

With libretro cores, press `Scroll Lock` to turn on RetroArch's **Game Focus**: all keyboard keys go to the Atari. To put keyboard keys on the controller, see the [**Pad2Key**](../../../../controllers/pad2key.md) page.

**ADVANCED SETTINGS > CONTROLS**:

* **USE MOUSE** (hatarib, on by default): mouse plugged into port 1. Turn it off for two-joystick games.
* **ENABLE SECOND JOYSTICK** (hatari2014, on by default): may conflict with the mouse.
* **ENABLE AUTOFIRE**, **BUTTON 2**, **USE JAGUAR JOYPADS (STE)** (hatari): autofire, 2nd button role (**SPACE BAR**, for Xenon 2, or **JUMP (UP)**, for platform games), STE controllers.

### Hotkeys

libretro cores use the standard RetroArch hotkeys. Hatari uses the common RetroBat hotkeys:

<table><thead><tr><th width="211">Hotkey</th><th width="114.5">Key</th><th>Hatari</th></tr></thead><tbody><tr><td>HOTKEY + SOUTH</td><td><code>F12</code></td><td>Emulator menu</td></tr><tr><td>HOTKEY + WEST</td><td><code>F2</code></td><td>Save state</td></tr><tr><td>HOTKEY + NORTH</td><td><code>F4</code></td><td>Load state</td></tr><tr><td>HOTKEY + R3</td><td><code>F8</code></td><td>Screenshot</td></tr><tr><td>HOTKEY + L3</td><td><code>F11</code></td><td>Fullscreen</td></tr><tr><td>HOTKEY + START</td><td>—</td><td>Quit</td></tr></tbody></table>

On the keyboard: `AltGr` + `Q` quits Hatari (`Esc` is an Atari key). `Pause` pauses. Keys `F1` to `F10` exist on the Atari keyboard: with **CONTROLS > FUNCTION KEYS = ATARI KEYBOARD**, `F2`, `F4` and `F8` go to the game, and saves and screenshots move to `AltGr` + `K`, `L` and `G` (controller hotkeys still send `F2`, `F4` and `F8`). See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="365.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\atarist</code></td></tr><tr><td>TOS</td><td><code>bios</code> (<code>tos.img</code>), <code>bios\hatari\tos</code></td></tr><tr><td>hatarib: copied TOS, TT and Falcon NVRAM</td><td><code>bios\hatarib</code>, <code>bios\hatarib.nvram</code></td></tr><tr><td>hatarib: floppy disks modified by games</td><td><code>saves\atarist</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\atarist\libretro.&#x3C;core></code></td></tr><tr><td>Hatari: save states (one per game)</td><td><code>saves\atarist\hatari</code> (<code>&#x3C;game>.sav</code>, <code>&#x3C;game>.auto.sav</code>)</td></tr><tr><td>Hatari: screenshots</td><td><code>screenshots</code></td></tr><tr><td>Hatari: videos</td><td><code>records\output\hatari</code></td></tr><tr><td>Hatari: configuration and log</td><td><code>emulators\hatari\hatari.cfg</code>, <code>emulators\hatari\hatari.log</code></td></tr></tbody></table>

hatarib never modifies your floppy disks: it writes a copy of the modified disk to `saves\atarist`, and uses it at the next launch. Delete this copy to go back to the original disk. Standalone Hatari writes straight to the disk.

## Guides

### Games on several disks: the m3u file

Create an `.m3u` file that lists the disks, one per line, then launch the `.m3u`. hatarib and Hatari read the same format. Optional lines:

<table><thead><tr><th width="281.5">Line</th><th>Effect</th></tr></thead><tbody><tr><td><code>#AUTO:C:\GAME\GAME.PRG</code></td><td>Starts this program at boot (TOS 1.04 or later).</td></tr><tr><td><code>#RES:low</code>, <code>#RES:med</code>, <code>#RES:high</code></td><td>Resolution at boot.</td></tr><tr><td><code>#BOOTA:2</code>, <code>#BOOTB:0</code></td><td>Disk inserted in drive A or B at boot (1 = first in the list, 0 = empty drive).</td></tr></tbody></table>

Example:

```
Game (Disk 1).st
Game (Disk 2).st
```

With hatarib, change disks from the RetroArch menu (**Disc Control**); SELECT chooses drive A or B. With Hatari, change disks from its menu (HOTKEY + SOUTH).

### Games installed on hard disk (GEMDOS)

Many games exist as « installed » versions, in a folder (hard disk versions). The Atari sees the folder as a hard disk:

1. Put the game folder in `roms\atarist`, for example `roms\atarist\Game`.
2. Next to it, create an empty file with the same name and the `.gem` extension: `roms\atarist\Game.gem`.
3.  To start the game automatically, create a `Game.m3u` file that contains:

    ```
    #AUTO:C:\GAME.PRG
    Game.gem
    ```

    replacing `GAME.PRG` with the game's program, with its path inside the folder.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (619).png" alt=""><figcaption></figcaption></figure></div>

4. Launch the `.m3u` (or the `.gem` without autostart).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (618).png" alt=""><figcaption></figcaption></figure></div>

With standalone Hatari, you can also name the folder `Game.gemdos`, or put a `Game.autorun` file next to the game, with the program to start (`C:\GAME.PRG`).

With hatarib, **EMULATION > HARD DISK BOOT** is automatic: the machine boots from the hard disk when the game has a hard disk and no floppy disk.

### Choosing the machine

By default, RetroBat emulates an **ST** with 1 MB of memory. A few games need an **STE** (STE « enhanced » games, Jaguar pads): **EMULATION > MACHINE TYPE**. With Hatari, choosing TOS 1.06 or the Jaguar pads switches to STE (4 MB) automatically. **EMULATION > MEMORY SIZE** (hatarib) or **RAM SIZE** (hatari) changes the memory.

### High resolution games

High resolution programs (640 × 400, black and white) need Atari's monochrome monitor: **VISUAL RENDERING > MONITOR TYPE > MONOCHROME HIGH RESOLUTION** (hatarib) or **VIDEO > MONITOR TYPE > MONOCHROME** (hatari).

### Other useful options

<table><thead><tr><th width="107">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>hatarib</td><td><strong>EMULATION > FAST FLOPPY ACCESS</strong></td><td>Faster loading (on by default). Turn it off for a protected game that does not start.</td></tr><tr><td>hatarib</td><td><strong>EMULATION > CYCLE EXACT</strong></td><td>Exact emulation, needed by some demos and games (on by default).</td></tr><tr><td>hatarib</td><td><strong>EMULATION > EMUTOS REGION</strong>, <strong>EMUTOS FRAMERATE</strong></td><td>EmuTOS language, 50 Hz or 60 Hz.</td></tr><tr><td>hatarib</td><td><strong>VIDEO > SCREEN BORDERS</strong></td><td>Border size, or picture cropped to 720p / 1080p.</td></tr><tr><td>hatarib</td><td><strong>VIDEO > PIXEL ASPECT RATIO</strong></td><td>Square pixels (default) or original shape (Atari monitor, TV).</td></tr><tr><td>hatarib</td><td><strong>USER INTERFACE > STATUS BAR</strong></td><td>Hatari status bar, or only the drive LED.</td></tr><tr><td>hatari</td><td><strong>EMULATION > FAST BOOT</strong></td><td>Faster TOS boot.</td></tr><tr><td>hatari</td><td><strong>EMULATION > AUTOSAVE</strong></td><td>Saves the game when quitting and resumes it at the next launch.</td></tr></tbody></table>

## Known issues

| Issue                                                           | Solution                                                                                                   |
| --------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Hatari shows « Missing TOS file »                               | Add `tos.img` to `bios`, or `emutos.img` to `bios\hatari\tos`. Or use hatarib, which has EmuTOS built in.  |
| « Panic » message at boot, or the game stops on the GEM desktop | The game is not compatible with EmuTOS: add an original TOS (`tos.img`, preferably TOS 1.02 or 1.04).      |
| A protected `.st` game does not start                           | Turn off **FAST FLOPPY ACCESS**, or use the `.stx` / `.ipf` version of the game.                           |
| The game asks for disk 2                                        | Use an `.m3u` file (see [**Guides**](atari-st.md#games-on-several-disks-the-m3u-file)), then change disks. |
| The joystick does not respond, the mouse moves instead          | The game reads the joystick on port 1 (the mouse port): turn off **USE MOUSE** (hatarib).                  |
| Keys F1 to F10 do not respond in a game (Hatari)                | Set **FUNCTION KEYS** to **ATARI KEYBOARD**.                                                               |
| Black screen with a high resolution program                     | Choose the monochrome monitor (see [**High resolution games**](atari-st.md#high-resolution-games)).        |
