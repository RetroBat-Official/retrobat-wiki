# Keisho controller mapping

## Overview

This page explains how to change the buttons of **Keisho** (formerly sm2-emu), the emulator of the [**Sega Model 1**](../../systems-and-emulators/supported-game-systems/arcade/sega/sega-model-1.md), [**Sega Model 2**](../../systems-and-emulators/supported-game-systems/arcade/sega/sega-model-2.md) and [**Sega Model 3**](../../systems-and-emulators/supported-game-systems/arcade/sega/sega-model-3.md) systems.

At each launch, RetroBat writes the controller configuration to `emulators\keisho\keisho.ini`, from two files:

<table><thead><tr><th width="236.5">File</th><th>Content</th></tr></thead><tbody><tr><td><code>keisho.yml</code></td><td>Controller buttons, per game and per layout</td></tr><tr><td><code>keisho_wheels.yml</code></td><td>Wheel buttons, per wheel type</td></tr></tbody></table>

Both files are shipped in `system\resources\inputmapping` (and `wheels` for the wheel). To change them, copy them to `user\inputmapping`: your copy is then used instead of the RetroBat file.

{% hint style="warning" %}
The per-game layouts saved in the Keisho menu (**Controls > Gamepad**) are erased at each launch, so that the RetroBat layout applies. To keep yours, use `keisho.yml`, or turn off **AUTOCONFIGURE CONTROLLERS**.
{% endhint %}

## Automatic configuration

Without changing any file, RetroBat sets up Keisho this way for players 1 and 2:

<table><thead><tr><th width="212.75">Control</th><th>Controller</th></tr></thead><tbody><tr><td>Directions</td><td>D-pad and left stick</td></tr><tr><td>Start, coin</td><td>START, SELECT</td></tr><tr><td>Gear down / up</td><td>L1 / R1</td></tr><tr><td>Steering, aiming</td><td>Left stick (aiming: either stick)</td></tr><tr><td>Accelerator, brake</td><td>R2, L2</td></tr><tr><td>Service, Test</td><td>L3, R3 (keyboard: 9, 0)</td></tr><tr><td>Buttons 1 to 4</td><td>Depends on the game, see <code>keisho.yml</code></td></tr></tbody></table>

The **CONTROLS** submenu options (stick deadzone, rumble) and **CONTROLLER LAYOUT** (arcade sticks) also apply. With **AUTOCONFIGURE CONTROLLERS** turned off, RetroBat no longer touches the controllers: Keisho keeps the settings of its menu.

## The keisho.yml file

### Search order

The file holds containers. RetroBat uses the first one found, in this order:

1. with a **CONTROLLER LAYOUT** selected: `<game>_<layout>`, then `<family>_<layout>`, then `default_<layout>`;
2. then `<game>`, `<family>`, `default`.

* `<game>` is the romset name (`vf2a`), `<family>` the name of its parent game (`vf2`): a parent game container is therefore used by all its clones.
* `<layout>` is `modern8`, `8alternative` or `6alternative` (CLASSIC 8 BUTTONS uses `6alternative`).
* An arcade stick layout selected by the user comes before the gamepad layout of the game.

### Keys and values

The **key** is the position of the button on the controller:

<table><thead><tr><th width="274">Key</th><th>Button</th></tr></thead><tbody><tr><td><code>south</code>, <code>east</code>, <code>west</code>, <code>north</code></td><td>SOUTH, EAST, WEST, NORTH</td></tr><tr><td><code>l1</code>, <code>r1</code>, <code>l2</code>, <code>r2</code></td><td>Shoulder buttons and triggers</td></tr><tr><td><code>l3</code>, <code>r3</code></td><td>Stick clicks</td></tr><tr><td><code>select</code>, <code>start</code></td><td>SELECT, START</td></tr><tr><td><code>up</code>, <code>down</code>, <code>left</code>, <code>right</code></td><td>D-pad</td></tr></tbody></table>

The **value** is the Keisho control: `Button1` to `Button4`, `Up`, `Down`, `Left`, `Right`, `Start`, `Coin`, `GearUp`, `GearDown`.

* One button can drive several controls, separated with a comma: `west: Button1, Coin`.
* A control can only be driven by one button: if it is listed twice, the first one wins.
* Controls missing from the container keep their default button (directions, Start, coin, gears). Buttons 1 to 4 that are not listed have no button.

Example, Virtua Fighter 2 with guard on EAST:

```yaml
vf2:
  west: Button1
  north: Button2
  east: Button3
```

### What Button1 to Button4 stand for

