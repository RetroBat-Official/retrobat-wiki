---
description: SNK
---

# Neo Geo Pocket Color

<div align="left"><figure><img src="../../../../.gitbook/assets/image (679).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Neo Geo Pocket Color** is the color version of SNK's handheld console, released in March 1999 in Japan, then in North America and Europe. It was discontinued in 2000 outside Japan and in 2001 in Japan, after SNK was bought out.

Its library has about 80 games, many of them fighting games and arcade adaptations: SNK vs. Capcom: The Match of the Millennium, The King of Fighters R-2, Metal Slug 1st and 2nd Mission, Sonic the Hedgehog Pocket Adventure… It stands out with its small microswitch stick, which "clicks" like an arcade stick, and its two buttons **A** and **B**.

It also plays every Neo Geo Pocket game; the Neo Geo Pocket has its own system in RetroBat (see the [**Neo Geo Pocket**](neo-geo-pocket.md) page).

{% embed url="https://en.wikipedia.org/wiki/Neo_Geo_Pocket_Color" %}

## At a glance

<table><thead><tr><th width="241.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\ngpc</code></td></tr><tr><td><strong>Extensions</strong></td><td>.ngp .ngc .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mednafen_ngp</td></tr><tr><td><strong>BIOS</strong></td><td>None (optional for ares)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk; Mednafen and ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores</td></tr><tr><td><strong>Netplay</strong></td><td>No (single-player console, link cable not emulated)</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="150.25">Emulator</th><th>For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: mednafen_ngp</strong> (default)</td><td>Everyone</td><td>Beetle NeoPop, the libretro version of Mednafen's Neo Geo Pocket emulation: reliable, no BIOS needed, RetroAchievements.</td><td>—</td></tr><tr><td><strong>libretro: race</strong></td><td>Alternative</td><td>RACE, another very light emulator, no BIOS needed. RetroAchievements.</td><td>—</td></tr><tr><td><strong>mednafen</strong> (standalone)</td><td>Mednafen users</td><td>Same emulation as the mednafen_ngp core, with autofire buttons.</td><td>No RetroAchievements. Save states with hotkeys.</td></tr><tr><td><strong>ares</strong></td><td>Purists</td><td>The most accurate emulation, with the real console BIOS.</td><td>Needs the BIOS (see <a href="neo-geo-pocket-color.md#bios"><strong>BIOS</strong></a>). No RetroAchievements. Save states with hotkeys.</td></tr><tr><td><strong>bizhawk: NeoPop</strong></td><td>BizHawk users</td><td>Mednafen's emulation in BizHawk, save states in the RetroBat menu.</td><td>—</td></tr></tbody></table>

**If in doubt, keep libretro: mednafen\_ngp.**

## BIOS

No BIOS is needed, except for **ares**. The other emulators have a built-in replacement BIOS.

