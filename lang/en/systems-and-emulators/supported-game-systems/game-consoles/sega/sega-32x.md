---
description: Sega
---

# Sega 32X

| <p></p><p><img src="../../../../.gitbook/assets/image (474).png" alt="" data-size="original"></p> | <p></p><p><img src="../../../../.gitbook/assets/image (475).png" alt="" data-size="original"></p> |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |

## Overview

The **32X** is an add-on that plugs into the cartridge slot of the MegaDrive. Sega released it at the end of 1994 to extend the life of its console while waiting for the Saturn. It adds two Hitachi SH-2 processors (the same family as in the Saturn) and a new video chip: more colours and 3D graphics, displayed over the MegaDrive picture.

Released only months before the Saturn, the 32X got about 40 games, among them _Virtua Racing Deluxe_, _Star Wars Arcade_, _Doom_, _Knuckles' Chaotix_, _Virtua Fighter_, _Kolibri_, _Space Harrier_ and _After Burner Complete_.

The handful of games that need both the Mega-CD and the 32X (Mega-CD 32X), such as the 32X versions of _Night Trap_ or _Corpse Killer_, are CD games: put them in the Mega-CD system and play them with **libretro: picodrive** or **ares: MegaCD32X**(see the [Mega-CD page](mega-cd-sega-cd.md)).

{% embed url="https://en.wikipedia.org/wiki/32X" %}

## At a glance

<table><thead><tr><th width="236.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\sega32x</code></td></tr><tr><td><strong>Extensions</strong></td><td>.32x .smd .bin .md .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: picodrive</td></tr><tr><td><strong>BIOS</strong></td><td>None required</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BlastEm, Jgenesis, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator to choose?

| Emulator                          | Strengths                                               | Limits                                 |
| --------------------------------- | ------------------------------------------------------- | -------------------------------------- |
| **libretro: picodrive** (default) | Fast and compatible, no BIOS needed, RetroAchievements  |                                        |
| jgenesis                          | Recent and accurate, no BIOS needed                     | Needs a more powerful PC               |
| blastem                           | Very accurate, multitap                                 | 32X BIOS required, needs a powerful PC |
| ares                              | Accurate multi-system emulator, no BIOS needed          | Needs a more powerful PC               |
| kega-fusion                       | Historical emulator, light, multitap                    | No longer maintained                   |
| bizhawk: PicoDrive                | PicoDrive with BizHawk's tools (TAS, RetroAchievements) |                                        |

## BIOS

Most emulators do not need any BIOS for the 32X. **BlastEm** needs the three 32X BIOS files, and Kega Fusion uses them if they are present. Copy them to the `bios` folder:

<table><thead><tr><th width="185.75">File</th><th width="232.25">Processor</th><th>MD5</th></tr></thead><tbody><tr><td>32X_G_BIOS.BIN</td><td>68000 (Mega Drive side)</td><td>6a5433f6a132a2b683635819a6dcf085</td></tr><tr><td>32X_M_BIOS.BIN</td><td>SH-2 master</td><td>f88354ec482be09aeccd76a97bb75868</td></tr><tr><td>32X_S_BIOS.BIN</td><td>SH-2 slave</td><td>7f041b6a55cd7423a6c08a219335269e</td></tr></tbody></table>

{% hint style="info" %}
RetroBat lists these files as OPTIONAL: they are only needed with BlastEm.
{% endhint %}

### Game region

The region decides which version of a game runs and whether it runs at 50 or 60 Hz. Every emulator detects it automatically. To force it, use REGION (lr-picodrive), FORCE REGION (BlastEm, Jgenesis), PREFERRED REGION (Ares) or CONSOLE REGION (Kega Fusion, BizHawk).

## Game formats

<table><thead><tr><th width="235.25">Format</th><th>Description</th></tr></thead><tbody><tr><td>.32x</td><td>32X cartridge dump (the usual format)</td></tr><tr><td>.bin / .md / .smd</td><td>Other cartridge formats</td></tr><tr><td>.zip / .7z</td><td>Compressed games</td></tr></tbody></table>

## Controls

