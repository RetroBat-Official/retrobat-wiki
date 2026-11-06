# Controllers Configuration

RetroBat configures your controllers in two steps:

1. **In RetroBat (EmulationStation)**: your controller is recognised and its buttons are known. This is done once per controller model.
2. **At each game launch (autoconfiguration)**: RetroBat writes the configuration of your controllers in the emulator, so that you can play without configuring each emulator.

For most branded controllers (Xbox, PlayStation, Switch Pro, 8BitDo…), there is nothing to do: both steps are automatic.

## Configuring a controller in RetroBat

Known controllers are configured automatically. To configure a controller that is not recognised, or to change its configuration, go to **MAIN MENU > CONTROLLER SETTINGS > CONTROLLER MAPPING**, then **hold a button** of the controller to configure:

<div align="left"><figure><img src="../.gitbook/assets/image (334).png" alt=""><figcaption></figcaption></figure></div>

The configuration screen asks for each input, one after the other:

<div align="left"><figure><img src="../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure></div>

* **Map the buttons by their position**, not by their label: SOUTH is the bottom face button, EAST the right one, and so on (see the table below).
* **Skip** an input your controller does not have by **holding any button** for one second.
* Required inputs: **SOUTH**, **EAST**, the **D-pad** (if your controller has one) and **HOTKEY**. If your controller has no dedicated button for HOTKEY, use **SELECT**.
* At the end, press **SOUTH** to confirm.

| RetroBat input                                  | Xbox                                                    | PlayStation                           | Nintendo                  |
| ----------------------------------------------- | ------------------------------------------------------- | ------------------------------------- | ------------------------- |
| SOUTH ![](<../.gitbook/assets/image (327).png>) | A                                                       | ✕ (Cross)                             | B                         |
| EAST ![](<../.gitbook/assets/image (328).png>)  | B                                                       | ○ (Circle)                            | A                         |
| NORTH ![](<../.gitbook/assets/image (329).png>) | Y                                                       | △ (Triangle)                          | X                         |
| WEST ![](<../.gitbook/assets/image (330).png>)  | X                                                       | □ (Square)                            | Y                         |
| START                                           | Menu ![](<../.gitbook/assets/image (331).png>) / Start  | Options                               | +                         |
| SELECT                                          | View ![](<../.gitbook/assets/image (332).png>) / Back   | Share / Create                        | −                         |
| D-PAD                                           | D-pad                                                   | D-pad                                 | D-pad                     |
| LEFT SHOULDER / RIGHT SHOULDER                  | LB / RB                                                 | L1 / R1                               | L / R                     |
| LEFT TRIGGER / RIGHT TRIGGER                    | LT / RT                                                 | L2 / R2                               | ZL / ZR                   |
| LEFT ANALOG / RIGHT ANALOG                      | Left / right stick                                      | Left / right stick                    | Left / right stick        |
| LEFT STICK PRESS / RIGHT STICK PRESS            | Left / right stick click (L3 / R3)                      | L3 / R3                               | Left / right stick click  |
| HOTKEY                                          | SELECT (View), or a dedicated button                    | SELECT (Share), or a dedicated button | − , or a dedicated button |

The configuration is saved for this controller model in `emulationstation\.emulationstation\es_input.cfg`.

### Player order

The order of the controllers (player 1, player 2…) is set in **MAIN MENU > CONTROLLER SETTINGS > CONTROLLERS PRIORITY**, with **P1'S CONTROLLER**, **P2'S CONTROLLER**…

<div align="left"><figure><img src="../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure></div>

## Autoconfiguration in the emulators

At each game launch, RetroBat writes the configuration of the connected controllers in the emulator (RetroArch and most standalone emulators): buttons, hotkeys, player order.

{% hint style="warning" %}
While autoconfiguration is enabled, the controller configuration of the emulator is **rewritten at each launch**: a mapping you make by hand in the emulator is lost at the next launch. To keep your own configuration, disable autoconfiguration (see below).
{% endhint %}

### Disabling autoconfiguration

Autoconfiguration can be disabled globally, for a system or for a game, with the **AUTOCONFIGURE CONTROLLERS** option:

* **Globally**: **MAIN MENU > GAME SETTINGS > AUTOCONFIGURE CONTROLLERS**: **OFF**.

<div align="left"><figure><img src="../.gitbook/assets/image (337).png" alt=""><figcaption></figcaption></figure></div>

* **For a system**: open the [View Options](../navigation/view-options.md) of the system, **ADVANCED SYSTEM OPTIONS > AUTOCONFIGURE CONTROLLERS**: **OFF**.

<div align="left"><figure><img src="../.gitbook/assets/image (338).png" alt=""><figcaption></figcaption></figure></div>

