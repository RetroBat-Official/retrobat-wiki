---
description: Commodore
---

# Amiga CDTV

<div align="left"><figure><img src="../../../../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Amiga CDTV** (Commodore Dynamic Total Vision) is Commodore's multimedia player, released in 1991. Shaped like a hi-fi unit to sit under a TV, it is an Amiga 500 (Motorola 68000, 1 MB of memory) with a single-speed CD-ROM drive, an infrared remote control and a Kickstart extended with the CDTV ROM. A keyboard, a mouse and a floppy drive were sold as extras.

The CDTV got about a hundred titles, many of them encyclopedias and educational programs, but also games, often Amiga games with CD music and voices: _Defender of the Crown_, _Lemmings_, _Battle Chess_, _Sim City_, _Wrath of the Demon_, _Psycho Killer_… It was a commercial failure, and Commodore replaced it with the CD32 in 1993.

{% embed url="https://en.wikipedia.org/wiki/Commodore_CDTV" %}

## At a glance

<table><thead><tr><th width="254"></th><th></th></tr></thead><tbody><tr><td>Games folder</td><td>📁 roms \ 📂 amigacdtv</td></tr><tr><td>File extensions</td><td>.cue .chd .iso .ccd .nrg .mds .m3u .rp9 .zip .7z</td></tr><tr><td>Default emulator</td><td>libretro: puae</td></tr><tr><td>BIOS</td><td>Kickstart 1.3 and CDTV extended ROM required</td></tr><tr><td>Controller autoconfig</td><td>Yes (except Amiga Forever)</td></tr><tr><td>RetroAchievements</td><td>No</td></tr><tr><td>Netplay</td><td>No</td></tr><tr><td>Save state manager (ES)</td><td>libretro cores, Amiberry</td></tr></tbody></table>

## Which emulator to choose?

| Emulator                     | Strengths                                                     | Limits                                         |
| ---------------------------- | ------------------------------------------------------------- | ---------------------------------------------- |
| **libretro: puae** (default) | Reliable, virtual keyboard, Pad2Key, one save file per title  |                                                |
| libretro: amiberry           | Recent UAE engine, .rp9 support                               |                                                |
| amiberry                     | Standalone version, CDTV remote emulation, Amiberry menu      | Multi-disc .m3u: first disc only               |
| winuae                       | The reference Amiga emulator, the most accurate               |                                                |
| amigaforever                 | Plays the .rp9 packages of Cloanto's commercial Amiga Forever | Amiga Forever must be installed, no autoconfig |

## BIOS

The CDTV needs **two** ROMs: the Kickstart 1.3 and the CDTV extended ROM. Copy them to the `bios` folder (or `bios\amiga`).

| File              | Short name     | Amiga Forever name        | MD5 (short name)                 | Used for                                |
| ----------------- | -------------- | ------------------------- | -------------------------------- | --------------------------------------- |
| Kickstart 1.3     | kick34005.A500 | amiga-os-130.rom          | 82a21c1890cae844b3df741f2762d48d | **Required**                            |
| CDTV extended ROM | kick34005.CDTV | amiga-os-130-cdtv-ext.rom | 89da1838a24460e4b93f4f0c5d92d48d | **Required**                            |
| Amiga Forever key | rom.key        |                           |                                  | Optional – encrypted Amiga Forever ROMs |

{% hint style="info" %}
RetroBat checks that both files are present. The Kickstart 1.3 is the same as for the Amiga 500.
{% endhint %}

* The **short names** work with every emulator: use them if you are not sure.
* The Amiga Forever ROMs are encrypted: copy the **rom.key** file supplied with Amiga Forever next to them.

RetroBat always emulates a standard CDTV (68000, 1 MB of Chip RAM): there is no model to choose.

## Game formats

<table><thead><tr><th width="184">Format</th><th>Description</th></tr></thead><tbody><tr><td>.chd</td><td>Compressed CD image, one file per title, keeps the CD audio tracks. <strong>Recommended</strong></td></tr><tr><td>.cue (+ .bin)</td><td>CD image with its audio tracks</td></tr><tr><td>.iso</td><td>Data-only CD image: the CD music is missing</td></tr><tr><td>.ccd / .nrg / .mds</td><td>Other CD image formats (CloneCD, Nero, Alcohol)</td></tr><tr><td>.m3u</td><td>Multi-disc title</td></tr><tr><td>.rp9</td><td>Amiga Forever package (Amiga Forever, lr-amiberry, lr-puae)</td></tr><tr><td>.zip / .7z</td><td>Compressed CD images, <strong>libretro cores only</strong></td></tr></tbody></table>

{% hint style="success" %}
Prefer **.chd**: one file per title, smaller, with the CD music. To convert a .cue/.bin title, use `chdman createcd -i "game.cue" -o "game.chd"`.
{% endhint %}

## Controls

### Controller autoconfiguration

The CDTV works like an Amiga 500: the **joystick** is in port 2 and the **mouse** in port 1. Player 1's controller goes to port 2 and your PC mouse to port 1.

