---
description: Cave
---

# Cave CV1000

<div align="left"><figure><img src="../../../.gitbook/assets/image (675).png" alt="" width="292"><figcaption></figcaption></figure></div>

## Overview

**CAVE** is a Japanese studio founded in 1994 by former Toaplan staff. It is the specialist of "manic" (or _danmaku_) shoot'em ups: screens covered with bullets, and a ship that only dies when its tiny central point is hit.

Its games were released on three generations of arcade boards:

* **68000-based CAVE boards** (1994-2001): **DonPachi**, **DoDonPachi**, **ESP Ra.De.**, **Guwange**, **Dangun Feveron**, **Uo Poko**, and also **Power Instinct 2** or **Pretty Soldier Sailor Moon** for other publishers;
* **IGS PGM** (2002-2003): **DoDonPachi Dai-Ou-Jou**, **Ketsui**, **Espgaluda**;
* **CV1000** (2004-2012): **Mushihimesama**, **Espgaluda II**, **Ibara**, **Muchi Muchi Pork!**, **Mushihimesama Futari**, **Deathsmiles**, **DoDonPachi DaiFukkatsu**, **Akai Katana**, **DoDonPachi SaiDaiOuJou**.

The `roms\cave` folder holds the games of these three generations. Not every emulator reads all of them).

{% embed url="https://en.wikipedia.org/wiki/Cave_(company)#Games_developed" %}

## At a glance

<table><thead><tr><th width="260.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\cave</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>pgm.zip</code> for PGM games)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators (buttons set game by game for the mame and mame2003_plus cores, standalone MAME and FBNeo)</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; MAME, FBNeo and Demul with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>fbneo, fbalpha, fbalpha2012 cores (fbneo recommended)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                      | Games read          | Strengths                                                                                                                      | Limits                                                                                                           |
| ----------------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| **libretro: fbneo** (default) | 68000, PGM, CV1000  | The current FinalBurn Neo in RetroArch: very compatible, light, dip switches, high scores, RetroAchievements, netplay, rewind. | —                                                                                                                |
| **libretro: fbalpha**         | 68000               | FB Alpha 0.2.97.44.                                                                                                            | Romset of its own version. No CV1000.                                                                            |
| **libretro: fbalpha2012**     | 68000               | FB Alpha 0.2.97.29, very light.                                                                                                | Romset of its own version. No CV1000.                                                                            |
| **libretro: mame2003\_plus**  | 68000               | Very light, buttons set game by game like lr-mame.                                                                             | MAME 0.78 romset. No CV1000.                                                                                     |
| **libretro: mame2016**        | 68000, PGM, CV1000  | MAME 0.174.                                                                                                                    | Romset of its own version. Slower than fbneo on CV1000 games. No buttons set game by game.                       |
| **libretro: mame**            | 68000, PGM, CV1000  | The current MAME, buttons set game by game.                                                                                    | More demanding.                                                                                                  |
| **fbneo** (standalone)        | 68000, PGM, CV1000  | The official FBNeo, buttons set game by game, a separate screen possible for vertical games.                                   | No RetroAchievements or netplay. Save states with hotkeys.                                                       |
| **mame64**                    | 68000, PGM, CV1000  | The official MAME, with all its settings. CV1000 slowdowns very close to the cabinet.                                          | More demanding. Save states with hotkeys.                                                                        |
| **demul**                     | CV1000 (list below) | Another CV1000 emulation.                                                                                                      | Only reads the CV1000 games of its list. Same button layout for every game. Save states not managed by RetroBat. |

**If in doubt, keep libretro: fbneo.** It reads every generation and runs well on a modest PC.

## BIOS

CAVE 68000 and CV1000 games need no BIOS.

IGS PGM games (**DoDonPachi Dai-Ou-Jou**, **Ketsui**, **Espgaluda**) need the board BIOS, `pgm.zip` (fbneo, mame, mame2016 cores, standalone FBNeo and MAME). Put it in `roms\cave`, next to the games.

