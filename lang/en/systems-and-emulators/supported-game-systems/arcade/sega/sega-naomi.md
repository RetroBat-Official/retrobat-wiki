---
description: Sega
---

# Sega NAOMI

<div align="left"><figure><img src="../../../../.gitbook/assets/image (600).png" alt="" width="418"><figcaption></figcaption></figure></div>

## Overview

The **NAOMI** (New Arcade Operation Machine Idea) is a Sega arcade board released in 1998. It reuses the Dreamcast architecture with more memory, which made console ports easier. Games first came on cartridges, then on GD-ROM from 2000 (the disc is copied to a memory board at startup). Very widespread, it also hosted games by Capcom, SNK, Treasure and Arc System Works, until the end of the 2000s.

Its games include **Crazy Taxi**, **The House of the Dead 2**, **Marvel vs. Capcom 2**, **Capcom vs. SNK 2**, **Ikaruga**, **Guilty Gear XX**, **Virtua Tennis**, **Dead or Alive 2**, **Power Stone 2**, **18 Wheeler**, **Ferrari F355 Challenge**, **Zombie Revenge**, **Under Defeat** and **Confidential Mission**.

RetroBat offers three emulators: the **flycast** libretro core (default), standalone **Flycast** and **Demul**.

{% embed url="https://en.wikipedia.org/wiki/Sega_NAOMI" %}

## At a glance

<table><thead><tr><th width="231.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\naomi</code></td></tr><tr><td><strong>Extensions</strong></td><td>.bin .dat .lst .zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: flycast</td></tr><tr><td><strong>BIOS</strong></td><td><code>naomi.zip</code> in <code>bios\dc</code></td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, every emulator (per-game mapping for the flycast cores)</td></tr><tr><td><strong>Save states</strong></td><td>flycast core, Flycast (managed by RetroBat); Demul through hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No (Flycast: GGPO and NAOMI network, specific to the emulator)</td></tr><tr><td><strong>Light guns</strong></td><td>flycast core, Flycast, Demul</td></tr><tr><td><strong>Wheels</strong></td><td>Flycast</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>hod2bios.zip</code>, <code>f355bios.zip</code>, <code>f355dlx.zip</code>, <code>airlbios.zip</code> in <code>bios\dc</code> (games with their own <a href="sega-naomi.md#bios">BIOS</a>)</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="172">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: flycast</strong> (default)</td><td>Very good compatibility, buttons placed as on the cabinet for each game, save states, up to 4 light guns, RetroArch shaders and hotkeys.</td><td>No mapping file supplied for wheels.</td></tr><tr><td><strong>flycast</strong></td><td>Same base as the core, with its own menus. Per-game mapping, save states, wheels, light guns with DemulShooter, GGPO online play and NAOMI network (linked cabinets).</td><td>—</td></tr><tr><td><strong>demul</strong></td><td>Long-standing emulator, also used for Atomiswave and Dreamcast.</td><td>Lower compatibility. Same button layout for every game. Save states not managed by RetroBat. Cannot read <code>.bin</code> / <code>.dat</code> / <code>.lst</code> files.</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="169.5">File</th><th width="136.5">Folder</th><th>Used by</th></tr></thead><tbody><tr><td><code>naomi.zip</code></td><td><code>bios\dc</code></td><td>Every game, every emulator</td></tr><tr><td><code>hod2bios.zip</code></td><td><code>bios\dc</code></td><td>The House of the Dead 2</td></tr><tr><td><code>f355bios.zip</code></td><td><code>bios\dc</code></td><td>Ferrari F355 Challenge Twin</td></tr><tr><td><code>f355dlx.zip</code></td><td><code>bios\dc</code></td><td>Ferrari F355 Challenge (deluxe version)</td></tr><tr><td><code>airlbios.zip</code></td><td><code>bios\dc</code></td><td>Airline Pilots</td></tr></tbody></table>

These archives are in MAME format. The flycast core and standalone Flycast both look for them in `bios\dc`; Demul finds them in `bios\dc`, `bios` or the games folder. Their content depends on the MAME version (reference md5 of `naomi.zip`: `eb4099aeb42ef089cfe94f8fe95e51f6`). GD-ROM games also use `naomi.zip`.

