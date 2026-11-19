---
description: SNK
---

# Neo Geo CD

<div align="left"><figure><img src="../../../../.gitbook/assets/image (640).png" alt="" width="540"><figcaption></figcaption></figure></div>

## Overview

The **Neo Geo CD** is the CD version of SNK's Neo Geo console, released in 1994. Its games, on CD-ROM, cost much less than AES cartridges, but the single-speed drive meant long loading times.

Three models were released:

* the **Front Loader** (1994), with a tray;
* the **Top Loader** (1995), with a lid;
* the **CDZ** (1996, Japan), with a faster drive.

The library has about a hundred games, mostly ports of Neo Geo games (The King of Fighters, Samurai Shodown, Metal Slug…), often with re-recorded CD music, plus a few exclusives.

Neo Geo cartridge games have their own system (see the [**Neo Geo**](neo-geo.md) page).

{% embed url="https://en.wikipedia.org/wiki/Neo_Geo_CD" %}

## At a glance

<table><thead><tr><th width="202.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\neogeocd</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .chd .iso .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: neocd</td></tr><tr><td><strong>BIOS</strong></td><td>Neo Geo CD BIOS (see BIOS)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; Raine with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (neocd recommended)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="155">Emulator</th><th width="141.5">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: neocd</strong> (default)</td><td>Everyone</td><td>Emulator dedicated to the Neo Geo CD. Finds the BIOS of the <code>bios\neocd</code> folder by itself, skips loading screens by default. RetroAchievements, netplay.</td><td><code>.cue</code> and <code>.chd</code> images only.</td></tr><tr><td><strong>libretro: geolith</strong></td><td>Purists</td><td>Very accurate emulation, compatible with every commercial game.</td><td><code>.cue</code> and <code>.chd</code> images only. MAME BIOS (<code>neocdz.zip</code>, plus <code>neocd.zip</code> for the Front / Top Loader).</td></tr><tr><td><strong>libretro: fbneo</strong></td><td>FBNeo users</td><td>Same core and settings as the Neo Geo games (button layouts).</td><td>CDZ model only. <code>.cue</code>, <code>.ccd</code> and <code>.chd</code> images only.</td></tr><tr><td><strong>raine</strong></td><td><code>.iso</code> or compressed images</td><td>Reads <code>.iso</code>, <code>.zip</code> and <code>.7z</code> images. Adjustable music and sound effects volumes.</td><td>Does not read <code>.chd</code>. No RetroAchievements or netplay.</td></tr></tbody></table>

**If in doubt, keep libretro: neocd.**

## BIOS

**neocd core**: put at least one of these BIOS files in `bios\neocd`. The core identifies the files by their content, so their name does not matter. It also looks for them in subfolders and in `.zip` files.

<table><thead><tr><th width="152">File</th><th width="193">Model</th><th>SHA-1</th></tr></thead><tbody><tr><td><code>neocd_z.rom</code></td><td>CDZ (RetroBat default choice)</td><td>b0f1c4fa8d4492a04431805f6537138b842b549f</td></tr><tr><td><code>neocd_sz.rom</code></td><td>CDZ (SMKDAN patch)</td><td>6a947457031dd3a702a296862446d7485aa89dbb</td></tr><tr><td><code>neocd_f.rom</code></td><td>Front Loader</td><td>a5f4a7a627b3083c979f6ebe1fabc5d2df6d083b</td></tr><tr><td><code>neocd_sf.rom</code></td><td>Front Loader (SMKDAN patch)</td><td>4a94719ee5d0e3f2b981498f70efc1b8f1cef325</td></tr><tr><td><code>neocd_t.rom</code></td><td>Top Loader</td><td>cc92b54a18a8bff6e595aabe8e5c360ba9e62eb5</td></tr><tr><td><code>neocd_st.rom</code></td><td>Top Loader (SMKDAN patch)</td><td>19729b51bdab60c42aafef6e20ea9234c7eb8410</td></tr><tr><td><code>neocd.bin</code></td><td>CDZ (MAME)</td><td>7bb26d1e5d1e930515219cb18bcde5b7b23e2eda</td></tr><tr><td><code>front-sp1.bin</code></td><td>Front Loader (MAME)</td><td>53bc1f283cdf00fa2efbb79f2e36d4c8038d743a</td></tr><tr><td><code>top-sp1.bin</code></td><td>Top Loader (MAME)</td><td>235f4d1d74364415910f73c10ae5482d90b4274f</td></tr><tr><td><code>uni-bioscd.rom</code></td><td>CDZ, Universe BIOS 3.3</td><td>5142f205912869b673a71480c5828b1eaed782a8</td></tr></tbody></table>

Without any BIOS, the neocd core starts with a built-in replacement BIOS. It is still incomplete: an original BIOS is recommended.

**Other emulators**: they use the MAME sets, to put in `bios`.

<table><thead><tr><th width="187.75">Emulator</th><th>Files</th></tr></thead><tbody><tr><td>libretro: geolith</td><td><code>neocdz.zip</code> (CDZ). For the Front Loader or the Top Loader: <code>neocd.zip</code> <strong>and</strong> <code>neocdz.zip</code>.</td></tr><tr><td>libretro: fbneo</td><td><code>neocdz.zip</code> and <code>neogeo.zip</code> (in <code>bios</code> or <code>bios\fbneo</code>)</td></tr><tr><td>raine</td><td><code>neocdz.zip</code></td></tr></tbody></table>

