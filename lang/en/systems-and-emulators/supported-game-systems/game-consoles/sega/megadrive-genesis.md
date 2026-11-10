---
description: Sega
---

# Megadrive - Genesis

<table data-header-hidden><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><img src="../../../../.gitbook/assets/image (457).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (458).png" alt="" data-size="original"></td><td></td></tr></tbody></table>

The **Mega Drive** (called **Genesis** in North America) is Sega's 16-bit console. It was released in Japan in October 1988, in North America in 1989 and in Europe in 1990. Built around a Motorola 68000 processor, with a Z80 and a Yamaha YM2612 FM sound chip, it brought arcade-quality games into the living room and sold around 30 million units. Its library counts more than 900 games: _Sonic the Hedgehog_, _Streets of Rage 2_, _Gunstar Heroes_, _Phantasy Star IV_, _Shinobi III_, _Ecco the Dolphin_, _Thunder Force IV_…

The original pad has **3 buttons** (A, B, C). A **6-button pad** (adding X, Y, Z and a MODE button) followed in 1993, mainly for fighting games such as _Street Fighter II'_.

The Mega-CD, 32X and MSU-MD games have their own systems: see the [Mega-CD](mega-cd-sega-cd.md), [32X](sega-32x.md) and [Megadrive (MSU)](megadrive-genesis-msu.md) pages.

{% embed url="https://en.wikipedia.org/wiki/Sega_Genesis" %}

## At a glance

<table><thead><tr><th width="249"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\megadrive</code></td></tr><tr><td><strong>Extensions</strong></td><td>.68k .sgd .smd .bin .gen .md .sg .wad .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: genesis_plus_gx</td></tr><tr><td><strong>BIOS</strong></td><td>None required</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BlastEm, Jgenesis, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (genesis_plus_gx)</td></tr></tbody></table>

## Which emulator to choose?

| Emulator                                  | Strengths                                                                               | Limits                                             |
| ----------------------------------------- | --------------------------------------------------------------------------------------- | -------------------------------------------------- |
| **libretro: genesis\_plus\_gx** (default) | Accurate and complete: 3/6-button pads, multitaps, mouse, lightguns, lock-on cartridges |                                                    |
| libretro: genesis\_plus\_gx\_wide         | Same, with a widescreen (16:9) display                                                  | Graphic glitches on the screen sides in some games |
| libretro: genesis\_plus\_gx\_expanded     | Plays very large ROMs and **Paprium**                                                   | Use it only for these games                        |
| libretro: picodrive                       | Very fast, for modest PCs                                                               | Less accurate                                      |
| libretro: fbneo                           | FBNeo alternative                                                                       | Games must be named as in the FBNeo database       |
| jgenesis                                  | Recent and accurate standalone emulator, shaders                                        | 2 players, no RetroAchievements                    |
| blastem                                   | Very accurate standalone emulator, multitap, console model choice                       | No RetroAchievements                               |
| mednafen                                  | Accurate, multitap                                                                      | No RetroAchievements                               |
| ares                                      | Accurate multi-system emulator                                                          | 2 players, no RetroAchievements                    |
| kega-fusion                               | Historical emulator, light, multitap                                                    | No longer maintained                               |
| bizhawk: Genplus-gx                       | Genesis Plus GX with BizHawk's tools (TAS, RetroAchievements)                           | 2 players                                          |

## BIOS

No BIOS is needed to play. A few optional files add extra features with the Genesis Plus GX cores. Copy them to the `bios` folder:

<table><thead><tr><th width="159.5">File</th><th>Used for</th><th>MD5</th></tr></thead><tbody><tr><td>bios_MD.bin</td><td>Show the original console boot screen (START ORIGINAL BIOS option)</td><td>45e298905a08f9cfb38fd504cd6dbc84</td></tr><tr><td>sk.bin</td><td>Sonic &#x26; Knuckles lock-on</td><td>4ea493ea4e9f6c9ebfccbdb15110367e</td></tr><tr><td>sk2chip.bin</td><td>Sonic &#x26; Knuckles lock-on (Sonic 2 part)</td><td>b4e76e416b887f4e7413ba76fa735f16</td></tr><tr><td>ggenie.bin</td><td>Game Genie cartridge</td><td>b5d5ff1147036b06944b4d2cac2dd1e7</td></tr><tr><td>areplay.bin</td><td>Action Replay cartridge</td><td>a0028b3043f9d59ceeb03da5b073b30d</td></tr></tbody></table>

