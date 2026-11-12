---
description: ScummVM Team
---

# ScummVM

<div align="left"><figure><img src="../../../.gitbook/assets/image (505).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Presentation

**ScummVM** is not an emulator: it is a program that replaces the original executable of hundreds of adventure and role-playing games, so they can run on current machines. You therefore need the data files of the games.

The project started in 2001 to bring back the LucasArts games written with the SCUMM engine, created in 1987 for Maniac Mansion: Monkey Island, Day of the Tentacle, Sam & Max, Full Throttle… Hence its name. It has since opened up to many other engines: Sierra (King's Quest, Space Quest), Revolution (Broken Sword, Beneath a Steel Sky), Westwood (Kyrandia), Cyan (Myst, Riven)… Since its merge with ResidualVM in 2020, it also runs 3D games such as Grim Fandango.

A few games are given away by their publishers and can be downloaded from the ScummVM website, for example Beneath a Steel Sky, Flight of the Amazon Queen or Lure of the Temptress.

{% embed url="https://en.wikipedia.org/wiki/ScummVM" %}

## At a glance

<table><thead><tr><th width="226.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\scummvm</code></td></tr><tr><td><strong>Extensions</strong></td><td>.scummvm .7z .zip .rar .squashfs</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: scummvm</td></tr><tr><td><strong>BIOS</strong></td><td>None required</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic (scummvm: handled by ScummVM)</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>MT32_CONTROL.ROM</code> and <code>MT32_PCM.ROM</code> in <code>bios\scummvm\extra</code> (Roland MT-32 music)</td></tr></tbody></table>

## Which emulator to choose?

Both emulators use the same ScummVM version and share their saves.

<table><thead><tr><th width="183.25">Emulator</th><th width="318.25">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: scummvm</strong> (default)</td><td>ScummVM inside RetroArch: controllers configured by RetroBat, shaders, decorations, usual hotkeys, cursor settings for the controller.</td><td>The <code>.scummvm</code> file must contain the game identifier.</td></tr><tr><td><strong>scummvm</strong></td><td>Detects the game by itself when the <code>.scummvm</code> file is empty. More display options: scalers, EGA / CGA / Amiga… rendering, screen rotation.</td><td>Controllers are not configured by RetroBat. Only one controller hotkey: quit.</td></tr></tbody></table>

## BIOS

ScummVM does not need any BIOS. Two optional files let you hear the music of games designed for the **Roland MT-32** synthesizer:

<table><thead><tr><th width="164.5">File</th><th width="337.25">MD5</th><th>Location</th></tr></thead><tbody><tr><td><code>MT32_CONTROL.ROM</code></td><td><code>5626206284b22c2734f3e9efefcd2675</code></td><td><code>bios\scummvm\extra</code></td></tr><tr><td><code>MT32_PCM.ROM</code></td><td><code>89e42e386e82e0cacb4a2704a03706ca</code></td><td><code>bios\scummvm\extra</code></td></tr></tbody></table>

They are used when the **AUDIO > SOUND MODE** option is set to **Emulated MT-32**.

The ScummVM data files (`bios\scummvm\extra` folder), its themes (`bios\scummvm\theme`) and the `Roland_SC-55.sf2` soundfont are provided with RetroBat.

## Which game format?

A ScummVM game is a **folder** that holds the files of the original game. RetroBat launches it through a small `.scummvm` text file placed in that folder.

<table><thead><tr><th width="260.25">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>Game folder + <code>.scummvm</code> file</strong></td><td>The recommended format: <code>roms\scummvm\Full Throttle\Full Throttle.scummvm</code>. The file contains the game identifier on its first line (see Guides).</td></tr><tr><td>.7z, .zip, .rar, .squashfs</td><td>The compressed game folder, with its <code>.scummvm</code> file at the root of the archive. RetroBat mounts or extracts the archive at launch.</td></tr></tbody></table>

The name of the `.scummvm` file is the one RetroBat shows in the game list.

With the **scummvm** emulator, the `.scummvm` file can stay empty (or be missing from an archive): ScummVM then detects the game found in the folder.

## Controls

### Automatic configuration

ScummVM games are played with the mouse and the keyboard. The mouse works with both emulators, and the controller moves the cursor.

**libretro: scummvm**: RetroBat configures the controllers. The core uses these buttons by default:

<table><thead><tr><th width="206.5">Controller</th><th>Action</th></tr></thead><tbody><tr><td>D-pad, left stick</td><td>Move the cursor</td></tr><tr><td>L1</td><td>Left click</td></tr><tr><td>R1</td><td>Right click</td></tr><tr><td>R2 (held)</td><td>Slow cursor, for more precision</td></tr><tr><td>SOUTH</td><td>ENTER</td></tr><tr><td>EAST</td><td>SPACE (pause)</td></tr><tr><td>NORTH</td><td>F5 (game menu)</td></tr><tr><td>WEST</td><td>ESC (skip a scene)</td></tr><tr><td>Right stick</td><td>Keyboard arrows</td></tr><tr><td>START</td><td>ScummVM menu</td></tr><tr><td>SELECT</td><td>Virtual keyboard</td></tr></tbody></table>

These buttons can be changed in the RetroArch core options (RetroPad category). Useful options, in **CONTROLS**:

<table><thead><tr><th width="259">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>POINTER DEVICE</strong></td><td>What moves the cursor: controller and mouse (default), controller only, or controller and pointer (touch screen).</td></tr><tr><td><strong>GAMEPAD CURSOR SPEED</strong></td><td>1.0 by default, meant for 320x200 games. Raise it to 2.0 for 640x480 games.</td></tr><tr><td><strong>ANALOG DEADZONE</strong></td><td>Raise it if the cursor moves by itself.</td></tr><tr><td><strong>KEYBOARD FOCUS</strong></td><td>Gives the whole keyboard to the game and disables the RetroArch keyboard shortcuts.</td></tr></tbody></table>

**scummvm**: RetroBat does not configure the controllers, ScummVM detects them itself. Default buttons:

<table><thead><tr><th width="230.25">Controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Move the cursor</td></tr><tr><td>R1 (held)</td><td>Slow cursor</td></tr><tr><td>SOUTH</td><td>Left click</td></tr><tr><td>EAST</td><td>Right click</td></tr><tr><td>NORTH</td><td>Skip a scene (ESC)</td></tr><tr><td>WEST</td><td>Skip a line of dialogue</td></tr><tr><td>L1</td><td>Game menu (F5)</td></tr><tr><td>D-pad</td><td>Directions</td></tr><tr><td>START</td><td>ScummVM menu</td></tr><tr><td>SELECT</td><td>Virtual keyboard</td></tr></tbody></table>

Some game engines define their own buttons. Everything can be changed in ScummVM: **Global Options > Keymaps**.

To bind other keyboard keys to the controller, create a profile from the game options in RetroBat: **CREATE PADTOKEY PROFILE** (both emulators). For more details, see the [**Pad2Key**](../../../controllers/pad2key.md) page.

### Hotkeys

| Action                             | libretro: scummvm | scummvm        | Keyboard (scummvm) |
| ---------------------------------- | ----------------- | -------------- | ------------------ |
| **Quit**                           | HOTKEY + START    | HOTKEY + START | CTRL + Q           |
| ScummVM menu (save, load, options) | START             | START          | CTRL + F5          |
| Virtual keyboard                   | SELECT            | SELECT         | CTRL + F7          |
| RetroArch menu                     | HOTKEY + SOUTH    | —              | —                  |
| Screenshot                         | HOTKEY + R3       | —              | ALT + S            |
| Fast forward                       | HOTKEY + RIGHT    | —              | —                  |
| Fullscreen                         | —                 | —              | ALT + ENTER        |
| Mute                               | —                 | —              | CTRL + U           |

The libretro core supports neither save states nor rewind: these hotkeys have no effect.

## Folders

| Content                                          | Folder                          |
| ------------------------------------------------ | ------------------------------- |
| Games                                            | `roms\scummvm`                  |
| Saves (shared by both emulators)                 | `saves\scummvm`                 |
| Data files, soundfonts, MT-32 ROMs               | `bios\scummvm\extra`            |
| ScummVM themes                                   | `bios\scummvm\theme`            |
| Configuration and added games, libretro: scummvm | `bios\scummvm.ini`              |
| Configuration and added games, scummvm           | `emulators\scummvm\scummvm.ini` |
| Log of the scummvm emulator                      | `emulators\scummvm\scummvm.log` |
| Screenshots                                      | `screenshots`                   |

## Guides

### Adding a game

1. Copy the game folder into `roms\scummvm`, for example `roms\scummvm\Full Throttle`.
2. In that folder, create a text file named after the game: `Full Throttle.txt`.
3. Write the game identifier on the first line, for example:

```
scumm:ft
```

4. Replace the `.txt` extension with `.scummvm`: `Full Throttle.scummvm`.
5. Update the RetroBat game list.

The identifier is listed in the compatibility list of the ScummVM website ([scummvm.org/compatibility](https://www.scummvm.org/compatibility/)), in the form `engine:game`. A few examples:

<table><thead><tr><th width="364">Game</th><th>Identifier</th></tr></thead><tbody><tr><td>The Secret of Monkey Island</td><td><code>scumm:monkey</code></td></tr><tr><td>Day of the Tentacle</td><td><code>scumm:tentacle</code></td></tr><tr><td>Sam &#x26; Max Hit the Road</td><td><code>scumm:samnmax</code></td></tr><tr><td>Beneath a Steel Sky</td><td><code>sky:sky</code></td></tr><tr><td>Broken Sword: The Shadow of the Templars</td><td><code>sword1:sword1</code></td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (506).png" alt=""><figcaption></figcaption></figure></div>

### Choosing a version or setting up a game in ScummVM

When a folder holds several versions of a game (floppy and CD, several languages), or to keep settings specific to a game, add the game in ScummVM:

1. In the **RetroBat** system, launch **ScummVM** or **ScummVM Libretro**, depending on the emulator you use.

<div align="left"><figure><img src="../../../.gitbook/assets/image (507).png" alt=""><figcaption></figcaption></figure></div>

2. Click **Add Game**, select the game folder then the version you want.

<div align="left"><figure><img src="../../../.gitbook/assets/image (508).png" alt=""><figcaption></figcaption></figure></div>

3. In the game options, read or change the **ID** field, for example `ft-cd-fr`, and set up the game (language, subtitles…).

<div align="left"><figure><img src="../../../.gitbook/assets/image (509).png" alt=""><figcaption></figcaption></figure></div>

4. In the game folder, create a `.scummvm` file that contains exactly this ID.

<div align="left"><figure><img src="../../../.gitbook/assets/image (510).png" alt=""><figcaption></figcaption></figure></div>

Each emulator keeps its own list of games: a game added in ScummVM is not known to ScummVM Libretro, and the other way round.

### Compressed game

Compress the **content** of the game folder, including the `.scummvm` file, so that this file sits at the root of the archive. Put the archive in `roms\scummvm`.

### Music: MT-32, AdLib or General MIDI

By default, ScummVM picks the sound output of each game by itself. The **AUDIO > SOUND MODE** option lets you force it:

<table><thead><tr><th width="220.25">Choice</th><th>Output</th></tr></thead><tbody><tr><td><strong>FluidSynth</strong></td><td>General MIDI, played with the soundfont selected in <strong>MIDI SOUNDFONT</strong>.</td></tr><tr><td><strong>Emulated MT-32</strong></td><td>Roland MT-32, the best music of many games from 1988 to 1992. Requires the two ROM files (see BIOS).</td></tr><tr><td><strong>AdLib</strong></td><td>The most common sound card of the time, with three emulations to choose from.</td></tr></tbody></table>

The **Roland SC-55** soundfont is provided. To use **Roland SC-88**, put a `Roland_SC-88.sf2` file in `bios\scummvm\extra`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (511).png" alt=""><figcaption></figcaption></figure></div>

### Saving

There are no save states: use the in-game saves. Press **START** to open the ScummVM menu, then **Save** or **Load**. Saves are read by both emulators.

## Known issues

| Issue                                                       | Solution                                                                                                                      |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| "Game not found" message, or back to the game list          | Check the identifier written in the `.scummvm` file, and that this file is in the game folder, along with all the game files. |
| The game starts with scummvm but not with libretro: scummvm | The `.scummvm` file is empty or missing from the archive: write the game identifier on its first line.                        |
| An ID created in ScummVM is not recognized                  | It was created in the other emulator: add the game in both, or use the `engine:game` identifier.                              |
| Message saying the game is not fully supported (scummvm)    | Turn on **EMULATION > ALLOW UNSUPPORTED GAMES**.                                                                              |
| The cursor is too slow with the controller                  | libretro: scummvm: raise **GAMEPAD CURSOR SPEED**.                                                                            |
| No MT-32 music                                              | Add `MT32_CONTROL.ROM` and `MT32_PCM.ROM` to `bios\scummvm\extra`, then select **Emulated MT-32** in **SOUND MODE**.          |
| The **Roland SC-88** choice changes nothing                 | The `Roland_SC-88.sf2` file is not provided: add it to `bios\scummvm\extra`.                                                  |
| Voices without subtitles, or the other way round            | Set **TEXT AND SPEECH** (libretro: scummvm) or **TEXT AND VOICES** (scummvm).                                                 |
