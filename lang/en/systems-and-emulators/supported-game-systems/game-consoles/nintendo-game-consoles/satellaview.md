---
description: Nintendo
---

# Satellaview

<div align="left"><figure><img src="../../../../.gitbook/assets/image (737).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Satellaview** is a Super Famicom add-on released in Japan in 1995, designed by Nintendo with the St.GIGA radio station. Plugged under the console and connected to a satellite dish, it received games, magazines and shows every day, broadcast until 2000.

Games were stored on a memory card (BS Memory Pack), read by the **BS-X** cartridge plugged into the console. Some could only be played at their broadcast time, with live voices and music (SoundLink). Among the best known titles: BS The Legend of Zelda, BS Zelda no Densetsu: Kodai no Sekiban, BS F-Zero Grand Prix, Radical Dreamers, BS Super Mario USA.

Games play like Super Nintendo games: controls, hotkeys and emulator options are described on the [**Super Nintendo**](super-nintendo-entertainment-system-super-famicom.md) page.

{% embed url="https://en.wikipedia.org/wiki/Satellaview" %}

## At a glance

<table><thead><tr><th width="211.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\satellaview</code></td></tr><tr><td><strong>Extensions</strong></td><td>.st .fig .bs .smc .sfc .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: snes9x</td></tr><tr><td><strong>BIOS</strong></td><td><code>BS-X.bin</code> required</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="165.25">Emulator</th><th width="113.25">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: snes9x</strong> (default)</td><td>Everyone</td><td>Fast and very compatible.</td><td>—</td></tr><tr><td><strong>libretro: mesen-s</strong></td><td>Purists</td><td>Accurate Mesen-S emulation.</td><td>—</td></tr><tr><td><strong>libretro: bsnes</strong></td><td>Purists</td><td>Very accurate bsnes emulation.</td><td>More demanding than snes9x.</td></tr><tr><td><strong>ares</strong></td><td>Purists</td><td>Very accurate emulation.</td><td>No RetroAchievements. Save states with hotkeys.</td></tr></tbody></table>

**If in doubt, keep libretro: snes9x.**

## BIOS

Satellaview games start through the BS-X cartridge: its content is needed by all emulators.

<table><thead><tr><th width="107.75">File</th><th width="226">Description</th><th width="77.25">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>BS-X.bin</code></td><td>BS-X cartridge (Japan)</td><td><code>bios</code></td><td>fed4d8242cfbed61343d53d48432aced</td></tr></tbody></table>

This file is required and checked by RetroBat.

## Which game format?

<table><thead><tr><th width="174">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.bs</strong></td><td>Content of a BS Memory Pack (the usual format of Satellaview games).</td></tr><tr><td><strong>.sfc</strong>, <strong>.smc</strong>, <strong>.fig</strong></td><td>Satellaview games converted to a Super Nintendo cartridge (some translations).</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive).</td></tr></tbody></table>

## Controls

RetroBat automatically configures controllers. Buttons, the **INVERT FACE BUTTONS** option and hotkeys are the same as on the [**Super Nintendo**](super-nintendo-entertainment-system-super-famicom.md#controls) page.

## Folders

<table><thead><tr><th width="287.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores: game saves</td><td><code>saves\satellaview</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\satellaview\libretro.&#x3C;core></code> (e.g. <code>saves\satellaview\libretro.snes9x</code>)</td></tr><tr><td>ares: game saves and save states</td><td><code>saves\satellaview\ares</code></td></tr><tr><td>Screenshots</td><td><code>screenshots\ares</code></td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="250.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game doesn't start</td><td>Check that <code>BS-X.bin</code> is in <code>bios</code>.</td></tr><tr><td>A <code>.st</code> game doesn't start</td><td>Sufami Turbo games go in <code>roms\sufami</code>.</td></tr></tbody></table>
