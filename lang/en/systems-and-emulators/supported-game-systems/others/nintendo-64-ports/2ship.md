# 2 Ship 2 Harkinian

<div align="left"><figure><img src="../../../../.gitbook/assets/image (612).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

**2 Ship 2 Harkinian** (2Ship) is a PC port of **The Legend of Zelda: Majora's Mask** (Nintendo, 2000), made by the HarbourMasters team, the Ship of Harkinian team, from the game's decompilation. It adds high resolution, widescreen, frame rates up to 360 fps, many enhancements, texture packs and a Randomizer mode.

The game is not provided: 2Ship extracts the data from your own ROM of the game (US Nintendo 64 or GameCube version).

{% embed url="https://github.com/HarbourMasters/2ship2harkinian" %}

## At a glance

<table><thead><tr><th width="199"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\2ship</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64 .n64 .v64</td></tr><tr><td><strong>Default emulator</strong></td><td>2ship</td></tr><tr><td><strong>BIOS</strong></td><td>None (game ROM required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (player 1)</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## BIOS

No BIOS is required.

## Which game format should I use?

2Ship reads Nintendo 64 ROMs in **.z64**, **.n64** and **.v64** format. `.zip` archives are not accepted.

Supported versions:

<table><thead><tr><th width="491.5">Version</th><th>Game language</th></tr></thead><tbody><tr><td>Nintendo 64 NTSC-U 1.0 (USA)</td><td>English</td></tr><tr><td>GameCube NTSC-U (USA, Zelda Collector's Edition version)</td><td>English</td></tr></tbody></table>

PAL and Japanese versions are not supported, so the game is in English. To check your ROM, load it in the compatibility checker below.

{% embed url="https://2ship.equipment/" %}

## Controls

### Automatic configuration

RetroBat sets up the player 1 controller at each launch:

<table><thead><tr><th width="226.5">RetroBat controller</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Left stick</td><td>Stick</td></tr><tr><td>SOUTH</td><td>A</td></tr><tr><td>WEST</td><td>B</td></tr><tr><td>L2</td><td>Z</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>Right stick</td><td>C buttons</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>Open / close the 2Ship menu</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

To put Z on the right trigger, set **CONTROLS > CONTROL LAYOUT** to **STANDARD (Z RIGHTTRIGGER)**.

The other **CONTROLS** options: **ANALOG DEADZONE**, **ENABLE RUMBLE** and **RUMBLE STRENGTH**, **ENABLE MOTION** and **GYRO SENSITIVITY** (controllers with a gyroscope).

To keep a configuration made in the 2Ship menu, disable **AUTOCONFIGURE CONTROLLERS**.

### N64 controllers

RetroBat recognizes the Nintendo Switch Online N64 controller and the Mayflash and Raphnet N64 adapters, and gives them a dedicated configuration.

{% hint style="info" %}
With the Mayflash adapter, plug the controllers in reverse order: player 1 is the controller plugged into the last port of the adapter.
{% endhint %}

For more details, see the [**Special controllers**](../../../../controllers/supported-controllers/gamepads/special-controllers.md) page.

### Hotkeys

<table><thead><tr><th width="230.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td><strong>SELECT</strong></td><td>Open / close the 2Ship menu</td></tr></tbody></table>

On the keyboard:

<table><thead><tr><th width="174">Key</th><th>Action</th></tr></thead><tbody><tr><td><strong>Esc</strong> or <strong>F1</strong></td><td>Open / close the menu</td></tr><tr><td><strong>F11</strong></td><td>Fullscreen</td></tr><tr><td><strong>Tab</strong></td><td>Toggle custom textures</td></tr><tr><td><strong>Ctrl + R</strong></td><td>Reset the game</td></tr></tbody></table>

While the menu is open, the controller moves through it: D-pad to choose, SOUTH to confirm, EAST to go back. The game no longer receives the controller inputs while the menu is shown.

## Folders

<table><thead><tr><th width="244">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Saves</td><td><code>emulators\2ship\saves</code></td></tr><tr><td>Extracted game data</td><td><code>emulators\2ship\mm.o2r</code></td></tr><tr><td>Mods and texture packs</td><td><code>emulators\2ship\mods</code></td></tr><tr><td>Presets</td><td><code>emulators\2ship\presets</code></td></tr><tr><td>Configuration</td><td><code>emulators\2ship\2ship2harkinian.json</code></td></tr></tbody></table>

## Guides

### First launch

On the first launch, RetroBat passes the ROM to 2Ship, which extracts its data to `mm.o2r` and then starts the game. The extraction takes a few minutes. The next launches start directly.

After a 2Ship update that changes the data format, RetroBat deletes the old archive and 2Ship extracts the data again.

One entry is enough in `roms\2ship`: once the data is extracted, the ROM is no longer read.

### Mods and texture packs

Place the mods (`.o2r` or `.otr` files: textures, models, music) in `emulators\2ship\mods`, then start the game. **Tab** toggles the custom textures in game.

### Randomizer

The Randomizer is set in the 2Ship menu (**SELECT** or **Esc**), before creating a new save.

### Other useful options

<table><thead><tr><th width="295.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Rendering resolution, from NATIVE (240 lines) to 4K. Default: <strong>2X(480)</strong>.</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>By default, the picture fills the screen. <strong>NATIVE (4:3)</strong> keeps the original proportions, <strong>WIDESCREEN (16:9)</strong>, <strong>3DS (5:3)</strong>, <strong>16:10</strong> or <strong>ULTRAWIDE (21:9)</strong> widen the field of view.</td></tr><tr><td><strong>DECORATIONS</strong></td><td>Decorations are only shown with <strong>GAME ASPECT RATIO</strong> set to <strong>NATIVE (4:3)</strong>.</td></tr><tr><td><strong>INTEGER SCALING</strong></td><td>Scales the picture by whole numbers only, for sharp pixels.</td></tr><tr><td><strong>EMULATION > TARGET FPS</strong></td><td>Frame rate, from 20 (original rate, default) to 360 fps. In-between frames are interpolated.</td></tr><tr><td><strong>EMULATION > MATCH FPS TO DISPLAY RATE</strong></td><td>Follows the display refresh rate (60 Hz, 144 Hz…) instead of <strong>TARGET FPS</strong>.</td></tr><tr><td><strong>VISUAL RENDERING > TEXTURE FILTERING</strong></td><td><strong>THREE POINT</strong> (default, like the N64), <strong>LINEAR</strong> or <strong>NONE</strong>.</td></tr><tr><td><strong>VISUAL RENDERING > ANTI-ALIASING (MSAA)</strong></td><td>Smooths polygon edges (1 to 8).</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td><strong>DIRECTX 11</strong> (default) or <strong>OPENGL</strong>.</td></tr><tr><td><strong>DRIVERS > AUDIO</strong></td><td><strong>WASAPI</strong> (default) or <strong>SDL</strong>.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="355.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>2Ship says the ROM is not supported</td><td>Only the US N64 1.0 version and the US GameCube version are accepted: check the ROM on <strong>2ship.equipment</strong>.</td></tr><tr><td>The game is in English</td><td>2Ship only supports the US versions of the game.</td></tr><tr><td>The 2Ship menu opens during the game</td><td><strong>SELECT</strong> opens the menu: press <strong>SELECT</strong> again to close it.</td></tr><tr><td>Black screen or crash at launch</td><td>Set <strong>DRIVERS > VIDEO</strong> to <strong>OPENGL</strong>.</td></tr><tr><td>Decorations are not shown</td><td>Set <strong>GAME ASPECT RATIO</strong> to <strong>NATIVE (4:3)</strong>.</td></tr><tr><td>A mod does not show</td><td>Check that it is in <code>emulators\2ship\mods</code> and made for the shipped 2Ship version; press <strong>Tab</strong> to enable custom textures.</td></tr></tbody></table>
