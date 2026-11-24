---
description: Fujitsu
---

# FM-TOWNS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (729).png" alt="" width="479"><figcaption></figcaption></figure></div>

## Overview

The **FM Towns** is a Fujitsu computer released in 1989, in Japan only. It was one of the first computers shipped with a CD-ROM drive as standard. It has an 80386 processor, 32,768 colors, FM and PCM sound, and its own graphical interface, Towns OS. Fujitsu released many models until 1997, and in 1993 a compatible console, the **FM Towns Marty**.

Its library is mostly CD-ROM games, often enhanced versions of games from other machines: Super Street Fighter II, Splatterhouse, Rayxanber, Alltynex, Zak McKracken and the Alien Mindbenders (its only 256-color version), Alone in the Dark, Lemmings…

{% embed url="https://en.wikipedia.org/wiki/FM_Towns" %}

## At a glance

<table><thead><tr><th width="216.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\fmtowns</code></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .d88 .d77 .hdm .xdf .cue .iso .img .mfm .game .cd .chd .zip</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: geartowns</td></tr><tr><td><strong>BIOS</strong></td><td>Required (4 FM Towns ROMs)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (Tsugaru: first controller detected by Windows)</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; MAME with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>geartowns core</td></tr><tr><td><strong>Netplay</strong></td><td>libretro geartowns and mame cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                          | For whom?  | Strengths                                                                                                                                                                                                                                         | Limits                                                                                                                                                      |
| --------------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **libretro: geartowns** (default) | Everyone   | Geartowns, an emulator dedicated to the FM Towns: game database (model, speed and memory chosen automatically), CD-ROM and floppy disks, disk swapping, 2 and 6-button and Marty pads, mouse on a stick, RetroAchievements, netplay, save states. | —                                                                                                                                                           |
| **tsugaru**                       | Purists    | Tsugaru, a very accurate FM Towns emulator.                                                                                                                                                                                                       | No `.chd`, `.m3u` or `.zip`. One controller, not configured. No save states and no RetroBat hotkeys (only HOTKEY + START, to quit). No options in RetroBat. |
| **libretro: mame**                | MAME users | MAME: FM Towns Model 1/2, II UX and Marty, software lists, netplay.                                                                                                                                                                               | Slower and less compatible than geartowns.                                                                                                                  |
| **mame64** (standalone MAME)      | MAME users | Same emulation as the libretro mame core.                                                                                                                                                                                                         | Same limits.                                                                                                                                                |

**If in doubt, keep libretro: geartowns.**

## BIOS

The FM Towns needs 4 ROMs: system, OS, font and dictionary. They are the ROMs of the FM Towns Model 1/2, the base model, used by default.

<table><thead><tr><th width="127.75">File</th><th width="126.25">MAME name</th><th width="337">MD5</th><th>Used by</th></tr></thead><tbody><tr><td><code>FMT_SYS.ROM</code></td><td><code>fmt_sys.rom</code></td><td>feaf8c5675151e00cfe3ad27673bff29</td><td>all</td></tr><tr><td><code>FMT_DOS.ROM</code></td><td><code>fmt_dos.rom</code></td><td>0585b19930d4a7f4c71bcc8a33746588</td><td>all</td></tr><tr><td><code>FMT_FNT.ROM</code></td><td><code>fmt_fnt.rom</code></td><td>eb44f2093f51eb7159f03e170b13af76</td><td>all</td></tr><tr><td><code>FMT_DIC.ROM</code></td><td><code>fmt_dic.rom</code></td><td>34847786d7de94b5d1133c956ab1d75d</td><td>all</td></tr><tr><td><code>FMT_F20.ROM</code></td><td><code>fmt_f20.rom</code></td><td>—</td><td>geartowns, optional (20-dot font)</td></tr></tbody></table>

Where should I put them? Names are accepted in upper or lower case.

<table><thead><tr><th width="407.75">Location</th><th width="106.5">geartowns</th><th width="111">Tsugaru</th><th width="81.5">MAME</th></tr></thead><tbody><tr><td><code>bios\fmtowns\</code> (the 4 files)</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td><code>bios\fmtowns.zip</code> (MAME ROM set)</td><td>✅</td><td>—</td><td>✅</td></tr><tr><td><code>bios\geartowns\</code> (the 4 files)</td><td>✅</td><td>✅</td><td>—</td></tr><tr><td><code>bios\geartowns\fmtowns\</code> or <code>bios\geartowns\fmtowns.zip</code></td><td>✅</td><td>folder only</td><td>—</td></tr></tbody></table>

