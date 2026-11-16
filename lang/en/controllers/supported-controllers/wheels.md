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
2. looks for the mapping of this wheel model in the mapping file of the emulator (your copy in `user\inputmapping` first, else `system\resources\inputmapping\wheels`);
3. writes this mapping in the emulator configuration (steering, pedals, gears, buttons).

If a wheel is not in the list of detected wheels, or has no mapping for the emulator, RetroBat does not configure it as a wheel.

{% hint style="info" %}
* A wheel **with pedals** is required (accelerator and brake): RetroBat does not offer to play with a wheel without pedals.
* The gear stick (shifter) is optional: without an H-shifter, enable **DISABLE GEAR STICK** (the gears then use the wheel buttons). For some Thrustmaster wheels, the shifter is a separate device: this is handled with the `DeportedShifter` value of the mapping files, or with **FORCE GEARSTICK DEVICE ID**.
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

<table><thead><tr><th width="140.25">Emulator</th><th width="175">Systems</th><th>Mapping file</th><th>Wheel options (WHEELS submenu)</th></tr></thead><tbody><tr><td><strong>Model 2 Emulator</strong></td><td>Sega Model 2</td><td><code>model2_wheels.yml</code></td><td>ENABLE FORCE FEEDBACK, DISABLE GEAR STICK, HOLD GEARS, FORCE GEARSTICK DEVICE ID</td></tr><tr><td><strong>Keisho</strong></td><td>Sega Model 1, Model 2, Model 3</td><td><code>keisho_wheels.yml</code> (buttons only: steering and pedals are detected by Keisho)</td><td>ENABLE FORCE FEEDBACK, FORCE FEEDBACK STRENGTH, DISABLE GEAR STICK</td></tr><tr><td><strong>Supermodel</strong></td><td>Sega Model 3</td><td><code>model3_wheels.yml</code></td><td>ENABLE FORCE FEEDBACK, FORCE WHEEL INDEX, DISABLE GEAR STICK, FORCE GEARSTICK DEVICE ID</td></tr><tr><td><strong>Model3-Vulkan</strong></td><td>Sega Model 3</td><td><code>model3vulkan_wheels.yml</code>, else <code>model3_wheels.yml</code></td><td>DISABLE GEAR STICK, FORCE WHEEL INDEX, FORCE GEARSTICK DEVICE ID</td></tr><tr><td><strong>Odin</strong></td><td>Hikaru (NASCAR Arcade), Gaelco (ATV Track, Smashing Drive)</td><td><code>odin_wheels.yml</code>, else <code>model3_wheels.yml</code> (without mapping, Odin steers with the first axis)</td><td>WHEEL ROTATION, FORCE FEEDBACK STRENGTH</td></tr><tr><td><strong>Linuxloader</strong></td><td>Sega Lindbergh</td><td><code>linuxloader_wheels.yml</code> (XInput wheels, seen as gamepads, use the controller mapping)</td><td></td></tr><tr><td><strong>Flycast</strong></td><td>Dreamcast, Naomi, Atomiswave</td><td><code>flycast_wheels.yml</code> (Dreamcast), <code>flycast_racing_wheels.yml</code> (Dreamcast with <strong>USE RACING CONTROLLER</strong>), <code>flycast_arcade_wheels.yml</code> (arcade)</td><td>USE RACING CONTROLLER, WHEEL BUTTON LAYOUT</td></tr><tr><td><strong>PCSX2</strong></td><td>PlayStation 2</td><td><code>pcsx2_wheels.yml</code></td><td>WHEEL TYPE PLAYER 1, ENABLE FORCE FEEDBACK, SIMULATE WHEEL WITH GAMEPAD…</td></tr><tr><td><strong>PCSX2x6</strong></td><td>Namco System 246/256</td><td><code>pcsx2x6_wheels.yml</code></td><td>ENABLE FORCE FEEDBACK</td></tr><tr><td><strong>TeknoParrot</strong></td><td>PC-based arcade</td><td><code>teknoparrot_wheels.yml</code></td><td>COIN &#x26; START BUTTONS, TEST &#x26; SERVICE BUTTONS, CUSTOM PROFILE…</td></tr><tr><td><strong>RetroArch - lr-flycast</strong></td><td>Dreamcast, Naomi, Atomiswave</td><td><code>libretro_flycast_wheels.yml</code> (not provided yet)</td><td>ENABLE WHEEL</td></tr></tbody></table>

### Wheels with a ready-made mapping

<table><thead><tr><th>Wheel</th><th width="70.5" align="center">Model 2</th><th width="76.75" align="center">Keisho</th><th width="104.25" align="center">Supermodel, Model3-Vulkan, Odin</th><th width="74.25" align="center">Linuxloader</th><th width="76.75" align="center">Flycast</th><th width="85.5" align="center">PCSX2 / PCSX2x6</th><th align="center">TeknoParrot</th></tr></thead><tbody><tr><td>Logitech G29</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Logitech G920</td><td align="center">✔</td><td align="center">✔</td><td align="center"></td><td align="center">✔</td><td align="center">✔</td><td align="center"></td><td align="center">✔</td></tr><tr><td>Logitech G923 (PlayStation)</td><td align="center">✔</td><td align="center">✔</td><td align="center"></td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Logitech G923 (Xbox)</td><td align="center">✔</td><td align="center">✔</td><td align="center"></td><td align="center">✔</td><td align="center">✔</td><td align="center"></td><td align="center">✔</td></tr><tr><td>Logitech Driving Force GT</td><td align="center"></td><td align="center">✔</td><td align="center"></td><td align="center"></td><td align="center">✔</td><td align="center">✔</td><td align="center"></td></tr><tr><td>Thrustmaster T300RS (PS3 mode)</td><td align="center">✔</td><td align="center">✔</td><td align="center"></td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Moza R5</td><td align="center"></td><td align="center">✔</td><td align="center"></td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td></tr></tbody></table>

TeknoParrot and Linuxloader also have a mapping for many other wheels (Logitech G Pro, Thrustmaster T150 / TMX / T248 / T300RS PS4 / T500RS / TX / TS-XW, Fanatec, Moza R9 / R12 / R16, Simucube, Simagic, Asetek, Cammus, PXN V9) and a `default` mapping used for the other detected wheels.

Supermodel, Model3-Vulkan and Odin use the same `model3_wheels.yml` file. Model3-Vulkan and Odin first read `model3vulkan_wheels.yml` / `odin_wheels.yml` when it exists (not provided by RetroBat). With a wheel set up by RetroBat, Model3-Vulkan turns off the steering smoothing and sensitivity meant for gamepads: the steering follows the wheel without filtering.

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

<table><thead><tr><th width="215.75">File</th><th>Buttons</th><th>Axes</th></tr></thead><tbody><tr><td><code>model2_wheels.yml</code></td><td><code>button0</code>, <code>button1</code>… (from 0)</td><td><code>axis0</code>, <code>axisinv0</code>…</td></tr><tr><td><code>keisho_wheels.yml</code></td><td><code>0</code>, <code>1</code>… (from 0), <code>-1</code> = none</td><td>Detected by Keisho (calibrate them in the Keisho menu)</td></tr><tr><td><code>model3_wheels.yml</code>, <code>linuxloader_wheels.yml</code></td><td><code>BUTTON1</code>, <code>BUTTON2</code>… (from 1), <code>POV1_UP</code>…</td><td><code>XAXIS_NEG</code>, <code>RZAXIS_POS</code>, <code>SLIDER1</code>…</td></tr></tbody></table>

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
