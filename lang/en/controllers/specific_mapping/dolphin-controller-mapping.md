# Dolphin controller mapping

## Overview

GameCube and Wii games use the controller in very different ways: GameCube controller, Wiimote held upright or sideways, Nunchuk, Classic Controller… RetroBat sets up Dolphin automatically, but some cases need a specific setup.

This page explains two things:

* how to get a specific controller or adapter recognized, with the `GCControllers.json` file;
* how to use your own Dolphin controller profile for a game.

{% hint style="info" %}
All information can be found on the Dolphin wiki:

[https://wiki.dolphin-emu.org/index.php?title=GameINI\_(Controller\_Settings)](https://wiki.dolphin-emu.org/index.php?title=GameINI_\(Controller_Settings\))
{% endhint %}

## Automatic configuration

RetroBat configures controllers at each launch. The settings are in the advanced system options, **CONTROLS** submenu:

* **GameCube**: **FACE BUTTON LAYOUT** and **PLAYER 1 CONTROLLER TYPE** (to 4). See the [**GameCube**](../../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/gamecube.md#controls) page.

<div align="left"><figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure></div>

* **Wii**: **WIIMOTE TYPE** and **EMULATED DEVICES**, to choose how the Wiimote is held, and real Wiimotes with a DolphinBar. See the [**Wii**](../../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/wii.md#controls) page.

<div align="left"><figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

In most cases, these options are enough.

## Specific controllers and adapters (GCControllers.json)

Some GameCube controller adapters, for example those from Mayflash or raphnet, show up in Windows as an ordinary gamepad. Their buttons are then not in the right place with the automatic configuration.

The `GCControllers.json` file gives RetroBat the exact mapping of these adapters. RetroBat recognizes the adapter by its identifier (GUID) and applies this mapping instead of the automatic configuration.

RetroBat ships this file in `system\resources\inputmapping`, with two adapters: **MAYFLASH GameCube Controller Adapter** and **raphnet technologies Dual Gamecube to USB v3.6**.

For an adapter that works with the Zadig driver and the Dolphin **GAMECUBE ADAPTER** mode, this file is not needed: see the [**GameCube**](../../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/gamecube.md#using-a-real-gamecube-controller-adapter) page.

### Adding an adapter

1. Copy `GCControllers.json` from `system\resources\inputmapping` to `user\inputmapping`. Your copy then fully replaces the RetroBat file: keep the existing adapters in it.
2. Add an entry for your adapter, following the model of the entries in the file:

```json
{
    "Emulator": "dolphin",
    "Name": "MAYFLASH GameCube Controller Adapter",
    "Guid": "03000000790000004318000000016800",
    "Driver": "DInput",
    "Mapping": {
        "Buttons/A": "`Button 1`",
        "Buttons/B": "`Button 2`",
        "Main Stick/Up": "`Axis Y-`"
    },
    "HotKeyMapping": {
        "General/Exit": "@(`Button 9`+`Button 7`)"
    },
    "ControllerInfo": {
        "needActivationSwitch": "false"
    }
}
```

<table><thead><tr><th width="152.75">Field</th><th>Content</th></tr></thead><tbody><tr><td><code>Emulator</code></td><td><code>dolphin</code> for Dolphin, <code>libretro</code> for lr-dolphin.</td></tr><tr><td><code>Name</code></td><td>Exact name of the adapter as Dolphin shows it in its device list. RetroBat uses it to point Dolphin to the device: an approximate name does not work.</td></tr><tr><td><code>Guid</code></td><td>Identifier of the adapter (see below).</td></tr><tr><td><code>Driver</code></td><td>Dolphin driver to use: <code>SDL</code> (default), <code>DInput</code>…</td></tr><tr><td><code>Mapping</code></td><td>The lines to write in <code>GCPadNew.ini</code> for this port.</td></tr><tr><td><code>HotKeyMapping</code></td><td>The Dolphin hotkeys to write in <code>Hotkeys.ini</code>, when the adapter is used by player 1. They then replace the RetroBat hotkeys.</td></tr><tr><td><code>ControllerInfo</code></td><td><code>needActivationSwitch</code>: <code>true</code> so that the mapping only applies when the <strong>USE GAMECUBE-LIKE CONTROLLER</strong> option is on, <code>false</code> so that it always applies.</td></tr></tbody></table>

With Dolphin, the `ControllerInfo` field must be present, as well as `HotKeyMapping` for the player 1 adapter: otherwise the mapping is not applied.

### Finding the GUID and the mapping

**The GUID**: start a GameCube game with the adapter plugged in, then open the `emulationstation\emulatorLauncher.log` file. Look for the `Checking specific Gamecube mapping for controller` line: the GUID is at the end of this line.

**The mapping**: set up the adapter once by hand in Dolphin.

1. Turn off **AUTOCONFIGURE CONTROLLERS** for the GameCube system.
2. Run `Dolphin.exe` from the `emulators\dolphin-emu` folder.
3. Open **Controllers**, choose **Standard Controller** for port 1, then **Configure**.
4. Choose the adapter in the **Device** list and set each button.
5. Close Dolphin and open `emulators\dolphin-emu\User\Config\GCPadNew.ini`: the `[GCPad1]` section holds the lines to copy into `Mapping`, and the `Device` line gives the driver and the exact name (`DInput/0/MAYFLASH GameCube Controller Adapter`).
6. Turn **AUTOCONFIGURE CONTROLLERS** back on.

<div align="left"><figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure></div>

## Per-game controller profile

A Dolphin profile is a complete controller setup, saved under a name. Linked to a game, it replaces the RetroBat configuration for that game only. This is useful for a game that needs a very specific setup.

This method only works with Dolphin, not with lr-dolphin.

### Step 1: create the profile

1. Run `Dolphin.exe` from the `emulators\dolphin-emu` folder.
2. Open **Controllers**, then **Configure** next to the port to set up:
   * **GameCube Controllers** for a GameCube game;
   * **Wii Remotes** (emulated Wiimote) for a Wii game.

<div align="left"><figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure></div>

3. Choose your controller in the **Device** list and set the buttons.
4. In the **Profile** area, type a name, for example `Mario Kart DD`, then click **Save**.

<div align="left"><figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure></div>

The profile keeps the controller chosen in **Device**. It will only work with this controller.

### Step 2: link the profile to the game

1. Still in Dolphin, right-click the game in the list, then **Properties**.

<div align="left"><figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure></div>

2. Open the **Game Config** tab, then **Editor**.
3. In the **User Config** area, add:

```ini
[Controls]
PadProfile1 = Mario Kart DD
```

<table><thead><tr><th width="315.25">Line</th><th>For</th></tr></thead><tbody><tr><td><code>PadProfile1</code> to <code>PadProfile4</code></td><td>GameCube controller of player 1 to 4</td></tr><tr><td><code>WiimoteProfile1</code> to <code>WiimoteProfile4</code></td><td>Wiimote of player 1 to 4</td></tr></tbody></table>

The name after the `=` sign must be exactly the one from step 1.

<div align="left"><figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure></div>

4. Close Dolphin. The profile is loaded each time the game is started from RetroBat.

Dolphin saves this setting in `emulators\dolphin-emu\User\GameSettings\<game ID>.ini`, for example `GALE01.ini` for Super Smash Bros. Melee. To go back to the RetroBat configuration, remove the `[Controls]` section from this file.

## Folders

<table><thead><tr><th width="277.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Adapter file shipped with RetroBat</td><td><code>system\resources\inputmapping\GCControllers.json</code></td></tr><tr><td>Your adapter file</td><td><code>user\inputmapping\GCControllers.json</code></td></tr><tr><td>Controller settings written by RetroBat</td><td><code>emulators\dolphin-emu\User\Config\GCPadNew.ini</code> (GameCube), <code>WiimoteNew.ini</code> (Wii), <code>Hotkeys.ini</code> (hotkeys)</td></tr><tr><td>GameCube profiles</td><td><code>emulators\dolphin-emu\User\Config\Profiles\GCPad</code></td></tr><tr><td>Wiimote profiles</td><td><code>emulators\dolphin-emu\User\Config\Profiles\Wiimote</code></td></tr><tr><td>Per-game settings</td><td><code>emulators\dolphin-emu\User\GameSettings</code></td></tr><tr><td>RetroBat log (controller GUIDs)</td><td><code>emulationstation\emulatorLauncher.log</code></td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="295.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>My settings made in Dolphin disappear at the next launch</td><td>RetroBat rewrites <code>GCPadNew.ini</code> and <code>WiimoteNew.ini</code> at each launch. Use a per-game profile, or turn off <strong>AUTOCONFIGURE CONTROLLERS</strong>.</td></tr><tr><td>My profile is not loaded</td><td>Check that the name in <code>[Controls]</code> is identical to the profile name, and that the profile was created with the controller you are using.</td></tr><tr><td>A game no longer follows some RetroBat options</td><td>The <code>&#x3C;game ID>.ini</code> file in <code>emulators\dolphin-emu\User\GameSettings</code> can replace other settings than controllers. Remove the lines concerned from it.</td></tr><tr><td>My adapter is not recognized</td><td>Check the GUID in <code>emulatorLauncher.log</code> and the exact name in Dolphin. If <code>needActivationSwitch</code> is <code>true</code>, turn on <strong>USE GAMECUBE-LIKE CONTROLLER</strong>.</td></tr></tbody></table>
