---
description: Sega
---

# Saturn

<div align="left"><figure><img src="../../../../.gitbook/assets/image (427).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Sega Saturn** is a 32-bit home console released by Sega in November 1994 in Japan, then in 1995 in North America (a surprise launch announced at the first E3) and Europe. It succeeded the Mega Drive and the Mega-CD and competed directly with the Sony PlayStation and later the Nintendo 64.

Inside, the Saturn is famously complex: two Hitachi SH-2 processors working in parallel, two video chips (VDP1 draws sprites and polygons, VDP2 handles the scrolling backgrounds), a Yamaha sound processor driven by a Motorola 68000, and a dedicated processor for the CD drive. This architecture made it a 2D powerhouse but hard to program in 3D, and it remains one of the most difficult consoles to emulate.

The Saturn had a cartridge slot, used for save memory cards and for RAM expansion cartridges (1 MB and 4 MB) required by some Japanese arcade conversions such as _X-Men vs. Street Fighter_ or _Metal Slug_.

The console sold around 9 million units and was discontinued in 1998 in the West and in 2000 in Japan. Its library is rich in classics: _Panzer Dragoon Saga_, _NiGHTS into Dreams_, _Virtua Fighter 2_, _Guardian Heroes_, _Radiant Silvergun_, _Burning Rangers_, _Sega Rally Championship_, _Saturn Bomberman_ and many fighting and shoot'em up games, a large part of them released only in Japan.

{% embed url="https://en.wikipedia.org/wiki/Sega_Saturn" %}

## At a glance

<table><thead><tr><th width="226.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\saturn</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .cue .toc .m3u .ccd .chd .iso .cso .mds .squashfs .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: kronos</td></tr><tr><td><strong>BIOS</strong></td><td><code>sega_101.bin</code>, <code>mpr-17933.bin</code> or <code>saturn_bios.bin</code> (at least one)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (except yabasanshiro), BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro core (mednafen_saturn)</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (kronos, mednafen_saturn, ymir), Mednafen, Kronos, BizHawk</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>mpr-18811-mx.ic1</code> (KOF 95), <code>mpr-19367-mx.ic1</code> (Ultraman), <code>mpeg_card.bin</code> (Video CD)</td></tr></tbody></table>

## Which emulator to choose?

RetroBat offers 10 emulators for the Saturn. If you are not sure, keep the default emulator (**lr-kronos**): it runs most games well, supports higher resolutions, RetroAchievements and netplay.

| Emulator                       | Strengths                                                                                                               | Limits                                                                        |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| **libretro: kronos** (default) | Good compatibility, internal resolution up to 8x, RetroAchievements, netplay                                            | Some graphical glitches in rare games                                         |
| libretro: mednafen\_saturn     | Most accurate emulation (Beetle Saturn), RetroAchievements, netplay, many controller types (3D pad, Arcade Racer, guns) | Needs a powerful CPU, original resolution only, BIOS matching the game region |
| libretro: ymir                 | Recent, accurate and fast emulator, RetroAchievements                                                                   | Original resolution only                                                      |
| libretro: yabasanshiro         | Light, high resolution                                                                                                  | Lower compatibility                                                           |
| ymir                           | Standalone version of Ymir: very good compatibility, rewind, memory manager (F1)                                        | 2 players maximum                                                             |
| mednafen                       | Same engine as Beetle Saturn, up to 12 players                                                                          | No .chd support                                                               |
| kronos                         | Standalone version of Kronos, high resolution, guns                                                                     |                                                                               |
| yabasanshiro                   | Standalone version of YabaSanshiro, Vulkan renderer                                                                     | Lower compatibility                                                           |
| bizhawk: saturnus              | Mednafen-based, tool-assisted features (TAS)                                                                            | No .chd support                                                               |
| ssf                            | Japanese emulator with very good compatibility, works without BIOS                                                      | Interface partly in Japanese                                                  |

