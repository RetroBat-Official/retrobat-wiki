---
description: Nintendo
---

# Game Boy Advance 2 players

## Overview

The Game Boy Advance **Game Link cable** connects up to four consoles. It is used to play together (Mario Kart: Super Circuit, The Legend of Zelda: Four Swords, Bomberman Tournament…) and to trade or battle in the Game Boy Advance Pokémon games.

The **Game Boy Advance 2 Players** system recreates this connection: RetroBat starts 2 to 4 linked consoles and shows them together on the same screen. Each player plays with their own controller, in player order. The consoles can use the same game or different games (Pokémon Ruby and Sapphire).

Games, buttons and picture options are those of the [**Game Boy Advance**](game-boy-advance.md) page.

{% embed url="https://en.wikipedia.org/wiki/List_of_Game_Boy_Advance_games" %}

## At a glance

<table><thead><tr><th width="229"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gba2players</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gba .zip .7z .m3u</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mgba_splitscreen</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>gba_bios.bin</code> optional)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic with mgba_splitscreen (controller 1: player 1…), to do in NO$GBA</td></tr><tr><td><strong>Save states</strong></td><td>libretro core; NO$GBA from its menu</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="172.75">Emulator</th><th width="144">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: mgba_splitscreen</strong> (default)</td><td>Everyone</td><td>2 to 4 linked mGBA consoles, different games with an <code>.m3u</code>, several screen layouts, Four Swords assist.</td><td>No RetroAchievements.</td></tr><tr><td><strong>nosgba</strong></td><td>Curious players</td><td>NO$GBA, 2 to 4 linked consoles.</td><td>Controllers to set up in NO$GBA. One game at a time (no <code>.m3u</code>).</td></tr></tbody></table>

**If in doubt, keep libretro: mgba\_splitscreen.**

## BIOS

No file is needed. `gba_bios.bin` (see the [**Game Boy Advance**](game-boy-advance.md#bios) page) is used by mgba\_splitscreen when present.

## Which game format?

<table><thead><tr><th width="125.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gba</strong></td><td>Game Boy Advance cartridge image: all consoles use the same game.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive): all consoles use the same game.</td></tr><tr><td><strong>.m3u</strong></td><td>List of 2 to 4 games: a different game in each console (see <a href="game-boy-advance-2-players.md#different-games-pokemon"><strong>Different games (Pokémon)</strong></a>). mgba_splitscreen only.</td></tr></tbody></table>

## Controls

With mgba\_splitscreen, RetroBat sets up the controllers automatically: the first controller plays on player 1's console, the second on player 2's, and so on. The buttons and the **INVERT FACE BUTTONS** option are the same as on the [**Game Boy Advance**](game-boy-advance.md#controls) page.

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gba_turbo.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

With NO$GBA, RetroBat does not set up the controllers: set them in the NO$GBA options. HOTKEY + START (or `Esc`) exits it.

mgba\_splitscreen hotkeys are the RetroArch ones (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="276.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game saves</td><td><code>saves\gba2players</code></td></tr><tr><td>mgba_splitscreen: save states</td><td><code>saves\gba2players\libretro.mgba_splitscreen</code></td></tr><tr><td>NO$GBA: save states</td><td><code>saves\gba2players\nosgba\sstates</code></td></tr></tbody></table>

## Guides

### Number of players and screen layout

| Emulator               | Option                                              | Effect                                                                                                                                                                                                         |
| ---------------------- | --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| mgba\_splitscreen core | **EMULATION > NUMBER OF PLAYERS**                   | Number of consoles running the same game: 2 (default), 3 or 4. With an `.m3u`, one console per game.                                                                                                           |
| mgba\_splitscreen core | **VIDEO > VIEW LAYOUT**                             | **SIDE BY SIDE (2x1)**, **STACKED (1x2)**, **QUADRANTS (2x2)**, **SPEAKER (BIG+STRIP)**, **FOCUS (SINGLE SCREEN)** or **OVERLAY (BIG+THUMBNAILS)**. By default, side by side with 2 players, quadrants with 4. |
| mgba\_splitscreen core | **EMULATION > FOCUSED PLAYER**                      | Console enlarged in the speaker, focus and overlay views.                                                                                                                                                      |
| mgba\_splitscreen core | **VIDEO > PLAYER OUTLINES AND BADGES**              | Colored frame and number on each player's screen (enabled by default).                                                                                                                                         |
| mgba\_splitscreen core | **AUDIO > AUDIO SOURCE**                            | Sound of player 1 (default), of another player, or **MIXED** from all consoles.                                                                                                                                |
| mgba\_splitscreen core | **AUDIO > AUDIO FILTER**, **AUDIO > AUDIO LIMITER** | Softens the sound and prevents saturation when the sound of several consoles is mixed (enabled by default).                                                                                                    |
| NO$GBA                 | **EMULATION > NUMBER OF PLAYERS**                   | 2 (default), 3 or 4 consoles.                                                                                                                                                                                  |

### Different games (Pokémon)

To trade or battle between two Pokémon versions, each console needs its own game. Create an `.m3u` file in `roms\gba2players`, with the names of the games, one per line. The first game goes in player 1's console, the second in player 2's, and so on (4 games max).

Example, file `Pokemon Ruby + Sapphire.m3u`:

```
Pokemon - Ruby Version (USA, Europe).gba
Pokemon - Sapphire Version (USA, Europe).gba
```

The games must be in `roms\gba2players`, next to the `.m3u`. Each player keeps the save of their game.

Three or four games are mostly used by the Game Boy Advance Pokémon games: 4-player Multi Battles (2 vs 2), Berry Blender (Ruby, Sapphire, Emerald), trades between different versions.

### The Legend of Zelda: Four Swords

The Four Swords link sometimes fails when the game starts. Enable **EMULATION > FOUR SWORDS LINK ASSIST** (mgba\_splitscreen core) to help it.

## Known issues

<table><thead><tr><th width="350.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The <code>.m3u</code> does not start</td><td>Check that the games are in <code>roms\gba2players</code> and that the names in the <code>.m3u</code> are exact (extension included). The <code>.m3u</code> is not read by NO$GBA.</td></tr><tr><td>A player does not respond</td><td>Connect all controllers before starting the game (mgba_splitscreen); with NO$GBA, set up the controllers in its options.</td></tr><tr><td>Four Swords does not find the other players</td><td>See <a href="game-boy-advance-2-players.md#the-legend-of-zelda-four-swords"><strong>The Legend of Zelda: Four Swords</strong></a>.</td></tr><tr><td>I want to play alone</td><td>This system is for multiplayer only: put the game in <code>roms\gba</code>.</td></tr></tbody></table>