## Which game format?

<table><thead><tr><th width="162.75">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>MAME format games, to keep as they are, neither unzipped nor renamed (<code>crzytaxi.zip</code>, <code>mvsc2.zip</code>, <code>hotd2.zip</code>…). Clones need the parent game in the same folder. GD-ROM games also have a <code>.chd</code> file (see <a href="sega-naomi.md#gd-rom-games-chd-files"><strong>Guides</strong></a>).</td></tr><tr><td><strong>.bin</strong>, <strong>.dat</strong>, <strong>.lst</strong></td><td>Former NullDC format (<code>.bin</code> / <code>.dat</code> images and their <code>.lst</code> list): flycast cores only.</td></tr><tr><td><strong>.decomp</strong></td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

## Controls

### Automatic setup

RetroBat sets up the controllers for the three emulators. The controls shared by every game:

<table><thead><tr><th width="124">Cabinet</th><th>Controller</th></tr></thead><tbody><tr><td>Joystick</td><td>D-pad, left stick</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Coin</td><td>SELECT</td></tr><tr><td>Test</td><td>R3 (with the service menu enabled, see <a href="sega-naomi.md#service-menu-and-test-menu"><strong>Guides</strong></a>)</td></tr><tr><td>Service</td><td>L3 (with the service menu enabled, see <a href="sega-naomi.md#service-menu-and-test-menu"><strong>Guides</strong></a>)</td></tr></tbody></table>

