---
description: Atari
---

# Atari XEGS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (611).png" alt="" width="469"><figcaption></figcaption></figure></div>

## Overview

The **Atari XE Game System** (XEGS) came out in 1987. It is an Atari 65XE shaped as a console: it runs the cartridges and disks of the Atari 8-bit computers, with a detachable keyboard and a light gun, the XG-1. Missile Command is built into the console: it starts when no cartridge is inserted and the keyboard is unplugged.

For the occasion, Atari re-released games from its computers on cartridge, often in new boxes: Ballblazer, Rescue on Fractalus!, Lode Runner, One-on-One Basketball, Archon, Flight Simulator II, Bug Hunt (light gun)… The console was discontinued in 1992.

Games for the Atari 8-bit computers have their own system (see the [**Atari 800**](../../home-computer/atari-computers/atari-800.md) page).

{% embed url="https://en.wikipedia.org/wiki/Atari_XEGS" %}

## At a glance

<table><thead><tr><th width="216.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\xegs</code></td></tr><tr><td><strong>Extensions</strong></td><td>.atr .dsk .xfd .bin .rom .car .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: atari800</td></tr><tr><td><strong>BIOS</strong></td><td>None (MAME: <code>xegs.zip</code>)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; MAME with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>libretro mame core</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="176.5">Emulator</th><th width="128">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: atari800</strong> (default)</td><td>Everyone</td><td>Atari800 7.0 in XEGS mode, built-in operating system (AltirraOS), XEGS keyboard plugged in or not, save states.</td><td>—</td></tr><tr><td><strong>altirra</strong></td><td>Purists</td><td>Altirra, the most accurate Atari 8-bit emulator, with the XEGS profile and the exact choice of cartridge type.</td><td>Only one fire button on the controller. No save states and no RetroBat hotkeys (only HOTKEY + START, to quit).</td></tr><tr><td><strong>libretro: mame</strong></td><td>MAME users</td><td>MAME's XEGS emulation, netplay.</td><td>Needs <code>xegs.zip</code>. Only cartridges from the MAME software list (see <a href="atarixegs.md#which-game-format"><strong>Which game format?</strong></a>).</td></tr><tr><td><strong>mame64</strong> (standalone MAME)</td><td>MAME users</td><td>Same emulation as the libretro mame core.</td><td>Same limits.</td></tr></tbody></table>

**If in doubt, keep libretro: atari800.**

## BIOS

No BIOS is needed with the atari800 core and Altirra: they have a free built-in operating system. MAME needs the console BIOS.

<table><thead><tr><th width="140.25">File</th><th width="149.25">Folder</th><th>MD5</th><th>Used by</th></tr></thead><tbody><tr><td><code>ATARIXL.ROM</code></td><td><code>bios</code></td><td>06daac977823773a3eea3422fd26a703</td><td>atari800 core (XL/XE OS), optional</td></tr><tr><td><code>BB01R4_OS.ROM</code></td><td><code>bios</code></td><td>b7a2a04677d34f069eeb643d5238bf86</td><td>atari800 core (XEGS OS), optional</td></tr><tr><td><code>XEGAME.ROM</code></td><td><code>bios</code></td><td>d7eb37aec6960cba36bc500e0e5d00bc</td><td>atari800 core (built-in Missile Command), optional</td></tr><tr><td><code>xegs.zip</code></td><td><code>bios</code></td><td>—</td><td>MAME (libretro mame core and mame64)</td></tr><tr><td><code>xegs.xml</code></td><td><code>bios\mame\hash</code></td><td>—</td><td>MAME: software list (shipped with RetroBat)</td></tr></tbody></table>

The RetroBat BIOS check lists them all as optional, as the default emulator does not need them. `xegs.zip` comes from the MAME BIOS set of the same version as RetroBat's MAME emulator.

## Which game format?

<table><thead><tr><th width="122">Type</th><th width="179.25">Extensions</th><th>Notes</th></tr></thead><tbody><tr><td>Cartridge</td><td><code>.car</code>, <code>.rom</code>, <code>.bin</code></td><td><code>.car</code> holds the cartridge type. With <code>.rom</code> and <code>.bin</code>, the emulator works it out from the file size.</td></tr><tr><td>Disk</td><td><code>.atr</code>, <code>.xfd</code>, <code>.dsk</code></td><td>The XEGS reads disks with the Atari computers' disk drive.</td></tr></tbody></table>

