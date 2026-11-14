---
description: Commodore
---

# Commodore 64

<div align="left"><figure><img src="../../../../.gitbook/assets/image (554).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Commodore 64** was released in 1982. It has 64 KB of memory, a graphics chip (VIC-II) handling sprites and scrolling, and above all the **SID** sound chip, whose music left its mark on a whole generation. Its price dropped quickly and it became the best-selling computer in history, with several million units sold until production ended in 1994. A redesigned version, the C64C, was released in 1986.

Its library counts thousands of games on tape, disk and cartridge: Impossible Mission, The Last Ninja, Maniac Mansion, Boulder Dash, Turrican or The Great Giana Sisters. The demo scene is still very active on it.

RetroBat emulates the C64 with **VICE**, the reference emulator for Commodore computers, and with **Frodo**, an older emulator.

{% embed url="https://en.wikipedia.org/wiki/Commodore_64" %}

## At a glance

<table><thead><tr><th width="239"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\c64</code></td></tr><tr><td><strong>Extensions</strong></td><td>.crt .d64 .d71 .d81 .g64 .nib .prg .t64 .tap .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: vice_x64</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores (except frodo)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (vice_x64, vice_x64sc)</td></tr><tr><td><strong>Optional BIOS</strong></td><td>JiffyDOS ROMs in <code>bios\vice</code> (vice_x64, vice_x64sc)</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                          | Strengths                                                                                        | Limitations                                                                |
| --------------------------------- | ------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| **libretro: vice\_x64** (default) | Very compatible and fast, all formats, virtual keyboard, save states, light pens and light guns. | —                                                                          |
| **libretro: vice\_x64sc**         | Cycle-exact emulation: for demos and the rare games that have issues with vice\_x64.             | Needs a bit more power.                                                    |
| **libretro: frodo**               | Lightweight emulator.                                                                            | Only reads `.d64` disks and `.t64` tapes. No save states. Less compatible. |

Keep **vice\_x64** unless a game or a demo does not work: then try **vice\_x64sc**.

## BIOS

No BIOS is needed: the C64 and disk drive ROMs are built into VICE and Frodo.

### JiffyDOS (optional)

**JiffyDOS** is a commercial ROM that replaces the kernal and the disk drive ROM to load disks much faster. It only works with the **vice\_x64** and **vice\_x64sc** cores.

<table><thead><tr><th>File</th><th width="131.5">Folder</th><th>Role</th><th>MD5</th></tr></thead><tbody><tr><td><code>JiffyDOS_C64.bin</code></td><td><code>bios\vice</code></td><td>C64 kernal</td><td>be09394f0576cf81fa8bacf634daf9a2</td></tr><tr><td><code>JiffyDOS_1541-II.bin</code></td><td><code>bios\vice</code></td><td>1541 drive ROM</td><td>1b1e985ea5325a1f46eb7fd9681707bf</td></tr><tr><td><code>JiffyDOS_1571_repl310654.bin</code></td><td><code>bios\vice</code></td><td>1571 drive ROM (optional)</td><td>41c6cc528e9515ffd0ed9b180f8467c0</td></tr><tr><td><code>JiffyDOS_1581.bin</code></td><td><code>bios\vice</code></td><td>1581 drive ROM (optional)</td><td>20b6885c6dc2d42c38754a365b043d71</td></tr></tbody></table>

RetroBat checks these files as optional BIOS. To use JiffyDOS:

1. Put at least `JiffyDOS_C64.bin` and `JiffyDOS_1541-II.bin` in `bios\vice`.
2. Enable the **EMULATION > JIFFYDOS** option. **TRUE DRIVE EMULATION** must stay enabled.

JiffyDOS is only used with disks: it is disabled automatically with tapes and cartridges. If the files are missing, RetroBat starts the game without JiffyDOS.

## Which game format should I use?

<table><thead><tr><th width="134">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.d64</strong></td><td>1541 disk image. The most common format.</td></tr><tr><td><strong>.crt</strong></td><td>Cartridge. Starts immediately.</td></tr><tr><td><strong>.prg</strong></td><td>Program only, loaded directly in memory. The fastest to start (VICE only).</td></tr><tr><td><strong>.tap</strong></td><td>Tape image. Loading is slow (see <a href="commodore-64.md#tape-games">Guides</a>). VICE only.</td></tr><tr><td>.t64</td><td>Tape archive, loaded directly.</td></tr><tr><td>.d71, .d81</td><td>1571 and 1581 drive disks (VICE only).</td></tr><tr><td>.g64, .nib</td><td>Exact images of copy-protected disks (VICE only).</td></tr><tr><td>.m3u</td><td>List of the disks of a game (see <a href="commodore-64.md#games-on-several-disks">Guides</a>).</td></tr><tr><td>.zip, .7z</td><td>Archive containing one of the formats above.</td></tr></tbody></table>

VICE starts the game by itself: there is no need to type `LOAD"*",8,1` then `RUN`.

## Controls

### Automatic configuration

RetroBat configures the controllers automatically. The joystick is plugged into **port 2**, used by most games.

<table><thead><tr><th width="220.25">RetroBat controller</th><th>Commodore 64 (VICE)</th></tr></thead><tbody><tr><td>D-pad</td><td>Joystick</td></tr><tr><td>SOUTH</td><td>Fire</td></tr><tr><td>EAST</td><td>Second fire (rarely used)</td></tr><tr><td>NORTH</td><td>Space bar</td></tr><tr><td>L2</td><td>RUN/STOP (Escape key)</td></tr><tr><td>R2</td><td>RETURN (Enter)</td></tr><tr><td>SELECT</td><td>Virtual keyboard</td></tr></tbody></table>

Many games ask you to press the space bar, RETURN or F1 to start: use NORTH, R2 or the virtual keyboard.

