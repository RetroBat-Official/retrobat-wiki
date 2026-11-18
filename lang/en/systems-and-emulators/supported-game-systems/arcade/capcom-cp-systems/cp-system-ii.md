---
description: Capcom
---

# CPS II

<div align="left"><figure><img src="../../../../.gitbook/assets/image (625).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **CP System II** (**CPS-2**) succeeded the CPS-1 in 1993. More than 40 games use it until 2003, mostly fighting games and beat'em ups:

* **Super Street Fighter II Turbo**, the **Street Fighter Alpha** series, **Darkstalkers** (Vampire), **X-Men: Children of the Atom**, **Marvel vs. Capcom**;
* **Dungeons & Dragons: Tower of Doom** and **Shadow over Mystara**, **Alien vs. Predator**, **Armored Warriors**, **Battle Circuit**;
* the vertical shoot'em ups **19XX**, **1944**, **Giga Wing**, **Mars Matrix**, **Progear**.

CPS-2 cartridges are encrypted, and a battery keeps the decryption key. Current romsets contain decrypted copies or the keys: nothing to do on your side.

In RetroBat, these games can also be stored in the FinalBurn Neo system (see the [**FinalBurn Neo**](../final-burn-neo.md) page).

{% embed url="https://en.wikipedia.org/wiki/CP_System_II" %}

## At a glance

<table><thead><tr><th width="257.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\cps2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; FBNeo with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (fbneo recommended)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="179">Emulator</th><th width="174.25">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: fbneo</strong> (default)</td><td>Everyone</td><td>The current FinalBurn Neo in RetroArch: very compatible, layouts for 6-button games, dip switches, high scores, RetroAchievements, netplay.</td><td>—</td></tr><tr><td><strong>libretro: fbalpha2012_cps2</strong></td><td>Very low-end PCs, old romsets</td><td>FB Alpha 2012 core dedicated to the CPS-2, very light.</td><td>FB Alpha 0.2.97.28 romset. Does not read <code>.7z</code>.</td></tr><tr><td><strong>libretro: fbalpha</strong></td><td>Old romsets</td><td>FB Alpha 0.2.97.44.</td><td>Romset of its own version, no longer updated.</td></tr><tr><td><strong>libretro: fbalpha2012</strong></td><td>Old romsets</td><td>FB Alpha 0.2.97.29.</td><td>Romset of its own version.</td></tr><tr><td><strong>fbneo</strong> (standalone)</td><td>Cabinets, arcade sticks</td><td>The official FBNeo, buttons set game by game by RetroBat (see the <a href="../final-burn-neo.md"><strong>FinalBurn Neo</strong></a> page).</td><td>No RetroAchievements or netplay. Save states with hotkeys.</td></tr></tbody></table>

**If in doubt, keep libretro: fbneo.**

## BIOS

No BIOS is needed.

## Which game format should I use?

Games are `.zip` or `.7z` romsets, to keep compressed and under their original name (`ssf2t.zip`…). The romset must match the emulator version:

<table><thead><tr><th width="302.75">Emulator</th><th>Romset version</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (standalone)</td><td>Latest FBNeo version</td></tr><tr><td>libretro: fbalpha2012_cps2</td><td>FB Alpha 0.2.97.28 (<code>.zip</code> only)</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

The fbalpha2012\_cps2 core is not offered for a `.7z` game. For details about romsets (non-merged, split, merged), see the [**Arcade Guide**](../../../arcade-guide.md) page.

## Controls

RetroBat sets up the controllers automatically. **SELECT** inserts a coin, **START** starts the game, the left stick and the d-pad move the player.

### fbneo core

The **CONTROLS > CONTROLLER TYPE** option picks the layout. For 6-button fighting games (Street Fighter Alpha, Darkstalkers…):

<table><thead><tr><th width="199.5">RetroBat controller</th><th width="221.5">CLASSIC (default)</th><th>MODERN</th></tr></thead><tbody><tr><td>WEST</td><td>Light punch</td><td>Light punch</td></tr><tr><td>NORTH</td><td>Medium punch</td><td>Medium punch</td></tr><tr><td>L1</td><td>Heavy punch</td><td>—</td></tr><tr><td>R1</td><td>Heavy kick</td><td>Heavy punch</td></tr><tr><td>R2</td><td>—</td><td>Heavy kick</td></tr><tr><td>SOUTH</td><td>Light kick</td><td>Light kick</td></tr><tr><td>EAST</td><td>Medium kick</td><td>Medium kick</td></tr></tbody></table>

The other games use the face buttons in order: SOUTH = button 1, EAST = button 2, WEST = button 3, NORTH = button 4.