* **For a game**: open the [Game Options](../navigation/game-options.md), **ADVANCED GAME OPTIONS > AUTOCONFIGURE CONTROLLERS**: **OFF**.

<div align="left"><figure><img src="../.gitbook/assets/image (339).png" alt=""><figcaption></figcaption></figure></div>

Set **AUTOCONFIGURE CONTROLLERS** to **OFF**

<div align="left"><figure><img src="../.gitbook/assets/image (340).png" alt=""><figcaption></figcaption></figure></div>

Then configure your controllers **directly in the emulator**:

* the standalone emulators can be opened from the **RETROBAT** system in the System View;
* in RetroArch, open the menu during the game (**HOTKEY + SOUTH** or **F1**) and go to **Controls**.

{% hint style="warning" %}
**Lightguns**: disabling **AUTOCONFIGURE CONTROLLERS** does not stop RetroBat from configuring the guns. To keep your own gun configuration, also set **ENABLE GUN** (advanced options > **GUNS**) to **OFF** for the same system or game.
{% endhint %}

## Adapting the controls without disabling autoconfiguration

RetroBat offers several ways to adapt the controls while keeping autoconfiguration:

<table><thead><tr><th width="264.5">Need</th><th width="264.5">Solution</th><th>Page</th></tr></thead><tbody><tr><td>Change a hotkey</td><td>Hotkey files <code>kb_hotkeys.yml</code> / <code>controller_hotkeys.yml</code></td><td><a href="../navigation/hotkeys.md">Hotkeys</a></td></tr><tr><td>Play arcade games with an arcade stick</td><td><strong>CONTROLLER LAYOUT</strong> option</td><td><a href="supported-controllers/arcade-sticks.md">Arcade Sticks</a></td></tr><tr><td>Choose another button layout for a console</td><td>Layout options of the system (e.g. Saturn <strong>BUTTON LAYOUT</strong>)</td><td>Page of the system in <a href="../systems-and-emulators/supported-game-systems/">Supported Game Systems</a></td></tr><tr><td>Change the mapping of a game or a core</td><td>Mapping files in <code>user\inputmapping</code></td><td><a href="specific_mapping/">Emulator specific controls mapping</a>, <a href="../systems-and-emulators/arcade-guide.md">Arcade Guide</a></td></tr><tr><td>Use an N64, Genesis, Saturn, GameCube controller or adapter</td><td>Special controllers</td><td><a href="supported-controllers/gamepads/special-controllers.md">Special controllers</a></td></tr><tr><td>Play computer games with a controller</td><td>PadToKey</td><td><a href="supported-controllers/keyboard.md">Keyboard</a></td></tr></tbody></table>

### How a mapping file works: two examples

#### Flycast (standalone)

The `flycast_Arcade.yml` file contains the mapping of many Naomi, Naomi 2 and Atomiswave games. Each block is a game (arcade games always have the same rom name, so the mapping is always applied):

<div align="left"><figure><img src="../.gitbook/assets/image (341).png" alt=""><figcaption></figcaption></figure></div>

For example, `l2: btn_trigger_left` means that the left trigger of your controller is assigned to the `btn_trigger_left` input of Flycast. RetroBat converts L2 into what your controller actually uses (axis or button):

<div align="left"><figure><img src="../.gitbook/assets/image (342).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure></div>

#### RetroArch (Flycast core)

The `libretro_flycast_naomi.yml` file contains, for each Naomi game, the remapping of the RetroArch RetroPad buttons to the inputs of the core:

<div align="left"><figure><img src="../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure></div>

For example, `btn_b: 4` means that the SOUTH button of the RetroPad sends the input with ID 4 of the core (here, DRIVE GEAR):

<div align="left"><figure><img src="../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (346).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
For RetroArch, these files do not change the mapping between your controller and the RetroPad: RetroBat creates a **core remap file** in `emulators\retroarch\config\remaps\<core name>`.
{% endhint %}

## Fixing controller issues

1. **Map your controller again** in **CONTROLLER SETTINGS > CONTROLLER MAPPING**, by position.
2. **Check the player order** in **CONTROLLERS PRIORITY**.
3. **Check that AUTOCONFIGURE CONTROLLERS is not set to OFF** (globally, for the system or for the game).
4. Launch the game and open `emulationstation\emulatorLauncher.log`: it shows the controllers detected and the configuration written.
5. If it still does not work, disable autoconfiguration, configure the controller directly in the emulator, and save the configuration file it creates.
6. Contact the RetroBat team (Discord or GitHub) with `es_input.cfg`, `emulatorLauncher.log` and the emulator configuration files from steps 4 and 5.
