---
description: Bang bang
---

# 🔫 Lightguns

RetroBat detects lightguns and configures them automatically in compatible emulators. This page explains how to connect and set up your gun.

To know which systems and emulators support guns, and how the buttons are mapped, see the [Gun controls](../../gun_controls.md) page.

## Supported lightguns

<table><thead><tr><th width="161.5">Lightgun</th><th width="135.5">Detection</th><th width="173.75">Several players</th><th>Notes</th></tr></thead><tbody><tr><td><strong>Sinden</strong></td><td>Automatic</td><td>Yes</td><td>Needs the Sinden software and a white border around the screen (both handled by RetroBat, see below).</td></tr><tr><td><strong>Gun4IR</strong></td><td>Automatic</td><td>Yes</td><td></td></tr><tr><td><strong>Blamcon</strong></td><td>Automatic</td><td>Yes</td><td></td></tr><tr><td><strong>RetroShooter</strong></td><td>Automatic</td><td>Yes</td><td></td></tr><tr><td><strong>AimTrak</strong> (Ultimarc)</td><td>Automatic</td><td>Yes</td><td></td></tr><tr><td><strong>AE Lightgun</strong></td><td>Automatic</td><td>Yes</td><td></td></tr><tr><td><strong>Xgunner</strong></td><td>Automatic</td><td>Yes</td><td></td></tr><tr><td><strong>Wiimote + DolphinBar</strong> (mode 1 or 2)</td><td>Automatic</td><td>Yes, one DolphinBar per Wiimote</td><td>See <a href="wiimoteandbar.md">Wiimote &#x26; DolphinBar</a>.</td></tr><tr><td><strong>Wiimote + WiimoteGun</strong> (DolphinBar mode 4)</td><td>When WiimoteGun is running</td><td>No (1 Wiimote)</td><td>See <a href="wiimotegun.md">WiimoteGun</a>.</td></tr><tr><td><strong>Wiimote + Wiimote4Guns</strong></td><td>Automatic</td><td>Yes, up to 4</td><td>See below.</td></tr><tr><td><strong>Mouse</strong></td><td>Always</td><td>–</td><td>A mouse can be used as a gun when no lightgun is connected.</td></tr></tbody></table>

{% hint style="info" %}
Most lightguns work as a **mouse and keyboard**. Check your gun's own software or manual if it has several modes, and keep it in its mouse mode.
{% endhint %}

## Lightgun detection

When a lightgun is connected, EmulationStation shows a notification and a gun icon in the top left corner, next to the controller icons: ![](<../../../.gitbook/assets/image (307).png>)

<div align="left"><figure><img src="../../../.gitbook/assets/image (308).png" alt=""><figcaption></figcaption></figure></div>

A crosshair is also displayed on the screen, so you can navigate the menus with the gun.

These can be changed in **MAIN MENU > CONTROLLER SETTINGS**:

* **SHOW GUN NOTIFICATIONS**: notifications when a gun is connected or disconnected.
* **DRAW GUN CROSSHAIR**: crosshair in EmulationStation.

<div align="left"><figure><img src="../../../.gitbook/assets/image (309).png" alt=""><figcaption></figcaption></figure></div>

## Lightgun games

RetroBat knows which games are lightgun games:

* A gun icon is displayed next to their name in the game list (**MAIN MENU > USER INTERFACE SETTINGS > ICONS > SHOW GUN ICON**).

<div align="left"><figure><img src="../../../.gitbook/assets/image (310).png" alt=""><figcaption></figcaption></figure></div>

* The **LIGHTGUN** filter shows only these games in a game list.
* The **lightgun games** collection groups them all. Enable it in **MAIN MENU > GAME COLLECTION SETTINGS > AUTOMATIC GAME COLLECTIONS**.

The list of lightgun games is the `emulationstation\resources\gamesdb.xml` file. A game is recognised when its file name matches (or contains) the `id` of a game marked `<gun/>` for its system.