## BIOS

### BIOS files

Copy the BIOS files to the `bios` folder of RetroBat.

| BIOS file        | MD5                              | Used by                                                                          |
| ---------------- | -------------------------------- | -------------------------------------------------------------------------------- |
| sega\_101.bin    | 85ec9ca47d8f6807718151cbcca8b964 | Japanese BIOS – Mednafen, BizHawk (Japanese games), lr-kronos, lr-ymir, Ymir     |
| mpr-17933.bin    | 3240872c70984b6cbfda1586cab68dbe | US/EU BIOS – Mednafen, BizHawk (US and European games), lr-kronos, lr-ymir, Ymir |
| saturn\_bios.bin | af5828fdff51384f99b3c4926be27762 | lr-kronos, lr-yabasanshiro, lr-ymir, Kronos, YabaSanshiro, Ymir                  |
| mpr-18811-mx.ic1 | 255113ba943c92a54facd25a10fd780c | _The King of Fighters '95_ ROM cartridge (optional)                              |
| mpr-19367-mx.ic1 | 1cd19988d1d72a3e7caa0b73234c96b4 | _Ultraman: Hikari no Kyojin Densetsu_ ROM cartridge (optional)                   |
| mpeg\_card.bin   |                                  | Video CD Card for lr-mednafen\_saturn (optional)                                 |

{% hint style="info" %}
RetroBat checks that at least one of the three BIOS **sega\_101.bin**, **mpr-17933.bin** or **saturn\_bios.bin** is present. The other files are listed as OPTIONAL.
{% endhint %}

### Which BIOS do I need?

* **To keep it simple**: put **sega\_101.bin** and **mpr-17933.bin** in the bios folder. All emulators will work, whatever the region of your games.
* **lr-kronos** (default) and **lr-ymir** accept any of the three BIOS. **Ymir** automatically picks the BIOS matching the game region among the files present in the bios folder.
* **lr-mednafen\_saturn, Mednafen and BizHawk** use the BIOS of the game region: sega\_101.bin for Japanese games, mpr-17933.bin for US and European games.
* **lr-yabasanshiro, Kronos and YabaSanshiro** use saturn\_bios.bin. Kronos and YabaSanshiro fall back to sega\_101.bin or mpr-17933.bin if it is missing.
* **SSF** uses its built-in BIOS (HLE) by default and needs no file.
* The Ymir, Kronos, YabaSanshiro and SSF standalone emulators have a **FORCE BIOS** option (EMULATION submenu) to choose the file to use. Kronos, YabaSanshiro and SSF also offer an **HLE** choice (built-in BIOS, less compatible).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (428).png" alt=""><figcaption></figcaption></figure></div>

### Changing the console language

Many Saturn games use the language set in the console, mostly European games which offer several languages.

| Emulator                                        | Option (EMULATION submenu)                           |
| ----------------------------------------------- | ---------------------------------------------------- |
| lr-kronos, lr-mednafen\_saturn, lr-yabasanshiro | LANGUAGE                                             |
| Kronos                                          | CONSOLE LANGUAGE (default: the language of RetroBat) |
| Mednafen                                        | CONSOLE LANGUAGE                                     |
| BizHawk                                         | BIOS LANGUAGE                                        |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (430).png" alt=""><figcaption></figcaption></figure></div>

For **Ymir** and **YabaSanshiro**, there is no option: enable **START BIOS** (EMULATION submenu), launch any game, then choose the language in the console settings. The setting is kept in the internal memory of the emulator. Disable START BIOS afterwards.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (429).png" alt=""><figcaption></figcaption></figure></div>

## Game formats

### Recommended formats

* **.chd** is recommended: a single compressed file per disc. It works with all emulators except **Mednafen** and **BizHawk** (use .cue with them). If a .chd game does not start with SSF, use the .cue version.
* **.cue/.bin**, **.ccd/.img/.sub**, **.mds/.mdf** and **.iso** are also supported.
* **.zip / .7z / .squashfs** archives are extracted at each launch, which is slower. Prefer .chd.

