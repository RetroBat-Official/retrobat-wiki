---
description: Nintendo
---

# GameCube

<div align="left"><figure><img src="../../../../.gitbook/assets/image (482).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **GameCube** is Nintendo's fourth home console, after the Nintendo 64. It launched in Japan in September 2001, in North America in November 2001 and in Europe in May 2002. Compact, with its carrying handle and bright colors ("indigo" purple, black, orange…), it stood apart from its rivals, the PlayStation 2 and the Xbox.

It reads 1.5 GB **mini-DVDs**, a Nintendo-specific format, and is built around an IBM PowerPC processor ("Gekko") and an ATI graphics chip ("Flipper"). Its controller, with its big central A button and analog triggers, remains a reference, especially for Super Smash Bros. A link cable connects it to a **Game Boy Advance**, used as a controller or second screen in some games, and the Game Boy Player add-on plays Game Boy games.

About 21 million units were sold, until 2007. Its library has many classics: Super Smash Bros. Melee, Metroid Prime, The Legend of Zelda: The Wind Waker, Super Mario Sunshine, Mario Kart: Double Dash!!, Resident Evil 4, F-Zero GX, Pikmin, Luigi's Mansion, Animal Crossing, Paper Mario: The Thousand-Year Door, Eternal Darkness…

{% embed url="https://en.wikipedia.org/wiki/GameCube" %}

## At a glance

|                              |                                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------- |
| **Games folder**             | `roms\gamecube`                                                                 |
| **Extensions**               | .dol .gcz .iso .ciso .wbfs .wad .rvz .wia .m3u .zip .7z .squashfs .json .decomp |
| **Default emulator**         | dolphin                                                                         |
| **BIOS**                     | None required (IPL optional)                                                    |
| **Controller configuration** | Automatic, all emulators                                                        |
| **Save states**              | libretro cores, Dolphin                                                         |
| **RetroAchievements**        | libretro cores, Dolphin                                                         |
| **Netplay**                  | No                                                                              |

## Which emulator should I choose?

| Emulator              | For whom?       | Strengths                                                                                                                                                             | Limits                                                                                |
| --------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **dolphin** (default) | Everyone        | The most compatible and complete: HD, widescreen, texture packs, modified games (Riivolution), GameCube adapter, Game Boy Advance link, per-game controller profiles. | —                                                                                     |
| **lr-dolphin**        | RetroArch users | RetroArch features (shaders, RetroArch menu).                                                                                                                         | Based on an older Dolphin version, less compatible. Doesn't read .zip, .7z and .json. |

**When in doubt, keep dolphin.**

## BIOS

No BIOS is needed: Dolphin runs games without one. The GameCube BIOS (`IPL.bin` file) is **optional**. It shows the console boot animation and improves font rendering in some games.

| Region | File      | MD5                              | Location (Dolphin)                  |
| ------ | --------- | -------------------------------- | ----------------------------------- |
| Europe | `IPL.bin` | 0cdda509e2da83c85bfe423dd87346cc | `emulators\dolphin-emu\User\GC\EUR` |
| USA    | `IPL.bin` | 019e39822a9ca3029124f74dd4d55ac4 | `emulators\dolphin-emu\User\GC\USA` |
| Japan  | `IPL.bin` | fc924a7c879b661abc37cec4f018fdf3 | `emulators\dolphin-emu\User\GC\JAP` |

