# Perfect Dark

<div align="left"><figure><img src="https://github.com/fabricecaruso/es-theme-carbon/blob/master/art/logos/pdark.png?raw=true" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

**Perfect Dark** is a first-person shooter by Rare, released in 2000 on the Nintendo 64. A spiritual successor to GoldenEye 007, it follows agent Joanna Dark through a spy and science-fiction campaign. It also offers a four-player split-screen multiplayer mode, the **Combat Simulator**, with computer-controlled opponents (the "simulants").

The **perfect\_dark** PC port, made by fgsfds from the game's decompilation, adds:

* mouse aiming and twin-stick controllers;
* widescreen and an adjustable field of view;
* 60 frames per second, and higher as an experimental option;
* fixes for a few original bugs.

The game is not provided: the port reads the data from your own ROM of the game.

{% embed url="https://github.com/fgsfdsfgs/perfect_dark" %}

## At a glance

<table><thead><tr><th width="232.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\pdark</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64 .n64 .v64</td></tr><tr><td><strong>Default emulator</strong></td><td>pdark</td></tr><tr><td><strong>BIOS</strong></td><td>None (game ROM required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (4 players)</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## BIOS

No BIOS is required.

## Which game format should I use?

Place the game's Nintendo 64 ROM in `roms\pdark`, uncompressed (no `.zip` or `.7z`). The ROM must be 32 MB.

The `.z64`, `.n64` and `.v64` formats are accepted. A `.n64` or `.v64` ROM is converted to `.z64` automatically on first launch, in `emulators\pdark\data`.

Supported versions:

<table><thead><tr><th width="110.25">Version</th><th width="140">Boot screen</th><th width="311.25">MD5 (.z64)</th><th>Note</th></tr></thead><tbody><tr><td>USA 1.1</td><td>NTSC version 8.7 final</td><td><code>e03b088b6ac9e0080440efed07c1e40f</code></td><td>Recommended version</td></tr><tr><td>USA 1.0</td><td>NTSC version 8.7 final</td><td><code>7f4171b0c8d17815be37913f535e4e93</code></td><td>Works, but not recommended</td></tr><tr><td>Europe</td><td>PAL 8.7 final</td><td><code>d9b5cd305d228424891ce38e71bc9213</code></td><td></td></tr><tr><td>Japan</td><td>JPN version 8.9 final</td><td><code>538d2b75945eae069b29c46193e74790</code></td><td></td></tr></tbody></table>

RetroBat detects the version from the ROM and starts the matching executable (US, European or Japanese): there is nothing to set. Beta versions and modified ROMs are not supported.

## Controls

### Controller setup

RetroBat configures up to 4 controllers automatically, one per player. The layout follows an Xbox controller, with one stick to move and the other to aim.

<table><thead><tr><th width="179.5">RetroBat controller</th><th>Action</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Left stick</td><td>Move</td><td>C buttons (analog)</td></tr><tr><td>Right stick</td><td>Look / aim</td><td>Stick</td></tr><tr><td>D-pad</td><td>Move forward, back, sideways</td><td>C buttons</td></tr><tr><td>R2</td><td>Fire / accept</td><td>Z</td></tr><tr><td>L2</td><td>Aim mode</td><td>R</td></tr><tr><td>SOUTH</td><td>Use / accept</td><td>A</td></tr><tr><td>EAST</td><td>Previous weapon / back in menus</td><td>D-pad left</td></tr><tr><td>WEST</td><td>Reload</td><td></td></tr><tr><td>NORTH</td><td>Next weapon</td><td></td></tr><tr><td>L1</td><td>Weapon menu (radial menu)</td><td>D-pad down</td></tr><tr><td>R1</td><td>Secondary fire mode</td><td>L</td></tr><tr><td>L3</td><td>Crouch (press repeatedly)</td><td></td></tr><tr><td>START</td><td>Pause</td><td>START</td></tr></tbody></table>

Combinations:

<table><thead><tr><th width="309">Combination</th><th>Action</th></tr></thead><tbody><tr><td><strong>SOUTH + R2</strong> or <strong>R1 + R2</strong></td><td>Secondary fire, once</td></tr><tr><td><strong>SOUTH + EAST</strong> or <strong>SOUTH + WEST</strong></td><td>Detonate placed explosives</td></tr></tbody></table>

**CONTROLS > RUMBLE STRENGTH** sets the rumble strength (50% by default).

### Keyboard and mouse

Player 1 can also play with keyboard and mouse, together with their controller. The mouse only controls player 1.

<table><thead><tr><th width="282.75">Key</th><th>Action</th></tr></thead><tbody><tr><td><strong>W A S D</strong></td><td>Move</td></tr><tr><td><strong>Mouse</strong></td><td>Look / aim</td></tr><tr><td><strong>Left click</strong> or <strong>Space</strong></td><td>Fire</td></tr><tr><td><strong>Right click</strong> or <strong>Z</strong></td><td>Aim mode; back in menus</td></tr><tr><td><strong>E</strong></td><td>Use</td></tr><tr><td><strong>R</strong></td><td>Reload</td></tr><tr><td><strong>Mouse wheel</strong></td><td>Previous / next weapon</td></tr><tr><td><strong>Q</strong> or <strong>middle click</strong></td><td>Weapon menu</td></tr><tr><td><strong>F</strong> or <strong>X</strong></td><td>Secondary fire mode</td></tr><tr><td><strong>Left Shift</strong></td><td>Half crouch</td></tr><tr><td><strong>Left Ctrl</strong></td><td>Full crouch</td></tr><tr><td><strong>Tab</strong></td><td>Pause</td></tr><tr><td><strong>Enter</strong></td><td>Accept in menus</td></tr><tr><td><strong>Arrow keys</strong></td><td>Nintendo 64 stick</td></tr></tbody></table>