| Games                                                                   | Button1         | Button2                    | Button3    | Button4   |
| ----------------------------------------------------------------------- | --------------- | -------------------------- | ---------- | --------- |
| Virtua Fighter, Virtua Fighter 2, Last Bronx, Fighting Vipers (Model 2) | Punch           | Kick                       | Guard      | (Guard 2) |
| Dead or Alive                                                           | Hold            | Punch                      | Kick       | —         |
| Sonic the Fighters                                                      | Punch           | Kick                       | Barrier    | —         |
| Virtua Fighter 3, Fighting Vipers 2                                     | Punch           | Kick                       | Guard      | Escape    |
| Spikeout                                                                | Beat            | Charge                     | Shift      | Jump      |
| Virtua Striker, Virtua Striker 2                                        | Long Pass       | Shoot                      | Short Pass | —         |
| Dynamite Cop                                                            | Punch           | Kick                       | Jump       | —         |
| Pilot Kids, Zero Gunner                                                 | Shot            | Bomb                       | —          | —         |
| Gun games                                                               | Shoot (also R2) | Reload / missile (also L2) | —          | —         |
| Driving games                                                           | VR1             | VR2                        | VR3        | VR4       |
| Harley-Davidson                                                         | Music select    | View                       | —          | —         |
| Star Wars Arcade                                                        | Laser           | Torpedo                    | —          | —         |
| Star Wars Trilogy                                                       | Event 1         | Event 2                    | —          | —         |
| Sega Bass Fishing                                                       | Cast            | Select                     | —          | —         |
| Magical Truck Adventure                                                 | Pedal           | —                          | —          | —         |

The layouts shipped with RetroBat are described on the [**Sega Model 1**](../../systems-and-emulators/supported-game-systems/arcade/sega/sega-model-1.md), [**Sega Model 2**](../../systems-and-emulators/supported-game-systems/arcade/sega/sega-model-2.md) and [**Sega Model 3**](../../systems-and-emulators/supported-game-systems/arcade/sega/sega-model-3.md) pages. For Virtua Fighter 3, Fighting Vipers 2 and Spikeout, they are the same as in `supermodel.yml` (Supermodel).

### Limits

Some controls cannot be set in `keisho.yml`:

* the view buttons (VR1 to VR4) of driving games are always buttons 1 to 4;
* Virtual On, Virtual On 2, Desert Tank, Sky Target, Ski Super G, Water Ski and Ski Champ use a Keisho layout of their own;
* Star Wars Trilogy fires with the triggers (Keisho moves the Up / Down controls there); Sega Bass Fishing uses the triggers for the reel and the line tension;
* axes (steering, aiming, pedals) are detected by Keisho.

For more details on arcade layouts, see the [**Arcade Guide**](../../systems-and-emulators/arcade-guide.md) page.

## The keisho\_wheels.yml file (wheels)

With **WHEELS > ENABLE WHEEL**, RetroBat sets up the wheel buttons from `system\resources\inputmapping\wheels\keisho_wheels.yml` (editable copy: `user\inputmapping\keisho_wheels.yml`).

* Each container is named after a wheel type known by RetroBat: `LogitechG29`, `LogitechG920`, `LogitechG923PS`, `LogitechG923X`, `LogitechDrivingForceGT`, `ThrustmasterT300RSPS3`, `MozaR5`.
* The **key** is the control: `Start`, `Coin`, `Button1` to `Button4` (also VR1 to VR4), `GearUp`, `GearDown`, `Test`, `Service`, `Menu`, `Gear1` to `Gear4`, `GearNeutral`.
* The **value** is the wheel button number (DirectInput order, the first button is 0); `-1` leaves the control without a button.
* `Gear1` to `Gear4` are the H shifter positions; they are not written with the **DISABLE GEAR STICK** option.
* Steering and pedals are always detected by Keisho; calibrate them in its menu if needed.
* A wheel without a container keeps the buttons set in the Keisho menu (**Controls > Wheel**).

Example:

```yaml
LogitechG29:
  Start: 9
  Coin: 8
  Button1: 0
  Button2: 2
  Button3: 1
  Button4: 3
  GearUp: 4
  GearDown: 5
```

For the list of wheel types, see the [**Wheels**](../supported-controllers/wheels.md) page.

## Known issues

<table><thead><tr><th width="311.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>My changes in <code>keisho.yml</code> have no effect</td><td>Check that the file is in <code>user\inputmapping</code>, the container name (romset or parent game) and the selected <strong>CONTROLLER LAYOUT</strong> (a <code>_&#x3C;layout></code> container comes first).</td></tr><tr><td>The layout set in the Keisho menu is lost</td><td>RetroBat erases it at each launch: use <code>keisho.yml</code>, or turn off <strong>AUTOCONFIGURE CONTROLLERS</strong>.</td></tr><tr><td>A button does nothing</td><td>A control can only be on one button: check that it is not already listed higher in the container.</td></tr></tbody></table>