* For lr-dolphin, put the file in `saves\gamecube\dolphin-emu\User\GC\<region>`.
* RetroBat doesn't check for the IPL, since it isn't required.
* To see the boot animation, turn off **SKIP BIOS** in the system or game options.
* The **Game Boy Advance link** (see [Guides](gamecube.md#guides)) uses the GBA BIOS: `bios\gba_bios.bin`.

### Changing the game language

In the system or game advanced options (Dolphin), set **EMULATION > LANGUAGE**: English, German, French, Spanish, Italian or Dutch.

Only **European (PAL)** games use it: US and Japanese games stay in their original language.

## Which game format?

<table><thead><tr><th width="197.75">Format</th><th width="122.75">dolphin</th><th width="106">lr-dolphin</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.iso</strong> (recommended)</td><td>✔</td><td>✔</td><td>Uncompressed disc image (1.4 GB).</td></tr><tr><td><strong>.rvz</strong> (recommended)</td><td>✔</td><td>✔</td><td>Dolphin's lossless compressed format: games 30 to 70% smaller.</td></tr><tr><td>.gcz / .wia / .ciso</td><td>✔</td><td>✔</td><td>Older compressed formats.</td></tr><tr><td>.zip / .7z / .squashfs</td><td>✔ (extracted at launch)</td><td>✘</td><td>Slower loading.</td></tr><tr><td>.m3u</td><td>✔</td><td>✔</td><td>Multi-disc games (<a href="gamecube.md#multi-disc-games">see below</a>).</td></tr><tr><td>.dol</td><td>✔</td><td>✔</td><td>Homebrew programs.</td></tr><tr><td>.json</td><td>✔</td><td>✘</td><td>Games modified with Riivolution patches (<a href="gamecube.md#modified-games-riivolution-patches-.json-files">see Guides</a>).</td></tr></tbody></table>

* To convert a game to .rvz, open Dolphin (`emulators\dolphin-emu\Dolphin.exe`), right-click the game, choose **Convert File…** and pick the **RVZ** format.
* .wbfs and .wad are **Wii** formats: those games go in `roms\wii`.

### Multi-disc games

A few games span two discs (Resident Evil 4, Metal Gear Solid: The Twin Snakes, Baten Kaitos, Tales of Symphonia…). Create a text file with the **.m3u** extension that lists the discs, one per line:

```
Tales of Symphonia (Disc 1).rvz
Tales of Symphonia (Disc 2).rvz
```

Dolphin swaps discs on its own when the game asks for it. You can also do it with **HOTKEY + L2**.

## Controls

### Automatic configuration

RetroBat configures your controllers automatically, for Dolphin and lr-dolphin, up to 4 players. Supported: XInput controllers (Xbox…), DualShock 4, DualSense, Switch Pro, most SDL controllers, and **real GameCube controllers** connected through an adapter ([see below](gamecube.md#using-a-real-gamecube-controller-adapter)).

<table><thead><tr><th width="230.25">RetroBat controller</th><th>GameCube controller</th></tr></thead><tbody><tr><td>Face buttons</td><td>A / B / X / Y (depending on the selected layout, <a href="gamecube.md#button-layout">see below</a>)</td></tr><tr><td>R1</td><td>Z</td></tr><tr><td>L2 / R2</td><td>L / R triggers</td></tr><tr><td>Left stick</td><td>Main stick</td></tr><tr><td>Right stick</td><td>C-stick</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

### Button layout

On the GameCube controller, the big **A** button is in the middle, **B** on the left, **X** on the right and **Y** on top. The **CONTROLS > FACE BUTTON LAYOUT** option sets how they are placed on your controller:

<table><thead><tr><th width="209.75">Layout</th><th width="109.25">SOUTH</th><th width="103.75">EAST</th><th width="115">WEST</th><th width="99">NORTH</th></tr></thead><tbody><tr><td><strong>NINTENDO</strong> (default)</td><td>B</td><td>A</td><td>Y</td><td>X</td></tr><tr><td><strong>POSITIONAL</strong></td><td>A</td><td>X</td><td>B</td><td>Y</td></tr><tr><td><strong>XBOX</strong></td><td>A</td><td>B</td><td>X</td><td>Y</td></tr><tr><td><strong>MIX (A/B NINTENDO)</strong></td><td>B</td><td>A</td><td>X</td><td>Y</td></tr></tbody></table>

* **NINTENDO**: letters match a Nintendo controller (Switch Pro…).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (483).png" alt="" width="225"><figcaption></figcaption></figure></div>

* **POSITIONAL**: matches the button positions of the GameCube controller.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (484).png" alt="" width="225"><figcaption></figcaption></figure></div>

* **XBOX**: letters match an Xbox controller.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (485).png" alt="" width="225"><figcaption></figcaption></figure></div>

* **MIX**: A/B match an Xbox controller, X/Y match a Nintendo controller.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (486).png" alt="" width="225"><figcaption></figcaption></figure></div>

### Using a real GameCube controller (adapter)

Dolphin can use a real GameCube controller through a USB adapter (official Nintendo WUP-028, Mayflash…). The **Zadig** driver must be installed first:

1. Download Zadig: [https://zadig.akeo.ie/](https://zadig.akeo.ie/)
2. Run Zadig, open **Options** and check **List All Devices**.
3. Select the adapter in the list (for example **WUP-028**).
4. With the arrows on the right, select the **libusbK** driver.
5. Click **Replace Driver** and wait (up to 5 minutes).
6. In RetroBat, set **CONTROLS > PLAYER 1 CONTROLLER TYPE** (and the following ones) to **GAMECUBE ADAPTER**.

If the adapter doesn't work, Dolphin may not support it.

**Mayflash** and **Raphnet** adapters are also recognized without Zadig: RetroBat configures them as a regular controller. In that case, do **not** set the controller type to **GAMECUBE ADAPTER**.

### Per-game controller profile

To use your own mapping for a specific game, create a profile in Dolphin and assign it to the game: see the [**Dolphin controller mapping** page](../../../../controllers/specific_mapping/dolphin-controller-mapping.md). To configure all controllers yourself, set **AUTOCONFIGURE CONTROLLERS** to **OFF**.

### Hotkeys

**Dolphin** uses the following hotkeys:

| Action                                    | Controller                     |
| ----------------------------------------- | ------------------------------ |
| Quit the game                             | HOTKEY + START                 |
| Pause                                     | HOTKEY + EAST                  |
| Save state (with screenshot) / Load state | HOTKEY + WEST / HOTKEY + NORTH |
| Next / previous state slot                | HOTKEY + UP / HOTKEY + DOWN    |
| Speed up / slow down                      | HOTKEY + RIGHT / HOTKEY + LEFT |
| Change disc / eject                       | HOTKEY + L2 / HOTKEY + L1      |
| Fullscreen                                | HOTKEY + L3                    |

**lr-dolphin** uses the RetroArch hotkeys ([see the Hotkeys page](../../../../navigation/hotkeys.md)).

## Folders

### Saves

On GameCube, games save to a **memory card**. RetroBat creates it for you, one per region:

<table><thead><tr><th width="225.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Dolphin saves</td><td><code>saves\gamecube\dolphin-emu\User\GC\&#x3C;region></code></td></tr><tr><td>lr-dolphin saves</td><td><code>saves\gamecube\dolphin-emu\User\GC\&#x3C;region>\Card A</code></td></tr><tr><td>Dolphin save states</td><td><code>saves\gamecube\dolphin</code></td></tr><tr><td>lr-dolphin save states</td><td><code>saves\gamecube\libretro.dolphin</code></td></tr></tbody></table>

* The region (EUR, USA or JAP) is detected from the game. **EMULATION > SYSTEM REGION** forces a region, for example to find a save made with another region's version.
* By default, each save is a separate file (**GCI** format). **EMULATION > SAVE FORMAT > MEMORY CARD** uses one file per region instead (like a real memory card), stored in `saves\gamecube\dolphin-emu\User\GC`.
* Dolphin and lr-dolphin don't use the same folder. To switch between them without losing your saves, turn on **EMULATION > SYNC SAVES BETWEEN CORE AND STANDALONE**.

### Other useful folders

<table><thead><tr><th width="305.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Dolphin BIOS (<code>IPL.bin</code>)</td><td><code>emulators\dolphin-emu\User\GC\&#x3C;region></code></td></tr><tr><td>lr-dolphin BIOS (<code>IPL.bin</code>)</td><td><code>saves\gamecube\dolphin-emu\User\GC\&#x3C;region></code></td></tr><tr><td>Texture packs</td><td><code>saves\gamecube\dolphin-emu\User\Load\Textures</code></td></tr><tr><td>Riivolution patches</td><td><code>saves\gamecube\dolphin-emu\User\Load\Riivolution</code></td></tr><tr><td>Resource packs</td><td><code>saves\gamecube\dolphin-emu\User\ResourcePacks</code></td></tr><tr><td>Texture and video dumps</td><td><code>saves\gamecube\dolphin-emu\User\Dump</code></td></tr><tr><td>Dolphin controller profiles and settings</td><td><code>emulators\dolphin-emu\User\Config</code></td></tr></tbody></table>

## Guides

### Achievements (RetroAchievements) and .rvz games

Dolphin and lr-dolphin support [RetroAchievements](../../../../advanced-features/retroachievements.md). But RetroBat can't recognize **.rvz** games when it indexes achievements: the trophy icon doesn't show in the game list, even though Dolphin announces achievements at launch.

RetroBat ships a tool that does this indexing instead:

1. Turn on achievements in **MAIN MENU > GAME SETTINGS > RETROACHIEVEMENT SETTINGS**, with your RetroAchievements account.
2. Launch a GameCube game with Dolphin at least once, so it gets installed.
3. **Close RetroBat completely.**
4. Run `system\tools\indexcheevosrvz.bat`.
5. Start RetroBat again: recognized games show the trophy icon.

The tool processes every .rvz file in `roms\gamecube` and `roms\wii`, and stores each game's RetroAchievements ID in the system's `gamelist.xml`. Games already indexed are skipped: run it again after adding new games. A game missing from the RetroAchievements database stays without a trophy.

{% hint style="info" %}
You can also add the ID by hand. It shows in the address bar of the game's page on retroachievements.org (for example 1234 in `retroachievements.org/game/1234`). With RetroBat closed, add the following line to the game's entry in `roms\gamecube\gamelist.xml`:

```
<cheevosId>1234</cheevosId>
```
{% endhint %}

### Custom textures (Dolphin)

HD texture packs exist for many games.

1. Find the game's **Game ID**: in Dolphin, right-click the game, then **Properties** (for example GZLE01 for The Wind Waker US).
2. Copy the pack to `saves\gamecube\dolphin-emu\User\Load\Textures`, in a folder named **exactly** after this Game ID.
3. Turn on **VISUAL RENDERING > CUSTOM TEXTURES** in the game options. **PREFETCH CUSTOM TEXTURES** makes the game smoother, but uses a lot of memory.

### Modified games (Riivolution patches, .json files)

Dolphin can start a game with **Riivolution** patches (translations, mods, fixes…) without changing the game file. Your choices are saved in a **.json** file (a "preset"): placed in `roms\gamecube`, it shows up in RetroBat as a separate game.

1. Launch a GameCube game once from RetroBat with Dolphin, so Dolphin uses the GameCube folders.
2. Copy the mod to `saves\gamecube\dolphin-emu\User\Load\Riivolution`. The mod's **riivolution** folder, which contains the .xml files, must end up in `saves\gamecube\dolphin-emu\User\Load\Riivolution\riivolution`.
3. Open Dolphin (`emulators\dolphin-emu\Dolphin.exe`). Your games show in the list.
4. Right-click the game, then **Start with Riivolution Patches…**.
5. Turn on the mod options, click **Save Preset…** and save the .json file in `roms\gamecube`, with the name to display in RetroBat.
6. Close Dolphin and update the game lists in RetroBat: the modified game appears in the list.

{% hint style="warning" %}
* The .json file stores the full path to the original game and the mod: if you move RetroBat or the game, create the preset again. Don't delete the original game.
* Only **Dolphin** starts .json files, not lr-dolphin.
{% endhint %}

### Game Boy Advance link

Some games use a Game Boy Advance as a controller or second screen (The Legend of Zelda: Four Swords Adventures, Final Fantasy Crystal Chronicles…). Dolphin can emulate the GBA:

1. Put `gba_bios.bin` in the `bios` folder.
2. Set the player's **CONTROLS > CONTROLLER TYPE** to **GBA**.
3. If the game needs a GBA cartridge, select it with **GBA ROM** and **GBA ROM PORT**.

## Known issues

**The trophy icon is missing for a compatible game** The game is in .rvz format: use the indexing tool (see [Guides](gamecube.md#achievements-retroachievements-and-.rvz-games)).

**My saves are gone**

* You switched from Dolphin to lr-dolphin (or the other way round): turn on **SYNC SAVES BETWEEN CORE AND STANDALONE**.
* The game's region differs from your save's: set **SYSTEM REGION** to the save's region.
* You changed the **SAVE FORMAT**: the two formats don't share saves.

**lr-dolphin doesn't start the game** lr-dolphin doesn't read .zip, .7z or .json games: extract them, or use Dolphin.

**The GameCube adapter doesn't respond** Check that the Zadig driver (libusbK) is installed and that the controller type is set to **GAMECUBE ADAPTER**. For a Mayflash or Raphnet adapter used without Zadig, the controller type must instead stay at its default.
