---
description: Fujitsu
---

# FM-7

<div align="left"><figure><img src="../../../../.gitbook/assets/image (728).png" alt="" width="300"><figcaption></figcaption></figure></div>

## Overview

The **FM-7** (Fujitsu Micro 7) is a Fujitsu computer released in 1982, in Japan. It has two Motorola 6809 processors: one runs the programs, the other handles the display. It was followed by the **FM-77AV** (1985), with 4,096 colors and FM sound. The FM Towns succeeded it in 1989.

Its library is mostly tape and floppy disk games, often adventure and role-playing games: Thexder, Xanadu, Hydlide, Ys…

{% embed url="https://en.wikipedia.org/wiki/FM-7" %}

## At a glance

<table><thead><tr><th width="239"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\fm7</code></td></tr><tr><td><strong>Extensions</strong></td><td>.wav .t77 .mfi .dfi .hfe .mfm .td0 .imd .d77 .d88 .1dd .cqm .cqi .dsk .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mame</td></tr><tr><td><strong>BIOS</strong></td><td><code>fm7.zip</code> (<code>fm77av.zip</code> for the FM-77AV)</td></tr><tr><td><strong>Controller setup</strong></td><td>Keyboard; Pad2Key for the controller</td></tr><tr><td><strong>Save states</strong></td><td>libretro core; MAME with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>libretro mame core</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                     | For whom?  | Strengths                                                                      | Limits                    |
| ---------------------------- | ---------- | ------------------------------------------------------------------------------ | ------------------------- |
| **libretro: mame** (default) | Everyone   | MAME in RetroArch: FM-7 and FM-77AV, tapes started automatically, save states. | —                         |
| **mame64** (standalone MAME) | MAME users | Same emulation, with the MAME menu.                                            | Save states with hotkeys. |

**If in doubt, keep libretro: mame.**

## BIOS

MAME needs the ROM set of the emulated model, in MAME format, of the same version as RetroBat's MAME emulator.

<table><thead><tr><th width="259.5">File</th><th width="153.25">Folder</th><th>Used by</th></tr></thead><tbody><tr><td><code>fm7.zip</code></td><td><code>bios</code></td><td>FM-7 (default model)</td></tr><tr><td><code>fm77av.zip</code></td><td><code>bios</code></td><td>FM-77AV (<strong>MODEL TO EMULATE = FM-77AV</strong>), optional</td></tr><tr><td><code>fm7_cass.xml</code>, <code>fm7_disk.xml</code>, <code>fm77av.xml</code></td><td><code>bios\mame\hash</code></td><td>MAME software lists (shipped with RetroBat), for <strong>FORCE SOFTLIST</strong></td></tr></tbody></table>

The RetroBat BIOS check asks for `fm7.zip` and lists the other files as optional.

## Which game format?

<table><thead><tr><th width="125.75">Type</th><th>Extensions</th><th>Notes</th></tr></thead><tbody><tr><td>Tape</td><td><code>.t77</code>, <code>.wav</code></td><td>RetroBat starts the tape automatically (<code>LOADM"",,R</code> command typed after 5 seconds).</td></tr><tr><td>Floppy disk</td><td><code>.d77</code>, <code>.d88</code>, <code>.mfi</code>, <code>.dfi</code>, <code>.hfe</code>, <code>.mfm</code>, <code>.td0</code>, <code>.imd</code>, <code>.1dd</code>, <code>.cqm</code>, <code>.cqi</code>, <code>.dsk</code></td><td><code>.d77</code> is the most common. The machine boots from the disk.</td></tr></tbody></table>

Files can be compressed as `.zip` or `.7z`. Games written for the FM-77AV only work on an FM-77AV: see [**Guides**](fm-7.md#fm-7-or-fm-77av).

## Controls

The FM-7 has no standard controller: most games are played with the keyboard, with the numeric keypad for directions. The PC keyboard is the FM-7 keyboard.

* To play with a controller, put keyboard keys on the controller with **Pad2Key** (see the [**Pad2Key**](../../../../controllers/pad2key.md) page).
* With the libretro mame core, press `Scroll Lock` to turn on RetroArch's **Game Focus**: all keys go to the FM-7.
* With standalone MAME, `Scroll Lock` toggles between the full emulated keyboard and the MAME keys.

### Hotkeys

The libretro mame core uses the standard RetroArch hotkeys. Standalone MAME uses the common RetroBat hotkeys. See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

| Content                         | Folder                                        |
| ------------------------------- | --------------------------------------------- |
| Games                           | `roms\fm7`                                    |
| BIOS                            | `bios` (`fm7.zip`, `fm77av.zip`)              |
| MAME software lists             | `bios\mame\hash`                              |
| libretro mame core: save states | `saves\fm7\libretro.mame`                     |
| Standalone MAME                 | See the [**MAME**](../../arcade/mame.md) page |

## Guides

### FM-7 or FM-77AV?

By default, RetroBat emulates an FM-7. Games written for the FM-77AV (more colors, FM sound) need **EMULATION > MODEL TO EMULATE = FM-77AV**, and the `fm77av.zip` file in `bios`.

### Starting a tape or a floppy disk

RetroBat chooses the media from the extension: tape for `.t77` and `.wav`, floppy disk for the others. If the game is not recognized (`.zip` archive, for example), **EMULATION > FORCE MEDIA TYPE** chooses **Cassette**, **Disk (Drive 1)** or **Disk (Drive 2)**.

### Software lists

**EMULATION > FORCE SOFTLIST** starts the game from a MAME software list (**Fujitsu FM-7 disk images**, **Fujitsu FM-7 cassettes**, **Fujitsu FM-77AV disk images**). The file must then have the game's short name in that list.

## Known issues

<table><thead><tr><th width="349">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>MAME does not start or asks for files</td><td><code>fm7.zip</code> is missing from <code>bios</code>, or it does not match the MAME version. For the FM-77AV, add <code>fm77av.zip</code>.</td></tr><tr><td>A tape does not start</td><td>Wait a few seconds for the command to be typed. Otherwise, type <code>LOADM"",,R</code> then Enter.</td></tr><tr><td>The game shows wrong colors or crashes</td><td>It is an FM-77AV game: see <a href="fm-7.md#fm-7-or-fm-77av"><strong>FM-7 or FM-77AV?</strong></a>.</td></tr><tr><td>Keyboard keys trigger RetroArch hotkeys</td><td>Press <code>Scroll Lock</code> (Game Focus).</td></tr></tbody></table>
