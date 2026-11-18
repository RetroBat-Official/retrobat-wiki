---
description: Atari
---

# Atari 800

<div align="left"><figure><img src="../../../../.gitbook/assets/image (616).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Atari 800** and **Atari 400** came out in late 1979. They were Atari's first home computers. Their graphics chips (ANTIC, CTIA then GTIA) and sound chip (POKEY) made them some of the most powerful machines of their time. The range continued with the 1200XL (1982), the 600XL and 800XL (1983), then the 65XE and 130XE (1985). All these models run the same software, with a few exceptions.

The game library is very rich: Star Raiders, M.U.L.E., Archon, Rescue on Fractalus!, Boulder Dash, Ballblazer, Alternate Reality… Games came on disk, tape and cartridge.

The RetroBat `atari800` system covers the whole 400/800/XL/XE range. The XE Game System (XEGS) console and the Atari 5200 console, from the same family, each have their own system (see the [**Atari XEGS**](../../game-consoles/atari-consoles/atarixegs.md) and [**Atari 5200**](../../game-consoles/atari-consoles/atari-5200.md) pages).

{% embed url="https://en.wikipedia.org/wiki/Atari_8-bit_family#Models" %}

## At a glance

<table><thead><tr><th width="202.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\atari800</code></td></tr><tr><td><strong>Extensions</strong></td><td>.rom .xfd .atr .atx .dcm .cas .bin .car .a52 .xex .com .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: atari800</td></tr><tr><td><strong>BIOS</strong></td><td>None (original ROMs optional)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro core</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="116.5">Emulator</th><th width="101.75">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: atari800</strong> (default)</td><td>Everyone</td><td>Atari800 7.0: the whole 400/800/XL/XE range, built-in operating system (AltirraOS) and BASIC (Altirra BASIC), virtual keyboard on the controller, save states.</td><td>—</td></tr><tr><td><strong>altirra</strong></td><td>Purists</td><td>Altirra, the most accurate Atari 8-bit emulator: excellent compatibility, copy-protected disks included.</td><td>Only one fire button on the controller. No save states and no RetroBat hotkeys (only HOTKEY + START, to quit).</td></tr></tbody></table>

**If in doubt, keep libretro: atari800.**

## BIOS

No BIOS is needed: the atari800 core has a free built-in operating system (AltirraOS) and BASIC (Altirra BASIC). The original ROMs improve compatibility with some software: the core uses them when they are in `bios`.

<table><thead><tr><th width="132.75">File</th><th width="73">Folder</th><th width="331">MD5</th><th>Used by</th></tr></thead><tbody><tr><td><code>ATARIOSA.ROM</code></td><td><code>bios</code></td><td>eb1f32f5d9f382db1bbfb8d7f9cb343a</td><td>atari800 core (400/800 OS A)</td></tr><tr><td><code>ATARIOSB.ROM</code></td><td><code>bios</code></td><td>a3e8d617c95d08031fe1b20d541434b2</td><td>atari800 core (400/800 OS B)</td></tr><tr><td><code>ATARIXL.ROM</code></td><td><code>bios</code></td><td>06daac977823773a3eea3422fd26a703</td><td>atari800 core (XL/XE OS)</td></tr><tr><td><code>ATARIBAS.ROM</code></td><td><code>bios</code></td><td>0bac0c6a50104045d902df4503a4c30b</td><td>atari800 core (BASIC)</td></tr></tbody></table>

The RetroBat BIOS check lists them as optional.

Altirra does not read the `bios` folder: it boots with its own built-in operating system. **EMULATION > KERNEL** (Altirra): **DEFAULT** uses the operating system chosen in Altirra's configuration, **INTERNAL** forces the built-in one.

## Which game format?

<table><thead><tr><th width="140.75">Type</th><th width="214.25">Extensions</th><th>Notes</th></tr></thead><tbody><tr><td>Disk</td><td><code>.atr</code>, <code>.atx</code>, <code>.xfd</code>, <code>.dcm</code></td><td><code>.atr</code> is the most common. <code>.atx</code> keeps copy protections.</td></tr><tr><td>Tape</td><td><code>.cas</code></td><td>RetroBat boots the tape automatically.</td></tr><tr><td>Cartridge</td><td><code>.car</code>, <code>.rom</code>, <code>.bin</code></td><td><code>.car</code> holds the cartridge type. With <code>.rom</code> and <code>.bin</code>, the emulator has to guess it.</td></tr><tr><td>Program</td><td><code>.xex</code>, <code>.com</code></td><td>Program loaded straight into memory.</td></tr><tr><td>Several disks</td><td><code>.m3u</code></td><td>List of a game's disks (see <strong>Guides</strong>).</td></tr></tbody></table>

Files can be compressed as `.zip` or `.7z` (one game per archive). `.a52` cartridges are Atari 5200 games: put them in `roms\atari5200`.

## Controls

RetroBat configures controllers automatically. The Atari joystick has a single fire button. The computer's **Start**, **Select** and **Option** keys are on the controller.

<table><thead><tr><th width="205.75">RetroBat controller</th><th width="228.5">libretro: atari800</th><th>altirra</th></tr></thead><tbody><tr><td>D-pad</td><td>Joystick</td><td>Joystick</td></tr><tr><td>Left stick</td><td>—</td><td>Joystick (<strong>USE LEFT STICK</strong> option)</td></tr><tr><td>SOUTH</td><td>Fire</td><td>Fire</td></tr><tr><td>EAST</td><td>Fire 2 (two-button joysticks, see <a href="atari-800.md#dual-stick-games-and-special-controllers"><strong>Guides</strong></a>)</td><td>—</td></tr><tr><td>WEST</td><td>Space</td><td>—</td></tr><tr><td>NORTH</td><td>Return</td><td>—</td></tr><tr><td>START</td><td>Start</td><td>Start</td></tr><tr><td>SELECT</td><td>Select</td><td>Select</td></tr><tr><td>L1</td><td>Option</td><td>—</td></tr><tr><td>L2</td><td>Esc</td><td>—</td></tr><tr><td>R2</td><td>Help (XL/XE)</td><td>—</td></tr><tr><td>L3</td><td>Virtual keyboard</td><td>—</td></tr></tbody></table>

