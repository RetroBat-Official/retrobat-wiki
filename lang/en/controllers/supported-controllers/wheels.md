---
description: Vroum vroum
---

# 🛞 Wheels

{% hint style="warning" %}
**Work in progress**: wheel support in RetroBat is still being built. Only a few wheels have a ready-made configuration for each emulator, and they could only be tested with the wheels the team owns.

**We need you!** If you own a wheel that is not configured yet, create its mapping (see below) and share it on the RetroBat Discord or on GitHub, so that it can be added to RetroBat for everyone.
{% endhint %}

## How it works

When the wheels are enabled, RetroBat:

1. detects the connected wheels by their USB identifier (see the list of detected wheels);
2. looks for the mapping of this wheel model in the mapping file of the emulator (`system\resources\inputmapping\wheels`);
3. writes this mapping in the emulator configuration (steering, pedals, gears, buttons).

If a wheel is not in the list of detected wheels, or has no mapping for the emulator, RetroBat does not configure it as a wheel.

{% hint style="info" %}
* A wheel **with pedals** is required (accelerator and brake): RetroBat does not offer to play with a wheel without pedals.
* The gear stick (shifter) is optional. For some Thrustmaster wheels, the shifter is a separate device: this is handled with the `DeportedShifter` value of the mapping files.
{% endhint %}

## Enabling the wheels

The wheels are **not enabled automatically**. Enable them for a system or for a game:

* For a system: open the [View Options](../../navigation/view-options.md) of the system, select **ADVANCED SYSTEM OPTIONS**, then **WHEELS**, and set **ENABLE WHEEL** to **ON**.
* For a game: same option in the [Game Options](../../navigation/game-options.md) > **ADVANCED GAME OPTIONS** > **WHEELS**.

<div align="left"><figure><img src="../../.gitbook/assets/image (323).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (324).png" alt=""><figcaption></figcaption></figure></div>

The **WHEELS** submenu also contains the wheel options of each emulator (force feedback, button layout…), see the table below.

### Wheel games

RetroBat knows which games are played with a wheel:

* A wheel icon is displayed next to their name in the game list (**MAIN MENU > USER INTERFACE SETTINGS > ICONS > SHOW WHEEL ICON**).

<div align="left"><figure><img src="../../.gitbook/assets/image (325).png" alt=""><figcaption></figcaption></figure></div>

* The **WHEEL** collection shows only these games in a game list.

<div align="left"><figure><img src="../../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure></div>

The list is the `emulationstation\resources\gamesdb.xml` file (games marked `<wheel/>`). To customise it, copy the file to `emulationstation\.emulationstation\resources\gamesdb.xml` and edit the copy: it is read first and is not overwritten by RetroBat updates.

<div align="left"><figure><img src="../../.gitbook/assets/image (326).png" alt=""><figcaption></figcaption></figure></div>

## Compatible emulators

| Emulator                   | Systems                      | Mapping file                                                                                                                                   | Wheel options (WHEELS submenu)                                           |
| -------------------------- | ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Model 2 Emulator**       | Sega Model 2                 | `model2_wheels.yml`                                                                                                                            | ENABLE FORCE FEEDBACK, HOLD GEARS                                        |
| **Supermodel**             | Sega Model 3                 | `model3_wheels.yml`                                                                                                                            | ENABLE FORCE FEEDBACK, FORCE WHEEL INDEX                                 |
| **Flycast**                | Dreamcast, Naomi, Atomiswave | `flycast_wheels.yml` (Dreamcast), `flycast_racing_wheels.yml` (Dreamcast with **USE RACING CONTROLLER**), `flycast_arcade_wheels.yml` (arcade) | USE RACING CONTROLLER, WHEEL BUTTON LAYOUT                               |
| **PCSX2**                  | PlayStation 2                | `pcsx2_wheels.yml`                                                                                                                             | WHEEL TYPE PLAYER 1, ENABLE FORCE FEEDBACK, SIMULATE WHEEL WITH GAMEPAD… |
| **PCSX2x6**                | Namco System 246/256         | `pcsx2x6_wheels.yml`                                                                                                                           | ENABLE FORCE FEEDBACK                                                    |
| **TeknoParrot**            | PC-based arcade              | `teknoparrot_wheels.yml`                                                                                                                       | COIN & START BUTTONS, TEST & SERVICE BUTTONS, CUSTOM PROFILE…            |
| **RetroArch - lr-flycast** | Dreamcast, Naomi, Atomiswave | `libretro_flycast_wheels.yml` (not provided yet)                                                                                               | ENABLE WHEEL                                                             |

