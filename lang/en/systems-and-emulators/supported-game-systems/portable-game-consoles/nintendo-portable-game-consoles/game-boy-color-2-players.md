---
description: Nintendo
---

# Game Boy Color 2 players

<div align="left"><figure><img src="../../../../.gitbook/assets/image (758).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Game Boy Color 2 Players** system links two Game Boy Colors over the Game Link cable, as [**Game Boy 2 Players**](game-boy-2-players.md) does for Game Boy games: RetroBat starts two linked consoles and shows them side by side. It is mostly used to trade and battle in Pokémon Gold, Silver and Crystal, or to play Mario Tennis, Super Mario Bros. Deluxe… together.

How it works, the options and `.m3u` files are described on the [**Game Boy 2 Players**](game-boy-2-players.md) page, the controls on the [**Game Boy**](game-boy.md) page.

{% embed url="https://en.wikipedia.org/wiki/List_of_multiplayer_Game_Boy_games" %}

## At a glance

<table><thead><tr><th width="195.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gbc2players</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gbc .zip .m3u .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: tgbdual</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (controller 1: left console, controller 2: right console)</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                        | For whom?       | Strengths                                                             | Limits |
| ------------------------------- | --------------- | --------------------------------------------------------------------- | ------ |
| **libretro: tgbdual** (default) | Everyone        | Light, made for two-player games, two different games with an `.m3u`. | —      |
| **libretro: sameboy**           | Purists         | Very accurate emulation, choice of color correction and sound output. | —      |
| **libretro: DoubleCherryGB**    | Multiplayer     | Up to **4 linked consoles**, several cable and adapter types.         | —      |
| **libretro: gearboy**           | Curious players | Recent emulator, choice of sound output (one console or both).        | —      |

**If in doubt, keep libretro: tgbdual.**

## BIOS

No file is needed.

## Which game format?

<table><thead><tr><th width="146.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gbc</strong></td><td>Game Boy Color cartridge image: both consoles use the same game.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive): both consoles use the same game.</td></tr><tr><td><strong>.m3u</strong></td><td>List of two games: a different game in each console (see <a href="game-boy-2-players.md#two-different-games-pokemon"><strong>Two different games (Pokémon)</strong></a> on the <strong>Game Boy 2 Players</strong> page).</td></tr></tbody></table>

Example, file `Pokemon Gold + Silver.m3u` in `roms\gbc2players`:

```
Pokemon - Gold Version (USA, Europe).gbc
Pokemon - Silver Version (USA, Europe).gbc
```

## Controls

RetroBat sets up the controllers automatically: the first controller plays on the left console (player 1), the second on the right one (player 2). The buttons and options are the same as on the [**Game Boy**](game-boy.md#controls) page.

## Folders

<table><thead><tr><th width="219">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game saves</td><td><code>saves\gbc2players</code></td></tr><tr><td>Save states</td><td><p><code>saves\gbc2players\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\gbc2players\libretro.tgbdual</code>)</p></td></tr></tbody></table>

## Guides

### Game Boy Color specific options

The screen layout, sound and DoubleCherryGB options are those of the [**Game Boy 2 Players**](game-boy-2-players.md) page. Only one changes:

<table><thead><tr><th width="162">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>sameboy core</td><td><strong>VISUAL RENDERING > COLOR CORRECTION MODE</strong></td><td>Replaces <strong>PALETTE</strong>: corrects the bright Game Boy Color colors (<strong>MODERN BALANCED</strong> by default).</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="279">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The <code>.m3u</code> does not start</td><td>Check that both games are in <code>roms\gbc2players</code> and that the names in the <code>.m3u</code> are exact (extension included).</td></tr><tr><td>A Game Boy game does not start</td><td>Put it in <code>roms\gb2players</code>.</td></tr></tbody></table>
