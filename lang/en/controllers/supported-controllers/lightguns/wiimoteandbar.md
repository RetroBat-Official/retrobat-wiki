---
description: Use a Wii Remote as a lightgun with a Mayflash DolphinBar (modes 1 and 2).
---

# Wiimote & Dolphinbar

## Wiimote & DolphinBar

This page explains how to use a Wii Remote (Wiimote) as a lightgun with a **Mayflash DolphinBar** in **mode 1 or mode 2**, and how the Wiimote buttons are mapped in each emulator.

{% hint style="info" %}
RetroBat uses the **same layout in every emulator**: trigger to fire, A to reload, D-pad Right for Start, D-pad Left for Coin. You only need to learn it once.
{% endhint %}

{% hint style="warning" %}
For the **mode 4** setup with the WiimoteGun software, see [WiimoteGun](wiimotegun.md). The layout on this page does not apply to mode 4.
{% endhint %}

### Set up the DolphinBar

| DolphinBar mode                 | How to select it                                | Wiimote LEDs | Use in RetroBat                          |
| ------------------------------- | ----------------------------------------------- | ------------ | ---------------------------------------- |
| **Mode 2 – Game** (recommended) | Hold **Home** + press **D-pad Left**            | 1 + 4        | Lightgun (default)                       |
| Mode 1 – Normal                 | Hold **Home** + press **D-pad Down**            | 1 + 2        | Lightgun                                 |
| Mode 1 – Multimedia             | Press **Home** + **D-pad Down** again in mode 1 | 1 + 3        | ❌ Not supported (D-pad sends media keys) |
| Mode 3 – Gamepad                | Hold **Home** + press **D-pad Up**              | 1 to 4       | ❌ Not a lightgun                         |
| Mode 4 – Wii emulator           | Hold **Home** + press **D-pad Right**           | 1 to 4       | WiimoteGun and Dolphin only              |

### Configure RetroBat

In EmulationStation, open the [Main Menu (START)](../../../navigation/main-menu.md), then **Game settings → Guns → Wiimote**:

* **WIIMOTE CONNECTION MODE**: select the DolphinBar mode you use:
  * **MODE 1 (NORMAL)**: select it if your DolphinBar is in mode 1
  * **MODE 2 (GAME)**: also used when the option is not set

<div align="left"><figure><img src="../../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure></div>

Then in the [advance system settings](../../../navigation/configuration-of-systems-and-games.md) or [game settings](../../../navigation/game-options.md):

* **ENABLE GUN**: ON
* **INVERT TRIGGER/RELOAD**: enable it if the trigger

<div align="left"><figure><img src="../../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure></div>

Start, Coin, fire and reload are **the same in modes 1 and 2**. The mode only changes a few additional buttons (1, 2, +).

### Button layout

| Wiimote button                           | Function                                           |
| ---------------------------------------- | -------------------------------------------------- |
| **B** (trigger)                          | Fire                                               |
| **A**                                    | Reload (or the second gun button)                  |
| **D-pad Right**                          | Start                                              |
| **D-pad Left**                           | Coin / Select                                      |
| **D-pad Down**                           | Secondary action (grenade, pedal, special weapon…) |
| **D-pad Up**                             | First game-specific button                         |
| **1** / **2** (mode 1) or **+** (mode 2) | Additional game-specific buttons                   |
| **Home**                                 | ⚠️ Do not use: it acts as the Windows key          |

The keyboard keys **1-4** (Start) and **5-8** (Coin) keep working in every emulator.

{% hint style="warning" %}
**DolphinBar side effects** (not RetroBat):

* Mode 2: buttons **1** and **2** send the Windows _volume up / volume down_ keys.
* Mode 2: button **−** sends _Escape_, which **quits** many emulators.
{% endhint %}

#### Two Wiimotes

In most emulators all keyboards are seen as one: both Wiimotes send the same keys. RetroBat then gives **player 2 other directions**:

|       | Player 1 Wiimote | Player 2 Wiimote |
| ----- | ---------------- | ---------------- |
| Start | D-pad **Right**  | D-pad **Up**     |
| Coin  | D-pad **Left**   | D-pad **Down**   |

**Each player should only use their own directions**: D-pad Up on the player 1 Wiimote starts player 2.

A few emulators can tell keyboards apart (**TeknoParrot**, **Supermodel**, **Flycast** with 2 guns). There, both Wiimotes use the same layout (Right = Start, Left = Coin).

