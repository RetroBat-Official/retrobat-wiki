---
description: Nintendo
---

# Game Boy 2 players

<div align="left"><figure><img src="../../../../.gitbook/assets/image (750).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Game Link cable** connects two Game Boys: each player has their own console and cartridge. It is used to play together (Tetris, Dr. Mario, F-1 Race…) or to trade and battle in Pokémon Red, Blue and Yellow.

The **Game Boy 2 Players** system recreates this connection: RetroBat starts two linked Game Boys and shows them side by side on the same screen. Player 1 plays on the left console with the first controller, player 2 on the right one with the second. Both consoles can use the same game or two different games (Pokémon Red and Blue).

Games, controls and hotkeys are those of the [**Game Boy**](game-boy.md) page.

{% embed url="https://en.wikipedia.org/wiki/List_of_multiplayer_Game_Boy_games" %}

## At a glance

<table><thead><tr><th width="197.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gb2players</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gb .zip .m3u .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: tgbdual</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (controller 1: left console, controller 2: right console)</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                        | For whom?       | Strengths                                                             | Limits |
| ------------------------------- | --------------- | --------------------------------------------------------------------- | ------ |
| **libretro: tgbdual** (default) | Everyone        | Light, made for two-player games, two different games with an `.m3u`. | —      |
| **libretro: sameboy**           | Purists         | Very accurate emulation, choice of palette and sound output.          | —      |
| **libretro: DoubleCherryGB**    | Multiplayer     | Up to **4 linked consoles**, several cable and adapter types.         | —      |
| **libretro: gearboy**           | Curious players | Recent emulator, choice of sound output (one console or both).        | —      |

**If in doubt, keep libretro: tgbdual.**

## BIOS

No file is needed.

## Which game format?

<table><thead><tr><th width="144">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gb</strong></td><td>Game Boy cartridge image: both consoles use the same game.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive): both consoles use the same game.</td></tr><tr><td><strong>.m3u</strong></td><td>List of two games: a different game in each console (see <a href="game-boy-2-players.md#two-different-games-pokemon"><strong>Two different games (Pokémon)</strong></a>).</td></tr></tbody></table>

## Controls

RetroBat sets up the controllers automatically: the first controller plays on the left console (player 1), the second on the right one (player 2). The buttons and the **INVERT FACE BUTTONS** and **REMAP SELECT TO** options are the same as on the [**Game Boy**](game-boy.md) page.

Hotkeys are the RetroArch ones (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="181.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game saves</td><td><code>saves\gb2players</code></td></tr><tr><td>Save states</td><td><p><code>saves\gb2players\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\gb2players\libretro.tgbdual</code>)</p></td></tr></tbody></table>

## Guides

### Two different games (Pokémon)

To trade or battle between Pokémon Red and Pokémon Blue, each console needs a different game. Create an `.m3u` file in `roms\gb2players`, with the names of both games, one per line. The first game goes in player 1's console, the second in player 2's.

Example, file `Pokemon Red + Blue.m3u`:

```
Pokemon - Red Version (USA, Europe).gb
Pokemon - Blue Version (USA, Europe).gb
```

<div align="left"><figure><img src="../../../../.gitbook/assets/image (751).png" alt=""><figcaption></figcaption></figure></div>

Both games must be in `roms\gb2players`, next to the `.m3u`. All four emulators accept `.m3u` files.

### Screen layout and sound

| Emulator                                 | Option                                | Effect                                                              |
| ---------------------------------------- | ------------------------------------- | ------------------------------------------------------------------- |
| tgbdual core, sameboy core, gearboy core | **VIDEO > SCREEN LAYOUT POSITIONING** | **SIDE BY SIDE** (default) or **TOP / BOTTOM**.                     |
| DoubleCherryGB core                      | **VIDEO > SCREEN LAYOUT POSITIONING** | **SPLIT SCREEN** (default), **TOP TO BOTTOM** or **LEFT TO RIGHT**. |
| sameboy core, DoubleCherryGB core        | **AUDIO > AUDIO OUTPUT**              | Sound of console 1 (default) or of another console.                 |
| gearboy core                             | **AUDIO > AUDIO OUTPUT**              | Sound of console 1 (default), console 2 or a **MIX** of both.       |
| sameboy core                             | **VISUAL RENDERING > PALETTE**        | Greyscale (default), lime, olive or teal.                           |

### Playing with 3 or 4 (DoubleCherryGB)

A few games are played by four with Nintendo's 4 player adapter (F-1 Race, Wave Race…) or with a ring cable (Faceball 2000). With the DoubleCherryGB core:

1. Choose the number of consoles in **EMULATION > NUMBER OF PLAYERS** (2 by default, up to 4).
2. Choose the connection in **EMULATION > LINK CABLE DEVICE**: **2 PLAYER LINK CABLE**, **4 PLAYER ADAPTER**, **FACEBALL 2000 RING CABLE**, or the adapters of the Tetris and Kwirk multiplayer hacks. By default, the core chooses by itself.

Each console gets a controller, in player order.

## Known issues

<table><thead><tr><th width="317.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The <code>.m3u</code> does not start</td><td>Check that both games are in <code>roms\gb2players</code> and that the names in the <code>.m3u</code> are exact (extension included).</td></tr><tr><td>Only one player responds</td><td>Connect a second controller before starting the game.</td></tr><tr><td><strong>GRID</strong> has no effect (DoubleCherryGB)</td><td>This choice does not exist in the current version of the core: use <strong>SPLIT SCREEN</strong>.</td></tr><tr><td>A Game Boy Color game does not start</td><td>Put it in <code>roms\gbc2players</code>.</td></tr></tbody></table>
