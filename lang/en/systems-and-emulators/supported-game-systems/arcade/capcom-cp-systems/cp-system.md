---
description: Capcom
---

# CPS I

<div align="left"><figure><img src="../../../../.gitbook/assets/image (623).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **CP System** (Capcom Play System, or **CPS-1**) is Capcom's first arcade board, released in 1988. About thirty games use it until 1995, including many classics:

* the fighting games **Street Fighter II** (The World Warrior, Champion Edition, Hyper Fighting);
* the beat'em ups **Final Fight**, **Captain Commando**, **Knights of the Round**, **The King of Dragons**;
* the action and shooting games **Strider**, **Ghouls'n Ghosts**, **Forgotten Worlds**, **1941**, **Mercs**, **U.N. Squadron**.

The last games (sometimes called "CPS-1.5") add the QSound chip: **Cadillacs and Dinosaurs**, **The Punisher**, **Warriors of Fate**, **Saturday Night Slam Masters**.

In RetroBat, these games can also be stored in the FinalBurn Neo system (see the [**FinalBurn Neo**](../final-burn-neo.md) page).

{% embed url="https://en.wikipedia.org/wiki/CP_System" %}

## At a glance

<table><thead><tr><th width="231.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\cps1</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; FBNeo with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (fbneo recommended)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                        | For whom?                     | Strengths                                                                                                                                   | Limits                                                     |
| ------------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **libretro: fbneo** (default)   | Everyone                      | The current FinalBurn Neo in RetroArch: very compatible, layouts for 6-button games, dip switches, high scores, RetroAchievements, netplay. | —                                                          |
| **libretro: fbalpha2012\_cps1** | Very low-end PCs, old romsets | FB Alpha 2012 core dedicated to the CPS-1, very light.                                                                                      | FB Alpha 0.2.97.28 romset. Does not read `.7z`.            |
| **libretro: fbalpha**           | Old romsets                   | FB Alpha 0.2.97.44.                                                                                                                         | Romset of its own version, no longer updated.              |
| **libretro: fbalpha2012**       | Old romsets                   | FB Alpha 0.2.97.29.                                                                                                                         | Romset of its own version.                                 |
| **fbneo** (standalone)          | Cabinets, arcade sticks       | The official FBNeo, buttons set game by game by RetroBat (see the [**FinalBurn Neo**](../final-burn-neo.md) page).                          | No RetroAchievements or netplay. Save states with hotkeys. |

**If in doubt, keep libretro: fbneo.**

## BIOS

No BIOS is needed.

## Which game format should I use?

Games are `.zip` or `.7z` romsets, to keep compressed and under their original name (`sf2ce.zip`…). The romset must match the emulator version:

<table><thead><tr><th width="306.5">Emulator</th><th>Romset version</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (standalone)</td><td>Latest FBNeo version</td></tr><tr><td>libretro: fbalpha2012_cps1</td><td>FB Alpha 0.2.97.28 (<code>.zip</code> only)</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

The fbalpha2012\_cps1 core is not offered for a `.7z` game. For details about romsets (non-merged, split, merged), see the [**Arcade Guide**](../../../arcade-guide.md) page.

## Controls

RetroBat sets up the controllers automatically. **SELECT** inserts a coin, **START** starts the game, the left stick and the d-pad move the player.

### fbneo core

The **CONTROLS > CONTROLLER TYPE** option picks the layout. For 6-button fighting games (Street Fighter II):

| RetroBat controller | CLASSIC (default) | MODERN       |
| ------------------- | ----------------- | ------------ |
| WEST                | Light punch       | Light punch  |
| NORTH               | Medium punch      | Medium punch |
| L1                  | Heavy punch       | —            |
| R1                  | Heavy kick        | Heavy punch  |
| R2                  | —                 | Heavy kick   |
| SOUTH               | Light kick        | Light kick   |
| EAST                | Medium kick       | Medium kick  |

The other games use the face buttons in order: SOUTH = button 1, EAST = button 2, WEST = button 3, NORTH = button 4.

**6-BUTTON PANEL** suits an arcade stick with two rows of three buttons. The other choices are described on the [**FinalBurn Neo**](../final-burn-neo.md) page.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (624).png" alt=""><figcaption></figcaption></figure></div>

### fbalpha2012\_cps1 core

Buttons are placed as with the fbneo core in CLASSIC. This core has no layout option.

