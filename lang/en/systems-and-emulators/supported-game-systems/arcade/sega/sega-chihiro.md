---
description: Sega
---

# Sega Chihiro

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/chihiro-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/chihiro.svg" alt=""></picture><figcaption></figcaption></figure></div>

Arcade - Released: 2002

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Sega_Chihiro" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>xemu-chihiro</li><li>chihiro (old CXBX-Reloaded version)</li><li>chihiro-gun (chihiro-ds 1.0)</li><li>cxbx</li><li>teknoparrot</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> chihiro</td></tr><tr><td><strong>File extension</strong></td><td>.xbe .iso .bin</td></tr></tbody></table>

The default emulator is the Xemu fork by Tovarichtch: [https://github.com/Tovarichtch/xemu](https://github.com/Tovarichtch/xemu)

## Bios Information

<table><thead><tr><th width="216.80555555555554">bios file</th><th width="558.75">Folder</th></tr></thead><tbody><tr><td>chihiro_xbox_bios.bin</td><td><code>\bios\chihiro</code></td></tr><tr><td>fpr21042_m29w160et.bin</td><td><p><code>\bios\chihiro</code></p><p><code>\emulators\cxbx-reloaded\EmuMediaBoard</code><br><code>\emulators\chihiro\EmuMediaBoard</code><br><code>\emulators\chihiro-ds\EmuMediaBoard</code><br><code>\emulators\teknoparrot\cxbxr\TeknoParrot\EmuMediaBoard</code></p></td></tr><tr><td>ic10_g24lc64.bin</td><td><p><code>\bios\chihiro</code></p><p><code>\emulators\cxbx-reloaded\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro-ds\EmuMediaBoard\chihiro</code><br><code>\emulators\teknoparrot\cxbxr\TeknoParrot\EmuMediaBoard\Chihiro</code></p></td></tr><tr><td>ic11_24lc024.bin</td><td><p><code>\bios\chihiro</code></p><p><code>\emulators\cxbx-reloaded\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro-ds\EmuMediaBoard\chihiro</code><br><code>\emulators\teknoparrot\cxbxr\TeknoParrot\EmuMediaBoard\Chihiro</code></p></td></tr><tr><td>pc20_g24lc64.bin</td><td><p><code>\bios\chihiro</code></p><p><code>\emulators\cxbx-reloaded\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro-ds\EmuMediaBoard\chihiro</code><br><code>\emulators\teknoparrot\cxbxr\TeknoParrot\EmuMediaBoard\Chihiro</code></p></td></tr></tbody></table>

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
