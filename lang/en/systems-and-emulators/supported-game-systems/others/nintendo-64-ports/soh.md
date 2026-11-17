# Ship Of Harkinian

<div align="left"><figure><img src="../../../../.gitbook/assets/image (614).png" alt="" width="403"><figcaption></figcaption></figure></div>

## Overview

**Ship of Harkinian** (SoH) is a PC port of **The Legend of Zelda: Ocarina of Time** (Nintendo, 1998), made by the HarbourMasters team from the game's decompilation. It adds high resolution, widescreen, frame rates up to 360 fps, many enhancements, texture packs and a Randomizer mode.

The game is not provided: SoH extracts the data from your own ROM of the game (Nintendo 64 or GameCube), original or **Master Quest**.

{% embed url="https://www.shipofharkinian.com" %}

## At a glance

<table><thead><tr><th width="219"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\soh</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64 .n64 .v64</td></tr><tr><td><strong>Default emulator</strong></td><td>soh</td></tr><tr><td><strong>BIOS</strong></td><td>None (game ROM required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (player 1)</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## BIOS

No BIOS is required.

## Which game format should I use?

SoH reads Nintendo 64 ROMs in **.z64**, **.n64** and **.v64** format (GameCube ROMs are N64 ROMs extracted from the disc). `.zip` archives are not accepted.

Supported versions:

<table><thead><tr><th width="325.75">Version</th><th width="163.25">Quest</th><th>Game languages</th></tr></thead><tbody><tr><td>Nintendo 64 NTSC 1.0, 1.1, 1.2 (USA, Japan)</td><td>Original</td><td>English, Japanese</td></tr><tr><td>Nintendo 64 PAL 1.0, 1.1</td><td>Original</td><td>English, German, French</td></tr><tr><td>GameCube NTSC (USA, Japan, Collector's Edition)</td><td>Original</td><td>English, Japanese</td></tr><tr><td>GameCube PAL</td><td>Original</td><td>English, German, French</td></tr><tr><td>GameCube Master Quest NTSC (USA, Japan)</td><td>Master Quest</td><td>English, Japanese</td></tr><tr><td>GameCube Master Quest PAL</td><td>Master Quest</td><td>English, German, French</td></tr><tr><td>GameCube PAL debug (original and Master Quest)</td><td>Both</td><td>English, German, French</td></tr></tbody></table>

To check your ROM, load it in the compatibility checker below: it tells whether it is supported, its region and whether it is Master Quest.

{% embed url="https://ship.equipment/" %}

One entry is enough in `roms\soh`: once the data is extracted, every ROM of the folder starts the same game.

## Controls

### Automatic configuration

RetroBat sets up the player 1 controller at each launch:

<table><thead><tr><th width="231.5">RetroBat controller</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Left stick</td><td>Stick</td></tr><tr><td>SOUTH</td><td>A</td></tr><tr><td>WEST</td><td>B</td></tr><tr><td>L2</td><td>Z</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>Right stick</td><td>C buttons</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>Open / close the SoH menu</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

To put Z on the right trigger, set **CONTROLS > CONTROL LAYOUT** to **STANDARD (Z RIGHTTRIGGER)**.

The other **CONTROLS** options: **ANALOG DEADZONE**, **ENABLE RUMBLE** and **RUMBLE STRENGTH**, **ENABLE MOTION** and **GYRO SENSITIVITY** (controllers with a gyroscope).

To keep a configuration made in the SoH menu, disable **AUTOCONFIGURE CONTROLLERS**.

### N64 controllers

RetroBat recognizes the Nintendo Switch Online N64 controller and the Mayflash and Raphnet N64 adapters, and gives them a dedicated configuration.

{% hint style="info" %}
With the Mayflash adapter, plug the controllers in reverse order: player 1 is the controller plugged into the last port of the adapter.
{% endhint %}

For more details, see the [**Special controllers**](../../../../controllers/supported-controllers/gamepads/special-controllers.md) page.

### Hotkeys

<table><thead><tr><th width="235.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td><strong>SELECT</strong></td><td>Open / close the SoH menu</td></tr></tbody></table>

On the keyboard:

<table><thead><tr><th width="170.25">Key</th><th>Action</th></tr></thead><tbody><tr><td><strong>Esc</strong> or <strong>F1</strong></td><td>Open / close the menu</td></tr><tr><td><strong>F11</strong></td><td>Fullscreen</td></tr><tr><td><strong>Tab</strong></td><td>Toggle custom textures</td></tr><tr><td><strong>Ctrl + R</strong></td><td>Reset the game</td></tr><tr><td><strong>F5</strong> / <strong>F6</strong> / <strong>F7</strong></td><td>Save state / change slot / load state (experimental, not managed by RetroBat)</td></tr></tbody></table>

While the menu is open, the controller moves through it: D-pad to choose, SOUTH to confirm, EAST to go back. The game no longer receives the controller inputs while the menu is shown.

## Folders

<table><thead><tr><th width="244">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Saves</td><td><code>emulators\soh\Save</code></td></tr><tr><td>Extracted game data</td><td><code>emulators\soh\oot.o2r</code> (Master Quest: <code>oot-mq.o2r</code>)</td></tr><tr><td>Mods and texture packs</td><td><code>emulators\soh\mods</code></td></tr><tr><td>Randomizer logs</td><td><code>emulators\soh\Randomizer</code></td></tr><tr><td>Configuration</td><td><code>emulators\soh\shipofharkinian.json</code></td></tr></tbody></table>

## Guides

### First launch

On the first launch, RetroBat passes the ROM to SoH, which extracts its data to `oot.o2r` (or `oot-mq.o2r` for a Master Quest ROM). The extraction takes a few minutes, then SoH asks **Run Ship of Harkinian?**: answer **Yes** to start the game.

The next launches start directly. After a SoH update that changes the data format, RetroBat deletes the old archive and SoH extracts the data again.

### Playing Master Quest

To get both quests, also place the Master Quest ROM in `roms\soh`: its name must contain "Master Quest", like the No-Intro names (for example `Legend of Zelda, The - Ocarina of Time - Master Quest (USA) (GameCube Edition).z64`). Start it once from RetroBat: SoH creates `oot-mq.o2r` next to `oot.o2r`.

With both archives, the file select screen lets you choose the quest (original or Master Quest) when creating a new save. The Randomizer can also mix the dungeons of both versions.

### Game language

Set **EMULATION > LANGUAGE** to **ENGLISH**, **DEUTSCH**, **FRENCH** or **JAPANESE**. German and French texts are only in the **PAL** versions of the game: with an NTSC version, the game stays in English. Japanese, on the other hand, needs an NTSC version.

### Mods and texture packs

Place the mods (`.o2r` or `.otr` files: textures, models, music) in `emulators\soh\mods`, then start the game. **Tab** toggles the custom textures in game.

### Randomizer

The Randomizer is set in the SoH menu (**SELECT** or **Esc**): choose the settings, generate a seed, then create a new Randomizer save on the file select screen.

### Other useful options

<table><thead><tr><th width="351.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Rendering resolution, from NATIVE (240 lines) to 4K. Default: <strong>2X(480)</strong>.</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>By default, the picture fills the screen. <strong>NATIVE (4:3)</strong> keeps the original proportions, <strong>WIDESCREEN (16:9)</strong>, <strong>3DS (5:3)</strong>, <strong>16:10</strong> or <strong>ULTRAWIDE (21:9)</strong> widen the field of view.</td></tr><tr><td><strong>DECORATIONS</strong></td><td>Decorations are only shown with <strong>GAME ASPECT RATIO</strong> set to <strong>NATIVE (4:3)</strong>.</td></tr><tr><td><strong>INTEGER SCALING</strong></td><td>Scales the picture by whole numbers only, for sharp pixels.</td></tr><tr><td><strong>EMULATION > TARGET FPS</strong></td><td>Frame rate, from 20 (original rate, default) to 360 fps. In-between frames are interpolated.</td></tr><tr><td><strong>EMULATION > MATCH FPS TO DISPLAY RATE</strong></td><td>Follows the display refresh rate (60 Hz, 144 Hz…) instead of <strong>TARGET FPS</strong>.</td></tr><tr><td><strong>VISUAL RENDERING > TEXTURE FILTERING</strong></td><td><strong>THREE POINT</strong> (default, like the N64), <strong>LINEAR</strong> or <strong>NONE</strong>.</td></tr><tr><td><strong>VISUAL RENDERING > ANTI-ALIASING (MSAA)</strong></td><td>Smooths polygon edges (1 to 8).</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td><strong>DIRECTX</strong> (default) or <strong>OPENGL</strong>.</td></tr><tr><td><strong>DRIVERS > AUDIO</strong></td><td><strong>WASAPI</strong> (default) or <strong>SDL</strong>.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="332.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>SoH says the ROM is not supported</td><td>Check the ROM on <strong>ship.equipment</strong>: only the listed versions are accepted. A modified ROM (translation, hack) does not work.</td></tr><tr><td>SoH stays on the "Run Ship of Harkinian?" window</td><td>It only shows once, after the extraction: answer <strong>Yes</strong>.</td></tr><tr><td>The game stays in English with the language set to <strong>FRENCH</strong></td><td>French only exists in the PAL versions of the game (see <a href="soh.md#game-language"><strong>Guides</strong></a>).</td></tr><tr><td>The Master Quest ROM starts the original quest</td><td>The file name must contain "Master Quest" for RetroBat to pass it to SoH (see <a href="soh.md#playing-master-quest"><strong>Guides</strong></a>).</td></tr><tr><td>The SoH menu opens during the game</td><td><strong>SELECT</strong> opens the menu: press <strong>SELECT</strong> again to close it.</td></tr><tr><td>Black screen or crash at launch</td><td>Set <strong>DRIVERS > VIDEO</strong> to <strong>OPENGL</strong>.</td></tr><tr><td>Decorations are not shown</td><td>Set <strong>GAME ASPECT RATIO</strong> to <strong>NATIVE (4:3)</strong>.</td></tr><tr><td>A mod does not show</td><td>Check that it is in <code>emulators\soh\mods</code> and made for the shipped SoH version; press <strong>Tab</strong> to enable custom textures.</td></tr></tbody></table>
