---
description: Commodore
---

# Amiga CD32

<div align="left"><figure><img src="../../../../.gitbook/assets/amigacd32.png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Amiga CD32** is the games console of the Amiga range, released by Commodore in September 1993. Billed as the first 32-bit CD console in Europe, it is built on the Amiga 1200: Motorola 68EC020 processor, **AGA** chipset, 2 MB of memory, plus a double-speed CD-ROM drive and the Akiko chip, which speeds up some 3D effects. Its pad has 7 buttons: four coloured buttons (red, blue, green, yellow), two shoulder buttons (rewind, fast forward) and Play.

The CD32 got about 150 games. Many are Amiga 1200 games with CD music, intros or voices: _Microcosm_, _Super Stardust_, _Banshee_, _Guardian_, _Liberation_, _Fears_, _The Chaos Engine_, _Beneath a Steel Sky_ with full speech… Commodore went bankrupt in April 1994, only a few months after the launch.

{% embed url="https://en.wikipedia.org/wiki/Amiga_CD32" %}

## At a glance

<table><thead><tr><th width="242.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\amigacd32</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .chd .iso .ccd .nrg .mds .lha .rp9 .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: puae</td></tr><tr><td><strong>BIOS</strong></td><td><code>kick40060.CD32</code> + <code>kick40060.CD32.ext</code> (or <code>amiga-os-310-cd32.rom</code> + <code>amiga-os-310-cd32-ext.rom</code>)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, except Amiga Forever</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, Amiberry</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator to choose?

| Emulator                     | Strengths                                                     | Limits                                                     |
| ---------------------------- | ------------------------------------------------------------- | ---------------------------------------------------------- |
| **libretro: puae** (default) | Reliable, full CD32 pad, CD options, one save file per game   |                                                            |
| libretro: amiberry           | Recent UAE engine, .rp9 support                               | CD32 pad not emulated: only fire buttons 1 and 2 (no Play) |
| amiberry                     | Standalone version: full CD32 pad, Amiberry menu              |                                                            |
| winuae                       | The reference Amiga emulator, the most accurate               |                                                            |
| amigaforever                 | Plays the .rp9 packages of Cloanto's commercial Amiga Forever | Amiga Forever must be installed, no autoconfig             |

## BIOS

### Required files

The CD32 needs **two** ROMs: its Kickstart and its extended ROM. Copy them to the `bios` folder (or `bios\amiga`).

| File                  | Short name         | Amiga Forever name        | MD5 (short name)                 | Used for                                |
| --------------------- | ------------------ | ------------------------- | -------------------------------- | --------------------------------------- |
| CD32 Kickstart 3.1    | kick40060.CD32     | amiga-os-310-cd32.rom     | 5f8924d013dd57a89cf349f4cdedc6b1 | **Required**                            |
| CD32 extended ROM     | kick40060.CD32.ext | amiga-os-310-cd32-ext.rom | bb72565701b1b6faece07d68ea5da639 | **Required**                            |
| Kickstart 3.1 (A1200) | kick40068.A1200    | amiga-os-310-a1200.rom    | 646773759326fbac3b2311fd8c8793ee | Optional – WHDLoad games (.lha)         |
| Amiga Forever key     | rom.key            |                           |                                  | Optional – encrypted Amiga Forever ROMs |

{% hint style="info" %}
RetroBat checks that both CD32 files are present. The other files are listed as OPTIONAL.
{% endhint %}

### Which file name should I use?

* The **short names** (`kick40060.CD32`, `kick40060.CD32.ext`) work with every emulator: use them if you are not sure.
* The Amiga Forever ROMs are encrypted: copy the **rom.key** file supplied with Amiga Forever next to them.
* Some packs contain a single 1 MB "combined" CD32 ROM. Only lr-puae reads it: prefer the two separate files.

### Choosing the CD32 model

By default, RetroBat emulates a standard CD32 (2 MB of memory). Some games run better with 8 MB of extra Fast RAM (EMULATION submenu):

<table><thead><tr><th width="164.5">Emulator</th><th>Option</th><th>Choices</th></tr></thead><tbody><tr><td>lr-puae</td><td>MODEL</td><td>CD32, CD32 + 8 MB Fast</td></tr><tr><td>lr-amiberry</td><td>MODEL</td><td>CD32, CD32 + 8 MB Fast</td></tr><tr><td>Amiberry</td><td>MODEL</td><td>CD32, CD32 + 8 MB Fast</td></tr><tr><td>WinUAE</td><td>FAST RAM / ENABLE JIT / USE FPU</td><td>+8 MB Fast RAM, JIT and FPU</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (454).png" alt=""><figcaption></figcaption></figure></div>

## Game formats

### Formats

<table><thead><tr><th width="186.5">Format</th><th>Description</th></tr></thead><tbody><tr><td>.chd</td><td>Compressed CD image, one file per game, keeps the CD audio tracks. <strong>Recommended</strong></td></tr><tr><td>.cue (+ .bin)</td><td>CD image with its audio tracks</td></tr><tr><td>.iso</td><td>Data-only CD image: the CD music is missing</td></tr><tr><td>.ccd / .nrg / .mds</td><td>Other CD image formats (CloneCD, Nero, Alcohol)</td></tr><tr><td>.lha</td><td><strong>WHDLoad</strong> version of a CD32 game</td></tr><tr><td>.rp9</td><td>Amiga Forever package (Amiga Forever, lr-amiberry, lr-puae)</td></tr><tr><td>.zip / .7z</td><td>Compressed CD images, <strong>libretro cores only</strong></td></tr></tbody></table>