### Wheels with a ready-made mapping

| Wheel                          | Model 2 | Supermodel | Flycast | PCSX2 / PCSX2x6 | TeknoParrot |
| ------------------------------ | :-----: | :--------: | :-----: | :-------------: | :---------: |
| Logitech G29                   |    ✔    |      ✔     |    ✔    |        ✔        |      ✔      |
| Logitech G920                  |    ✔    |            |    ✔    |                 |      ✔      |
| Logitech G923 (PlayStation)    |    ✔    |            |    ✔    |        ✔        |      ✔      |
| Logitech G923 (Xbox)           |    ✔    |            |    ✔    |                 |      ✔      |
| Logitech Driving Force GT      |         |            |    ✔    |        ✔        |             |
| Thrustmaster T300RS (PS3 mode) |    ✔    |            |    ✔    |        ✔        |      ✔      |
| Moza R5                        |         |            |    ✔    |        ✔        |      ✔      |

TeknoParrot also has a mapping for many other wheels (Logitech G Pro, Thrustmaster T150 / TMX / T248 / T300RS PS4 / T500RS / TX / TS-XW, Fanatec, Moza R9 / R12 / R16, Simucube, Simagic, Asetek, Cammus, PXN V9) and a `default` mapping used for the other detected wheels.

{% hint style="info" %}
**Thrustmaster T300RS**: set the pedals to **split** in the Thrustmaster Control Panel, and make sure they are not inverted (fixed by holding **MODE + L3 + R3**).
{% endhint %}

## Adding or modifying a wheel mapping

{% hint style="info" %}
The wheel mapping files provided by RetroBat are in `system\resources\inputmapping\wheels`. Your own files go in `user\inputmapping`
{% endhint %}

Each mapping file contains **one block per wheel model**, named with the RetroBat wheel name (see Detected wheels). The lines of the block are indented with 2 spaces.

{% hint style="warning" %}
Each emulator uses **its own notation** for buttons and axes (button numbers starting at 0 or 1, axis names…). Always start from an existing block of **the same file** (the `LogitechG29` block is a good example) and read the explanations at the top of the file.
{% endhint %}

### Example: Model 2 Emulator

The `LogitechG29` block of `model2_wheels.yml`:

```yaml
LogitechG29:
  DeportedShifter: false
  Up: hatup
  Down: hatdown
  Left: hatleft
  Right: hatright
  Steer: axis0
  Throttle: axis1
  Brake: axis2
  ShiftDown: button5
  ShiftUp: button4
  South: button0
  East: button2
  West: button1
  North: button3
  Start: button9
  Select: button8
  Gear1: button12
  Gear2: button13
  Gear3: button14
  Gear4: button15
  GearN: button18
  Service: button10
  Test: button11
```

* `axis0`, `axis1`… are the axes of the wheel (steering, accelerator, brake). Use `axisinv` instead of `axis` to invert an axis.
* `button0`, `button1`… are the buttons of the wheel, **numbered from 0**. In the Windows game controller panel (`joy.cpl` > Properties), buttons are numbered from 1: subtract 1.
* `DeportedShifter: true` is only for wheels whose shifter is a separate device.

To add your wheel:

1. Copy the file to `user\inputmapping` (for example `user\inputmapping\model2_wheels.yml`): RetroBat reads this copy first, and it is not overwritten by updates.
2. Duplicate the `LogitechG29` block and rename it with the name of your wheel (for example `ThrustmasterT150:`).
3. Replace the values with the axes and buttons of your wheel, then test in game.
4. Check `emulationstation\emulatorLauncher.log`: the `[WHEELS]` lines show the detected wheel and the mapping used.

{% hint style="info" %}
For **Flycast** and **PCSX2**, the easiest way is to configure the wheel once in the emulator itself, then copy the values from the configuration file it creates (for Flycast: `emulators\flycast\mappings`). The `name` value must be the exact name of the wheel shown by the emulator.
{% endhint %}

{% hint style="success" %}
Your mapping works? Share it on the RetroBat Discord or on GitHub, so that it can be added to RetroBat!
{% endhint %}

### RetroArch (lr-flycast)

The wheel support is ready for the **lr-flycast** core (**ENABLE WHEEL** option), but **RetroBat does not provide a mapping file for it yet**. To use your wheel with lr-flycast, create the `libretro_flycast_wheels.yml` file in `user\inputmapping`, with one block per wheel:

