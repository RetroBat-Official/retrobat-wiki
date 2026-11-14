# m2emulator controller mapping

## Overview

This page explains how to set up the controls of **m2emulator**, the default Model 2 emulator of RetroBat, yourself. For the other Model 2 emulators (Keisho, Supermodel, MAME), see the [**Sega Model 2**](../../systems-and-emulators/supported-game-systems/arcade/sega/sega-model-2.md) page.

m2emulator saves the keys of each game in a `.input` file in the `emulators\m2emulator\CFG` folder. RetroBat offers three ways to fill it:

<table><thead><tr><th width="164.5">Method</th><th width="370.75">For whom</th><th>File</th></tr></thead><tbody><tr><td><strong>Automatic configuration</strong> (default)</td><td>Most players: RetroBat writes the keys of each game at each launch.</td><td>—</td></tr><tr><td><strong>Per-game mapping</strong></td><td>Moving the buttons of a fighting game or a "standard" game, while keeping the automatic configuration.</td><td><code>model2.yml</code></td></tr><tr><td><strong>Templates</strong></td><td>Using your own configuration, made in m2emulator, for a given game.</td><td><code>templatescfg\&#x3C;driver>\&#x3C;game>.input</code></td></tr></tbody></table>

Wheels have their own file, `model2_wheels.yml` (see [**Wheels**](model2-controller-mapping.md#wheels-model2_wheels.yml) below).

## Automatic configuration

At each launch, RetroBat writes the `.input` file of the game with the layout described on the [**Sega Model 2**](../../systems-and-emulators/supported-game-systems/arcade/sega/sega-model-2.md) page (controls per game type). The settings are in the system advanced settings, **CONTROLS** submenu:

<table><thead><tr><th width="279">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>DRIVERS > CONTROLLER</strong></td><td>XINPUT (default) for Xbox and compatible controllers, DINPUT for the others. RetroBat also switches to DINPUT when no XInput controller is found.</td></tr><tr><td><strong>CONTROLLER LAYOUT</strong></td><td>Arcade stick layouts (modern8, 8alternative, 6alternative), for fighting games and "standard" games.</td></tr><tr><td><strong>USE SHOULDER BUTTONS FOR RACING GAMES</strong></td><td>Accelerator and brake on R1 / L1 (automatic gearbox only).</td></tr><tr><td><strong>SWITCH JOYPAD INDEX</strong>, <strong>FORCE PLAYER 1 PAD INDEX</strong> / <strong>PLAYER 2</strong></td><td>Choice of each player's controller.</td></tr></tbody></table>

<div align="left"><figure><img src="../../.gitbook/assets/image (559).png" alt=""><figcaption></figcaption></figure></div>

RetroBat only configures automatically the games listed on the **Sega Model 2** page. For another game, it leaves the `.input` file alone: set the keys once in m2emulator (**Game > Configure Controls**, see step 1 of the templates), and they are kept.

With **AUTOCONFIGURE CONTROLLERS** turned off, RetroBat does not change any `.input` file (guns are still configured).

## Per-game mapping (model2.yml)

The `model2.yml` file moves the buttons of fighting games and "standard" games, without leaving the automatic configuration: RetroBat still handles directions, Start, coin, Service and Test, the driver and the controller indexes.

1. Copy `system\resources\inputmapping\model2.yml` to `user\inputmapping`. Your copy is then used instead of the RetroBat file.
2. Edit the game container, then start the game: the `.input` file is written again with your buttons.

**Games and available actions** (clones use the container of their parent game):

<table><thead><tr><th width="192">Game</th><th width="180.5">Container</th><th>Actions</th></tr></thead><tbody><tr><td>Dead or Alive</td><td><code>doa</code></td><td>Hold, Punch, Kick</td></tr><tr><td>Fighting Vipers</td><td><code>fvipers</code></td><td>Punch, Kick, Guard, Guard 2</td></tr><tr><td>Last Bronx</td><td><code>lastbrnx</code></td><td>Punch, Kick, Guard</td></tr><tr><td>Sonic the Fighters</td><td><code>schamp</code></td><td>Punch, Kick, Barrier</td></tr><tr><td>Virtua Fighter 2</td><td><code>vf2</code></td><td>Punch, Kick, Guard</td></tr><tr><td>Dynamite Cop</td><td><code>dynamcop</code></td><td>Punch, Kick, Jump</td></tr><tr><td>Pilot Kids</td><td><code>pltkids</code></td><td>Shot, Bomb</td></tr><tr><td>Virtua Striker</td><td><code>vstriker</code></td><td>Short Pass, Long Pass, Shoot</td></tr><tr><td>Zero Gunner</td><td><code>zerogun</code></td><td>Shot, Bomb</td></tr></tbody></table>

**Containers**: the container is named after the parent game (`vf2`). You can add one container per layout, `<game>_modern8`, `<game>_8alternative` or `<game>_6alternative`, used when this **CONTROLLER LAYOUT** is selected (CLASSIC 8 BUTTONS uses `_6alternative`). RetroBat looks for `<game>_<layout>`, then `<game>`; without a container, it keeps its default layout.

**Values**: the position of the button on the controller:

<table><thead><tr><th width="316.5">Value</th><th>Button</th></tr></thead><tbody><tr><td><code>a</code></td><td>SOUTH</td></tr><tr><td><code>b</code></td><td>EAST</td></tr><tr><td><code>x</code></td><td>WEST</td></tr><tr><td><code>y</code></td><td>NORTH</td></tr><tr><td><code>leftshoulder</code> / <code>rightshoulder</code></td><td>L1 / R1</td></tr><tr><td><code>leftstick</code> / <code>rightstick</code></td><td>left / right stick click</td></tr><tr><td><code>back</code> / <code>start</code></td><td>SELECT / START</td></tr></tbody></table>

An action missing from the container has no button.

Example, Virtua Fighter 2 with guard on EAST and kick on SOUTH:

```yaml
vf2:
  Guard: b
  Punch: x
  Kick: a
```

For more details on arcade layouts, see the [**Arcade Guide**](../../systems-and-emulators/arcade-guide.md) page.

## Templates (configuration made in m2emulator)

This method replaces the automatic configuration with a file prepared in m2emulator. It applies to every game that has a template, except when guns are enabled.

### Step 1: create the game configuration

1. In the system advanced settings, select the driver of your controller: **DRIVERS > CONTROLLER > XINPUT** (Xbox and compatible controllers) or **DINPUT** (the others).

<div align="left"><figure><img src="../../.gitbook/assets/image (563).png" alt=""><figcaption></figcaption></figure></div>

2. Start the game, then press **ALT + ENTER** to leave fullscreen and show the m2emulator menu.
3. Open **Game > Configure Controls** and set the keys.

<div align="left"><figure><img src="../../.gitbook/assets/image (562).png" alt=""><figcaption></figcaption></figure></div>

4. Close the window and exit the emulator: the `<game>.input` file is saved in `emulators\m2emulator\CFG`.

<div align="left"><figure><img src="../../.gitbook/assets/image (560).png" alt=""><figcaption></figcaption></figure></div>

### Step 2: copy the file to the templates folder

Copy the file to the folder of the driver selected in step 1:

* `emulators\m2emulator\templatescfg\xinput` for XINPUT;
* `emulators\m2emulator\templatescfg\dinput` for DINPUT.

<div align="left"><figure><img src="../../.gitbook/assets/image (561).png" alt=""><figcaption></figcaption></figure></div>

The template must have **the name of the parent game**: `daytona.input` is also used for `daytonas` or `daytonam`. RetroBat already ships templates for XInput controllers, and for PlayStation 4 and 5 controllers in DInput: you can replace them with your own.

### Step 3: turn on templates

In the system advanced settings, select **CONTROLS > TYPE OF AUTOCONFIGURATION > TEMPLATES**. At each launch, RetroBat copies the game template to `emulators\m2emulator\CFG`.

<div align="left"><figure><img src="../../.gitbook/assets/image (564).png" alt=""><figcaption></figcaption></figure></div>

## Wheels (model2\_wheels.yml)

With **WHEELS > ENABLE WHEEL**, RetroBat sets up the wheel from `system\resources\inputmapping\wheels\model2_wheels.yml`. Each container is named after a wheel type known by RetroBat (`LogitechG29`, `LogitechG920`, `LogitechG923PS`, `LogitechG923X`, `ThrustmasterT300RSPS3`…). A `<wheel>_<game>` container (for example `LogitechG29_daytona`) has priority for one game.

<table><thead><tr><th width="359">Key</th><th>Role</th></tr></thead><tbody><tr><td><code>Steer</code>, <code>Throttle</code>, <code>Brake</code></td><td>Wheel and pedal axes: <code>axis0</code>, <code>axis1</code>… (<code>axisinv1</code> reverses the axis)</td></tr><tr><td><code>Up</code>, <code>Down</code>, <code>Left</code>, <code>Right</code></td><td>D-pad: <code>hatup</code>, <code>hatdown</code>…</td></tr><tr><td><code>ShiftUp</code>, <code>ShiftDown</code>, <code>Gear1</code> to <code>Gear4</code>, <code>GearN</code></td><td>Paddles and shifter: <code>button4</code>…</td></tr><tr><td><code>South</code>, <code>East</code>, <code>West</code>, <code>North</code>, <code>Start</code>, <code>Select</code>, <code>Service</code>, <code>Test</code></td><td>Buttons</td></tr><tr><td><code>DeportedShifter</code></td><td><code>true</code> only for Thrustmaster wheels whose shifter is seen as a separate device</td></tr></tbody></table>

Your own version goes in `user\inputmapping\model2_wheels.yml` (it has priority over the RetroBat file). For the list of wheel types and the other options, see the [**Wheels**](../supported-controllers/wheels.md) page.

## Known issues

<table><thead><tr><th width="359">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>My template is not used</td><td>Check its name (the parent game's), its folder (the selected driver's), the <strong>TEMPLATES</strong> option, and that guns are not enabled.</td></tr><tr><td>My buttons change at each launch</td><td>The automatic configuration rewrites the <code>.input</code> file: use <code>model2.yml</code> or templates, or turn off <strong>AUTOCONFIGURE CONTROLLERS</strong>.</td></tr><tr><td><code>model2.yml</code> has no effect on a driving or gun game</td><td>Per-game mapping only applies to the fighting games and "standard" games <a href="model2-controller-mapping.md#per-game-mapping-model2.yml">listed above</a>.</td></tr></tbody></table>
