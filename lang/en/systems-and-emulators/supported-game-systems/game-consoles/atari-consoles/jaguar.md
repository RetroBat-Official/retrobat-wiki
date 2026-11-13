---
description: Atari
---

# Jaguar

<div align="left"><figure><img src="../../../../.gitbook/assets/image.png" alt="" width="425"><figcaption></figcaption></figure></div>

## Presentation

The **Jaguar** is Atari's last console. It came out in late 1993 in the United States, then in 1994 in Europe and Japan, and Atari marketed it as the first "64-bit" console. Its controller is instantly recognizable: three action buttons and a twelve-key keypad, over which you slide a plastic overlay specific to each game.

The machine was powerful but hard to program, and publishers soon left it for the PlayStation and the Saturn. It only has about fifty cartridge games, including Tempest 2000, Alien vs Predator, Iron Soldier, Doom and Rayman, and sold fewer than 250,000 units. A CD drive came out in 1995 (see the [**Jaguar CD**](jaguarcd.md) page), then Atari stopped making consoles in 1996.

{% embed url="https://en.wikipedia.org/wiki/Atari_Jaguar" %}

## At a glance

<table><thead><tr><th width="225.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\jaguar</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .cue .cdi .j64 .jag .rom .abs .cof .bin .prg .squashfs</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: virtualjaguar</td></tr><tr><td><strong>BIOS</strong></td><td>None required</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BigPEmu, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>[BIOS] Atari Jaguar (World).j64</code> (needed by Phoenix)</td></tr></tbody></table>

## Which emulator to choose?

<table><thead><tr><th width="144">Emulator</th><th width="172.75">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: virtualjaguar</strong> (default)</td><td>Everyone</td><td>Built into RetroArch: shaders, decorations, RetroAchievements, netplay. Doubled resolution, overclocking, Team Tap, Jaguar Pro controller.</td><td>A few demanding games run better with BigPEmu.</td></tr><tr><td><strong>bigpemu</strong></td><td>Those who want the best compatibility</td><td>Very good compatibility, save states, rewind, up to 8 players, the whole keypad on the controller.</td><td>No RetroAchievements. Hotkeys on L2 instead of the HOTKEY button.</td></tr><tr><td><strong>bizhawk</strong> (Jaguar)</td><td>Tool-assisted speedrun (TAS)</td><td>Recording and analysis tools, RetroAchievements.</td><td>Few options in RetroBat.</td></tr><tr><td><strong>phoenix</strong></td><td>As a fallback</td><td>An alternative when the others do not fit.</td><td>Requires the BIOS, no save states, only one hotkey (quit).</td></tr></tbody></table>

**When in doubt, keep libretro: virtualjaguar, and try BigPEmu if a game misbehaves.**

## BIOS

Only Phoenix needs a BIOS file. The other emulators embed it or do without it.

<table><thead><tr><th width="290.25">File</th><th width="251.25">MD5</th><th width="81.75">Location</th><th>Emulator</th></tr></thead><tbody><tr><td><code>[BIOS] Atari Jaguar (World).j64</code></td><td><code>bcfe348c565d9dedb173822ee6850dea</code></td><td><code>bios</code></td><td>Phoenix</td></tr></tbody></table>

With libretro: virtualjaguar, the **EMULATION > START ORIGINAL BIOS** option shows the console boot screen, which some games require. No file needs to be added: the BIOS is included in the core.

## Which game format?

<table><thead><tr><th width="195.25">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.j64, .jag, .rom, .bin</strong></td><td>Cartridge dumps, the usual format.</td></tr><tr><td>.abs, .cof, .prg</td><td>Homebrew programs.</td></tr><tr><td>.zip, .7z</td><td>The compressed game, accepted by all emulators.</td></tr><tr><td>.squashfs</td><td>BigPEmu only.</td></tr><tr><td>.cue, .cdi</td><td>Jaguar CD games: rather put them in <code>roms\jaguarcd</code> (see the <a href="jaguarcd.md"><strong>Jaguar CD</strong></a> page).</td></tr></tbody></table>

## Controls

### Automatic configuration

