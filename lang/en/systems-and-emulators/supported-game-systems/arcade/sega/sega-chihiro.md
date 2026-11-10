---
description: Sega
---

# Sega Chihiro

<div align="left"><figure><img src="../../../../.gitbook/assets/image (481).png" alt="" width="557"><figcaption></figcaption></figure></div>

## Overview

The **Chihiro** is an arcade system designed by **Sega** with **Microsoft** and released in **2002**. It uses the Xbox architecture (Intel Pentium III CPU at 733 MHz, NVIDIA NV2A graphics chip) with twice the main memory (128 MB). It is named after the heroine of the movie _Spirited Away_.

Like the Naomi and Triforce systems, the Chihiro reads its games from a **GD-ROM**: the whole disc is copied to the memory of a DIMM board at startup, so there is no loading during gameplay. It is Sega's last arcade system derived from a home console; its successor, the Lindbergh, is based on PC architecture.

Its best-known games include **The House of the Dead III**, **Virtua Cop 3**, **Ghost Squad**, **OutRun 2**, **Crazy Taxi High Roller**, **Ollie King** and, from Namco, **Wangan Midnight Maximum Tune** 1 and 2. Several of them were later ported to the Xbox, thanks to the shared hardware.

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Sega_Chihiro" %}

## At a glance <a href="#at-a-glance" id="at-a-glance"></a>

<table><thead><tr><th width="244"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\chihiro</code></td></tr><tr><td><strong>Extensions</strong></td><td>.xbe .iso .bin</td></tr><tr><td><strong>Default emulator</strong></td><td>xemu-chihiro</td></tr><tr><td><strong>BIOS</strong></td><td><code>chihiro_xbox_bios.bin</code>, <code>fpr21042_m29w160et.bin</code>, <code>ic10_g24lc64.bin</code>, <code>ic11_24lc024.bin</code>, <code>pc20_g24lc64.bin</code> in <code>bios\chihiro</code></td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators (xemu-chihiro: supported games)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>xemu-chihiro, chihiro and chihiro-gun (DemulShooter), TeknoParrot</td></tr><tr><td><strong>Wheels</strong></td><td>xemu-chihiro, TeknoParrot</td></tr></tbody></table>

