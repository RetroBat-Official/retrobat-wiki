---
description: Atari
---

# Jaguar CD

<div align="left"><figure><img src="../../../../.gitbook/assets/image (546).png" alt="" width="298"><figcaption></figcaption></figure></div>

## Presentation

The **Jaguar CD** is the CD-ROM drive of the Jaguar (see the [**Jaguar**](jaguar.md) page). It came out in September 1995 in the United States and sits on top of the console, in place of the cartridge. Its double-speed drive reads CD games and audio CDs, the latter with visual effects: Jeff Minter's Virtual Light Machine.

Games save on a separate cartridge, the Memory Track, plugged on top of the drive. Arriving late, when the PlayStation and the Saturn already held the market, the Jaguar CD only got about a dozen games, including Myst, Battlemorph, Highlander, Blue Lightning, Primal Rage, Baldies, Dragon's Lair and Space Ace. Atari stopped the Jaguar the following year.

{% embed url="https://en.wikipedia.org/wiki/Atari_Jaguar_CD" %}

## At a glance

<table><thead><tr><th width="220.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\jaguarcd</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .cdi .bigpimg .zip .7z .squashfs</td></tr><tr><td><strong>Default emulator</strong></td><td>bigpemu</td></tr><tr><td><strong>BIOS</strong></td><td>None required</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BigPEmu, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>[BIOS] Atari Jaguar CD (World).j64</code> (libretro: virtualjaguar, with <strong>START ORIGINAL BIOS</strong>)</td></tr></tbody></table>

## Which emulator to choose?

<table><thead><tr><th width="136.5">Emulator</th><th width="179.5">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>bigpemu</strong> (default)</td><td>Everyone</td><td>Runs every Jaguar CD game. Memory Track plugged in automatically, save states, rewind, the whole keypad on the controller. Also reads <code>.bigpimg</code> images.</td><td>No RetroAchievements. Hotkeys on L2 instead of the HOTKEY button.</td></tr><tr><td><strong>libretro: virtualjaguar</strong></td><td>Those who want RetroAchievements or netplay</td><td>Built into RetroArch: shaders, decorations, RetroAchievements, netplay. CD BIOS included in the core, adjustable CD read speed.</td><td>Does not read compressed <code>.cue</code> games (<code>.zip</code>, <code>.7z</code>, <code>.squashfs</code>) or <code>.bigpimg</code>.</td></tr><tr><td><strong>bizhawk</strong> (Jaguar)</td><td>Tool-assisted speedruns (TAS)</td><td>Recording and analysis tools, RetroAchievements.</td><td>Lower CD compatibility. Does not read <code>.cdi</code> or <code>.bigpimg</code>.</td></tr></tbody></table>

**When in doubt, keep BigPEmu. Switch to libretro: virtualjaguar for RetroAchievements.**

## BIOS

No file is needed: BigPEmu and BizHawk do without, and libretro: virtualjaguar includes the CD drive BIOS.

<table><thead><tr><th width="232.75">File</th><th width="220.75">MD5</th><th width="88">Location</th><th>Emulator</th></tr></thead><tbody><tr><td><code>[BIOS] Atari Jaguar CD (World).j64</code> (optional)</td><td><code>77cd95c7ad06a39f4c59995094aa10f9</code></td><td><code>bios</code></td><td>libretro: virtualjaguar</td></tr></tbody></table>

With libretro: virtualjaguar, the **EMULATION > START ORIGINAL BIOS** option boots the game through the real drive BIOS and its animation. The core then uses `[BIOS] Atari Jaguar CD (World).j64` if it is in `bios`, otherwise its built-in copy.

To install BIOS files and check which ones are missing, see the **Adding BIOS files** page.

## Which game format?

<table><thead><tr><th width="181.5">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.cue</strong> (+ .bin)</td><td>The recommended format (Redump dumps). Accepted by all emulators.</td></tr><tr><td>.cdi</td><td>Accepted by BigPEmu and libretro: virtualjaguar, not by BizHawk. Some <code>.cdi</code> dumps are bad: if in trouble, prefer the <code>.cue</code> version.</td></tr><tr><td>.bigpimg</td><td>BigPEmu's own format, read by BigPEmu only.</td></tr><tr><td>.zip, .7z, .squashfs</td><td>The compressed game. BigPEmu and BizHawk decompress it. libretro: virtualjaguar only accepts a <code>.cdi</code> compressed as <code>.zip</code> or <code>.7z</code>.</td></tr></tbody></table>