{% hint style="info" %}
To customise the list, copy the file to `emulationstation\.emulationstation\resources\gamesdb.xml` and edit the copy: it is read first and is not overwritten by RetroBat updates. Your copy will not receive the games added in later updates.
{% endhint %}

{% hint style="info" %}
Some games are in the list although the gun is only used in some levels or mini-games.
{% endhint %}

## Enabling the guns

For games in the list, **the guns are enabled automatically** when you launch the game (except on Wii, where the Wiimotes are used as real Wiimotes).

For other games, or to change this behaviour, use the **ENABLE GUN** option:

* For a system: open the [View Options](../../../navigation/view-options.md) of the system, select **ADVANCED SYSTEM OPTIONS**, then **GUNS**.
* For a game: open the [Game Options](../../../navigation/game-options.md) and select **ADVANCED GAME OPTIONS**, then **GUNS**.

<div align="left"><figure><img src="../../../.gitbook/assets/image (311).png" alt=""><figcaption></figcaption></figure></div>

Set **ENABLE GUN** to **OFF** to play a lightgun game with a gamepad.

{% hint style="info" %}
Disabling the controller autoconfiguration does not disable the gun configuration: set **ENABLE GUN** to **OFF** as well.
{% endhint %}

Other common options in the **GUNS** submenu (depending on the emulator):

<table><thead><tr><th width="235.25">Option</th><th>Description</th></tr></thead><tbody><tr><td><strong>USE ONE GUN ONLY</strong></td><td>Configures only one gun when several are connected.</td></tr><tr><td><strong>RELOAD WITH BUTTON</strong></td><td>Reloads with a button instead of shooting off-screen, for guns that cannot shoot off-screen.</td></tr><tr><td><strong>INVERT TRIGGER/RELOAD</strong></td><td>Inverts the trigger and reload buttons (e.g. with a Wii Zapper).</td></tr></tbody></table>

## Several guns and player order

RetroBat assigns the guns to the players in this order:

1. Dedicated lightguns, following their own player number when the gun has one (Gun4IR, Blamcon, Sinden, RetroShooter…).
2. Wiimotes (Wiimote4Guns P1 to P4, then DolphinBar).
3. Other mice.

If the order is wrong, you can force it with **P1 MOUSE/GUN INDEX** to **P4 MOUSE/GUN INDEX**:

* RetroArch: **MAIN MENU > GAME SETTINGS > RETROARCH OPTIONS > GUNS**.
* Other emulators: system advanced options > **GUNS**, when the emulator offers it.

{% hint style="info" %}
The detected guns, in their order, are listed in `emulationstation\emulatorLauncher.log` (lines starting with `[RawLightGun]`).
{% endhint %}

## Sinden Lightgun

<div align="left"><figure><img src="../../../.gitbook/assets/image (312).png" alt="" width="188"><figcaption></figcaption></figure></div>

