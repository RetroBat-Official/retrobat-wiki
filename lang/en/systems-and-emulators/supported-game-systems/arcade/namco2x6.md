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

<table><thead><tr><th width="236.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\namco2x6</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .m3u .acgame</td></tr><tr><td><strong>Default emulator</strong></td><td>pcsx2x6</td></tr><tr><td><strong>BIOS</strong></td><td><code>r27v1602f.7d</code> or <code>r27v1602f.8g</code> in <code>bios\pcsx2\bios</code></td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>pcsx2x6, TeknoParrot</td></tr><tr><td><strong>Wheels</strong></td><td>pcsx2x6, TeknoParrot</td></tr></tbody></table>

## Which emulator to choose?

| Emulator              | Strengths                                                                                 | Limits                                               |
| --------------------- | ----------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| **pcsx2x6** (default) | PCSX2 fork dedicated to System 246/256: best compatibility, high resolution, guns, wheels | Needs a System 246/256 BIOS and the game dongle dump |
| play                  | Works with MAME-style .zip romsets, no BIOS needed                                        | Lower compatibility, no guns                         |
| teknoparrot           | Runs the games through TeknoParrot profiles (Play! or pcsx2x6 inside TeknoParrot)         | Requires TeknoParrot and its game profiles           |

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

| Section | Entry     | Description                                                                     |
| ------- | --------- | ------------------------------------------------------------------------------- |
| \[game] | name      | Game name                                                                       |
| \[game] | gameid    | Game ID (mandatory)                                                             |
| \[game] | platform  | `246`, `256` or `super256` (Time Crisis 4)                                      |
| \[data] | subdir    | Game subfolder (default: the game ID)                                           |
| \[data] | elf       | Boot program (default: `boot.elf`)                                              |
| \[data] | dongle    | Dongle file in `saves\namco2x6\memcards` (default: `GAMEID.ps2`)                |
| \[data] | card      | Second memory card, only for the Conquest mode of _Soulcalibur II_              |
| \[data] | mediasrc  | Game data file (default: `GAMEID.chd`)                                          |
| \[data] | media     | `CD`, `DVD` or `HDD`                                                            |
| \[data] | sram      | Settings file (default: `sram.bin`)                                             |
| \[data] | 256Region | Region of the System 256 (`ASIA4`, `ASIA5`, `JAPAN`), used by Taiko no Tatsujin |

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

Play! uses a PlayStation 2 controller layout. Specific mappings per game are stored in `system\resources\inputmapping\play_Arcade.yml` (copy it to `user\inputmapping` to customize it).

If you disable **AUTOCONFIGURE CONTROLLERS**, Play! uses the input profile named after the game in `emulators\play\Play Data Files\inputprofiles` (or the default profile).

### Hotkeys

| Hotkey             | pcsx2x6      | Play! |
| ------------------ | ------------ | ----- |
| HOTKEY + START     | Quit         | Quit  |
| HOTKEY + SOUTH     | Menu         |       |
| HOTKEY + WEST      | Save state   |       |
| HOTKEY + NORTH     | Load state   |       |
| HOTKEY + UP / DOWN | Change slot  |       |
| HOTKEY + LEFT      | Slow motion  |       |
| HOTKEY + RIGHT     | Fast forward |       |
| HOTKEY + R3        | Screenshot   |       |
| HOTKEY + L3        | Pause        |       |

### Light guns

pcsx2x6 supports 2 guns for _Time Crisis 3_, _Time Crisis 4_, _Vampire Night_ or _Cobra The Arcade_. Enable **ENABLE GUN** (GUNS submenu).

* Coins and Start: keys 5/6 and 1/2. With a Mayflash DolphinBar, D-pad left = coin, D-pad right = start.
* **SINDEN BORDER**: border for Sinden guns (enabled automatically when a Sinden gun is detected).
* **CROSSHAIR**: mouse cursor or custom crosshair.

### Wheels

pcsx2x6 configures the following wheels automatically when **ENABLE WHEEL** is on (WHEELS submenu): Logitech G29, Logitech G923 (PS), Logitech Driving Force GT, Thrustmaster T300RS (PS3), Moza R5.

* **ENABLE FORCE FEEDBACK**: force feedback.
* **GEARUP/GEARDOWN TO GEAR3/GEAR4 CONVERTER**: sequential shifting on games using a gear stick.
* **FORCE WHEEL 1 INDEX**: if RetroBat selects the wrong wheel.

## Folders

| Emulator | Content                         | Folder                            |
| -------- | ------------------------------- | --------------------------------- |
| pcsx2x6  | Dongles (.ps2) and memory cards | `saves\namco2x6\memcards`         |
| pcsx2x6  | Machine settings (sram.bin)     | game subfolder in `roms\namco2x6` |
| pcsx2x6  | Save states                     | `saves\namco2x6\namco2x6\sstates` |
| pcsx2x6  | Screenshots                     | `screenshots\pcsx2x6`             |
| play     | Data and input profiles         | `emulators\play\Play Data Files`  |
| play     | Arcade profiles                 | `emulators\play\arcadedefs`       |

## Guides

### Service menu (test mode)

Arcade games are configured in their service menu: free play, difficulty, number of rounds, controls test… Enable **ENABLE SERVICE MENU** (EMULATION submenu), launch the game and press R3 (or 0 on the keyboard). The settings are saved in the `sram.bin` file of the game.

<div align="left"><figure><img src="../../../.gitbook/assets/image (444).png" alt=""><figcaption></figcaption></figure></div>

### Soulcalibur II Conquest mode

The Conquest mode uses a second memory card. Add `card=ConquestCard0.conquestcard` to the `[data]` section of the .acgame file and put the card in `saves\namco2x6\memcards`. At first use, open the service menu and select DATA CLEAR > Clear All, then exit and save: the card is formatted at the next boot.

### Improving graphics

Use **INTERNAL RESOLUTION** (pcsx2x6 and Play!) to render the games in high definition, and the PCSX2 visual options (VISUAL RENDERING submenu).

## Known issues

<table><thead><tr><th width="300.25">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>"No BIOS found in bios/pcsx2/bios folder."</td><td>Copy r27v1602f.8g (or r27v1602f.7d) to <code>bios\pcsx2\bios</code>.</td></tr><tr><td>A System 256 game does not start</td><td>Use the System 256 BIOS: FORCE BIOS = SYSTEM 256.</td></tr><tr><td>The game stops at the dongle check</td><td>Check that the .ps2 file is in <code>saves\namco2x6\memcards</code> and named like the <code>dongle</code> entry (or <code>GAMEID.ps2</code>).</td></tr><tr><td>The game starts in the service menu</td><td>Disable ENABLE SERVICE MENU.</td></tr><tr><td>Play! does not find the game</td><td>The .zip (or .m3u) must have the exact name of the Play! arcade profile.</td></tr><tr><td><em>Soulcalibur II</em> hangs on a white screen</td><td>Format the Conquest card (see Guides).</td></tr></tbody></table>
