# Visual Pinball

<div align="left"><figure><img src="../../../.gitbook/assets/image (718).png" alt=""><figcaption></figcaption></figure></div>

## Overview

**Visual Pinball** is a pinball simulator and table editor, created by **Randy Davis** in 2000 and now developed by the community as **Visual Pinball X** (VPX). Free, it plays thousands of tables: recreations of real pinball machines (Williams, Bally, Stern, Gottlieb, Data East…) and original tables.

For solid-state machines, **VPinMAME** emulates the electronics of the real machine from its ROM: original rules, sounds and dot matrix display (DMD). Other components complete the table: **backglass** (animated backbox art, `.directb2s` files), **FlexDMD / UltraDMD** (DMD of original tables), **PinUP Player** (videos of "PuP packs") and **DOF** feedback devices for equipped cabinets.

RetroBat provides Visual Pinball X 10.8 with all these components and sets them up: screens (1 to 3), DMD, backglass and controller.

{% embed url="https://en.wikipedia.org/wiki/Visual_Pinball" %}

{% embed url="https://www.vpforums.org/" %}

## At a glance

<table><thead><tr><th width="237.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\vpinball</code></td></tr><tr><td><strong>Extensions</strong></td><td>.vpx .7z .zip .rar</td></tr><tr><td><strong>Default emulator</strong></td><td>vpinball (Visual Pinball X 10.8)</td></tr><tr><td><strong>BIOS</strong></td><td>None (pinball ROMs go in <code>roms\vpinball\roms</code>)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (player 1)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="150.75">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>vpinball</strong> (only emulator)</td><td>Visual Pinball X 10.8 with VPinMAME, backglass, DMD and PuP packs. Screens computed automatically (1, 2 or 3 screens). Controller and keyboard set up.</td><td>Windows permission requests on first launch (see <a href="visual-pinball.md#known-issues"><strong>Known issues</strong></a>). One controller only (player 1).</td></tr></tbody></table>

**Future Pinball** tables (`.fpt`) have their own system: [**Future Pinball**](future-pinball.md) (`roms\fpinball`).

## BIOS

No BIOS required. Solid-state tables need the **ROM** of the real machine (see below).

## Which game format?

<table><thead><tr><th width="154">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.vpx</strong></td><td>Visual Pinball X table.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong>, <strong>.rar</strong></td><td>Archive holding the table (and its files). RetroBat extracts it at launch and starts the first <code>.vpx</code> found.</td></tr></tbody></table>

Visual Pinball 9 `.vpt` tables are not listed.

Depending on the table, other files are needed. They are listed where the table was downloaded:

| File                                      | Role                                        | Where to put it                                                                                    |
| ----------------------------------------- | ------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `.directb2s`                              | Backglass (animated backbox art)            | Next to the table, **with the same name** as the `.vpx`.                                           |
| ROM `.zip`                                | Electronics of the real machine (VPinMAME)  | `roms\vpinball\roms`, without renaming the `.zip`.                                                 |
| `.UltraDMD` or table folder               | DMD of original tables (FlexDMD / UltraDMD) | Next to the table, without renaming the folder.                                                    |
| Music (`.mp3`, `.ogg`)                    | Music of some original tables               | `emulators\vpinball\Music` or a `music` folder next to the table, keeping the provided subfolders. |
| PuP pack                                  | Extra videos and sounds                     | `emulators\vpinball\PinUPSystem\PUPVideos\<pack name>`                                             |
| DMD colorization (`.pal`, `.vni`, `.cRZ`) | Colored DMD                                 | `emulators\vpinball\VPinMAME\altcolor\<ROM name>`                                                  |
| Alternative sounds                        | Replaced ROM sounds                         | `emulators\vpinball\VPinMAME\altsound\<ROM name>`                                                  |

```
roms\
└─ vpinball\
   ├─ My table.vpx
   ├─ My table.directb2s
   ├─ My table.UltraDMD\      (if provided)
   ├─ music\                  (if provided)
   └─ roms\
      └─ afm_113b.zip
```

ROMs are also looked for in a `roms` folder next to the table, then in `emulators\vpinball\VPinMAME\roms`. A table in an archive (`.zip`, `.7z`, `.rar`) can hold its own `roms` folder, otherwise `roms\vpinball\roms` is used.

