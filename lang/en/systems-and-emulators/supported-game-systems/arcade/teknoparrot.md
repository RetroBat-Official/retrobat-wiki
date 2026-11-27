---
description: TeknoGods
---

# TeknoParrot

<div align="left"><figure><img src="../../../.gitbook/assets/image.png" alt="" width="295"><figcaption></figcaption></figure></div>

## Overview

Since the mid-2000s, many arcade cabinets are actual PCs: Sega Lindbergh, RingEdge and RingWide, Taito Type X, Namco System ES, NesicaxLive, Raw Thrills… **TeknoParrot** runs these games on Windows by emulating the I/O boards (JVS), card readers and cabinet devices: **Mario Kart Arcade GP DX**, **Initial D**, **Wangan Midnight Maximum Tune**, **The House of the Dead 4**, **Tekken 7**, **BlazBlue**, **Street Fighter V Type Arcade**…

TeknoParrot is developed by TeknoGods. Some games and features require a TeknoParrot Patreon subscription (RetroBat does not recommend to subscribe!).

{% embed url="https://teknogods.github.io/index.html" %}

## Quick facts

<table><thead><tr><th width="250.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\teknoparrot</code></td></tr><tr><td><strong>Extensions</strong></td><td>.teknoparrot .parrot .game (folders) .zip .7z .rar</td></tr><tr><td><strong>Default emulator</strong></td><td>teknoparrot</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, per game (<code>teknoparrot.yml</code> file); player 1 only for games missing from the file</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>Yes, up to 4 (DemulShooter for supported games)</td></tr><tr><td><strong>Wheels</strong></td><td>Yes</td></tr></tbody></table>

## Which emulator?

<table><thead><tr><th width="143.25">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>teknoparrot</strong> (only emulator)</td><td>Starts each game with its TeknoParrot profile. Controllers, light guns and wheels configured by RetroBat; fullscreen, resolution, region and free play set from RetroBat.</td><td>No save states. Some games require a TeknoParrot Patreon subscription.</td></tr></tbody></table>

TeknoParrot is also used by other RetroBat systems, with its own built-in emulator:

| System                                | Page                                 |
| ------------------------------------- | ------------------------------------ |
| Sega Lindbergh                        | [Sega Lindbergh](sega/lindbergh.md)  |
| Sega Chihiro (Cxbx)                   | [Sega Chihiro](sega/sega-chihiro.md) |
| Triforce (Dolphin)                    | [Triforce](sega/triforce.md)         |
| Namco System 246/256 (PCSX2x6, Play!) | [Namco 246/256](namco2x6.md)         |
| Namco System 357/369 (RPCS3)          | [Namco 357/369](namco3xx.md)         |

## Install TeknoParrot

TeknoParrot is not included with RetroBat.