**6-BUTTON PANEL** suits an arcade stick with two rows of three buttons. The other choices are described on the [**FinalBurn Neo**](../final-burn-neo.md) page.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (626).png" alt=""><figcaption></figcaption></figure></div>

### fbalpha2012\_cps2 core

Buttons are placed as with the fbneo core in CLASSIC. **CONTROLS > CONTROL TYPE**: **gamepad** (default, the one of the table above) or **arcade** (layout for arcade sticks).

### FBNeo (standalone)

RetroBat sets the buttons game by game with the `fbneo.yml` mapping file: see the [**FinalBurn Neo**](../final-burn-neo.md) page.

### Hotkeys

The libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page). For standalone FBNeo, see the [**FinalBurn Neo**](../final-burn-neo.md) page.

## Folders

<table><thead><tr><th width="350.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\cps2</code></td></tr><tr><td>fbneo core: NVRAM, EEPROM, high scores</td><td><code>saves\cps2\fbneo</code></td></tr><tr><td>fbalpha2012_cps2, fbalpha, fbalpha2012 cores: game saves</td><td><code>saves\cps2</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\cps2\libretro.&#x3C;core></code></td></tr><tr><td>High score file (<code>hiscore.dat</code>)</td><td><p><code>bios\fbneo</code> (fbneo)</p><p><code>bios\fba</code> (fbalpha), copied to <code>bios\fbalpha2012</code> (fbalpha2012_cps2) and <code>saves\cps2</code> (fbalpha2012)</p></td></tr><tr><td>Standalone FBNeo</td><td>See the <a href="../final-burn-neo.md"><strong>FinalBurn Neo</strong></a> page</td></tr></tbody></table>

## Guides

### Service menu and dip switches

The cabinet service menu sets the difficulty, the number of lives, free play…

* fbneo core: **START + L1 + R1**, or another combination with **EMULATION > DIAGNOSTIC MENU INPUT**.
* **R3** opens the service menu (fbalpha2012\_cps2 core).

The board **dip switches** are set in the RetroArch menu (**HOTKEY + SOUTH**), **Core Options > Dip switches** (fbneo core). **EMULATION > ENABLE FREE PLAY** (fbneo core) sets free play directly when the game allows it.

### Vertical games

Vertical shoot'em ups (19XX, 1944, Giga Wing, Mars Matrix) are displayed the right way up, with a vertical decoration.

* fbneo core: **VIDEO > TATE MODE** rotates the picture for a screen standing vertically.
* fbalpha2012\_cps2 core: **VIDEO > AUTO ROTATE**, on by default, rotates the picture of vertical games. When off, the directions are rotated for a screen standing vertically.
* Standalone FBNeo: **VIDEO > VERTICAL MONITOR INDEX** shows vertical games on another screen.

### High scores

**EMULATION > ENABLE HISCORES**, on by default, keeps the high scores of compatible games. RetroBat provides the `hiscore.dat` file to each core (see [**Folders**](cp-system-ii.md#folders)).

### RetroAchievements

The fbneo core is the best supported by RetroAchievements for arcade. In hardcore mode, keep **EMULATION > CPU OVERCLOCK** at 100% or more. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

| Emulator                 | Option                        | Effect                                                            |
| ------------------------ | ----------------------------- | ----------------------------------------------------------------- |
| fbneo, fbalpha2012\_cps2 | **EMULATION > CPU OVERCLOCK** | Reduces the original slowdowns of some games. Can cause glitches. |
| fbneo                    | **VIDEO > FORCE 60HZ**        | Forces games to 60 Hz (original rate: about 59.6 Hz).             |
| fbalpha2012\_cps2        | **VIDEO > FRAMESKIP**         | Skips frames on a PC that is too slow.                            |
| fbneo                    | **AUDIO > LOWPASS FILTER**    | Softens the sound.                                                |
| fbalpha2012\_cps2        | **AUDIO > AUDIO FILTER**      | Softens the sound (from 0 to 95%).                                |

## Known issues

<table><thead><tr><th width="350.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start, or a file is missing</td><td>The romset does not match the emulator version (see <a href="cp-system-ii.md#which-game-format-should-i-use"><strong>Which game format should I use?</strong></a>).</td></tr><tr><td>The fbalpha2012_cps2 core is not offered</td><td>The game is a <code>.7z</code>: this core only reads <code>.zip</code>.</td></tr><tr><td>High scores are not kept</td><td>The game is not in <code>hiscore.dat</code>, or <strong>ENABLE HISCORES</strong> is off. They are not kept in netplay.</td></tr><tr><td>RetroAchievements switches to normal mode</td><td><strong>CPU OVERCLOCK</strong> is below 100%, or cheats are active.</td></tr></tbody></table>
