# MAME controller mapping

## Overview

Every arcade cabinet had its own control panel: one button, six buttons, a wheel, a trackball… So there is no controller setup that fits all MAME games.

RetroBat sets the buttons automatically, game by game, for **lr-mame**, **mame2003\_plus**, **MAME** and **GroovyMAME**. This page explains how that setup is chosen and how to change it: layout for an arcade stick, fixing one game, IPAC2 or X-Arcade panel, personal profile.

The table of default buttons and the hotkeys are on the [**MAME**](../../systems-and-emulators/supported-game-systems/arcade/mame.md) page.

## How RetroBat chooses the buttons

When a game starts, RetroBat looks in this order for:

1. **your configuration** of the game, in `user\inputmapping`;
2. **the configuration of the game shipped with RetroBat**, in `system\resources\inputmapping` (more than 3,000 games);
3. if the game is a clone without a configuration, **the one of its parent game**;
4. otherwise, **the default configuration** of the selected layout.

The files depend on the emulator:

<table><thead><tr><th width="172">Emulator</th><th width="318">Files shipped with RetroBat</th><th>Your files</th></tr></thead><tbody><tr><td><strong>MAME, GroovyMAME</strong></td><td>One <code>&#x3C;game>.xml</code> file per game in <code>system\resources\inputmapping\mame</code></td><td><code>user\inputmapping\mame\&#x3C;game>.xml</code></td></tr><tr><td><strong>lr-mame</strong></td><td><code>system\resources\inputmapping\libretro_mame.yml</code> (buttons) and <code>system\resources\inputmapping\lr-mame\&#x3C;game>.cfg</code> (MAME menu shortcuts)</td><td><code>user\inputmapping\libretro_mame.yml</code></td></tr><tr><td><strong>mame2003_plus</strong></td><td>The same <code>libretro_mame.yml</code> as lr-mame, and <code>system\resources\inputmapping\libretro_mame2003_plus.yml</code> for games whose buttons differ in this MAME version</td><td><code>user\inputmapping\libretro_mame2003_plus.yml</code></td></tr></tbody></table>

These files describe buttons with generic names and hold one section per layout. RetroBat converts them at launch for the connected controller.

Do not edit the files in the `system` folder: they are replaced by each update.

## Controller layout

On an arcade stick, buttons are arranged in two rows. The **CONTROLS > CONTROLLER LAYOUT** option tells RetroBat how your panel is built, so that it can reproduce the layout of the original cabinet on it.

<table><thead><tr><th width="240.75">Layout</th><th width="239.25">Top row</th><th>Bottom row</th></tr></thead><tbody><tr><td><strong>CONTROLLER(SNES)</strong> (default)</td><td>For gamepads</td><td></td></tr><tr><td><strong>MODERN 8 BUTTONS</strong></td><td>WEST, NORTH, R1, L1</td><td>SOUTH, EAST, R2, L2</td></tr><tr><td><strong>8 BUTTONS ALTERNATIVE</strong></td><td>WEST, NORTH, L1, L2</td><td>SOUTH, EAST, R1, R2</td></tr><tr><td><strong>6 BUTTONS</strong></td><td>WEST, NORTH, L1</td><td>SOUTH, EAST, R1</td></tr><tr><td><strong>CLASSIC 8 BUTTONS</strong></td><td>Handled as 6 BUTTONS</td><td></td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (523).png" alt=""><figcaption></figcaption></figure>

Per-game configurations follow these rules:

* **6-button game** (Street Fighter II): buttons 1, 2, 3 on the top row, buttons 4, 5, 6 on the bottom row;
* **game with 3 buttons or fewer**: top row with MODERN 8 BUTTONS and 6 BUTTONS, bottom row with 8 BUTTONS ALTERNATIVE.

This option can also be set for all arcade systems in **GAME SETTINGS > CONTROLS > SPECIAL CONTROLLERS** (see the [**Arcade Sticks**](../supported-controllers/arcade-sticks.md) page).

### Games without a dedicated configuration

