# Softpatching

A **patch** is a file that contains changes for a ROM: translation, bug fixes, improvements, hacks… **Softpatching** applies the patch when the game starts, in memory: your original ROM is never modified, and you can play with or without the patch.

{% hint style="info" %}
Softpatching works with the **RetroArch cores** that load the game in memory (mainly cartridge systems and handhelds). See the list of compatible cores below.
{% endhint %}

## Patch formats

<table><thead><tr><th width="171.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>IPS</strong> (<code>.ips</code>)</td><td>The oldest and most common format. Simple, but it does not check the ROM: a patch applied to the wrong version of the ROM can give a broken game.</td></tr><tr><td><strong>UPS</strong> (<code>.ups</code>)</td><td>Checks that the ROM is the right one before applying the patch. Often used for Game Boy Advance.</td></tr><tr><td><strong>BPS</strong> (<code>.bps</code>)</td><td>The most modern format. Checks the ROM and the result. Recommended when available.</td></tr><tr><td><strong>xdelta</strong> (<code>.xdelta</code>)</td><td>Format used for large files, for example some Nintendo DS translations. Checks the ROM before applying the patch.</td></tr></tbody></table>

{% hint style="warning" %}
A patch is made for **one precise version** of a ROM (region, revision, with or without header). The readme of the patch usually tells you which ROM to use. With UPS, BPS and xdelta, the patch is not applied if the ROM is not the right one.
{% endhint %}

## Where to put the patches

Choose where RetroBat looks for patches with the **SOFTPATCHING** option:

* for all systems: **MAIN MENU > GAME SETTINGS**, **RETROARCH OPTIONS** group > **EMULATION** > **SOFTPATCHING**;
* for one system or one game: **ADVANCED SETTINGS > EMULATION > SOFTPATCHING** in the system or game options.

<div align="left"><figure><img src="../.gitbook/assets/image (414).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="210.75">Choice</th><th>Where to put the patch</th><th>Name of the patch</th></tr></thead><tbody><tr><td><strong>AUTO</strong> (default)</td><td>Next to the ROM</td><td>Same name as the ROM: <code>Game.sfc</code> → <code>Game.ips</code></td></tr><tr><td><strong>PATCH IN PATCH SUBFOLDER</strong></td><td>In a <code>patches</code> folder next to the ROMs: <code>roms\snes\patches\</code></td><td>Same name as the ROM: <code>patches\Game.ips</code></td></tr><tr><td><strong>PATCH IN ROM SUBFOLDER</strong></td><td>In a folder named after the ROM followed by <code>-patches</code>: <code>roms\snes\Game-patches\</code></td><td>Any name</td></tr><tr><td><strong>DISABLED</strong></td><td>No patch is applied, even if a patch file exists.</td><td></td></tr></tbody></table>

Example with AUTO:

```
roms\snes\
   Game.sfc
   Game.bps
```

Example with PATCH IN ROM SUBFOLDER:

```
roms\snes\
   Zelda.sfc
   Zelda-patches\
      Translation.bps
```

{% hint style="info" %}
* For a zipped ROM, name the patch after the .zip: `Game.zip` → `Game.ips`.
* When a patch is applied, RetroArch shows a message at the start of the game.
* With **PATCH IN ROM SUBFOLDER**, you can keep several versions of patches for the same game, and switch from one to another by renaming the folder.
{% endhint %}

## Applying several patches

Several patches can be applied one after the other (for example a translation, then a fix of this translation). Number them, starting from the second one:

```
Game.ips     ← applied first
Game.ips1    ← applied second
Game.ips2    ← applied third
```

* Up to 10 patches: from `Game.ips` to `Game.ips9`.
* Use the **same format** for all the patches of a game (`.ips`, `.ips1`… or `.bps`, `.bps1`… or `.xdelta`, `.xdelta1`…).
* The order matters: follow the order given by the authors of the patches.
* With **PATCH IN ROM SUBFOLDER**, the first patch can have any name, and the next ones take the same name with the number: `Translation.bps`, `Translation.bps1`…

## Saves

A patched game uses the **same save file** as the original game, because it has the same name. To keep separate saves, make a copy of the ROM with another name, and name the patch after this copy.

## Compatible cores

The **SOFTPATCHING** option is available for these RetroArch cores:

<table><thead><tr><th width="264">System</th><th>Cores</th></tr></thead><tbody><tr><td>Nintendo - NES / Famicom</td><td>FCEUmm, Mesen, Nestopia UE, QuickNES</td></tr><tr><td>Nintendo - SNES / Super Famicom, Satellaview</td><td>bsnes, bsnes HD beta, bsnes-jg, bsnes Mercury Accuracy, bsnes Mercury Balanced, Mednafen SNES, Mesen-S, Snes9x, Snes9x 2002, Snes9x 2005, Snes9x 2005 Plus, Snes9x 2010</td></tr><tr><td>Nintendo - Game Boy / Game Boy Color</td><td>DoubleCherryGB, Gambatte, Gearboy, mGBA, SameBoy, TGB Dual, VBA-M</td></tr><tr><td>Nintendo - Game Boy Advance</td><td>mGBA, mGBA splitscreen, Mednafen GBA, VBA-M, VBA Next</td></tr><tr><td>Nintendo - Nintendo DS</td><td>melonDS, melonDS DS</td></tr><tr><td>Nintendo - Nintendo 64</td><td>Mupen64Plus-Next</td></tr><tr><td>Nintendo - Virtual Boy</td><td>Mednafen VB</td></tr><tr><td>Nintendo - Pokémon mini</td><td>PokeMini</td></tr><tr><td>Sega - Master System / Game Gear</td><td>Gearsystem, Genesis Plus GX, PicoDrive, SMS Plus GX</td></tr><tr><td>Sega - Mega Drive / Genesis</td><td>BlastEm, Genesis Plus GX (Wide, Expanded), PicoDrive</td></tr><tr><td>NEC - PC Engine / TurboGrafx-16</td><td>Mednafen PCE, Mednafen PCE Fast</td></tr><tr><td>Bandai - WonderSwan / Color</td><td>Mednafen WonderSwan</td></tr><tr><td>SNK - Neo Geo Pocket / Color</td><td>Mednafen NGP</td></tr><tr><td>Atari - 2600 / 5200 / 7800</td><td>Stella, Stella 2014 (2600), a5200 (5200), ProSystem (7800)</td></tr><tr><td>Atari - Lynx</td><td>Gearlynx, Handy, Holani, Mednafen Lynx</td></tr><tr><td>Atari - Jaguar</td><td>Virtual Jaguar</td></tr><tr><td>Coleco - ColecoVision</td><td>Gearcoleco, JollyCV</td></tr><tr><td>Vectrex</td><td>vecx</td></tr><tr><td>Watara - Supervision</td><td>Potator</td></tr><tr><td>Magnavox - Odyssey²</td><td>O2EM</td></tr><tr><td>Fairchild - Channel F</td><td>FreeChaF</td></tr></tbody></table>

## Common problems

<table><thead><tr><th width="297.75">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>The patch is not applied</td><td>Check the name of the patch (the same as the ROM, except with PATCH IN ROM SUBFOLDER), its folder and the SOFTPATCHING option. Check that the core is in the list above.</td></tr><tr><td>The game is broken or does not start</td><td>The patch is not made for this version of the ROM. Check the readme of the patch.</td></tr><tr><td>Only the first patch is applied</td><td>Check the numbering: <code>Game.ips</code>, then <code>Game.ips1</code>, <code>Game.ips2</code>… with the same format.</td></tr></tbody></table>
