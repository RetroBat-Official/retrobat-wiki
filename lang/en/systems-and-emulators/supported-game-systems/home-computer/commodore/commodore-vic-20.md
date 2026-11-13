---
description: Commodore
---

# Commodore VIC-20

<div align="left"><figure><img src="../../../../.gitbook/assets/image (552).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **VIC-20** was released in 1980 in Japan (as the VIC-1001), then in 1981 in Europe and North America. It was the first personal computer to sell more than one million units. It only has 5 KB of memory and displays 22 columns of text, but its price and simplicity made it the first machine of many players and programmers.

Games were released on cartridge and tape, then on disk. Many programs need a **memory expansion** (3, 8 or 16 KB), which was plugged into the cartridge port. Its library includes arcade conversions such as Gorf, Omega Race or Jupiter Lander. The Commodore 64 replaced it from 1982.

RetroBat emulates the VIC-20 with **VICE**, the reference emulator for Commodore computers.

{% embed url="https://en.wikipedia.org/wiki/VIC-20" %}

## At a glance

<table><thead><tr><th width="254"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\c20</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nib .a0 .b0 .crt .d64 .d81 .prg .tap .t64 .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: vice_xvic</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (vice_xvic)</td></tr></tbody></table>

## Which emulator should I choose?

The VIC-20 has only one emulator in RetroBat.

| Emulator                           | Strengths                                                                                                            | Limitations                                                                                                  |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **libretro: vice\_xvic** (default) | Very accurate emulation, memory expansions, emulated disk and tape drives, virtual keyboard, save states, light pen. | Tape games load slowly, as on the real machine (see [Guides](commodore-vic-20.md#speeding-up-tape-loading)). |

## BIOS

No BIOS is needed: the VIC-20 ROMs are built into VICE.

## Which game format should I use?

<table><thead><tr><th width="186.5">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.crt</strong></td><td>Cartridge in VICE format. Starts immediately.</td></tr><tr><td><strong>.a0</strong>, <strong>.b0</strong></td><td>Raw cartridge image, named after its memory address.</td></tr><tr><td><strong>.prg</strong></td><td>Program only, loaded directly in memory. The fastest to start.</td></tr><tr><td><strong>.d64</strong>, .d81</td><td>Disk image (1541 and 1581 drives).</td></tr><tr><td><strong>.tap</strong></td><td>Tape image. Loading is slow (see <a href="commodore-vic-20.md#speeding-up-tape-loading">Guides</a>).</td></tr><tr><td>.t64</td><td>Tape archive.</td></tr><tr><td>.nib</td><td>Exact image of a copy-protected disk.</td></tr><tr><td>.m3u</td><td>List of the disks or tapes of a game.</td></tr><tr><td>.zip, .7z</td><td>Archive containing one of the formats above.</td></tr></tbody></table>

VICE starts the game by itself: there is no need to type the load command.

## Controls

### Automatic configuration

RetroBat configures the controllers automatically. The VIC-20 has only one joystick port, used by the player 1 controller.

<table><thead><tr><th width="209">RetroBat controller</th><th>VIC-20</th></tr></thead><tbody><tr><td>D-pad</td><td>Joystick</td></tr><tr><td>SOUTH</td><td>Fire</td></tr><tr><td>NORTH</td><td>Space bar</td></tr><tr><td>L2</td><td>RUN/STOP (Escape key)</td></tr><tr><td>R2</td><td>RETURN (Enter)</td></tr><tr><td>SELECT</td><td>Virtual keyboard</td></tr></tbody></table>

Many games ask you to press the space bar, RETURN or a function key to start: use NORTH, R2 or the virtual keyboard.

### Virtual keyboard

**SELECT** shows or hides the virtual keyboard. Move with the D-pad and press a key with **SOUTH**. In the virtual keyboard, **START** types RETURN, **NORTH** the space bar, **WEST** toggles SHIFT LOCK and **EAST** makes the keyboard transparent.

### Keyboard

A keyboard plugged into the PC works as a VIC-20 keyboard. Enable **CONTROLS > KEYBOARD FOCUS** so that the keys do not trigger RetroArch hotkeys. The **Scroll Lock** key turns this mode on or off in game.

### Control options

| Option                                      | Effect                                                      |
| ------------------------------------------- | ----------------------------------------------------------- |
| **CONTROLS > JOYSTICK PORT TYPE**           | Joystick (default), paddles, mouse, light pen or light gun. |
| **CONTROLS > RETROPAD FACE BUTTON OPTIONS** | Changes the fire button, or puts "up" (jump) on a button.   |
| **CONTROLS > PLAYER 1 CONTROLLER TYPE**     | RETROPAD (default), JOYSTICK or KEYBOARD.                   |

### Light guns

The **GUNS > ENABLE GUN** option plugs a light pen into the joystick port. The **JOYSTICK PORT TYPE** option selects another light pen or light gun model.

For more details, see the [**Lightguns**](../../../../controllers/supported-controllers/lightguns/) page.

### Hotkeys

vice\_xvic uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

<table><thead><tr><th width="265.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Save states</td><td><code>saves\c20\libretro.vice_xvic</code></td></tr><tr><td>Save disks created by VICE</td><td><code>saves\c20</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Memory expansion

Many VIC-20 games need a memory expansion. The **EMULATION > MEMORY EXPANSION** option is set to **AUTOMATIC**: VICE selects the expansion from the size of the program.

You can also give the expansion in the file name: `(8k)`, `(16k)`, `[8k]`… For example `My game (16k).prg`. Or select a fixed value in the option (3, 8, 16, 24 or 35 KB).

### Speeding up tape loading

A tape game takes several minutes to load. The **EMULATION > FAST LOAD** option runs the emulation at maximum speed during loading, as long as no sound is played. It also works with disks, if **EMULATION > TRUE DRIVE EMULATION** is enabled.

### Choosing the model and region

The **EMULATION > MODEL TYPE** option selects the emulated machine: VIC-20 PAL or NTSC, or Super VIC (VIC-20 with 16 KB more).

The **Auto** models choose the region from the file name: `NTSC`, `(USA)` or `(Japan)` start the game in NTSC, `PAL` or `(Europe)` in PAL. Without a tag, the region of the selected model is used. The default setting is **VIC-20 PAL Auto**.

### Other useful options

| Option                                    | Effect                                               |
| ----------------------------------------- | ---------------------------------------------------- |
| **VISUAL RENDERING > COLOR PALETTE**      | Colodore (default), Mike, VICE internal palette…     |
| **VISUAL RENDERING > CROP**               | Hides the border around the picture.                 |
| **VISUAL RENDERING > PIXEL ASPECT RATIO** | Shape of the pixels: automatic, PAL, NTSC or square. |

## Known issues

| Issue                                                            | Solution                                                                                                            |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| The game does not start, shows an empty screen or a memory error | It needs another memory expansion: add it to the file name (`(8k)`, `(16k)`…) or select it in **MEMORY EXPANSION**. |
| The game runs too fast or the picture is shifted                 | It is not run in the right region: select a **PAL** or **NTSC** model.                                              |
| The game stays on a loading screen                               | This is normal with a tape: enable **FAST LOAD** or use a `.prg` / `.crt` version.                                  |
| The game asks you to press a key                                 | Use NORTH (space bar), R2 (RETURN) or the virtual keyboard (SELECT).                                                |