* **flycast core** and **Flycast**: the position of the action buttons is defined game by game, to match the cabinet layout. The files used are `libretro_flycast_naomi.yml` (core) and `flycast_Arcade.yml` (Flycast), see the [**Emulator specific controller configuration**](../../../../controllers/controller-configuration.md#adapting-the-controls-without-disabling-autoconfiguration) page. **CONTROLS > CONTROLLER LAYOUT** picks another layout when the file offers one (for example for Dead or Alive 2).
* **Flycast**: **CONTROLS > USE DPAD** moves the analog controls to the d-pad.
* **Demul**: same layout for every game: buttons 1 to 4 on SOUTH, EAST, WEST, NORTH, buttons 5 to 8 on L1, R1, L2, R2.

### Light guns

Light gun games (**The House of the Dead 2**, **Confidential Mission**, **Death Crimson OX**, **Ninja Assault**, **Lupin the Third: The Shooting**) work with the flycast core (up to 4 guns), Flycast (2 guns, 4 with DemulShooter) and Demul (1 gun, 2 with DemulShooter). For the options and buttons, see the [**Light gun controls**](../../../../controllers/gun_controls.md) page.

### Wheels

Flycast supports wheels (**WHEELS > ENABLE WHEEL**) for **18 Wheeler**, **Crazy Taxi**, **Ferrari F355 Challenge** (with the clutch), **Tokyo Bus Guide** and **Wave Runner GP**. **WHEELS > WHEEL BUTTON LAYOUT** adapts the buttons to the game (for example reverse on B for Crazy Taxi). The flycast core also supports wheels, but RetroBat does not supply its mapping file yet. For the supported wheels, see the [**Wheels**](../../../../controllers/supported-controllers/wheels.md) page.

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

<table><thead><tr><th width="195.75">Hotkey</th><th width="209.75">Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td></td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Demul save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Demul load state</td><td>F4</td></tr></tbody></table>

Demul save states stay in Demul: they do not show up in the save state manager.

## Folders

<table><thead><tr><th width="349">Content</th><th>Folder</th></tr></thead><tbody><tr><td>BIOS</td><td><code>bios\dc</code></td></tr><tr><td>flycast core: save states</td><td><code>saves\naomi\libretro.flycast</code></td></tr><tr><td>Flycast: game saves (NVRAM, EEPROM)</td><td><code>saves\naomi\reicast</code></td></tr><tr><td>Flycast: save states</td><td><code>saves\naomi\flycast\sstates</code> (copied from <code>saves\naomi\reicast\states</code>)</td></tr><tr><td>Flycast: configuration</td><td><code>emulators\flycast\emu.cfg</code></td></tr><tr><td>Demul: game saves (NVRAM)</td><td><code>saves\naomi\demul</code></td></tr><tr><td>Demul: configuration</td><td><code>emulators\demul\Demul.ini</code>, <code>emulators\demul\padDemul.ini</code></td></tr><tr><td>Per-game mapping (flycast core, Flycast)</td><td><code>system\resources\inputmapping</code> (editable copy in <code>user\inputmapping</code>)</td></tr></tbody></table>

## Guides

### GD-ROM games (CHD files)

GD-ROM games (**Ikaruga**, **Capcom vs. SNK 2**, **Guilty Gear XX**…) need, on top of their `.zip`, the disc image in `.chd` format. Place the `.chd` in a folder named after the `.zip`, without renaming either of them:

```
roms\
└─ naomi\
   ├─ ikaruga\
   │  └─ gdl-0010.chd
   └─ ikaruga.zip
```

Only the `.zip` shows up in the game list.

### Service menu and test menu

The cabinet test menu sets the number of credits, the difficulty, the number of rounds, and checks the controls.

1. Enable **EMULATION > SERVICE MODE** (flycast core) or **EMULATION > ENABLE SERVICE MENU** (Flycast). With Demul, the buttons are always active.
2. In game, press **R3** (Test) to open the menu, then browse with the cabinet buttons. **L3** (Service) adds a service credit.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (601).png" alt="" width="563"><figcaption></figcaption></figure></div>

### Free play and region

* **EMULATION > FREE PLAY** (flycast core, Flycast, on by default) sets the game without coins: START is enough to play. When off, add credits with **SELECT**.
* **EMULATION > REGION** (flycast core) picks the cabinet region (Japan, USA, Europe): it changes the language and sometimes the game content.

These settings are written to the cabinet memory at launch. If a game keeps the former setting, change it in its test menu too.

### Other useful options

<table><thead><tr><th width="327.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Raises the rendering resolution (the three emulators).</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>Flycast, Demul: 4:3, 16:9 or stretched.</td></tr><tr><td><strong>VISUAL RENDERING > WIDESCREEN PATCHES</strong> / <strong>WIDESCREEN HACK</strong></td><td>16:9 display: the patches fix compatible games, the hack stretches the picture of every game (with glitches).</td></tr><tr><td><strong>VIDEO > TATE MODE</strong></td><td>Vertical display for shoot'em ups (Ikaruga, Under Defeat…) on a rotated screen (flycast core, Flycast).</td></tr><tr><td><strong>NETWORK > NETWORK TYPE</strong> (Flycast)</td><td>GGPO for online fighting games, or <strong>NAOMI</strong> to link several cabinets; <strong>HOST GAME</strong> and <strong>SERVER</strong> tell who hosts.</td></tr><tr><td><strong>NETWORK > BROADCAST DIGITAL OUTPUTS</strong></td><td>Sends the cabinet outputs (lamps…) to MameHooker (flycast core, Flycast).</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="340.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start</td><td>Check <code>naomi.zip</code> in <code>bios\dc</code> (or the game's own BIOS), and the parent game for a clone.</td></tr><tr><td>A GD-ROM game does not start</td><td>Check the <code>.chd</code> in the folder named after the <code>.zip</code> (see <a href="sega-naomi.md#gd-rom-games-chd-files"><strong>Guides</strong></a>).</td></tr><tr><td>The House of the Dead 2 does not start</td><td>Add <code>hod2bios.zip</code> to <code>bios\dc</code>.</td></tr><tr><td>The buttons are not in the right place</td><td>With Demul, the layout is the same for every game: use the flycast core or Flycast.</td></tr><tr><td>A <code>.bin</code> / <code>.dat</code> / <code>.lst</code> game does not start with Demul</td><td>Demul only reads MAME format games: use the flycast core or Flycast.</td></tr><tr><td>The light gun game does not react</td><td>Enable <strong>GUNS > ENABLE GUN</strong>, then check the <a href="../../../../controllers/gun_controls.md"><strong>Light gun controls</strong></a> page.</td></tr></tbody></table>
