---
description: Bang Bang !
---

# Gun controls

This page lists the systems and emulators in which RetroBat configures lightguns, and how the gun buttons are mapped. To connect a gun, enable it and set the common options, see [Lightguns](supported-controllers/lightguns/).

## How RetroBat maps a gun

A lightgun works as a mouse (aiming and buttons), often with a keyboard for its extra buttons. In each emulator, RetroBat assigns them to the emulated gun with the same logic:

<table><thead><tr><th width="371.5">Gun button</th><th>Default mapping</th></tr></thead><tbody><tr><td>Trigger</td><td>Left click</td></tr><tr><td>Second button (reload, A, cursor…, depending on the gun)</td><td>Right click</td></tr><tr><td>Third button</td><td>Middle click</td></tr><tr><td>Start</td><td>Key 1 (P1), 2 (P2), 3 (P3), 4 (P4)</td></tr><tr><td>Coin / Select</td><td>Key 5 (P1), 6 (P2), 7 (P3), 8 (P4)</td></tr></tbody></table>

* **Reload**: in most games, you reload by shooting off the screen. If your gun cannot shoot off-screen, enable **RELOAD WITH BUTTON**.
* **INVERT TRIGGER/RELOAD** swaps the left and right clicks (e.g. Wii Zapper).
* **Wiimote with DolphinBar**: the buttons send other keys, RetroBat adapts the mapping (D-pad Right = Start, D-pad Left = Coin). See [Wiimote & DolphinBar](supported-controllers/lightguns/wiimoteandbar.md).
* **RetroArch**: the buttons of your gamepad also stay assigned to the gun buttons (Start, Select, auxiliary buttons, D-pad), so you can use a gamepad along with the gun.

## Enabling the guns

For lightgun games, the guns are enabled automatically (see [Lightguns](supported-controllers/lightguns/)). Exceptions:

* **RPCS3**: choose the type of gun with **ENABLE GUN** (**RAW MOUSE** for GunCon 3, **PS EYE** for PlayStation Move games). It is never enabled automatically.
* **Hypseus** and **Singe 2**: the gun always works as a mouse, there is no option to enable.
* **Wii**: the Wiimotes are used as real Wiimotes, see the [Wii](../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/wii.md) page.

## Compatible systems and emulators

The **Guns** column gives the number of guns RetroBat can configure at the same time. The game must also support several players.

