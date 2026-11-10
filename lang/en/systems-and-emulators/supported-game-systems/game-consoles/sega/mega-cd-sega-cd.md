---
description: Sega
---

# Mega-CD - Sega-CD

| <p></p><p><img src="../../../../.gitbook/assets/image (472).png" alt="" data-size="original"></p> | <p></p><p><img src="../../../../.gitbook/assets/image (473).png" alt="" data-size="original"></p> |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |

## Overview

The **Mega-CD** (called **Sega CD** in North America) is a CD-ROM drive that plugs into the MegaDrive. It was released in Japan in December 1991, in North America in 1992 and in Europe in 1993. It adds a second, faster 68000 processor, a chip able to scale and rotate images, extra memory and CD-quality sound. Its CDs held far more data than a cartridge: full-motion video, voices and CD soundtracks.

About 200 games came out on Mega-CD: _Sonic CD_, _Snatcher_, _Lunar: The Silver Star_, _Popful Mail_, _Silpheed_, _Robo Aleste_, _Final Fight CD_, _Shining Force CD_, as well as video games such as _Night Trap_ and _Sewer Shark_.

The Mega-CD plays the MegaDrive cartridges too, but put those in the MegaDrive system: see the [Megadrive - Genesis page](megadrive-genesis.md).

{% embed url="https://en.wikipedia.org/wiki/Sega_CD" %}

## At a glance

<table><thead><tr><th width="262.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\megacd</code></td></tr><tr><td><strong>Extensions</strong></td><td>.chd .cue .iso .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: genesis_plus_gx</td></tr><tr><td><strong>BIOS</strong></td><td><code>bios_CD_U.bin</code>, <code>bios_CD_E.bin</code> or <code>bios_CD_J.bin</code> (at least one)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BlastEm, Jgenesis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (genesis_plus_gx)</td></tr></tbody></table>

## Which emulator to choose?

<table><thead><tr><th width="229.5">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: genesis_plus_gx</strong> (default)</td><td>Accurate and complete: all formats, disc swap, lightguns, multitaps</td><td></td></tr><tr><td>libretro: genesis_plus_gx_wide</td><td>Same, with a widescreen (16:9) display</td><td>Graphic glitches on the sides in some games</td></tr><tr><td>libretro: picodrive</td><td>Very fast, for modest PCs. The only one that plays the Mega-CD 32X games</td><td>Less accurate, no RAM cartridge</td></tr><tr><td>jgenesis</td><td>Recent and accurate, RAM cartridge, can load the disc into memory</td><td>.chd and .cue only, first disc only for .m3u</td></tr><tr><td>blastem</td><td>Very accurate</td><td>.cue and .iso, no .m3u</td></tr><tr><td>ares</td><td>Accurate multi-system emulator, also plays the Mega-CD 32X games (MegaCD32X core)</td><td>First disc only for .m3u</td></tr><tr><td>kega-fusion</td><td>Historical emulator, light</td><td>.cue and .iso only, no longer maintained</td></tr></tbody></table>

## BIOS

The Mega-CD needs its BIOS, which differs by region. Copy them to the `bios` folder:

<table><thead><tr><th width="153.25">File</th><th width="225.75">Console</th><th>MD5</th></tr></thead><tbody><tr><td>bios_CD_E.bin</td><td>Mega-CD (Europe)</td><td>e66fa1dc5820d254611fdcdba0662372</td></tr><tr><td>bios_CD_U.bin</td><td>Sega CD (North America)</td><td>854b9150240a198070150e4566ae1290</td></tr><tr><td>bios_CD_J.bin</td><td>Mega-CD (Japan)</td><td>278a9397d192149e84e820ac621a8edd</td></tr></tbody></table>

{% hint style="info" %}
Each game starts with the BIOS of its own region: a European game needs bios\_CD\_E.bin, an American game bios\_CD\_U.bin, a Japanese game bios\_CD\_J.bin. Copy the three files if you have games from several regions. RetroBat checks that at least one of them is present and lists the others as OPTIONAL.
{% endhint %}

All emulators use the same file names.

### Game region

