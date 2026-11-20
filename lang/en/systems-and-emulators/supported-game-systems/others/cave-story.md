---
description: Studio Pixel
---

# Cave Story

<div align="left"><figure><img src="../../../.gitbook/assets/image (651).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

**Cave Story** (Studio Pixel, 2004) is a 2D action and exploration game, created alone by Daisuke Amaya. The original game is free.

RetroBat runs it with two libretro cores: **nxengine** (default) and **doukutsu\_rs**.

{% embed url="https://en.wikipedia.org/wiki/Cave_Story" %}

## At a glance

<table><thead><tr><th width="232.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\cavestory</code></td></tr><tr><td><strong>Extensions</strong></td><td>.libretro .exe</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: nxengine</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

| Emulator                         | Strengths                                                | Limitations         |
| -------------------------------- | -------------------------------------------------------- | ------------------- |
| **libretro: nxengine** (default) | Reference engine for the original game.                  | Original game only. |
| **libretro: doukutsu\_rs**       | Modern engine: widescreen, internal resolution up to x4. |                     |

## Install the game

Download the game from the RetroBat [**CONTENT DOWNLOADER**](../../../advanced-features/updates-and-content-download.md#content-downloader) menu, or from the website:

{% embed url="https://www.cavestory.org/download/cave-story.php" %}

Direct download of the English version: [cavestoryen.zip](http://www.cavestory.org/downloads/cavestoryen.zip).

Two ways to start the game:

| Launched file                                    | Effect                                                                                                           |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| `Doukutsu.exe` in `roms\cavestory\<game folder>` | The selected core runs the game of this folder.                                                                  |
| `nxengine.libretro` in `roms\cavestory`          | The nxengine core is started without a file: it runs the game of `bios\nxengine` (`bios\nxengine\Doukutsu.exe`). |

## Controls

Default RetroArch controls.

### Hotkeys

RetroArch hotkeys. See the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="189">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game</td><td><code>roms\cavestory\&#x3C;game folder></code> or <code>bios\nxengine</code></td></tr><tr><td>Saves</td><td><code>saves\cavestory</code></td></tr></tbody></table>