### FBNeo (standalone)

RetroBat sets the buttons game by game with the `fbneo.yml` mapping file: see the [**FinalBurn Neo**](../final-burn-neo.md) page.

### Hotkeys

The libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page). For standalone FBNeo, see the [**FinalBurn Neo**](../final-burn-neo.md) page.

## Folders

| Content                                                   | Folder                                                                                                                                                                             |
| --------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Games                                                     | `roms\cps1`                                                                                                                                                                        |
| fbneo core: NVRAM, EEPROM, high scores                    | `saves\cps1\fbneo`                                                                                                                                                                 |
| fbalpha2012\_cps1, fbalpha, fbalpha2012 cores: game saves | `saves\cps1`                                                                                                                                                                       |
| libretro cores: save states                               | `saves\cps1\libretro.<core>`                                                                                                                                                       |
| High score file (`hiscore.dat`)                           | <p><code>bios\fbneo</code> (fbneo)</p><p><code>bios\fba</code> (fbalpha), copied to <code>bios\fbalpha2012</code> (fbalpha2012_cps1) and <code>saves\cps1</code> (fbalpha2012)</p> |
| Standalone FBNeo                                          | See the [**FinalBurn Neo**](../final-burn-neo.md) page                                                                                                                             |

## Guides

### Service menu and dip switches

The cabinet service menu sets the difficulty, the number of lives, free play…

* fbneo core: **START + L1 + R1**, or another combination with **EMULATION > DIAGNOSTIC MENU INPUT**.
* **R3** opens the service menu (fbalpha2012\_cps1 core).

The board **dip switches** are set in the RetroArch menu (**HOTKEY + SOUTH**), **Core Options > Dip switches** (fbneo core). **EMULATION > ENABLE FREE PLAY** (fbneo core) sets free play directly when the game allows it.

### Vertical games

Vertical shoot'em ups (1941, Mercs, Varth) are displayed the right way up, with a vertical decoration.

* fbneo core: **VIDEO > TATE MODE** rotates the picture for a screen standing vertically.
* fbalpha2012\_cps1 core: **VIDEO > AUTO ROTATE**, on by default, rotates the picture of vertical games. When off, the directions are rotated for a screen standing vertically.
* Standalone FBNeo: **VIDEO > VERTICAL MONITOR INDEX** shows vertical games on another screen.

### High scores

**EMULATION > ENABLE HISCORES**, on by default, keeps the high scores of compatible games. RetroBat provides the `hiscore.dat` file to each core (see [**Folders**](cp-system.md#folders)).

### RetroAchievements

The fbneo core is the best supported by RetroAchievements for arcade. In hardcore mode, keep **EMULATION > CPU OVERCLOCK** at 100% or more. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="218.25">Emulator</th><th width="241.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td>fbneo, fbalpha2012_cps1</td><td><strong>EMULATION > CPU OVERCLOCK</strong></td><td>Reduces the original slowdowns of some games. Can cause glitches.</td></tr><tr><td>fbneo</td><td><strong>VIDEO > FORCE 60HZ</strong></td><td>Forces games to 60 Hz (original rate: about 59.6 Hz).</td></tr><tr><td>fbalpha2012_cps1</td><td><strong>VIDEO > FRAMESKIP</strong></td><td>Skips frames on a PC that is too slow.</td></tr><tr><td>fbneo</td><td><strong>AUDIO > LOWPASS FILTER</strong></td><td>Softens the sound.</td></tr><tr><td>fbalpha2012_cps1</td><td><strong>AUDIO > AUDIO FILTER</strong></td><td>Softens the sound (from 0 to 95%).</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="356.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start, or a file is missing</td><td>The romset does not match the emulator version (see <a href="cp-system.md#which-game-format-should-i-use"><strong>Which game format should I use?</strong></a>).</td></tr><tr><td>The fbalpha2012_cps1 core is not offered</td><td>The game is a <code>.7z</code>: this core only reads <code>.zip</code>.</td></tr><tr><td>High scores are not kept</td><td>The game is not in <code>hiscore.dat</code>, or <strong>ENABLE HISCORES</strong> is off. They are not kept in netplay.</td></tr><tr><td>RetroAchievements switches to normal mode</td><td><strong>CPU OVERCLOCK</strong> is below 100%, or cheats are active.</td></tr></tbody></table>