| Emulator             | Autoconfig | Players |
| -------------------- | ---------- | ------- |
| lr-puae, lr-amiberry | Yes        | 2       |
| Amiberry             | Yes        | 2       |
| WinUAE               | Yes        | 2       |
| Amiga Forever        | No         |         |

Your PC keyboard works as the optional CDTV keyboard.

### Default layout

| CDTV             | libretro cores | Amiberry |
| ---------------- | -------------- | -------- |
| Joystick         | D-pad          | D-pad    |
| Fire button 1    | SOUTH          | SOUTH    |
| Fire button 2    | EAST           | EAST     |
| Space bar        | NORTH          |          |
| Mouse            | Analog sticks  | PC mouse |
| Mouse buttons    | L2 / R2        | PC mouse |
| Virtual keyboard | SELECT         | SELECT   |
| Emulator menu    |                | R3       |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (456).png" alt="" width="225"><figcaption></figcaption></figure></div>

### Useful control options

<table><thead><tr><th width="140.75">Emulator</th><th>Option</th><th>Description</th></tr></thead><tbody><tr><td>lr-puae</td><td>PAD BUTTON LAYOUT</td><td>Other button layouts (jump on a button…)</td></tr><tr><td>Amiberry</td><td>CONTROLLER TYPE</td><td>CDTV PAD emulates the joystick of the CDTV remote control</td></tr><tr><td>Amiberry</td><td>PORT 1 DEVICE</td><td>Mouse, joystick (player 2) or nothing in the mouse port</td></tr><tr><td>Amiberry</td><td>SWAP JOYSTICK PORTS</td><td>For the few titles that want the joystick in port 1</td></tr><tr><td>WinUAE</td><td>SWAP JOYSTICK PORTS / SECOND CONTROLLER</td><td>Swap the ports, put player 2 in port 1</td></tr></tbody></table>

For the other control options, see the Amiga 500 page.

### Hotkeys

**libretro cores**: standard RetroBat hotkeys.

| Hotkey         | Amiberry   | WinUAE | Amiga Forever |
| -------------- | ---------- | ------ | ------------- |
| HOTKEY + START | Quit       | Quit   |               |
| HOTKEY + WEST  | Save state |        |               |
| HOTKEY + NORTH | Load state |        |               |

The Amiberry menu opens with R3 or F12, the WinUAE menu with F12.

## Folders

<table><thead><tr><th width="164.5">Emulator</th><th>Content</th><th>Folder</th></tr></thead><tbody><tr><td>lr-puae</td><td>Saves (NVRAM, one file per title)</td><td><code>saves\amigacdtv</code></td></tr><tr><td>lr-amiberry</td><td>Saves</td><td><code>saves\amigacdtv\LR-amiberry</code></td></tr><tr><td>libretro</td><td>Save states</td><td><code>saves\amigacdtv\libretro.&#x3C;core></code></td></tr><tr><td>Amiberry</td><td>Save states, saves (NVRAM)</td><td><code>saves\amigacdtv\amiberry</code></td></tr><tr><td>Amiberry</td><td>Screenshots</td><td><code>screenshots\amiberry</code></td></tr><tr><td>WinUAE</td><td>Save states</td><td><code>saves\amigacdtv\winuae</code></td></tr><tr><td>WinUAE</td><td>Saves (NVRAM)</td><td><code>saves\amigacdtv\winuae\nvram</code></td></tr><tr><td>WinUAE</td><td>Screenshots / videos</td><td><code>screenshots\winuae</code> / <code>records\winuae</code></td></tr></tbody></table>

## Guides

### Saves

CDTV titles save to the internal memory of the unit (NVRAM). Each emulator keeps it in its own saves folder: switching emulators does not bring your saves with you. With lr-puae, each title gets its own save file.

### Multi-disc titles

Group the discs of a title with a .m3u file, for example `Title.m3u` in `roms\amigacdtv`:

```
Title (Disc 1).chd
Title (Disc 2).chd
```

With the libretro cores, change disc with HOTKEY + L1 (eject/insert) and HOTKEY + L2/R2 (previous/next disc). Amiberry only starts the first disc: change the disc from its menu.

## Known issues

<table><thead><tr><th width="321.5">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>"Kickstart not found" or black screen</td><td>Copy kick34005.A500 <strong>and</strong> kick34005.CDTV to the bios folder.</td></tr><tr><td>Amiga Forever ROMs do not work</td><td>Copy rom.key next to them.</td></tr><tr><td>No music</td><td>The .iso format has no CD audio: use a .cue/.bin or .chd image.</td></tr><tr><td>The title stays on the CDTV logo or does not load</td><td>With lr-puae, enable CD INSERT DELAY. Otherwise try another emulator.</td></tr><tr><td>The title only reacts to the mouse</td><td>Many CDTV titles are mouse-driven: use the analog sticks (libretro) or your PC mouse.</td></tr><tr><td>The joystick does not respond</td><td>The title wants the joystick in port 1: enable SWAP JOYSTICK PORTS (Amiberry, WinUAE).</td></tr><tr><td>A .zip/.7z title does not start</td><td>Only the libretro cores read archives: extract it, or convert it to .chd.</td></tr></tbody></table>