Keys are given for a QWERTY keyboard: on another layout, use the keys at the same position.

### Hotkeys

<table><thead><tr><th width="261.5">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Exit</td></tr><tr><td><strong>Alt + Enter</strong></td><td>Fullscreen / window</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="325.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Save</td><td><code>saves\pdark\eeprom.bin</code></td></tr><tr><td>Saved multiplayer setups</td><td><code>emulators\pdark\mpsetups.bin</code></td></tr><tr><td>Configuration</td><td><code>emulators\pdark\pd.ini</code></td></tr><tr><td>Converted ROM (<code>.n64</code> / <code>.v64</code> ROM)</td><td><code>emulators\pdark\data</code></td></tr><tr><td>Game Boy Color ROM (optional)</td><td><code>emulators\pdark\data\pd.gbc</code></td></tr></tbody></table>

A save from an older RetroBat version (`emulators\pdark\eeprom.bin`) is copied automatically to `saves\pdark` on first launch.

## Guides

### Multiplayer

The **Combat Simulator** (multiplayer and simulants) is played by up to 4 players in split screen. Missions can also be played by 2 players: in **co-operative**, or in **counter-operative**, where the second player controls the enemies. Connect one controller per player before starting the game: RetroBat gives player 1's controller to player 1, and so on.

### Extended game options

The port adds an **Extended Options** menu to the game's options (**Video**, **Audio**, **Mouse**, **Controller**, **Game**, **Key Bindings** pages). It includes:

* **Vert FOV**: the field of view;
* **HUD Centering**: keeps the HUD in a 4:3 area at the center of the screen;
* **Crouch Mode**: how crouching works;
* the crosshair colour and size;
* **Uncap Tickrate**: frame rate above 60 frames per second (experimental, see [**Known issues**](pdark.md#known-issues)).

These settings are kept between sessions, except the ones RetroBat manages (fullscreen, resolution, vertical sync, filtering, anti-aliasing, keys and rumble).

### Unlocking cheats with the Game Boy Color version

On the Nintendo 64, the Transfer Pak unlocked a few cheats using the Perfect Dark Game Boy Color cartridge. The port emulates this: place the Game Boy Color ROM (USA / Europe version) in `emulators\pdark\data`, named `pd.gbc`.

### Other useful options

<table><thead><tr><th width="351.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>VERTICAL SYNC</strong></td><td>On by default.</td></tr><tr><td><strong>SKIP INTRO</strong></td><td>Starts directly on the game menu.</td></tr><tr><td><strong>VIDEO > VIDEO MODE</strong></td><td>By default, the game uses the desktop resolution.</td></tr><tr><td><strong>VIDEO > MONITOR INDEX</strong></td><td>Screen the game is displayed on.</td></tr><tr><td><strong>VISUAL RENDERING > TEXTURE FILTERING</strong></td><td><strong>BILINEAR</strong> (default), <strong>NEAREST NEIGHBOR</strong> (sharp pixels) or <strong>THREE POINT</strong> (like the Nintendo 64).</td></tr><tr><td><strong>VISUAL RENDERING > DETAIL TEXTURES</strong></td><td>On by default.</td></tr><tr><td><strong>VISUAL RENDERING > ANTI-ALIASING (MSAA)</strong></td><td>Smooths polygon edges: <strong>NO</strong> (default), <strong>2X</strong>, <strong>4X</strong>, <strong>8X</strong> or <strong>16X</strong>.</td></tr><tr><td><strong>AUTOCONFIGURE CONTROLLERS</strong></td><td>When off, RetroBat no longer changes the keys: the ones set in <strong>Extended Options > Key Bindings</strong> are kept.</td></tr></tbody></table>

The picture always fills the screen (widescreen): decorations are not available for this game.

## Known issues

<table><thead><tr><th width="362.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>"Unsupported rom" message at launch</td><td>The ROM is not a supported version, is compressed, or is not 32 MB (see <a href="pdark.md#which-game-format-should-i-use"><strong>Which game format should I use?</strong></a>).</td></tr><tr><td>"ROM header does not match" or "Data segment is not 1173-compressed"</td><td>Modified ROM, beta or bad dump: use a ROM whose MD5 is in the list of supported versions.</td></tr><tr><td>Black screen or crash at launch</td><td>The port needs an OpenGL 3.0 graphics card; update the graphics driver.</td></tr><tr><td>Keys changed in the game come back at every launch</td><td>Turn off <strong>AUTOCONFIGURE CONTROLLERS</strong> for this game.</td></tr><tr><td>Slowdowns or bugs above 60 frames per second</td><td><strong>Uncap Tickrate</strong> is experimental: the game misbehaves above about 165 frames per second. Keep vertical sync on, or cap the frame rate with <strong>Framerate Limit</strong> (<strong>Extended Options > Video</strong>).</td></tr><tr><td>The mouse does not control the other players</td><td>Expected: keyboard and mouse only work for player 1.</td></tr></tbody></table>