The PC keyboard is the Atari keyboard. With the atari800 core, press `Scroll Lock` to turn on RetroArch's **Game Focus**: all keys go to the emulated computer. To put keyboard keys on the controller, see the **Pad2Key** page.

**ADVANCED SETTINGS > CONTROLS**:

* **PLAYER 1 / PLAYER 2 CONTROLLER TYPE** (atari800 core): **ATARI JOYSTICK** (default), **ATARI KEYBOARD**, **RETROPAD**.
* **FORCE USE OF PORT 2** (Altirra): for games that read the joystick on port 2.
* **FORCE PLAYER 1 / 2 PAD INDEX** (Altirra): chooses each player's controller.

### Hotkeys

The atari800 core uses the standard RetroArch hotkeys. With Altirra, RetroBat only sets HOTKEY + START (quit). See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="329">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\atari800</code></td></tr><tr><td>BIOS (atari800 core)</td><td><code>bios</code></td></tr><tr><td>atari800 core: save states</td><td><code>saves\atari800\libretro.atari800</code></td></tr><tr><td>atari800 core: engine configuration file</td><td><code>emulators\retroarch\.atari800.cfg</code></td></tr><tr><td>Altirra: configuration</td><td><code>emulators\altirra\Altirra.ini</code></td></tr><tr><td>Screenshots (atari800 core)</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Choosing the machine

A few early games only work on a 400/800, a few late games need an XL/XE with 64K or 128K.

* atari800 core: **EMULATION > EMULATED SYSTEM**. **800XL (64K)** by default. Choose **400/800 (48K) (OS B)** for an early game, **130XE (128K)** for a game that needs 128K.
* Altirra: **EMULATION > FORCE MACHINE** (**ATARI 800**, **ATARI 600XL/800XL**, **ATARI 1200XL**…). **EMULATION > SELECT PROFILE AUTOMATICALLY** lets Altirra choose from the game.

### BASIC programs

BASIC programs need the machine's BASIC: turn on **EMULATION > INTERNAL BASIC** (atari800 core). The core uses `ATARIBAS.ROM` when present, the built-in Altirra BASIC otherwise. Leave the option off for games: some do not boot with BASIC on.

### Dual stick games and special controllers

**CONTROLS > CONTROLLER HACKS** (atari800 core):

* **DUAL STICK**: the port 2 joystick is on the right stick, for Robotron: 2084 and Space Dungeon.
* **SWAP PORTS**: for games that read the joystick on port 2 (Wizard of Wor, Apple Panic).
* **JOY 2B+**: multi-button joysticks (EAST = Fire 2).

For paddle games: **CONTROLS > ENABLE PADDLE MODE**, and **PADDLE SPEED** to set the speed.

### Games on several disks

Create an `.m3u` file that lists the disks, one per line, then launch the `.m3u`. With the atari800 core, change disks from the RetroArch menu (**Disc Control**).

### Other useful options

<table><thead><tr><th width="143.25">Emulator</th><th width="247">Option</th><th>Effect</th></tr></thead><tbody><tr><td>atari800 core</td><td><strong>OUTPUT RESOLUTION</strong></td><td>Picture size: <strong>NATIVE (336x240)</strong> or larger, with the borders.</td></tr><tr><td>atari800 core</td><td><strong>VIDEO > VIDEO FORMAT</strong></td><td><strong>NTSC</strong> (default) or <strong>PAL</strong>, for European games.</td></tr><tr><td>atari800 core</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td>Ready-made color palettes (<strong>JAKUB</strong>, <strong>REAL</strong>, <strong>XFORMER</strong>…).</td></tr><tr><td>atari800 core</td><td><strong>VIDEO > ARTIFACTING MODE</strong></td><td>Colors created by TV sets in some high resolution games.</td></tr><tr><td>altirra</td><td><strong>VIDEO > VIDEO STANDARD</strong></td><td>NTSC (default), PAL, SECAM…</td></tr><tr><td>altirra</td><td><strong>VIDEO > CTIA VIDEO CHIP</strong></td><td>Video chip of the first Atari 800s, needed by a few very old games.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="346.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Blue « BOOT ERROR » screen, or the game crashes at boot</td><td>Change the machine (see <a href="atari-800.md#choosing-the-machine"><strong>Choosing the machine</strong></a>). Or add the original ROMs to <code>bios</code> (atari800 core).</td></tr><tr><td>A program shows « READY » or does not start</td><td>It is a BASIC program: turn on <strong>INTERNAL BASIC</strong>. The other way round, a game that shows « READY » instead of starting may need BASIC off.</td></tr><tr><td>A <code>.rom</code> or <code>.bin</code> cartridge does not start</td><td>The cartridge type is guessed wrong. Use the <code>.car</code> version of the game.</td></tr><tr><td>The joystick does not respond in a game</td><td>The game reads port 2: <strong>SWAP PORTS</strong> (atari800 core) or <strong>FORCE USE OF PORT 2</strong> (Altirra).</td></tr><tr><td>Keyboard keys trigger RetroArch hotkeys</td><td>Press <code>Scroll Lock</code> (Game Focus).</td></tr></tbody></table>
