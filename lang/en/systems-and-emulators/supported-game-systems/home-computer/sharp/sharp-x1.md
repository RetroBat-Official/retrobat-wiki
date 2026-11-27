---
description: Sharp
---

# Sharp X1

<div align="left"><figure><img src="../../../../.gitbook/assets/image (759).png" alt="" width="300"><figcaption></figcaption></figure></div>

## Overview

The **Sharp X1** is a Japanese 8-bit computer released in 1982, built around a Z80 CPU. Its color graphics and redefinable characters (PCG) made it a gaming machine; it was followed by the X1 turbo (1984) and X1 turbo Z (1986). The first Thunder Force (1983) was released on the X1.

{% embed url="https://en.wikipedia.org/wiki/Sharp_X1" %}

## At a glance

<table><thead><tr><th width="212.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\x1</code></td></tr><tr><td><strong>Extensions</strong></td><td>.dx1 .zip .2d .2hd .tfd .d88 .88d .hdm .xdf .dup .cmd .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: x1</td></tr><tr><td><strong>BIOS</strong></td><td><code>IPLROM.X1</code> required</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (player 1)</td></tr><tr><td><strong>Save states</strong></td><td>libretro core</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="114">File</th><th width="207.25">Description</th><th width="111.5">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>IPLROM.X1</code></td><td>X1 boot ROM</td><td><code>bios\xmil</code></td><td>eeeea1cd29c6e0e8b094790ae969bfa7</td></tr><tr><td><code>IPLROM.X1T</code></td><td>X1 turbo boot ROM (<strong>ROM TYPE</strong> TURBO or TURBOZ)</td><td><code>bios\xmil</code></td><td>56c28adcf1f3a2f87cf3d57c378013f5</td></tr></tbody></table>

`IPLROM.X1` is required, `IPLROM.X1T` optional; both are checked by RetroBat.

## Which game format?

| Format                                                                                  | Description        |
| --------------------------------------------------------------------------------------- | ------------------ |
| **.2d**, **.2hd**, **.d88**, **.88d**, **.hdm**, **.xdf**, **.dup**, **.dx1**, **.tfd** | Floppy disk image. |
| **.cmd**                                                                                | Core command file. |
| **.zip**, **.7z**                                                                       | A compressed game. |

## Controls

RetroBat sets up the player 1 controller (a single joystick port):

<table><thead><tr><th width="195.25">RetroBat controller</th><th>X1</th></tr></thead><tbody><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>SOUTH</td><td>Button 1 (main fire)</td></tr><tr><td>EAST</td><td>Button 2</td></tr></tbody></table>

The PC keyboard stays active; many X1 games are played with the keyboard. To put keyboard keys on the controller, see the [**Keyboard / PadToKey**](../../../../controllers/pad2key.md) page.

### Hotkeys

The x1 core uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="202.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game saves</td><td>on the game's floppy disk (file in <code>roms\x1</code>)</td></tr><tr><td>Save states</td><td><code>saves\x1\libretro.x1</code></td></tr><tr><td>BIOS</td><td><code>bios\xmil</code></td></tr></tbody></table>

## Guides

### X1 turbo games

Games made for the X1 turbo need **EMULATION > ROM TYPE > TURBO** (or **TURBOZ**) and the `IPLROM.X1T` BIOS.

## Known issues

<table><thead><tr><th width="334">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Black screen at startup</td><td>Add <code>IPLROM.X1</code> to <code>bios\xmil</code>.</td></tr><tr><td>An X1 turbo game does not start</td><td>Choose <strong>ROM TYPE > TURBO</strong> and add <code>IPLROM.X1T</code> (see <a href="sharp-x1.md#x1-turbo-games"><strong>X1 turbo games</strong></a>).</td></tr><tr><td>The game does not respond to the controller</td><td>It is played with the keyboard: use the PC keyboard or the <strong>Keyboard / PadToKey</strong> page.</td></tr></tbody></table>