### Arcade emulators

#### TeknoParrot

| Wiimote                              | Function                                                   |
| ------------------------------------ | ---------------------------------------------------------- |
| B / A                                | Fire / Reload                                              |
| Right / Left                         | Start / Coin                                               |
| Down                                 | Secondary action (middle mouse button of the game profile) |
| Up, then 1, 2 (mode 1) or + (mode 2) | Extra buttons of the game                                  |

* **Extra buttons** (menu selection in _Time Crisis 3/4_, pedals in _2 Spicy_ and _Time Crisis 5_…) are placed automatically in the order defined in `system\resources\inputmapping\teknoparrot.yml`. If there are not enough free buttons (for example _Police 911_), the remaining ones stay on the keyboard arrows.
* **Two Wiimotes**: each Wiimote has its own layout. If player 1 and 2 are swapped, enable **WIIMOTE FIX ASSOCIATION**.
* **COIN\START BUTTONS** set to _ON KEYBOARD_ moves Start/Coin back to the keyboard (1-4 / 5-8).

#### Model 2

Two Wiimotes use the shared layout (player 2: Up = Start, Down = Coin). **FORCE KEYBOARD FOR START/COIN** puts Start/Coin back on the keyboard only.

#### Model 3 (Supermodel)

| Wiimote      | Function      |
| ------------ | ------------- |
| B / A        | Fire / Reload |
| Right / Left | Start / Coin  |

With two guns Supermodel reads each keyboard separately: both Wiimotes use Right/Left.

#### Flycast (Naomi, Atomiswave)

| Wiimote      | Function      |
| ------------ | ------------- |
| B / A        | Fire / Reload |
| Right / Left | Start / Coin  |
| Down         | Button B      |
| Up           | Button X      |

With one Wiimote, Start/Coin are on the Wiimote only (Flycast allows one key per button).

#### MAME

| Wiimote                 | Function            |
| ----------------------- | ------------------- |
| B / A                   | Button 1 / Button 2 |
| Right / Left            | Start / Coin        |
| Down (one Wiimote only) | Button 3            |

Two Wiimotes: player 2 uses Up/Down for Start/Coin.

#### ArcadeDuck

| Wiimote      | Function                                      |
| ------------ | --------------------------------------------- |
| B / A        | Fire / Reload                                 |
| Right / Left | Start / Coin                                  |
| Down         | _Judge Dredd_: secondary weapon (one Wiimote) |

With two Wiimotes, the _Judge Dredd_ secondary weapon is on **1** (mode 1) or **+** (mode 2) for player 1, and on **2** for player 2 (mode 1 only).

#### PCSX2 arcade (pcsx2x6: Namco System 246/256)

Start and Coin are sent through the cabinet inputs: player 1 Right/Left, player 2 Up/Down.

#### xemu (Chihiro)

| Wiimote      | One Wiimote    | Two Wiimotes                     |
| ------------ | -------------- | -------------------------------- |
| B            | Fire           | Fire                             |
| A            | Reload         | Pedal / change                   |
| Start / Coin | Right / Left   | P1: Right / Left – P2: Up / Down |
| Down         | Pedal / change | –                                |
| Up           | Body sensor    | –                                |

With two Wiimotes, reload by aiming off-screen.

#### Lindbergh (Linuxloader)

| Wiimote                 | One Wiimote             | Two Wiimotes            |
| ----------------------- | ----------------------- | ----------------------- |
| B / A                   | Fire / Reload           | Fire / Reload           |
| Right / Left            | Start (+ action) / Coin | Start (+ action) / Coin |
| Down                    | Gun button              | P2 Coin                 |
| Up                      | Left pedal              | P2 Start                |
| 1 (mode 1) / + (mode 2) | Right pedal             | Gun button              |
| 2 (mode 1)              | –                       | Left pedal              |

Player 2 gun needs **USE DEMULSHOOTER**.

#### Hypseus (Singe gun games)

Start / Coin: player 1 Right/Left, player 2 Up/Down. B fires, A is the second gun button.

### Console emulators

On consoles, the gun often has its own D-pad: the Wiimote D-pad then stays a D-pad.

#### RetroArch (Libretro cores)

