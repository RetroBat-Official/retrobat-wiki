# RetroBat Folder Structure

Once RetroBat is installed, the installation folder contains the following folders and files:

<div align="left"><figure><img src="../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Folders marked as "internal" below are managed by RetroBat and may be overwritten during updates. Store your own files in the folders intended for them (`decorations`, `user`, etc.).
{% endhint %}

## bios folder

This is where BIOS and firmware files must be placed for all systems, with a few exceptions.

{% hint style="info" %}
Unless specified otherwise, BIOS files go directly at the root of the `bios` folder. Some emulators use their own subfolder (for example `bios\pcsx2\bios`, `bios\dc`, `bios\mame`…): these subfolders are created by the installer.

The required BIOS files and their location are listed on each system's page in the [Supported Game Systems](../systems-and-emulators/supported-game-systems/) section. See also [Adding BIOS files](adding-bios-files.md).
{% endhint %}

## cheats folder

This folder stores the cheat files used by emulators that support cheats, when the "cheats" feature is enabled. It contains one subfolder per emulator (`retroarch`, `pcsx2`, `duckstation`, `mame`…).

## decorations folder

This folder is empty after installation. Use it to add your own bezels: they will be available in RetroBat in addition to the default bezels located in `system\decorations`.

## emulationstation folder

This folder contains the executables of the RetroBat interface (EmulationStation) and of emulatorLauncher, the program that configures and starts the emulators. The structure is the following:

<div align="left"><figure><img src="../.gitbook/assets/image (217).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
The RetroBat configuration files (`es_settings.cfg`, `es_input.cfg`, `es_systems.cfg`…) and the log files are located in this folder and its `.emulationstation` subfolder.
{% endhint %}

### .emulationstation subfolder

#### collections

