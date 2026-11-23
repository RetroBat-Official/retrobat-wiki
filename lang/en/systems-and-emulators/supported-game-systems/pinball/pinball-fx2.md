---
description: Zen Studios
---

# Pinball FX2

<div align="left"><figure><img src="../../../.gitbook/assets/image (709).png" alt=""><figcaption></figcaption></figure></div>

## Overview

**Pinball FX2** is the **Zen Studios** pinball platform released in 2010 on Xbox 360, then in 2013 on PC. Removed from sale on Steam in 2017, replaced by Pinball FX3, it can still be downloaded by its owners.

{% embed url="https://en.wikipedia.org/wiki/Pinball_FX_2" %}

## At a glance

<table><thead><tr><th width="235.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\pinballfx2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pxp .table</td></tr><tr><td><strong>Default emulator</strong></td><td>pinballfx (steam version)</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>By the game (not changed by RetroBat)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator to choose?

The `pinballfx` emulator has two versions (core):

<table><thead><tr><th width="158.25">Version</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>steam</strong> (default)</td><td>The game installed with Steam is started by Steam, directly on the chosen table.</td><td>Steam must be installed, with the game.</td></tr><tr><td><strong>nonsteam</strong></td><td>Starts the game executable directly, without Steam.</td><td>The game must be in <code>emulators\pinballfx2</code>.</td></tr></tbody></table>

With **nonsteam**, RetroBat looks for `Pinball FX2.exe` in the `emulators\pinballfx2` folder. If the game is not there, a message gives the expected folder.

## BIOS

No BIOS needed.

## Cabinet Mode

To start a table from RetroBat, you need:

* [x] the Pinball FX2 game;
* [x] at least one table you bought;
* [x] **Cabinet Mode** enabled with a Personal Activation Code, requested from Zen Studios.

{% hint style="info" %}
Code request: [Zen Studios form](https://zenstudios.com/home/pinball-cabinet-support-request/). More information about [Cabinet Mode](https://www.pinballfx.com/?page_id=7754#end-anchor).
{% endhint %}

## Add tables

Once Cabinet Mode is enabled, each table is a file placed in `roms\pinballfx2`:

* either the `.pxp` file of the table, copied from the `data_steam` folder of the game;
* or an empty `.table` file named exactly like the table (for example `Citadel.table`).

<div align="left"><figure><img src="../../../.gitbook/assets/image (710).png" alt=""><figcaption></figcaption></figure></div>

The `.pxp` files of all the tables are in the `data_steam` folder of the game (in Steam: right-click on the game, **Manage > Browse local files**).

{% hint style="warning" %}
The `data_steam` folder contains all the tables: only the ones you own will start.
{% endhint %}

<details>

<summary>Table names</summary>

* `Alien_Isolation`
* `Alien_vs_Predator`
* `Aliens`
* `AmericanDad`
* `Archer`
* `Atlantis`
* `BETHESDA_Doom`
* `BETHESDA_Fallout`
* `BETHESDA_Skyrim`
* `BioLab`
* `BobsBurgers`
* `CastleStorm`
* `Citadel`
* `EarthDefense`
* `Eldorado`
* `Excalibur`
* `FamilyGuy`
* `Football`
* `Football_Arsenal`
* `Football_Barcelona`
* `Football_Juventus`
* `Football_Liverpool`
* `Football_Milan`
* `Football_RealMadrid`
* `Football_Roma`
* `Looter`
* `Mars`
* `MARVEL_Age_of_Ultron`
* `MARVEL_Ant-Man`
* `MARVEL_Avengers`
* `MARVEL_Blade`
* `MARVEL_CaptainAmerica`
* `MARVEL_CivilWar`
* `MARVEL_Deadpool`
* `MARVEL_DrStrange`
* `MARVEL_FantasticFour`
* `MARVEL_FearItSelf`
* `MARVEL_GhostRider`
* `MARVEL_Guardians`
* `MARVEL_InfinityGauntlet`
* `MARVEL_IronMan`
* `MARVEL_MoonKnight`
* `MARVEL_MsMarvel`
* `MARVEL_SpiderMan`
* `MARVEL_Thor`
* `MARVEL_Venom`
* `MARVEL_Wolverine`
* `MARVEL_WOP_TheNextGeneration`
* `MARVEL_WWH`
* `MARVEL_XMen`
* `Paranormal`
* `Pasha`
* `PlantsVsZombies`
* `Portal`
* `Rome`
* `Shaman`
* `SouthPark1`
* `SouthPark2`
* `SplosionMan`
* `STARWARS_Boba_Fett`
* `STARWARS_CloneWars`
* `STARWARS_Darth_Vader`
* `STARWARS_Droids`
* `STARWARS_Episode_4`
* `STARWARS_Episode_5`
* `STARWARS_Episode_6`
* `STARWARS_Episode_7`
* `STARWARS_Han_Solo`
* `STARWARS_Light_VS_Dark`
* `STARWARS_MFO`
* `STARWARS_Rebels`
* `STARWARS_SFA`
* `Tesla`
* `TheWalkingDead`
* `V12`
* `Western`

</details>

## Controls

The game handles the controller itself (XInput controller recommended): RetroBat does not change its configuration. Controls are changed in the game options.

<table><thead><tr><th width="204">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Left flipper</td><td>L1 or L2</td></tr><tr><td>Right flipper</td><td>R1 or R2</td></tr><tr><td>Launch the ball</td><td>Right stick down (pull, then release)</td></tr><tr><td>Auto launch the ball</td><td>SOUTH</td></tr><tr><td>Backbox view</td><td>Right stick up</td></tr><tr><td>Nudge the table</td><td>Left stick</td></tr><tr><td>Visual extras</td><td>EAST</td></tr><tr><td>Wizard power</td><td>WEST</td></tr><tr><td>Change view</td><td>NORTH</td></tr><tr><td>Menu</td><td>START or SELECT</td></tr></tbody></table>

## Hotkeys

<table><thead><tr><th width="180.25">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Quit the game</td><td>HOTKEY + START</td></tr></tbody></table>

The Game Control Center is not available for these systems.

## Useful options

In the advanced system or game settings:

* **VIDEO > VIDEO MODE**: Windows resolution during the game.
* **EMULATION > KILL LAUNCHER WHEN EXIT**: closes Steam when quitting the game (steam version).

## Folders

<table><thead><tr><th width="254">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Tables</td><td><code>roms\pinballfx2</code></td></tr><tr><td>Game (nonsteam version)</td><td><code>emulators\pinballfx2</code></td></tr><tr><td>Saves, scores, settings</td><td>Handled by the game (and by Steam)</td></tr></tbody></table>

## Known issues

* **The game opens on its menu, without the table**: Cabinet Mode not activated (see above), or table not owned.
* **"Game not found: copy it in '…'"** (nonsteam version): the game is not in the given folder, or its executable has another name.
* **"Steam is not installed."** (steam version): Steam was not found.
