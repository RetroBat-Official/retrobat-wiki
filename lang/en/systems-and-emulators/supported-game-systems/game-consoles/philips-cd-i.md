---
description: Philips
---

# Philips CD-i

<div align="left"><figure><img src="../../../.gitbook/assets/image (590).png" alt="" width="288"><figcaption></figcaption></figure></div>

## Overview

The **CD-i** (Compact Disc Interactive) is a Philips multimedia player released in 1991. Designed for the living room as much as for education, it plays game, encyclopedia and music CDs. The **Digital Video Cartridge**, a cartridge inserted at the back, adds MPEG video decoding: it is needed by full-motion video (FMV) games and Video CDs. Philips discontinued the CD-i in 1998.

Its games include **Hotel Mario**, **Link: The Faces of Evil**, **Zelda: The Wand of Gamelon**, **Burn:Cycle**, **The 7th Guest**, **Dragon's Lair**, **Mad Dog McCree**, **Space Ace**, **Lemmings** and **Tetris**.

RetroBat offers five emulators: the **same\_cdi** (default), **zcdi** and **mame** libretro cores, **OpenCDi** and **MAME**.

{% embed url="https://en.wikipedia.org/wiki/CD-i#Philips_models" %}

## At a glance

<table><thead><tr><th width="210.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\cdi</code></td></tr><tr><td><strong>Extensions</strong></td><td>.chd .cue .toc .nrg .gdi .iso .cdr .m3u</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: same_cdi</td></tr><tr><td><strong>BIOS</strong></td><td><code>cdimono1.zip</code> in <code>bios</code></td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic: libretro cores, OpenCDi; MAME: PadToKey</td></tr><tr><td><strong>Save states</strong></td><td>zcdi core, mame core, OpenCDi (managed by RetroBat)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>zcdi and mame cores</td></tr><tr><td><strong>Light guns</strong></td><td>zcdi core (Peacekeeper, port 1)</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>vmpega.rom</code> (Digital Video Cartridge) for FMV games with zcdi and OpenCDi</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="179.5">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: same_cdi</strong> (default)</td><td>MAME emulation dedicated to the CD-i, adjustable internal resolution.</td><td>No FMV games (Digital Video Cartridge not emulated), no save states.</td></tr><tr><td><strong>libretro: zcdi</strong></td><td>FMV games with <code>vmpega.rom</code>, save states, netplay, Peacekeeper light gun, mouse, two players, disk swapping (<code>.m3u</code>).</td><td>Cannot read <code>.toc</code>, <code>.nrg</code>, <code>.gdi</code> and <code>.cdr</code> files.</td></tr><tr><td><strong>libretro: mame</strong></td><td>Full MAME emulation, save states, netplay.</td><td>No FMV games, no automatic controller setup.</td></tr><tr><td><strong>opencdi</strong></td><td>Recent standalone emulator: FMV games, save states managed by RetroBat, mouse, video levels.</td><td>Cannot read <code>.toc</code>, <code>.nrg</code>, <code>.gdi</code> and <code>.cdr</code> files. Picks PAL or NTSC from the file name.</td></tr><tr><td><strong>mame</strong></td><td>Same emulation as the mame core, as a standalone emulator.</td><td>No FMV games, no automatic controller setup.</td></tr></tbody></table>

## BIOS

A single file is enough for every emulator: `cdimono1.zip` (MAME ROM set), in `bios`. RetroBat copies it, or extracts from it the files each emulator needs.

<table><thead><tr><th width="194.5">Emulator</th><th>Files</th><th>Folder</th></tr></thead><tbody><tr><td>same_cdi</td><td><code>cdimono1.zip</code> (copied automatically from <code>bios</code> when missing)</td><td><code>bios\same_cdi\bios</code></td></tr><tr><td>mame core, MAME</td><td><code>cdimono1.zip</code></td><td><code>bios</code> or <code>bios\same_cdi\bios</code></td></tr><tr><td>zcdi</td><td><code>cdi200.rom</code> (NTSC), <code>cdi220b.rom</code> (PAL), extracted automatically from <code>cdimono1.zip</code>; <code>vmpega.rom</code> for FMV games</td><td><code>bios</code></td></tr><tr><td>OpenCDi</td><td><code>cdimono1.zip</code> or <code>cdibios.zip</code>, or <code>cdi220b.rom</code> / <code>cdi200.rom</code>; <code>vmpega.rom</code> for FMV games (loose or inside <code>cdimono1.zip</code>)</td><td><code>bios</code> or <code>bios\same_cdi\bios</code></td></tr></tbody></table>

