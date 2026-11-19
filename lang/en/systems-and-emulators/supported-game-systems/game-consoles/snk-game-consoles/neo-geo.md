---
description: SNK
---

# Neo Geo

<div align="left"><figure><img src="../../../../.gitbook/assets/image (636).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Neo Geo** is an SNK system released in 1990, in two versions that play the same games:

* the **MVS** (Multi Video System), an arcade board that can hold up to 6 games in a single cabinet;
* the **AES** (Advanced Entertainment System), the home console, sold as "the arcade at home".

SNK released about 150 games for it until 2004, mostly fighting and action games: The King of Fighters, Metal Slug, Samurai Shodown, Fatal Fury, Garou: Mark of the Wolves…

In RetroBat, Neo Geo games are arcade **romsets** (`mslug.zip` for Metal Slug), together with the `neogeo.zip` BIOS. The Geolith emulator uses another format, `.neo` (see [**Which game format should I use?**](neo-geo.md#which-game-format-should-i-use)).

Neo Geo CD games have their own system (see the [**Neo Geo CD**](neo-geo-cd.md) page).

{% embed url="https://en.wikipedia.org/wiki/Neo_Geo" %}

## At a glance

<table><thead><tr><th width="226.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\neogeo</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .neo .wad</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td><code>neogeo.zip</code> (and <code>aes.zip</code> for geolith)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; FBNeo, Raine and MAME with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (fbneo recommended)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="189">Emulator</th><th>For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: fbneo</strong> (default)</td><td>Everyone</td><td>FinalBurn Neo in RetroArch: very compatible, Universe BIOS by default, Neo Geo button layouts, per-game memory cards, RetroAchievements, netplay.</td><td>FBNeo romsets only.</td></tr><tr><td><strong>libretro: geolith</strong></td><td>Purists</td><td>Very accurate AES and MVS emulation, compatible with every commercial game. Supports the 4-player multitap, the V-Liner and the trackball of The Irritating Maze.</td><td>Only reads <code>.neo</code> files (to be converted, see <a href="neo-geo.md#which-game-format-should-i-use"><strong>Which game format should I use?</strong></a>).</td></tr><tr><td><strong>fbneo</strong> (standalone)</td><td>Cabinets, arcade sticks</td><td>The official FBNeo, buttons set game by game by RetroBat (see the <a href="../../arcade/final-burn-neo.md"><strong>FinalBurn Neo</strong></a> page).</td><td>No RetroAchievements or netplay. Save states with hotkeys.</td></tr><tr><td><strong>raine</strong></td><td>The curious</td><td>Historic Neo Geo and Neo Geo CD emulator, with its own menu.</td><td>No RetroAchievements or netplay.</td></tr><tr><td><strong>mame64</strong> (MAME)</td><td>MAME users</td><td>The official MAME, with your MAME romsets.</td><td>MAME romsets of the same version. Settings in the MAME menu.</td></tr><tr><td><strong>libretro: fbalpha, fbalpha2012_neogeo</strong></td><td>Very low-end PCs, old romsets</td><td>Old FB Alpha versions, lighter.</td><td>Need the romset of their own version, no longer updated.</td></tr></tbody></table>

**If in doubt, keep libretro: fbneo.**

## BIOS

<table><thead><tr><th width="140.75">File</th><th>Used by</th><th>Content</th></tr></thead><tbody><tr><td><code>neogeo.zip</code></td><td>All emulators</td><td>MVS BIOS (all regions), AES BIOS and Universe BIOS</td></tr><tr><td><code>aes.zip</code></td><td>geolith (AES system type, its default)</td><td>AES BIOS</td></tr><tr><td><code>irrmaze.zip</code></td><td>geolith</td><td>The Irritating Maze BIOS (trackball), in MVS</td></tr></tbody></table>

* Put these files in the `bios` folder. `neogeo.zip` can also go next to the games, in `roms\neogeo`, except for geolith which only reads `bios`.
* With **libretro: fbalpha2012\_neogeo**, `neogeo.zip` must be in `roms\neogeo`: this core does not read the `bios` folder.
* `neogeo.zip` must come from the same version as your games: FBNeo's for fbneo, MAME's for MAME. For geolith, `neogeo.zip`, `aes.zip` and `irrmaze.zip` must come from a recent MAME set.

The RetroBat BIOS check asks for `neogeo.zip` (in `bios` or `roms\neogeo`) and lists `aes.zip` and `irrmaze.zip` as optional.

**Which BIOS is used?**

<table><thead><tr><th width="202">Emulator</th><th>Option</th><th>RetroBat default</th></tr></thead><tbody><tr><td>libretro: fbneo</td><td><strong>EMULATION > BIOS</strong></td><td><strong>UNIVERSE BIOS</strong> (<strong>DIPSWITCH</strong> in RetroAchievements hardcore mode)</td></tr><tr><td>libretro: geolith</td><td><strong>EMULATION > SYSTEM TYPE</strong>: <strong>AES (HOME CONSOLE)</strong>, <strong>MVS (ARCADE)</strong> or <strong>UNIVERSE BIOS</strong></td><td>AES, USA region</td></tr><tr><td>libretro: fbalpha, fbalpha2012_neogeo</td><td><strong>EMULATION > NEOGEO MODE</strong></td><td><strong>UNIVERSE BIOS</strong></td></tr><tr><td>raine</td><td><strong>EMULATION > BIOS</strong></td><td><strong>UNIVERSE BIOS V3.2</strong></td></tr><tr><td>fbneo (standalone)</td><td>FBNeo menu (<strong>F1</strong>), <strong>Input > Set dipswitches</strong>, <strong>BIOS</strong> setting</td><td>FBNeo setting</td></tr><tr><td>mame64</td><td>MAME menu (<strong>TAB</strong>), <strong>BIOS Selection</strong></td><td>MAME default BIOS</td></tr></tbody></table>

## Which game format should I use?

**`.zip` / `.7z` romsets**: keep them compressed and under their original name (`kof98.zip`, `mslug3.zip`…).

<table><thead><tr><th width="300.25">Emulator</th><th>Romset version</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (standalone)</td><td>Latest FBNeo version</td></tr><tr><td>mame64</td><td>MAME version shipped with RetroBat</td></tr><tr><td>raine</td><td>Raine's own game list: a recent FBNeo or MAME romset usually works, not always</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012_neogeo</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

For details about romsets (non-merged, split, merged), see the [**Arcade Guide**](../../../arcade-guide.md) page.

**`.neo` files** (geolith only): this is the format of TerraOnion's NeoSD cartridge, one file per game. Geolith does not read MAME / FBNeo romsets: convert them with the **lithogen** tool (link below). A `.neo` can also be stored in a `.zip`; RetroBat then checks that the zip really contains a `.neo`.

{% embed url="https://github.com/carmiker/lithogen" %}

For a `.neo` file, only geolith is offered. The other way round, geolith is not offered for a `.7z`.

## Controls

RetroBat sets up the controllers automatically. On every emulator, **SELECT** inserts a coin and **START** starts the game. The left stick and the d-pad move the player.

The Neo Geo has 4 buttons, **A**, **B**, **C** and **D**, lined up from left to right on the original stick. The libretro cores add button combinations on the shoulder buttons, handy for special moves and the BIOS menus.

| RetroBat controller | fbneo (CLASSIC, default) | fbneo (MODERN) | geolith   | raine   |
| ------------------- | ------------------------ | -------------- | --------- | ------- |
| SOUTH               | A                        | B              | A         | A       |
| EAST                | B                        | D              | B         | B       |
| WEST                | C                        | A              | C         | C       |
| NORTH               | D                        | C              | D         | D       |
| L1                  | C + D                    | B + C + D      | C + D     | —       |
| R1                  | A + B                    | C + D          | A + B     | —       |
| L2                  | B + C + D                | A + B + C      | B + C     | —       |
| R2                  | A + B + C                | A + B          | A + B + C | —       |
| L3                  | —                        | —              | Test      | Service |
| R3                  | —                        | —              | Service   | Test    |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (637).png" alt=""><figcaption></figcaption></figure></div>

**fbneo core**: **CONTROLS > CONTROLLER TYPE** also offers layouts made for Neo Geo hardware: **4 BUTTONS - NEOGEO MINI**, **6 BUTTONS - NEOGEO VARIATION** and the three **8 BUTTONS - MVS**. The RetroBat **TATTOO** option can show a button diagram next to the game, for the CLASSIC, MODERN and 6-BUTTON PANEL layouts.

**geolith core**: **CONTROLS > 4-PLAYER MODE** turns on the NEO-FTC1B multitap for the few 4-player games. It only works with the **MVS (ARCADE)** system type and the **JAPAN** or **ASIA** region.

**Raine**: **CONTROLS > USE HAT AND STICK** also moves the player with the d-pad (on by default).

**FBNeo (standalone)** and **MAME**: see the [**FinalBurn Neo**](../../arcade/final-burn-neo.md) and [**MAME**](../../arcade/mame.md) pages.

### Hotkeys

The libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page). For standalone FBNeo, see the [**FinalBurn Neo**](../../arcade/final-burn-neo.md) page; for MAME, the [**MAME**](../../arcade/mame.md) page.

**Raine**

<table><thead><tr><th width="198.25">Hotkey</th><th width="206.5">Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td>ESC</td></tr><tr><td>HOTKEY + WEST</td><td>Save state</td><td>F2</td></tr><tr><td>HOTKEY + NORTH</td><td>Load state</td><td>F4</td></tr><tr><td>HOTKEY + UP / DOWN</td><td>Next save slot</td><td>F6</td></tr><tr><td>HOTKEY + R3</td><td>Screenshot</td><td>F8</td></tr><tr><td>HOTKEY + EAST</td><td>Raine menu</td><td>F1</td></tr><tr><td>HOTKEY + L3</td><td>Pause</td><td>P</td></tr><tr><td>HOTKEY + LEFT</td><td>Frame advance</td><td>K</td></tr><tr><td>—</td><td>Fullscreen / window</td><td>F</td></tr><tr><td>—</td><td>Reset the game</td><td>F9</td></tr></tbody></table>

The keys can be changed in the `kb_hotkeys.yml` file (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

| Content                                                      | Folder                                                                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| Games                                                        | `roms\neogeo`                                                                                          |
| BIOS                                                         | `bios` (or `roms\neogeo`, see [**BIOS**](neo-geo.md#bios))                                             |
| fbneo core: memory cards, NVRAM, high scores                 | `saves\neogeo\fbneo`                                                                                   |
| geolith core: memory cards and NVRAM (`.mcr`, `.nv`, `.srm`) | `saves\neogeo`                                                                                         |
| libretro cores: save states                                  | `saves\neogeo\libretro.<core>`                                                                         |
| Raine: save states and game saves                            | `emulators\raine\savegame`                                                                             |
| Raine: screenshots                                           | `screenshots\raine`                                                                                    |
| Raine: configuration                                         | `emulators\raine\config\raine32_sdl.cfg`                                                               |
| FBNeo, MAME                                                  | See the [**FinalBurn Neo**](../../arcade/final-burn-neo.md) and [**MAME**](../../arcade/mame.md) pages |

## Guides

### The Universe BIOS

The **Universe BIOS** (UniBIOS) is an improved BIOS made by fans. It can switch a game to its AES or MVS version, change the region (some games differ in Japan) and gives access to cheats. It is the RetroBat default BIOS with the fbneo, fbalpha and fbalpha2012\_neogeo cores, and with Raine.

* **BIOS settings**: hold **A + B + C** while the game boots.
* **In-game menu** (cheats, game settings): press **START + A + B + C** during the game.

With the libretro cores, **A + B + C** is on **R2** (on **L2** with the MODERN layout of the fbneo core): hold R2 at boot, or press START + R2 in game.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (638).png" alt="" width="563"><figcaption><p>UNIVERSE BIOS setting screen</p></figcaption></figure></div>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (639).png" alt="" width="491"><figcaption><p>In-Game MENU</p></figcaption></figure></div>

### AES or MVS?

Most games are the same on both versions. A few differences:

* in **MVS** (arcade), you must insert coins (**SELECT**), and the difficulty or the number of lives are set in the cabinet menu;
* in **AES** (console), there are no coins, and some games have different options or content;
* depending on the region, some games change (blood, texts, censorship).

With the Universe BIOS, the choice is made in its settings. With geolith, use **EMULATION > SYSTEM TYPE**. Some games, mostly bootlegs and hacks, need the MVS. **EMULATION > FREE PLAY** (geolith) removes the need to insert coins in MVS.

**USER INTERFACE > SHOW ROM MENU** (geolith) opens the MVS system settings menu at boot.

### Memory cards

The AES and the MVS save games on a memory card.

* The fbneo core creates one memory card per game, in `saves\neogeo\fbneo`.
* Geolith inserts a memory card by default and saves it in `saves\neogeo`.

### RetroAchievements

Neo Geo games are listed under the Arcade category of RetroAchievements. The fbneo core is the best supported. Geolith is recognized with its `.neo` files.

In hardcore mode, RetroArch refuses the Universe BIOS with the fbneo core. RetroBat sets the BIOS to **DIPSWITCH** by itself in hardcore: leave **EMULATION > BIOS** on its default setting. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

**geolith core**

| Option                                              | Effect                                                                                                                                  |
| --------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **EMULATION > REGION**                              | USA (default), Europe, Japan or Asia.                                                                                                   |
| **EMULATION > OVERCLOCK**                           | Speeds up the CPU to reduce the original slowdowns. Can cause glitches.                                                                 |
| **VIDEO > GAME ASPECT RATIO (CORE)**                | **1:1 (SQUARE PIXELS)** (default), **45:44 (ACCURATE NTSC)** or **4:3 (TRADITIONAL NTSC)**. Used when **GAME ASPECT RATIO** is on AUTO. |
| **VISUAL RENDERING > SPRITE PER LINE LIMIT (HACK)** | Reduces flickering sprites when there are too many on a line. Above 96, can cause glitches.                                             |

**fbneo core**: see the [**FinalBurn Neo**](../../arcade/final-burn-neo.md) page (overclocking, diagnostic menu, dip switches, high scores).

**Raine**

<table><thead><tr><th width="342.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > THROTTLE</strong></td><td>On by default. When off, the game runs as fast as possible.</td></tr><tr><td><strong>VIDEO > KEEP ASPECT RATIO</strong></td><td>Keeps the picture proportions (on by default).</td></tr><tr><td><strong>VIDEO > ROTATE SCREEN</strong></td><td>Rotates the picture by 90°, 180° or 270°.</td></tr><tr><td><strong>VISUAL RENDERING > SCALING FILTER</strong></td><td><strong>NEAREST NEIGHBOR</strong> (sharp pixels, default) or <strong>LINEAR</strong> (smoothed picture).</td></tr><tr><td><strong>USER INTERFACE > SHOW FPS</strong></td><td>Shows the frame rate.</td></tr></tbody></table>

## Known issues

| Issue                                                                   | Solution                                                                                                                                                                                                                         |
| ----------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| The game does not start, or a file is missing                           | The romset does not match the emulator version, or `neogeo.zip` is missing or comes from another version (see [**BIOS**](neo-geo.md#bios) and [**Which game format should I use?**](neo-geo.md#which-game-format-should-i-use)). |
| Geolith: message "Geolith core requires a .neo file in the zip archive" | The zip is a MAME / FBNeo romset: convert it to `.neo` with lithogen, or use the fbneo core.                                                                                                                                     |
| Geolith: the game does not start in AES                                 | `aes.zip` is missing from `bios`, or the game needs the MVS: set **EMULATION > SYSTEM TYPE** to **MVS (ARCADE)**.                                                                                                                |
| Black screen with sound                                                 | The selected BIOS is missing from `neogeo.zip`: use the `neogeo.zip` of the same version as the emulator, or choose another BIOS.                                                                                                |
| RetroAchievements switches to normal mode                               | The Universe BIOS is selected: set **EMULATION > BIOS** back to its default setting.                                                                                                                                             |
| libretro: fbalpha2012\_neogeo does not find the BIOS                    | Put `neogeo.zip` in `roms\neogeo`.                                                                                                                                                                                               |
| Geolith: 4-player mode does not work                                    | Set **SYSTEM TYPE** to **MVS (ARCADE)** and **REGION** to **JAPAN** or **ASIA**.                                                                                                                                                 |