{% hint style="info" %}
RetroBat lists these files as OPTIONAL: their absence never prevents a game from starting.
{% endhint %}

### Game region

The Mega Drive has no system language: the region decides which version of a game runs (Japanese, American or European, 60 or 50 Hz). Every emulator detects it automatically. To force it, use CONSOLE REGION (lr-genesis\_plus\_gx, BizHawk, Kega Fusion), REGION (lr-picodrive), FORCE REGION (BlastEm, Jgenesis) or PREFERRED REGION (Ares).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (471).png" alt=""><figcaption></figcaption></figure></div>

## Game formats

<table><thead><tr><th width="282.75">Format</th><th>Description</th></tr></thead><tbody><tr><td>.md / .bin / .gen / .smd</td><td>Cartridge dump (the most common formats)</td></tr><tr><td>.68k / .sgd / .sg / .wad</td><td>Other cartridge formats</td></tr><tr><td>.zip / .7z</td><td>Compressed games</td></tr></tbody></table>

## Controls

### Controller autoconfiguration

<table><thead><tr><th>Emulator</th><th width="175.75">Autoconfig</th><th>Players</th></tr></thead><tbody><tr><td>lr-genesis_plus_gx (all 3 cores)</td><td>Yes</td><td>2, up to 8 with a multitap (CONTROLLER TYPE)</td></tr><tr><td>lr-picodrive</td><td>Yes</td><td>2</td></tr><tr><td>lr-fbneo</td><td>Yes</td><td>2</td></tr><tr><td>Jgenesis</td><td>Yes</td><td>2</td></tr><tr><td>BlastEm</td><td>Yes</td><td>2, up to 8 (USE MULTITAP)</td></tr><tr><td>Mednafen</td><td>Yes</td><td>2, up to 8 (USE MULTITAP)</td></tr><tr><td>Ares</td><td>Yes</td><td>2</td></tr><tr><td>Kega Fusion</td><td>Yes</td><td>2, up to 8 (USE MULTITAP, automatic beyond 2 controllers)</td></tr><tr><td>BizHawk</td><td>Yes</td><td>2</td></tr></tbody></table>

### Default layout (6-button pad)

| Mega Drive | Controller |   | Mega Drive | Controller |
| ---------- | ---------- | - | ---------- | ---------- |
| A          | WEST       |   | X          | L1         |
| B          | SOUTH      |   | Y          | NORTH      |
| C          | EAST       |   | Z          | R1         |
| START      | START      |   | MODE       | SELECT     |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (459).png" alt="" width="225"><figcaption></figcaption></figure></div>

The D-pad and the left stick both act as the Mega Drive D-pad.

### Other layouts

The **BUTTON LAYOUT** option (CONTROLS submenu) moves the buttons, for example to put C or Z on a shoulder button. The tattoo follows the chosen layout.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (470).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th>Option</th><th width="79.25">WEST</th><th width="78">SOUTH</th><th width="80.5">EAST</th><th width="96.25">NORTH</th><th width="93.5">L1</th><th width="118">R1</th></tr></thead><tbody><tr><td>L/R as X/Z (default)</td><td>A</td><td>B</td><td>C</td><td>Y</td><td>X</td><td>Z</td></tr><tr><td>L/R as Z/C</td><td>X</td><td>A</td><td>B</td><td>Y</td><td>Z</td><td>C</td></tr><tr><td>L/R as Y/Z</td><td>A</td><td>B</td><td>C</td><td>X</td><td>Y</td><td>Z</td></tr><tr><td>L/R as Y/B</td><td>X</td><td>A</td><td>C</td><td>Z</td><td>Y</td><td>B</td></tr><tr><td>L/R as B/Y</td><td>X</td><td>A</td><td>C</td><td>Z</td><td>B</td><td>Y</td></tr></tbody></table>

