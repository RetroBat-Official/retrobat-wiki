---
description: Amstrad
---

# Amstrad CPC

<div align="left"><figure><img src="../../../.gitbook/assets/image (491).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Amstrad CPC** (Colour Personal Computer) is a range of 8-bit home computers launched in 1984 by the British company Amstrad, founded by Alan Sugar. The idea was simple: sell a complete computer, ready to plug in. The CPC 464 bundles in one purchase the computer with its keyboard, a built-in cassette deck and a monitor (colour or green monochrome), all running from a single power plug.

The machine is built around a Zilog Z80A processor at 4 MHz, 64 KB of memory, a 27-colour palette and the AY-3-8912 sound chip. It boots straight into Locomotive BASIC: on a real CPC, you have to type a command to start a game.

The range evolved quickly:

* **CPC 464** (1984): 64 KB, cassette deck;
* **CPC 664** (1985): a 3-inch floppy drive replaces the cassette deck;
* **CPC 6128** (1985): 128 KB and floppy drive, the most common model;
* **464 Plus** and **6128 Plus** (1990): cartridge port, 4096-colour palette and hardware sprites, like the GX4000 console (see the [**Amstrad GX4000**](../game-consoles/gx4000.md) page).

With around three million units sold, the CPC was a huge success in France, Spain and the United Kingdom. Its library holds thousands of titles: Gryzor, Renegade, Rick Dangerous, Sorcery, Get Dexter, L'Aigle d'Or, Head Over Heels, Barbarian, Prince of Persia, La Abadía del Crimen…

{% embed url="https://en.wikipedia.org/wiki/Amstrad_CPC" %}

## At a glance

<table><thead><tr><th width="234"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\amstradcpc</code></td></tr><tr><td><strong>Extensions</strong></td><td>.dsk .kcr .sna .tap .cdt .voc .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: cap32</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (cap32)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (cap32)</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="159">Emulator</th><th width="167.75">For whom?</th><th width="233.75">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: cap32</strong> (default)</td><td>Everyone</td><td>Starts games by itself (disks and tapes), virtual keyboard, keyboard keys already placed on the controller for nearly 400 games, multi-disk games, RetroAchievements, light guns.</td><td>—</td></tr><tr><td><strong>libretro: crocods</strong></td><td>Those who want the simplest option</td><td>Starts quickly, runs disks by itself.</td><td>Disks and snapshots only, no tapes, no virtual keyboard, no RetroAchievements.</td></tr><tr><td><strong>capriceforever</strong></td><td>Advanced users</td><td>Very accurate emulation, many hardware expansions (memory, speech synthesizers, PlayCity, Multiface II…), two floppy drives.</td><td>No save states in RetroBat, no RetroAchievements, a keyboard is recommended.</td></tr></tbody></table>

**When in doubt, keep cap32.**

## BIOS

No BIOS is needed: the emulators already include the Amstrad ROMs.

### Machine language

The CPC existed in English (QWERTY keyboard), French (AZERTY keyboard) and Spanish versions. By default, RetroBat emulates an English CPC 6128. Some French games expect an AZERTY keyboard.

<table><thead><tr><th width="142">Emulator</th><th>Option</th><th>Choices</th></tr></thead><tbody><tr><td>cap32</td><td><strong>EMULATION > KEYBOARD LAYOUT</strong></td><td>ENGLISH (default), FRENCH, SPANISH</td></tr><tr><td>capriceforever</td><td><strong>EMULATION > AMSTRAD MODEL</strong></td><td>CPC 6128 UK (default), CPC 6128 FR, CPC 6128 ES, CPC 464 UK, CPC 464 FR, CPC 464 ES</td></tr><tr><td>crocods</td><td>—</td><td>English only</td></tr></tbody></table>

With cap32, the **EMULATION > MODEL TYPE** option also lets you emulate a 464 or a 664 for the oldest games.

## Which game format?

<table><thead><tr><th width="118.25">Format</th><th width="88.5">cap32</th><th width="102">crocods</th><th width="122.75">capriceforever</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.dsk</strong></td><td>✔</td><td>✔</td><td>✔</td><td>Floppy disk. Recommended format: fast loading.</td></tr><tr><td>.m3u</td><td>✔</td><td>✘</td><td>✔</td><td>Games on several disks (see Guides).</td></tr><tr><td>.cdt / .voc</td><td>✔</td><td>✘</td><td>✘</td><td>Tape. Long loading, like on the real machine.</td></tr><tr><td>.tap</td><td>✔</td><td>✘</td><td>✔</td><td>Tape.</td></tr><tr><td>.sna</td><td>✔</td><td>✔</td><td>✘</td><td>Snapshot: memory copy of an already loaded game.</td></tr><tr><td>.kcr</td><td>✘</td><td>✔</td><td>✘</td><td>CrocoDS-specific format.</td></tr><tr><td>.zip</td><td>✔</td><td>✘</td><td>✔ (extracted at launch)</td><td></td></tr><tr><td>.7z</td><td>✔</td><td>✔</td><td>✔ (extracted at launch)</td><td></td></tr></tbody></table>

