# Special controllers

For some systems, RetroBat recognises controllers that reproduce the original console pad (N64 controllers, Genesis/Saturn-style pads, GameCube adapters…) and maps them **button for button**, so that each button does exactly what it did on the original console.

These mappings are stored in `.json` files. RetroBat already provides mappings for the controllers listed on this page, and you can add your own.

{% hint style="info" %}
When a special controller is detected, the mapping you configured in RetroBat (CONTROLLER SETTINGS) is ignored for this controller: the mapping from the `.json` file is used instead.
{% endhint %}

## How it works

RetroBat identifies the controller by its **GUID** (and, for RetroArch, by the input driver in use). Two cases exist:

<table><thead><tr><th width="151.5">Case</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>Automatic</strong></td><td>Controllers with a unique identifier (adapters, 8BitDo pads in D-input mode, Nintendo Switch Online N64 controller…). The special mapping is applied as soon as the controller is connected.</td></tr><tr><td><strong>Needs activation</strong></td><td>Controllers that share their identifier with standard pads (for example an 8BitDo M30 in X-input mode is seen as an Xbox 360 controller). The special mapping is only applied if you enable the matching option in the system's advanced configuration, <strong>CONTROLS</strong> submenu.</td></tr></tbody></table>

{% hint style="warning" %}
Only enable the **USE xxx-LIKE CONTROLLER** options when you actually play with one of the controllers listed below. Otherwise, a standard Xbox or Switch controller may receive the special mapping and its buttons will be wrong.
{% endhint %}

To check that a special mapping was applied, open `emulationstation\emulatorLauncher.log` after launching a game and look for a line like `Performing specific … mapping for <controller name>`.

## Mapping files

The files are located in `system\resources\inputmapping`:

<table><thead><tr><th width="220.25">File</th><th>Systems</th></tr></thead><tbody><tr><td><code>n64Controllers.json</code></td><td>Nintendo 64</td></tr><tr><td><code>mdControllers.json</code></td><td>Mega Drive / Genesis, Mega-CD / Sega CD, 32X</td></tr><tr><td><code>saturnControllers.json</code></td><td>Saturn</td></tr><tr><td><code>GCControllers.json</code></td><td>GameCube</td></tr><tr><td><code>3doControllers.json</code></td><td>3DO</td></tr><tr><td><code>arcade_sticks.json</code></td><td>Custom arcade stick mapping (RetroArch)</td></tr><tr><td><code>kbpads\*.yml</code></td><td>Arcade sticks recognised as a keyboard (I-PAC2, X-Arcade Tankstick)</td></tr></tbody></table>

{% hint style="info" %}
If you modify a file, copy it to `user\inputmapping` (`user\inputmapping\kbpads` for `.yml` files) and edit the copy. RetroBat reads this folder first, and it is not overwritten by updates.
{% endhint %}

## Nintendo 64

<table><thead><tr><th>Controller</th><th width="91.75" align="center">RetroArch</th><th width="86.75" align="center">Ares</th><th width="85.5" align="center">BizHawk</th><th width="79.25" align="center">RMG</th><th width="90.5" align="center">Simple64</th><th width="111" align="center">Ship ports</th></tr></thead><tbody><tr><td>Nintendo Switch Online N64 Controller</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td></tr><tr><td>8BitDo N64 Controller</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">–</td></tr><tr><td>Mayflash N64 adapter</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td></tr><tr><td>Raphnet N64 adapter</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td></tr><tr><td>SWITCH CO.LTD. USB Controller (D-input/SDL)</td><td align="center">Auto</td><td align="center">–</td><td align="center">Auto</td><td align="center">–</td><td align="center">–</td><td align="center">–</td></tr><tr><td>SWITCH CO.LTD. USB Controller (X-input)</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">–</td></tr></tbody></table>

* **RetroArch**: Mupen64Plus-Next and ParaLLEl N64 cores.
* **BizHawk**: Ares64 and Mupen64Plus cores.
* **RMG**: Rosalie's Mupen GUI (Mupen64Plus).
* **Ship ports**: Ship of Harkinian, 2 Ship 2 Harkinian, Ghostship.
* **Option**: **USE N64-LIKE CONTROLLER** (system advanced configuration > CONTROLS).

### N64 TRIGGER INVERT

On controllers with two triggers (Nintendo Switch Online N64 controller, 8BitDo N64 controller), the **Z** button is mapped to the left trigger by default. Enable **N64 TRIGGER INVERT** to use the right trigger instead.

This is a global option: **GAME SETTINGS > CONTROLS > SPECIAL CONTROLLERS > N64 TRIGGER INVERT**. It works with RetroArch, Ares, BizHawk, RMG and Simple64.

<div align="left"><figure><img src="../../../.gitbook/assets/image (306).png" alt=""><figcaption></figcaption></figure></div>

## Mega Drive / Genesis (and Mega-CD, 32X)