Files can be compressed as `.zip` or `.7z` (one game per archive).

**With MAME**, RetroBat launches cartridges through the `xegs` software list: the file must have the game's short name in that list (the game name in the MAME `xegs` software set). A renamed cartridge, or one missing from the list, does not start. **EMULATION > FORCE SOFTLIST** and **EMULATION > FORCE MEDIA TYPE** can force the list or the media type.

## Controls

RetroBat configures controllers automatically. The XEGS controller is the one-button Atari joystick. The console's **Start**, **Select** and **Option** keys are on the controller.

| RetroBat controller | libretro: atari800            | altirra                              |
| ------------------- | ----------------------------- | ------------------------------------ |
| D-pad               | Joystick                      | Joystick                             |
| Left stick          | —                             | Joystick (**USE LEFT STICK** option) |
| SOUTH               | Fire                          | Fire                                 |
| EAST                | Fire 2 (two-button joysticks) | —                                    |
| WEST                | Space                         | —                                    |
| NORTH               | Return                        | —                                    |
| START               | Start                         | Start                                |
| SELECT              | Select                        | Select                               |
| L1                  | Option                        | —                                    |
| L2                  | Esc                           | —                                    |
| R2                  | Help                          | —                                    |
| L3                  | Virtual keyboard              | —                                    |

With MAME, controls follow RetroBat's MAME layout: see the [**MAME**](../../arcade/mame.md) page.

RetroBat does not set up the XG-1 light gun (Bug Hunt, Crossbow…) with any emulator.

**CONTROLS > ATTACH XEGS KEYBOARD** (atari800 core, on by default): keyboard plugged in or not. With the keyboard unplugged, the console boots as it does without a keyboard: a few games behave differently.

### Hotkeys

libretro cores use the standard RetroArch hotkeys. Standalone MAME uses the common RetroBat hotkeys. With Altirra, RetroBat only sets HOTKEY + START (quit). See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="319">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\xegs</code></td></tr><tr><td>BIOS</td><td><code>bios</code> (<code>xegs.zip</code> for MAME)</td></tr><tr><td>MAME software list</td><td><code>bios\mame\hash\xegs.xml</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\xegs\libretro.&#x3C;core></code></td></tr><tr><td>atari800 core: engine configuration file</td><td><code>emulators\retroarch\.atari800.cfg</code></td></tr><tr><td>Standalone MAME</td><td>See the <a href="../../arcade/mame.md"><strong>MAME</strong></a> page</td></tr><tr><td>Altirra: configuration</td><td><code>emulators\altirra\Altirra.ini</code></td></tr></tbody></table>

## Guides

### Cartridge type (Altirra)

With a `.rom` or `.bin` cartridge, Altirra chooses the type from the file size (8K, 16K, XEGS 32K to 1M). If the game does not start, choose the type in **EMULATION > SELECT CART**. `.car` cartridges do not need it.

### Other useful options

<table><thead><tr><th width="145.75">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>atari800 core</td><td><strong>VIDEO > VIDEO FORMAT</strong></td><td><strong>NTSC</strong> (default) or <strong>PAL</strong>.</td></tr><tr><td>atari800 core</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td>Ready-made color palettes.</td></tr><tr><td>atari800 core</td><td><strong>CONTROLS > CONTROLLER HACKS</strong></td><td><strong>DUAL STICK</strong>, <strong>SWAP PORTS</strong>, <strong>JOY 2B+</strong> (see the <strong>Atari 800</strong> page).</td></tr><tr><td>altirra</td><td><strong>VIDEO > VIDEO STANDARD</strong></td><td>NTSC (default), PAL, SECAM…</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="334">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>MAME does not start or asks for files</td><td><code>xegs.zip</code> is missing from <code>bios</code>, or the cartridge name is not the one in the <code>xegs</code> software list. Use the atari800 core or Altirra.</td></tr><tr><td>A <code>.rom</code> or <code>.bin</code> cartridge does not start</td><td>Use the <code>.car</code> version, or choose the type in <strong>SELECT CART</strong> (Altirra).</td></tr><tr><td>A light gun game does not respond</td><td>RetroBat does not set up the XG-1 light gun.</td></tr></tbody></table>
