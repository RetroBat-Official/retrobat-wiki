---
description: Sega
---

# Sega NAOMI 2

<div align="left"><figure><img src="../../../../.gitbook/assets/image (602).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **NAOMI 2** is the more powerful version of the NAOMI, released by Sega in 2000. It doubles the processors and graphics chips (two SH-4, two PowerVR2) and adds a geometry processor, the Elan, for much richer 3D scenes. Its games come on cartridges or GD-ROM. Its library is short but memorable, including racing games linked over a network.

Its games include **Virtua Fighter 4** (and Evolution, Final Tuned), **Initial D Arcade Stage** (1 to 3), **Beach Spikers**, **Club Kart**, **Wild Riders**, **Soul Surfer**, **The King of Route 66** and **Virtua Striker 3**.

RetroBat offers three emulators: the **flycast** libretro core (default), standalone **Flycast** and **Demul**.

{% embed url="https://en.wikipedia.org/wiki/Sega_NAOMI" %}

## At a glance

<table><thead><tr><th width="211.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\naomi2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: flycast</td></tr><tr><td><strong>BIOS</strong></td><td><code>naomi2.zip</code> in <code>bios\dc</code></td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, every emulator (per-game mapping for the flycast cores)</td></tr><tr><td><strong>Save states</strong></td><td>flycast core, Flycast (managed by RetroBat); Demul through hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No (Flycast: GGPO and NAOMI network, specific to the emulator)</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>Flycast</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="165.75">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: flycast</strong> (default)</td><td>Very good compatibility, buttons placed as on the cabinet for each game, save states, RetroArch shaders and hotkeys.</td><td>No mapping file supplied for wheels.</td></tr><tr><td><strong>flycast</strong></td><td>Same base as the core, with its own menus. Per-game mapping, save states, wheels (Initial D, Club Kart, The King of Route 66, Wild Riders), GGPO online play and NAOMI network (linked cabinets).</td><td>—</td></tr><tr><td><strong>demul</strong></td><td>Long-standing emulator, also used for NAOMI and Atomiswave.</td><td>Lower compatibility. Same button layout for every game. Save states not managed by RetroBat.</td></tr></tbody></table>

## BIOS

| File         | Folder    | Used by                    |
| ------------ | --------- | -------------------------- |
| `naomi2.zip` | `bios\dc` | Every game, every emulator |

`naomi2.zip` is the NAOMI 2 BIOS in MAME format, different from the NAOMI one. The flycast core and standalone Flycast both look for it in `bios\dc`; Demul finds it in `bios\dc`, `bios` or the games folder. Its content depends on the MAME version.

<details>

<summary>Content of naomi2.zip</summary>

```
naomi2.zip
- 315-6146.bin "728bfe038ce280872057e365ebfc0fee"
- 315-6215.bin "baf83367044924067e09856ba164aa6f"
- epr-23605.ic27 "6f8ad6e3ab04c8ae1cbcaa652b91cf4e"
- epr-23605a.ic27 "f3f39513484df216d9979f6ae7577942"
- epr-23605b.ic27 "ab046e62c51d67fb89eade2b8d5f6a8d"
- epr-23605c.ic27 "096a5217ff6e6c6cafe65a03336760ab"
- epr-23605c_multi.ic27 "659d579ba9aef5b025d87323044e83f4"
- epr-23607.ic27 "cbe0984d03d73869c23da5a3dd2ce207"
- epr-23607b.ic27 "b624ec7b3b90fdf3be103cdfb1679d1d"
- epr-23607c.ic27 "a9d82db14b823a5a57885bea1a998eb7"
- epr-23608.ic27 "3b1315be24dc8d17f4fa18f3bfc5fe5c"
- epr-23608a.ic27 "0143cf852cb2a8a41f217bc688f62105"
- epr-23608b.ic27 "8b88c1f5a06e9b560e887c3b9f879237"
- epr-23608c.ic27 "b49702e4fadb3b5f9143a3d20afd04b5"
- epr-23609b.ic27 "ecadb008179ca1e6f4fe3fa091ab5df2"
- main_eeprom.bin "edeed38a9795e062a9af28c3eba22040"
- sp5001.bin "14e6bffff0d4dff6a5a547e7c43680ff"
- sp5001-a.bin "689d2228b00fb59781f82af6e8ecdb78"
- sp5001-b.bin "8373a11106c1c2fc21ac839f75ea488f"
- sp5002-a.bin "7eecfb8e8f82b47ffab92a0c5528100e"
- x76f100_eeprom.bin "960ece0dc22a7c5ff81c812a2993e7cc"
```