<table><thead><tr><th width="185">File</th><th width="67.75">Folder</th><th width="319.5">MD5</th><th>Used by</th></tr></thead><tbody><tr><td><code>[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp</code></td><td><code>bios</code></td><td>d87d876c4391935c9d48ef352a3ff02d</td><td>ares, Neo Geo Pocket system</td></tr><tr><td><code>[BIOS] SNK Neo Geo Pocket Color (Japan, Europe) (En,Ja).ngp</code></td><td><code>bios</code></td><td>3655aacebb43a963607d4cf821fc1301</td><td>ares, Neo Geo Pocket Color system</td></tr></tbody></table>

ares takes the BIOS of the console of each system. If it is missing, it uses the other one: one of the two files is enough to play both systems. The files must have exactly these names.

> **Older installation**: RetroBat used to rely on a single file, `[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp`, which actually contained the **Color BIOS** (MD5 3655aacebb43a963607d4cf821fc1301). ares still works with this file. For each system to get the right BIOS, rename it to `[BIOS] SNK Neo Geo Pocket Color (Japan, Europe) (En,Ja).ngp`, then add the monochrome BIOS under the other name.

The RetroBat BIOS check lists them as optional.

On the first launch with ares, the BIOS may ask you to set the console language, date and time, as on the real machine. **EMULATION > FAST BOOT** (ares) skips the BIOS boot animation.

## Which game format should I use?

Games are `.ngp` files (Neo Geo Pocket games) or `.ngc` files (Neo Geo Pocket Color games), possibly compressed in `.zip` or `.7z` (one game per archive). Every emulator reads both formats.

### Neo Geo Pocket or Neo Geo Pocket Color?

RetroBat has two systems, `ngp` and `ngpc`, with the same emulators. Put each game in the system of its console.

* With the libretro cores, Mednafen and BizHawk, the emulator picks the mode from the game by itself: a color game is shown in color, even in the `ngp` system.
* With **ares**, the system picks the emulated console: `ngp` emulates the monochrome Neo Geo Pocket, `ngpc` the Neo Geo Pocket Color. In this system, ares emulates the **color** console.
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

| Content                               | Folder                                                                                                                   |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Games                                 | `roms\ngpc`                                                                                                              |
| BIOS (ares)                           | `bios`                                                                                                                   |
| libretro cores, Mednafen: game saves  | `saves\ngpc`                                                                                                             |
| libretro cores: save states           | `saves\ngpc\libretro.<core>`                                                                                             |
| Mednafen: save states                 | `saves\ngpc\mednafen\sstates`                                                                                            |
| ares: game saves and save states      | `saves\ngpc\ares`                                                                                                        |
| BizHawk: game saves                   | `saves\ngpc\bizhawk`                                                                                                     |
| BizHawk: save states                  | `saves\ngpc\bizhawk\sstates\NeoPop`                                                                                      |
| Screenshots (Mednafen, ares, BizHawk) | <p><code>screenshots\mednafen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\ngpc</code></p> |

## Guides

### Game language

Many games are bilingual English / Japanese: the console picks the language. RetroBat sets **English** by default.

* mednafen\_ngp and race cores, Mednafen, BizHawk: **EMULATION > CONSOLE LANGUAGE** (**ENGLISH** or **JAPANESE**). Restart the game after a change.
* ares: the language is set in the console BIOS menu, as on the real machine.

### RetroAchievements

Neo Geo Pocket and Neo Geo Pocket Color games are in the same RetroAchievements category. The mednafen\_ngp and race cores are compatible. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="90.75">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>ares</td><td><strong>VISUAL RENDERING > INTERFRAME BLENDING</strong></td><td>Mimics the ghosting of the LCD screen: some games use it for transparency effects.</td></tr><tr><td>ares</td><td><strong>VISUAL RENDERING > ACCURATE COLOR EMULATION</strong></td><td>Colors close to those of the original screen.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="344">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>ares asks for a firmware or does not start</td><td>Neither BIOS is present, or they do not have exactly the right name in <code>bios</code> (see <a href="neo-geo-pocket-color.md#bios"><strong>BIOS</strong></a>). Or use another emulator, which needs no BIOS.</td></tr><tr><td>The BIOS check reports a different file (Neo Geo Pocket system)</td><td>The file <code>[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp</code> is the Color BIOS of an older installation: rename it (see <a href="neo-geo-pocket-color.md#bios"><strong>BIOS</strong></a>).</td></tr><tr><td>A game is shown in black and white</td><td>With ares, the game is stored in the <code>ngp</code> system: move it to <code>roms\ngpc</code>.</td></tr><tr><td>A game is shown in Japanese</td><td>Set <strong>EMULATION > CONSOLE LANGUAGE</strong> to <strong>ENGLISH</strong>, then restart the game. Some games only exist in Japanese.</td></tr><tr><td>A game offers a two-player mode with a cable</td><td>The link cable between two consoles (and the connection to the Dreamcast) is not emulated by any emulator.</td></tr></tbody></table>