The region of the game decides which BIOS is used and whether the game runs at 50 or 60 Hz. Every emulator detects it automatically. To force it, use CONSOLE REGION (lr-genesis\_plus\_gx, Kega Fusion), REGION (lr-picodrive), FORCE REGION (BlastEm, Jgenesis) or PREFERRED REGION (Ares): the BIOS of the forced region is then needed.

## Game formats

<table><thead><tr><th width="155.25">Format</th><th>Description</th></tr></thead><tbody><tr><td>.chd</td><td>Compressed CD image, one file per game, keeps the CD audio tracks. <strong>Recommended</strong> (libretro cores, Jgenesis, Ares)</td></tr><tr><td>.cue (+ .bin)</td><td>CD image with its audio tracks, read by every emulator</td></tr><tr><td>.iso</td><td>Data-only CD image: the CD music is missing. Not read by Jgenesis</td></tr><tr><td>.m3u</td><td>Multi-disc game</td></tr><tr><td>.zip / .7z</td><td>Compressed CD image, libretro cores and Jgenesis only. Prefer .chd</td></tr></tbody></table>

{% hint style="success" %}
Mega-CD games rely heavily on CD music: avoid .iso and prefer **.chd**. To convert a .cue/.bin game: `chdman createcd -i "game.cue" -o "game.chd"`.
{% endhint %}

### Multi-disc games

Some games come on several CDs (_Night Trap_…). Create a .m3u file in `roms\megacd`, for example `Night Trap.m3u`:

```
Night Trap (Disc 1).chd
Night Trap (Disc 2).chd
```

* **libretro cores**: change disc with HOTKEY + L1 (eject/insert) and HOTKEY + L2/R2 (previous/next disc).
* **Jgenesis, Ares**: only the first disc starts.
* **BlastEm, Kega Fusion**: no .m3u support, start each disc on its own.

## Controls

The Mega-CD uses the MegaDrive controller: autoconfiguration, layouts, 3-button pad, MegaDrive-style controllers and multitaps work as for the MegaDrive. See the [Megadrive - Genesis page](megadrive-genesis.md) for the details.

<table><thead><tr><th width="218.75">Emulator</th><th width="147">Autoconfig</th><th>Players</th></tr></thead><tbody><tr><td>lr-genesis_plus_gx, lr-genesis_plus_gx_wide</td><td>Yes</td><td>2, up to 8 with a multitap (CONTROLLER TYPE)</td></tr><tr><td>lr-picodrive</td><td>Yes</td><td>2</td></tr><tr><td>Jgenesis</td><td>Yes</td><td>2</td></tr><tr><td>BlastEm</td><td>Yes</td><td>2, up to 8 (USE MULTITAP)</td></tr><tr><td>Ares</td><td>Yes</td><td>2</td></tr><tr><td>Kega Fusion</td><td>Yes</td><td>2, up to 8 (USE MULTITAP)</td></tr></tbody></table>

### Default layout (6-button pad)

<table><thead><tr><th width="123.5">Mega Drive</th><th width="112.25">Controller</th><th width="177.25"></th><th width="139">Mega Drive</th><th>Controller</th></tr></thead><tbody><tr><td>A</td><td>WEST</td><td></td><td>X</td><td>L1</td></tr><tr><td>B</td><td>SOUTH</td><td></td><td>Y</td><td>NORTH</td></tr><tr><td>C</td><td>EAST</td><td></td><td>Z</td><td>R1</td></tr><tr><td>START</td><td>START</td><td></td><td>MODE</td><td>SELECT</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (459).png" alt="" width="225"><figcaption></figcaption></figure></div>