### Multi-disc games

Use a .m3u file to group the discs of a game. Example for _Panzer Dragoon Saga_: create `Panzer Dragoon Saga.m3u` in the `roms\saturn` folder with this content:

```
Panzer Dragoon Saga (Disc 1).chd
Panzer Dragoon Saga (Disc 2).chd
Panzer Dragoon Saga (Disc 3).chd
Panzer Dragoon Saga (Disc 4).chd
```

RetroBat automatically hides the discs referenced in the .m3u from the game list.

Changing disc:

* **libretro cores**: use the disc hotkeys (HOTKEY + L1 to eject/insert, HOTKEY + L2/R2 to select the previous/next disc).
* **Mednafen**: HOTKEY + R2 selects the next disc, HOTKEY + L1 ejects/inserts it.
* **Ymir, Kronos, YabaSanshiro**: choose the disc to start with the **DISC NUMBER** option (EMULATION submenu), **SSF**: **DISC INDEX** option.

## Controls

### Controller autoconfiguration

RetroBat configures your controllers automatically for all Saturn emulators.

<table><thead><tr><th>Emulator</th><th width="165.75">Autoconfig</th><th>Players</th></tr></thead><tbody><tr><td>libretro cores</td><td>Yes</td><td>Up to 8 (multitap)</td></tr><tr><td>Ymir</td><td>Yes</td><td>2</td></tr><tr><td>Mednafen</td><td>Yes</td><td>Up to 12 (multitap)</td></tr><tr><td>Kronos, YabaSanshiro</td><td>Yes</td><td>Up to 12 (USE MULTITAP option)</td></tr><tr><td>BizHawk</td><td>Yes</td><td>Up to 12</td></tr><tr><td>SSF</td><td>Yes</td><td>Up to 12</td></tr></tbody></table>

To play with more than 2 players, enable the multitap: **USE MULTITAP** (Kronos, YabaSanshiro, Mednafen, lr-kronos, lr-yabasanshiro) or **MULTITAP PORT 1 / PORT 2** (lr-mednafen\_saturn).

### Default layout

The Saturn controller has 6 face buttons (A B C / X Y Z) and two shoulder buttons (L R). By default, RetroBat maps them as follows:

<table><thead><tr><th width="297.75">Saturn controller</th><th>Your controller</th></tr></thead><tbody><tr><td>A</td><td>SOUTH</td></tr><tr><td>B</td><td>EAST</td></tr><tr><td>C</td><td>R1</td></tr><tr><td>X</td><td>WEST</td></tr><tr><td>Y</td><td>NORTH</td></tr><tr><td>Z</td><td>L1</td></tr><tr><td>L</td><td>L2</td></tr><tr><td>R</td><td>R2</td></tr><tr><td>START</td><td>START</td></tr><tr><td>D-pad</td><td>D-pad</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (431).png" alt="" width="225"><figcaption></figcaption></figure></div>

### Alternative layouts

The **BUTTON LAYOUT** option (CONTROLS submenu) moves the 6 face buttons, which is useful for fighting games:

<table><thead><tr><th>Option</th><th width="91.75">A</th><th width="89.25">B</th><th width="76.75">C</th><th width="85.5">X</th><th width="101.75">Y</th><th>Z</th></tr></thead><tbody><tr><td>L/R as Z/C (default)</td><td>SOUTH</td><td>EAST</td><td>R1</td><td>WEST</td><td>NORTH</td><td>L1</td></tr><tr><td>L/R as Y/Z</td><td>WEST</td><td>SOUTH</td><td>EAST</td><td>NORTH</td><td>L1</td><td>R1</td></tr><tr><td>L/R as X/Z</td><td>WEST</td><td>SOUTH</td><td>EAST</td><td>L1</td><td>NORTH</td><td>R1</td></tr></tbody></table>