| System                        | Emulator                                               | Guns                      | Notes                                                              |
| ----------------------------- | ------------------------------------------------------ | ------------------------- | ------------------------------------------------------------------ |
| Arcade                        | lr-fbneo                                               | Up to 4                   |                                                                    |
|                               | lr-mame, lr-mame2003\_plus, lr-mame2016                | Up to 4                   |                                                                    |
|                               | MAME (mame64, groovymame)                              | Up to 4                   |                                                                    |
| 3DO                           | lr-opera                                               | Up to 4                   |                                                                    |
| ActionMax, Daphne, Singe      | hypseus                                                | Several                   | One mouse per gun (except with **USE ONE GUN ONLY**)               |
|                               | singe2                                                 | 1                         |                                                                    |
| Amiga                         | amiberry                                               | 2                         | Light pen or Trojan Phazer (**GUN TYPE**)                          |
| Amstrad CPC, GX4000           | lr-cap32                                               | Up to 4                   | Phaser or Gunstick (**LIGHTGUN MODE**)                             |
| Atari 2600                    | lr-stella                                              | Up to 4                   |                                                                    |
| Atomiswave, Naomi, Naomi 2    | lr-flycast                                             | Up to 4                   |                                                                    |
|                               | flycast                                                | 2 (4 with DemulShooter)   |                                                                    |
|                               | demul                                                  | 1 (2 with DemulShooter)   |                                                                    |
| Commodore 64                  | lr-vice                                                | 1                         |                                                                    |
| Dreamcast                     | lr-flycast                                             | Up to 4                   |                                                                    |
|                               | flycast                                                | 2 (4 with DemulShooter)   |                                                                    |
|                               | demul                                                  | 1 (2 with DemulShooter)   |                                                                    |
| Lindbergh                     | linuxloader                                            | 1 (4 with DemulShooter)   |                                                                    |
|                               | teknoparrot                                            | Up to 4                   |                                                                    |
| Master System                 | lr-genesis\_plus\_gx, lr-genesis\_plus\_gx\_wide       | Up to 4                   |                                                                    |
|                               | lr-gearsystem                                          | Up to 4                   |                                                                    |
|                               | mesen                                                  | 1                         |                                                                    |
|                               | bizhawk (SMSHawk)                                      | 1                         |                                                                    |
| Mega Drive / Genesis, Mega-CD | lr-genesis\_plus\_gx, lr-genesis\_plus\_gx\_wide       | 1                         | Menacer or Justifier (**GUN TYPE**)                                |
| Model 2                       | m2emulator                                             | 2                         | DemulShooter starts automatically with 2 guns                      |
| Model 3                       | supermodel                                             | 2                         | 2 guns need **MULTIGUN (RAW INPUT)** (enabled by default)          |
|                               | lr-supermodel                                          | Up to 4                   |                                                                    |
| Namco System 246/256          | pcsx2x6                                                | 2                         |                                                                    |
|                               | teknoparrot                                            | Up to 4                   |                                                                    |
| NES / Famicom                 | lr-fceumm, lr-mesen, lr-nestopia                       | 1                         |                                                                    |
|                               | mesen, mednafen, jgenesis, bizhawk (NesHawk)           | 1                         |                                                                    |
| PlayStation                   | lr-mednafen\_psx\_hw, lr-pcsx\_rearmed, lr-swanstation | Up to 4                   | GunCon or Justifier (**GUN TYPE**, lr-mednafen\_psx\_hw)           |
|                               | duckstation                                            | 2                         |                                                                    |
|                               | mednafen                                               | 1                         |                                                                    |
| PlayStation 2                 | pcsx2                                                  | 1                         |                                                                    |
| PlayStation 3                 | rpcs3                                                  | 2 (GunCon 3), 1 (PS Move) |                                                                    |
| PSX Arcade                    | arcadeduck                                             | Several                   |                                                                    |
| Saturn                        | lr-kronos, lr-mednafen\_saturn, lr-ymir                | Up to 4                   |                                                                    |
|                               | kronos, mednafen, bizhawk (Saturnus)                   | 1                         |                                                                    |
| Sega Chihiro                  | xemu-chihiro                                           | 2                         |                                                                    |
|                               | cxbx, chihiro, chihiro-gun                             | 1 (2 with DemulShooter)   |                                                                    |
|                               | teknoparrot                                            | Up to 4                   |                                                                    |
| Super Nintendo                | lr-snes9x                                              | 1 (2 with Justifiers)     | Superscope, Justifier, M.A.C.S. Rifle or Justifiers (**GUN TYPE**) |
|                               | lr-bsnes, lr-bsnes\_hd\_beta, lr-bsnes-jg, lr-mesen-s  | 1                         |                                                                    |
|                               | snes9x                                                 | 1 (2 with 2 Justifier)    |                                                                    |
|                               | mesen, mednafen, jgenesis, bizhawk (BSNES, Snes9x)     | 1                         |                                                                    |
| TeknoParrot                   | teknoparrot                                            | Up to 4                   |                                                                    |
| Wii                           | dolphin                                                | 1                         |                                                                    |
| Windows                       | Games compatible with DemulShooter                     | Up to 4                   | DemulShooter starts automatically with 2 guns or more              |
| Xbox                          | cxbx                                                   | 1                         |                                                                    |

### DemulShooter

DemulShooter adds the support of several guns (and of outputs such as recoil) to games and emulators that cannot handle several guns on their own. It is provided with RetroBat in `system\tools\demulshooter`.

* **Model 2 (m2emulator)** and **Windows games**: DemulShooter starts automatically when 2 guns or more are connected. Set **USE DEMULSHOOTER** to **OFF** to disable it.
* **Flycast, Demul, TeknoParrot, Linuxloader, Chihiro (Cxbx)**: set **USE DEMULSHOOTER** to **ON** in the **GUNS** options of the system or game.

For outputs (recoil, lights) with MAME, Flycast, Demul, Model 2, Supermodel, TeknoParrot and Windows games, also see the **USE MAMEHOOKER** option.

## Button mapping per emulator

### RetroArch

<table><thead><tr><th width="389">Cores</th><th>Left click</th><th>Right click</th><th>Middle click</th></tr></thead><tbody><tr><td>lr-cap32, lr-fceumm, lr-kronos, lr-mame, lr-mame2003_plus, lr-mame2016, lr-mednafen_saturn, lr-mesen, lr-opera, lr-stella, lr-supermodel, lr-vice, lr-ymir</td><td>Trigger</td><td>Reload</td><td>Start</td></tr><tr><td>lr-bsnes, lr-bsnes_hd_beta, lr-bsnes-jg, lr-gearsystem, lr-genesis_plus_gx, lr-genesis_plus_gx_wide, lr-mednafen_psx_hw, lr-mesen-s, lr-pcsx_rearmed, lr-snes9x, lr-swanstation</td><td>Trigger</td><td>Aux A</td><td>Aux B</td></tr><tr><td>lr-fbneo, lr-flycast</td><td>Trigger</td><td>Aux A</td><td>Start</td></tr><tr><td>lr-nestopia</td><td>Trigger</td><td>Aux B</td><td>–</td></tr></tbody></table>

* Keyboard (player 1): Start = **1**, Select = **5**, D-pad = arrow keys. Player 2: **2** / **6**, etc.
* **RELOAD WITH BUTTON**: reload goes to the right click, and the button of the right click moves to the middle click.
* **GUN A/B BUTTONS MAPPING** > **KEYPAD LEFT/RIGHT**: Aux A and Aux B on the left and right arrow keys (D-pad of a Wiimote).

