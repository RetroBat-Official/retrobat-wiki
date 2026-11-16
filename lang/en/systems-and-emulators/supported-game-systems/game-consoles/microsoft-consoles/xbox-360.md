---
description: Microsoft
---

# Xbox 360

<div align="left"><figure><img src="../../../../.gitbook/assets/image (573).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Xbox 360** is Microsoft's second home console. It was released in November 2005, a year before the PlayStation 3 and the Wii, and started the high-definition generation. It is built around a three-core PowerPC processor (Xenon) and an ATI graphics chip (Xenos) with embedded video memory.

Its online service, **Xbox Live**, with achievements, profiles and **Xbox Live Arcade** (small downloadable games), defined the generation. The console sold about 84 million units, despite the failures of the first models (the "Red Ring of Death"). Notable games include Halo 3, Gears of War, Forza Motorsport, Mass Effect, Fable II, Red Dead Redemption and Left 4 Dead.

RetroBat uses **Xenia**, the only Xbox 360 emulator, in several versions: **Xenia Canary** (default), **Xenia Edge**, **Xenia Manager** and **Xenia** (original version).

{% embed url="https://en.wikipedia.org/wiki/Xbox_360" %}

## In short

<table><thead><tr><th width="221.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\xbox360</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .xex .xcp .zar .m3u .xbox360 .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>xenia-canary</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>No (Xenia detects the controllers itself)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="167">Emulator</th><th width="306.25">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>xenia-canary</strong> (default)</td><td>The most active and most compatible version. Game patches, profiles, console settings (language, resolution, aspect ratio).</td><td>Needs a recent PC (Direct3D 12 or Vulkan).</td></tr><tr><td><strong>xenia-edge</strong></td><td>Derived from Canary, with fixes and per-game settings. PAL 50 Hz mode.</td><td>Controllers through SDL only (no controller type choice). Its per-game settings take priority over RetroBat's (see <a href="xbox-360.md#xenia-edge-per-game-settings">Guides</a>).</td></tr><tr><td><strong>xenia-manager</strong></td><td>Launcher that installs and manages the Xenia versions. RetroBat can use the per-game configuration made in Xenia Manager. Three versions: <strong>canary</strong>, <strong>mousehook</strong> (mouse and keyboard for shooters), <strong>netplay</strong> (online play).</td><td></td></tr><tr><td><strong>xenia</strong></td><td>Original version.</td><td>No longer updated: less compatible than Canary, fewer options.</td></tr></tbody></table>