The MAME software list `cdi.xml` goes in `bios\mame\hash` (optional).

<details>

<summary>Content of cdimono1.zip and md5</summary>

```
cdimono1.zip
- cdi200.rom "2969341396aa61e0143dc2351aaa6ef6"
- cdi220.rom "ac80a92c988ce07fbd6a8f21ded34cf1"
- cdi220b.rom "ac0d468be366779c9df633be98da250a"
- zx405037p__cdi_servo_2.1__b43t__llek9215.mc68hc705c8a_withtestrom.7201 "3e59b8a9a423d3ecd612a32fe4e2d748"
- zx405042p__cdi_slave_2.0__b43t__zzmk9213.mc68hc705c8a_withtestrom.7206 "3d20cf7550f1b723158b42a1fd5bac62"

vmpega.rom "53ba3bf7443187a657baa272d01d3771"

```

</details>

## Which game format?

<table><thead><tr><th width="229">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.chd</strong></td><td>Compressed image, read by every emulator. The recommended format.</td></tr><tr><td><strong>.cue</strong> (+ .bin)</td><td>Standard CD image, read by every emulator.</td></tr><tr><td><strong>.iso</strong></td><td>CD image, read by every emulator.</td></tr><tr><td><strong>.toc</strong>, <strong>.nrg</strong>, <strong>.gdi</strong>, <strong>.cdr</strong></td><td>Only read by same_cdi and MAME.</td></tr><tr><td><strong>.m3u</strong></td><td>List of the discs of a multi-disc game (see <a href="philips-cd-i.md#multi-disc-games"><strong>Guides</strong></a>).</td></tr></tbody></table>

## Controls

### Automatic setup

The CD-i controller has a d-pad (or a thumbpad) moving a cursor and two action buttons.

| RetroBat controller | same\_cdi | zcdi          | OpenCDi  |
| ------------------- | --------- | ------------- | -------- |
| D-pad, left stick   | Cursor    | Cursor        | Cursor   |
| SOUTH               | Button 1  | Button 1      | Button 1 |
| EAST                | Button 2  | Button 2      | Button 2 |
| NORTH               | —         | Button 1      | —        |
| WEST                | —         | Buttons 1 + 2 | Button 2 |
| START               | —         | —             | Button 1 |

With the mame core and MAME, RetroBat does not set up the controller: use the MAME configuration or a **PadToKey** profile (see the [**PadToKey**](../../../controllers/pad2key.md) page).

### Mouse and second player

* **zcdi core**: **CONTROLS > PLAYER 1 CONTROLLER TYPE**: gamepad (default) or mouse. **PLAYER 2 CONTROLLER TYPE**: none, gamepad or mouse; a second gamepad is used automatically when connected.
* **OpenCDi**: **CONTROLS > POINTING DEVICE**: gamepad (the controller and the keyboard move the cursor) or mouse (the PC mouse moves the cursor, the controller only keeps its buttons). **HOTKEY + L3** switches mode in game. **MOUSE SENSITIVITY** sets the cursor speed.

### Light guns

The zcdi core emulates the **Peacekeeper** light gun on port 1 (American Laser Games titles such as **Mad Dog McCree**). Enable **GUNS > ENABLE GUN**. For more details, see the [**Light guns**](../../../controllers/supported-controllers/lightguns/) page.

### Hotkeys

**libretro cores, MAME**: usual RetroArch / RetroBat hotkeys (save, load, disk swap…). For more details, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

**OpenCDi**

<table><thead><tr><th width="285.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td><strong>HOTKEY + SOUTH</strong></td><td>Pause</td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Save state</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Load state</td></tr><tr><td><strong>HOTKEY + d-pad up / down</strong></td><td>Next / previous save slot</td></tr><tr><td><strong>HOTKEY + L3</strong></td><td>Switch gamepad / mouse</td></tr><tr><td><strong>HOTKEY + R3</strong></td><td>Screenshot</td></tr></tbody></table>