### Virtual keyboard (VICE)

**SELECT** shows or hides the virtual keyboard. Move with the D-pad and press a key with **SOUTH**. In the virtual keyboard, **START** types RETURN, **NORTH** the space bar, **WEST** toggles SHIFT LOCK and **EAST** makes the keyboard transparent.

### Keyboard

A keyboard plugged into the PC works as a C64 keyboard. Enable **CONTROLS > KEYBOARD FOCUS** so that the keys do not trigger RetroArch hotkeys. The **Scroll Lock** key turns this mode on or off in game.

With VICE, the **Right CTRL** key swaps joystick ports 1 and 2 in game.

### Control options (VICE)

<table><thead><tr><th width="327.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>CONTROLS > JOYSTICK PORT</strong></td><td>Port 2 (default) or port 1, for the games that expect the joystick in port 1.</td></tr><tr><td><strong>CONTROLS > JOYSTICK PORT TYPE</strong></td><td>Joystick (default), paddles, mouse, KoalaPad, light pen or light gun.</td></tr><tr><td><strong>CONTROLS > RETROPAD FACE BUTTON OPTIONS</strong></td><td>Changes the fire button, or puts "up" (jump) on a button.</td></tr><tr><td><strong>CONTROLS > PLAYER 1 CONTROLLER TYPE</strong> / <strong>PLAYER 2</strong></td><td>RETROPAD (default), JOYSTICK or KEYBOARD.</td></tr></tbody></table>

### Light guns

With vice\_x64 and vice\_x64sc, the **GUNS > ENABLE GUN** option plugs a light pen or a light gun into port 1, the only C64 port that accepts them. By default, it is a light pen (up trigger). The **JOYSTICK PORT TYPE** option selects another model, for example the **Magnum Light Phaser** or the **Stack Light Rifle**.

For more details, see the [**Lightguns**](../../../../controllers/supported-controllers/lightguns/) page.

### Hotkeys

The libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="332.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Save states</td><td><code>saves\c64\libretro.vice_x64</code>, <code>saves\c64\libretro.vice_x64sc</code></td></tr><tr><td>Save disks created by VICE</td><td><code>saves\c64</code></td></tr><tr><td>Optional VICE files (JiffyDOS, <code>vicerc</code> configuration)</td><td><code>bios\vice</code></td></tr><tr><td>JiffyDOS ROMs, VICE <code>vicerc</code> configuration</td><td><code>bios\vice</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Games on several disks

Create an `.m3u` file that lists the disks in order, one per line:

```
My game (Disk 1).d64
My game (Disk 2).d64
```

Place the `.m3u` and the disks in `roms\c64`. Change disk in game with the [RetroArch hotkeys](../../../../navigation/hotkeys.md) for multi-disk games.

### Tape games

A tape game (`.tap`) takes several minutes to load, as on the real machine. The **EMULATION > FAST LOAD** option runs the emulation at maximum speed during loading, as long as no sound is played. It also works with disks, if **TRUE DRIVE EMULATION** is enabled. The **EMULATION > WARP BOOST** option makes this mode even faster.

When possible, prefer the `.d64`, `.t64` or `.crt` version of the game.

### Choosing the model and region

The **EMULATION > MODEL TYPE** option selects the emulated machine: C64 or C64C, PAL or NTSC, SX-64, C64 Games System…

* The **auto** models choose the region from the file name: `NTSC`, `(USA)` or `(Japan)` start the game in NTSC, `PAL` or `(Europe)` in PAL. Without a tag, the region of the selected model is used. The default setting is **C64 PAL auto**, suited to the vast majority of games, which are European.
* A European game run in NTSC runs too fast and its music is wrong.

### Memory expansion

The **EMULATION > MEMORY EXPANSION** option adds a RAM Expansion Unit (REU) from 128 KB to 16 MB. Only a few recent programs and demos need it.

### Other useful options

| Option                                    | Effect                                                                                     |
| ----------------------------------------- | ------------------------------------------------------------------------------------------ |
| **VISUAL RENDERING > COLOR PALETTE**      | Colodore (default), Pepto, VICE internal palette…                                          |
| **VISUAL RENDERING > CROP**               | Hides the border around the picture.                                                       |
| **VISUAL RENDERING > PIXEL ASPECT RATIO** | Shape of the pixels: automatic, PAL, NTSC or square.                                       |
| **EMULATION > TRUE DRIVE EMULATION**      | Emulates the disk drive exactly (enabled by default). Needed by many copy-protected games. |
| **OUTPUT RESOLUTION** (frodo)             | Resolution of the picture produced by Frodo.                                               |

## Known issues

<table><thead><tr><th width="289">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The joystick does not respond</td><td>The game expects the joystick in the other port: change <strong>JOYSTICK PORT</strong>, or press <strong>Right CTRL</strong> on the keyboard.</td></tr><tr><td>The game runs too fast or the music is wrong</td><td>It is a European game run in NTSC: select a <strong>PAL</strong> model.</td></tr><tr><td>A copy-protected disk does not start</td><td>Check that <strong>TRUE DRIVE EMULATION</strong> is enabled, or use a <code>.g64</code> / <code>.nib</code> image.</td></tr><tr><td>The game stays on a loading screen</td><td>This is normal with a tape: loading takes several minutes. Enable <strong>FAST LOAD</strong> or use a <code>.d64</code> / <code>.t64</code> version.</td></tr><tr><td>A <code>.prg</code> or <code>.tap</code> file does not start with frodo</td><td>Frodo only reads <code>.d64</code> and <code>.t64</code>: use vice_x64.</td></tr><tr><td>The game asks you to press a key</td><td>Use NORTH (space bar), R2 (RETURN) or the virtual keyboard (SELECT).</td></tr></tbody></table>