1. Download **TeknoParrot Installer** from the [TeknoParrot download page](https://teknoparrot.com/en/Home/Download).
2. Extract the archive to the `emulators\teknoparrot` folder and run the installer: it downloads TeknoParrot and the required components.
3. Start `emulators\teknoparrot\TeknoParrotUi.exe` once and install all the updates it offers.

<div align="left"><figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption><p>TeknoParrot updates</p></figcaption></figure></div>

TeknoParrot also recommends installing **DirectX (June 2010)** and the **Visual C++ Redistributable** packages (links on its download page).

{% hint style="warning" %}
Your antivirus may flag some TeknoParrot files: these are false positives (files that patch the games to run them). Add an exception for the `emulators\teknoparrot` folder.
{% endhint %}

{% hint style="info" %}
**TeknoParrot UI 2.0** (experimental version offered on the same page) is not supported by RetroBat yet: use **TeknoParrot Installer**.
{% endhint %}

## BIOS

No BIOS required.

## Which game format?

Each game is a **folder** (copy of the cabinet hard drive). Rename the folder with the `.teknoparrot`, `.parrot` or `.game` extension and put it in `roms\teknoparrot`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure></div>

RetroBat uses the folder name (without the extension) to find the game's **TeknoParrot profile**. The easiest is to use the profile name, i.e. the name of the game's `.xml` file in `emulators\teknoparrot\GameProfiles` (or of the `.json` file in `emulators\teknoparrot\Metadata`).

For example, for _Mario Kart Arcade GP DX_ (profile `MKDX.xml`): `MKDX.teknoparrot`, `MKDX.parrot` or `MKDX.game`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure></div>

RetroBat also recognizes:

* the **game name** given in the profile's `Metadata` file (case, `:`, `-`, `.` and `'` ignored), for example `Mario Kart Arcade GP DX.teknoparrot`;
* the **original folder name** of many games, for example `Mario kart dx.teknoparrot`.

If no profile is found, RetroBat shows the "Unable to find game profile" message: rename the folder with the profile name.

```
roms\
└─ teknoparrot\
   └─ MKDX.teknoparrot\
      └─ MK_AGP3_FINAL.exe (and the other game files)
```

### Compressed games

A game can also be compressed as `.zip`, `.7z` or `.rar`: name the archive like the profile (`MKDX.zip`). RetroBat extracts it to a temporary folder before starting it (or mounts it as a drive when WinFsp or Dokan is installed).

{% hint style="info" %}
TeknoParrot games are large: extraction can take a while. An uncompressed folder starts faster.
{% endhint %}

The list of compatible games is on the [TeknoParrot website](https://teknoparrot.com/).

## Controls

RetroBat configures controllers **per game** with the `system\resources\inputmapping\teknoparrot.yml` file (more than 1,000 entries). To change a game's mapping, see the [**TeknoParrot controller mapping**](../../../controllers/specific_mapping/teknoparrot-controller-mapping.md) page.

Buttons shared by most games, as on the other arcade emulators (see the [arcade guide](../../arcade-guide.md)):

| Action               | Controller     |
| -------------------- | -------------- |
| Coin                 | SELECT         |
| Start                | START          |
| Test (operator menu) | R3             |
| Service              | L3             |
| Exit                 | HOTKEY + START |

In the operator menu, Service (L3) moves the cursor and Test (R3) confirms, in most games.

For a game missing from the file, RetroBat configures player 1:

| Action                              | Controller                       |
| ----------------------------------- | -------------------------------- |
| Directions                          | D-pad (or left stick)            |
| Steering, gas, brake (racing games) | Left stick, R2, L2               |
| Buttons 1 to 4                      | SOUTH, EAST, NORTH, WEST         |
| Buttons 5 and 6                     | L1, R1 (L3, R3 with DirectInput) |
| Coin / Start                        | SELECT / START                   |

**CONTROLS > CONTROLLER LAYOUT** picks a layout matching your arcade stick, for the games that have one in the file (see the arcade guide).

**DRIVERS > INPUT** chooses the controller API: XInput is picked automatically for an XInput controller, DirectInput otherwise.

## Light guns

Up to 4 light guns: enable **GUNS > ENABLE GUN**. Shooting games have a dedicated gun mapping (`<game>_gun` entry of the `teknoparrot.yml` file). See the [**Light gun controls**](../../../controllers/gun_controls.md) page.

| Action                    | Light gun      |
| ------------------------- | -------------- |
| Shoot                     | Left click     |
| Reload / button 2         | Right click    |
| Button 3 (grenade…)       | Middle click   |
| Player 1 / player 2 start | Keyboard 1 / 2 |
| Player 1 / player 2 coin  | Keyboard 5 / 6 |
| Test / Service            | Keyboard 0 / 9 |

Useful options (**GUNS** submenu):

| Option                                                | Effect                                                                       |
| ----------------------------------------------------- | ---------------------------------------------------------------------------- |
| **COIN\START BUTTONS**                                | ON GUN, ON KEYBOARD or TEST/SERVICE ON KEYBOARD.                             |
| **HIDE CROSSHAIR** / **HIDE GUN MODEL**               | Hides the crosshair or the weapon model (game dependent).                    |
| **OFFSCREEN RELOAD HACK**                             | Reload by shooting off-screen (enabled by default).                          |
| **USE DEMULSHOOTER**                                  | Starts DemulShooter for supported games.                                     |
| **GUN 1 INDEX** … **GUN 4 INDEX**, **KEYBOARD INDEX** | Order of the light guns and associated keyboard, when several are connected. |

## Wheels

Enable **WHEELS > ENABLE WHEEL**: RetroBat configures the wheel, pedals and gear stick for racing games. See the [**Wheels**](../../../controllers/supported-controllers/wheels.md) page.

<table data-header-hidden><thead><tr><th width="326.5"></th><th></th></tr></thead><tbody><tr><td>Option (<strong>WHEELS</strong> submenu)</td><td>Effect</td></tr><tr><td><strong>COIN &#x26; START BUTTONS</strong></td><td>Where Coin and Start are mapped.</td></tr><tr><td><strong>TEST &#x26; SERVICE BUTTONS</strong></td><td>On the wheel, on the controller (R3 / L3) or on the keyboard (0 / 9).</td></tr><tr><td><strong>DISABLE GEAR STICK</strong></td><td>Does not use the gear stick.</td></tr><tr><td><strong>GEARUP/GEARDOWN TO GEAR3/GEAR4 CONVERTER</strong></td><td>Simulates a sequential shifter on an H-pattern gear stick.</td></tr><tr><td><strong>BATTLEGEAR4TUNED SHIFT MODE</strong></td><td>Shift mode of Battle Gear 4 Tuned.</td></tr><tr><td><strong>CUSTOM PROFILE</strong></td><td>Loads a custom wheel mapping profile (1 to 4).</td></tr><tr><td><strong>FORCE GEARSTICK DEVICE ID</strong></td><td>Chooses the gear stick to use.</td></tr></tbody></table>

## Decorations

**DECORATIONS** shows a bezel around the game. For the games listed in `system\tools\teknoparrotReshade.yml` (mostly shooting games, for the Sinden border), the bezel uses ReShade; for the others, RetroBat displays it over the game window.

## Hotkeys

<table><thead><tr><th width="214">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Exit</td></tr></tbody></table>

No save states.

## Folders

<table><thead><tr><th width="224">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\teknoparrot</code></td></tr><tr><td>TeknoParrot</td><td><code>emulators\teknoparrot</code></td></tr><tr><td>Game profiles</td><td><code>emulators\teknoparrot\GameProfiles</code> (and <code>Metadata</code>)</td></tr><tr><td>Per-game settings (written by RetroBat)</td><td><code>emulators\teknoparrot\UserProfiles</code></td></tr><tr><td>TeknoParrot general settings</td><td><code>emulators\teknoparrot\ParrotData.xml</code></td></tr><tr><td>Controller and light gun mapping</td><td><code>system\resources\inputmapping\teknoparrot.yml</code> (editable copy: <code>user\inputmapping\teknoparrot.yml</code>)</td></tr><tr><td>Wheel mapping</td><td><code>system\resources\inputmapping\wheels\teknoparrot_wheels.yml</code>, <code>system\resources\inputmapping\teknoparrot_wheel_mapping.yml</code></td></tr><tr><td>ReShade bezels, special profiles and executables</td><td><code>system\tools\teknoparrotReshade.yml</code>, <code>system\tools\teknoparrotInfo.yml</code></td></tr></tbody></table>

## Useful options

| Option                                               | Effect                                                                                                                              |
| ---------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **EMULATION > REGION/LANGUAGE**                      | USA/ENGLISH, EXPORT/ENGLISH or JAPANESE, for the games that offer it.                                                               |
| **EMULATION > FREE PLAY**                            | Play without coins (enabled by default).                                                                                            |
| **EMULATION > DISABLE ADMIN RIGHTS**                 | Does not start the game as administrator, even if its profile asks for it (no more Windows prompt, but some games no longer start). |
| **VIDEO > FULLSCREEN MODE**                          | WINDOWED, FULLSCREEN WINDOW or EXCLUSIVE FULLSCREEN. By default, fullscreen window when the game offers it.                         |
| **VIDEO > USE SCREEN RESOLUTION**                    | Forces the current screen resolution for games that allow a custom resolution.                                                      |
| **VIDEO > USE CUSTOM RESOLUTION**                    | Uses the resolution of **VIDEO > VIDEO MODE**.                                                                                      |
| **DRIVERS > INPUT**                                  | XINPUT, DIRECTINPUT, RAW INPUT or MERGED INPUT, for the games that offer it.                                                        |
| **CONTROLS > JOYSTICK DEADZONE**                     | Stick deadzone for driving games (less twitchy steering with a controller).                                                         |
| **CONTROLS > FORCE PLAYER 1 / 2 PAD INDEX**          | Useful with XInput if the controllers are not ordered right.                                                                        |
| **USER INTERFACE > HIDE TEKNOPARROT ON STARTUP**     | The TeknoParrot window is hidden by default; disable it if a game does not start correctly.                                         |
| **USER INTERFACE > SHOW CONSOLE**                    | Shows the TeknoParrot console (debugging).                                                                                          |
| **USER INTERFACE > SHOW MOUSE CURSOR**               | Shows the cursor (hidden by default).                                                                                               |
| **USER INTERFACE > APM3ID (REQUIRE ONLINE PROFILE)** | APM3 ID for TeknoParrot online games.                                                                                               |
| **USER INTERFACE > DISCORD RICH PRESENCE**           | Shows the current game on Discord.                                                                                                  |

## Known issues

| Problem                                       | Solution                                                                                                                                                 |
| --------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Unable to find game profile" message         | Rename the game folder with its profile name (see [**Which game format?**](teknoparrot.md#which-game-format)).                                           |
| The game does not start, nothing is displayed | Start the game once from `TeknoParrotUi.exe` to see the error message, then disable **HIDE TEKNOPARROT ON STARTUP**. Also check the antivirus exception. |
| Black screen in fullscreen                    | Set **VIDEO > FULLSCREEN MODE** to WINDOWED or FULLSCREEN WINDOW.                                                                                        |
| Windows asks for administrator rights         | Normal for some games; **EMULATION > DISABLE ADMIN RIGHTS** removes the prompt, if the game supports it.                                                 |
| Controls do not respond                       | Keep **DRIVERS > INPUT** on automatic; with several XInput controllers, use **FORCE PLAYER 1 PAD INDEX**.                                                |
| The operator menu opens by mistake            | Test is on R3: avoid pressing the right stick, or use an arcade layout.                                                                                  |
| Subscriber-only game                          | Some games require a TeknoParrot Patreon subscription.                                                                                                   |