**ROM name**: it is written in the table script (`cGameName = "…"`). RetroBat reads it at launch and logs it in `emulationstation\emulatorLauncher.log` (`VPinMAME rom name read from table` line).

<div align="left"><figure><img src="../../../.gitbook/assets/image (721).png" alt=""><figcaption><p>Backglass with the same name as the table</p></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (720).png" alt=""><figcaption><p>ROM in roms\vpinball\roms</p></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (722).png" alt=""><figcaption></figcaption></figure></div>

At launch, RetroBat shows the table backglass (if any) while loading.

## Controls

RetroBat sets up the player 1 controller and the keyboard at each launch:

<table><thead><tr><th width="239">RetroBat controller</th><th>Visual Pinball</th></tr></thead><tbody><tr><td>L1 / R1</td><td>Left / right flipper</td></tr><tr><td>SOUTH</td><td>Plunger (hold then release)</td></tr><tr><td>R2</td><td>Analog plunger</td></tr><tr><td>D-pad up</td><td>Nudge forward</td></tr><tr><td>D-pad left / right</td><td>Nudge left / right</td></tr><tr><td>D-pad down</td><td>Mechanical tilt</td></tr><tr><td>Left stick</td><td>Nudge (analog), with <strong>CONTROLS > ENABLE ANALOG NUDGE</strong></td></tr><tr><td>EAST</td><td>Action button (lockbar)</td></tr><tr><td>WEST / NORTH</td><td>Left / right MagnaSave</td></tr><tr><td>SELECT</td><td>Insert coin</td></tr><tr><td>START</td><td>Start game</td></tr><tr><td>L3</td><td>Pause</td></tr></tbody></table>

L2 and the right stick are not used. The action button launches the ball or fires on many recent tables, the MagnaSaves hold the ball on some tables (Black Knight, Jungle Lord…).

<table><thead><tr><th width="262.75">Keyboard</th><th>Visual Pinball</th></tr></thead><tbody><tr><td><code>Left Shift</code> / <code>Right Shift</code></td><td>Left / right flipper</td></tr><tr><td><code>Left Windows</code> / <code>Right Alt</code></td><td>Left / right staged flipper (tables using it)</td></tr><tr><td><code>Enter</code></td><td>Plunger</td></tr><tr><td><code>Space</code></td><td>Nudge forward</td></tr><tr><td><code>Z</code> / <code>/</code></td><td>Nudge left / right</td></tr><tr><td><code>T</code></td><td>Mechanical tilt</td></tr><tr><td><code>Left Ctrl</code> / <code>Right Ctrl</code></td><td>Left / right MagnaSave</td></tr><tr><td><code>Left Alt</code></td><td>Action button (lockbar)</td></tr><tr><td><code>5</code> / <code>4</code></td><td>Insert coin (coin slot 1 / 2)</td></tr><tr><td><code>1</code></td><td>Start game</td></tr><tr><td><code>P</code></td><td>Pause</td></tr><tr><td><code>-</code> / <code>=</code></td><td>Volume down / up</td></tr><tr><td><code>X</code></td><td>Table menu (long press: exit)</td></tr><tr><td><code>F10</code></td><td>In-game table settings (view, lighting…)</td></tr><tr><td><code>F11</code></td><td>Frames per second</td></tr></tbody></table>

Keys given for a QWERTY keyboard: Visual Pinball reads the key position (on an AZERTY keyboard, `Z` is `W`, `/` is `!` and `-` is `)`). `Esc` is disabled.

To keep your own Visual Pinball settings (controller and keyboard), disable **AUTOCONFIGURE CONTROLLERS**. **DRIVERS > INPUT** chooses DIRECTINPUT or XINPUT (by default according to the controller), or **USE** [**PAD2KEY**](../../../controllers/pad2key.md) (the controller emulates the keyboard, with the same buttons).

### Hotkeys

<table><thead><tr><th width="142">Action</th><th>Controller</th><th>Keyboard</th></tr></thead><tbody><tr><td>Exit</td><td>HOTKEY + START</td><td><code>X</code> (long press)</td></tr><tr><td>Screenshot</td><td>HOTKEY + R3</td><td><code>Print Screen</code></td></tr></tbody></table>

The screenshot becomes the game image in RetroBat if it has none, otherwise it is saved in `screenshots`.