This folder is created by EmulationStation when you create your first [editable game collection](../navigation/game-collections.md#editable-game-collections). Each collection is stored in a `.cfg` file named after the collection, which lists the games it contains with their paths.

#### music

Audio files placed in this folder are played as background music in the interface. RetroBat supports `.mp3`, `.ogg`, `.wav` and `.flac` files, as well as some less common formats.

To skip to the next song, press the left stick (`[L3]`), or use the Quick Access menu: in the System View, press `[SELECT]` and choose **SKIP TO THE NEXT SONG**.

<div align="left"><figure><img src="../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure></div>

Songs are played randomly.

You can also play specific music for each system. Create a subfolder named exactly like the system's `roms` folder (for example `music\snes`), and put your audio files in it.

* With the **ONLY PLAY SYSTEM-SPECIFIC MUSIC FOLDER** option **enabled**, RetroBat plays the songs of the system you are browsing (for example `music\3do`) and the songs located directly in `music`, but not the songs of other systems.
* With this option **disabled**, RetroBat randomly plays any song from `music` and all its subfolders.

<div align="left"><figure><img src="../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure></div>

#### scripts

EmulationStation can run your own scripts or programs on certain events. Place them in the subfolder matching the event:

| Subfolder    | Event                                   |
| ------------ | --------------------------------------- |
| `game-start` | A game is launched                      |
| `game-end`   | A game is closed                        |
| `quit`       | RetroBat is closed                      |
| `reboot`     | The computer is restarted from RetroBat |
| `shutdown`   | The computer is shut down from RetroBat |
| `sleep`      | The computer goes to sleep              |
| `wake`       | The computer wakes up                   |

#### themes

Themes downloaded with the **CONTENT DOWNLOADER** are stored in this folder. You can also copy themes here manually.

#### themesettings

This folder stores the per-theme settings. When you customize a theme from the theme menu, its settings are saved here, in a `.cfg` file named after the theme.

#### video

Place videos here to use them as intro ("splash screen") before RetroBat starts. You can easily configure the intro videos with [BatGui](../advanced-features/batgui.md) or in [`retrobat.ini`](../advanced-features/retrobat.ini.md).

## emulators folder

This folder contains the emulators.

RetroArch is provided with RetroBat. All other emulators are downloaded automatically the first time you run a game that needs them, or when you start them from the RetroBat system menu.

{% hint style="info" %}
For legal or technical reasons, some emulators cannot be downloaded automatically by RetroBat. You must download them yourself and place them in the matching folder:

* Switch emulators
* PICO-8
* 3DSen
* TeknoParrot
{% endhint %}

## library folder

Use this folder to store magazines or manuals. They appear in RetroBat in a "Library" system and can be read with the **imageviewer** libretro core.

## records folder

This folder receives the gameplay videos recorded by emulators that support video recording. The videos are saved in `records\output`, the recording settings in `records\config`.

## roms folder

This is where you copy your games. Each game must be placed in the folder of its system (for example `roms\snes`) and have a file extension supported by the emulator. These folders are created by the installer.

More information on each system's page in the [Supported Game Systems](../systems-and-emulators/supported-game-systems/) section, and in [Adding a game](adding-a-game.md).

## saves folder

This folder contains your game saves (in-game saves and save states), organized by system, then by emulator (for example `saves\psx\duckstation`).

## screenshots folder

This folder contains the screenshots taken while playing.

{% hint style="info" %}
If a save or a screenshot is not stored in the right folder, please report it to the RetroBat team so that it can be fixed.
{% endhint %}

## sounds folder

The `sounds\retroachievements` subfolder stores the sounds played when you unlock a RetroAchievement. Files copied there automatically appear as choices in the **UNLOCK SOUND** option of the RetroAchievements settings:

<div align="left"><figure><img src="../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Sound files must be in `.ogg` format and placed in `sounds\retroachievements`, not at the root of `sounds`.
{% endhint %}

## system folder

This folder contains RetroBat configuration files and the default assets provided with RetroBat (bezels, shaders…). The structure is the following:

<div align="left"><figure><img src="../.gitbook/assets/image (221).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
The content of this folder is replaced when RetroBat is updated. Do not modify it: use the `user` and `decorations` folders for your own files.
{% endhint %}

### configgen, download, modules, scripts and tools subfolders

Internal RetroBat files (installation, update and launcher modules, tools used by RetroBat). They do not need to be modified.

### decorations subfolder

The default bezels provided with RetroBat.

### es\_menu subfolder

The shortcuts to the emulators shown in the "RetroBat" system, which lets you open the emulators directly.

### loadingscreens subfolder

This folder is not created by the installer: create it if you want to play a short video (`.mp4`) when a game is launched, instead of the default zoom effect on the game image.

RetroBat looks for the video in this order, and plays the first one it finds:

| File                                     | Played for            |
| ---------------------------------------- | --------------------- |
| `loadingscreens\<system>\<rom name>.mp4` | One specific game     |
| `loadingscreens\<system>\<system>.mp4`   | All games of a system |
| `loadingscreens\<system>.mp4`            | All games of a system |
| `loadingscreens\default.mp4`             | All games             |

For example, `loadingscreens\gamecube.mp4` is played for all GameCube games.

Example videos are provided in `system\templates\loadingscreens`.

### padtokey subfolder

The default [padtokey](../controllers/pad2key.md) files provided with RetroBat.

### resources subfolder

Resources used by RetroBat. The `inputmapping` subfolder contains the files used to configure controls automatically for some emulators or specific controller types.

<div align="left"><figure><img src="../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
These files are overwritten when RetroBat is updated. To keep your modified versions, copy them to the `user\inputmapping` folder.
{% endhint %}

### shaders subfolder

The default shaders (video filters) provided with RetroBat.

### tattoos subfolder

The default controller layout images ("tattoos") for several systems.

### templates subfolder

The original version of RetroBat configuration files, as provided at installation. If a file has been deleted or damaged, you can copy its original version from here to its destination folder.

## user folder

This folder stores your own customization files, which are kept when RetroBat is updated:

<table><thead><tr><th width="154">Subfolder</th><th>Content</th></tr></thead><tbody><tr><td><code>apikey</code></td><td>Your Steam API key (<code>steam.apikey</code> file)</td></tr><tr><td><code>customratio</code></td><td>Custom aspect ratios for libretro cores: <code>&#x3C;system>_customratio.txt</code> (whole system) or <code>&#x3C;system>_&#x3C;rom name>_customratio.txt</code> (one game)</td></tr><tr><td><code>inputmapping</code></td><td>Your modified inputmapping files</td></tr><tr><td><code>padtokey</code></td><td>Your own padtokey files</td></tr><tr><td><code>tattoos</code></td><td>Your own controller layout images (<code>default</code> and <code>games</code> subfolders)</td></tr></tbody></table>