RetroBat automatically configures the controllers for all emulators. The three action buttons are in the same place everywhere; the keypad depends on the emulator.

| Jaguar controller | libretro: virtualjaguar, BizHawk | libretro with **MAP JAGUAR PRO CONTROLLER** | BigPEmu           |
| ----------------- | -------------------------------- | ------------------------------------------- | ----------------- |
| A                 | EAST                             | EAST                                        | EAST              |
| B                 | SOUTH                            | SOUTH                                       | SOUTH             |
| C                 | WEST                             | WEST                                        | WEST              |
| Pause             | SELECT                           | SELECT                                      | SELECT            |
| Option            | START                            | START                                       | START             |
| 0                 | NORTH                            | Right stick down                            | Right stick down  |
| 1                 | L1                               | Left stick left                             | L1                |
| 2                 | R1                               | Left stick up                               | Left stick up     |
| 3                 | L2                               | Left stick right                            | R1                |
| 4                 | R2                               | L2                                          | Left stick left   |
| 5                 | L3                               | Right stick up                              | Right stick up    |
| 6                 | R3                               | R2                                          | Left stick right  |
| 7                 | —                                | L1                                          | Right stick left  |
| 8                 | —                                | NORTH                                       | Left stick down   |
| 9                 | —                                | R1                                          | Right stick right |
| \*                | —                                | L3                                          | L3                |
| #                 | —                                | R3                                          | R3                |

| Libretro : VirtualJaguar                         | BigPEmu                                          |
| ------------------------------------------------ | ------------------------------------------------ |
| ![](<../../../../.gitbook/assets/image (1).png>) | ![](<../../../../.gitbook/assets/image (2).png>) |

On the Jaguar Pro controller, the X, Y, Z, L and R buttons duplicate keys 7, 8, 9, 4 and 6: the **MAP JAGUAR PRO CONTROLLER** option therefore puts them on L1, NORTH, R1, L2 and R2.

Useful options, in **CONTROLS**:

<table><thead><tr><th width="212">Option</th><th width="133.25">Emulator</th><th>Effect</th></tr></thead><tbody><tr><td><strong>PLAYER 1</strong> / <strong>2 CONTROLLER TYPE</strong></td><td>libretro: virtualjaguar</td><td>Team Tap (3 or 4 players), rotary controller with the mouse (Tempest 2000), mouse, analog stick (BattleSphere).</td></tr><tr><td><strong>ENABLE MULTITAP</strong></td><td>BigPEmu</td><td>Team Tap in port 1, port 2 or both: up to 5 or 8 controllers.</td></tr><tr><td><strong>USE LEFT STICK</strong></td><td>BigPEmu</td><td>The left stick replaces the D-pad.</td></tr></tbody></table>

### Hotkeys

With BigPEmu, hotkeys use **L2** instead of the HOTKEY button, except for quitting.

Libretro : virtualjaguar uses [standard RetroArch hotkeys](../../../../navigation/hotkeys.md).

| Action               | BigPEmu        | BizHawk            | Keyboard (BigPEmu, BizHawk) |
| -------------------- | -------------- | ------------------ | --------------------------- |
| **Quit**             | HOTKEY + START | HOTKEY + START     | ESC (BizHawk)               |
| Save state           | L2 + WEST      | HOTKEY + WEST      | F2                          |
| Load state           | L2 + NORTH     | HOTKEY + NORTH     | F4                          |
| Next / previous slot | —              | HOTKEY + UP / DOWN | F7 / F6 (BizHawk)           |
| Screenshot           | L2 + R3        | HOTKEY + R3        | F8                          |
| Rewind               | L2 + LEFT      | HOTKEY + LEFT      | BACKSPACE                   |
| Fast forward         | L2 + RIGHT     | HOTKEY + RIGHT     | L                           |
| Emulator menu        | L2 + SOUTH     | —                  | F1 (BigPEmu)                |
| Pause                | —              | HOTKEY + SOUTH     | P (BizHawk)                 |
| Fullscreen           | —              | HOTKEY + L3        | F (BizHawk)                 |

Phoenix only has one hotkey: **HOTKEY + START** to quit.