RetroBat checks no BIOS for this system.

## Which game format should I use?

Games are `.zip` or `.7z` romsets, to keep compressed and under their original name (`ddonpach.zip`, `mushisam.zip`…). The romset must match the emulator version:

<table><thead><tr><th width="289">Emulator</th><th>Romset version</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (standalone)</td><td>Latest FBNeo version</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr><tr><td>libretro: mame2003_plus</td><td>MAME 0.78 (and mame2003_plus additions)</td></tr><tr><td>libretro: mame2016</td><td>MAME 0.174</td></tr><tr><td>libretro: mame, mame64</td><td>Latest MAME version</td></tr><tr><td>demul</td><td>CV1000 games of the list below</td></tr></tbody></table>

Clones need their parent game in the same folder. For details about romsets (non-merged, split, merged), see the [**Arcade Guide**](../../arcade-guide.md) page.

**CV1000 games read by Demul**:

| Romset                                                       | Game                                           |
| ------------------------------------------------------------ | ---------------------------------------------- |
| `akatana`                                                    | Akai Katana                                    |
| `deathsml`, `dsmbl`                                          | Deathsmiles, Deathsmiles MegaBlack Label       |
| `ddpdfk`, `ddpdfk10`, `dfkbl`                                | DoDonPachi DaiFukkatsu (1.5, 1.0, Black Label) |
| `ddpsdoj`                                                    | DoDonPachi SaiDaiOuJou                         |
| `espgal2`, `espgal2a`                                        | Espgaluda II                                   |
| `futari10`, `futari15`, `futari15a`, `futaribl`, `futariblj` | Mushihimesama Futari (1.0, 1.5, Black Label)   |
| `ibara`, `ibarao`, `ibarablk`, `ibarablka`                   | Ibara, Ibara Kuro Black Label                  |
| `mmmbanc`                                                    | Medal Mahjong Moukari Bancho                   |
| `mmpork`                                                     | Muchi Muchi Pork!                              |
| `mushisam`, `mushisama`, `mushisamb`                         | Mushihimesama                                  |
| `mushitam`, `mushitama`                                      | Puzzle! Mushihimetama                          |
| `pinkswts`, `pinkswtsa`, `pinkswtsb`, `pinkswtsx`            | Pink Sweets: Ibara Sorekara                    |

## Controls

RetroBat sets up the controllers automatically for every emulator. **SELECT** inserts a coin, **START** starts the game, the left stick and the d-pad move the ship.

In most games, **button 1** shoots (held, it gives a focused shot or a laser, depending on the game) and **button 2** drops a bomb. CAVE games use 2 to 4 buttons.

The button positions depend on the emulator:

| RetroBat controller | fbneo, fbalpha, fbalpha2012, mame2016 cores; Demul | mame, mame2003\_plus cores; standalone MAME and FBNeo |
| ------------------- | -------------------------------------------------- | ----------------------------------------------------- |
| SOUTH               | Button 1                                           | Button 2                                              |
| EAST                | Button 2                                           | Button 3                                              |
| WEST                | Button 3                                           | Button 1                                              |
| NORTH               | Button 4                                           | Button 4                                              |

* **mame core, mame2003\_plus, MAME**: buttons set game by game. A game without a dedicated setup uses the same default layout. For mame2003\_plus, keep the core controller type on automatic.
* **Standalone FBNeo**: buttons set game by game from the `fbneo.yml` file. A game missing from the file keeps the keys set in FBNeo.
* **Demul**: same layout for every game.

### Arcade sticks

On an arcade stick, set **CONTROLS > CONTROLLER LAYOUT** to match your panel (mame core, mame2003\_plus, standalone MAME and FBNeo). With the fbneo core, choose **CONTROLS > CONTROLLER TYPE > 6-BUTTON PANEL**. For more details, see the [**Arcade sticks**](../../../controllers/supported-controllers/arcade-sticks.md) page.