The **INVERT TRIGGERS AND SHOULDERS** option uses L1/R1 for the Saturn L and R buttons instead of L2/R2.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (432).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (433).png" alt="" width="225"><figcaption></figcaption></figure></div>

| Option                | Control layout                                                                      |
| --------------------- | ----------------------------------------------------------------------------------- |
| L/R AS Y/Z            | <img src="../../../../.gitbook/assets/image (434).png" alt="" data-size="original"> |
| L/R AS Y/Z (inverted) | <img src="../../../../.gitbook/assets/image (435).png" alt="" data-size="original"> |
| L/R AS X/Z            | <img src="../../../../.gitbook/assets/image (436).png" alt="" data-size="original"> |
| L/R AS X/Z (inverted) | <img src="../../../../.gitbook/assets/image (437).png" alt="" data-size="original"> |

### Using a Saturn-like controller

RetroBat knows the **8BitDo M30** (XInput, Switch, DInput and 2.4G modes) and maps it like an original Saturn controller. In XInput, Switch and DInput modes, enable **USE SATURN-LIKE CONTROLLER** (CONTROLS submenu). The 2.4G version is mapped automatically.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (438).png" alt=""><figcaption></figcaption></figure></div>

The mapping is stored in `system\resources\inputmapping\saturnControllers.json`: you can add other controllers to this file.

### 3D Pad, Arcade Racer and mouse

The **CONTROLLER TYPE** option (CONTROLS submenu) emulates other Saturn controllers:

<table><thead><tr><th width="219">Emulator</th><th>Available types</th></tr></thead><tbody><tr><td>lr-mednafen_saturn</td><td>Joypad, 3D Pad, Arcade Racer, Mission Stick, mouse, Stunner, Twin-Stick, Virtua Gun, keyboard</td></tr><tr><td>lr-ymir</td><td>Saturn Pad, mouse, Virtua Gun, 3D Pad, Arcade Racer, Mission Stick</td></tr><tr><td>lr-kronos</td><td>Joypad, 3D Pad, wheel, mouse</td></tr><tr><td>lr-yabasanshiro</td><td>Saturn Pad, 3D Pad</td></tr><tr><td>Ymir</td><td>Standard controller, 3D Pad, Shuttle Mouse, Virtua Gun (mouse)</td></tr></tbody></table>

The 3D Pad is recommended for _NiGHTS into Dreams_ and the analog games. Steering wheels are not configured automatically: select **Arcade Racer** and use the analog stick, or map your wheel in the RetroArch menu.

### Light guns

<table><thead><tr><th width="189">Emulator</th><th>How to enable</th></tr></thead><tbody><tr><td>lr-mednafen_saturn</td><td>ENABLE GUNS (GUNS submenu): Virtua Gun, crosshair option, Sinden supported</td></tr><tr><td>lr-ymir</td><td>ENABLE GUNS + GUN TYPE (Stunner/Virtua Gun or mouse)</td></tr><tr><td>lr-kronos</td><td>ENABLE GUNS (the gun is emulated as a mouse)</td></tr><tr><td>Kronos</td><td>ENABLE GUNS + GUN PORT (port 2 by default)</td></tr><tr><td>Mednafen</td><td>ENABLE GUN</td></tr><tr><td>BizHawk</td><td>ENABLE GUNS</td></tr><tr><td>Ymir</td><td>CONTROLLER TYPE = VIRTUA GUN (MOUSE)</td></tr></tbody></table>

### Hotkeys

**libretro cores**: standard RetroBat hotkeys (menu, save states, rewind, fast forward, screenshot, disc change…).

**Standalone emulators**:

