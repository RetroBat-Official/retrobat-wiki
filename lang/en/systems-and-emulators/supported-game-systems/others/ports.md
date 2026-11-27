# Ports

<div align="left"><figure><img src="../../../.gitbook/assets/image (773).png" alt=""><figcaption></figcaption></figure></div>

## Overview

Some libretro cores are not emulators but **complete games** that run in RetroArch. The **Ports** system groups them. RetroBat provides six of these games, ready to play:

<table><thead><tr><th width="119.5">Game</th><th width="197.75">File</th><th>Genre</th></tr></thead><tbody><tr><td><strong>2048</strong></td><td><code>2048.libretro</code></td><td>Puzzle: slide the tiles to reach 2048.</td></tr><tr><td><strong>Anarch</strong></td><td><code>anarch.libretro</code></td><td>First-person shooter, in 90s style.</td></tr><tr><td><strong>Craft</strong></td><td><code>craft.libretro</code></td><td>Block building, inspired by Minecraft.</td></tr><tr><td><strong>Gong</strong></td><td><code>gong.libretro</code></td><td>Pong, against the computer or with two players.</td></tr><tr><td><strong>Mr. Boom</strong></td><td><code>mrboom.libretro</code></td><td>Bomberman, up to 8 players.</td></tr><tr><td><strong>XRick</strong></td><td><code>xrick.libretro</code></td><td>Free version of Rick Dangerous.</td></tr></tbody></table>

RetroBat's other game ports (Doom, Quake, Cave Story, Sonic…) have their own system and their own page.

## At a glance

<table><thead><tr><th width="211.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\ports</code></td></tr><tr><td><strong>Extensions</strong></td><td>.libretro</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro (the core is named after the file)</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>2048, Gong, Mr. Boom</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

There is nothing to choose: each `<core>.libretro` file starts the libretro core of the same name. `mrboom.libretro` starts the mrboom core, `craft.libretro` the craft core…

## BIOS

No BIOS is needed.

XRick needs its data, `data.zip`, which RetroBat installs in `roms\ports\xrick`.

## Which game format?

The `.libretro` files are empty: only their name matters. RetroBat provides them, with their images and descriptions.

If you delete one of these games by mistake, simply create an empty file named after the core, for example `gong.libretro`, in `roms\ports`.

## Controls

RetroBat sets up controllers automatically.

**2048**

<table><thead><tr><th width="207.75">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>D-pad</td><td>Slide the tiles</td></tr><tr><td>START</td><td>Start</td></tr><tr><td>SELECT</td><td>Pause</td></tr></tbody></table>

**Anarch**

<table><thead><tr><th width="215.25">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>D-pad</td><td>Move</td></tr><tr><td>SOUTH</td><td>Game button B</td></tr><tr><td>EAST</td><td>Game button A</td></tr><tr><td>WEST</td><td>Jump</td></tr><tr><td>NORTH</td><td>Game button C</td></tr><tr><td>L1 / R1</td><td>Previous / next weapon</td></tr><tr><td>START</td><td>Map</td></tr><tr><td>SELECT</td><td>Menu</td></tr></tbody></table>

**Craft**

<table><thead><tr><th width="185.25">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Move</td></tr><tr><td>Right stick</td><td>Aim</td></tr><tr><td>D-pad</td><td>Move forward, backward, aim left or right</td></tr><tr><td>L1 / R1</td><td>Move left / right</td></tr><tr><td>L2 / R2</td><td>Aim up / down</td></tr><tr><td>SOUTH</td><td>Jump</td></tr><tr><td>WEST</td><td>Destroy block</td></tr><tr><td>NORTH</td><td>Place block</td></tr><tr><td>EAST</td><td>Next block</td></tr><tr><td>SELECT</td><td>Zoom out</td></tr></tbody></table>

**Gong**

<table><thead><tr><th width="285.25">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>D-pad (up, down)</td><td>Move the paddle</td></tr><tr><td>SOUTH, EAST, WEST, NORTH</td><td>Speed up the paddle</td></tr></tbody></table>

Player 2 is played by the computer by default. To play with two players, open the RetroArch menu (**HOTKEY + SOUTH**), then **Core Options > Player 2** and select a human player.

**Mr. Boom**

<table><thead><tr><th width="210.25">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>D-pad</td><td>Move, push a bomb</td></tr><tr><td>SOUTH</td><td>Drop a bomb, join the game</td></tr><tr><td>EAST</td><td>Detonate the bomb (with the remote control), join the game</td></tr><tr><td>NORTH</td><td>Jump (on a kangaroo), join the game</td></tr><tr><td>SELECT</td><td>Add a computer player (player selection screen)</td></tr><tr><td>START</td><td>Start the game</td></tr></tbody></table>

Each connected controller can join the game, up to 8 players.

**XRick**

<table><thead><tr><th width="266.5">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>D-pad</td><td>Move, jump (up), crouch (down)</td></tr><tr><td>EAST</td><td>Attack</td></tr><tr><td>EAST + left / right</td><td>Bayonet stab</td></tr><tr><td>EAST + up</td><td>Shoot</td></tr><tr><td>EAST + down</td><td>Drop a bomb</td></tr></tbody></table>

### Hotkeys

The games use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../navigation/hotkeys.md) page).

## Folders

| Content                                     | Folder                        |
| ------------------------------------------- | ----------------------------- |
| Games (`.libretro` files)                   | `roms\ports`                  |
| Game list images                            | `roms\ports\images`           |
| XRick data                                  | `roms\ports\xrick\data.zip`   |
| Saves (2048: games and high scores; Anarch) | `saves\ports`                 |
| Craft world (`craft.db`)                    | `bios`                        |
| Save states                                 | `saves\ports\libretro.<core>` |

## Guides

### Game options

Each game has its own options in the RetroArch menu (**HOTKEY + SOUTH**, then **Core Options**):

* **Mr. Boom**: teams (by color, by sex…), monsters, bomb autofire;
* **Craft**: resolution, field of view, draw distance, inverted aim;
* **Gong**: human or computer player 2.

## Known issues

<table><thead><tr><th width="351.5">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>XRick does not start</td><td>The <code>roms\ports\xrick\data.zip</code> file is missing.</td></tr><tr><td>A game disappeared from the list</td><td>Create the empty <code>&#x3C;core>.libretro</code> file again in <code>roms\ports</code>.</td></tr><tr><td>Craft does not keep the game with save states</td><td>Craft does not support save states: the world is saved automatically in <code>bios\craft.db</code>.</td></tr></tbody></table>
