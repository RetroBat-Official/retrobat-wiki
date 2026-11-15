---
description: Namco
---

# Namco 246/256

<div align="left"><figure><img src="../../../.gitbook/assets/image (441).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Namco System 246** is an arcade system board released by Namco in 2001. It is built on the hardware of the Sony PlayStation 2 (the arcade "COH-H" models), with a few additions for arcade use: a JVS interface for the cabinet controls, a security dongle (a special memory card that contains the game software) and the game data on a CD, a DVD or a hard drive.

It was followed by the **System 256**, a faster revision used by games such as _Tekken 5_, and the **System Super 256**, made for _Time Crisis 4_. These boards are often called **System 2x6**.

Many famous arcade games ran on these boards: _Tekken 4_ and _Tekken 5_, _Soulcalibur II_ and _III_, _Time Crisis 3_ and _4_, _Vampire Night_, _Ridge Racer V Arcade Battle_, _Wangan Midnight Maximum Tune_, _Cobra The Arcade_, _Bloody Roar 3_, _Super Dragon Ball Z_, _Mobile Suit Gundam_ games and the _Taiko no Tatsujin_ series.

{% embed url="https://en.wikipedia.org/wiki/Namco_System_246" %}

## At a glance

<table><thead><tr><th width="236.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\namco2x6</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .m3u .acgame</td></tr><tr><td><strong>Default emulator</strong></td><td>pcsx2x6</td></tr><tr><td><strong>BIOS</strong></td><td><code>r27v1602f.7d</code> or <code>r27v1602f.8g</code> in <code>bios\pcsx2\bios</code></td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>play</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>pcsx2x6, play, TeknoParrot</td></tr><tr><td><strong>Wheels</strong></td><td>pcsx2x6, TeknoParrot</td></tr></tbody></table>

## Which emulator to choose?

<table><thead><tr><th width="125.75">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>pcsx2x6</strong> (default)</td><td>PCSX2 fork dedicated to System 246/256: best compatibility, high resolution, guns, wheels</td><td>Needs a System 246/256 BIOS and the game dongle dump</td></tr><tr><td>play</td><td>Works with MAME-style .zip romsets, no BIOS needed</td><td>Lower compatibility, one gun only (mouse aiming)</td></tr><tr><td>teknoparrot</td><td>Runs the games through TeknoParrot profiles (Play! or pcsx2x6 inside TeknoParrot)</td><td>Requires TeknoParrot and its game profiles</td></tr></tbody></table>

## BIOS

### BIOS files

The BIOS is only needed by **pcsx2x6**. Copy it to the `bios\pcsx2\bios` folder of RetroBat.

| BIOS file    | Board      |
| ------------ | ---------- |
| r27v1602f.7d | System 246 |
| r27v1602f.8g | System 256 |

{% hint style="info" %}
One BIOS is enough. RetroBat checks that at least one of these files is present.
{% endhint %}

### Which BIOS do I need?

* **r27v1602f.8g** (System 256) is recommended: it runs the System 256 games and the System 246 games.
* RetroBat chooses the BIOS automatically: the System 246 BIOS when the `.acgame` file of the game declares `platform=246`, the System 256 BIOS otherwise. If the chosen file is missing, the other one is used.
* To choose yourself, use the **FORCE BIOS** option (EMULATION submenu): SYSTEM 246 or SYSTEM 256.

<div align="left"><figure><img src="../../../.gitbook/assets/image (442).png" alt=""><figcaption></figcaption></figure></div>

* Play! and TeknoParrot do not use these files.

## Game formats

### pcsx2x6: .acgame files

An arcade game is made of several files: the game data (CD, DVD or hard drive image), a boot program (.elf), the security dongle (.ps2) and the settings of the machine (sram.bin). A small **.acgame** text file tells pcsx2x6 where to find them.

Example for a game whose ID is `NM00007`:

```
📁 roms\namco2x6
   📄 SoulCalibur II.acgame
   📂 NM00007
      📄 NM00007.chd      (game data)
      📄 boot.elf         (boot program)
      📄 sram.bin         (created at first launch if missing)
📁 saves\namco2x6\memcards
   📄 NM00007.ps2         (security dongle)
```

Content of `SoulCalibur II.acgame`:

```ini
[game]
gameid=NM00007
```

With recent versions of pcsx2x6, the **gameid** is the only mandatory entry: the other values are found automatically. You can still declare them:

<table><thead><tr><th width="157">Section</th><th>Entry</th><th>Description</th></tr></thead><tbody><tr><td>[game]</td><td>name</td><td>Game name</td></tr><tr><td>[game]</td><td>gameid</td><td>Game ID (mandatory)</td></tr><tr><td>[game]</td><td>platform</td><td><code>246</code>, <code>256</code> or <code>super256</code> (Time Crisis 4)</td></tr><tr><td>[data]</td><td>subdir</td><td>Game subfolder (default: the game ID)</td></tr><tr><td>[data]</td><td>elf</td><td>Boot program (default: <code>boot.elf</code>)</td></tr><tr><td>[data]</td><td>dongle</td><td>Dongle file in <code>saves\namco2x6\memcards</code> (default: <code>GAMEID.ps2</code>)</td></tr><tr><td>[data]</td><td>card</td><td>Second memory card, only for the Conquest mode of <em>Soulcalibur II</em></td></tr><tr><td>[data]</td><td>mediasrc</td><td>Game data file (default: <code>GAMEID.chd</code>)</td></tr><tr><td>[data]</td><td>media</td><td><code>CD</code>, <code>DVD</code> or <code>HDD</code></td></tr><tr><td>[data]</td><td>sram</td><td>Settings file (default: <code>sram.bin</code>)</td></tr><tr><td>[data]</td><td>256Region</td><td>Region of the System 256 (<code>ASIA4</code>, <code>ASIA5</code>, <code>JAPAN</code>), used by Taiko no Tatsujin</td></tr></tbody></table>

{% hint style="info" %}
The **.ps2** files are dumps of the game security dongle, not memory cards. pcsx2x6 is supplied with a script (`utils/arcade_game_template.py`) that creates a template .acgame file and boot program for each game.
{% endhint %}

All these information can be found on the PCSX2X6 emulator website :

{% embed url="https://ps2homebrew-arcade.github.io/pcsx2x6/game_config/" %}

### Play!: .zip and .m3u files

* Copy the game romset (**.zip**, MAME format) to `roms\namco2x6`. The file name must match the Play! arcade profile (for example `tekken4.zip`). If the game uses a disc or a hard drive image (.chd), put it in a subfolder with the same name as the game, like with MAME.
* For games without a .zip file, create an empty **.m3u** file named after the Play! arcade profile. The list of profiles is in `emulators\play\arcadedefs`.

### TeknoParrot

The game file must have the same name as the TeknoParrot profile (`emulators\teknoparrot\GameProfiles`). RetroBat reads the profile to know whether TeknoParrot must use Play! or pcsx2x6. See the TeknoParrot page for the installation of the games.

## Controls

### Controller autoconfiguration

| Emulator    | Autoconfig | Players |
| ----------- | ---------- | ------- |
| pcsx2x6     | Yes        | 2       |
| play        | Yes        | 2       |
| teknoparrot | Yes        | 2       |

### Arcade layout (pcsx2x6)

<table><thead><tr><th width="220.25">Arcade control</th><th>Your controller</th></tr></thead><tbody><tr><td>Coin</td><td>SELECT</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Joystick</td><td>D-pad</td></tr><tr><td>Buttons 1 to 4</td><td>WEST, NORTH, SOUTH, EAST</td></tr><tr><td>Test (service menu)</td><td>R3</td></tr><tr><td>Service</td><td>L3</td></tr></tbody></table>

For fighting games, the buttons follow the arcade layout: for example _Tekken_ left punch WEST, right punch NORTH, left kick SOUTH, right kick EAST, and _Soulcalibur_ A (horizontal) WEST, B (vertical) NORTH, G (guard) SOUTH, K (kick) EAST. Racing games use R2 to accelerate, L2 to brake and L1/R1 to shift gears.

Test and Service are only active when **ENABLE SERVICE MENU** is on (EMULATION submenu).

<div align="left"><figure><img src="../../../.gitbook/assets/image (443).png" alt=""><figcaption></figcaption></figure></div>

The **CONTROLLER LAYOUT** option (CONTROLS submenu) moves the shoulder buttons and triggers (MODERN 8 BUTTONS, 8 BUTTONS ALTERNATIVE).

<div align="left"><figure><img src="../../../.gitbook/assets/image (445).png" alt=""><figcaption></figcaption></figure></div>

### Keyboard and arcade sticks

