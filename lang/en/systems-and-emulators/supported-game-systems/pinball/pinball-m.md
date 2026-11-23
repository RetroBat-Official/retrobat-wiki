---
description: Zen Studios
---

# Pinball FX Midnight

<div align="left"><figure><img src="../../../.gitbook/assets/image (716).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**Pinball FX Midnight**, called **Pinball M** until March 2026, is the **Zen Studios** pinball platform for horror tables, released at the end of 2023. Like Pinball FX, the game is free and tables are bought separately; Wrath of the Elder Gods is free.

RetroBat starts a table directly, in the chosen game mode.

{% embed url="https://zenstudios.com/games/pinball-m/" %}

## At a glance

<table><thead><tr><th width="231.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\pinballm</code></td></tr><tr><td><strong>Extensions</strong></td><td>.table</td></tr><tr><td><strong>Default emulator</strong></td><td>pinballfx (steam version)</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>By the game (not changed by RetroBat)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator to choose?

The `pinballfx` emulator has two versions (core):

<table><thead><tr><th width="149.5">Version</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>steam</strong> (default)</td><td>The game installed with Steam is started by Steam, directly on the chosen table.</td><td>Steam must be installed, with the game.</td></tr><tr><td><strong>nonsteam</strong></td><td>Starts the game executable directly, without Steam.</td><td>The game must be in <code>emulators\pinballm</code>.</td></tr></tbody></table>

With **nonsteam**, RetroBat looks for `Pinball FX Midnight.exe`, `Pinball M.exe` or `PinballM.exe` in the `emulators\pinballm` folder. If the game is not there, a message gives the expected folder.

## BIOS

No BIOS needed.

## Add tables

Each table is a small `.table` text file that contains the **table number**:

1. In `roms\pinballm`, create a text file, for example `The Thing.txt`.
2. Write the table number on the first line (175 for The Thing).
3. Save, then change the `.txt` extension to `.table`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (717).png" alt=""><figcaption></figcaption></figure></div>

See the example on the [Pinball FX](pinball-fx.md) page.

{% hint style="warning" %}
Only the tables you own start from RetroBat (in addition to the free table).
{% endhint %}

<details>

<summary>Table numbers</summary>

| No. | Table                                    |
| --- | ---------------------------------------- |
| 90  | Fallout™ Pinball                         |
| 91  | The Elder Scrolls V: Skyrim™ Pinball     |
| 92  | DOOM™ Pinball                            |
| 147 | Wrath of the Elder Gods (Director's Cut) |
| 171 | Chucky's Killer Pinball                  |
| 174 | Dead by Daylight™ Pinball                |
| 175 | The Thing Pinball                        |
| 176 | Duke Nukem's Big Shot Pinball            |
| 180 | Texas Chainsaw Massacre Pinball          |
| 183 | System Shock Pinball                     |
| 191 | Camp Bloodbrook                          |

</details>

## Controls

The game handles the controller itself (XInput controller recommended): RetroBat does not change its configuration. Controls are changed in the game options.

<table><thead><tr><th width="259">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Left flipper</td><td>L1 or L2</td></tr><tr><td>Right flipper</td><td>R1 or R2</td></tr><tr><td>Launch the ball</td><td>Right stick down (pull, then release)</td></tr><tr><td>Auto launch the ball</td><td>SOUTH</td></tr><tr><td>Backbox view</td><td>Right stick up</td></tr><tr><td>Nudge the table</td><td>Left stick</td></tr><tr><td>Visual extras</td><td>EAST</td></tr><tr><td>Wizard power</td><td>WEST</td></tr><tr><td>Change view</td><td>NORTH</td></tr><tr><td>Menu</td><td>START or SELECT</td></tr></tbody></table>

## Hotkeys

<table><thead><tr><th width="242.75">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Quit the game</td><td>HOTKEY + START</td></tr></tbody></table>

The Game Control Center is not available for these systems.

## Useful options

In the advanced system or game settings:

* **GAME OPTIONS > GAME MODE**: mode started with the table. When not set, the game keeps the mode chosen in its menu.

<table><thead><tr><th width="245.25">Choice</th><th>Game mode</th></tr></thead><tbody><tr><td>Classic</td><td>Classic game (<code>Classic</code>)</td></tr><tr><td>Pro</td><td>Pro mode (<code>Pro</code>)</td></tr><tr><td>Practice</td><td>Practice (<code>Practice</code>)</td></tr><tr><td>Hotseat 2 / 3 / 4 Players</td><td>Multiplayer, taking turns (<code>Hotseat_2</code> to <code>Hotseat_4</code>)</td></tr><tr><td>1 ball challenge</td><td>One ball only (<code>Challenge_BallLimited</code>)</td></tr><tr><td>5 minute time challenge</td><td>Game limited to 5 minutes (<code>Challenge_TimeLimited</code>)</td></tr><tr><td>Distance challenge</td><td>Distance challenge (<code>Challenge_DistanceLimited</code>)</td></tr><tr><td>Flips challenge</td><td>Limited number of flips (<code>Challenge_FlipLimited</code>)</td></tr></tbody></table>

* **VIDEO > VIDEO MODE**: Windows resolution during the game.
* **EMULATION > KILL LAUNCHER WHEN EXIT**: closes Steam when quitting the game (steam version).

A mode that does not exist for the table is ignored: the table starts with its default settings.

## Folders

<table><thead><tr><th width="257.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Tables</td><td><code>roms\pinballm</code></td></tr><tr><td>Game (nonsteam version)</td><td><code>emulators\pinballm</code></td></tr><tr><td>Saves, scores, settings</td><td>Handled by the game (and by Steam)</td></tr></tbody></table>

## Known issues

* **The game opens without starting the table**: you do not own the table, or its number is wrong.
* **"'….table' must contain the table number on its first line."**: the `.table` file is empty or does not contain a number.
* **"Game not found: copy it in '…'"** (nonsteam version): the game is not in the given folder, or its executable has another name.
* **"Steam is not installed."** (steam version): Steam was not found.
