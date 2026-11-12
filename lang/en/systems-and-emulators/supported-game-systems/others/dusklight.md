# Dusklight

<div align="left"><figure><img src="../../../.gitbook/assets/image (512).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

**Dusklight** is a PC port of **The Legend of Zelda: Twilight Princess**, released in late 2006 on GameCube and Wii. It is not an emulator: the game was rebuilt from the decompilation work on the GameCube version and runs directly on the PC.

The port stays faithful to the original game and adds modern options: high resolution, widescreen, higher frame rate, quality of life enhancements (quick transform, autosave, faster climbing…), gyro aiming, texture packs and mods.

Dusklight contains no game data: you must provide the disc image of your own copy.

{% embed url="https://github.com/TwilitRealm/dusklight" %}

{% embed url="https://twilitrealm.dev/" %}

## At a glance

<table><thead><tr><th width="246.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\dusklight</code></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .iso .rvz</td></tr><tr><td><strong>Default emulator</strong></td><td>dusklight</td></tr><tr><td><strong>BIOS</strong></td><td>None (original game disc image required)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

Dusklight is the only program offered for this system.

To play Twilight Princess with an emulator, see the [**GameCube**](../game-consoles/nintendo-game-consoles/gamecube.md) and [**Wii**](../game-consoles/nintendo-game-consoles/wii.md) pages.

## Recognized game versions

<table><thead><tr><th width="192">Version</th><th width="124.25">ID</th><th>Languages</th></tr></thead><tbody><tr><td>GameCube Europe</td><td>GZ2P01</td><td>English, French, German, Spanish, Italian</td></tr><tr><td>GameCube USA</td><td>GZ2E01</td><td>English</td></tr><tr><td>GameCube Japan</td><td>GZ2J01</td><td>Japanese</td></tr><tr><td>Wii Europe</td><td>RZDP01</td><td>English, French, German, Spanish, Italian</td></tr><tr><td>Wii USA</td><td>RZDE01</td><td>English (and French, Spanish depending on the disc revision)</td></tr><tr><td>Wii Japan</td><td>RZDJ01</td><td>Japanese</td></tr></tbody></table>

The Korean Wii version is not supported.

Even with a Wii disc, Dusklight shows the interface of the GameCube version.

### Game language

The language is set with the **EMULATION > LANGUAGE** option. Available languages depend on the disc: to play in French, German, Spanish or Italian, use a European version.

## Which game format?

<table><thead><tr><th width="161.5">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.rvz</strong></td><td>Compressed image, smaller. Dolphin can convert an <code>.iso</code> to <code>.rvz</code>.</td></tr><tr><td>.iso</td><td>Full image.</td></tr><tr><td>.m3u</td><td>Text file holding the path to the disc image. Avoids copying the game if it is already in <code>roms\gamecube</code> or <code>roms\wii</code> (see <a href="dusklight.md#using-a-game-already-in-gamecube-or-wii">Guides</a>).</td></tr></tbody></table>

## Controls

### Automatic configuration

RetroBat automatically assigns controllers to game ports 1 to 4, following the RetroBat player order. Buttons are the ones defined by Dusklight, depending on the controller type:

| GameCube controller | Xbox controller | Other controllers (PlayStation, Switch Pro…) |
| ------------------- | --------------- | -------------------------------------------- |
| A                   | SOUTH           | SOUTH                                        |
| B                   | WEST            | EAST                                         |
| X                   | EAST            | WEST                                         |
| Y                   | NORTH           | NORTH                                        |
| Z                   | R1              | R1                                           |
| L / R               | L2 / R2         | L2 / R2                                      |
| START               | START           | START                                        |
| Control stick       | Left stick      | Left stick                                   |
| C-stick             | Right stick     | Right stick                                  |
| D-pad               | D-pad           | D-pad                                        |

The **SELECT** button opens the Dusklight menu. There you can change the buttons, manage mods and tune the game. In this menu, **A** confirms and **B** goes back (GameCube buttons from the table).

<div align="left"><figure><img src="../../../.gitbook/assets/image (513).png" alt=""><figcaption></figcaption></figure></div>

Two useful options in **CONTROLS**: **FREE CAMERA** (camera on the right stick) and **GYRO AIM** (aim by moving a DualSense, DualShock 4, Switch Pro… controller).