<table><thead><tr><th width="147.75">Cabinet button</th><th width="173">CONTROLLER(SNES)</th><th width="180.5">MODERN 8 BUTTONS</th><th width="173">6 BUTTONS</th></tr></thead><tbody><tr><td>Button 1</td><td>WEST <img src="../../.gitbook/assets/image (539).png" alt=""></td><td>WEST <img src="../../.gitbook/assets/image (540).png" alt=""></td><td>WEST <img src="../../.gitbook/assets/image (541).png" alt=""></td></tr><tr><td>Button 2</td><td>SOUTH <img src="../../.gitbook/assets/image (527).png" alt=""></td><td>NORTH <img src="../../.gitbook/assets/image (536).png" alt=""></td><td>NORTH <img src="../../.gitbook/assets/image (537).png" alt=""></td></tr><tr><td>Button 3</td><td>EAST <img src="../../.gitbook/assets/image (531).png" alt=""></td><td>R1</td><td>L1</td></tr><tr><td>Button 4</td><td>NORTH <img src="../../.gitbook/assets/image (535).png" alt=""></td><td>SOUTH <img src="../../.gitbook/assets/image (528).png" alt=""></td><td>SOUTH <img src="../../.gitbook/assets/image (529).png" alt=""></td></tr><tr><td>Button 5</td><td>L1</td><td>EAST <img src="../../.gitbook/assets/image (532).png" alt=""></td><td>EAST <img src="../../.gitbook/assets/image (533).png" alt=""></td></tr><tr><td>Button 6</td><td>R1</td><td>R2</td><td>R1</td></tr><tr><td>Button 7</td><td>L2</td><td>L1</td><td>L2</td></tr><tr><td>Button 8</td><td>R2</td><td>L2</td><td>R2</td></tr></tbody></table>

Buttons 7 and 8 are only set for MAME, GroovyMAME and mame2003\_plus.

**8 BUTTONS ALTERNATIVE**: same as 6 BUTTONS with lr-mame and mame2003\_plus, same as CONTROLLER(SNES) with MAME and GroovyMAME.

## Which method should I choose?

| You want to…                                                 | MAME, GroovyMAME                                        | lr-mame                                    |
| ------------------------------------------------------------ | ------------------------------------------------------- | ------------------------------------------ |
| Fit the buttons to your arcade stick                         | **CONTROLLER LAYOUT**                                   | **CONTROLLER LAYOUT**                      |
| Fix the buttons of one game, keeping automatic configuration | `user\inputmapping\mame\<game>.xml` file                | `user\inputmapping\libretro_mame.yml` file |
| Set buttons in the MAME menu and keep them                   | **CONTROLLER PROFILE**: NONE                            | **USE OWN CFG FILE**                       |
| Use an IPAC2 or X-Arcade panel                               | **CONTROLLER PROFILE**: IPAC2 or X-ARCADE               | —                                          |
| Use your own controller file                                 | **CONTROLLER PROFILE**: CUSTOM 1 to 8, or GAME SPECIFIC | —                                          |
| Let MAME choose the buttons of the game                      | —                                                       | **ENABLE PER GAME AUTO MAPPING**           |
| Set everything yourself                                      | Turn off **AUTOCONFIGURE CONTROLLERS**                  | Turn off **AUTOCONFIGURE CONTROLLERS**     |

These options are in the advanced system options, **CONTROLS** submenu. For mame2003\_plus, see its own section below.

<div align="left"><figure><img src="../../.gitbook/assets/image (524).png" alt=""><figcaption></figcaption></figure></div>

## MAME and GroovyMAME

### Controller profile

The **CONTROLS > CONTROLLER PROFILE** option chooses where the buttons come from:

<table><thead><tr><th width="250.25">Choice</th><th>Effect</th></tr></thead><tbody><tr><td><strong>RETROBAT AUTO</strong> (default)</td><td>RetroBat automatic configuration, game by game.</td></tr><tr><td><strong>X-ARCADE</strong>, <strong>IPAC2</strong></td><td>Profiles shipped with RetroBat for these panels: <code>X-Arcade.cfg</code> and <code>ipac2.cfg</code> in <code>saves\mame\ctrlr</code>.</td></tr><tr><td><strong>CUSTOM 1</strong> to <strong>8</strong></td><td>Your <code>custom1.cfg</code> to <code>custom8.cfg</code> file in <code>saves\mame\ctrlr</code>.</td></tr><tr><td><strong>GAME SPECIFIC</strong></td><td>A file named after the game in <code>saves\mame\ctrlr</code>, for example <code>wjammers.cfg</code> for <code>wjammers.zip</code>.</td></tr><tr><td><strong>NONE</strong></td><td>RetroBat sets nothing: MAME uses its <code>.cfg</code> files.</td></tr></tbody></table>

### MAME .cfg files

MAME saves its per-game settings in `saves\mame\cfg`: `default.cfg` for all games, `<game>.cfg` for one game. They hold the buttons set in the MAME menu, and also the cabinet switches (DIP switches).

MAME reads the controller profile first, then `default.cfg`, then the `.cfg` of the game: the last one read wins. **A button set in a `.cfg` file therefore takes priority over the profile.**

With the **RETROBAT AUTO** profile, RetroBat removes the buttons from `default.cfg` and `<game>.cfg` for the session, then puts them back. DIP switches are kept. Buttons changed in the MAME menu during the session are not kept; a copy of the files of the last session stays in `saves\mame\cfgbackupmame64`.

With the other profiles, RetroBat does not touch these files.

lr-mame and MAME share the `saves\mame\cfg` folder. The **EMULATION > SEPARATE CFG FOLDER FROM LIBRETRO** option gives MAME its own folder, `saves\mame\cfg64`.

### Fixing the buttons of a game (XML file)

1. Copy the file of the game, for example `sf2.xml`, from `system\resources\inputmapping\mame` to `user\inputmapping\mame`.
2. Open the copy with a text editor. Each layout has its `<layout type="...">` section: `default` (gamepad), `modern8`, `8alternative`, `6alternative`. If the section of your layout does not exist, RetroBat uses the `default` section.
3. In the section you need, change the controller button name in the `mapping` line:

```xml
<button type="P1_BUTTON1" tag=":IN1" mask="16" defvalue="16" function="P1_BUTTON1">
  <mapping type="standard" name="JOY_west" />
</button>
```

<div align="left"><figure><img src="../../.gitbook/assets/image (542).png" alt=""><figcaption></figcaption></figure></div>

Several buttons can trigger the same action, separated by `OR`: `JOY_right OR JOY_lsright`.

**Accepted names**

| Name                                                                     | Button                                                                         |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `JOY_south`, `JOY_east`, `JOY_west`, `JOY_north`                         | Face buttons                                                                   |
| `JOY_l1`, `JOY_r1`                                                       | L1 and R1                                                                      |
| `JOY_l2`, `JOY_r2`                                                       | L2 and R2, used as buttons                                                     |
| `JOY_l2trigger`, `JOY_r2trigger`                                         | L2 and R2, analog                                                              |
| `JOY_l3`, `JOY_r3`                                                       | Stick clicks                                                                   |
| `JOY_start`, `JOY_select`                                                | START and SELECT                                                               |
| `JOY_up`, `JOY_down`, `JOY_left`, `JOY_right`                            | D-pad                                                                          |
| `JOY_lsup`, `JOY_lsdown`, `JOY_lsleft`, `JOY_lsright`                    | Left stick, as directions                                                      |
| `JOY_rsup`, `JOY_rsdown`, `JOY_rsleft`, `JOY_rsright`                    | Right stick, as directions                                                     |
| `JOY_leftstickx`, `JOY_leftsticky`, `JOY_rightstickx`, `JOY_rightsticky` | Full axis of a stick (wheel, dial, analog stick)                               |
| `MOUSE_BUTTON1`…, `MOUSE_XAXIS`, `MOUSE_YAXIS`                           | Mouse                                                                          |
| `GUN_BUTTON1`…, `GUN_XAXIS`, `GUN_YAXIS`                                 | Light gun                                                                      |
| `KEYCODE_...`                                                            | Keyboard key, in MAME format (`KEYCODE_ENTER`, `KEYCODE_P`, `KEYCODE_LSHIFT`…) |