The Sinden lightgun needs the Sinden software (`Lightgun.exe`), available on the [Sinden website](https://sindenlightgun.com/drivers/).

### First setup (outside RetroBat)

Before using the guns in RetroBat, run the Sinden software once on its own:

1. Configure and calibrate your gun(s) in the software (one tab per gun).
2. Enable **Start automatically**, so that the gun starts tracking as soon as the software is launched by RetroBat:

<div align="left"><figure><img src="../../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure></div>

3. Close the software: your settings are saved in the `Lightgun.exe.Config` file, next to `Lightgun.exe`.

### Sinden software in RetroBat

RetroBat starts it automatically when a Sinden gun is detected. Either:

* put the software in the `system\tools\sinden` folder of RetroBat,

<div align="left"><figure><img src="../../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure></div>

* or set its location in **MAIN MENU > GAME SETTINGS > GUNS > SINDEN > SINDEN SOFTWARE PATH**.

<div align="left"><figure><img src="../../../.gitbook/assets/image (313).png" alt=""><figcaption></figcaption></figure></div>

Other options in **GAME SETTINGS > GUNS > SINDEN**:

<table><thead><tr><th width="221.5">Option</th><th>Description</th></tr></thead><tbody><tr><td><strong>SINDEN BUTTONS CONFIGURATION</strong></td><td><strong>STANDARD</strong> (default): RetroBat sets the gun buttons as mouse buttons and keys, as expected by the emulators. <strong>GAMEPAD MODE</strong>: the buttons are sent as gamepad buttons. <strong>NO CONFIGURATION</strong>: RetroBat keeps your own Sinden configuration.</td></tr><tr><td><strong>KILL SINDEN SOFTWARE</strong></td><td>Closes the Sinden software when the game ends.</td></tr></tbody></table>

**White border**: the Sinden needs a white border around the game to locate the screen. RetroBat adds it automatically (as a bezel) when the guns are enabled.

For some standalone emulators, the border is drawn with ReShade: select the **sindenborder** shader set if the border does not appear.

<div align="left"><figure><img src="../../../.gitbook/assets/image (315).png" alt=""><figcaption></figcaption></figure></div>

## Wiimote

<div align="left"><figure><img src="../../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure></div>

A Wii Remote (Wiimote) can be used as a lightgun in three ways:

<table><thead><tr><th width="158.5">Method</th><th width="167.75">DolphinBar mode</th><th width="176.25">Players</th><th>Software</th></tr></thead><tbody><tr><td><strong>DolphinBar alone</strong></td><td>Mode 1 or mode 2</td><td>One DolphinBar per Wiimote</td><td>None. See <a href="wiimoteandbar.md">Wiimote &#x26; DolphinBar</a>.</td></tr><tr><td><strong>WiimoteGun</strong></td><td>Mode 4</td><td>1</td><td>Provided with RetroBat. See <a href="wiimotegun.md">WiimoteGun</a>.</td></tr><tr><td><strong>Wiimote4Guns</strong></td><td>Mode 4, or Bluetooth without DolphinBar</td><td>Up to 4</td><td>To install: <a href="https://github.com/Aynshe/WiimoteGun">Wiimote4Guns (Aynshe)</a>.</td></tr></tbody></table>

Tell RetroBat which mode you use in **MAIN MENU > GAME SETTINGS > GUNS > WIIMOTE > WIIMOTE CONNECTION MODE**. With 2 Wiimotes, **WIIMOTE FIX ASSOCIATION** can fix a wrong association between the Wiimotes and their keyboard in some emulators.

<div align="left"><figure><img src="../../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
For Wii games in Dolphin, the Wiimotes are used as **real Wiimotes** (DolphinBar in mode 4): see the [Wii page](../../../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/wii.md).
{% endhint %}

### Wiimote4Guns

Wiimote4Guns is a version of WiimoteGun by Aynshe that supports **up to 4 Wiimotes**, connected with a DolphinBar in mode 4 or directly in Bluetooth, with a 1-bar sensor or a 4-LED layout. Each Wiimote is seen by RetroBat as a separate lightgun (Wiimote4Guns P1 to P4) and configured automatically for multiplayer games.

1. Install Wiimote4Guns as described on the [project page](https://github.com/Aynshe/WiimoteGun) (Windows 10 or 11, .NET 10 x64 runtime; Wiimote4Guns installs its own virtual driver).
2. Disable the WiimoteGun provided with RetroBat: in the `retrobat.ini` file at the root of RetroBat, set `WiimoteGun=0` (default value).
3. Set the DolphinBar to **mode 4**.

{% hint style="info" %}
For better accuracy, place the DolphinBar (or the sensor bar) **under** the screen, as close as possible to the picture, and set the switch at the back of the DolphinBar to the **bottom** position.
{% endhint %}

{% hint style="warning" %}
WiimoteGun and Wiimote4Guns must not run at the same time.
{% endhint %}

## Other lightguns

* [Gun4IR](https://www.gun4ir.com/)
* [RetroShooter](https://retroshooter.com/)
* [Blamcon](https://blamcon.com/)
* [AimTrak (Ultimarc)](https://www.ultimarc.com/)

These guns are detected automatically by their USB identifier. Set them to their mouse (and keyboard) mode with their own software if they have several modes.
