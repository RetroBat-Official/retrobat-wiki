---
description: Sammy Corporation
---

# Atomiswave

<div align="left"><figure><img src="../../../.gitbook/assets/image (591).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Atomiswave** is an arcade board by Sammy, released in 2003. It reuses the Dreamcast architecture (SH-4 processor, PowerVR2 graphics chip): games come on cartridges and the control panel is swapped depending on the game (joysticks, light guns, wheel). Cheap to run, it took over from the Neo Geo MVS at SNK, which released its last fighting games on it. The last titles came out in 2009.

Its games include **The King of Fighters XI**, **The King of Fighters Neowave**, **NeoGeo Battle Coliseum**, **Metal Slug 6**, **Samurai Shodown VI** (Samurai Spirits Tenkaichi Kenkakuden), **Guilty Gear Isuka**, **Fist of the North Star**, **The Rumble Fish 2**, **Dolphin Blue**, **Demolish Fist**, **Faster Than Speed**, **Maximum Speed**, and light gun games (**Sports Shooting USA**, **Extreme Hunting**, **Ranger Mission**).

RetroBat offers three emulators: the **flycast** libretro core (default), standalone **Flycast** and **Demul**.

{% embed url="https://en.wikipedia.org/wiki/Atomiswave" %}

## At a glance

<table><thead><tr><th width="227.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\atomiswave</code></td></tr><tr><td><strong>Extensions</strong></td><td>.bin .lst .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: flycast</td></tr><tr><td><strong>BIOS</strong></td><td><code>awbios.zip</code> in <code>bios\dc</code></td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, every emulator (per-game mapping for the flycast cores)</td></tr><tr><td><strong>Save states</strong></td><td>flycast core, Flycast (managed by RetroBat); Demul through hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No (Flycast: GGPO online play, specific to the emulator)</td></tr><tr><td><strong>Light guns</strong></td><td>flycast core, Flycast, Demul</td></tr><tr><td><strong>Wheels</strong></td><td>Flycast</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="192">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: flycast</strong> (default)</td><td>Very good compatibility, buttons placed as on the cabinet for each game, save states, up to 4 light guns, RetroArch shaders and hotkeys.</td><td>No mapping file supplied for wheels.</td></tr><tr><td><strong>flycast</strong></td><td>Same base as the core, with its own menus. Per-game mapping, save states, wheels (Maximum Speed, Faster Than Speed), light guns with DemulShooter, GGPO online play.</td><td>—</td></tr><tr><td><strong>demul</strong></td><td>Long-standing emulator, also used for Naomi and Dreamcast.</td><td>Lower compatibility. Same button layout for every game. Save states not managed by RetroBat. Cannot read <code>.bin</code> / <code>.lst</code> files.</td></tr></tbody></table>

## BIOS

| File         | Folder    | Used by        |
| ------------ | --------- | -------------- |
| `awbios.zip` | `bios\dc` | Every emulator |

`awbios.zip` is the Atomiswave BIOS in MAME format. The flycast core and standalone Flycast both look for it in `bios\dc`; Demul finds it in `bios\dc`, `bios` or the games folder. Its content depends on the MAME version (reference md5: `0ec5ae5b5a5c4959fa8b43fcf8687f7c`).

## Which game format?

<table><thead><tr><th width="122.75">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>MAME format games, to keep as they are, neither unzipped nor renamed (<code>kofxi.zip</code>, <code>mslug6.zip</code>, <code>ngbc.zip</code>…). Clones (<code>kofnwj</code>, <code>ngbcj</code>…) need the parent game in the same folder.</td></tr><tr><td><strong>.bin</strong>, <strong>.lst</strong></td><td>Former NullDC format (a <code>.bin</code> image and its <code>.lst</code> list): flycast cores only.</td></tr></tbody></table>

## Controls

### Automatic setup

RetroBat sets up the controllers for the three emulators. The controls shared by every game:

<table><thead><tr><th width="174">Cabinet</th><th>Controller</th></tr></thead><tbody><tr><td>Joystick</td><td>D-pad, left stick</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Coin</td><td>SELECT</td></tr><tr><td>Test</td><td>R3 (with the service menu enabled, see <a href="atomiswave.md#service-menu-and-test-menu"><strong>Guides</strong></a>)</td></tr><tr><td>Service</td><td>L3 (with the service menu enabled, see <a href="atomiswave.md#service-menu-and-test-menu"><strong>Guides</strong></a>)</td></tr></tbody></table>