To reverse an axis, add `_reverse` to its name: `JOY_leftstickx_reverse`.

**Game without a file**: create `user\inputmapping\mame\<game>.xml` using an existing file as a model. The `type`, `tag`, `mask` and `defvalue` attributes of each button must be those of the game in MAME: you find them in `saves\mame\cfg\<game>.cfg` after setting this button once in the MAME menu. The `README.txt` file in `user\inputmapping\mame` describes the format.

### Creating your own controller profile

1. Run `mame.exe` from the `emulators\mame` folder.
2. Open **General Settings**, then **Input Assignments**, and set the buttons. The **User Interface** part is for the MAME menu, the **Player** parts are for games.

<div align="left"><figure><img src="../../.gitbook/assets/image (543).png" alt="" width="375"><figcaption></figcaption></figure></div>

3. Save. MAME creates the `default.cfg` file in `emulators\mame\cfg`.
4. Rename this file `custom1.cfg` (up to `custom8.cfg`) and move it to `saves\mame\ctrlr`.
5. In RetroBat, choose **CONTROLS > CONTROLLER PROFILE**: CUSTOM 1.

<div align="left"><figure><img src="../../.gitbook/assets/image (525).png" alt=""><figcaption></figcaption></figure></div>

For a profile dedicated to one game, name the file like the romset (`wjammers.cfg` for `wjammers.zip`), put it in `saves\mame\ctrlr` and choose **GAME SPECIFIC**.

## lr-mame

### Fixing the buttons of a game (libretro\_mame.yml)

1. Copy `libretro_mame.yml` from `system\resources\inputmapping` to `user\inputmapping`. Your copy then fully replaces the RetroBat file.
2. Find the entry of the game. There is one per layout: `sf2` (gamepad), `sf2_modern8`, `sf2_8alternative`, `sf2_6alternative`. If the entry of your layout does not exist, RetroBat uses the `sf2` entry, which must always be present.

```
sf2_modern8:
  analog_dpad_mode: 0
  btn_a: 10
  btn_b: 9
  btn_x: 8
  btn_y: 0
```

3. Each line gives, for a button of your controller, the cabinet button to trigger.

<table><thead><tr><th width="259">Name</th><th>Controller button</th></tr></thead><tbody><tr><td><code>btn_a</code></td><td>EAST <img src="../../.gitbook/assets/image (530).png" alt=""></td></tr><tr><td><code>btn_b</code></td><td>SOUTH <img src="../../.gitbook/assets/image (526).png" alt=""></td></tr><tr><td><code>btn_x</code></td><td>NORTH <img src="../../.gitbook/assets/image (534).png" alt=""></td></tr><tr><td><code>btn_y</code></td><td>WEST <img src="../../.gitbook/assets/image (538).png" alt=""></td></tr><tr><td><code>btn_l</code>, <code>btn_r</code></td><td>L1, R1</td></tr><tr><td><code>btn_l2</code>, <code>btn_r2</code></td><td>L2, R2</td></tr></tbody></table>

<table><thead><tr><th width="169">Value</th><th>Cabinet button</th></tr></thead><tbody><tr><td><code>0</code></td><td>Button 1</td></tr><tr><td><code>8</code></td><td>Button 2</td></tr><tr><td><code>1</code></td><td>Button 3</td></tr><tr><td><code>9</code></td><td>Button 4</td></tr><tr><td><code>10</code></td><td>Button 5</td></tr><tr><td><code>11</code></td><td>Button 6</td></tr><tr><td><code>14</code></td><td>Button 7</td></tr><tr><td><code>15</code></td><td>Button 8</td></tr><tr><td><code>-1</code></td><td>None</td></tr></tbody></table>

In the example, EAST (`btn_a: 10`) triggers button 5 of the cabinet.

### MAME menu

The MAME menu opens with **START + SOUTH**. **SOUTH** confirms and **EAST** goes back.

As buttons change from one game to another, RetroBat writes these shortcuts into `saves\mame\cfg\<game>.cfg` at each launch, from the files in `system\resources\inputmapping\lr-mame`. A copy of the previous session is kept in `saves\mame\cfgbackup`.