## Controls

### Automatic configuration

RetroBat configures controllers automatically for all emulators, exactly as for the Jaguar: the A, B, C, Pause and Option buttons and the keypad are placed the same way. The full table and the options (Team Tap, Jaguar Pro controller, left stick) are on the [**Jaguar**](jaguar.md#controls) page.

### Hotkeys

The virtualjaguar libretro core uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page). With BigPEmu, hotkeys use **L2** instead of the HOTKEY button, except for quitting (**HOTKEY + START**). BigPEmu and BizHawk hotkeys are detailed on the [**Jaguar**](jaguar.md#hotkeys) page.

## Folders

<table><thead><tr><th width="352.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>CD BIOS (optional, libretro: virtualjaguar)</td><td><code>bios</code></td></tr><tr><td>libretro core saves (Memory Track)</td><td><code>saves\jaguarcd</code></td></tr><tr><td>BizHawk saves</td><td><code>saves\jaguarcd\bizhawk</code></td></tr><tr><td>libretro core save states</td><td><code>saves\jaguarcd\libretro.virtualjaguar</code></td></tr><tr><td>BigPEmu save states</td><td><code>saves\jaguarcd\bigpemu</code></td></tr><tr><td>BizHawk save states</td><td><code>saves\jaguarcd\bizhawk\sstates\Jaguar</code></td></tr><tr><td>BigPEmu configuration and data (including the Memory Track)</td><td><code>emulators\bigpemu\userdata</code></td></tr><tr><td>libretro core screenshots</td><td><code>screenshots</code></td></tr><tr><td>BizHawk screenshots</td><td><code>screenshots\bizhawk\jaguarcd</code></td></tr><tr><td>libretro core cheat codes</td><td><code>cheats\retroarch</code></td></tr><tr><td>BizHawk cheat codes</td><td><code>cheats\bizhawk\jaguarcd</code></td></tr></tbody></table>

## Guides

### Saving your games (Memory Track)

Jaguar CD games save on the Memory Track cartridge. There is nothing to do:

* **BigPEmu**: RetroBat plugs in the CD drive and the Memory Track every time a game from the Jaguar CD system (or a `.cue` file) is launched.
* **libretro: virtualjaguar**: the core emulates the Memory Track and stores saves in `saves\jaguarcd`.

### Shorter loading times

The real drive is double-speed, and loading can be long. With libretro: virtualjaguar, the **EMULATION > CD READ SPEED** option speeds up reading (**4X**, **8X** or **INSTANT**). Too high a speed can crash some games: go back to **AUTO** (double speed) if there is a problem.

## Known issues

<table><thead><tr><th width="337.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>A compressed <code>.cue</code> game (<code>.zip</code>, <code>.7z</code>, <code>.squashfs</code>) does not start with libretro: virtualjaguar</td><td>Decompress it into <code>roms\jaguarcd</code>, or use BigPEmu.</td></tr><tr><td>A <code>.cdi</code> game does not start or stops on the selection screen (World Tour Racing for example)</td><td>The dump is often bad: use the <code>.cue</code> version (Redump). BizHawk does not read <code>.cdi</code> at all.</td></tr><tr><td>A <code>.bigpimg</code> file does not start</td><td>This format is only read by BigPEmu.</td></tr><tr><td>Loading is long</td><td>With libretro: virtualjaguar, raise <strong>CD READ SPEED</strong>.</td></tr><tr><td>Hotkeys do not respond with BigPEmu</td><td>They use <strong>L2</strong>, not the HOTKEY button.</td></tr><tr><td>A game needs keypad keys 7, 8 or 9</td><td>With libretro: virtualjaguar, turn on <strong>MAP JAGUAR PRO CONTROLLER</strong>, or use BigPEmu, which puts the whole keypad on the controller.</td></tr></tbody></table>