## Folders

<table><thead><tr><th width="310.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>BIOS (Phoenix)</td><td><code>bios</code></td></tr><tr><td>Saves of the libretro cores</td><td><code>saves\jaguar</code></td></tr><tr><td>BizHawk saves</td><td><code>saves\jaguar\bizhawk</code></td></tr><tr><td>Save states of the libretro cores</td><td><code>saves\jaguar\libretro.virtualjaguar</code></td></tr><tr><td>Save states of BigPEmu</td><td><code>saves\jaguar\bigpemu</code></td></tr><tr><td>Save states of BizHawk</td><td><code>saves\jaguar\bizhawk\sstates\Jaguar</code></td></tr><tr><td>BigPEmu configuration and data</td><td><code>emulators\bigpemu\userdata</code></td></tr><tr><td>Phoenix configuration</td><td><code>emulators\phoenix\phoenix.config.xml</code></td></tr><tr><td>Screenshots of the libretro cores</td><td><code>screenshots</code></td></tr><tr><td>BizHawk screenshots</td><td><code>screenshots\bizhawk\jaguar</code></td></tr><tr><td>Cheats of the libretro cores</td><td><code>cheats\retroarch</code></td></tr><tr><td>BizHawk cheats</td><td><code>cheats\bizhawk\jaguar</code></td></tr></tbody></table>

## Guides

### Playing with 3 or 4 players using the Team Tap

A few games accept more than two players through the Team Tap adapter, for example White Men Can't Jump and NBA Jam Tournament Edition.

* **libretro: virtualjaguar**: set **CONTROLS > PLAYER 1 CONTROLLER TYPE** to **TEAM TAP**.
* **BigPEmu**: set **CONTROLS > ENABLE MULTITAP** to **IN PORT 1**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure></div>

### Tempest 2000 with the rotary controller

Tempest 2000 plays best with a rotary controller. With libretro: virtualjaguar, set **PLAYER 1 CONTROLLER TYPE** to **ROTARY (MOUSE)**: the mouse spins the ship.

### Configuring BigPEmu directly

To reach the settings RetroBat does not offer, open BigPEmu from the **RetroBat** system of the system list, or run `emulators\bigpemu\Configure BigPEmu.bat`. Video settings and controllers are rewritten by RetroBat each time a game is launched.

In game, **L2 + SOUTH** opens the BigPEmu menu.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure></div>

### BigPEmu video effects

The **VISUAL RENDERING > EFFECT** option applies one of the filters built into BigPEmu (scanlines, CRT…). It only works when no RetroBat shader is selected.

To disable RetroBat shaders for this system, see the [**Configuration of systems and games**](../../../../navigation/configuration-of-systems-and-games.md) page.

## Known issues

<table><thead><tr><th width="321.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Phoenix does not launch the game</td><td>Put <code>[BIOS] Atari Jaguar (World).j64</code> in <code>bios</code>.</td></tr><tr><td>A game is slow or glitchy with libretro: virtualjaguar</td><td>Try BigPEmu. On a modest PC, the <strong>FAST BLITTER</strong> option speeds up the core, at the cost of lower compatibility.</td></tr><tr><td>Hotkeys do not respond with BigPEmu</td><td>They use <strong>L2</strong>, not the HOTKEY button. A controller without an L2 trigger therefore has no hotkeys.</td></tr><tr><td>A game needs keys 7, 8 or 9</td><td>With libretro: virtualjaguar, turn on <strong>MAP JAGUAR PRO CONTROLLER</strong>, or use BigPEmu, which puts the whole keypad on the controller.</td></tr><tr><td>A <code>.squashfs</code> file does not launch</td><td>This format is only read by BigPEmu.</td></tr><tr><td>A game made for Europe does not run at the right speed</td><td>Turn on <strong>PAL MODE</strong> (libretro: virtualjaguar, BigPEmu) or <strong>FORCE PAL</strong> (BizHawk).</td></tr><tr><td><strong>EFFECT</strong> changes nothing in BigPEmu</td><td>Disable RetroBat shaders for this system.</td></tr></tbody></table>
