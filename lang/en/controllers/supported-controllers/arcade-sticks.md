# 🕹️ Arcade Sticks

Arcade sticks (fight sticks, hitboxes, arcade panels with a USB encoder) are handled like gamepads in RetroBat. On top of that, RetroBat can reproduce the **original button layout of the arcade cabinet** on your stick, thanks to the **CONTROLLER LAYOUT** option.

## Choose the right mode on your stick

Most recent sticks have a mode switch or a button combination (see your stick's manual): **XInput / PC / X**, **DirectInput / D**, **PlayStation / PS**, **Switch / NS**…

{% hint style="success" %}
**Use XInput mode whenever your stick offers it.** The stick is then recognised as a standard Xbox controller: it is configured automatically, and its buttons match the layouts described below without any setting.
{% endhint %}

<table><thead><tr><th width="216.5">Mode</th><th>Notes</th></tr></thead><tbody><tr><td><strong>XInput</strong> (recommended)</td><td>Automatic configuration. The 8 buttons are A, B, X, Y, LB, RB, LT, RT.</td></tr><tr><td><strong>PlayStation / Switch</strong></td><td>Works too (buttons are handled by position), but XInput remains the simplest.</td></tr><tr><td><strong>DirectInput</strong> (cheap USB encoders, Zero Delay…)</td><td>Must be configured once in <strong>MAIN MENU > CONTROLLER SETTINGS > CONTROLLER MAPPING</strong>. Map the buttons following the reference layout below, so that the layouts work as expected.</td></tr></tbody></table>

**Lever**: if your stick has a **DP / LS / RS** switch, keep it on **DP** (D-pad). Only use **LS** (left stick) for games that need an analog input.

### Mapping a DirectInput stick

When configuring the stick in **CONTROLLER MAPPING**, map the buttons by position, as on a "modern" 8-button panel:

<table><thead><tr><th width="145.5"></th><th width="129.75">Button 1</th><th width="137">Button 2</th><th>Button 3</th><th>Button 4</th></tr></thead><tbody><tr><td><strong>Top row</strong></td><td>WEST</td><td>NORTH</td><td>RIGHT SHOULDER</td><td>LEFT SHOULDER</td></tr><tr><td><strong>Bottom row</strong></td><td>SOUTH</td><td>EAST</td><td>RIGHT TRIGGER</td><td>LEFT TRIGGER</td></tr></tbody></table>

Also map **START**, **SELECT** (used as Coin) and **HOTKEY** (usually the same button as SELECT).

## Choose the layout (CONTROLLER LAYOUT)

The **CONTROLLER LAYOUT** option is located in the system's advanced configuration (or the game's advanced configuration) > **CONTROLS**. It tells RetroBat how the buttons of your stick are laid out, so that each game uses the same buttons as on the original cabinet.

<div align="left"><figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure></div>

The diagrams below show the buttons as **XInput** names them (PlayStation equivalent: X = □, Y = △, A = ✕, B = ○, LB/RB = L1/R1, LT/RT = L2/R2).

| Value                           | Top row         | Bottom row      | For                                                                       |
| ------------------------------- | --------------- | --------------- | ------------------------------------------------------------------------- |
| **CONTROLLER (SNES)** (default) | –               | –               | Gamepads: the mapping is designed for a controller.                       |
| **MODERN 8 BUTTONS**            | X · Y · RB · LB | A · B · RT · LT | Most fight sticks and hitboxes (Hori, Qanba, Mayflash, 8BitDo, Victrix…). |
| **8 BUTTONS ALTERNATIVE**       | X · Y · LB · LT | A · B · RB · RT | Panels whose 3rd and 4th columns are LB/RB and LT/RT.                     |
| **6 BUTTONS**                   | X · Y · LB      | A · B · RB      | 6-button panels (Astro City style).                                       |
| **CLASSIC 8 BUTTONS**           | X · Y · LB      | A · B · RB      | Currently uses the 6 BUTTONS layout.                                      |