With **EMULATION > USE EXIT TABLE TO EXIT**, HOTKEY + START sends `X` to Visual Pinball instead of closing its window: its menu opens (choose **Quit**). With **EMULATION > DISABLE MENU**, `X` exits the table directly.

## Folders

<table><thead><tr><th width="354">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Tables, backglasses, <code>ScreenRes.txt</code></td><td><code>roms\vpinball</code></td></tr><tr><td>ROMs</td><td><code>roms\vpinball\roms</code></td></tr><tr><td>Pinball scores and settings (NVRAM)</td><td><code>emulators\vpinball\VPinMAME\nvram</code></td></tr><tr><td>DMD colorization, alternative sounds</td><td><p><code>emulators\vpinball\VPinMAME\altcolor</code></p><p><code>emulators\vpinball\VPinMAME\altsound</code></p></td></tr><tr><td>Music</td><td><code>emulators\vpinball\Music</code></td></tr><tr><td>PuP packs</td><td><code>emulators\vpinball\PinUPSystem\PUPVideos</code></td></tr><tr><td>Visual Pinball settings</td><td><code>emulators\vpinball\VPinballX.ini</code></td></tr><tr><td>External DMD and hardware DMD settings</td><td><code>emulators\vpinball\VPinMAME\DmdDevice.ini</code></td></tr><tr><td>Backglass settings</td><td><code>emulators\vpinball\BackglassServer\B2STableSettings.xml</code> (copied to <code>roms\vpinball</code>)</td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr></tbody></table>

At each launch, RetroBat rewrites part of `VPinballX.ini`, `ScreenRes.txt` and `DmdDevice.ini` from its options.

## Guides

### Setting up the screens (1, 2 or 3 screens)

On a PC with a single screen, there is nothing to set. For a cabinet or several screens, set **SCREENS > SCREEN SETUP**: RetroBat then places the playfield, the backglass and the DMD by itself.

<table><thead><tr><th width="292.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>SCREENS > SCREEN SETUP</strong></td><td><strong>DETECT CONNECTED SCREENS</strong> (up to 3), <strong>1 SCREEN</strong>, <strong>2 SCREENS (PLAYFIELD + BACKGLASS)</strong> or <strong>3 SCREENS (PLAYFIELD + BACKGLASS + DMD)</strong>.</td></tr><tr><td><strong>VIDEO > MONITOR INDEX</strong></td><td>Playfield screen. Not set: the primary screen.</td></tr><tr><td><strong>SCREENS > BACKGLASS SCREEN</strong></td><td>Not set: the largest of the other screens.</td></tr><tr><td><strong>SCREENS > DMD LOCATION</strong></td><td>Not set: on the playfield with 1 screen, at the bottom of the backglass screen with 2 screens, on its own screen with 3 screens. <strong>HARDWARE DMD ONLY</strong>: only on a plugged-in DMD (ZeDMD, PIN2DMD…).</td></tr><tr><td><strong>SCREENS > DMD SCREEN</strong></td><td>With 3 screens. Not set: the smallest remaining screen.</td></tr><tr><td><strong>VIDEO > TABLE VIEW</strong></td><td>Not set: <strong>DESKTOP</strong> with a landscape screen, <strong>FULL SINGLE SCREEN</strong> with a portrait screen, <strong>CABINET</strong> with several screens.</td></tr><tr><td><strong>VIDEO > ENABLE BACKGLASS</strong></td><td>Not set: the backglass is shown when it has a screen (not with 1 screen).</td></tr><tr><td><strong>VIDEO > SCREEN ROTATION</strong></td><td>Rotates the playfield screen during the game (screen lying in a cabinet), then puts it back.</td></tr><tr><td><strong>SCREENS > IGNORE TABLE .RES FILE</strong></td><td>Ignores the table's own backglass placement (<code>.res</code> file next to the table) during the game.</td></tr></tbody></table>

Screens are numbered as for **MONITOR INDEX** (0 = first screen).

<div align="left"><figure><img src="../../../.gitbook/assets/image (719).png" alt=""><figcaption></figcaption></figure></div>

Without **SCREEN SETUP**, RetroBat keeps the former behavior: the values of the **SCREENRES** menu (backglass and DMD size and position), otherwise the playfield on the primary screen and the backglass on screen 2. The `emulators\vpinball\BackglassServer\B2S_ScreenResIdentifier.exe` tool helps find these values. To keep a hand-made `ScreenRes.txt`, enable **SCREENRES > DISABLE SCREENRES OVERWRITE**.