The default emulator is the Xemu fork by Tovarichtch: [https://github.com/Tovarichtch/xemu](https://github.com/Tovarichtch/xemu)

## BIOS

Place the following files in `bios\chihiro`. RetroBat checks that they are present.

<table><thead><tr><th width="274">File</th><th>Required</th></tr></thead><tbody><tr><td><code>chihiro_xbox_bios.bin</code></td><td>Yes</td></tr><tr><td><code>ic10_g24lc64.bin</code></td><td>Yes</td></tr><tr><td><code>ic11_24lc024.bin</code></td><td>Yes</td></tr><tr><td><code>pc20_g24lc64.bin</code></td><td>Yes</td></tr><tr><td><code>fpr21042_m29w160et.bin</code></td><td>Yes (xemu-chihiro also accepts <code>fpr-23887_29lv160te.ic4</code> or <code>fpr-23887.bin</code>)</td></tr></tbody></table>

With **xemu-chihiro** (default emulator), there is nothing else to do: RetroBat uses the files from the `bios\chihiro` folder directly.

### CXBX-based emulators (chihiro, chihiro-gun, cxbx, TeknoParrot)

These emulators read the board files from their own `EmuMediaBoard` folder. Copy them from `bios\chihiro`:

<table><thead><tr><th width="359">File</th><th>Destination</th></tr></thead><tbody><tr><td><code>fpr21042_m29w160et.bin</code></td><td><code>EmuMediaBoard\</code></td></tr><tr><td><code>ic10_g24lc64.bin</code>, <code>ic11_24lc024.bin</code>, <code>pc20_g24lc64.bin</code></td><td><code>EmuMediaBoard\chihiro\</code></td></tr></tbody></table>

The `EmuMediaBoard` folder is in each emulator's folder: `emulators\chihiro`, `emulators\chihiro-ds` (chihiro-gun), `emulators\cxbx-reloaded` and TeknoParrot.

## Controls

### XEMU-CHIHIRO

RetroBat configures the Chihiro controls automatically for the games supported by xemu-chihiro:

<table><thead><tr><th width="152.75">Type</th><th>Games</th></tr></thead><tbody><tr><td>Lightgun</td><td>The House of the Dead III, Virtua Cop 3, Ghost Squad</td></tr><tr><td>Driving</td><td>Crazy Taxi High Roller, OutRun 2, Wangan Midnight Maximum Tune 2</td></tr><tr><td>Other</td><td>Ollie King, Gundam Battle Operating Simulator</td></tr></tbody></table>

{% hint style="info" %}
* Only the **player 1 controller** (the first controller in EmulationStation) is used for the game controls. Player 2 has **Start / Coin on the keyboard** only, except in the lightgun games with two guns.
* **Test** (`0`) and **Service** (`9`) are always on the keyboard.
* To use your own mapping, set **AUTOCONFIGURE CONTROLLERS** to OFF and configure the controls in xemu-chihiro.
{% endhint %}

#### Gamepad (player 1)

The buttons use the Xbox names (A = bottom button). With a Nintendo layout pad, enable **INVERT FACE BUTTONS** (Controls) to swap A/B and X/Y.

**System buttons (all games)**

<table><thead><tr><th width="202.75">Gamepad</th><th>Function</th></tr></thead><tbody><tr><td>Start</td><td>Start</td></tr><tr><td>Back / Select</td><td>Coin</td></tr><tr><td>B</td><td>Card In (card games: one press inserts the card, Maximum Tune ejects it on a second press)</td></tr></tbody></table>

**Driving games** (Crazy Taxi High Roller, OutRun 2, Maximum Tune 2)

| Gamepad            | Function            |
| ------------------ | ------------------- |
| Left stick         | Steering            |
| Right trigger (RT) | Gas                 |
| Left trigger (LT)  | Brake               |
| RB / LB            | Gear up / Gear down |

| Gamepad | Crazy Taxi High Roller | OutRun 2    | Maximum Tune 2 |
| ------- | ---------------------- | ----------- | -------------- |
| A       | Jump                   | –           | –              |
| B       | Drive gear             | –           | Card In        |
| X       | Reverse                | –           | Intrude change |
| Y       | –                      | View change | View change    |

**Ollie King**

| Gamepad                 | Function               |
| ----------------------- | ---------------------- |
| Left stick left / right | Swing left / right     |
| Left stick up / down    | Board front / rear     |
| LB / RB                 | Left grab / Right grab |

**Gundam Battle Operating Simulator** (twin-stick cockpit)

| Gamepad     | Function                     |
| ----------- | ---------------------------- |
| Left stick  | Left lever                   |
| LT / LB     | Left lever trigger / button  |
| Right stick | Right lever                  |
| RT / RB     | Right lever trigger / button |
| A           | Pedal                        |

#### Keyboard

| Key    | Function                            |
| ------ | ----------------------------------- |
| 1 / 5  | Player 1 Start / Coin               |
| 2 / 6  | Player 2 Start / Coin               |
| 0 / 9  | Test / Service                      |
| Arrows | Steering, gas (Up) and brake (Down) |
| Z / X  | Gear up / Gear down                 |
| C      | Card In                             |

The game-specific keys are the xemu-chihiro defaults (for example Space for the Virtua Cop 3 pedal and the Ghost Squad weapon change, W A S D + arrows for Gundam). They can be changed in the xemu-chihiro input menu.

#### Lightgun games

Xemu-chihiro reads each mouse or lightgun separately: with two guns, each player has their own gun.

| Gun                  | The House of the Dead III | Virtua Cop 3            | Ghost Squad             |
| -------------------- | ------------------------- | ----------------------- | ----------------------- |
| Trigger (left click) | Fire                      | Fire                    | Fire                    |
| Right click          | Gun button                | Gun button              | Gun button              |
| Middle click         | –                         | Pedal (take cover)      | Weapon change           |
| Reload               | Aim off-screen and fire   | Aim off-screen and fire | Aim off-screen and fire |

* **Start / Coin**: keyboard `1` / `5` for player 1, `2` / `6` for player 2 (most lightguns can send these keys).
* **RELOAD WITH BUTTON**: for guns that cannot shoot off-screen. The middle click reloads, and the pedal / weapon change moves to the keyboard (`Q` for player 1, `S` for player 2).
* **INVERT TRIGGER/RELOAD**: swaps the left and right clicks.

{% hint style="info" %}
**Wiimote with a DolphinBar**: Start / Coin are on the Wiimote D-pad. See Wiimote & DolphinBar.
{% endhint %}

#### Wheels and force feedback

A wheel used as player 1 controller drives with the same bindings as a gamepad (steering, pedals, paddles on RB / LB). Options in **Wheels**:

<table><thead><tr><th width="309">Option</th><th>Description</th></tr></thead><tbody><tr><td>ENABLE FORCE FEEDBACK</td><td>Drive board force feedback (OutRun 2, Maximum Tune), on a wheel or as gamepad rumble</td></tr><tr><td>FORCE FEEDBACK STRENGTH</td><td>Strength of the effects</td></tr><tr><td>INVERT FORCE FEEDBACK</td><td>Enable if the wheel is pushed away from the center instead of toward it</td></tr><tr><td>WHEEL ROTATION</td><td>Degrees of rotation for full lock (270 = arcade cabinet)</td></tr><tr><td>WHEEL AUTO-CENTER / AUTO-CENTER STRENGTH</td><td>Centering spring while the game does not send force feedback</td></tr></tbody></table>

### CXBX

Controls must be set up directly in CXBX-Reloaded emulator in `\emulators\cxbx-reloaded` folder.

<div align="left"><figure><img src="https://i.imgur.com/W2oGLGE.png" alt=""><figcaption></figcaption></figure></div>

For Teknoparrot, controls are managed in a similar way to other Teknoparrot games: [details here](../teknoparrot.md#controls)

## Specific system information

### ROMs

#### XEMU-CHIHIRO

Xemu-Chihiro requires game roms in bin format, this tool can be used to convert a MAME recent romset file into the required format:

{% embed url="https://github.com/Tovarichtch/chihiro-netboot" %}

#### CXBX

Chihiro roms come in the form of a folder containing multiple files including .xbe files.

The game folder must be placed in the `\roms\chihiro` folder.

<div align="left"><figure><img src="https://i.imgur.com/K61I22N.png" alt=""><figcaption></figcaption></figure></div>

Usually the .xbe file ending with t (e.g.`vc3_t.xbe`) is used to run the test menu.

### Test menu

The Test menu contains options that can be adjusted within the game itself, such as aligning the crosshair for lightgun games and changing the difficulty.&#x20;

* **On xemu-chihiro**: access the test menu with 9 and 0 on your keyboard
* **On cxbx**: run the .xbe file ending with "t" to enter the test menu.

<div align="left"><figure><img src="https://i.imgur.com/V1mJQyY.png" alt=""><figcaption></figcaption></figure></div>

### Use Cerbios firmware (XEMU)

Download the Cerbios firmware and rename it 'Cerbios.bin', place it in the retrobat\bios folder.

In RetroBat advanced options for xemu, select the firmware:

<div align="left"><figure><img src="https://i.imgur.com/WYDyd9G.png" alt=""><figcaption></figcaption></figure></div>
