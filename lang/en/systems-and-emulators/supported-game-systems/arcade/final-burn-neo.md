# Final Burn Neo

<div align="left"><figure><img src="../../../.gitbook/assets/image (629).png" alt=""><figcaption></figcaption></figure></div>

## Overview

**FinalBurn Neo** (FBNeo) is an arcade emulator. Its history starts in 2000 with **Final Burn**, created by Dave for Capcom's CPS-1 and CPS-2 boards. The project became **FinalBurn Alpha** (FB Alpha), then the team took it over in 2019 under the name FinalBurn Neo.

FBNeo aims at playability rather than full documentation of the machines: it is light, fast and known for its fighting games and shoot'em ups. It emulates thousands of games, including:

* Capcom CPS-1, CPS-2 and CPS-3;
* SNK Neo Geo;
* Cave, IGS PGM, Toaplan;
* Konami, Sega System 16 / 18, Taito, Data East, Irem…

Each game is a file called a [**romset**](../../arcade-guide.md#understanding-romsets) (`sf2.zip` for Street Fighter II), whose content must match the emulator version (see [**Which game format should I use?**](final-burn-neo.md#which-game-format-should-i-use)).

In RetroBat, the FinalBurn Neo system holds all the games of the FBNeo romset. CPS-1, CPS-2, CPS-3, Neo Geo and Cave also have their own system.

{% embed url="https://github.com/finalburnneo/FBNeo" %}

## At a glance

<table><thead><tr><th width="236.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\fbneo</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>Depends on the game (see BIOS)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (libretro cores; FBNeo for the games of the mapping file)</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; FBNeo with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (fbneo recommended)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Lightguns</strong></td><td>fbneo core (up to 4)</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                                       | For whom?                     | Strengths                                                                                                                                              | Limits                                                                                                          |
| ---------------------------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------- |
| **libretro: fbneo** (default)                  | Everyone                      | The current FBNeo in RetroArch: shaders, decorations, save states, RetroAchievements, netplay, lightguns, dip switches in the core options.            | —                                                                                                               |
| **fbneo** (standalone)                         | Cabinets, arcade sticks       | The official FBNeo. Buttons set game by game by RetroBat (mapping file), with arcade stick layouts, and a separate screen possible for vertical games. | No RetroAchievements or netplay. Save states with hotkeys only.                                                 |
| **libretro: fbalpha**                          | Old romsets                   | FB Alpha 0.2.97.44.                                                                                                                                    | Needs the romset of its own version, no longer updated.                                                         |
| **libretro: fbalpha2012, fbalpha2012\_neogeo** | Very low-end PCs, old romsets | FB Alpha 0.2.97.29, lighter.                                                                                                                           | Needs the romset of its own version. The Neo Geo BIOS of fbalpha2012\_neogeo goes next to the games (see BIOS). |

**If in doubt, keep libretro: fbneo.**

## BIOS

Only some games need a BIOS: it is a romset shared between several games of the same hardware. It must come from the same FBNeo version as your games.

| File                                           | Hardware                               |
| ---------------------------------------------- | -------------------------------------- |
| `neogeo.zip`                                   | SNK Neo Geo                            |
| `pgm.zip`                                      | IGS PolyGame Master                    |
| `skns.zip`                                     | Kaneko Super Nova System               |
| `decocass.zip`                                 | Data East Cassette System              |
| `isgsm.zip`                                    | ISG Selection Master Type 2006         |
| `atarisy1.zip`                                 | Atari System 1                         |
| `bubsys.zip`                                   | Konami Bubble System                   |
| `cchip.zip`                                    | Taito C-Chip (internal ROM)            |
| `midssio.zip`                                  | Midway SSIO (sound board internal ROM) |
| `namcoc69.zip`, `namcoc70.zip`, `namcoc75.zip` | Namco C69 / C70 / C75                  |
| `nmk004.zip`                                   | NMK004 (internal ROM)                  |
| `ym2608.zip`                                   | Yamaha YM2608 (internal ROM)           |

Place these files in `bios`, `bios\fbneo` or next to the games, in `roms\fbneo`. The RetroBat BIOS check lists them all as optional, in `bios`.

With **libretro: fbalpha2012\_neogeo**, `neogeo.zip` must be next to the games, in `roms\fbneo`: this core does not read the `bios` folder.

**Neo Geo BIOS**: with the fbneo core, the **EMULATION > BIOS** option chooses the BIOS of the Neo Geo games. By default, RetroBat uses the **UNIVERSE BIOS**, except in RetroAchievements hardcore mode (see [**Guides**](final-burn-neo.md#retroachievements)). The Universe BIOS must be in `neogeo.zip`: this is the case with the FBNeo `neogeo.zip`.

## Which game format should I use?

Games are `.zip` or `.7z` romsets, to keep compressed and under their original name (`mslug.zip`, `sfiii3n.zip`…).

<table><thead><tr><th width="369">Emulator</th><th>Romset version</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (standalone)</td><td>Latest FBNeo version (<code>.dat</code> files of the FBNeo repository)</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012, fbalpha2012_neogeo</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

A romset from another version, or from a MAME version, may not start or may not work properly. For details on romset types (non-merged, split, merged) and samples, see the [**Arcade Guide**](../../arcade-guide.md) page.

## Controls

### fbneo core (libretro)

RetroBat configures the controllers automatically, up to 4 players. **SELECT** inserts a coin, **START** starts the game, the left stick and the D-pad move the player.

The **CONTROLS > CONTROLLER TYPE** option chooses the button layout:

| RetroBat controller | CLASSIC (default) | MODERN   |
| ------------------- | ----------------- | -------- |
| SOUTH               | Button 1          | Button 1 |
| EAST                | Button 2          | Button 2 |
| WEST                | Button 3          | Button 3 |
| NORTH               | Button 4          | Button 4 |
| R1                  | Button 5          | Button 6 |
| L1                  | Button 6          | —        |
| R2                  | —                 | Button 5 |

6-button fighting games (Street Fighter…):

| RetroBat controller | CLASSIC (default) | MODERN       |
| ------------------- | ----------------- | ------------ |
| WEST                | Light punch       | Light punch  |
| NORTH               | Medium punch      | Medium punch |
| L1                  | Heavy punch       | —            |
| R1                  | Heavy kick        | Heavy punch  |
| R2                  | —                 | Heavy kick   |
| SOUTH               | Light kick        | Light kick   |
| EAST                | Medium kick       | Medium kick  |

Neo Geo games:

| RetroBat controller | CLASSIC (default) | MODERN |
| ------------------- | ----------------- | ------ |
| SOUTH               | A                 | B      |
| EAST                | B                 | D      |
| WEST                | C                 | A      |
| NORTH               | D                 | C      |

The other **CONTROLLER TYPE** choices adapt the controller to some hardware:

* **4 BUTTONS - NEOGEO MINI**, **6 BUTTONS - NEOGEO VARIATION** and the three **8 BUTTONS - MVS**: Neo Geo pads and sticks;
* **6-BUTTON PANEL**: 6-button arcade panel;
* **MOUSE**, **POINTER**, **TOUCHSCREEN**: trackball or pointer games;
* **LIGHTGUN**, **ANALOG ARCADE GUN**: lightguns (see [**Guides**](final-burn-neo.md#lightguns)).

**CONTROLS > ANALOG SPEED** slows down the analog controls (steering wheels, trackballs) of games that react too fast.

<div align="left"><figure><img src="../../../.gitbook/assets/image (632).png" alt=""><figcaption></figcaption></figure></div>

### FBNeo (standalone)

RetroBat configures the controllers game by game, from the `fbneo.yml` mapping file (about 3,000 games). The file is in `system\resources\inputmapping`. To change it, copy it to `user\inputmapping`: that copy is the one used.

A clone without its own entry uses the entry of its parent game. A game missing from the file is not configured by RetroBat: it keeps the keys set in FBNeo (**F5**, or **Input > Map game inputs** menu).

The **CONTROLS > CONTROLLER LAYOUT** option chooses the layout. It is useful mostly with an arcade stick:

* **CONTROLLER(SNES)** (default);
* **MODERN 8 BUTTONS**;
* **CLASSIC 8 BUTTONS**;
* **8 BUTTONS ALTERNATIVE**;
* **6 BUTTONS**.

With the default layout, a 6-button fighting game plays like the core in CLASSIC: WEST / NORTH / L1 for punches, SOUTH / EAST / R1 for kicks. The cabinet Service button is on **R3**.

With XInput controllers (Xbox and compatible pads), FBNeo uses XInput. As soon as one controller is not XInput, it uses DirectInput for all controllers. **DRIVERS > INPUT** forces DirectInput. In DirectInput, if the controllers do not control the right players, turn on **CONTROLS > USE ALTERNATE INDEX**.

Without a controller, FBNeo keeps its default keyboard setup.

### Hotkeys

The libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../navigation/hotkeys.md) page).

**FBNeo (standalone)**

| Hotkey             | Action                                                             | Keyboard  |
| ------------------ | ------------------------------------------------------------------ | --------- |
| **HOTKEY + START** | Exit                                                               | —         |
| HOTKEY + WEST      | Save state                                                         | F2        |
| HOTKEY + NORTH     | Load state                                                         | F4        |
| HOTKEY + UP        | Next save slot                                                     | F7        |
| HOTKEY + DOWN      | Previous save slot                                                 | F6        |
| HOTKEY + RIGHT     | Fast forward (hold)                                                | L         |
| HOTKEY + LEFT      | Rewind (to turn on in the FBNeo menu: **Input > Rewind Settings**) | BACKSPACE |
| HOTKEY + EAST      | Pause                                                              | P         |
| HOTKEY + R3        | Screenshot                                                         | F8        |
| —                  | Show / hide the FBNeo menu                                         | F1        |
| —                  | Fullscreen / window                                                | F         |
| —                  | Fast forward (toggle)                                              | SPACE     |
| —                  | Leave fullscreen                                                   | ESCAPE    |

The keys can be changed in the `kb_hotkeys.yml` file (see the [**Hotkeys**](../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="326.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\fbneo</code></td></tr><tr><td>BIOS</td><td><code>bios</code>, <code>bios\fbneo</code> or <code>roms\fbneo</code></td></tr><tr><td>Samples (fbneo core, FBNeo)</td><td><code>bios\fbneo\samples</code></td></tr><tr><td>High score file (<code>hiscore.dat</code>)</td><td><code>bios\fbneo</code> (copied to <code>saves\fbneo\fbneo</code> for standalone FBNeo)</td></tr><tr><td>Cheats (fbneo core, FBNeo)</td><td><code>bios\fbneo\cheats</code></td></tr><tr><td>NVRAM, EEPROM, high scores, Neo Geo memory cards</td><td><code>saves\fbneo\fbneo</code></td></tr><tr><td>fbneo core: save states</td><td><code>saves\fbneo\libretro.fbneo</code></td></tr><tr><td>fbneo core: IPS patches</td><td><code>bios\fbneo\ips\&#x3C;game></code></td></tr><tr><td>FBNeo: save states</td><td><code>emulators\fbneo\savestates</code></td></tr><tr><td>FBNeo: IPS patches</td><td><code>emulators\fbneo\support\ips\&#x3C;game></code></td></tr><tr><td>FBNeo: configuration</td><td><code>emulators\fbneo\config\fbneo64.ini</code>, per-game keys in <code>emulators\fbneo\config\games</code></td></tr><tr><td>Per-game mapping (FBNeo)</td><td><code>system\resources\inputmapping\fbneo.yml</code> (editable copy in <code>user\inputmapping</code>)</td></tr><tr><td>Samples (fbalpha2012)</td><td><code>bios\fba\samples</code></td></tr></tbody></table>

## Guides

### Diagnostic menu and dip switches

Many cabinets have a test menu, often called the service menu. It sets the difficulty, the number of lives, free play…

With the fbneo core, **START + L1 + R1** opens this menu in game. **EMULATION > DIAGNOSTIC MENU INPUT** chooses another combination (or **NONE**). Not every cabinet has this menu.

<div align="left"><figure><img src="../../../.gitbook/assets/image (631).png" alt=""><figcaption></figcaption></figure></div>

**Dip switches** are the switches on the cabinet board. With the fbneo core:

1. Open the RetroArch menu (**HOTKEY + SOUTH**).
2. Go to **Core Options > Dip switches**.
3. Change the game settings.

Each game has its own dip switches. **EMULATION > ENABLE FREE PLAY** sets the free play one directly when the game has it.

<div align="left"><figure><img src="../../../.gitbook/assets/image (630).png" alt=""><figcaption></figcaption></figure></div>

With standalone FBNeo, dip switches are set in the FBNeo menu: **F1** to show it, then **Input > Set dipswitches** (or **Ctrl + F5**).

### High scores

**EMULATION > ENABLE HISCORES**, on by default, keeps the game high scores between sessions, like cabinets with a save. The `hiscore.dat` file is provided by RetroBat in `bios\fbneo`.

Scores are stored in `saves\fbneo\fbneo`, the same folder for the fbneo core and standalone FBNeo. They are not kept in netplay.

### RetroAchievements

FBNeo is the core best supported by RetroAchievements for arcade. In hardcore mode, RetroArch refuses:

* the Universe BIOS of Neo Geo games;
* patched romsets;
* a reduced processor speed;
* cheats.

RetroBat sets the BIOS and patched romsets by itself in hardcore. Keep **EMULATION > BIOS** on its default setting and **EMULATION > CPU OVERCLOCK** at 100% or more.

For more details, see the [**RetroAchievements**](../../../advanced-features/retroachievements.md) page.

### Vertical games

Vertical shoot'em ups (Cave, Toaplan…) are displayed rotated the right way, with a vertical decoration by default.

* With the fbneo core, **VIDEO > TATE MODE** rotates the picture for a screen turned vertically.
* With standalone FBNeo, **VIDEO > VERTICAL MONITOR INDEX** shows vertical games on another screen.

### Lightguns

The fbneo core supports up to 4 lightguns in the games that use them (Operation Wolf, Lethal Enforcers…). For lightgun setup, see the [**Lightguns**](../../../controllers/supported-controllers/lightguns/) page.

### IPS patches

IPS patches change a game: translation, fix, hack version. They are `.dat` files stored in a folder named after the game.

* **fbneo core**: place the patches in `bios\fbneo\ips\<game>`, then choose them in the RetroArch core options (RetroArch menu, **Core Options**). They are turned off in RetroAchievements hardcore mode.
* **FBNeo (standalone)**: place the patches in `emulators\fbneo\support\ips\<game>`, then turn on **EMULATION > ENABLE IPS PATCH**. Without any other setting, the patches ticked in FBNeo are applied. **EMULATION > IPS PATCH FILE** chooses a single patch, which must be in that folder.

### Other useful options

**fbneo core**

<table><thead><tr><th width="301.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > CPU OVERCLOCK</strong></td><td>Speeds up the emulated processor, to reduce the original slowdowns of some games. Under 100%, RetroAchievements hardcore mode is refused.</td></tr><tr><td><strong>VIDEO > FRAMESKIP</strong></td><td>Skips frames on a PC that is too slow.</td></tr><tr><td><strong>VIDEO > FORCE 60HZ</strong></td><td>Forces games to 60 Hz (the original rate is sometimes different, e.g. 59.18 Hz on Neo Geo).</td></tr><tr><td><strong>VIDEO > VECTOR RESOLUTION</strong></td><td>Rendering resolution of vector games (Asteroids…).</td></tr><tr><td><strong>AUDIO > SAMPLE RATE</strong></td><td>44,100 Hz (RetroBat default) or 48,000 Hz.</td></tr><tr><td><strong>AUDIO > LOWPASS FILTER</strong></td><td>Softens the sound.</td></tr></tbody></table>

**FBNeo (standalone)**

<table><thead><tr><th width="327.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>DRIVERS > VIDEO</strong></td><td><strong>DIRECTX9</strong> (default), <strong>DIRECTX9 (ALT)</strong>, <strong>DIRECT3D 11</strong>… Decorations through ReShade only work with DirectX 9 and Direct3D 11.</td></tr><tr><td><strong>VISUAL RENDERING > SCANLINES</strong></td><td>Scanlines, from <strong>LIGHT</strong> to <strong>VERY INTENSE</strong>.</td></tr><tr><td><strong>LATENCY REDUCTION > ENABLE RUN-AHEAD</strong></td><td>Reduces the delay between a button press and its reaction on screen.</td></tr><tr><td><strong>VIDEO > FORCE 60HZ</strong></td><td>Forces games to 60 Hz.</td></tr><tr><td><strong>INTEGER SCALING</strong></td><td>Enlarges the picture by a whole number of times, for sharp pixels.</td></tr><tr><td><strong>DRIVERS > AUDIO</strong></td><td><strong>DIRECT SOUND</strong> (default), <strong>XAUDIO 2</strong> or <strong>WASAPI</strong>.</td></tr></tbody></table>

## Known issues

| Issue                                                              | Solution                                                                                                                                                                                                   |
| ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| The game does not start, or a file is missing                      | The romset does not match the emulator version, or a BIOS is missing (see [**BIOS**](final-burn-neo.md#bios) and [**Which game format should I use?**](final-burn-neo.md#which-game-format-should-i-use)). |
| Black screen with sound on a Neo Geo game                          | The chosen BIOS is missing from `neogeo.zip`: use the `neogeo.zip` of the same FBNeo version, or set **EMULATION > BIOS** to **UNIVERSE BIOS**.                                                            |
| A Konami game (or another) fails its boot test                     | The saved NVRAM / EEPROM is damaged: delete the game files in `saves\fbneo\fbneo`.                                                                                                                         |
| RetroAchievements switches to softcore on a Neo Geo game           | The BIOS is set to **UNIVERSE BIOS**: put **EMULATION > BIOS** back to its default setting.                                                                                                                |
| Odd transparency effects                                           | `.bld` files in the blend folder (`bios\fbneo\blend` for the core): remove them.                                                                                                                           |
| Standalone FBNeo: the buttons of a game are not configured         | The game is not in `fbneo.yml`: set the keys in FBNeo (**F5**), or add the game to a copy of the file placed in `user\inputmapping`.                                                                       |
| Standalone FBNeo: the controllers do not control the right players | Turn on **CONTROLS > USE ALTERNATE INDEX**, or unplug the unused controllers.                                                                                                                              |
| A `.bin` or `.chd` file does not start                             | FBNeo only reads `.zip` / `.7z` romsets in this system. Neo Geo CDs go to the Neo Geo CD system.                                                                                                           |