<div align="left"><figure><img src="../../../.gitbook/assets/image (676).png" alt=""><figcaption></figcaption></figure></div>

### Hotkeys

libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../navigation/hotkeys.md) page).

**MAME (mame64)**

| Hotkey             | Action       | Keyboard  |
| ------------------ | ------------ | --------- |
| **HOTKEY + START** | Quit         | ESC       |
| HOTKEY + SOUTH     | MAME menu    | TAB       |
| HOTKEY + WEST      | Save state   | F2        |
| HOTKEY + NORTH     | Load state   | F4        |
| HOTKEY + RIGHT     | Fast forward | SPACE     |
| HOTKEY + LEFT      | Rewind       | BACKSPACE |
| —                  | Pause        | P         |

**FBNeo (standalone)**

| Hotkey             | Action                     | Keyboard |
| ------------------ | -------------------------- | -------- |
| **HOTKEY + START** | Quit                       | —        |
| HOTKEY + WEST      | Save state                 | F2       |
| HOTKEY + NORTH     | Load state                 | F4       |
| HOTKEY + UP        | Next save slot             | F7       |
| HOTKEY + DOWN      | Previous save slot         | F6       |
| HOTKEY + RIGHT     | Fast forward (hold)        | L        |
| HOTKEY + SOUTH     | Pause                      | P        |
| HOTKEY + R3        | Screenshot                 | F8       |
| —                  | Show / hide the FBNeo menu | F1       |

**Demul**

| Hotkey             | Action           | Keyboard |
| ------------------ | ---------------- | -------- |
| **HOTKEY + START** | Quit             |          |
| **HOTKEY + WEST**  | Demul save state | F2       |
| **HOTKEY + NORTH** | Demul load state | F4       |

MAME, FBNeo and Demul save states stay in the emulator: they do not show up in the save state manager.

## Folders

<table><thead><tr><th width="367.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games, <code>pgm.zip</code> BIOS</td><td><code>roms\cave</code></td></tr><tr><td>fbneo core: NVRAM, EEPROM, high scores</td><td><code>saves\cave\fbneo</code></td></tr><tr><td>fbalpha, fbalpha2012 cores: game saves</td><td><code>saves\cave</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\cave\libretro.&#x3C;core></code></td></tr><tr><td>High score file (<code>hiscore.dat</code>)</td><td><code>bios\fbneo</code> (fbneo), <code>bios\fba</code> (fbalpha), copied to <code>saves\cave</code> (fbalpha2012)</td></tr><tr><td>Standalone FBNeo: NVRAM, EEPROM, high scores</td><td><code>saves\fbneo\fbneo</code></td></tr><tr><td>MAME: NVRAM, save states</td><td><p><code>saves\mame\nvram</code></p><p><code>saves\mame\states</code></p></td></tr><tr><td>Demul: NVRAM</td><td><code>saves\cave\demul</code></td></tr><tr><td>Demul: configuration</td><td><p><code>emulators\demul\Demul.ini</code></p><p><code>emulators\demul\padDemul.ini</code></p></td></tr><tr><td>Buttons set game by game</td><td><code>system\resources\inputmapping</code> (editable copy in <code>user\inputmapping</code>)</td></tr></tbody></table>

## Guides

### Vertical games

Most CAVE games are played on a vertical screen. They are displayed the right way up, with a vertical bezel.

* fbneo core: **VIDEO > TATE MODE** rotates the picture for a screen standing vertically.
* Standalone FBNeo: **VIDEO > VERTICAL MONITOR INDEX** shows vertical games on another screen.

### CV1000 games: speed and slowdowns

CV1000 games need more power than the others. On a modest PC, the sound stutters and the music slows down.

On the cabinet, games slow down when the screen fills with bullets: these slowdowns are part of the game.

