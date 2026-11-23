---
description: SNK
---

# Neo Geo Pocket

<div align="left"><figure><img src="../../../../.gitbook/assets/image (678).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Neo Geo Pocket** is SNK's first handheld console, released in Japan in October 1998. Its screen is **monochrome**, in shades of grey. Lacking success against the Game Boy, it was replaced as early as March 1999 by the Neo Geo Pocket Color, and has only about ten games (Samurai Shodown!, King of Fighters R-1, Neo Geo Cup '98…).

Like its successor, it stands out with its small microswitch stick, which "clicks" like an arcade stick, and its two buttons **A** and **B**.

Most Neo Geo Pocket Color games also run on the Neo Geo Pocket, in black and white (see [**Neo Geo Pocket or Neo Geo Pocket Color?**](neo-geo-pocket.md#neo-geo-pocket-or-neo-geo-pocket-color)). They have their own system in RetroBat (see the [**Neo Geo Pocket Color**](neo-geo-pocket-color.md) page).

{% embed url="https://en.wikipedia.org/wiki/Neo_Geo_Pocket" %}

## At a glance

<table><thead><tr><th width="225.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\ngp</code></td></tr><tr><td><strong>Extensions</strong></td><td>.ngp .ngc .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mednafen_ngp</td></tr><tr><td><strong>BIOS</strong></td><td>None (optional for ares)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk; Mednafen and ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores</td></tr><tr><td><strong>Netplay</strong></td><td>No (single-player console, link cable not emulated)</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                              | For whom?      | Strengths                                                                                                                | Limits                                                                                                   |
| ------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------- |
| **libretro: mednafen\_ngp** (default) | Everyone       | Beetle NeoPop, the libretro version of Mednafen's Neo Geo Pocket emulation: reliable, no BIOS needed, RetroAchievements. | —                                                                                                        |
| **libretro: race**                    | Alternative    | RACE, another very light emulator, no BIOS needed. RetroAchievements.                                                    | —                                                                                                        |
| **mednafen** (standalone)             | Mednafen users | Same emulation as the mednafen\_ngp core, with autofire buttons.                                                         | No RetroAchievements. Save states with hotkeys.                                                          |
| **ares**                              | Purists        | The most accurate emulation, with the real console BIOS.                                                                 | Needs the BIOS (see [**BIOS**](neo-geo-pocket.md#bios)). No RetroAchievements. Save states with hotkeys. |
| **bizhawk: NeoPop**                   | BizHawk users  | Mednafen's emulation in BizHawk, save states in the RetroBat menu.                                                       | —                                                                                                        |

**If in doubt, keep libretro: mednafen\_ngp.**

## BIOS

No BIOS is needed, except for **ares**. The other emulators have a built-in replacement BIOS.

<table><thead><tr><th width="204.25">File</th><th width="66.5">Folder</th><th width="323.75">MD5</th><th>Used by</th></tr></thead><tbody><tr><td><code>[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp</code></td><td><code>bios</code></td><td>d87d876c4391935c9d48ef352a3ff02d</td><td>ares, Neo Geo Pocket system</td></tr><tr><td><code>[BIOS] SNK Neo Geo Pocket Color (Japan, Europe) (En,Ja).ngp</code></td><td><code>bios</code></td><td>3655aacebb43a963607d4cf821fc1301</td><td>ares, Neo Geo Pocket Color system</td></tr></tbody></table>

ares takes the BIOS of the console of each system. If it is missing, it uses the other one: one of the two files is enough to play both systems. The files must have exactly these names.

> **Older installation**: RetroBat used to rely on a single file, `[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp`, which actually contained the **Color BIOS** (MD5 3655aacebb43a963607d4cf821fc1301). ares still works with this file. For each system to get the right BIOS, rename it to `[BIOS] SNK Neo Geo Pocket Color (Japan, Europe) (En,Ja).ngp`, then add the monochrome BIOS under the other name.

The RetroBat BIOS check lists them as optional.

On the first launch with ares, the BIOS may ask you to set the console language, date and time, as on the real machine. **EMULATION > FAST BOOT** (ares) skips the BIOS boot animation.

## Which game format should I use?

Games are `.ngp` files (Neo Geo Pocket games) or `.ngc` files (Neo Geo Pocket Color games), possibly compressed in `.zip` or `.7z` (one game per archive). Every emulator reads both formats.

### Neo Geo Pocket or Neo Geo Pocket Color?

RetroBat has two systems, `ngp` and `ngpc`, with the same emulators. Put each game in the system of its console.

* With the libretro cores, Mednafen and BizHawk, the emulator picks the mode from the game by itself: a color game is shown in color, even in the `ngp` system.
* With **ares**, the system picks the emulated console: `ngp` emulates the monochrome Neo Geo Pocket, `ngpc` the Neo Geo Pocket Color. In this system, ares emulates the **monochrome** console.
* On the real monochrome Neo Geo Pocket, most color games run in black and white. A few do not start (Sonic the Hedgehog Pocket Adventure, SNK vs. Capcom: The Match of the Millennium…).

## Controls

RetroBat sets up the controllers automatically. The console has a stick (on the controller d-pad), two buttons **A** and **B**, an **Option** button (pause and game menus) and a **Power** button.

| RetroBat controller | libretro cores | mednafen     | ares   | bizhawk |
| ------------------- | -------------- | ------------ | ------ | ------- |
| D-pad               | Stick          | Stick        | Stick  | Stick   |
| SOUTH               | A              | A            | A      | A       |
| EAST                | B              | B            | B      | B       |
| WEST                | —              | A (autofire) | —      | —       |
| NORTH               | —              | B (autofire) | —      | —       |
| START               | Option         | Option       | Option | Option  |
| L1                  | —              | —            | Power  | —       |

### Hotkeys

The libretro cores use the standard RetroArch hotkeys. Mednafen, ares and BizHawk use the common RetroBat hotkeys (save and load state, screenshot, fast forward…). See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

| Content                               | Folder                                                                                                                  |
| ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Games                                 | `roms\ngp`                                                                                                              |
| BIOS (ares)                           | `bios`                                                                                                                  |
| libretro cores, Mednafen: game saves  | `saves\ngp`                                                                                                             |
| libretro cores: save states           | `saves\ngp\libretro.<core>`                                                                                             |
| Mednafen: save states                 | `saves\ngp\mednafen\sstates`                                                                                            |
| ares: game saves and save states      | `saves\ngp\ares`                                                                                                        |
| BizHawk: game saves                   | `saves\ngp\bizhawk`                                                                                                     |
| BizHawk: save states                  | `saves\ngp\bizhawk\sstates\NeoPop`                                                                                      |
| Screenshots (Mednafen, ares, BizHawk) | <p><code>screenshots\mednafen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\ngp</code></p> |

## Guides

### Game language

Many games are bilingual English / Japanese: the console picks the language. RetroBat sets **English** by default.

* mednafen\_ngp and race cores, Mednafen, BizHawk: **EMULATION > CONSOLE LANGUAGE** (**ENGLISH** or **JAPANESE**). Restart the game after a change.
* ares: the language is set in the console BIOS menu, as on the real machine.

### RetroAchievements

Neo Geo Pocket and Neo Geo Pocket Color games are in the same RetroAchievements category. The mednafen\_ngp and race cores are compatible. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="83.25">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>ares</td><td><strong>VISUAL RENDERING > INTERFRAME BLENDING</strong></td><td>Mimics the ghosting of the LCD screen: some games use it for transparency effects.</td></tr><tr><td>ares</td><td><strong>VISUAL RENDERING > ACCURATE COLOR EMULATION</strong></td><td>Colors close to those of the original screen.</td></tr></tbody></table>

## Known issues

| Issue                                                           | Solution                                                                                                                                                              |
| --------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ares asks for a firmware or does not start                      | Neither BIOS is present, or they do not have exactly the right name in `bios` (see [**BIOS**](neo-geo-pocket.md#bios)). Or use another emulator, which needs no BIOS. |
| The BIOS check reports a different file (Neo Geo Pocket system) | The file `[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp` is the Color BIOS of an older installation: rename it (see [**BIOS**](neo-geo-pocket.md#bios)).      |
| A game is shown in black and white                              | With ares, the game is stored in the `ngp` system: move it to `roms\ngpc`.                                                                                            |
| A game is shown in Japanese                                     | Set **EMULATION > CONSOLE LANGUAGE** to **ENGLISH**, then restart the game. Some games only exist in Japanese.                                                        |
| A game offers a two-player mode with a cable                    | The link cable between two consoles (and the connection to the Dreamcast) is not emulated by any emulator.                                                            |