The **BUTTON LAYOUT**, **USE 3 BUTTON CONTROLLER** (CONTROLLER TYPE with lr-genesis\_plus\_gx) and **USE GENESIS-LIKE CONTROLLER** options (CONTROLS submenu) work as for the [Mega Drive](megadrive-genesis.md#controls). For the 8BitDo M30, see the [Special controllers page](../../../../controllers/supported-controllers/gamepads/special-controllers.md#mega-drive-genesis-and-mega-cd-32x).

### Lightguns

Several Mega-CD games use a lightgun, such as _Lethal Enforcers_ or _Snatcher_ (Justifier). With the Genesis Plus GX cores, enable the guns (GUNS submenu) and choose the GUN TYPE: **Justifier** or **Menacer**. See the [Lightguns page](../../../../controllers/supported-controllers/lightguns/).

### Hotkeys

**libretro cores**: [standard RetroBat hotkeys](../../../../navigation/hotkeys.md).

| Hotkey         | BlastEm    | Jgenesis   | Ares       | Kega Fusion |
| -------------- | ---------- | ---------- | ---------- | ----------- |
| HOTKEY + START | Quit       | Quit       | Quit       | Quit        |
| HOTKEY + WEST  | Save state | Save state | Save state |             |
| HOTKEY + NORTH | Load state | Load state | Load state |             |

## Folders

<table><thead><tr><th width="132">Emulator</th><th>Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro</td><td>Game saves (internal memory, RAM cartridge)</td><td><code>saves\megacd</code></td></tr><tr><td>libretro</td><td>Save states</td><td><code>saves\megacd\libretro.&#x3C;core></code></td></tr><tr><td>BlastEm</td><td>Game saves and save states</td><td><code>saves\megacd\blastem\&#x3C;game></code></td></tr><tr><td>Jgenesis</td><td>Game saves</td><td><code>saves\megacd\jgenesis</code></td></tr><tr><td>Ares</td><td>Game saves</td><td><code>saves\megacd\ares</code></td></tr><tr><td>Kega Fusion</td><td>Game saves / save states</td><td><code>saves\megacd</code> / <code>saves\megacd\kega-fusion\sstates</code></td></tr><tr><td>Screenshots</td><td></td><td><code>screenshots</code> (subfolder per emulator)</td></tr></tbody></table>

## Guides

### Mega-CD 32X games

A few games need both the Mega-CD and the 32X, such as the 32X versions of _Night Trap_, _Corpse Killer_, _Slam City_ or _Fahrenheit_. Put them in `roms\megacd` and set the emulator of these games to **libretro: picodrive** or **ares: MegaCD32X** (game options): the other emulators do not emulate the 32X on top of the Mega-CD. The Mega-CD BIOS is required, the 32X BIOS is not.

### Game saves and the RAM cartridge

Mega-CD games save to the internal memory of the console, which is small and shared by all games. An optional **RAM cartridge** added more space. With Jgenesis, the **RAM CART** option (EMULATION submenu, enabled by default) emulates it. If a game says the memory is full, delete old saves from the BIOS memory manager: start the emulator without a game, or press START on the BIOS screen.

### Loading the disc into memory

With Jgenesis, **LOAD GAME TO RAM** copies the whole disc into memory at startup: the game starts a bit later but reads are faster afterwards.

## Known issues

<table><thead><tr><th width="336.5">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>Black screen or "BIOS not found"</td><td>Copy the BIOS of the game's region (bios_CD_E/U/J.bin) to the bios folder.</td></tr><tr><td>No music in the game</td><td>The .iso format has no CD audio: use a .cue/.bin or .chd image.</td></tr><tr><td>A .chd game does not start with Kega Fusion or BlastEm</td><td>Use lr-genesis_plus_gx, Jgenesis or Ares, or a .cue/.bin image.</td></tr><tr><td>A .iso game does not start with Jgenesis</td><td>Jgenesis only reads .chd and .cue: convert the game to .chd.</td></tr><tr><td>The second disc does not start</td><td>Use a .m3u file with a libretro core and swap discs with HOTKEY + L1 / L2 / R2.</td></tr><tr><td>The game says the memory is full</td><td>Delete old saves in the BIOS memory manager, or enable RAM CART with Jgenesis.</td></tr><tr><td>The buttons are not where I expect</td><td>Change BUTTON LAYOUT. See the Megadrive - Genesis page.</td></tr><tr><td>A Mega-CD 32X game shows a black screen</td><td>Use libretro: picodrive or ares: MegaCD32X for this game.</td></tr></tbody></table>
