# Starship

<div align="left"><figure><img src="../../../../.gitbook/assets/image (615).png" alt="" width="563"><figcaption></figcaption></figure></div>

Game engine to play Star Fox 64.

{% embed url="https://github.com/HarbourMasters/Starship" %}

## At a glance

<table><thead><tr><th width="232.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\starship</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64</td></tr><tr><td><strong>Default emulator</strong></td><td>starship</td></tr><tr><td><strong>BIOS</strong></td><td>None (game ROM required)</td></tr><tr><td><strong>Controller setup</strong></td><td>No (Starship configuration)</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## BIOS

No BIOS is required.

## Which game format should I use?

Starship only reads ROMs in **.z64** format. A `.n64` or `.v64` ROM must first be converted to `.z64` (for example with the hack64.net online tool).

{% embed url="https://hack64.net/tools/swapper.php" %}

Supported versions:

<table><thead><tr><th width="265.25">Version</th><th>Use</th></tr></thead><tbody><tr><td>Nintendo 64 USA 1.0 and 1.1</td><td>Full game</td></tr><tr><td>Nintendo 64 Japan 1.0</td><td>Japanese voices only</td></tr><tr><td>Nintendo 64 Europe 1.0</td><td>European ("Lylat") voices only</td></tr></tbody></table>

A US version is required to play. The Japanese and European versions are only used to replace the voices (see [**Guides**](starship.md#japanese-or-european-voices)).

One entry is enough in `roms\starship`: once the data is extracted, the ROM is no longer read.

## Controls

### Controller setup

RetroBat does not set up the controller: Starship uses its own default configuration, which follows the button positions.

<table><thead><tr><th width="275.25">RetroBat controller</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Left stick</td><td>Stick</td></tr><tr><td>SOUTH</td><td>A</td></tr><tr><td>WEST</td><td>B</td></tr><tr><td>NORTH or R2</td><td>C left</td></tr><tr><td>EAST or L2</td><td>C down</td></tr><tr><td>Right stick (up / right)</td><td>C up / C right</td></tr><tr><td>L1</td><td>Z</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>Open / close the Starship menu bar</td></tr></tbody></table>

To change the buttons, use **Settings > Controller > Controller Mapping** in the Starship menu bar: the configuration is kept.

**CONTROLS > INVERT Y AXIS** inverts the vertical axis when flying.

While the menu bar is open, the controller moves through it: D-pad to choose, SOUTH to confirm. The game no longer receives the controller inputs while the menu bar is shown.

### Hotkeys

<table><thead><tr><th width="222.75">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td><strong>SELECT</strong></td><td>Open / close the Starship menu bar</td></tr></tbody></table>

On the keyboard:

<table><thead><tr><th width="151.5">Key</th><th>Action</th></tr></thead><tbody><tr><td><strong>F1</strong></td><td>Open / close the menu bar</td></tr><tr><td><strong>F4</strong></td><td>Reset the game</td></tr><tr><td><strong>F11</strong></td><td>Fullscreen</td></tr><tr><td><strong>Tab</strong></td><td>Toggle custom textures</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="260.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Save</td><td><code>emulators\starship\default.sav</code></td></tr><tr><td>Extracted game data</td><td><code>emulators\starship\sf64.o2r</code></td></tr><tr><td>Mods and texture packs</td><td><code>emulators\starship\mods</code></td></tr><tr><td>Configuration</td><td><code>emulators\starship\starship.cfg.json</code></td></tr></tbody></table>

## Guides

### First launch

Starship does not take the ROM as an argument: RetroBat copies it to `emulators\starship`, then Starship guides the extraction.

1. At the **Please provide a Starfox 64 ROM** question, answer **Yes**.
2. In the window that opens (already in `emulators\starship`), choose the ROM, then confirm the extraction start message.
3. The extraction takes a few minutes. At the **ROM Extracted. Extract another?** question, answer **No** (or **Yes** to add the Japanese or European voices right away).

The next launches start directly.

### Japanese or European voices

With a Japanese or European ROM, Starship can replace the game voices: use **Settings > Language > Install JP/EU Audio** in the menu bar (Starship closes, the voices are used from the next launch), or answer **Yes** to **Extract another?** on the first launch. Then choose the voice language in **Settings > Language > Voices**.

### Mods and texture packs

Place the mods (`.o2r` or `.otr` files: textures, models, music) in `emulators\starship\mods`, then start the game. **Tab** toggles the custom textures in game.

### Other useful options

<table><thead><tr><th width="341.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Rendering resolution, from <strong>240p (NATIVE)</strong> to <strong>2160p (4K)</strong>. Default: <strong>720p</strong>.</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>By default, the picture fills the screen. <strong>NATIVE (4:3)</strong> keeps the original proportions, <strong>WIDESCREEN (16:9)</strong>, <strong>3DS (5:3)</strong>, <strong>16:10</strong> or <strong>ULTRAWIDE (21:9)</strong> widen the field of view.</td></tr><tr><td><strong>DECORATIONS</strong></td><td>Decorations are only shown with <strong>GAME ASPECT RATIO</strong> set to <strong>NATIVE (4:3)</strong>.</td></tr><tr><td><strong>INTEGER SCALING</strong></td><td>Scales the picture by whole numbers only, for sharp pixels.</td></tr><tr><td><strong>VERTICAL SYNC</strong></td><td>On by default.</td></tr><tr><td><strong>VISUAL RENDERING > TARGET FPS</strong></td><td>Frame rate, from 30 (original rate) to 360 fps. In-between frames are interpolated. By default, the game follows the display refresh rate (60 Hz, 144 Hz…).</td></tr><tr><td><strong>VISUAL RENDERING > TEXTURE FILTERING</strong></td><td><strong>LINEAR</strong> (default), <strong>THREE POINT</strong> (like the N64) or <strong>NONE</strong>.</td></tr><tr><td><strong>VISUAL RENDERING > ANTI-ALIASING (MSAA)</strong></td><td>Smooths polygon edges (1 to 8).</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td><strong>OPENGL</strong> (default) or <strong>DIRECTX</strong>.</td></tr><tr><td><strong>DRIVERS > AUDIO</strong></td><td><strong>WASAPI</strong> (default) or <strong>SDL</strong>.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="314">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Starship asks for a ROM at each launch</td><td>The extraction did not succeed: choose a US ROM in <code>.z64</code> format (see <a href="starship.md#which-game-format-should-i-use"><strong>Which game format should I use?</strong></a>).</td></tr><tr><td>"Unsupported ROM"</td><td>The ROM is not in the list of supported versions, or is not in <code>.z64</code> format.</td></tr><tr><td>A console window opens with the game</td><td>It is part of Starship: do not close it, that would also close the game.</td></tr><tr><td>The buttons do not suit you</td><td>RetroBat does not set up the Starship controller: change them in <strong>Settings > Controller > Controller Mapping</strong>.</td></tr><tr><td>Black screen or crash at launch</td><td>Set <strong>DRIVERS > VIDEO</strong> to <strong>DIRECTX</strong>.</td></tr><tr><td>Decorations are not shown</td><td>Set <strong>GAME ASPECT RATIO</strong> to <strong>NATIVE (4:3)</strong>.</td></tr><tr><td>A mod does not show</td><td>Check that it is in <code>emulators\starship\mods</code> and made for the shipped Starship version; press <strong>Tab</strong> to enable custom textures.</td></tr></tbody></table>
