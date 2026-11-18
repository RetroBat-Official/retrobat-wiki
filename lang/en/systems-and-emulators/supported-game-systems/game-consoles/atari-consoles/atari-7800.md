---
description: Atari
---

# Atari 7800

<div align="left"><figure><img src="../../../../.gitbook/assets/image (635).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Atari 7800 ProSystem** was shown in 1984, but only really came out in 1986, after Jack Tramiel bought Atari. Its MARIA graphics chip displays far more sprites than Atari's earlier consoles. It also runs almost all Atari 2600 games. Its controller, the **ProLine**, has two buttons. The console was discontinued in 1992.

Its library has about sixty games: Asteroids, Ms. Pac-Man, Food Fight, Ballblazer, Choplifter!, Karateka, Commando, Ninja Golf, Midnight Mutants… 2600 games have their own system in RetroBat (see the [**Atari 2600**](atari-2600.md) page).

{% embed url="https://en.wikipedia.org/wiki/Atari_7800" %}

## At a glance

<table><thead><tr><th width="225.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\atari7800</code></td></tr><tr><td><strong>Extensions</strong></td><td>.a78 .bin .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: prosystem</td></tr><tr><td><strong>BIOS</strong></td><td>None (required for BizHawk)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro core, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro core, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="145.25">Emulator</th><th width="144">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: prosystem</strong> (default)</td><td>Everyone</td><td>ProSystem: light, no BIOS, built-in game database, RetroAchievements.</td><td>—</td></tr><tr><td><strong>bizhawk: A78</strong></td><td>BizHawk users</td><td>A7800Hawk: accurate emulation, High Score cartridge (high scores), RetroAchievements, save states in the RetroBat menu.</td><td>Needs the BIOS (see <a href="atari-7800.md#bios"><strong>BIOS</strong></a>).</td></tr></tbody></table>

**If in doubt, keep libretro: prosystem.**

## BIOS

ProSystem needs no BIOS: it uses the BIOS of the game's region when present (Atari boot screen). BizHawk needs the BIOS of the game's region: it does not start the game without it.

<table><thead><tr><th width="175.5">File</th><th width="74">Folder</th><th width="334">MD5</th><th>Used by</th></tr></thead><tbody><tr><td><code>7800 BIOS (U).rom</code></td><td><code>bios</code></td><td>0763f1ffb006ddbe32e52d497ee848ae</td><td>ProSystem (optional), BizHawk (NTSC games)</td></tr><tr><td><code>7800 BIOS (E).rom</code></td><td><code>bios</code></td><td>397bb566584be7b9764e7a68974c4263</td><td>ProSystem (optional), BizHawk (PAL games)</td></tr><tr><td><code>A78_highscore.bin</code></td><td><code>bios</code></td><td>—</td><td>BizHawk: High Score cartridge (optional)</td></tr></tbody></table>

The RetroBat BIOS check lists them as optional, as the default emulator does not need them. Files must have exactly these names.

> **Older installation**: the `ProSystem.dat` file is no longer used, the game database is built into the core. You can delete it from `bios`.

Atari's **High Score** cartridge kept the high scores of compatible games (Asteroids, Food Fight…). BizHawk emulates this cartridge when `A78_highscore.bin` is present.

## Which game format?

Games are `.a78` files, possibly compressed as `.zip` or `.7z` (one game per archive). The `.a78` file has a header that describes the cartridge (size, POKEY sound chip, region). `.bin` files have no header: the emulator has to guess the cartridge type. Prefer `.a78` files.

## Controls

RetroBat configures controllers automatically. The ProLine controller has two buttons: one-button games accept both. The console switches are on the controller.

| RetroBat controller | libretro: prosystem | bizhawk  |
| ------------------- | ------------------- | -------- |
| D-pad               | Joystick            | Joystick |
| SOUTH               | Button 1            | Button 1 |
| EAST                | Button 2            | Button 2 |
| NORTH               | Reset               | Reset    |
| START               | Pause               | Pause    |
| SELECT              | Select              | —        |
| L1                  | Left difficulty     | —        |
| R1                  | Right difficulty    | —        |
| L2                  | —                   | Select   |

With BizHawk, the controller's SELECT button is used for hotkeys: the console's Select switch is on L2.

### Hotkeys

ProSystem uses the standard RetroArch hotkeys. BizHawk uses the common RetroBat hotkeys. See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="245.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\atari7800</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>ProSystem: save states</td><td><code>saves\atari7800\libretro.prosystem</code></td></tr><tr><td>BizHawk: game saves</td><td><code>saves\atari7800\bizhawk</code></td></tr><tr><td>BizHawk: save states</td><td><code>saves\atari7800\bizhawk\sstates\A78</code></td></tr><tr><td>BizHawk: screenshots</td><td><code>screenshots\bizhawk\atari7800</code></td></tr></tbody></table>

## Guides

### Dual stick games

Robotron: 2084 and T:ME Salvo are played with two joysticks. **CONTROLS > DUAL STICK** (ProSystem) puts the second joystick on player 1's right stick.

### RetroAchievements

ProSystem and BizHawk are compatible. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="130.75">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>ProSystem</td><td><strong>VISUAL RENDERING > COLOR DEPTH</strong></td><td><strong>24 BIT</strong>: more accurate colors.</td></tr><tr><td>ProSystem</td><td><strong>AUDIO > AUDIO FILTER</strong></td><td>Softens the harsh sound of some games.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="351.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>BizHawk does not start the game or asks for a firmware</td><td>The BIOS of the game's region is missing from <code>bios</code> (see <a href="atari-7800.md#bios"><strong>BIOS</strong></a>), or it does not have exactly the right name.</td></tr><tr><td>The game stays paused or does not start</td><td>Press START (Pause) or NORTH (Reset).</td></tr><tr><td>A <code>.bin</code> game does not start</td><td>Use the <code>.a78</code> version of the game.</td></tr><tr><td>Light gun games do not respond</td><td>RetroBat does not set up the light gun (Alien Brigade, Barnyard Blaster, Crossbow, Meltdown) with any emulator.</td></tr></tbody></table>