<table><thead><tr><th width="325.25">Option / emulator</th><th>Control layout</th></tr></thead><tbody><tr><td>L/R as Z/C</td><td><img src="../../../../.gitbook/assets/image (461).png" alt="" data-size="original"></td></tr><tr><td>L/R as Y/Z</td><td><img src="../../../../.gitbook/assets/image (462).png" alt="" data-size="original"></td></tr><tr><td>L/R as Y/B</td><td><img src="../../../../.gitbook/assets/image (465).png" alt=""></td></tr><tr><td>L/R as B/Y</td><td><img src="../../../../.gitbook/assets/image (464).png" alt=""></td></tr></tbody></table>

Available with every emulator.

### 3-button pad

Some early games misbehave with a 6-button pad (buttons or menus triggering on their own). Switch to the 3-button pad: A, B and C then stay on WEST, SOUTH and EAST, whatever the layout.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (469).png" alt=""><figcaption></figcaption></figure></div>

| Emulator                                       | Option                             |
| ---------------------------------------------- | ---------------------------------- |
| lr-genesis\_plus\_gx                           | CONTROLLER TYPE > JOYPAD 3 BUTTONS |
| Mednafen                                       | CONTROLLER TYPE                    |
| lr-picodrive, Jgenesis, BlastEm, Ares, BizHawk | USE 3 BUTTON CONTROLLER            |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (460).png" alt="" width="225"><figcaption></figcaption></figure></div>

Ares switches to 3 buttons by itself for the games known to be incompatible.

### Mega Drive-style controllers

RetroBat recognises controllers that reproduce the Mega Drive pad (8BitDo M30) and maps them button for button. Depending on the controller mode, this is automatic or requires the **USE GENESIS-LIKE CONTROLLER** option (CONTROLS submenu). In Kega Fusion, choose YES(DPAD) or YES(ANALOG).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (468).png" alt=""><figcaption></figcaption></figure></div>

Full list of controllers and modes: see the [Special controllers page](../../../../controllers/supported-controllers/gamepads/special-controllers.md).

### Multitaps (up to 8 players)

Some games accept more than 2 players with an adapter: the Sega **Team Player** (_Gauntlet IV_…) or the EA **4-Way Play** (EA Sports games such as _FIFA_ or _NHL_).

<table><thead><tr><th width="222.75">Emulator</th><th>Option</th></tr></thead><tbody><tr><td>lr-genesis_plus_gx</td><td>CONTROLLER TYPE > JOYPAD 3/6 BUTTONS + TEAMPLAYER, or + 4-WAY PLAY</td></tr><tr><td>BlastEm</td><td>USE MULTITAP: PORT 1, PORT 2 or BOTH PORTS</td></tr><tr><td>Mednafen</td><td>USE MULTITAP</td></tr><tr><td>Kega Fusion</td><td>USE MULTITAP (automatic when more than 2 controllers are connected)</td></tr></tbody></table>

### Lightguns, mouse and analog joystick

With the Genesis Plus GX cores:

* **Lightguns**: enable the guns (GUNS submenu) and choose the GUN TYPE: **Menacer** (_T2: The Arcade Game_, _Body Count_, _Menacer 6-in-1_…) or **Justifier** (_Lethal Enforcers I_ and _II_). See the Lightguns page.
* **Mouse**: CONTROLLER TYPE > MOUSE, for the rare games compatible with the Sega Mouse.
* **XE-1AP**: CONTROLLER TYPE > XE-1AP, the analog joystick used by a few games such as _After Burner II_.

### Hotkeys

**libretro cores and Mednafen**: [standard RetroBat hotkeys](../../../../navigation/hotkeys.md).

<table><thead><tr><th>Hotkey</th><th width="103">BlastEm</th><th width="99.75">Jgenesis</th><th width="100.5">Ares</th><th width="97.25">BizHawk</th><th width="140.75">Kega Fusion</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td><td>Quit</td><td>Quit</td><td>Quit</td><td>Quit</td></tr><tr><td>HOTKEY + WEST</td><td>Save state</td><td>Save state</td><td>Save state</td><td>Save state</td><td></td></tr><tr><td>HOTKEY + NORTH</td><td>Load state</td><td>Load state</td><td>Load state</td><td>Load state</td><td></td></tr></tbody></table>

