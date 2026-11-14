---
description: Sony
---

# PlayStation Vita

<div align="left"><figure><img src="../../../../.gitbook/assets/image.png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **PlayStation Vita** was released in December 2011 in Japan, then in February 2012 in Europe and North America. It succeeded the PSP with a large OLED touchscreen, a rear touch pad, two analog sticks, a gyroscope and two cameras.

In 2013 Sony released a slimmer model with an LCD screen, then the **PlayStation TV**, a small home console that plays Vita games on a TV with a DualShock controller. Production ended in 2019. The console is home to games such as Uncharted: Golden Abyss, Gravity Rush, Persona 4 Golden, Tearaway or WipEout 2048, and to many indie games.

**Vita3K**, the emulator provided by RetroBat, is the first PS Vita emulator able to run commercial games. It is improving quickly, but compatibility varies a lot from one game to another.

{% embed url="https://en.wikipedia.org/wiki/PlayStation_Vita" %}

## At a glance

<table><thead><tr><th width="237.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\psvita</code></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .psvita .vpk .zip .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>vita3k</td></tr><tr><td><strong>BIOS</strong></td><td>PS Vita firmware to install in Vita3K (automatic from <code>bios\vita3k</code>, see BIOS)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, handled by Vita3K</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

Vita3K is the only PS Vita emulator in RetroBat.

| Emulator             | Strengths                                                                                                          | Limitations                                                                |
| -------------------- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| **vita3k** (default) | Runs many commercial games and homebrews, upscaling, custom textures, cheats, PlayStation TV mode for multiplayer. | Young emulator: many games still have bugs or do not boot. No save states. |