To keep RetroBat from changing the controller assignment, turn off **AUTOCONFIGURE CONTROLLERS**.

### Hotkeys

<table><thead><tr><th width="249">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td>SELECT or F1</td><td>Dusklight menu</td></tr><tr><td>F11</td><td>Fullscreen / windowed</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="269">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Saves and settings</td><td><code>emulators\dusklight\data</code></td></tr><tr><td>Settings file</td><td><code>emulators\dusklight\data\config.json</code></td></tr><tr><td>Controller to port assignment</td><td><code>emulators\dusklight\data\controller_ports.dat</code></td></tr><tr><td>Mods shared by all games</td><td><code>emulators\dusklight\data\mods</code></td></tr><tr><td>Mods for a single game</td><td><code>roms\dusklight\&#x3C;game name></code> (folder named like the launched file)</td></tr><tr><td>Texture packs</td><td><code>emulators\dusklight\data\texture_replacements</code></td></tr></tbody></table>

## Guides

### Using a game already in GameCube or Wii

There is no need to copy the disc image a second time.

1. In `roms\dusklight`, create a text file, for example `Twilight Princess.m3u`.
2. Write the full path to the disc image in it:

```
D:\RetroBat\roms\gamecube\Zelda Twilight Princess (Europe).rvz
```

3. Launch the `.m3u` file from RetroBat.

### Original game or enhanced game?

The **EMULATION > ENHANCEMENTS** option sets all quality of life enhancements at once:

<table><thead><tr><th width="294">Choice</th><th>Effect</th></tr></thead><tbody><tr><td><strong>DUSKLIGHT (RECOMMENDED)</strong></td><td>Quick transform, bigger wallets, fast climbing, instant saves, autosave, improved maps…</td></tr><tr><td><strong>CLASSIC (GAMECUBE)</strong></td><td>The game behaves as on GameCube.</td></tr><tr><td>Not set</td><td>Settings made in the Dusklight menu are kept.</td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (514).png" alt=""><figcaption></figcaption></figure></div>

The **MIRROR MODE** option flips the world left to right, like in the Wii version.

### Mods

Mods are `.dusk` files. A mod found in the mods folder is loaded and enabled automatically at launch.

**Mods for all games**: copy the `.dusk` files to `emulators\dusklight\data\mods`.

**Mods for a single game**: in `roms\dusklight`, create a folder with the same name as the game file, without the extension, and copy the `.dusk` files into it. When this folder exists, RetroBat only loads the mods it contains.

This lets you have several entries in RetroBat, each with its own mods:

```
roms\dusklight\Twilight Princess.m3u
roms\dusklight\Twilight Princess Rando.m3u
roms\dusklight\Twilight Princess Rando\randomizer.dusk
```

Here, `Twilight Princess` starts with the shared mods and `Twilight Princess Rando` with the mod from its folder.

**Playing without mods**: turn off the **EMULATION > ENABLE MODS** option.

To disable a single mod, or to install one from the catalog, open the Dusklight menu (**SELECT**). A mod installed from this menu goes to the mods folder used by the launched game.

## Known issues

| Issue                                                     | Solution                                                                                                                                                      |
| --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Dusklight doesn't recognize the game                      | Use an unmodified image of one of the recognized versions (see [known versions](dusklight.md#recognized-game-versions)). The Korean Wii version doesn't work. |
| The game is in English, my language is not offered        | The language depends on the disc: use a European version, then pick **LANGUAGE**.                                                                             |
| The `.m3u` file doesn't launch                            | The file must hold the full path to the disc image, on the first line.                                                                                        |
| A menu opens when I press SELECT                          | This is the Dusklight menu. Close it with the GameCube **B** button (see [Controls](dusklight.md#controls)).                                                  |
| The B and X buttons are not where I want them             | Change them in the Dusklight menu (**SELECT**).                                                                                                               |
| A mod stays active although **ENABLE MODS** is turned off | Mods placed in `emulators\dusklight\mods` are always loaded. Move them to `emulators\dusklight\data\mods`.                                                    |
| Black screen or crash at launch                           | Dusklight needs a graphics card supporting Direct3D 12 or Vulkan. Try **DRIVERS > VIDEO**: DIRECT3D 11.                                                       |
