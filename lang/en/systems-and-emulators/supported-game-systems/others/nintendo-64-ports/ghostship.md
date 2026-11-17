# Ghostship

<div align="left"><figure><img src="../../../../.gitbook/assets/image (613).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**Ghostship** is a PC port of **Super Mario 64** (Nintendo, 1996), made by the HarbourMasters team from the game's decompilation. It adds high resolution, widescreen, frame rates up to 360 fps, many enhancements and texture packs.

The game is not provided: Ghostship extracts the data from your own ROM of the game (US or Japanese version).

{% embed url="https://github.com/HarbourMasters/Ghostship" %}

## At a glance

<table><thead><tr><th width="207.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\ghostship</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64</td></tr><tr><td><strong>Default emulator</strong></td><td>ghostship</td></tr><tr><td><strong>BIOS</strong></td><td>None (game ROM required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (player 1)</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## BIOS

No BIOS is required.

## Which game format should I use?

Ghostship only reads ROMs in **.z64** format. A `.n64` or `.v64` ROM must first be converted to `.z64` (for example with the hack64.net online tool).

{% embed url="https://hack64.net/tools/swapper.php" %}

Supported versions:

<table><thead><tr><th width="222.75">Version</th><th>SHA-1</th></tr></thead><tbody><tr><td>Nintendo 64 USA</td><td><code>9bef1128717f958171a4afac3ed78ee2bb4e86ce</code></td></tr><tr><td>Nintendo 64 Japan</td><td><code>8a20a5c83d6ceb0f0506cfc9fa20d8f438cafe51</code></td></tr></tbody></table>

One entry is enough in `roms\ghostship`: once the data is extracted, the ROM is no longer read.

## Controls

### Automatic configuration

RetroBat sets up the player 1 controller at each launch:

<table><thead><tr><th width="216.5">RetroBat controller</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Left stick</td><td>Stick</td></tr><tr><td>SOUTH</td><td>A</td></tr><tr><td>WEST</td><td>B</td></tr><tr><td>L2</td><td>Z</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>Right stick</td><td>C buttons</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>Open / close the Ghostship menu</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

To put Z on the right trigger, set **CONTROLS > CONTROL LAYOUT** to **STANDARD (Z RIGHTTRIGGER)**.

The other **CONTROLS** options: **ANALOG DEADZONE**, **ENABLE RUMBLE** and **RUMBLE STRENGTH**, **ENABLE MOTION** and **GYRO SENSITIVITY** (controllers with a gyroscope).

To keep a configuration made in the Ghostship menu, disable **AUTOCONFIGURE CONTROLLERS**.

### N64 controllers

RetroBat recognizes the Nintendo Switch Online N64 controller and the Mayflash and Raphnet N64 adapters, and gives them a dedicated configuration.

{% hint style="info" %}
With the Mayflash adapter, plug the controllers in reverse order: player 1 is the controller plugged into the last port of the adapter.
{% endhint %}

For more details, see the [**Special controllers**](../../../../controllers/supported-controllers/gamepads/special-controllers.md) page.

### Hotkeys

<table><thead><tr><th width="225.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td><strong>SELECT</strong></td><td>Open / close the Ghostship menu</td></tr></tbody></table>

On the keyboard:

<table><thead><tr><th width="171.5">Key</th><th>Action</th></tr></thead><tbody><tr><td><strong>Esc</strong></td><td>Open / close the menu</td></tr><tr><td><strong>F11</strong></td><td>Fullscreen</td></tr><tr><td><strong>Tab</strong></td><td>Toggle custom textures</td></tr><tr><td><strong>Ctrl + R</strong></td><td>Reset (inside a level)</td></tr></tbody></table>

While the menu is open, the controller moves through it: D-pad to choose, SOUTH to confirm, EAST to go back. The game no longer receives the controller inputs while the menu is shown.

## Folders

<table><thead><tr><th width="262.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Saves</td><td><code>emulators\ghostship\saves</code></td></tr><tr><td>Extracted game data</td><td><code>emulators\ghostship\sm64.o2r</code></td></tr><tr><td>Mods and texture packs</td><td><code>emulators\ghostship\mods</code></td></tr><tr><td>Configuration</td><td><code>emulators\ghostship\ghostship.cfg.json</code></td></tr></tbody></table>

## Guides

### First launch

On the first launch, RetroBat passes the ROM to Ghostship, which extracts its data to `sm64.o2r` and then starts the game. The extraction takes a few minutes. The next launches start directly.

After a Ghostship update that changes the data format, RetroBat deletes the old archive and Ghostship extracts the data again.

### Mods and texture packs

Place the mods (`.o2r` or `.otr` files: textures, models, music) in `emulators\ghostship\mods`, then start the game. The **Mods** section of the Ghostship menu manages them. **Tab** toggles the custom textures in game.

### Other useful options

<table><thead><tr><th width="336.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Rendering resolution, from <strong>240p (NATIVE)</strong> to <strong>2160p (4K)</strong>. Default: <strong>720p</strong>.</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>By default, the picture fills the screen. <strong>NATIVE (4:3)</strong> keeps the original proportions, <strong>WIDESCREEN (16:9)</strong>, <strong>3DS (5:3)</strong>, <strong>16:10</strong> or <strong>ULTRAWIDE (21:9)</strong> widen the field of view.</td></tr><tr><td><strong>DECORATIONS</strong></td><td>Decorations are only shown with <strong>GAME ASPECT RATIO</strong> set to <strong>NATIVE (4:3)</strong>.</td></tr><tr><td><strong>INTEGER SCALING</strong></td><td>Scales the picture by whole numbers only, for sharp pixels.</td></tr><tr><td><strong>VERTICAL SYNC</strong></td><td>On by default.</td></tr><tr><td><strong>VISUAL RENDERING > TARGET FPS</strong></td><td>Frame rate, from 30 (original rate) to 360 fps. In-between frames are interpolated. By default, the game follows the display refresh rate (60 Hz, 144 Hz…).</td></tr><tr><td><strong>VISUAL RENDERING > TEXTURE FILTERING</strong></td><td><strong>LINEAR</strong> (default), <strong>THREE POINT</strong> (like the N64) or <strong>NONE</strong>.</td></tr><tr><td><strong>VISUAL RENDERING > ANTI-ALIASING (MSAA)</strong></td><td>Smooths polygon edges (1 to 8).</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td><strong>OPENGL</strong> (default), <strong>DIRECTX 11</strong> or <strong>VULKAN</strong>.</td></tr><tr><td><strong>DRIVERS > AUDIO</strong></td><td><strong>WASAPI</strong> (default) or <strong>SDL</strong>.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="339">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Ghostship says the ROM is not supported</td><td>Only the US and Japanese versions are accepted, in <code>.z64</code> format: check the ROM SHA-1 (see <strong>Which game format should I use?</strong>).</td></tr><tr><td>The Ghostship menu opens during the game</td><td><strong>SELECT</strong> opens the menu: press <strong>SELECT</strong> again to close it.</td></tr><tr><td>Black screen or crash at launch</td><td>Change the video driver with <strong>DRIVERS > VIDEO</strong> (<strong>DIRECTX 11</strong> or <strong>VULKAN</strong>).</td></tr><tr><td>Decorations are not shown</td><td>Set <strong>GAME ASPECT RATIO</strong> to <strong>NATIVE (4:3)</strong>.</td></tr><tr><td>A mod does not show</td><td>Check that it is in <code>emulators\ghostship\mods</code> and made for the shipped Ghostship version; press <strong>Tab</strong> to enable custom textures.</td></tr></tbody></table>