**The simplest: the 4 files in `bios\fmtowns\`**, which works with all three emulators. The RetroBat BIOS check accepts each of these locations.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (730).png" alt=""><figcaption></figcaption></figure></div>

Other models need their own ROM set:

| Model                                        | ROM set                                              | geartowns | MAME       |
| -------------------------------------------- | ---------------------------------------------------- | --------- | ---------- |
| FM Towns 1F/2F, 10F/20F, II CX, II UX, II UG | `fmtownsux` (II UX)                                  | ✅         | II UX only |
| FM Towns II HG                               | `fmtownshr` (II HR), or else `fmtownsftv` (Fresh TV) | ✅         | —          |
| FM Towns Marty                               | `fmtmarty` (`mrom.m36`, `mrom.m37`)                  | ✅         | ✅          |

Put them as MAME zips in `bios` (`bios\fmtownsux.zip`…) or in `bios\geartowns` (`bios\geartowns\fmtownsux\`…). The BIOS check lists them as optional.

Tsugaru saves the machine settings (CMOS) to a `CMOS.DAT` file, in the ROM folder it uses.

## Which game format?

<table><thead><tr><th width="180.75">Type</th><th width="223">Extensions</th><th>Notes</th></tr></thead><tbody><tr><td>CD-ROM</td><td><code>.cue</code> (with its <code>.bin</code> files), <code>.iso</code>, <code>.chd</code></td><td>Most games. <code>.chd</code>: not with Tsugaru.</td></tr><tr><td>CD-ROM (folder)</td><td><code>.game</code>, <code>.cd</code></td><td>Folder that holds the <code>.cue</code> and its tracks, renamed <code>Game.game</code> or <code>Game.cd</code>. Tsugaru and MAME.</td></tr><tr><td>Floppy disk</td><td><code>.d88</code>, <code>.d77</code>, <code>.hdm</code>, <code>.xdf</code>, <code>.img</code>, <code>.mfm</code></td><td><code>.mfm</code>: not with Tsugaru.</td></tr><tr><td>Several disks</td><td><code>.m3u</code></td><td>List of a game's CDs or floppy disks. geartowns and MAME.</td></tr><tr><td>Archive</td><td><code>.zip</code></td><td>geartowns and MAME.</td></tr></tbody></table>

A few CD games need a floppy disk to save: see [**Guides**](fm-towns.md#games-that-need-a-save-disk).

## Controls

RetroBat configures controllers automatically for geartowns and MAME. The FM Towns pad has two buttons, **A** and **B**, and the **RUN** and **SELECT** keys. The PC mouse is the FM Towns mouse, and the PC keyboard the FM Towns keyboard.

| RetroBat controller | geartowns (original gamepad)    | geartowns (6-button gamepad) | tsugaru (XInput controller) |
| ------------------- | ------------------------------- | ---------------------------- | --------------------------- |
| D-pad               | D-pad                           | D-pad                        | D-pad                       |
| SOUTH               | B                               | B                            | A                           |
| EAST                | A                               | C                            | B                           |
| WEST                | —                               | A                            | RUN                         |
| NORTH               | —                               | Y                            | SELECT                      |
| START               | RUN                             | RUN                          | —                           |
| SELECT              | SELECT                          | SELECT                       | —                           |
| L1                  | —                               | X                            | —                           |
| R1                  | — (Zoom with the Marty gamepad) | Z                            | —                           |

* With geartowns, **CONTROLS > PLAYER 1 / PLAYER 2 CONTROLLER TYPE**: **ORIGINAL GAMEPAD** (port 1 default), **MARTY GAMEPAD**, **6-BUTTON GAMEPAD** (Super Street Fighter II), **MOUSE** (port 2 default), **KEYBOARD**.
* With geartowns, **CONTROLS > ANALOG STICK MOUSE** moves the mouse with the left or right stick (L2 / R2 = buttons). A port must be set to **MOUSE**. **MOUSE SENSITIVITY** and **ANALOG MOUSE SPEED** set the speed.
* Tsugaru uses the first controller detected by Windows (port 1) and the mouse (port 2). Buttons depend on the controller: with an XInput controller, the first 4 buttons are SOUTH, EAST, WEST, NORTH.
* With MAME, **CONTROLS > JOYSTICK TYPE** chooses the emulated controller (**FM Towns 2-button Pad**, **FM Towns 6-button Pad**, **FM Towns Marty Pad**…). Controls follow RetroBat's MAME layout: see the **MAME** page.

With libretro cores, press `Scroll Lock` to turn on RetroArch's **Game Focus**: all keyboard keys go to the FM Towns. To put keyboard keys on the controller, see the [**Pad2Key**](../../../../controllers/pad2key.md) page.

### Hotkeys

libretro cores use the standard RetroArch hotkeys. Standalone MAME uses the common RetroBat hotkeys. With Tsugaru, only HOTKEY + START (quit) works; `Scroll Lock` pauses. See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="316.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\fmtowns</code></td></tr><tr><td>BIOS</td><td><code>bios\fmtowns</code>, <code>bios\geartowns</code>, <code>bios</code> (MAME zips)</td></tr><tr><td>geartowns: CMOS (machine settings)</td><td><code>saves\fmtowns\geartowns.geartowns.cmos</code> (one file per game with <strong>PER GAME CMOS</strong>)</td></tr><tr><td>geartowns: save disks</td><td><code>saves\fmtowns</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\fmtowns\libretro.&#x3C;core></code></td></tr><tr><td>Tsugaru: CMOS</td><td><code>CMOS.DAT</code> in the ROM folder used</td></tr><tr><td>MAME: user disk</td><td><code>saves\mame\fmtowns</code></td></tr><tr><td>Standalone MAME</td><td>See the <a href="../../arcade/mame.md"><strong>MAME</strong></a> page</td></tr></tbody></table>

## Guides

### Model, speed and memory

With geartowns, leave **EMULATION > MODEL**, **CPU SPEED** and **MAIN RAM** on automatic: the core chooses from its game database. A few games benefit from a faster processor (Super Street Fighter II, Alltynex): **CPU SPEED**. **CPU DYNAREC** (on by default) speeds up most games.

With MAME, **EMULATION > MODEL TO EMULATE**: **FM TOWNS (MODEL 1/2) (Default)**, **FM TOWNS II UX** or **FM TOWNS MARTY**. **RAM SIZE**: 2 or 4 MB.

Tsugaru emulates an FM Towns at 33 MHz with 8 MB of memory. The model depends on the ROMs used.

### Games that need a save disk

Some CD games save to a floppy disk, or ask for a system disk.

* geartowns: turn on **EMULATION > SAVE DISK**. A blank floppy disk is added to the disk list, then kept in `saves\fmtowns`. Insert it from the RetroArch menu (**Disc Control**) when the game asks for it.
* MAME: **EMULATION > ADD USER DISK**: **BLANK DISK**, or **SYSTEM DISK** (put the system disk, named after the game with the `.hdm` extension, in `saves\mame\fmtowns`).

### Games on several disks

Create an `.m3u` file that lists the CDs or floppy disks, one per line, then launch the `.m3u`. With geartowns, change disks from the RetroArch menu (**Disc Control**). **EMULATION > DISK CONTROL DRIVE** chooses the floppy drive, **FLOPPY MULTIDRIVE** also inserts the next floppy disk into drive 2.

### RetroAchievements

The geartowns core is compatible. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="145.75">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>geartowns</td><td><strong>EMULATION > CD READ SPEED</strong>, <strong>PRELOAD CD-ROM</strong></td><td>Faster loading. Some games do not like a faster drive.</td></tr><tr><td>geartowns</td><td><strong>EMULATION > PER GAME CMOS</strong></td><td>Separate machine settings for each game (recommended for netplay).</td></tr><tr><td>geartowns</td><td><strong>EMULATION > BOOT DEVICE</strong></td><td>Forces booting from the CD, a floppy disk or a hard disk (1F/2F and later models).</td></tr><tr><td>geartowns</td><td><strong>VIDEO > GAME ASPECT RATIO (CORE)</strong></td><td>4:3 (default), square pixels, 16:9, 16:10.</td></tr><tr><td>geartowns</td><td><strong>VIDEO > FRAMESKIP</strong></td><td>Avoids sound crackling on a slow PC.</td></tr><tr><td>geartowns</td><td><strong>CONTROLS > ALLOW OPPOSING DIRECTIONS</strong></td><td>Left + right or up + down at the same time.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="357.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start, missing firmware message (geartowns)</td><td>The 4 ROMs are missing, or they are not in a location that is read (see <a href="fm-towns.md#bios"><strong>BIOS</strong></a>). For another model than the Model 1/2, add its ROM set.</td></tr><tr><td>Tsugaru does not start</td><td>The ROMs are not in a folder (Tsugaru does not read zips), or the game is a <code>.chd</code>, <code>.m3u</code> or <code>.zip</code>.</td></tr><tr><td>The game asks for a floppy disk</td><td>See <a href="fm-towns.md#games-that-need-a-save-disk"><strong>Games that need a save disk</strong></a>.</td></tr><tr><td>The game stutters or the sound crackles</td><td>Keep <strong>CPU DYNAREC</strong> on. On a slow PC, turn on <strong>FRAMESKIP</strong>.</td></tr><tr><td>A fighting game is missing moves</td><td>Set <strong>PLAYER 1 CONTROLLER TYPE</strong> to <strong>6-BUTTON GAMEPAD</strong>.</td></tr><tr><td>Keyboard keys trigger RetroArch hotkeys</td><td>Press <code>Scroll Lock</code> (Game Focus).</td></tr></tbody></table>