### DMD (dot matrix display)

| Option                                         | Effect                                                                                                                              |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **VPINMAME > DMD**                             | **INTERNAL** (default): VPinMAME DMD window. **EXTERNAL**: dmdext DMD, which also handles hardware DMDs. **NONE**: no VPinMAME DMD. |
| **VPINMAME > VIRTUAL DMD**                     | External DMD window (enabled by default).                                                                                           |
| **VPINMAME > ZEDMD**, **ZEDMDHD**, **PIN2DMD** | USB hardware DMDs (with **DMD** set to **EXTERNAL**).                                                                               |
| **VPINMAME > COLORIZE DMD**                    | Colored DMD (VPinMAME).                                                                                                             |
| **VPINMAME > SCALE DMD (ZOOM)**                | Dot size of the VPinMAME DMD.                                                                                                       |

### Other useful options

| Option                                                                           | Effect                                                                                           |
| -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| **VERTICAL SYNC**                                                                | **FRAME PACING** by default.                                                                     |
| **VIDEO > VIDEO MODE**                                                           | Resolution of the playfield screen during the game.                                              |
| **VIDEO > EXCLUSIVE FULLSCREEN**                                                 | Visual Pinball changes the resolution itself, instead of RetroBat.                               |
| **VISUAL RENDERING > ANTI-ALIASING**, **SUPERSAMPLING**                          | Smoother picture (supersampling needs a powerful graphics card).                                 |
| **VISUAL RENDERING > AMBIENT OCCLUSION**, **SHARPEN IMAGE**, **LEVEL OF DETAIL** | Picture quality: lower them on a low-end PC.                                                     |
| **VISUAL RENDERING > ENVIRONMENT LIGHTING**                                      | Room lighting, from day to night.                                                                |
| **AUDIO > AUDIO CHANNELS**                                                       | Sounds in 2 channels or surround (cabinets with extra speakers).                                 |
| **AUDIO > DISABLE MUSIC**                                                        | Mutes the music of original tables.                                                              |
| **DIRECT OUTPUT (DOF)**                                                          | For each element (contactors, knocker, flippers…): feedback device (DOF), sound effect, or both. |
| **BACKGLASS > HIDE GRILL**                                                       | Hides the speaker grill below the backglass.                                                     |
| **CONTROLS > JOYSTICK DEADZONE**, **RUMBLE MODE**                                | Stick dead zone, controller rumble.                                                              |
| **CONTROLS > DISABLE JOYSTICK STICK**                                            | Stick and R2 are no longer used.                                                                 |

## Known issues

| Problem                                                                                                | Solution                                                                                                                                                                             |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Windows asks for administrator permission at launch                                                    | Normal on first launch, and after moving RetroBat: RetroBat registers the components (VPinMAME, backglass, DMD, PinUP Player). Accept, otherwise ROMs, backglass or DMD do not work. |
| The table does not start or VPinMAME does not find the ROM                                             | Put the ROM in `roms\vpinball\roms`, without renaming it (see [**ROM name**](visual-pinball.md#which-game-format)). Some tables need a specific ROM version.                         |
| No backglass                                                                                           | The `.directb2s` must have the same name as the table. With 1 screen, the backglass is disabled: force it with **VIDEO > ENABLE BACKGLASS**.                                         |
| Backglass or DMD badly placed                                                                          | Set **SCREENS > SCREEN SETUP**. If a `.res` file is next to the table, try **IGNORE TABLE .RES FILE**.                                                                               |
| The VPinMAME DMD shows up at the wrong place, with a screen on the left of or above the primary screen | In Windows, place the DMD screen on the right of or below the primary screen, or set **VPINMAME > DMD** to **EXTERNAL**.                                                             |
| No music                                                                                               | Music in `emulators\vpinball\Music` (or `music` next to the table), with the provided subfolders.                                                                                    |
| Display issues                                                                                         | Intel graphics: **VIDEO > SOFTWARE VERTEX PROCESSING**. Other graphics cards: **VIDEO > USE NVIDIA DEPTH BUFFER**.                                                                   |
| The table is slow                                                                                      | Lower **SUPERSAMPLING**, **AMBIENT OCCLUSION** and **ANTI-ALIASING**.                                                                                                                |