## Folders

| Content                                         | Folder                                |
| ----------------------------------------------- | ------------------------------------- |
| BIOS                                            | `bios`                                |
| same\_cdi: BIOS                                 | `bios\same_cdi\bios`                  |
| MAME software list                              | `bios\mame\hash`                      |
| zcdi and mame cores: save states                | `saves\cdi\libretro.<core>`           |
| zcdi core: console memory (NVRAM, one per disc) | `saves\cdi`                           |
| OpenCDi: console memory (one per game)          | `saves\cdi\opencdi\nvram`             |
| OpenCDi: console memory (shared)                | `saves\cdi\opencdi\nvram_mk48t08.bin` |
| OpenCDi: save states                            | `saves\cdi\opencdi`                   |
| OpenCDi: screenshots                            | `screenshots`                         |

## Guides

### FMV games (Digital Video Cartridge)

Full-motion video games (**Dragon's Lair**, **Space Ace**, **Mad Dog McCree**, **Who Shot Johnny Rock?**, **Burn:Cycle**…) and Video CDs need the Digital Video Cartridge. Only **zcdi** and **OpenCDi** emulate it, with the `vmpega.rom` file in `bios`:

* **zcdi** uses it automatically when the file is present;
* **OpenCDi** also looks for it inside `cdimono1.zip`; **EMULATION > DIGITAL VIDEO CARTRIDGE** removes it.

With same\_cdi, the mame core and MAME, these games do not start: pick zcdi or OpenCDi for them.

### Multi-disc games

Create a `.m3u` file in `roms\cdi`, with one line per disc, in order:

```
Burn Cycle (Europe) (Disc 1).chd
Burn Cycle (Europe) (Disc 2).chd
```

* **zcdi core**: swap discs with the RetroArch hotkeys.
* **OpenCDi** boots the first disc; the next ones are inserted in game with `Ctrl` + `I`. With **CONSOLE MEMORY (NVRAM) > PER GAME**, every disc shares the same memory.

### Starting the game

Like a real player, the CD-i can stop on its menu: **PLAY CD-I** then has to be chosen to start the disc.

* **zcdi core**: **EMULATION > AUTO PLAY** (on by default) starts the disc directly.
* **OpenCDi** starts the disc directly.
* **same\_cdi, mame core, MAME**: if the menu shows up, select **PLAY CD-I** with the cursor, then press button 1.

### Other useful options

| Option                                           | Effect                                                                     |
| ------------------------------------------------ | -------------------------------------------------------------------------- |
| **INTERNAL RESOLUTION** (same\_cdi)              | Sharper picture, from 640x480 (native) to 3840x2160.                       |
| **EMULATION > THROTTLE** (same\_cdi)             | Enable it if the game runs too fast on a high refresh rate display.        |
| **EMULATION > REGION** (zcdi)                    | NTSC (`cdi200.rom`) or PAL (`cdi220b.rom`).                                |
| **EMULATION > CONSOLE MEMORY (NVRAM)** (OpenCDi) | One memory per game (never full) or one shared memory as on a real player. |
| **VISUAL RENDERING > VIDEO LEVELS** (OpenCDi)    | Studio (dark grey black, as on a period TV) or full range (deep black).    |

## Known issues

| Issue                                                                  | Solution                                                                                                                  |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| An FMV game (Dragon's Lair, Mad Dog McCree…) does not start            | Use zcdi or OpenCDi, with `vmpega.rom` in `bios`.                                                                         |
| The game stays on the CD-i menu                                        | Choose **PLAY CD-I**, or use zcdi / OpenCDi, which start the disc directly.                                               |
| OpenCDi starts an American game in PAL                                 | OpenCDi picks NTSC when the file name contains `(USA)`, `(Japan)` or `NTSC`: keep the No-Intro / Redump name of the game. |
| A `.toc`, `.nrg`, `.gdi` or `.cdr` does not start with zcdi or OpenCDi | Convert the game to `.chd`, or use same\_cdi.                                                                             |
| OpenCDi reports a missing BIOS                                         | Place `cdimono1.zip` (or `cdi220b.rom`) in `bios`.                                                                        |
