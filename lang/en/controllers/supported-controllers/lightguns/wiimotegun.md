---
description: Turn you Wiimote into a Mouse and use it with Lightgun games.
---

# WiimoteGun & Wiimote4Guns

Use your Wiimote as a lightgun with a Mayflash DolphinBar in **mode 4**.

With a DolphinBar in **mode 4**, the Wiimote is not seen as a mouse by Windows: a software is needed to turn it into a lightgun. Two are compatible with RetroBat:

<table data-header-hidden><thead><tr><th width="129.5"></th><th width="260.25"></th><th></th></tr></thead><tbody><tr><td></td><td><strong>WiimoteGun</strong></td><td><strong>Wiimote4Guns</strong></td></tr><tr><td>Author</td><td>Fabrice Caruso (<a href="https://github.com/fabricecaruso/WiimoteGun">GitHub</a>)</td><td>Aynshe (<a href="https://github.com/Aynshe/WiimoteGun">GitHub</a>), based on WiimoteGun</td></tr><tr><td>Installation</td><td>Provided with RetroBat</td><td>To install yourself</td></tr><tr><td>Wiimotes</td><td>1</td><td><strong>Up to 4 on a single DolphinBar</strong></td></tr><tr><td>Start</td><td>With RetroBat (<code>retrobat.ini</code>)</td><td>Its own startup (service) - can be started with RetroBat</td></tr><tr><td>Extras</td><td>–</td><td>Gamepad mode, rumble, 4-LED sensor layouts…</td></tr></tbody></table>

{% hint style="warning" %}
Only use **one** of these two programs at a time.
{% endhint %}

For modes 1 and 2 of the DolphinBar (without software), see [Wiimote & DolphinBar](wiimoteandbar.md).

## DolphinBar setup

1. Place the DolphinBar **under** the screen, as close as possible to the picture, and set the switch at the back to **BOTTOM** (or **TOP** if the bar is above the screen).
2. Set the DolphinBar to **mode 4**: press the **MODE** button of the bar until LED 4 lights up, or hold **Home** and press **D-pad Right** on the Wiimote.
3. Pair your Wiimote(s) with the **SYNC** button of the DolphinBar.

## WiimoteGun

### Enable WiimoteGun

WiimoteGun is provided with RetroBat but is disabled by default. To start it with RetroBat, set `WiimoteGun=1` in the [retrobat.ini](../../../advanced-features/retrobat.ini.md) file at the root of RetroBat.

Then, in **MAIN MENU > GAME SETTINGS > GUNS > WIIMOTE**, set **WIIMOTE CONNECTION MODE** to **MODE 4 (WIIMOTEGUN)**.

When WiimoteGun runs, its icon appears in the Windows taskbar. It is grey when no Wiimote is detected, and green when a Wiimote is detected:

<div align="left"><figure><img src="../../../.gitbook/assets/image (319).png" alt=""><figcaption></figcaption></figure></div>

### Calibration

Long-press the **Home** button of the Wiimote to start the calibration, then follow the instructions on the screen.

### Options

Right-click the WiimoteGun icon in the taskbar and select **Options** to choose how your Wiimote is connected:

<div align="left"><figure><img src="../../../.gitbook/assets/image (320).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
WiimoteGun is only active when the DolphinBar is in mode 4.
{% endhint %}

## Wiimote4Guns

Wiimote4Guns is a version of WiimoteGun by Aynshe. Its main advantage: **up to 4 Wiimotes on a single DolphinBar**, for multiplayer lightgun games, with a classic sensor bar or a 4-LED layout.

### Installation

1. Disable the WiimoteGun provided with RetroBat: in `retrobat.ini`, keep `WiimoteGun=0` (default value).
2. Download and install Wiimote4Guns from the [project page](https://github.com/Aynshe/WiimoteGun/releases). It requires Windows 10 or 11 and the .NET 10 (x64) runtime, and installs its own virtual driver.
3. Set the DolphinBar to **mode 4** and pair your Wiimotes.

### Use in RetroBat

* Each Wiimote is detected as a separate lightgun (**Wiimote4Guns P1** to **P4**): RetroBat configures them automatically, in the order of the players.
* Each Wiimote sends the Start and Coin keys of its own player (`1` / `5` for player 1, `2` / `6` for player 2…), so each player starts and inserts coins with their own Wiimote.
* Calibration: long-press **Home** on the Wiimote.

Wiimote4Guns also offers:

* a **gamepad mode** (virtual controllers for each player), used in particular for rail shooters in Dolphin, PCSX2 and DuckStation;
* **rumble** in the Wiimotes, with OutputHooker and DemulShooter;
* an on-screen menu (overlay) to change its settings while playing.

## Wii games (Dolphin)

For Wii games, Dolphin uses the Wiimotes directly as **real Wiimotes** with the DolphinBar in mode 4: see the [Wii](../../../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/wii.md) page.