## Controls

### Automatic configuration

RetroBat configures controllers automatically for all emulators (two controllers at most with Caprice Forever).

An Amstrad joystick only has two or three fire buttons. Many games also use the keyboard: to pick "joystick" in a menu, start the game or pause. RetroBat therefore places keyboard keys on the controller.

| RetroBat controller | cap32                 | crocods  | capriceforever |
| ------------------- | --------------------- | -------- | -------------- |
| D-pad / left stick  | Joystick              | Joystick | Joystick       |
| EAST                | Fire 1                | Fire 1   | Fire 1         |
| SOUTH               | Fire 2                | Fire 2   | Fire 2         |
| NORTH               | Fire 3                | —        | —              |
| WEST                | Combo key (see below) | —        | —              |
| L1                  | CONTROL               | —        | —              |
| R1                  | RETURN                | —        | —              |
| L2                  | F1                    | —        | —              |
| R2                  | F2                    | —        | —              |
| START               | —                     | RETURN   | —              |
| SELECT              | —                     | Space    | —              |
| L3                  | Virtual Keyboard      |          |                |

With crocods, the second controller sends the keyboard cursor keys and Space, not a second joystick.

### Combo key and virtual keyboard (cap32)

Hold **WEST** and press another button to send a command to the Amstrad:

| Combination            | Action                                                    |
| ---------------------- | --------------------------------------------------------- |
| **L3 or WEST + START** | Shows or hides the virtual keyboard                       |
| WEST + EAST            | Types `RUN"DISK` then `RUN"DISC` (starts many disk games) |
| WEST + SOUTH           | Types `CAT` (lists the disk content)                      |
| WEST + NORTH           | Types the commands that start a tape                      |
| WEST + UP              | Types `1` then `Y`                                        |
| WEST + DOWN            | Types `2` then `N`                                        |
| WEST + RIGHT           | Types `3` then `J`                                        |
| WEST + LEFT            | Types `4` then `S`                                        |
| WEST + L1 / R1         | Previous / next disk (`.m3u` games)                       |

The combinations with directions are meant to answer game menus (choices 1 to 4, yes / no, joystick…).

In the virtual keyboard, move the cursor with the D-pad and press a key with **EAST**. The mouse works too.

The **CONTROLS > COMBO KEY** option lets you pick another button.

### Keyboard keys on the controller (cap32)

