---
description: Capcom
---

# CPS III

<div align="left"><figure><img src="../../../../.gitbook/assets/image (627).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **CP System III** (**CPS-3**) is Capcom's last arcade board, released in 1996. Games were shipped on CD-ROM, with a security cartridge. Only six games use it, all in 2D:

* **Street Fighter III**: New Generation, 2nd Impact and 3rd Strike;
* **JoJo's Venture** and **JoJo's Bizarre Adventure: Heritage for the Future**;
* **Red Earth** (Warzard in Japan).

Current romsets contain the whole game (BIOS included) in a single `.zip` file: there is no CD or `.chd` file to provide.

In RetroBat, these games can also be stored in the FinalBurn Neo system (see the [**FinalBurn Neo**](../final-burn-neo.md) page).

{% embed url="https://en.wikipedia.org/wiki/CP_System_III" %}

## At a glance

<table><thead><tr><th width="230.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\cps3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; FBNeo with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (fbneo recommended)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="174.5">Emulator</th><th width="165.25">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: fbneo</strong> (default)</td><td>Everyone</td><td>The current FinalBurn Neo in RetroArch: very compatible, layouts for 6-button games, dip switches, high scores, RetroAchievements, netplay.</td><td>—</td></tr><tr><td><strong>libretro: fbalpha2012_cps3</strong></td><td>Very low-end PCs, old romsets</td><td>FB Alpha 2012 core dedicated to the CPS-3, very light.</td><td>FB Alpha 0.2.97.29 romset. Does not read <code>.7z</code>.</td></tr><tr><td><strong>libretro: fbalpha</strong></td><td>Old romsets</td><td>FB Alpha 0.2.97.44.</td><td>Romset of its own version, no longer updated.</td></tr><tr><td><strong>libretro: fbalpha2012</strong></td><td>Old romsets</td><td>FB Alpha 0.2.97.29.</td><td>Romset of its own version.</td></tr><tr><td><strong>fbneo</strong> (standalone)</td><td>Cabinets, arcade sticks</td><td>The official FBNeo, buttons set game by game by RetroBat (see the <a href="../final-burn-neo.md"><strong>FinalBurn Neo</strong></a> page).</td><td>No RetroAchievements or netplay. Save states with hotkeys.</td></tr></tbody></table>

**If in doubt, keep libretro: fbneo.**

## BIOS

No BIOS is needed. The CPS-3 board BIOS is included in the romset of each game.

## Which game format should I use?

Games are `.zip` or `.7z` romsets, to keep compressed and under their original name (`sfiii3.zip`…). The romset must match the emulator version:

<table><thead><tr><th width="302.75">Emulator</th><th>Romset version</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (standalone)</td><td>Latest FBNeo version</td></tr><tr><td>libretro: fbalpha2012_cps3</td><td>FB Alpha 0.2.97.29 (<code>.zip</code> only)</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

The fbalpha2012\_cps3 core is not offered for a `.7z` game. For details about romsets (non-merged, split, merged), see the [**Arcade Guide**](../../../arcade-guide.md) page.

The `.decomp` extension is for PC ports, see the [**Recompilations**](../../others/recomp.md) page.

## Controls

RetroBat sets up the controllers automatically. **SELECT** inserts a coin, **START** starts the game, the left stick and the d-pad move the player.

### fbneo core

The **CONTROLS > CONTROLLER TYPE** option picks the layout. For 6-button fighting games (Street Fighter III, JoJo, Red Earth):

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

<div align="left"><figure><img src="../../../../.gitbook/assets/image (628).png" alt=""><figcaption></figcaption></figure></div>

### fbalpha2012\_cps3 core

Buttons are placed as with the fbneo core in CLASSIC. **CONTROLS > PLAYER 1 / 2 CONTROLS**: **gamepad** (default, the one of the table above) or **arcade** (layout for arcade sticks).

