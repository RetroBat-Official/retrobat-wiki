# GemRB

<div align="left"><figure><img src="../../../.gitbook/assets/image (781).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**GemRB** is a free version of BioWare's **Infinity Engine**. It runs the role-playing games **Baldur's Gate**, **Baldur's Gate II**, **Icewind Dale**, **Icewind Dale II** and **Planescape: Torment**, with their add-ons and mods.

GemRB has been developed for more than 20 years: compatibility is good, but games may still have flaws.

The games are not provided: you need the original releases (BioWare, Black Isle), from your own copies.

{% embed url="https://gemrb.org/" %}

## At a glance

<table><thead><tr><th width="244"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gemrb</code></td></tr><tr><td><strong>Extensions</strong></td><td>.auto .bg1 .bg2 .how .iwd .iwd2 .pst</td></tr><tr><td><strong>Default emulator</strong></td><td>gemrb</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic: the left stick moves the pointer</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Compatibility

<table><thead><tr><th>Game</th><th width="119">Playable</th><th width="143">Complete</th><th>Polished</th></tr></thead><tbody><tr><td>Baldur's Gate</td><td>YES</td><td>YES</td><td>YES</td></tr><tr><td>Baldur's Gate II</td><td>YES</td><td>YES</td><td>YES</td></tr><tr><td>Icewind Dale</td><td>YES</td><td>YES</td><td>YES</td></tr><tr><td>Icewind Dale II</td><td>YES</td><td>NO</td><td>NO</td></tr><tr><td>Planescape: Torment</td><td>YES</td><td>YES</td><td>NO</td></tr><tr><td>Enhanced Editions (Beamdog)</td><td>NO</td><td>NO</td><td>NO</td></tr></tbody></table>

## BIOS

No BIOS is needed.

## Which game format?

Each game is a folder holding all the files of the installed game. The folder name ends with a dot followed by the game identifier:

<table><thead><tr><th width="454">Game</th><th>Identifier</th></tr></thead><tbody><tr><td>Baldur's Gate (with or without Tales of the Sword Coast)</td><td><code>bg1</code></td></tr><tr><td>Baldur's Gate II: Shadows of Amn (with or without Throne of Bhaal)</td><td><code>bg2</code></td></tr><tr><td>Icewind Dale (without add-on)</td><td><code>iwd</code></td></tr><tr><td>Icewind Dale: Heart of Winter (with or without Trials of the Luremaster)</td><td><code>how</code></td></tr><tr><td>Icewind Dale II</td><td><code>iwd2</code></td></tr><tr><td>Planescape: Torment</td><td><code>pst</code></td></tr><tr><td>Automatic detection (to try)</td><td><code>auto</code></td></tr></tbody></table>

Example for Baldur's Gate:

<div align="left"><figure><img src="../../../.gitbook/assets/image (783).png" alt=""><figcaption></figcaption></figure></div>

## Controls

The games are played with mouse and keyboard (point and click). Touch screens work as a mouse.

RetroBat enables the controller: the left stick moves the pointer, the right stick scrolls the map. **CONTROLS > POINTER SPEED** and **STICK DEADZONE** adjust it. With several controllers, only the player 1 one is used.

### Hotkeys

<table><thead><tr><th width="301.5">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="285.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\gemrb\&#x3C;game>.&#x3C;identifier></code></td></tr><tr><td>Saves</td><td><code>saves\gemrb\&#x3C;game></code></td></tr><tr><td>Configuration</td><td><code>emulators\gemrb\GemRB.cfg</code></td></tr></tbody></table>

## Guides

### Change the resolution

Without a widescreen mod, the games are displayed in their original resolutions:

| Game                                                     | Original resolutions                 |
| -------------------------------------------------------- | ------------------------------------ |
| Baldur's Gate (with or without Tales of the Sword Coast) | 640x480                              |
| Baldur's Gate II (with or without Throne of Bhaal)       | 640x480, 800x600, 1024x768, 1280x960 |
| Icewind Dale (without add-on)                            | 640x480                              |
| Icewind Dale: Heart of Winter                            | 640x480, 800x600, 1024x768, 1280x960 |
| Icewind Dale II                                          | 800x600, 1024x768, 1280x960          |
| Planescape: Torment                                      | 640x480                              |

Select the resolution in **INTERNAL GAME RESOLUTION** (DESKTOP = screen resolution):

<div align="left"><figure><img src="../../../.gitbook/assets/image (782).png" alt=""><figcaption></figcaption></figure></div>

### Widescreen mods

For a widescreen resolution, apply a widescreen mod to the game (depending on the game, other mods may be needed for the interface to display correctly):

{% embed url="https://www.gibberlings3.net/mods/tools/widescreen/" %}

Follow the mod instructions, then select in **INTERNAL GAME RESOLUTION** the resolution set with the mod (DESKTOP if it is the screen one).

### Options

* **VISUAL RENDERING > ZOOM**: map zoom with the mouse wheel, like the Enhanced Editions.
* **EMULATION > LANGUAGE ENCODING**: only for the Asian versions of the games.

## Known issues

| Issue                                                | Solution                                            |
| ---------------------------------------------------- | --------------------------------------------------- |
| The wrong game is started or the game does not start | Check the identifier at the end of the folder name. |
| The pointer moves on its own                         | Increase **STICK DEADZONE**.                        |