* **flycast core** and **Flycast**: the position of the action buttons is defined game by game, to match the cabinet layout. The files used are `libretro_flycast_atomiswave.yml` (core) and `flycast_Arcade.yml` (Flycast), see the [**Emulator specific controller configuration**](../../../controllers/controller-configuration.md#adapting-the-controls-without-disabling-autoconfiguration) page. **CONTROLS > CONTROLLER LAYOUT** picks another layout when the file offers one.
* **Flycast**: **CONTROLS > USE DPAD** moves the analog controls to the d-pad.
* **Demul**: same layout for every game: buttons 1 to 4 on SOUTH, EAST, WEST, NORTH, buttons 5 to 8 on L1, R1, L2, R2.

### Light guns

Light gun games (**Sports Shooting USA**, **Extreme Hunting**, **Extreme Hunting 2**, **Ranger Mission**, **Sega Clay Challenge**) work with the flycast core (up to 4 guns), Flycast (2 guns, 4 with DemulShooter) and Demul (1 gun, 2 with DemulShooter). For the options and buttons, see the [**Light gun controls**](../../../controllers/gun_controls.md) page.

### Wheels

Flycast supports wheels for **Maximum Speed** and **Faster Than Speed** (**WHEELS > ENABLE WHEEL**, **WHEEL BUTTON LAYOUT**). The flycast core also supports wheels, but RetroBat does not supply its mapping file yet. For the supported wheels, see the [**Wheels**](../../../controllers/supported-controllers/wheels.md) page.

### Hotkeys

The flycast core uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../navigation/hotkeys.md) page).

**Flycast**

<table><thead><tr><th width="191">Hotkey</th><th width="185.75">Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td>Esc</td></tr><tr><td><strong>HOTKEY + SOUTH</strong></td><td>Flycast menu</td><td>F1</td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Load state</td><td>F4</td></tr><tr><td><strong>HOTKEY + RIGHT</strong></td><td>Fast forward (hold)</td><td>L</td></tr><tr><td><strong>HOTKEY + R3</strong></td><td>Screenshot</td><td>F8</td></tr></tbody></table>

**Demul**

<table><thead><tr><th width="204.75">Hotkey</th><th width="185.75">Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td></td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Demul save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Demul load state</td><td>F4</td></tr></tbody></table>

Demul save states stay in Demul: they do not show up in the save state manager.

## Folders

| Content                                  | Folder                                                                             |
| ---------------------------------------- | ---------------------------------------------------------------------------------- |
| BIOS                                     | `bios\dc`                                                                          |
| flycast core: save states                | `saves\atomiswave\libretro.flycast`                                                |
| Flycast: game saves (NVRAM)              | `saves\atomiswave\reicast`                                                         |
| Flycast: save states                     | `saves\atomiswave\flycast\sstates` (copied from `saves\atomiswave\reicast\states`) |
| Flycast: configuration                   | `emulators\flycast\emu.cfg`                                                        |
| Demul: game saves (NVRAM)                | `saves\atomiswave\demul`                                                           |
| Demul: configuration                     | `emulators\demul\Demul.ini`, `emulators\demul\padDemul.ini`                        |
| Per-game mapping (flycast core, Flycast) | `system\resources\inputmapping` (editable copy in `user\inputmapping`)             |

## Guides

### Service menu and test menu

The cabinet test menu sets the number of credits, the difficulty, the number of rounds, and checks the controls.

1. Enable **EMULATION > SERVICE MODE** (flycast core) or **EMULATION > ENABLE SERVICE MENU** (Flycast). With Demul, the buttons are always active.
2. In game, press **R3** (Test) to open the menu, then browse with the cabinet buttons. **L3** (Service) adds a service credit.

<div align="left"><figure><img src="../../../.gitbook/assets/image (592).png" alt="" width="563"><figcaption></figcaption></figure></div>

### Credits

Atomiswave games have no free play mode that the emulator can set: add credits with **SELECT**, or set free play in the game's test menu when it offers it.

### Other useful options

| Option                                                | Effect                                                                    |
| ----------------------------------------------------- | ------------------------------------------------------------------------- |
| **INTERNAL RESOLUTION**                               | Raises the rendering resolution (the three emulators).                    |
| **GAME ASPECT RATIO**                                 | Flycast, Demul: 4:3, 16:9 or stretched.                                   |
| **VISUAL RENDERING > WIDESCREEN HACK** (flycast core) | Stretches the picture to 16:9, with glitches in some games.               |
| **VIDEO > TATE MODE**                                 | Vertical display (flycast core, Flycast).                                 |
| **NETWORK > BROADCAST DIGITAL OUTPUTS**               | Sends the cabinet outputs (lamps…) to MameHooker (flycast core, Flycast). |

## Known issues

<table><thead><tr><th width="355.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start</td><td>Check <code>awbios.zip</code> in <code>bios\dc</code>, and the parent game for a clone.</td></tr><tr><td>The game asks for credits</td><td>Press <strong>SELECT</strong> to add a credit.</td></tr><tr><td>The buttons are not in the right place</td><td>With Demul, the layout is the same for every game: use the flycast core or Flycast.</td></tr><tr><td>A <code>.bin</code> / <code>.lst</code> game does not start with Demul</td><td>Demul only reads MAME format games: use the flycast core or Flycast.</td></tr><tr><td>The light gun game does not react</td><td>Enable <strong>GUNS > ENABLE GUN</strong>, then check the <a href="../../../controllers/gun_controls.md"><strong>Light gun controls</strong></a> page.</td></tr></tbody></table>