<table><thead><tr><th width="114.25">Hotkey</th><th width="114.25">Ymir</th><th width="111.75">Mednafen</th><th width="111.75">BizHawk</th><th width="113">Kronos</th><th width="115.5">YabaSanshiro</th><th>SSF</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td><td>Quit</td><td>Quit</td><td>Quit</td><td>Quit</td><td>Quit</td></tr><tr><td>HOTKEY + SOUTH</td><td>Ymir settings</td><td>Pause</td><td>Pause</td><td></td><td></td><td></td></tr><tr><td>HOTKEY + WEST</td><td>Save state</td><td>Save state</td><td>Save state</td><td></td><td>Save state (slot 1)</td><td></td></tr><tr><td>HOTKEY + NORTH</td><td>Load state</td><td>Load state</td><td>Load state</td><td></td><td>Load state (slot 1)</td><td></td></tr><tr><td>HOTKEY + UP / DOWN</td><td></td><td>Change slot</td><td>Change slot</td><td></td><td></td><td></td></tr><tr><td>HOTKEY + LEFT</td><td>Rewind (REWIND BUFFER)</td><td>Rewind</td><td>Rewind</td><td></td><td></td><td></td></tr><tr><td>HOTKEY + RIGHT</td><td>Fast forward</td><td>Fast forward</td><td>Fast forward</td><td></td><td></td><td></td></tr><tr><td>HOTKEY + R3</td><td>Screenshot</td><td>Screenshot</td><td>Screenshot</td><td>Screenshot</td><td>Screenshot</td><td></td></tr><tr><td>HOTKEY + L3</td><td>Fullscreen</td><td>Fullscreen</td><td>Fullscreen</td><td>Fullscreen</td><td>Fullscreen</td><td></td></tr><tr><td>HOTKEY + L1</td><td></td><td>Eject disc</td><td></td><td></td><td></td><td></td></tr><tr><td>HOTKEY + R2</td><td></td><td>Next disc</td><td></td><td></td><td></td><td></td></tr></tbody></table>

{% hint style="info" %}
With Ymir, the rewind only works if **REWIND BUFFER** is enabled (EMULATION submenu).
{% endhint %}

## Folders

### Saves (backup memory)

Each emulator uses its own save files: a save made with one emulator is not available in another one, except between lr-kronos and lr-mednafen\_saturn (option **SHARE SAVE WITH MEDNAFEN** of lr-kronos, enabled by default).

| Emulator       | Save folder                                                                                                                                     |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| libretro cores | `saves\saturn`                                                                                                                                  |
| Ymir           | `saves\saturn\ymir\state` (one file per game with PER GAME BACKUP RAM, enabled by default), `saves\saturn\ymir\backup` (memory manager exports) |
| Mednafen       | `saves\saturn`                                                                                                                                  |
| Kronos         | `saves\saturn\kronos\bkram.bin`                                                                                                                 |
| YabaSanshiro   | `saves\saturn\yabasanshiro\bkram.bin`                                                                                                           |
| BizHawk        | `saves\saturn\bizhawk`                                                                                                                          |
| SSF            | emulator folder (`emulators\ssf`)                                                                                                               |

### Save states and screenshots

<table><thead><tr><th width="160.75">Emulator</th><th>Save states</th><th>Screenshots</th></tr></thead><tbody><tr><td>libretro cores</td><td><code>saves\saturn\libretro.&#x3C;core></code></td><td><code>screenshots</code></td></tr><tr><td>Ymir</td><td><code>saves\saturn\ymir\savestates</code></td><td><code>screenshots\ymir</code></td></tr><tr><td>Mednafen</td><td><code>saves\saturn\mednafen\sstates</code></td><td><code>screenshots\mednafen</code></td></tr><tr><td>Kronos</td><td><code>saves\saturn\kronos\sstates</code></td><td><code>screenshots\kronos</code></td></tr><tr><td>YabaSanshiro</td><td><code>saves\saturn\yabasanshiro\sstates</code></td><td></td></tr><tr><td>BizHawk</td><td><code>saves\saturn\bizhawk\sstates</code></td><td><code>screenshots\bizhawk\saturn</code></td></tr></tbody></table>

