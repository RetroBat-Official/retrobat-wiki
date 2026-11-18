---
description: Nintendo
---

# Family Computer Disk Systems

<div align="left"><figure><img src="../../../../.gitbook/assets/image (622).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Famicom Disk System** is a floppy disk drive that connects under the Famicom, released in Japan in February 1986. Its disks (Disk Cards) hold more data than the cartridges of the time, can save the game and could be rewritten with a new game at kiosks in shops. It also adds a sound channel.

Its library includes the original version of The Legend of Zelda, Metroid, Kid Icarus, Super Mario Bros. 2 (the Japanese sequel), Doki Doki Panic, Akumajō Dracula (Castlevania)… Many of these games were later released on cartridge in the West: these versions go in `roms\nes`.

{% embed url="https://en.wikipedia.org/wiki/Famicom_Disk_System" %}

## At a glance

<table><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\fds</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nes .fds .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: fceumm</td></tr><tr><td><strong>BIOS</strong></td><td><code>disksys.rom</code> required</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; Mesen and ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="137.75">Emulator</th><th width="113.5">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: fceumm</strong> (default)</td><td>Everyone</td><td>Very compatible, RetroAchievements, netplay.</td><td>Manual side change (see <a href="family-computer-disk-system.md#changing-sides"><strong>Changing sides</strong></a>).</td></tr><tr><td><strong>libretro: nestopia</strong></td><td>Everyone</td><td>Very accurate, RetroAchievements, netplay.</td><td>Manual side change.</td></tr><tr><td><strong>libretro: mesen</strong></td><td>Purists</td><td>Very accurate, automatic side change, fast forward while loading, RetroAchievements, netplay.</td><td>—</td></tr><tr><td><strong>mesen</strong></td><td>Mesen users</td><td>Mesen 2: automatic side change, fast forward while loading.</td><td>No RetroAchievements. Save states with hotkeys.</td></tr><tr><td><strong>ares</strong></td><td>Purists</td><td>Very accurate emulation.</td><td>No RetroAchievements. Save states with hotkeys.</td></tr></tbody></table>

**If in doubt, keep libretro: fceumm**, or choose libretro: mesen to avoid changing sides by hand.

## BIOS

<table><thead><tr><th width="125.25">File</th><th width="220.5">Description</th><th width="76.25">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>disksys.rom</code></td><td>Famicom Disk System BIOS</td><td><code>bios</code></td><td>ca30b50f880eb660a320674ed365ef7a</td></tr></tbody></table>

This file is required (all emulators) and checked by RetroBat. For Mesen, RetroBat copies it to `emulators\mesen\Firmware`.

## Which game format?

<table><thead><tr><th width="139">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.fds</strong></td><td>Disk image (all its sides).</td></tr><tr><td><strong>.nes</strong></td><td>Cartridge game, also accepted.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive).</td></tr></tbody></table>

## Controls

Controls are those of the NES: see the [**NES**](nintendo-entertainment-system-family-computer.md#controls) page, **Controls** section (layout, rotated buttons, Xbox layout, turbo).

With the fceumm and nestopia cores, L1 and R1 control the disk drive: see [**Changing sides**](family-computer-disk-system.md#changing-sides).

Hotkeys: see the [**NES**](nintendo-entertainment-system-family-computer.md#hotkeys) page, **Hotkeys** section (Mesen, ares; RetroArch hotkeys for libretro cores).

## Folders

<table><thead><tr><th width="314">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores, Mesen: game saves</td><td><code>saves\fds</code></td></tr><tr><td>libretro cores: save states</td><td><p><code>saves\fds\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\fds\libretro.fceumm</code>)</p></td></tr><tr><td>Mesen: save states</td><td><code>saves\fds\mesen\SaveStates</code></td></tr><tr><td>ares: game saves and save states</td><td><code>saves\fds\ares</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>Screenshots</td><td><code>screenshots\mesen</code>, <code>screenshots\ares</code></td></tr></tbody></table>

## Guides

### Changing sides

Many games ask you to flip the disk ("PLEASE SET DISK CARD SIDE B"):

<table><thead><tr><th width="221.5">Emulator</th><th>How to</th></tr></thead><tbody><tr><td>fceumm core</td><td>R1 ejects the disk, L1 changes the side, R1 inserts it again.</td></tr><tr><td>nestopia core</td><td>L1 changes the side. For a game on two disks, R1 switches to the other disk.</td></tr><tr><td>mesen core, Mesen</td><td>Automatic: <strong>EMULATION > AUTOMATICALLY INSERT DISK</strong> (on by default) changes the side when the game asks for it.</td></tr></tbody></table>

### Faster loading

Disk loading is slow, as on the real console. With Mesen (core or standalone), **EMULATION > FAST FORWARD WHEN LOADING** speeds up emulation during each load.

## Known issues

| Issue                                             | Solution                                                                                   |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| The game does not start, or Mesen asks for a file | Add `disksys.rom` to `bios` (see [**BIOS**](family-computer-disk-system.md#bios)).         |
| The game stays on "SET DISK CARD SIDE B"          | Change the side (see [**Changing sides**](family-computer-disk-system.md#changing-sides)). |