Supported controller: **8BitDo M30** (the mode depends on how it is connected and switched on; see the [Gamepads](./) page).

<table><thead><tr><th width="252.75">M30 mode</th><th>Activation</th></tr></thead><tbody><tr><td>X-input</td><td>Option</td></tr><tr><td>Switch</td><td>Option</td></tr><tr><td>D-input</td><td>Auto</td></tr><tr><td>2.4G receiver</td><td>Auto</td></tr></tbody></table>

* **Emulators**: RetroArch (Genesis Plus GX, Genesis Plus GX Wide, Genesis Plus GX Expanded and PicoDrive cores), Ares, BizHawk (Genplus-gx, PicoDrive), BlastEm, Jgenesis, Kega Fusion, Mednafen.
* **Option**: **USE GENESIS-LIKE CONTROLLER** (system advanced configuration > CONTROLS). In Kega Fusion, the option lets you choose **YES (DPAD)** or **YES (ANALOG)**.

## Saturn

Supported controller: **8BitDo M30**.

<table><thead><tr><th width="95.5">M30 mode</th><th width="90.5" align="center">RetroArch</th><th width="83" align="center">BizHawk</th><th width="90.5" align="center">Mednafen</th><th width="75.5" align="center">Kronos</th><th width="104.25" align="center">SSF</th><th width="113" align="center">YabaSanshiro</th><th align="center">Ymir</th></tr></thead><tbody><tr><td>X-input</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td></tr><tr><td>Switch</td><td align="center">Option</td><td align="center">Option</td><td align="center">–</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td></tr><tr><td>D-input</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Option</td><td align="center">Auto</td><td align="center">Option</td><td align="center">Option</td></tr><tr><td>2.4G receiver</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Not supported</td><td align="center">Auto</td><td align="center">Not supported</td></tr></tbody></table>

* **RetroArch**: Beetle Saturn, Kronos, YabaSanshiro, Yabause and Ymir cores.
* **BizHawk**: Saturnus core.
* **Option**: **USE SATURN-LIKE CONTROLLER** (system advanced configuration > CONTROLS). In Kronos, SSF and YabaSanshiro, choose **YES (DPAD)** or **YES (ANALOG)**.

## GameCube

Special mappings for GameCube controllers are only available with **Dolphin** (standalone), for the GameCube and Triforce systems.

| Adapter                                        | Activation |
| ---------------------------------------------- | ---------- |
| Mayflash GameCube Controller Adapter (PC mode) | Auto       |
| raphnet Dual GameCube to USB adapter           | Auto       |

The **USE GAMECUBE-LIKE CONTROLLER** option is available for entries that need activation (none in the provided file at the moment).

### Wii U GameCube adapter (official or Mayflash in Wii U mode)

Dolphin can use this adapter directly (rumble supported, all 4 ports):