The RetroBat BIOS check asks for at least one BIOS in `bios\neocd`, and lists `neocdz.zip`, `neocd.zip` and `neogeo.zip` as optional.

**Which model is emulated?**

<table><thead><tr><th width="147">Emulator</th><th>Option</th><th>RetroBat default</th></tr></thead><tbody><tr><td>libretro: neocd</td><td><strong>EMULATION > BIOS</strong>: <strong>CDZ</strong>, <strong>CDZ (MAME)</strong>, <strong>FRONT LOADER</strong>, <strong>TOP LOADER</strong>, <strong>FRONT LOADER (MAME)</strong>, <strong>TOP LOADER (MAME)</strong>, <strong>UNIVERSE</strong></td><td><strong>CDZ</strong> (<code>neocd_z.rom</code>). If missing, the first BIOS found.</td></tr><tr><td>libretro: geolith</td><td><strong>EMULATION > BIOS</strong>: <strong>CDZ</strong>, <strong>FRONT LOADER</strong>, <strong>TOP LOADER</strong>, <strong>CDZ (UNIVERSE BIOS)</strong></td><td><strong>CDZ</strong></td></tr><tr><td>libretro: fbneo</td><td>—</td><td>CDZ</td></tr><tr><td>raine</td><td>—</td><td>CDZ (<code>neocdz.zip</code>)</td></tr></tbody></table>

The **CDZ** model loads faster. The Front Loader and the Top Loader are mostly useful for games that run badly on the CDZ.

## Which game format should I use?

<table><thead><tr><th>Format</th><th width="101">neocd</th><th width="115.25">geolith</th><th width="103.75">fbneo</th><th width="121.5">raine</th></tr></thead><tbody><tr><td><code>.cue</code> + <code>.bin</code></td><td>yes</td><td>yes</td><td>yes</td><td>yes</td></tr><tr><td><code>.chd</code></td><td>yes</td><td>yes</td><td>yes</td><td>no</td></tr><tr><td><code>.iso</code></td><td>no</td><td>no</td><td>no</td><td>yes</td></tr><tr><td><code>.zip</code> / <code>.7z</code> (compressed image)</td><td>no</td><td>no</td><td>no</td><td>yes</td></tr></tbody></table>

* **`.chd` is recommended**: a single compressed file, with the audio tracks.
* For a `.cue` game, keep the `.cue` and its files (`.bin`, or `.iso` with `.wav`, `.flac`, `.ogg`, `.mp3` audio tracks) in the same folder. The neocd core reads both kinds of `.cue`.
* Only the emulators that can read the game format are offered.

To convert a `.cue` image to `.chd`, use the `chdman.exe` tool shipped with MAME (`emulators\mame` folder): `chdman createcd -i game.cue -o game.chd`.

## Controls

RetroBat sets up the controllers automatically. **START** and **SELECT** match those of the Neo Geo CD controller. The left stick and the d-pad move the player.

The Neo Geo CD has 4 buttons, **A**, **B**, **C** and **D**. The libretro cores add button combinations on the shoulder buttons, handy for special moves.

<table><thead><tr><th>RetroBat controller</th><th>neocd</th><th>geolith</th><th>fbneo (CLASSIC, default)</th><th width="134">raine</th></tr></thead><tbody><tr><td>SOUTH</td><td>A</td><td>A</td><td>A</td><td>A</td></tr><tr><td>EAST</td><td>B</td><td>B</td><td>B</td><td>B</td></tr><tr><td>WEST</td><td>C</td><td>C</td><td>C</td><td>C</td></tr><tr><td>NORTH</td><td>D</td><td>D</td><td>D</td><td>D</td></tr><tr><td>L1</td><td>C + D</td><td>C + D</td><td>C + D</td><td>—</td></tr><tr><td>R1</td><td>A + B</td><td>A + B</td><td>A + B</td><td>—</td></tr><tr><td>L2</td><td>B + C + D</td><td>B + C</td><td>B + C + D</td><td>—</td></tr><tr><td>R2</td><td>A + B + C</td><td>A + B + C</td><td>A + B + C</td><td>—</td></tr></tbody></table>