{% hint style="success" %}
Prefer **.chd**: one file per game, smaller, with the CD music. To convert a .cue/.bin game, use `chdman createcd -i "game.cue" -o "game.chd"`.
{% endhint %}

## Controls

### Controller autoconfiguration

| Emulator      | Autoconfig | Players |
| ------------- | ---------- | ------- |
| lr-puae       | Yes        | 2       |
| lr-amiberry   | Yes        | 2       |
| Amiberry      | Yes        | 2       |
| WinUAE        | Yes        | 2       |
| Amiga Forever | No         |         |

Player 1's controller goes to port 2 of the console, player 2's controller to port 1.

### Default layout

| CD32 pad                 | lr-puae, Amiberry |
| ------------------------ | ----------------- |
| D-pad                    | D-pad             |
| Red                      | SOUTH             |
| Blue                     | EAST              |
| Green                    | WEST              |
| Yellow                   | NORTH             |
| Rewind                   | L1                |
| Fast forward             | R1                |
| Play                     | START             |
| Virtual keyboard         | SELECT            |
| Emulator menu (Amiberry) | R3                |

<div align="left"><figure><img src="../../../../.gitbook/assets/amigacd32 (1).png" alt="" width="225"><figcaption></figcaption></figure></div>

WinUAE also emulates the full CD32 pad. With lr-amiberry, only the red and blue buttons work for now.

### Useful control options

<table><thead><tr><th width="117">Emulator</th><th>Option</th><th>Description</th></tr></thead><tbody><tr><td>lr-puae</td><td>PAD BUTTON LAYOUT</td><td>Rotate the face buttons and/or make the blue button jump (up)</td></tr><tr><td>lr-puae</td><td>PLAYER 1 CONTROLLER TYPE</td><td>Leave it on AUTO: the CD32 pad is selected automatically</td></tr><tr><td>Amiberry</td><td>CONTROLLER TYPE</td><td>CD32 pad by default on this system</td></tr><tr><td>Amiberry</td><td>PORT 1 DEVICE</td><td>Joystick (player 2), mouse or nothing in the second port</td></tr><tr><td>WinUAE</td><td>PAD MODE / SECOND CONTROLLER</td><td>CD32 pad or joystick, player 2 or mouse in the second port</td></tr></tbody></table>

### Hotkeys

**libretro cores**: [standard RetroBat hotkeys](../../../../navigation/hotkeys.md).

<table><thead><tr><th>Hotkey</th><th width="149">Amiberry</th><th width="166.75">WinUAE</th><th>Amiga Forever</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td><td>Quit</td><td></td></tr><tr><td>HOTKEY + WEST</td><td>Save state</td><td></td><td></td></tr><tr><td>HOTKEY + NORTH</td><td>Load state</td><td></td><td></td></tr></tbody></table>

START alone is the Play button of the CD32 pad. The Amiberry menu opens with R3 or F12, the WinUAE menu with F12.

## Folders

<table><thead><tr><th width="139.5">Emulator</th><th>Content</th><th>Folder</th></tr></thead><tbody><tr><td>lr-puae</td><td>Game saves (NVRAM, one file per game)</td><td><code>saves\amigacd32</code></td></tr><tr><td>lr-amiberry</td><td>Game saves</td><td><code>saves\amigacd32\LR-amiberry</code></td></tr><tr><td>libretro</td><td>Save states</td><td><code>saves\amigacd32\libretro.&#x3C;core></code></td></tr><tr><td>Amiberry</td><td>Save states, game saves (NVRAM)</td><td><code>saves\amigacd32\amiberry</code></td></tr><tr><td>Amiberry</td><td>Screenshots</td><td><code>screenshots\amiberry</code></td></tr><tr><td>WinUAE</td><td>Save states</td><td><code>saves\amigacd32\winuae</code></td></tr><tr><td>WinUAE</td><td>Game saves (NVRAM)</td><td><code>saves\amigacd32\winuae\nvram</code></td></tr><tr><td>WinUAE</td><td>Screenshots / videos</td><td><code>screenshots\winuae</code> / <code>records\winuae</code></td></tr></tbody></table>

## Guides

### Game saves

CD32 games save to the small internal memory of the console (NVRAM). Each emulator keeps it in its own saves folder: switching emulators does not bring your saves with you. With lr-puae, each game gets its own save file, so the memory never fills up.

### WHDLoad games

Some CD32 games also exist as WHDLoad versions (.lha). They start like an Amiga 1200 and need the Kickstart 3.1 (A1200). You can also put them in the Amiga AGA system: see the Amiga 1200 page.

## Known issues

<table><thead><tr><th width="321.5">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>"Kickstart not found" or black screen</td><td>Copy kick40060.CD32 <strong>and</strong> kick40060.CD32.ext to the bios folder.</td></tr><tr><td>Amiga Forever ROMs do not work</td><td>Copy rom.key next to them.</td></tr><tr><td>No music in the game</td><td>The .iso format has no CD audio: use a .cue/.bin or .chd image.</td></tr><tr><td>The game stays on the CD32 logo or does not load</td><td>With lr-puae, enable CD INSERT DELAY. Otherwise try the CD32 + 8 MB Fast model or another emulator.</td></tr><tr><td>Play, green or yellow button does nothing</td><td>lr-amiberry does not emulate the CD32 pad yet: use lr-puae, Amiberry or WinUAE.</td></tr><tr><td>A .zip/.7z game does not start</td><td>Only the libretro cores read archives: extract it, or convert it to .chd.</td></tr><tr><td>Saves are missing after changing emulator</td><td>Each emulator has its own saves: go back to the previous emulator.</td></tr></tbody></table>