* **fbneo core**: CV1000 games have dip switches specific to their emulation (**Speed Hacks**, **Thread Blitter**, **Blitter Timing**, **Blitter Delay**, CPU rate). They set the emulation speed and how the slowdowns are reproduced. Open the RetroArch menu (**HOTKEY + SOUTH**), then **Core Options > Dip switches**.
* **MAME (mame64)**: the MAME menu (**HOTKEY + SOUTH**) gives access to the blitter settings of CV1000 games.

### Service menu and dip switches

The cabinet service menu sets the difficulty, the number of lives, free play…

* **fbneo core**: **START + L1 + R1**, or another combination with **EMULATION > DIAGNOSTIC MENU INPUT**. Dip switches are set in **Core Options > Dip switches**. **EMULATION > ENABLE FREE PLAY** sets free play directly when the game allows it.
* **MAME (mame64)**: **R3** opens the test menu, **L3** is the Service button to move in it (keyboard: **0** and **9**).
* **Demul**: **R3** (Test) and **L3** (Service) on the player 1 controller; on the keyboard, **0** and **9** when no controller is set up.
* **Standalone FBNeo**: dip switches in the FBNeo menu (**F1**, then **Input > Set dipswitches**).

### High scores

**EMULATION > ENABLE HISCORES**, on by default, keeps the high scores of compatible games with the fbneo, fbalpha and fbalpha2012 cores. RetroBat provides the `hiscore.dat` file to each core (see [**Folders**](cave-cv1000.md#folders)).

### RetroAchievements

The fbneo core is the best supported by RetroAchievements for arcade games. In hardcore mode, keep **EMULATION > CPU OVERCLOCK** at 100% or more. For more details, see the [**RetroAchievements**](../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="93.25">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>fbneo</td><td><strong>EMULATION > CPU OVERCLOCK</strong></td><td>Reduces the original slowdowns. Changes the gameplay and may cause glitches.</td></tr><tr><td>fbneo</td><td><strong>VIDEO > FRAMESKIP</strong></td><td>Skips frames on a PC that is too slow.</td></tr><tr><td>fbneo</td><td><strong>AUDIO > LOWPASS FILTER</strong></td><td>Softens the sound.</td></tr><tr><td>demul</td><td><strong>INTERNAL RESOLUTION</strong></td><td>Raises the rendering resolution.</td></tr><tr><td>demul</td><td><strong>GAME ASPECT RATIO</strong></td><td>4:3, 16:9 or stretched.</td></tr><tr><td>demul</td><td><strong>EMULATION > CPU MODE</strong></td><td><strong>DYNAREC</strong> (default) for speed, <strong>INTERPRETER</strong> for compatibility.</td></tr></tbody></table>

## Known issues

| Issue                                                                    | Solution                                                                                                                                                                        |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| The game does not start, or a file is missing                            | The romset does not match the emulator version (see [**Which game format should I use?**](cave-cv1000.md#which-game-format-should-i-use)), or the parent of a clone is missing. |
| A CV1000 game does not start with fbalpha, fbalpha2012 or mame2003\_plus | These cores do not read CV1000 games: use the fbneo core.                                                                                                                       |
| A game does not start with Demul                                         | Demul only reads the CV1000 games of its list (see [**Which game format should I use?**](cave-cv1000.md#which-game-format-should-i-use)).                                       |
| Ketsui, Espgaluda or DoDonPachi Dai-Ou-Jou does not start                | Add `pgm.zip` to `roms\cave`.                                                                                                                                                   |
| A CV1000 game slows down, the sound stutters                             | The PC lacks power: use the fbneo core, adjust its CV1000 dip switches (see [**Guides**](cave-cv1000.md#service-menu-and-dip-switches)) or **FRAMESKIP**.                       |
| The buttons are not at the same place from one emulator to another       | See the table in [**Controls**](cave-cv1000.md#controls).                                                                                                                       |
| High scores are not kept                                                 | **ENABLE HISCORES** is off, or the game is not in `hiscore.dat`. They are not kept in netplay.                                                                                  |