| Wiimote                 | Function                            |
| ----------------------- | ----------------------------------- |
| B / A                   | Fire / Reload (depends on the core) |
| Right / Left            | Gun Start / Gun Select              |
| Down / Up               | Aux A / Aux B                       |
| 1 (mode 1) / + (mode 2) | Aux C                               |

* Only **player 1** uses the Wiimote buttons (RetroArch merges all keyboards).
* **GUN A/B BUTTONS MAPPING**: keep the default (or _directions_) to get Aux A/B/C on the D-pad.

#### Flycast (Dreamcast)

| Wiimote      | Mode 2        | Mode 1        |
| ------------ | ------------- | ------------- |
| B / A        | Fire / Reload | Fire / Reload |
| D-pad        | Gun D-pad     | Gun D-pad     |
| Start        | **+**         | **1**         |
| Button A / B | **1** / **2** | –             |

{% hint style="danger" %}
With one Wiimote in mode 2, the **−** button quits Flycast (Escape).
{% endhint %}

#### DuckStation (PlayStation GunCon)

| Wiimote          | Player 1                  | Player 2                  |
| ---------------- | ------------------------- | ------------------------- |
| B                | Fire                      | Fire                      |
| A                | Shoot off-screen (reload) | Shoot off-screen (reload) |
| GunCon A (Start) | Right                     | Up                        |
| GunCon B         | Left                      | Down                      |

**GUN A/B BUTTONS** overrides this layout when set.

#### PCSX2 (PlayStation 2 GunCon 2)

| Wiimote      | Function       |
| ------------ | -------------- |
| B / A        | Fire / Reload  |
| Right / Left | Start / Select |
| Down / Up    | GunCon 2 A / B |

**GUN MAPPING** overrides this layout when set.

#### Xbox (Cxbx-Reloaded, EMS TopGun)

| Wiimote | Mode 2         | Mode 1         |
| ------- | -------------- | -------------- |
| B / A   | Trigger / Grip | Trigger / Grip |
| D-pad   | Gun stick      | Gun stick      |
| Start   | **+**          | **1**          |
| Back    | Keyboard 5     | **2**          |

#### BizHawk

| System (gun)                 | Right | Left   | Down   |
| ---------------------------- | ----- | ------ | ------ |
| NES (Zapper)                 | Start | Select | –      |
| SNES (Super Scope)           | Pause | –      | Cursor |
| Saturn (Stunner)             | Start | –      | –      |
| Master System (Light Phaser) | Pause | –      | –      |

#### Jgenesis

| System (gun)       | Right | Left   | Down         | A                |
| ------------------ | ----- | ------ | ------------ | ---------------- |
| NES (Zapper)       | Start | Select | –            | Shoot off-screen |
| SNES (Super Scope) | Pause | –      | Turbo switch | Cursor           |

#### Snes9x

| Gun         | Right | Down         | A      |
| ----------- | ----- | ------------ | ------ |
| Super Scope | Pause | Turbo switch | Cursor |
| Justifier   | Start | –            | Start  |

### Troubleshooting

<table><thead><tr><th width="354">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>Start/Coin do not respond</td><td>Check the Wiimote LEDs (mode 2: 1 + 4, mode 1: 1 + 2) and <strong>WIIMOTE CONNECTION MODE</strong>.</td></tr><tr><td>D-pad plays/pauses music</td><td>The DolphinBar is in mode 1 Multimedia (LEDs 1 + 3): press <strong>Home + D-pad Down</strong>.</td></tr><tr><td>PC volume changes</td><td>Normal in mode 2 when pressing <strong>1</strong> or <strong>2</strong>.</td></tr><tr><td>The Windows Start menu opens</td><td><strong>Home</strong> was pressed: it acts as the Windows key.</td></tr><tr><td>The emulator closes when pressing <strong>−</strong></td><td>Mode 2 sends Escape on <strong>−</strong>. Avoid this button, or use mode 1.</td></tr><tr><td>Trigger reloads instead of firing</td><td>Some setups (Nunchuk, Wii Zapper) swap the clicks: enable <strong>INVERT TRIGGER/RELOAD</strong>.</td></tr><tr><td>Player 1 and 2 are swapped (TeknoParrot)</td><td>Enable <strong>WIIMOTE FIX ASSOCIATION</strong>.</td></tr><tr><td>Pressing D-pad Right also moves the game character</td><td>The keyboard is configured as player 1 controller: use a gamepad as player 1.</td></tr></tbody></table>