* the keys are the RetroArch inputs: `a`, `b`, `x`, `y`, `start`, `select`, `up`, `down`, `left`, `right`, `l`, `r`, `l2`, `r2`, `l3`, `r3`, `l_x_minus`, `l_x_plus`, `l_y_minus`, `l_y_plus`…;
* a value starting with `+` or `-` is an **axis** (for example `-0` for axis 0 in the negative direction), any other value is a **button** number;
* the optional `driver` key sets the RetroArch input driver to use with this wheel (`sdl2`, `dinput`…).

```yaml
LogitechG29:
  driver: sdl2
  l_x_minus: ...   # steering left (axis)
  l_x_plus: ...    # steering right (axis)
  r2: ...          # accelerator (axis)
  l2: ...          # brake (axis)
  a: ...           # button
  b: ...           # button
  start: ...       # button
```

If you create this file, please share it with the team!

## Detected wheels

<details>

<summary>RetroBat wheel names and USB identifiers</summary>

| RetroBat name                | USB identifier (VID / PID) |
| ---------------------------- | -------------------------- |
| AsetekForte                  | 2433 / F301                |
| AsetekInvicta                | 2433 / F300                |
| AsetekLaPrima                | 2433 / F303                |
| AsetekTonyKannan             | 2433 / F306                |
| CammusC5                     | 3416 / 0301                |
| CammusC12                    | 3416 / 0302                |
| FanatecClubSportWheelBaseV2  | 0EB7 / 0001                |
| FanatecClubSportWheelBaseV25 | 0EB7 / 0004                |
| FanatecCSLElite              | 0EB7 / 0E03                |
| FanatecCSLElitePS4           | 0EB7 / 0005                |
| FanatecCSRElite              | 0EB7 / 0011                |
| FanatecDD                    | 0EB7 / 0020                |
| FanatecPodiumDD1             | 0EB7 / 0006                |
| FanatecPodiumDD2             | 0EB7 / 0007                |
| LogitechDrivingForce         | 046D / C294, C298          |
| LogitechDrivingForceGT       | 046D / C29A                |
| LogitechG25                  | 046D / C299                |
| LogitechG27                  | 046D / C29B                |
| LogitechG29                  | 046D / C24F, C260          |
| LogitechG920                 | 046D / C262                |
| LogitechG923PS               | 046D / C266, C267          |
| LogitechG923X                | 046D / C26D, C26E          |
| LogitechGPro                 | 046D / C272                |
| LogitechMomoForce            | 046D / C295                |
| LogitechMomoRacing           | 046D / CA03                |
| LogitechRacingWheel          | 046D / CA04                |
| LogitechSpeedForce           | 046D / C29C                |
| LogitechWingmanFormula       | 046D / C202                |
| LogitechWingmanFormulaForce  | 046D / C293                |
| LogitechWingmanFormulaGP     | 046D / C20E                |
| MicrosoftSideWinder          | 045E / 001A, 0034          |
| MozaR3                       | 346E / 0005                |
| MozaR5                       | 346E / 0004                |
| MozaR9                       | 346E / 0002                |
| MozaR12                      | 346E / 0006                |
| MozaR16                      | 346E / 0000                |
| PXNV9                        | 11FF / 0511                |
| SimagicM10                   | 0483 / 0522                |
| Simucube1                    | 16D0 / 0D5A                |
| Simucube2Pro                 | 16D0 / 0D60                |
| Simucube2Sport               | 16D0 / 0D61                |
| Simucube2Ultimate            | 16D0 / 0D5F                |
| SimXperienceAccuForcePro     | 1FC9 / 804C                |
| ThrustmasterF430FF           | 044F / B56A                |
| ThrustmasterFGTFF            | 044F / B654                |
| ThrustmasterFGTRumbleForce   | 044F / B651                |
| ThrustmasterNascarProFF2     | 044F / B605                |
| ThrustmasterRGT              | 044F / B653                |
| ThrustmasterT150             | 044F / B677                |
| ThrustmasterT248             | 044F / B696                |
| ThrustmasterT300RSPS3        | 044F / B66E                |
| ThrustmasterT300RSPS3ADV     | 044F / B66F                |
| ThrustmasterT300RSPS4        | 044F / B66D                |
| ThrustmasterT500RS           | 044F / B56E                |
| ThrustmasterTMX              | 044F / B67F                |
| ThrustmasterTSPC             | 044F / B689                |
| ThrustmasterTSXW             | 044F / B692                |
| ThrustmasterTX               | 044F / B669                |
| VRSDirectForcePro            | 0483 / A355                |

</details>

Your wheel is not in the list? Find its VID and PID in the Windows Device Manager (Properties > Details > Hardware Ids) and send them to the team on Discord or GitHub.