| Action        | Keyboard (QWERTY) | Keyboard (AZERTY) |
| ------------- | ----------------- | ----------------- |
| Coin P1 / P2  | 5 / 6             | ( / -             |
| Start P1 / P2 | 1 / 2             | & / é             |
| Test          | 0                 | à                 |
| Service       | 9                 | ç                 |

RetroBat detects AZERTY keyboards automatically; the **AZERTY KEYBOARD** option forces it. For arcade sticks recognized as a keyboard (IPAC, X-Arcade), use **CONFIGURE SPECIAL KEYBOARD STICK** (CONTROLS submenu).

### Play! controls

RetroBat configures the Play! buttons game by game, with the `system\resources\inputmapping\play.yml` file. Fighting games have the same buttons as with pcsx2x6, and the **CONTROLLER LAYOUT** option (CONTROLS submenu) places the buttons for arcade sticks.

<table><thead><tr><th width="220.25">Arcade control</th><th>Your controller</th></tr></thead><tbody><tr><td>Coin</td><td>SELECT</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Joystick</td><td>D-pad</td></tr><tr><td>Test (service menu)</td><td>R3</td></tr></tbody></table>

* **Service menu:** Play! opens it when L3 and R3 are pressed together, RetroBat puts both on R3. In games that use the button 5 of the cabinet, press R3 and that button: right kick (EAST) in _Tekken 4_, _Tekken 5_ and _Pride GP 2003_, jump (SOUTH) in _Super Dragon Ball Z_. With Play!, the service menu is always active (no ENABLE SERVICE MENU option) and there is no Service button.
* **Racing games** (_Ace Driver 3_, _Wangan Midnight_, _Battle Gear 3_, _Moto GP_, _Ridge Racer V_): steering on the left stick, gas on R2, brake on L2, gear shifting on L1 / R1 in the games that have gears. Play! does not support real wheels.
* **Shooting games** (_Time Crisis 3_ and _4_, _Cobra The Arcade_, _Vampire Night_): you aim with the mouse. With a controller, shoot with R2 and pedal with L2 (no pedal in _Vampire Night_). With a gun, see Light guns below.
* Games without settings in `play.yml` (_Taiko no Tatsujin_, _Bloody Roar 3_, _Zoids Infinity_…) use the PS2 layout: SOUTH = ✕, EAST = ○, WEST = □, NORTH = △, and L1 / R1 / L2 / R2.

To change the buttons of a game, copy `play.yml` to `user\inputmapping` and edit the copy. Each game is a block named after the game (for example `tekken4`), with one line per controller button (`south`, `east`, `west`, `north`, `l1`, `r1`, `l2`, `r2`, `l3`, `r3`, `select`, `start`) and the cabinet control (`Button1` to `Button10`, `gas` for the accelerator, `brake` for the brake):

```yaml
tekken4:
  west: Button1   # left punch
  north: Button2  # right punch
  south: Button4  # left kick
  east: Button5   # right kick
```

A `<game>_modern8`, `<game>_8alternative` or `<game>_6alternative` block is used instead when the CONTROLLER LAYOUT option has that value. A clone uses the block of its parent game.

If you disable **AUTOCONFIGURE CONTROLLERS**, Play! uses the input profile named after the game in `emulators\play\Play Data Files\inputprofiles` (or the default profile).

### Hotkeys

<table><thead><tr><th width="228.25">Hotkey</th><th>pcsx2x6</th><th>Play!</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td><td>Quit</td></tr><tr><td>HOTKEY + SOUTH</td><td>Menu</td><td></td></tr><tr><td>HOTKEY + WEST</td><td>Save state</td><td>Save state</td></tr><tr><td>HOTKEY + NORTH</td><td>Load state</td><td>Load state</td></tr><tr><td>HOTKEY + UP / DOWN</td><td>Change slot</td><td></td></tr><tr><td>HOTKEY + LEFT</td><td>Slow motion</td><td></td></tr><tr><td>HOTKEY + RIGHT</td><td>Fast forward</td><td></td></tr><tr><td>HOTKEY + R3</td><td>Screenshot</td><td></td></tr><tr><td>HOTKEY + L3</td><td>Pause</td><td></td></tr></tbody></table>

With Play!, the state uses the slot chosen in RetroBat before the launch: it does not change during the game.

### Light guns

pcsx2x6 supports 2 guns for _Time Crisis 3_, _Time Crisis 4_, _Vampire Night_ or _Cobra The Arcade_. Enable **ENABLE GUN** (GUNS submenu).

* Coins and Start: keys 5/6 and 1/2. With a Mayflash DolphinBar, D-pad left = coin, D-pad right = start.
* **SINDEN BORDER**: border for Sinden guns (enabled automatically when a Sinden gun is detected).
* **CROSSHAIR**: mouse cursor or custom crosshair.

**Play!** supports one gun (player 1) for _Time Crisis 3_, _Time Crisis 4_, _Cobra The Arcade_ and _Vampire Night_: the aim follows the mouse cursor. With **ENABLE GUN**: trigger = left click, pedal = right click (_Time Crisis_, _Cobra_), Start = key 1, coin = key 5. The buttons are in the `<game>_gun` blocks of `play.yml`.

### Wheels

pcsx2x6 configures the following wheels automatically when **ENABLE WHEEL** is on (WHEELS submenu): Logitech G29, Logitech G923 (PS), Logitech Driving Force GT, Thrustmaster T300RS (PS3), Moza R5.

* **ENABLE FORCE FEEDBACK**: force feedback.
* **GEARUP/GEARDOWN TO GEAR3/GEAR4 CONVERTER**: sequential shifting on games using a gear stick.
* **FORCE WHEEL 1 INDEX**: if RetroBat selects the wrong wheel.

## Folders

<table><thead><tr><th width="138.25">Emulator</th><th>Content</th><th>Folder</th></tr></thead><tbody><tr><td>pcsx2x6</td><td>Dongles (.ps2) and memory cards</td><td><code>saves\namco2x6\memcards</code></td></tr><tr><td>pcsx2x6</td><td>Machine settings (sram.bin)</td><td>game subfolder in <code>roms\namco2x6</code></td></tr><tr><td>pcsx2x6</td><td>Save states</td><td><code>saves\namco2x6\namco2x6\sstates</code></td></tr><tr><td>pcsx2x6</td><td>Screenshots</td><td><code>screenshots\pcsx2x6</code></td></tr><tr><td>play</td><td>Data and input profiles</td><td><code>emulators\play\Play Data Files</code></td></tr><tr><td>play</td><td>Arcade profiles</td><td><code>emulators\play\arcadedefs</code></td></tr><tr><td>play</td><td>Save states</td><td><code>saves\namco2x6\play\states</code></td></tr><tr><td>play</td><td>Buttons per game</td><td><code>system\resources\inputmapping\play.yml</code> (custom copy in <code>user\inputmapping</code>)</td></tr></tbody></table>

## Guides

### Service menu (test mode)

Arcade games are configured in their service menu: free play, difficulty, number of rounds, controls test… Enable **ENABLE SERVICE MENU** (EMULATION submenu), launch the game and press R3 (or 0 on the keyboard). The settings are saved in the `sram.bin` file of the game.

<div align="left"><figure><img src="../../../.gitbook/assets/image (444).png" alt=""><figcaption></figcaption></figure></div>

### Soulcalibur II Conquest mode

The Conquest mode uses a second memory card. Add `card=ConquestCard0.conquestcard` to the `[data]` section of the .acgame file and put the card in `saves\namco2x6\memcards`. At first use, open the service menu and select DATA CLEAR > Clear All, then exit and save: the card is formatted at the next boot.

### Improving graphics

Use **INTERNAL RESOLUTION** (pcsx2x6 and Play!) to render the games in high definition, and the PCSX2 visual options (VISUAL RENDERING submenu).

## Known issues

<table><thead><tr><th width="300.25">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>"No BIOS found in bios/pcsx2/bios folder."</td><td>Copy r27v1602f.8g (or r27v1602f.7d) to <code>bios\pcsx2\bios</code>.</td></tr><tr><td>A System 256 game does not start</td><td>Use the System 256 BIOS: FORCE BIOS = SYSTEM 256.</td></tr><tr><td>The game stops at the dongle check</td><td>Check that the .ps2 file is in <code>saves\namco2x6\memcards</code> and named like the <code>dongle</code> entry (or <code>GAMEID.ps2</code>).</td></tr><tr><td>The game starts in the service menu</td><td>Disable ENABLE SERVICE MENU.</td></tr><tr><td>Play! does not find the game</td><td>The .zip (or .m3u) must have the exact name of the Play! arcade profile.</td></tr><tr><td><em>Soulcalibur II</em> hangs on a white screen</td><td>Format the Conquest card (see Guides).</td></tr><tr><td>The service menu does not open with Play!</td><td>Press R3. In <em>Tekken</em>, <em>Pride GP 2003</em> and <em>Super Dragon Ball Z</em>, press R3 and the button 5 (see Play! controls).</td></tr></tbody></table>