### Other emulators

<table><thead><tr><th width="211.5">Emulator</th><th>Mapping</th></tr></thead><tbody><tr><td>MAME (mame64, groovymame)</td><td>Button 1: left click, Button 2: right click, Button 3: middle click. Start: 1 to 4, Coin: 5 to 8</td></tr><tr><td>flycast</td><td>Trigger: left click, Reload: right click, Start: middle click. Some Naomi/Atomiswave games use other buttons (<code>flycast_Arcade.yml</code> file, <strong>MOUSE MAPPING</strong> option)</td></tr><tr><td>demul</td><td>Mapping of the emulator</td></tr><tr><td>m2emulator</td><td>See <a href="specific_mapping/model2-controller-mapping.md">Model 2 controller mapping</a></td></tr><tr><td>supermodel</td><td>Trigger: left click, Off-screen shot (reload): right click</td></tr><tr><td>teknoparrot</td><td>Per game, in the <code>teknoparrot.yml</code> file (see below)</td></tr><tr><td>linuxloader</td><td>Trigger: left click, Reload: right click, Gun button: middle click, Action: key 1. Change with <strong>RELOAD MAPPING</strong>, <strong>GUN BUTTON MAPPING</strong> and <strong>ACTION BUTTON MAPPING</strong></td></tr><tr><td>xemu-chihiro</td><td>Trigger: left click, second button: right click, third button: middle click, reload by shooting off-screen. Start: 1 / 2, Coin: 5 / 6</td></tr><tr><td>cxbx (Xbox, Chihiro)</td><td>Trigger: left click, Grip: right click, A: S, B: D, Start: 1, Back: 5</td></tr><tr><td>arcadeduck</td><td>Trigger: left click, Reload: right click</td></tr><tr><td>pcsx2 (PS2)</td><td>Trigger: left click, Off-screen shot: right click, Recalibrate: middle click, A: 1, B: 2, C: 3, Start: Enter, Select: Backspace. Change with <strong>GUNCON BUTTON MAPPING</strong> and <strong>CALIBRATION BUTTON</strong></td></tr><tr><td>pcsx2x6 (Namco 246/256)</td><td>Trigger: left click, A: right click, Start: 1 / 2, Coin: 5 / 6</td></tr><tr><td>rpcs3</td><td>GunCon 3: Trigger: left click. PS Move (PS EYE): standard mouse mapping of RPCS3; the middle click is needed to pass the calibration screen (R1 can also be used)</td></tr><tr><td>duckstation</td><td>Trigger: left click, A: right click, B: middle click, Off-screen shot: 1 (P1) / 2 (P2). Change A/B with <strong>GUN MAPPING A/B</strong></td></tr><tr><td>mednafen</td><td>NES Zapper: Trigger: left click, Away trigger: right click. PSX GunCon: Trigger: left click, A: right click, B: middle click, Off-screen shot: Space. PSX Justifier: Trigger: left click, O: right click, Start: middle click, Off-screen shot: Space. SNES Super Scope: Trigger: left click, Cursor: right click, Turbo: middle click, Off-screen shot: Space. Saturn: Trigger: left click, Off-screen shot: right click, Start: middle click</td></tr><tr><td>mesen</td><td>NES Zapper and SMS Light Phaser: Fire: left click, Off-screen shot: right click. SNES Super Scope: Fire: left click, Cursor: right click, Turbo: middle click</td></tr><tr><td>jgenesis</td><td>NES Zapper: Fire: left click, Off-screen shot: right click. SNES Super Scope: Fire: left click, Cursor: right click, Pause: middle click</td></tr><tr><td>bizhawk</td><td>NES Zapper and SMS Light Phaser: Trigger: left click. SNES Super Scope: Trigger: left click, Cursor: middle click, Turbo: right click. Saturn: Trigger: left click, Off-screen shot: right click, Start: middle click</td></tr><tr><td>snes9x</td><td>Mapping of the emulator for the Super Scope / Justifier</td></tr><tr><td>kronos</td><td>Trigger: left click, Start: right click</td></tr><tr><td>amiberry</td><td>Light pen button: left click</td></tr><tr><td>dolphin (Wii)</td><td>B: left click, A: right click, Shake: middle click, 1: key 1, 2: key 5, +: Enter, −: Backspace. Some games use another mapping, defined in <code>gamesdb.xml</code></td></tr></tbody></table>

### TeknoParrot mapping file

The gun mapping of each TeknoParrot game is defined in `system\resources\inputmapping\teknoparrot.yml`. To change it, copy the file to `user\inputmapping\teknoparrot.yml` and edit the copy: it is read first and is not overwritten by RetroBat updates.

In this file, the gun buttons are declared with `mouseleft`, `mousemiddle`, `mouseright`, `button4`, `button5`, and the keyboard keys with `kb_` followed by the key (e.g. `kb_5`).