1. Install the WinUSB driver for the adapter with [Zadig](https://zadig.akeo.ie/), as explained in the [Dolphin guide](https://dolphin-emu.org/docs/guides/how-use-official-gc-controller-adapter-wii-u/).
2. In the GameCube system advanced configuration > CONTROLS, set **PLAYER 1 CONTROLLER TYPE** (and players 2 to 4 if needed) to **GAMECUBE ADAPTER**.

## 3DO

Supported controller: **8BitDo M30**, with the **RetroArch Opera** core.

<table><thead><tr><th width="274">M30 mode</th><th>Activation</th></tr></thead><tbody><tr><td>X-input</td><td>Option</td></tr><tr><td>Switch</td><td>Option</td></tr><tr><td>D-input</td><td>Auto</td></tr><tr><td>2.4G receiver</td><td>Auto</td></tr></tbody></table>

**Option**: **USE 3DO-LIKE CONTROLLER** (system advanced configuration > CONTROLS).

## Wiimotes (Wii)

With **Dolphin** (standalone), the **WIIMOTE TYPE** option (Wii system advanced configuration > CONTROLS) defines how Wii controllers are handled:

<table><thead><tr><th width="225.25">Value</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>REAL</strong> (default)</td><td>Real Wiimotes, connected via Bluetooth or with a Mayflash DolphinBar in <strong>mode 4</strong>.</td></tr><tr><td><strong>EMULATED</strong></td><td>Your gamepads act as Wiimotes. Choose the emulated device (Wiimote, sideways Wiimote, Nunchuk, Classic Controller…) with <strong>EMULATED DEVICES</strong>.</td></tr><tr><td><strong>REAL AS EMULATED</strong> / <strong>(NUNCHUK)</strong> / <strong>(CC)</strong></td><td>A real Wiimote is used through Dolphin's emulated Wiimote, without extension, with a Nunchuk or with a Classic Controller.</td></tr></tbody></table>

Other useful options:

* **NUMBER OF WIIMOTES**: forces the number of Wiimotes the game detects (set it to 1 for games that switch to multiplayer as soon as several controllers are connected).
* **USE GAMECUBE CONTROLLERS**: also configures your gamepads as GameCube controllers, for Wii games that support them.
* **DISABLE WIIMOTE CONTINUOUS SCANNING**: RetroBat automatically disables continuous scanning when a DolphinBar is detected, when Wiimotes are emulated, and for GameCube games. Set this option to force the behaviour.

To use a Wiimote as a lightgun, see the [Wiimote and DolphinBar](../lightguns/wiimoteandbar.md) page.

## Arcade sticks recognised as a keyboard (I-PAC2, X-Arcade Tankstick)

Some arcade sticks and encoders are seen by Windows as a **keyboard** (Ultimarc I-PAC2, X-Arcade Tankstick…). Their keys follow the MAME defaults (player 1: arrows, Left Ctrl, Left Alt, Space…, Start `1`, Coin `5`; player 2: `R`/`F`/`D`/`G`, `A`, `S`…, Start `2`, Coin `6`).

<table><thead><tr><th width="186.5">Emulator</th><th>How to configure</th></tr></thead><tbody><tr><td><strong>RetroArch</strong></td><td><strong>GAME SETTINGS > RETROARCH OPTIONS > CONTROLS > CONFIGURE SPECIAL KEYBOARD STICK</strong>: choose <strong>IPAC2</strong> or <strong>X-ARCADE TANKSTICK</strong>. Applies to all RetroArch games.</td></tr><tr><td><strong>MAME</strong> (standalone, GroovyMAME and HBMame)</td><td>System advanced configuration > CONTROLS > <strong>CONTROLLER PROFILE</strong>: choose <strong>IPAC2</strong> or <strong>X-ARCADE</strong>. The profiles are located in <code>saves\mame\ctrlr</code>; you can also create your own profiles (<strong>CUSTOM 1</strong> to <strong>6</strong>) or one profile per game (<strong>GAME SPECIFIC</strong>, file named after the rom).</td></tr><tr><td><strong>PCSX2x6</strong> (Namco System 246/256)</td><td>System advanced configuration > CONTROLS > <strong>CONFIGURE SPECIAL KEYBOARD STICK</strong>.</td></tr></tbody></table>

The RetroArch and PCSX2x6 mappings come from `kbpads\libretro_<type>.yml` and `kbpads\pcsx2x6_<type>.yml`. Each file has a `default` block, and you can add blocks named after a **system**, a **core** (RetroArch only) or a **rom** (file name without extension). They are applied in this order: `default` → system → core → game, and you only need to list what changes.

Example (`user\inputmapping\kbpads\libretro_ipac2.yml`):

```yaml
default:
  input_player1_a: ctrl
  input_player1_b: alt
  # ...
snes:
  input_player1_a: alt
  input_player1_b: ctrl
```

## Custom arcade stick mapping (RetroArch)

For an arcade stick recognised as a **gamepad**, you can define a dedicated RetroArch mapping:

1. Copy `system\resources\inputmapping\arcade_sticks.json` to `user\inputmapping`.
2. Replace the example entry (`Arcade Stick Test`) with the GUID of your stick and your mapping.
3. Enable **GAME SETTINGS > RETROARCH OPTIONS > CONTROLS > USE CUSTOM ARCADE STICK MAPPING**.

## Adding your own controller

1. Copy the `.json` file of the system to `user\inputmapping`.
2. Find the GUID of your controller: it is the `deviceGUID` value in `emulationstation\.emulationstation\es_input.cfg`.
3. Duplicate an existing entry **for the same emulator** (the mapping format differs for each emulator) and change `Name`, `Guid` and `Mapping`. Main fields:

<table><thead><tr><th width="154">Field</th><th>Description</th></tr></thead><tbody><tr><td><code>Emulator</code></td><td>Emulator the entry applies to (<code>libretro</code>, <code>ares</code>, <code>bizhawk</code>, <code>mupen64</code>, <code>dolphin</code>…).</td></tr><tr><td><code>Guid</code></td><td>Controller GUID; several GUIDs can be separated with commas.</td></tr><tr><td><code>Driver</code></td><td>RetroArch only: input driver (<code>xinput</code>, <code>dinput</code>, <code>sdl2</code>). Leave empty if not needed.</td></tr><tr><td><code>Mapping</code></td><td>Button mapping, in the emulator's format.</td></tr><tr><td><code>HotKeyMapping</code></td><td>RetroArch only: hotkeys for player 1 with this controller.</td></tr><tr><td><code>ControllerInfo</code></td><td>Extra settings: <code>needActivationSwitch: "true"</code> makes the mapping depend on the USE xxx-LIKE CONTROLLER option; <code>switch_trigger</code> is the button used by N64 TRIGGER INVERT.</td></tr></tbody></table>

4. Launch a game and check `emulationstation\emulatorLauncher.log`.

{% hint style="success" %}
Your mapping works? Share it on the RetroBat Discord or on GitHub so it can be added to RetroBat!
{% endhint %}