For nearly 400 games, RetroBat automatically places on the controller the keyboard keys the game needs. The game is recognized by its file name (see [Guides](amstrad-cpc.md#customizing-the-keys-of-a-game-cap32)).

### Keyboard

A keyboard plugged into the PC acts as the Amstrad keyboard with all emulators.

* With cap32 and crocods, turn on **CONTROLS > KEYBOARD FOCUS** so that keys don't trigger RetroArch shortcuts. The **Scroll Lock** key toggles this mode in game.
* With cap32, **F9** shows the virtual keyboard. For tapes: **Home** = play, **End** = stop, **Page Up** = rewind.
* With Caprice Forever, the **CONTROLS > KEYBOARD AS JOYSTICK** option turns the arrow keys into the joystick, **ALT** into fire 1 and **CTRL** into fire 2.

To configure your controllers yourself, turn off **AUTOCONFIGURE CONTROLLERS**.

### Hotkeys

**cap32** and **crocods** use the RetroArch hotkeys (see the [Hotkeys page](../../../navigation/hotkeys.md)).

**Caprice Forever**: **HOTKEY + START** to quit.

## Folders

<table><thead><tr><th width="304">Content</th><th>Folder</th></tr></thead><tbody><tr><td>cap32 save states</td><td><code>saves\amstradcpc\libretro.cap32</code></td></tr><tr><td>crocods save states</td><td><code>saves\amstradcpc\libretro.crocods</code></td></tr><tr><td>Saves written to disk (cap32)</td><td><code>saves\amstradcpc</code> (<code>.sav</code> file named after the disk, the original disk is not modified)</td></tr><tr><td>Caprice Forever snapshots</td><td><code>saves\amstradcpc\capriceforever</code></td></tr><tr><td>Caprice Forever screenshots</td><td><code>screenshots\capriceforever</code></td></tr><tr><td>Caprice Forever cheats</td><td><code>cheats\capriceforever</code></td></tr><tr><td>Caprice Forever controller profiles</td><td><code>emulators\capriceforever\Profiles</code></td></tr><tr><td>Per-game keys provided by RetroBat (cap32)</td><td><code>system\resources\inputmapping\libretro_cap32.json</code></td></tr><tr><td>Custom per-game keys (cap32)</td><td><code>user\inputmapping\libretro_cap32.json</code></td></tr></tbody></table>

## Guides

### Games on several disks (.m3u)

Create a text file named after the game, with the `.m3u` extension, next to the disks. Write one disk name per line:

```
Alive (F) - Disk 1A.dsk
Alive (F) - Disk 1B.dsk
```

Then launch the `.m3u` file from RetroBat.

* **cap32**: swap disks in game with **WEST + L1** (previous) or **WEST + R1** (next).
* **Caprice Forever**: the first line goes into drive A, the second into drive B.

### Forcing the launch command

cap32 guesses the command to type to start a game. If the game doesn't start, you can force the right command.

**cap32**: create a `.m3u` file that starts with a `#COMMAND:` line, followed by the disk name:

```
#COMMAND:RUN"COMMANDO.BIN
Commando (Europe).dsk
```

**Caprice Forever**: create next to the game a text file with the same name and the `.autorun` extension, for example `Commando (Europe).autorun`. Its first line holds the command:

```
RUN"COMMANDO.BIN
```

To find the name of the file to run, list the disk content with `CAT` (**WEST + SOUTH** with cap32).

### Customizing the keys of a game (cap32)

RetroBat reads the per-game keys from `system\resources\inputmapping\libretro_cap32.json`. To change or add a game:

1. Copy this file to `user\inputmapping`. RetroBat then uses your copy, which is not overwritten by updates.
2. Open the copy with a text editor.
3. In the game's `Roms` list, add the exact name of your file, without extension. If the name is not listed, RetroBat compares the simplified file name (lowercase, no spaces, no text between parentheses or brackets) with the `Name` field.

<div align="left"><figure><img src="../../../.gitbook/assets/image (492).png" alt=""><figcaption></figcaption></figure></div>

### Playing with a light gun (cap32)

1. In the game options, turn on **GUNS > ENABLE GUN**.
2. Pick **GUNS > LIGHTGUN MODE** according to the game:

<table><thead><tr><th width="305.25">Mode</th><th>Games</th></tr></thead><tbody><tr><td><strong>PHASER</strong> (Amstrad Magnum Phaser)</td><td>Operation Wolf, Bullseye, Missile Ground Zero, Robot Attack, Rookie, Solar Invasion, American Turbo-King, Billy the Kid, Bronx Street Cop, F-16 Fighting Falcon, Jungle Warfare</td></tr><tr><td><strong>GUNSTICK</strong></td><td>Mike Gunner, Bestial Warrior, Cosmic Sheriff, El Equipo A, Guillermo Tell, Outlaws, Solo, Sootland, Space Smugglers, Target Plus, Trigger</td></tr><tr><td><strong>WEST PHASER</strong> (Loriciel West Phaser)</td><td>West Phaser</td></tr><tr><td><strong>TROJAN PHAZER</strong> (Trojan Light Phazer)</td><td>Cartridge games: see the <a href="../game-consoles/gx4000.md"><strong>Amstrad GX4000</strong></a> page</td></tr></tbody></table>

The **SHOW CROSSHAIR** option displays a crosshair on screen.

## Known issues

<table><thead><tr><th width="334">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game doesn't start, the screen stays on <code>Ready</code></td><td>The automatic command didn't find the right file. Try <strong>WEST + EAST</strong>, type the command with the virtual keyboard (<strong>WEST + START</strong>), or force it (see <a href="amstrad-cpc.md#forcing-the-launch-command">Guides</a>).</td></tr><tr><td>The game asks you to press a key or to pick keyboard / joystick</td><td>Use the virtual keyboard (<strong>L3</strong> or <strong>WEST + START</strong>) or the <strong>WEST + direction</strong> combinations.</td></tr><tr><td>Typed keys are wrong in a French game</td><td>Pick <strong>KEYBOARD LAYOUT</strong>: FRENCH (cap32) or <strong>AMSTRAD MODEL</strong>: CPC 6128 FR (Caprice Forever).</td></tr><tr><td>A very old game doesn't work</td><td>With cap32, pick <strong>MODEL TYPE</strong>: 464.</td></tr><tr><td>A tape takes a very long time to load</td><td>This is normal. Use RetroArch fast-forward (see the <a href="../../../navigation/hotkeys.md">Hotkeys page</a>) or prefer the <code>.dsk</code> disk version.</td></tr><tr><td>RetroArch shortcuts trigger when I type on the keyboard</td><td>Turn on <strong>KEYBOARD FOCUS</strong>.</td></tr><tr><td>The light gun doesn't respond</td><td>Check <strong>LIGHTGUN MODE</strong>. GUNSTICK mode doesn't work with a green monitor: leave <strong>MONITOR TYPE</strong> on COLOR.</td></tr><tr><td>crocods doesn't start the game</td><td>crocods only reads <code>.dsk</code>, <code>.sna</code> and <code>.kcr</code> files: use cap32.</td></tr><tr><td>The controller doesn't respond with Caprice Forever</td><td>The controller is not recognized: turn on <strong>KEYBOARD AS JOYSTICK</strong> or use cap32.</td></tr><tr><td>The virtual keyboard opens when I press L3</td><td>L3 always opens the virtual keyboard, even in games where RetroBat places a key on L3, and with <strong>HOTKEY + L3</strong>. Press <strong>L3</strong> again to close it.</td></tr></tbody></table>