### Other useful folders

* `bios\cdb`: CD block ROM for the **LOW LEVEL CD BLOCK** option of Ymir (and lr-ymir).
* `emulators\ssf\Setting`: personal SSF setting files (option **USE OWN GAME SETTING FILE**).

## Guides

### Improving graphics

* **Higher resolution**: **INTERNAL RESOLUTION** option with lr-kronos (up to 8x), Kronos, YabaSanshiro and lr-yabasanshiro. Beetle Saturn and Ymir only render in original resolution.
* **IMPROVED MESH**: replaces the mesh transparency of the Saturn with real transparency (lr-kronos, lr-mednafen\_saturn, Ymir, Kronos).
* **DEINTERLACE**: removes the flickering of high-resolution games (Ymir, lr-ymir, lr-mednafen\_saturn: DEINTERLACE MODE).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (439).png" alt=""><figcaption></figcaption></figure></div>

### Expansion cartridges

Some games need a cartridge in the console slot:

* **RAM cartridges (1 MB / 4 MB)**: required by many Japanese SNK and Capcom games (_X-Men vs. Street Fighter_, _Marvel Super Heroes_, _Metal Slug_, _The King of Fighters '96_…). lr-kronos, Kronos, lr-mednafen\_saturn, Ymir and lr-ymir insert the right cartridge automatically for known games. Otherwise, choose it with the cartridge option (EMULATION submenu): **ADD-ON CARTRIDGE**, **CARTRIDGE**, **CARTRIDGE TYPE** or **EXPANSION CARTRIDGE** depending on the emulator.
* **ROM cartridges**: _The King of Fighters '95_ and _Ultraman: Hikari no Kyojin Densetsu_ need their own cartridge. Copy **mpr-18811-mx.ic1** and **mpr-19367-mx.ic1** to the bios folder: they are loaded automatically.
* **Backup memory cartridges**: extend the save memory.

### Using the console BIOS menu

Enable **START BIOS** (EMULATION submenu of Ymir, Kronos and YabaSanshiro) to start the console BIOS instead of the game: you can then manage the saves of the internal memory, set the clock and the language, or play audio CDs.

With Ymir, the memory manager is also available in the Ymir settings (HOTKEY + SOUTH or F1).

### SSF settings

By default, RetroBat writes its own SSF configuration and deletes the per-game settings of the `emulators\ssf\Setting\Saturn` folder at each launch. To use your own settings, enable **USE OWN GAME SETTING FILE**: RetroBat then changes nothing in the SSF configuration (controllers included).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (440).png" alt=""><figcaption></figcaption></figure></div>

## Known issues

| Problem                                                                 | Solution                                                                                                                    |
| ----------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Black screen or error at launch                                         | Check the BIOS (MISSING BIOS CHECK). With lr-mednafen\_saturn, Mednafen and BizHawk, add the BIOS matching the game region. |
| The game asks for an expansion cartridge or freezes on the title screen | Select a 4 MB RAM cartridge in the cartridge option, or use lr-kronos / Ymir which insert it automatically.                 |
| _KOF '95_ or _Ultraman_ do not start                                    | Copy mpr-18811-mx.ic1 / mpr-19367-mx.ic1 to the bios folder.                                                                |
| The game is not in the right language                                   | See "Changing the console language".                                                                                        |
| A .chd game does not start with Mednafen or BizHawk                     | These emulators do not support .chd: use the .cue version or another emulator.                                              |
| Slowdowns with lr-mednafen\_saturn                                      | Beetle Saturn needs a powerful CPU: use lr-kronos or Ymir.                                                                  |
| The 8BitDo M30 buttons are mixed up                                     | Enable USE SATURN-LIKE CONTROLLER.                                                                                          |
| My saves are missing after changing emulator                            | Each emulator has its own saves (see Folders).                                                                              |