The 32X uses the MegaDrive controller: autoconfiguration, layouts, 3-button pad, Mega Drive-style controllers and multitaps work as for the MegaDrive. See the [Megadrive - Genesis page](megadrive-genesis.md#controls) for the details.

<table><thead><tr><th width="189.75">Emulator</th><th width="165.75">Autoconfig</th><th>Players</th></tr></thead><tbody><tr><td>lr-picodrive</td><td>Yes</td><td>2</td></tr><tr><td>Jgenesis</td><td>Yes</td><td>2</td></tr><tr><td>BlastEm</td><td>Yes</td><td>2, up to 8 (USE MULTITAP)</td></tr><tr><td>Ares</td><td>Yes</td><td>2</td></tr><tr><td>Kega Fusion</td><td>Yes</td><td>2, up to 8 (USE MULTITAP)</td></tr><tr><td>BizHawk</td><td>Yes</td><td>2</td></tr></tbody></table>

### Default layout (6-button pad)

| Mega Drive | Controller |   | Mega Drive | Controller |
| ---------- | ---------- | - | ---------- | ---------- |
| A          | WEST       |   | X          | L1         |
| B          | SOUTH      |   | Y          | NORTH      |
| C          | EAST       |   | Z          | R1         |
| START      | START      |   | MODE       | SELECT     |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (459).png" alt="" width="225"><figcaption></figcaption></figure></div>

The **BUTTON LAYOUT** option (CONTROLS submenu) is available with every emulator. **USE 3 BUTTON CONTROLLER** exists with lr-picodrive, Jgenesis and BlastEm, and **USE GENESIS-LIKE CONTROLLER** with every emulator. For the 8BitDo M30, see the [Special controllers page](../../../../controllers/supported-controllers/gamepads/special-controllers.md).

### Hotkeys

**libretro core**: [standard RetroBat hotkeys](../../../../navigation/hotkeys.md).

| Hotkey         | BlastEm    | Jgenesis   | Ares       | BizHawk    | Kega Fusion |
| -------------- | ---------- | ---------- | ---------- | ---------- | ----------- |
| HOTKEY + START | Quit       | Quit       | Quit       | Quit       | Quit        |
| HOTKEY + WEST  | Save state | Save state | Save state | Save state |             |
| HOTKEY + NORTH | Load state | Load state | Load state | Load state |             |

## Folders

<table><thead><tr><th width="149.5">Emulator</th><th width="199">Content</th><th>Folder</th></tr></thead><tbody><tr><td>lr-picodrive</td><td>Saves</td><td><code>saves\sega32x</code></td></tr><tr><td>lr-picodrive</td><td>Save states</td><td><code>saves\sega32x\libretro.picodrive</code></td></tr><tr><td>BlastEm</td><td>Saves and save states</td><td><code>saves\sega32x\blastem\&#x3C;game></code></td></tr><tr><td>Jgenesis</td><td>Saves</td><td><code>saves\sega32x\jgenesis</code></td></tr><tr><td>Ares</td><td>Saves</td><td><code>saves\sega32x\ares</code></td></tr><tr><td>Kega Fusion</td><td>Saves / save states</td><td><code>saves\sega32x</code> / <code>saves\sega32x\kega-fusion\sstates</code></td></tr><tr><td>BizHawk</td><td>Saves</td><td><code>saves\sega32x\bizhawk</code></td></tr><tr><td>Screenshots</td><td></td><td><code>screenshots</code> (subfolder per emulator)</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="307.75">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>Black screen with BlastEm</td><td>Copy the three 32X BIOS files to the bios folder, or use lr-picodrive.</td></tr><tr><td>The game is slow or stutters</td><td>32X emulation is demanding with BlastEm, Jgenesis and Ares: use lr-picodrive.</td></tr><tr><td>A Mega-CD 32X game does not start</td><td>Put it in the Mega-CD system and use libretro: picodrive or ares: MegaCD32X.</td></tr><tr><td>The buttons are not where I expect</td><td>Change BUTTON LAYOUT. See the Megadrive - Genesis page.</td></tr></tbody></table>