The Xenia Canary compatibility list ([github.com/xenia-canary/game-compatibility](https://github.com/xenia-canary/game-compatibility/issues)) shows the state of each game. If a game does not work with Canary, try Edge.

## BIOS

The Xbox 360 has no BIOS to provide: Xenia replaces the console system with its own code.

### Console language

Games use the language of the emulated console settings. By default, RetroBat uses the RetroBat language (English if it does not exist on Xbox 360). The **EMULATION > LANGUAGE** option forces another language.

With Canary and Xenia Manager, RetroBat also writes in the console settings (`xconfig.settings` file) the aspect ratio (**CONSOLE ASPECT RATIO**), the video standard (**VIDEO > VIDEO STANDARD**) and the output resolution (**VIDEO > INTERNAL GAME RESOLUTION**).

## Which game format?

<table><thead><tr><th width="165.25">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.iso</strong></td><td>Disc image. The most common format. A folder that contains an <code>.iso</code> image can also be launched: RetroBat uses the first image found.</td></tr><tr><td><strong>.xex</strong></td><td>Extracted game: launch the <code>default.xex</code> file of the game folder.</td></tr><tr><td><strong>.zar</strong></td><td>Game compressed into a single file (ZArchive), depending on the emulator.</td></tr><tr><td><strong>.xcp</strong></td><td>Xbox Live content package, depending on the emulator.</td></tr><tr><td><strong>.m3u</strong>, <strong>.xbox360</strong></td><td>Text file that gives the path of the game, for games without extension (Xbox Live Arcade, Games on Demand): see <a href="xbox-360.md#launching-an-xbox-live-arcade-or-games-on-demand-game">Guides</a>.</td></tr><tr><td>.decomp</td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

`.zip` and `.7z` archives are not supported.

## Controls

### Controller configuration

RetroBat does not configure the controllers for Xenia: the emulator detects them itself, up to 4 players. The player order is Xenia's, it can differ from RetroBat's.

The **CONTROLS > CONTROLLER TYPE** option (Canary, Xenia Manager, Xenia) chooses how Xenia reads the controllers:

<table><thead><tr><th width="240.25">Choice</th><th>Use</th></tr></thead><tbody><tr><td><strong>SDL</strong> (default)</td><td>All controllers (Xbox, PlayStation, Switch…).</td></tr><tr><td><strong>XBOX CONTROLLER</strong></td><td>Xbox controllers (XInput) only.</td></tr><tr><td><strong>KEYBOARD</strong></td><td>Keyboard.</td></tr></tbody></table>

Xenia Edge always uses SDL.

<table><thead><tr><th width="221.5">Xbox 360</th><th>Controller</th></tr></thead><tbody><tr><td>A, B, X, Y</td><td>SOUTH, EAST, WEST, NORTH</td></tr><tr><td>LB, RB</td><td>L1, R1</td></tr><tr><td>LT, RT</td><td>L2, R2</td></tr><tr><td>Back, Start</td><td>SELECT, START</td></tr><tr><td>Stick clicks</td><td>L3, R3</td></tr><tr><td>D-pad, sticks</td><td>D-pad, sticks</td></tr></tbody></table>

**Xenia Manager, mousehook version**: mouse and keyboard are set in Xenia Manager, RetroBat does not change them.

### Hotkeys

<table><thead><tr><th width="247.75">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr></tbody></table>

The other RetroBat hotkeys (menu, save states, fast forward…) are not handled for Xenia, which has no save states.

## Folders

<table><thead><tr><th width="310.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Canary configuration</td><td><code>emulators\xenia-canary\xenia-canary.config.toml</code></td></tr><tr><td>Edge configuration</td><td><code>emulators\xenia-edge\xenia-edge.config.toml</code></td></tr><tr><td>Xenia configuration</td><td><code>emulators\xenia\xenia.config.toml</code></td></tr><tr><td>Xenia Manager emulators</td><td><code>emulators\xenia-manager\Emulators\Xenia Canary</code> (<code>Xenia Mousehook</code>, <code>Xenia Netplay</code>)</td></tr><tr><td>Xenia Manager library</td><td><code>emulators\xenia-manager\Config\games.json</code></td></tr><tr><td>Content (saves, profiles, title updates, downloadable content)</td><td><code>saves\xbox360\xenia\content</code></td></tr></tbody></table>

All Xenia versions use the same `content` folder: saves and profiles are shared between Canary, Edge, Xenia Manager and Xenia.

At the first launch, RetroBat moves the `content` folder of the launched Xenia version to `saves\xbox360\xenia\content`, to keep your saves. If you also had saves in another version, copy the content of its `content` folder (for example `emulators\xenia-edge\content`) to `saves\xbox360\xenia\content`.

With a Xenia Manager game configuration, the folder set in Xenia Manager is used.

## Guides

### Launching an Xbox Live Arcade or Games on Demand game

These games come as a series of folders, ending with a file without extension. For example, for Banjo-Tooie:

`roms\xbox360\Banjo Tooie\58410955\000D0000\ABB9CAB336175357D09F2D922735D23C62F90DDD`

1. Create a text file in `roms\xbox360`, with the `.m3u` or `.xbox360` extension (for example `Banjo Tooie.m3u`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (574).png" alt=""><figcaption></figcaption></figure></div>

2. On the first line, write the path of the game file, from `roms\xbox360`:

```
\Banjo Tooie\58410955\000D0000\ABB9CAB336175357D09F2D922735D23C62F90DDD
```

3. Update the game list: this file is the game shown in RetroBat.

### Using profiles

Xbox 360 profiles keep the saves and achievements of each player in Xenia.

1. Create the profile in Xenia Canary or Edge (emulator menu), then quit.
2. In RetroBat, choose **EMULATION > PROFILE PLAYER 1** (to 4) and select the profile folder in `saves\xbox360\xenia\content` (its name is the profile ID, 16 characters).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (575).png" alt=""><figcaption></figcaption></figure></div>

The profile must be in `saves\xbox360\xenia\content`, otherwise RetroBat ignores it.

### Using the Xenia Manager configuration

1. Open Xenia Manager (`emulators\xenia-manager`), add your games and set them up (the canary, mousehook and netplay versions come with RetroBat).
2. In RetroBat, choose the **xenia-manager** emulator and the version (**canary**, **mousehook** or **netplay**) for the system or the game.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (576).png" alt=""><figcaption></figcaption></figure></div>

At launch, RetroBat looks for the game in the Xenia Manager library (`Config\games.json`), by its file name. If the game has a configuration, RetroBat gives it to Xenia and does not apply its own options. Otherwise, the RetroBat options are used, as with Canary.

### Xenia Edge per-game settings

Xenia Edge applies the per-game settings of its `config` folder (`<game ID>.config.toml`), which take priority over RetroBat's. To apply the RetroBat options, enable **EMULATION > IGNORE OPTIMIZED SETTINGS**: the folder is set aside during the game, then put back.

### Other useful options

<table><thead><tr><th width="346.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Raises the rendering resolution, from 1280x720 (default) up to 5120x2880.</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td>DIRECT3D12 or VULKAN. By default, Xenia chooses.</td></tr><tr><td><strong>EMULATION > ENABLE PATCHES</strong></td><td>Canary and Edge: applies the game patches of the <code>patches</code> folder of the emulator (fixes, 60 frames per second…).</td></tr><tr><td><strong>VIDEO > FRAMERATE LIMIT</strong></td><td>Canary and Edge: 60 frames per second by default.</td></tr><tr><td><strong>EMULATION > REFRESH MEMORY PAGES STATE</strong></td><td>Canary and Edge: fixes invisible characters in Team Ninja games.</td></tr><tr><td><strong>VIDEO > READBACK RESOLVE</strong></td><td>Needed for some games, but slows down emulation a lot.</td></tr><tr><td><strong>EMULATION > LICENCE MASK</strong></td><td>Enables downloaded content (<strong>FIRST LICENCE ENABLED</strong> by default).</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="359">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start</td><td>Check the game state in the compatibility list, then try Edge, or change the video driver (<strong>DRIVERS > VIDEO</strong>).</td></tr><tr><td>The controller does not respond</td><td>Check <strong>CONTROLS > CONTROLLER TYPE</strong>: <strong>SDL</strong> for all controllers, <strong>XBOX CONTROLLER</strong> for Xbox controllers.</td></tr><tr><td>Players are not in the right order</td><td>The order is handled by Xenia: connect the controllers in player order before launching the game.</td></tr><tr><td>Stuttering at the start of a game</td><td>Shaders are compiled the first time: keep <strong>VIDEO > USE ASYNCHRONOUS SHADER COMPILATION</strong> enabled.</td></tr><tr><td>Invisible characters or objects</td><td>Enable <strong>EMULATION > REFRESH MEMORY PAGES STATE</strong> (Team Ninja games), or try <strong>VIDEO > READBACK RESOLVE</strong>.</td></tr><tr><td>RetroBat options are not applied with Edge</td><td>Enable <strong>EMULATION > IGNORE OPTIMIZED SETTINGS</strong> (see <a href="xbox-360.md#xenia-edge-per-game-settings">Guides</a>).</td></tr><tr><td>RetroBat options are not applied with Xenia Manager</td><td>The game has a configuration in Xenia Manager: set it up in Xenia Manager.</td></tr><tr><td>An Xbox Live Arcade game does not show up</td><td>Create an <code>.m3u</code> or <code>.xbox360</code> file (see <a href="xbox-360.md#launching-an-xbox-live-arcade-or-games-on-demand-game">Guides</a>).</td></tr></tbody></table>