### Keeping the settings made in the MAME menu

Turn on **CONTROLS > USE OWN CFG FILE**. Buttons set in the MAME menu are then kept in `saves\mame\cfg\<game>.cfg`. On first activation, the configuration of the last session is imported. The CONTROLLER LAYOUT option no longer applies to this game.

### Letting MAME choose

With **ENABLE PER GAME AUTO MAPPING**, RetroBat no longer applies its per-game configurations: the core places the buttons.

## mame2003\_plus

By default, mame2003\_plus reuses the per-game configurations of lr-mame and follows the **CONTROLLER LAYOUT** option. Games whose buttons are different in this old MAME version have their own configuration, or else the default configuration.

<table><thead><tr><th width="282.75">You want to…</th><th>Setting</th></tr></thead><tbody><tr><td>Use a core layout, the same for all games</td><td><strong>CONTROLS > PLAYER 1 CONTROLLER TYPE</strong>: RETROPAD, FIGHTSTICK, 8-BUTTON or 6-BUTTON. RetroBat then no longer sets buttons game by game.</td></tr><tr><td>Fix the buttons of one game</td><td><code>user\inputmapping\libretro_mame2003_plus.yml</code> file</td></tr><tr><td>Set buttons in the MAME menu</td><td><strong>ENABLE MAME REMAPPING</strong> (on by default), then <strong>L3</strong></td></tr></tbody></table>

In the MAME menu, the buttons to confirm and cancel depend on the game: **SOUTH** and **WEST** with the default configuration.

**Fixing a game**: copy `libretro_mame2003_plus.yml` from `system\resources\inputmapping` to `user\inputmapping`, then add or edit the entry of the game in it. The format is the one of `libretro_mame.yml`, with two differences:

* buttons 7 and 8 are written `12` and `13`;
* a `use: default` entry marks a game that uses the default configuration.

Games missing from this file are read from `libretro_mame.yml`.

## Folders

<table><thead><tr><th width="301.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>RetroBat per-game configurations</td><td><code>system\resources\inputmapping</code></td></tr><tr><td>Your per-game configurations</td><td><code>user\inputmapping</code></td></tr><tr><td>MAME controller profiles</td><td><code>saves\mame\ctrlr</code></td></tr><tr><td>MAME per-game settings (cfg)</td><td><code>saves\mame\cfg</code> (or <code>saves\mame\cfg64</code>)</td></tr><tr><td>Backup copies of cfg files</td><td><code>saves\mame\cfgbackup</code> (lr-mame), <code>saves\mame\cfgbackupmame64</code> (MAME)</td></tr><tr><td>mame2003_plus settings</td><td><code>saves\mame\mame2003-plus</code></td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="351.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Buttons are not in the right place on my arcade stick</td><td>Set <strong>CONTROLLER LAYOUT</strong> to match your panel.</td></tr><tr><td>With mame2003_plus, <strong>CONTROLLER LAYOUT</strong> has no effect</td><td>Leave <strong>PLAYER 1 CONTROLLER TYPE</strong> and <strong>PLAYER 2 CONTROLLER TYPE</strong> on AUTO.</td></tr><tr><td>My settings made in the MAME menu are lost</td><td>Automatic configuration replaces them. MAME: choose the NONE profile. lr-mame: turn on <strong>USE OWN CFG FILE</strong>.</td></tr><tr><td>My custom controller profile is ignored</td><td>A <code>default.cfg</code> or <code>&#x3C;game>.cfg</code> file in <code>saves\mame\cfg</code> holds other buttons: delete it or remove the buttons from it.</td></tr><tr><td>My <code>user\inputmapping\mame\&#x3C;game>.xml</code> file is ignored</td><td>The file must have the exact romset name, and the profile must be <strong>RETROBAT AUTO</strong>.</td></tr><tr><td>My fix in <code>libretro_mame.yml</code> is ignored</td><td>Edit the copy placed in <code>user\inputmapping</code>, and the entry of your layout (<code>&#x3C;game>_modern8</code>…).</td></tr></tbody></table>