* **PLAYER 1 / 2 LATERAL BUTTONS**: **L1/R1** (default) or **R1/R2** for the strong punch and kick.

### FBNeo (standalone)

RetroBat sets the buttons game by game with the `fbneo.yml` mapping file: see the [**FinalBurn Neo**](../final-burn-neo.md) page.

### Hotkeys

The libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page). For standalone FBNeo, see the [**FinalBurn Neo**](../final-burn-neo.md) page.

## Folders

| Content                                                   | Folder                                                                                                                                          |
| --------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Games                                                     | `roms\cps3`                                                                                                                                     |
| fbneo core: NVRAM, EEPROM, high scores                    | `saves\cps3\fbneo`                                                                                                                              |
| fbalpha2012\_cps3, fbalpha, fbalpha2012 cores: game saves | `saves\cps3`                                                                                                                                    |
| libretro cores: save states                               | `saves\cps3\libretro.<core>`                                                                                                                    |
| High score file (`hiscore.dat`)                           | <p><code>bios\fbneo</code> (fbneo)</p><p><code>bios\fba</code> (fbalpha), copied to <code>saves\cps3</code> (fbalpha2012_cps3, fbalpha2012)</p> |
| Standalone FBNeo                                          | See the [**FinalBurn Neo**](../final-burn-neo.md) page                                                                                          |

## Guides

### Service menu and dip switches

The cabinet service menu sets the difficulty, the number of lives, free play…

* fbneo core: **START + L1 + R1**, or another combination with **EMULATION > DIAGNOSTIC MENU INPUT**.
* With the fbalpha2012\_cps3 core, choose a combination in **EMULATION > DIAGNOSTIC MENU INPUT** (none by default).

The board **dip switches** are set in the RetroArch menu (**HOTKEY + SOUTH**), **Core Options > Dip switches** (fbneo core). The region of CPS-3 games (Japan, Asia, Europe, USA…) is changed the same way: some games change their name or content with the region.

### High scores

**EMULATION > ENABLE HISCORES**, on by default, keeps the high scores of compatible games. RetroBat provides the `hiscore.dat` file to each core (see [**Folders**](cp-system-iii.md#folders)).

### RetroAchievements

The fbneo core is the best supported by RetroAchievements for arcade. In hardcore mode, keep **EMULATION > CPU OVERCLOCK** at 100% or more. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="227">Emulator</th><th width="233.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td>fbneo, fbalpha2012_cps3</td><td><strong>EMULATION > CPU OVERCLOCK</strong></td><td>Reduces the original slowdowns of some games. Can cause glitches.</td></tr><tr><td>fbneo</td><td><strong>VIDEO > FORCE 60HZ</strong></td><td>Forces games to 60 Hz (original rate: about 59.6 Hz).</td></tr><tr><td>fbalpha2012_cps3</td><td><strong>VIDEO > FRAMESKIP</strong></td><td>Skips frames on a PC that is too slow.</td></tr><tr><td>fbneo</td><td><strong>AUDIO > LOWPASS FILTER</strong></td><td>Softens the sound.</td></tr><tr><td>fbalpha2012_cps3</td><td><strong>AUDIO > SAMPLE RATE</strong></td><td>44,100 Hz by default.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="344">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start, or a file is missing</td><td>The romset does not match the emulator version (see <a href="cp-system-iii.md#which-game-format-should-i-use"><strong>Which game format should I use?</strong></a>).</td></tr><tr><td>The fbalpha2012_cps3 core is not offered</td><td>The game is a <code>.7z</code>: this core only reads <code>.zip</code>.</td></tr><tr><td>High scores are not kept</td><td>The game is not in <code>hiscore.dat</code>, or <strong>ENABLE HISCORES</strong> is off. They are not kept in netplay.</td></tr><tr><td>RetroAchievements switches to normal mode</td><td><strong>CPU OVERCLOCK</strong> is below 100%, or cheats are active.</td></tr></tbody></table>