The Vita3K compatibility list ([vita3k.org](https://vita3k.orghttps/vita3k.org/compatibility)) shows the status of each game.

## BIOS

Vita3K needs the PS Vita **firmware**. It comes in three packages, all provided by Sony:

| File                    | Content                       | Use                                                    |
| ----------------------- | ----------------------------- | ------------------------------------------------------ |
| `PSP2UPDAT.PUP`         | Console firmware              | Needed by most games                                   |
| `PSP2UPDAT_FONT.PUP`    | System fonts                  | Recommended: without it, text is missing in some games |
| `PSP2UPDAT_PREINST.PUP` | Console pre-installed content | Optional                                               |

The three files are downloaded under the same name (`PSP2UPDAT.PUP`): rename them as shown in the table. The names `font_fresh.pup` and `preinst_fresh.pup` are also accepted for the fonts and the pre-installed content.

RetroBat checks these three files as optional BIOS: once the firmware is installed, they are no longer needed.

The firmware is not read from the `bios` folder: it has to be **installed** in the Vita3K data folder. RetroBat takes care of it:

1. Download the firmware from the PlayStation website ("PS Vita System Software Update" page). The links to the fonts and the pre-installed content are given in the Vita3K welcome window (**Help > View Welcome Dialog**).
2. Rename the files and place them in `bios\vita3k`.
3. Launch a game: RetroBat installs the missing packages before starting the game. A window shows the installation in progress.

The installation only happens once. The files in `bios\vita3k` can then be kept for a reinstallation.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (556).png" alt=""><figcaption></figcaption></figure></div>

### Installing the firmware from Vita3K

You can also install the firmware from the Vita3K interface:

1. Launch a game once from RetroBat, then quit it: this way Vita3K stores the RetroBat data folder.
2. Open Vita3K from the RetroBat emulators menu.
3. Select **File > Install Firmware (.PUP)** and install each `.PUP` file one after the other.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (555).png" alt=""><figcaption></figcaption></figure></div>

If you open Vita3K without ever launching a game, it offers its own data folder (in the Windows `AppData` folder): firmware installed there is not seen by RetroBat.

## Which game format should I use?

PS Vita games have to be **installed** in Vita3K before they can be launched. RetroBat installs packages and folders automatically at the first launch.

<table><thead><tr><th width="153.25">Format</th><th width="245.75">Installation</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.vpk</strong></td><td>Automatic at the first launch</td><td>Game or homebrew package.</td></tr><tr><td><strong>.zip</strong></td><td>Automatic at the first launch</td><td>Compressed decrypted game (NoNpDrm dump for instance).</td></tr><tr><td><strong><code>.psvita</code> folder</strong></td><td>Automatic at the first launch</td><td>The game folder, which contains <code>eboot.bin</code> and <code>sce_sys</code>, renamed with <code>.psvita</code> at the end.</td></tr><tr><td>.m3u</td><td>Game already installed</td><td>Text file that contains the game ID (see <a href="psvita.md#using-an-.m3u-file">Guides</a>).</td></tr><tr><td><code>.psvita</code> file</td><td>Game already installed</td><td>Empty file whose name contains the game ID between square brackets: <code>WipEout 2048 [PCSA00029].psvita</code>.</td></tr><tr><td>.decomp</td><td>—</td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

RetroBat reads the game ID (for instance `PCSE00000`) in the `param.sfo` file of the package or folder. If it is not found, it looks for it between square brackets in the file name: `Street Fighter X Tekken [PCSE00005].vpk`.

`.pkg` files are not launched by RetroBat: install them from Vita3K (**File > Install Package (.pkg)**), with their license (zRIF), then use an `.m3u` file.

## Controls

### Automatic configuration

RetroBat does not configure the controller buttons: Vita3K detects the controllers itself and applies its default layout at each launch. Xbox, DualShock 4 and DualSense controllers work without any setting.

| PS Vita       | Controller    |
| ------------- | ------------- |
| Cross         | SOUTH         |
| Circle        | EAST          |
| Square        | WEST          |
| Triangle      | NORTH         |
| L, R          | L1, R1        |
| SELECT, START | SELECT, START |
| D-pad, sticks | D-pad, sticks |
| PS button     | GUIDE         |

* The L2, R2, L3 and R3 buttons and rumble only exist on the PlayStation TV: they only work with the **CONTROLS > PLAYSTATION TV MODE** option.
* The gyroscope of compatible controllers (DualShock 4, DualSense…) is used by the games that need it.
* The **EMULATION > CONFIRM BUTTON** option selects the button used to confirm in system menus: **CROSS** (default) or **CIRCLE** (Japanese convention).

### Touchscreen and touch pad

| Action                 | Mouse       | DualShock 4 / DualSense controller  |
| ---------------------- | ----------- | ----------------------------------- |
| Touch the front screen | Left click  | Touch pad                           |
| Touch the rear pad     | Right click | Touch pad, after a press on the pad |

For the controller touch pad, pressing the pad (or the T key on the keyboard) switches from the front screen to the rear pad, and back.

### Keyboard

On the keyboard, Vita3K uses these default keys:

| PS Vita                         | Keyboard           |
| ------------------------------- | ------------------ |
| Left stick                      | W, A, S, D         |
| Right stick                     | I, J, K, L         |
| D-pad                           | Arrow keys         |
| Triangle, Circle, Cross, Square | V, C, X, Z         |
| L, R                            | Q, E               |
| SELECT, START                   | Right SHIFT, ENTER |
| PS button                       | P                  |

Keys can be changed in Vita3K (**Settings > Controls**, **Keyboard** category).

### Hotkeys

| Hotkey             | Action                                   | Keyboard |
| ------------------ | ---------------------------------------- | -------- |
| **HOTKEY + START** | Quit                                     | ESC      |
| —                  | Fullscreen                               | F11      |
| —                  | Switch between front screen and rear pad | T        |

Screenshots have no default key: one can be added in Vita3K (**Settings > Controls**, **Hotkeys** category), as well as for texture replacement.

## Folders

| Content                                          | Folder                                                             |
| ------------------------------------------------ | ------------------------------------------------------------------ |
| Vita3K data folder (pref-path)                   | `saves\psvita\vita3k`                                              |
| Installed games                                  | `saves\psvita\vita3k\ux0\app\<game ID>`                            |
| Installed updates and downloadable content (DLC) | `saves\psvita\vita3k\ux0\patch`, `saves\psvita\vita3k\ux0\addcont` |
| Game saves                                       | `saves\psvita\vita3k\ux0\user\00\savedata`                         |
| Firmware files to install                        | `bios\vita3k`                                                      |
| Vita3K configuration                             | `emulators\vita3k\config.yml`                                      |
| Vita3K per-game configurations                   | `emulators\vita3k\config`                                          |
| Custom textures                                  | `emulators\vita3k\textures\import\<game ID>`                       |
| Cheats                                           | `emulators\vita3k\cheats`                                          |
| Patches                                          | `emulators\vita3k\patch`                                           |
| Screenshots                                      | `emulators\vita3k\screenshots`                                     |

The data folder can be moved with the **EMULATION > CHANGE PREF-PATH** option. It contains the installed games: make sure there is enough space.

**Vita3K portable mode**: if a non-empty `portable` folder is next to `Vita3K.exe`, Vita3K stores everything in it (configuration, data in `portable\fs`, cheats, screenshots…) and the CHANGE PREF-PATH option is ignored. An empty `portable` folder is removed by RetroBat.

## Guides

### Adding a game

1. Copy the `.vpk` or `.zip` file, or the game folder renamed to `.psvita`, to `roms\psvita`.
2. Update the RetroBat game list.
3. Launch the game. At the first launch, RetroBat has Vita3K install the game: a window shows the progress, then the game starts. Next launches are direct.

Once the game is installed, the package is no longer used. To save space, you can replace it with an `.m3u` file.

### Using an .m3u file

The `.m3u` file launches a game already installed in Vita3K. In `roms\psvita`, create a text file named after the game, for instance `WipEout 2048.m3u`, that only contains the game ID:

```
PCSA00029
```

The game ID is shown in the Vita3K game list. It is also the name of the game folder in `saves\psvita\vita3k\ux0\app`.

### Updates and DLC

Updates and downloadable content are installed from Vita3K (**File > Install Archive (.zip / .vpk / .vci)** or **File > Install Package (.pkg)**). Open Vita3K from the RetroBat emulators menu.

### Multiplayer

The **CONTROLS > PLAYSTATION TV MODE** option emulates a PlayStation TV, which accepts up to 4 controllers for local multiplayer games. It also enables L2, R2, L3, R3 and rumble. Games that require the touchscreen may not work in this mode.

### Custom textures

Vita3K can replace the textures of a game with high-definition textures.

1. Place the texture pack in `emulators\vita3k\textures\import`, in a folder named after the game ID (for instance `import\PCSA00029`).
2. Enable the **VISUAL RENDERING > CUSTOM TEXTURES** option.

### Cheats

Vita3K reads the code databases of the FinalCheat / VitaCheat plugins (`.psv` files).

1. Place the code file in `emulators\vita3k\cheats`, named after the game ID (for instance `PCSA00147.psv`).
2. Open Vita3K from the RetroBat emulators menu, then **Manage > Cheats**.
3. Tick the codes to enable and click **Save**: they will be active the next time the game is launched.

The **EMULATION > ENABLE CHEATS** option, on by default, disables all codes without unticking them.

### Vita3K per-game settings

Vita3K can save settings for each game. By default, RetroBat ignores them and applies its own settings. The **EMULATION > USE VITA3K PER-GAME CONFIG** option uses the Vita3K per-game settings, which then take priority over the RetroBat ones.

### Other useful options

| Option                                  | Effect                                                                                                                                   |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **INTERNAL RESOLUTION**                 | Increases the rendering resolution (up to 8X). Native resolution is 960x544.                                                             |
| **EMULATION > LANGUAGE**                | Language of the emulated console. By default, it is the RetroBat language.                                                               |
| **EMULATION > FPS HACK**                | Runs some 30 fps games at 60 fps.                                                                                                        |
| **VIDEO > MEMORY MAPPING**              | Vulkan only. Improves performance and fixes many graphical issues, but may be unstable on some GPUs.                                     |
| **VIDEO > RENDERER ACCURACY**           | **HIGH** (default) or **STANDARD**, faster but less accurate.                                                                            |
| **DRIVERS > VIDEO**                     | Vulkan (default) or OpenGL.                                                                                                              |
| **AUDIO > NGS AUDIO SUPPORT**           | Audio library used by many games. Disable only if a game crashes or has audio issues.                                                    |
| **MODULES > MODULES MANAGEMENT METHOD** | **AUTOMATIC** lets Vita3K choose the firmware modules to load (recommended). **EMULATOR SETTINGS** keeps the modules selected in Vita3K. |

## Known issues

<table><thead><tr><th width="316.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>"PS Vita game … is not installed in Vita3K" message</td><td>The <code>.m3u</code> or <code>.psvita</code> file points to a game that is not installed. Check the game ID, or launch the <code>.vpk</code> / <code>.zip</code> package of the game once to install it.</td></tr><tr><td>The first launch of a game seems stuck</td><td>Vita3K is installing the game: wait for the progress bar to finish. Large games can take several minutes.</td></tr><tr><td>Missing text or squares instead of letters</td><td>The font package is not installed: add <code>PSP2UPDAT_FONT.PUP</code> to <code>bios\vita3k</code> (see BIOS).</td></tr><tr><td>The game does not boot or crashes</td><td>Check its status in the Vita3K compatibility list and that the firmware is installed. Try another <strong>MEMORY MAPPING</strong> method or video driver.</td></tr><tr><td>Black screen with OpenGL on an AMD integrated GPU</td><td>Enable <strong>VIDEO > DISABLE MASK BIT (OPENGL)</strong>.</td></tr><tr><td>Buttons changed in Vita3K go back to their default value</td><td>RetroBat resets the controller buttons at each launch. Keyboard keys are kept.</td></tr><tr><td>Two identical controllers do not work in PlayStation TV mode</td><td>Vita3K limitation: use controllers of different models.</td></tr><tr><td>My RetroBat settings are not applied to a game</td><td>A Vita3K per-game setting is used: disable <strong>USE VITA3K PER-GAME CONFIG</strong>.</td></tr></tbody></table>