With the fbneo core, **CONTROLS > CONTROLLER TYPE** offers the same layouts as for the Neo Geo (see the [**Neo Geo**](neo-geo.md#controls) page).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (641).png" alt="" width="225"><figcaption><p>NeoCD standard controls</p></figcaption></figure></div>

### Hotkeys

The libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

**Raine**

| Hotkey             | Action              | Keyboard |
| ------------------ | ------------------- | -------- |
| **HOTKEY + START** | Quit                | ESC      |
| HOTKEY + WEST      | Save state          | F2       |
| HOTKEY + NORTH     | Load state          | F4       |
| HOTKEY + UP / DOWN | Next save slot      | F6       |
| HOTKEY + R3        | Screenshot          | F8       |
| HOTKEY + EAST      | Raine menu          | F1       |
| HOTKEY + L3        | Pause               | P        |
| HOTKEY + LEFT      | Frame advance       | K        |
| —                  | Fullscreen / window | F        |
| —                  | Reset the game      | F9       |

The keys can be changed in the `kb_hotkeys.yml` file (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

| Content                                                           | Folder                           |
| ----------------------------------------------------------------- | -------------------------------- |
| Games                                                             | `roms\neogeocd`                  |
| BIOS (neocd core)                                                 | `bios\neocd`                     |
| BIOS (geolith, fbneo, raine)                                      | `bios`                           |
| neocd core: game saves (console memory, one `.srm` file per game) | `saves\neogeocd`                 |
| geolith core: game saves                                          | `saves\neogeocd`                 |
| fbneo core: game saves                                            | `saves\neogeocd\fbneo`           |
| libretro cores: save states                                       | `saves\neogeocd\libretro.<core>` |
| Raine: save states and game saves                                 | `emulators\raine\savegame`       |
| Raine: screenshots                                                | `screenshots\raine`              |

## Guides

### Loading times

Loading is the main drawback of the Neo Geo CD. Several options reduce it:

<table><thead><tr><th width="153.25">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>neocd, geolith</td><td><strong>EMULATION > CD SKIP LOADING</strong></td><td>Automatic fast forward during loading. On by default with neocd, off with geolith.</td></tr><tr><td>neocd, geolith</td><td><strong>EMULATION > CD SPEED</strong></td><td>Replaces the drive wait loop of the BIOS, to load faster. Off by default. No effect with the Universe BIOS on geolith.</td></tr><tr><td>raine</td><td><strong>EMULATION > IMPROVE CD LOADING SPEED</strong></td><td>Speed of the emulated drive, from 1X to 48X (8X by default), or <strong>NO</strong> for the original speed.</td></tr><tr><td>raine</td><td><strong>EMULATION > PERFORMANCE MODE</strong></td><td>Speeds up emulation at the cost of accuracy (on by default).</td></tr></tbody></table>

### Game saves

The Neo Geo CD saves games in its internal memory. With the neocd core, RetroBat creates one memory per game (a `.srm` file in `saves\neogeocd`): the saves of one game do not fill the memory of the others.

With the neocd core, a save state keeps the type of BIOS used. A state made with the built-in BIOS does not load correctly with an original BIOS, and the other way round.

### The Universe BIOS

The Universe CD BIOS can change the region and gives access to cheats. It is selected with **EMULATION > BIOS**: **UNIVERSE** (neocd, `uni-bioscd.rom` file) or **CDZ (UNIVERSE BIOS)** (geolith). Its menus open as on the Neo Geo (see the [**Neo Geo**](neo-geo.md) page).

In RetroAchievements hardcore mode, the neocd core refuses the Universe BIOS: keep another BIOS to play in hardcore.

### RetroAchievements

The Neo Geo CD has its own category on RetroAchievements. The neocd core is recommended. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="144.5">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>neocd, geolith</td><td><strong>EMULATION > REGION</strong></td><td>Japan, USA (default), Europe (and Asia with geolith). Some games change with the region.</td></tr><tr><td>geolith</td><td><strong>VIDEO > GAME ASPECT RATIO (CORE)</strong></td><td><strong>1:1 (SQUARE PIXELS)</strong> (default), <strong>45:44 (ACCURATE NTSC)</strong> or <strong>4:3 (TRADITIONAL NTSC)</strong>. Used when <strong>GAME ASPECT RATIO</strong> is on AUTO.</td></tr><tr><td>raine</td><td><strong>AUDIO > CD MUSIC VOLUME</strong> / <strong>CD SFX VOLUME</strong></td><td>Volume of the CD music and of the sound effects, from 0 to 200 (70 by default).</td></tr></tbody></table>

## Known issues

| Issue                                                                | Solution                                                                                                                                             |
| -------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| The neocd core starts without BIOS or some games crash               | No BIOS recognized in `bios\neocd`: the core uses its built-in BIOS, which is incomplete. Add an original BIOS (see [**BIOS**](neo-geo-cd.md#bios)). |
| Geolith: the game does not start with the Front Loader or Top Loader | These models need `neocd.zip` **and** `neocdz.zip` in `bios`.                                                                                        |
| fbneo or Raine do not start                                          | `neocdz.zip` is missing from `bios` (and `neogeo.zip` for fbneo).                                                                                    |
| An `.iso`, `.zip` or `.7z` game only offers Raine                    | The other emulators only read `.cue` and `.chd`. Convert the game to `.chd`.                                                                         |
| A `.chd` does not start with Raine                                   | Raine does not read `.chd`: use the neocd core.                                                                                                      |
| Metal Slug 2: crackling sound (neocd)                                | Use a CDZ BIOS.                                                                                                                                      |
| Cyber Lip asks to format the memory                                  | Normal console behavior: accept the format on the BIOS screen.                                                                                       |
| RetroAchievements switches to normal mode                            | The Universe BIOS is selected: choose another BIOS in **EMULATION > BIOS**.                                                                          |
