---
description: Bandai
---

# SuFami Turbo

<div align="left"><figure><img src="../../../../.gitbook/assets/image (736).png" alt="" width="441"><figcaption></figcaption></figure></div>

## Overview

The **Sufami Turbo** is a Bandai adapter released in Japan in June 1996. Plugged into the Super Famicom cartridge slot, it holds two mini-cartridges, sold cheaper than regular games. One is enough to play; with two compatible cartridges, some games share data or unlock bonuses (SD Gundam Generation, SD Ultra Battle).

Thirteen games were released, all in Japan: the SD Gundam Generation series, Poi Poi Ninja World, Crayon Shin-chan: Nagagutsu Dobon!!, Gegege no Kitarou, Sailor Moon Stars: Fuwa Fuwa Panic 2…

Games play like Super Nintendo games: controls, hotkeys and emulator options are described on the [**Super Nintendo**](super-nintendo-entertainment-system-super-famicom.md) page.

{% embed url="https://en.wikipedia.org/wiki/SuFami_Turbo" %}

## At a glance

<table><thead><tr><th width="240.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\sufami</code></td></tr><tr><td><strong>Extensions</strong></td><td>.st .fig .bs .smc .sfc .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: snes9x</td></tr><tr><td><strong>BIOS</strong></td><td><code>STBIOS.bin</code> required</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="166.5">Emulator</th><th width="100.75">For whom?</th><th width="220">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: snes9x</strong> (default)</td><td>Everyone</td><td>Fast and very compatible.</td><td>One cartridge at a time.</td></tr><tr><td><strong>libretro: bsnes-jg</strong></td><td>Purists</td><td>Very accurate bsnes emulation.</td><td>One cartridge at a time.</td></tr><tr><td><strong>ares</strong></td><td>Purists</td><td>Very accurate emulation.</td><td>One cartridge at a time. No RetroAchievements. Save states with hotkeys.</td></tr></tbody></table>

**If in doubt, keep libretro: snes9x.**

## BIOS

Games start through the Sufami Turbo adapter: its content is needed by all emulators.

<table><thead><tr><th width="119">File</th><th width="228">Description</th><th width="81.75">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>STBIOS.bin</code></td><td>Sufami Turbo adapter (Japan)</td><td><code>bios</code></td><td>d3a44ba7d42a74d3ac58cb9c14c6a5ca</td></tr></tbody></table>

This file is required and checked by RetroBat.

## Which game format?

<table><thead><tr><th width="141.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.st</strong></td><td>Image of a Sufami Turbo mini-cartridge.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive).</td></tr></tbody></table>

## Controls

RetroBat automatically configures controllers. Buttons, the **INVERT FACE BUTTONS** option and hotkeys are the same as on the [**Super Nintendo**](super-nintendo-entertainment-system-super-famicom.md#controls) page.

## Folders

<table><thead><tr><th width="302.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores: game saves</td><td><code>saves\sufami</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\sufami\libretro.&#x3C;core></code> (e.g. <code>saves\sufami\libretro.snes9x</code>)</td></tr><tr><td>ares: game saves and save states</td><td><code>saves\sufami\ares</code></td></tr><tr><td>Screenshots</td><td><code>screenshots\ares</code></td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="317.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game doesn't start</td><td>Check that <code>STBIOS.bin</code> is in <code>bios</code>.</td></tr><tr><td>Two-cartridge bonuses don't unlock</td><td>RetroBat loads one cartridge at a time.</td></tr><tr><td>A <code>.bs</code> game doesn't start</td><td>Satellaview games go in <code>roms\satellaview</code>.</td></tr></tbody></table>