</details>

## Which game format?

<table><thead><tr><th width="136.5">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>MAME format games, to keep as they are, neither unzipped nor renamed (<code>vf4.zip</code>, <code>initdv3e.zip</code>, <code>clubkrt.zip</code>…). Clones need the parent game in the same folder. GD-ROM games also have a <code>.chd</code> file (see <a href="sega-naomi-2.md#gd-rom-games-chd-files"><strong>Guides</strong></a>).</td></tr><tr><td><strong>.decomp</strong></td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

## Controls

### Automatic setup

RetroBat sets up the controllers for the three emulators. The controls shared by every game:

<table><thead><tr><th width="177.75">Cabinet</th><th>Controller</th></tr></thead><tbody><tr><td>Joystick</td><td>D-pad, left stick</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Coin</td><td>SELECT</td></tr><tr><td>Test</td><td>R3 (with the service menu enabled, see <a href="sega-naomi-2.md#service-menu-and-test-menu"><strong>Guides</strong></a>)</td></tr><tr><td>Service</td><td>L3 (with the service menu enabled, see <a href="sega-naomi-2.md#service-menu-and-test-menu"><strong>Guides</strong></a>)</td></tr></tbody></table>

* **flycast core** and **Flycast**: the position of the action buttons is defined game by game, to match the cabinet layout. The files used are `libretro_flycast_naomi2.yml` (core) and `flycast_Arcade.yml` (Flycast), see the [**Emulator specific controller configuration**](../../../../controllers/controller-configuration.md#adapting-the-controls-without-disabling-autoconfiguration) page. **CONTROLS > CONTROLLER LAYOUT** picks another layout when the file offers one.
* **Flycast**: **CONTROLS > USE DPAD** moves the analog controls to the d-pad.
* **Demul**: same layout for every game: buttons 1 to 4 on SOUTH, EAST, WEST, NORTH, buttons 5 to 8 on L1, R1, L2, R2.

### Wheels

Flycast supports wheels (**WHEELS > ENABLE WHEEL**) for **Initial D**, **Club Kart**, **The King of Route 66**, **Wild Riders** and **Sega Driving Simulator**. **WHEELS > WHEEL BUTTON LAYOUT** adapts the buttons to the game: gears on A / B for Initial D, reverse on X for The King of Route 66. The flycast core also supports wheels, but RetroBat does not supply its mapping file yet. For the supported wheels, see the [**Wheels**](../../../../controllers/supported-controllers/wheels.md) page.

### Hotkeys

The flycast core uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

**Flycast**

| Hotkey             | Action              | Keyboard |
| ------------------ | ------------------- | -------- |
| **HOTKEY + START** | Quit                | Esc      |
| **HOTKEY + SOUTH** | Flycast menu        | F1       |
| **HOTKEY + WEST**  | Save state          | F2       |
| **HOTKEY + NORTH** | Load state          | F4       |
| **HOTKEY + RIGHT** | Fast forward (hold) | L        |
| **HOTKEY + R3**    | Screenshot          | F8       |

**Demul**

| Hotkey             | Action           | Keyboard |
| ------------------ | ---------------- | -------- |
| **HOTKEY + START** | Quit             |          |
| **HOTKEY + WEST**  | Demul save state | F2       |
| **HOTKEY + NORTH** | Demul load state | F4       |

Demul save states stay in Demul: they do not show up in the save state manager.

## Folders

| Content                                  | Folder                                                                     |
| ---------------------------------------- | -------------------------------------------------------------------------- |
| BIOS                                     | `bios\dc`                                                                  |
| flycast core: save states                | `saves\naomi2\libretro.flycast`                                            |
| Flycast: game saves (NVRAM, EEPROM)      | `saves\naomi2\reicast`                                                     |
| Flycast: save states                     | `saves\naomi2\flycast\sstates` (copied from `saves\naomi2\reicast\states`) |
| Flycast: configuration                   | `emulators\flycast\emu.cfg`                                                |
| Demul: game saves (NVRAM)                | `saves\naomi2\demul`                                                       |
| Demul: configuration                     | `emulators\demul\Demul.ini`, `emulators\demul\padDemul.ini`                |
| Per-game mapping (flycast core, Flycast) | `system\resources\inputmapping` (editable copy in `user\inputmapping`)     |

## Guides

### GD-ROM games (CHD files)

GD-ROM games (**Virtua Fighter 4**, **Initial D**…) need, on top of their `.zip`, the disc image in `.chd` format. Place the `.chd` in a folder named after the `.zip`, without renaming either of them:

```
roms\
└─ naomi2\
   ├─ vf4tuned\
   │  └─ gds-0036f.chd
   └─ vf4tuned.zip
```

Only the `.zip` shows up in the game list.

### Service menu and test menu

The cabinet test menu sets the number of credits, the difficulty, the number of rounds, and checks the controls.

1. Enable **EMULATION > SERVICE MODE** (flycast core) or **EMULATION > ENABLE SERVICE MENU** (Flycast). With Demul, the buttons are always active.
2. In game, press **R3** (Test) to open the menu, then browse with the cabinet buttons. **L3** (Service) adds a service credit.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (603).png" alt="" width="563"><figcaption></figcaption></figure></div>

### Free play and region

* **EMULATION > FREE PLAY** (flycast core, Flycast, on by default) sets the game without coins: START is enough to play. When off, add credits with **SELECT**.
* **EMULATION > REGION** (flycast core) picks the cabinet region (Japan, USA, Europe): it changes the language and sometimes the game content.

These settings are written to the cabinet memory at launch. If a game keeps the former setting, change it in its test menu too.

### Other useful options

<table><thead><tr><th width="320.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Raises the rendering resolution (the three emulators).</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>Flycast, Demul: 4:3, 16:9 or stretched.</td></tr><tr><td><strong>VISUAL RENDERING > WIDESCREEN PATCHES</strong> / <strong>WIDESCREEN HACK</strong></td><td>16:9 display: the patches fix compatible games, the hack stretches the picture of every game (with glitches).</td></tr><tr><td><strong>NETWORK > NETWORK TYPE</strong> (Flycast)</td><td>GGPO for online fighting games, or <strong>NAOMI</strong> to link several cabinets (Club Kart, Initial D, The King of Route 66); <strong>HOST GAME</strong> and <strong>SERVER</strong> tell who hosts.</td></tr><tr><td><strong>NETWORK > BROADCAST DIGITAL OUTPUTS</strong></td><td>Sends the cabinet outputs (lamps…) to MameHooker (flycast core, Flycast).</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="332.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start</td><td>Check <code>naomi2.zip</code> in <code>bios\dc</code> (<code>naomi.zip</code> does not fit), and the parent game for a clone.</td></tr><tr><td>A GD-ROM game does not start</td><td>Check the <code>.chd</code> in the folder named after the <code>.zip</code> (see <a href="sega-naomi-2.md#gd-rom-games-chd-files"><strong>Guides</strong></a>).</td></tr><tr><td>The game is slow or badly displayed with Demul</td><td>Use the flycast core or Flycast, more compatible for NAOMI 2.</td></tr><tr><td>The buttons are not in the right place</td><td>With Demul, the layout is the same for every game: use the flycast core or Flycast.</td></tr></tbody></table>
