# REminiscence

<div align="left"><figure><img src="../../../.gitbook/assets/image (788).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

**Flashback** (Delphine Software, 1992) is a 2D action-adventure game, with rotoscoped animations, in a science fiction world.

RetroBat runs it with the **REminiscence** libretro core, a rewrite of the game engine.

The game files are not provided: use the ones from your own copy, **PC version (DOS or CD)**, or the files of the [GOG](https://www.gog.com/game/flashback) / [Steam](https://store.steampowered.com/app/961620/Flashback/) versions.

{% embed url="https://docs.libretro.com/library/reminiscence/" %}

## At a glance

<table><thead><tr><th width="235.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\reminiscence</code></td></tr><tr><td><strong>Extensions</strong></td><td>.rem</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: reminiscence</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

{% hint style="warning" %}
The core only runs the PC (DOS) version of the game: Amiga or Macintosh files are not recognized.
{% endhint %}

## Which game format?

An empty `.rem` file starts the game whose files are in its folder or its subfolders.

## Controls

<table><thead><tr><th width="226.5">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>D-pad, left stick</td><td>Move</td></tr><tr><td>SOUTH</td><td>Draw / holster the weapon</td></tr><tr><td>EAST</td><td>Use the item</td></tr><tr><td>NORTH</td><td>Action</td></tr><tr><td>WEST</td><td>Inventory / skip</td></tr></tbody></table>

### Hotkeys

RetroArch hotkeys. See the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="201.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game</td><td><code>roms\reminiscence\Flashback</code></td></tr></tbody></table>

## Guides

### File layout

In `roms\reminiscence`, create a `Flashback` folder. Copy the game files into it; for the GOG and Steam versions, these are the files of the `Flashback_Data\StreamingAssets\data` folder:

<div align="left"><figure><img src="../../../.gitbook/assets/image (791).png" alt=""><figcaption></figcaption></figure></div>

Some voices and music may be missing. The Amiga music by Raphaël Gesqua can be added to the `Flashback` folder:

<div align="left"><figure><img src="../../../.gitbook/assets/image (789).png" alt=""><figcaption></figcaption></figure></div>

Finally, create an empty text file in `roms\reminiscence`, named `Flashback`, with the `.rem` extension (`Flashback.rem`):

<div align="left"><figure><img src="../../../.gitbook/assets/image (790).png" alt=""><figcaption></figcaption></figure></div>

## Known issues

<table><thead><tr><th width="275.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start</td><td>The files are not the PC (DOS) version ones, or they are not in the folder of the <code>.rem</code> file or one of its subfolders.</td></tr></tbody></table>
