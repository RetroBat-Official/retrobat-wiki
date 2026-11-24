---
description: Diablo
---

# DevilutionX

<div align="left"><figure><img src="../../../.gitbook/assets/image (731).png" alt="" width="416"><figcaption></figcaption></figure></div>

## Overview

**Diablo** (Blizzard, 1996) is an action role-playing game that started the "hack and slash" genre. Its **Hellfire** add-on (Sierra, 1997) adds a character, quests and two areas.

RetroBat uses **DevilutionX**, a port of the original game: high resolution, widescreen, controller play, quality of life improvements.

The game files are not provided: use the ones from your own copy (CD, [GOG](https://www.gog.com/game/diablo), [Battle.net](https://eu.shop.battle.net/fr-fr/family/diablo)) or the [demo](http://ftp.blizzard.com/pub/demos/diablosw.exe).

{% embed url="https://github.com/diasurgical/devilutionX" %}

## At a glance

<table><thead><tr><th width="237.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\devilutionx</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game .win</td></tr><tr><td><strong>Default emulator</strong></td><td>devilutionx</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (DevilutionX controls)</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves, quick save / load with the controller</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## BIOS

No BIOS is needed. You need the game files:

<table><thead><tr><th width="217.75">Game</th><th>Files</th></tr></thead><tbody><tr><td>Diablo</td><td><code>diabdat.mpq</code></td></tr><tr><td>Diablo (demo)</td><td><code>spawn.mpq</code></td></tr><tr><td>Hellfire</td><td><code>hellfire.mpq</code>, <code>hfmonk.mpq</code>, <code>hfmusic.mpq</code>, <code>hfvoice.mpq</code> (with <code>diabdat.mpq</code>)</td></tr></tbody></table>

## Which game format?

Each game is a `.game` folder of `roms\devilutionx` holding its `.mpq` files.

With Diablo and Hellfire in the same folder, Diablo is started, unless the folder name contains "hellfire". **GAME** selects DIABLO or HELLFIRE.

## Controls

### Automatic configuration

DevilutionX recognizes the controller and its default controls. All connected controllers move the hero: **CONTROLS > PLAYER 1 CONTROLLER ONLY** limits them to the player 1 one (for example if another controller drifts).

### Hotkeys

<table><thead><tr><th width="264">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr><tr><td>SELECT + L3</td><td>Quick save</td></tr><tr><td>START + L3</td><td>Quick load</td></tr><tr><td>START + R3</td><td>Screenshot</td></tr></tbody></table>

The controller shortcuts can be disabled with **CONTROLS > GAMEPAD SHORTCUTS**.

## Folders

<table><thead><tr><th width="166.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\devilutionx\&#x3C;game>.game</code></td></tr><tr><td>Saves</td><td><code>saves\devilutionx\&#x3C;game></code></td></tr><tr><td>Configuration</td><td><code>roms\devilutionx\&#x3C;game>.game\diablo.ini</code></td></tr></tbody></table>

## Guides

### File layout

In `roms\devilutionx`, create a `diablo.game` folder:

Copy into it the `diabdat.mpq` file of your CD or install folder (or extract it from the GOG installer):

{% embed url="https://github.com/diasurgical/devilutionX/wiki/Extracting-the-.MPQs-from-the-GoG-installer" %}

For Hellfire, also copy `hellfire.mpq`, `hfmonk.mpq`, `hfmusic.mpq` and `hfvoice.mpq`:

<div align="left"><figure><img src="../../../.gitbook/assets/image (732).png" alt=""><figcaption></figcaption></figure></div>

The demo is started with `spawn.mpq` instead of `diabdat.mpq`:

{% embed url="https://github.com/diasurgical/devilutionx-assets/releases/latest/download/spawn.mpq" %}

### Options

* **INTERNAL GAME RESOLUTION** up to 1280x960, **WIDESCREEN** to fill widescreen displays.
* **EMULATION > RUN IN TOWN**, **AUTO GOLD PICKUP**, **AUTO REFILL BELT**.
* **USER INTERFACE > EXPERIENCE BAR**, **ENEMY HEALTH BAR**, **ITEM LABELS**.

### Mods

DevilutionX mods are listed on the project wiki:

{% embed url="https://github.com/diasurgical/devilutionX/wiki/Mods-and-related-projects" %}

## Known issues

<table><thead><tr><th width="340.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The hero moves on its own</td><td>Another controller drifts: enable <strong>PLAYER 1 CONTROLLER ONLY</strong>, or increase <strong>STICK DEADZONE</strong>.</td></tr><tr><td>The game asks to choose between Diablo and Hellfire</td><td>Set <strong>GAME</strong>.</td></tr></tbody></table>