## Folders

<table><thead><tr><th width="129.5">Emulator</th><th width="169">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro</td><td>Saves</td><td><code>saves\megadrive</code></td></tr><tr><td>libretro</td><td>Save states</td><td><code>saves\megadrive\libretro.&#x3C;core></code></td></tr><tr><td>BlastEm</td><td>Saves and save states</td><td><code>saves\megadrive\blastem\&#x3C;game></code></td></tr><tr><td>Jgenesis</td><td>Saves</td><td><code>saves\megadrive\jgenesis</code></td></tr><tr><td>Mednafen</td><td>Saves / save states</td><td><code>saves\megadrive</code> / <code>saves\megadrive\mednafen\sstates</code></td></tr><tr><td>Ares</td><td>Saves</td><td><code>saves\megadrive\ares</code></td></tr><tr><td>Kega Fusion</td><td>Saves / save states</td><td><code>saves\megadrive</code> / <code>saves\megadrive\kega-fusion\sstates</code></td></tr><tr><td>BizHawk</td><td>Saves</td><td><code>saves\megadrive\bizhawk</code></td></tr><tr><td>Screenshots</td><td></td><td><code>screenshots</code> (subfolder per emulator)</td></tr></tbody></table>

## Guides

### Playing Paprium

_Paprium_ (WaterMelon, 2020) is a beat 'em up whose cartridge contains an extra chip and a CD-quality soundtrack. Only the **genesis\_plus\_gx\_expanded** core plays it fully: with the standard core, only the demo mini-game starts.

1. Copy the game to `roms\megadrive`.
2. For the music, create the `roms\megadrive\paprium` folder and copy the MP3 files of the official soundtrack into it, **with their original names** (for example `02 90's Acid Dub Character Select.mp3`). Without them, the game has no music.
3. In the game options, set the emulator to **libretro: genesis\_plus\_gx\_expanded**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure></div>

4. Do not enable run-ahead with this game.

Recent FBNeo versions also play Paprium: the game must then be in `roms\megadrive\paprium.zip` and the MP3 files in `bios\fbneo\samples\paprium.zip`.

### Sonic & Knuckles lock-on

On the console, _Sonic & Knuckles_ accepts another cartridge on top of it (_Sonic 2_, _Sonic 3_). With lr-genesis\_plus\_gx, copy `sk.bin` (and `sk2chip.bin` for Sonic 2) to `bios`, set **CARTRIDGE LOCK-ON** to SONIC AND KNUCKLES, then start the _Sonic 2_ or _Sonic 3_ game. The same option loads the Game Genie (`ggenie.bin`) and the Action Replay (`areplay.bin`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure></div>

### Widescreen

The **genesis\_plus\_gx\_wide** core displays the games in 16:9 by drawing extra columns on the sides. The **WIDESCREEN - EXTRA COLUMNS TO DRAW** option sets their number. Some games show glitches on the edges: switch back to the standard core for them.

## Known issues

<table><thead><tr><th width="320.25">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>A game reacts strangely (buttons or menus on their own)</td><td>Use the 3-button pad.</td></tr><tr><td>The buttons are not where I expect</td><td>Change BUTTON LAYOUT, or check that USE GENESIS-LIKE CONTROLLER is off with a standard controller.</td></tr><tr><td>My 8BitDo M30 is not mapped correctly</td><td>Enable USE GENESIS-LIKE CONTROLLER (X-input and Switch modes). See the <a href="../../../../controllers/supported-controllers/gamepads/special-controllers.md">Special controllers page</a>.</td></tr><tr><td>A game does not start with lr-fbneo</td><td>FBNeo only accepts games named as in its database: use lr-genesis_plus_gx.</td></tr><tr><td>Paprium only runs a mini-game</td><td>Use the genesis_plus_gx_expanded core.</td></tr><tr><td>A game runs too fast or too slow</td><td>Wrong region (PAL/NTSC): force the region in the emulator options.</td></tr><tr><td>Only 2 players in a 4-player game</td><td>Enable a multitap (CONTROLLER TYPE or USE MULTITAP).</td></tr></tbody></table>