{% hint style="info" %}
To find your layout, look at the labels printed on your stick (or press each button in Windows' **Set up USB game controllers**, `joy.cpl`), then pick the line that matches what your top and bottom rows send.
{% endhint %}

Examples (MODERN 8 BUTTONS):

* **3-button game** (e.g. Golden Axe): buttons 1-2-3 on the top row.
* **6-button game** (e.g. Street Fighter II): punches on the top row, kicks on the bottom row, as on the original cabinet.

### Emulators supporting the layouts

<table><thead><tr><th width="340.25">Emulator</th><th>Games</th></tr></thead><tbody><tr><td><strong>MAME</strong> (standalone, HBMAME, GroovyMAME)</td><td>All games, with exact cabinet layouts for the games provided by RetroBat.</td></tr><tr><td><strong>RetroArch - MAME</strong> core</td><td>All games, with exact cabinet layouts for the games provided by RetroBat.</td></tr><tr><td><strong>RetroArch - Flycast</strong> and <strong>Supermodel</strong> cores</td><td>Games listed in the mapping files.</td></tr><tr><td><strong>FBNeo</strong> (standalone)</td><td>Games listed in the mapping file.</td></tr><tr><td><strong>Flycast</strong> (standalone, Naomi / Atomiswave)</td><td>Games listed in the mapping file.</td></tr><tr><td><strong>Supermodel</strong> (Model 3)</td><td>Games listed in the mapping file.</td></tr><tr><td><strong>TeknoParrot</strong></td><td>Games listed in the mapping file.</td></tr><tr><td><strong>Lindbergh</strong> (linuxloader)</td><td>All games.</td></tr><tr><td><strong>PCSX2x6</strong> (Namco System 246/256)</td><td>All games.</td></tr><tr><td><strong>ArcadeDuck</strong> (Zinc)</td><td>All games, with game-specific layouts when available.</td></tr></tbody></table>

Games that are not listed use the standard RetroBat mapping. You can add or modify game layouts in `user\inputmapping`: see the [Emulator specific controls mapping](../specific_mapping/) page.

## Arcade buttons

| Function        | Stick          | Keyboard  |
| --------------- | -------------- | --------- |
| Start (P1 / P2) | START          | `1` / `2` |
| Coin (P1 / P2)  | SELECT         | `5` / `6` |
| Test            | R3             | `0`       |
| Service         | L3             | `9`       |
| Exit the game   | HOTKEY + START | `Esc`     |

{% hint style="info" %}
Most sticks have no L3/R3 buttons: use the keyboard keys `9` / `0` to open the operator menus (Test / Service), or the L3/R3 switch of your stick if it has one.
{% endhint %}

See the [Arcade Guide](../../systems-and-emulators/arcade-guide.md) for more details on arcade controls and romsets.

## Sticks recognised as a keyboard (I-PAC2, X-Arcade Tankstick)

Some sticks and encoders are seen by Windows as a **keyboard**. RetroBat provides ready-made configurations for them:

* **RetroArch**: **GAME SETTINGS > RETROARCH OPTIONS > CONTROLS > CONFIGURE SPECIAL KEYBOARD STICK**.
* **MAME**: system advanced configuration > CONTROLS > **CONTROLLER PROFILE** (IPAC2 or X-ARCADE).
* **PCSX2x6**: system advanced configuration > CONTROLS > **CONFIGURE SPECIAL KEYBOARD STICK**.

All the details are on the [Special controllers](gamepads/special-controllers.md) page.

{% hint style="info" %}
If your encoder can work as a gamepad (XInput), prefer this mode: the stick then benefits from automatic configuration and from the layouts above.
{% endhint %}

## Custom stick mapping (RetroArch)

For a stick recognised as a gamepad, you can also force a dedicated RetroArch mapping with the `arcade_sticks.json` file and the **USE CUSTOM ARCADE STICK MAPPING** option: see the [Special controllers page](gamepads/special-controllers.md).
