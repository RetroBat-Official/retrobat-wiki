---
description: Atari
---

# Atari 5200

<div align="left"><figure><img src="../../../../.gitbook/assets/image (634).png" alt="" width="425"><figcaption></figcaption></figure></div>

Game console - Lifespan: 1982 - 1984

{% embed url="https://en.wikipedia.org/wiki/Atari_5200" %}

## At a glance

<table><thead><tr><th width="252.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\atari5200</code></td></tr><tr><td><strong>Extensions</strong></td><td>.a52 .bin .rom .car .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: a5200</td></tr><tr><td><strong>BIOS</strong></td><td><code>5200.rom</code> (optional, recommended)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>libretro a5200 core</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="161.5">Emulator</th><th width="120.5">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: a5200</strong> (default)</td><td>Everyone</td><td>Emulator dedicated to the 5200: keypad on screen or on the buttons, netplay, save states.</td><td>Does not read <code>.car</code> cartridges.</td></tr><tr><td><strong>libretro: atari800</strong></td><td>Alternative</td><td>Atari800 7.0 in 5200 mode: keypad on the buttons, virtual keyboard, save states.</td><td>—</td></tr><tr><td><strong>altirra</strong></td><td>Purists</td><td>Altirra, the most accurate emulator of the Atari 8-bit family, with the exact choice of cartridge type.</td><td>Keypad not available on the controller. No save states and no RetroBat hotkeys (only HOTKEY + START, to quit).</td></tr></tbody></table>

**If in doubt, keep libretro: a5200.**

## BIOS

The BIOS is optional: a5200, atari800 and Altirra have a free built-in operating system (Altirra 5200 OS). The real BIOS is still recommended: it is more compatible. Without it, a5200 shows « Missing BIOS file (5200.rom) - using internal » at launch.

<table><thead><tr><th width="106.5">File</th><th width="77">Folder</th><th width="340.75">MD5</th><th>Used by</th></tr></thead><tbody><tr><td><code>5200.rom</code></td><td><code>bios</code></td><td>281f20ea4320404ec820fb7ec0693b38</td><td>a5200 and atari800 cores</td></tr></tbody></table>

The RetroBat BIOS check lists it as optional. Altirra does not read the `bios` folder: it uses its built-in operating system.

## Which game format?

Games are cartridge images:

* `.a52`, `.bin`, `.rom`: raw images, read by all emulators. The cartridge type is worked out from the file size.
* `.car`: image with a header that holds the cartridge type. Read by atari800 and Altirra, not by a5200.

Files can be compressed as `.zip` or `.7z` (one game per archive).

## Controls

RetroBat configures controllers automatically. The 5200 analog joystick is on the left stick, and also on the D-pad (digital).

<table><thead><tr><th width="169">RetroBat controller</th><th>libretro: a5200</th><th>libretro: atari800</th><th>altirra</th></tr></thead><tbody><tr><td>D-pad</td><td>Joystick</td><td>Joystick</td><td>Joystick</td></tr><tr><td>Left stick</td><td>Analog joystick</td><td>Analog joystick</td><td>Analog joystick</td></tr><tr><td>SOUTH</td><td>Fire 2</td><td>Fire 1</td><td>Fire 2</td></tr><tr><td>EAST</td><td>Fire 1</td><td>Fire 2</td><td>—</td></tr><tr><td>WEST</td><td><code>*</code></td><td><code>#</code></td><td>Fire 1</td></tr><tr><td>NORTH</td><td><code>#</code></td><td><code>*</code></td><td>—</td></tr><tr><td>START</td><td>Start</td><td>Start</td><td>Start</td></tr><tr><td>SELECT</td><td>Pause</td><td>Pause</td><td>Pause</td></tr><tr><td>L1</td><td>On-screen keypad</td><td><code>0</code></td><td>—</td></tr><tr><td>R1</td><td><code>0</code></td><td><code>1</code></td><td>—</td></tr><tr><td>L2</td><td><code>3</code></td><td><code>2</code></td><td>—</td></tr><tr><td>R2</td><td><code>1</code></td><td><code>3</code></td><td>—</td></tr><tr><td>L3</td><td><code>7</code></td><td><code>7</code></td><td>—</td></tr><tr><td>R3</td><td><code>5</code></td><td>Virtual keyboard</td><td>Reset</td></tr></tbody></table>

With a5200, **CONTROLS > CONTROLLER TYPE** sets the L1 role: **JOYSTICK (OSD KEYPAD)** (default) shows the keypad, choose a key with the D-pad and confirm with EAST. **JOYSTICK (DIRECT KEYPAD BUTTONS)** puts the `9` key on L1.

With atari800, **CONTROLS > PLAYER 1 / PLAYER 2 CONTROLLER TYPE** stays on **ATARI5200 JOYSTICK** for the 5200.

### Hotkeys

libretro cores use the standard RetroArch hotkeys. With Altirra, RetroBat only sets HOTKEY + START (quit). See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="349">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\atari5200</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\atari5200\libretro.&#x3C;core></code></td></tr><tr><td>atari800 core: engine configuration file</td><td><code>emulators\retroarch\.atari800.cfg</code></td></tr><tr><td>Altirra: configuration</td><td><code>emulators\altirra\Altirra.ini</code></td></tr></tbody></table>

## Guides

### The keypad

Many 5200 games use the keypad: level, number of players, in-game functions (Star Raiders uses it for views and weapons). With a5200, the on-screen keypad (L1) gives access to all keys. With atari800, the most used keys are on the buttons, and the virtual keyboard (R3) gives the others. With Altirra, use another emulator for these games.

### Dual stick games

Robotron: 2084 and Space Dungeon were played with two controllers side by side. **CONTROLS > INPUT HACK > DUAL STICK** (a5200) or **CONTROLS > CONTROLLER HACKS > DUAL STICK** (atari800) puts the second controller on the right stick. **SWAP PORTS** fixes Wizard of Wor, which reads the controllers the wrong way round.

### Cartridge type (Altirra)

With a raw image, Altirra chooses the type from the file size (4K, 8K, 16K, 32K, Bounty Bob). If the game does not start, choose the type in **EMULATION > SELECT CART** (**5200 16K ONE CHIP** or **TWO CHIPS** for 16K games, **5200 64K SUPERCART**…).

### Other useful options

<table><thead><tr><th width="107">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>a5200</td><td><strong>VISUAL RENDERING > INTERFRAME BLENDING</strong></td><td>Mimics screen ghosting and reduces flicker.</td></tr><tr><td>a5200</td><td><strong>AUDIO > AUDIO FILTER</strong></td><td>Softens the harsh sound of the POKEY chip.</td></tr><tr><td>atari800</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td>Ready-made color palettes.</td></tr><tr><td>altirra</td><td><strong>VIDEO > VIDEO STANDARD</strong></td><td><strong>NTSC</strong> (default) or <strong>NTSC 50</strong>.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="324">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>« Missing BIOS file (5200.rom) » message</td><td>a5200 uses its built-in operating system. Add <code>5200.rom</code> to <code>bios</code> for better compatibility.</td></tr><tr><td>A <code>.car</code> cartridge does not start</td><td>a5200 does not read this format: use atari800 or Altirra.</td></tr><tr><td>The game asks for a keypad key</td><td>a5200: L1 (on-screen keypad). atari800: buttons or virtual keyboard (R3). See <a href="atari-5200.md#the-keypad"><strong>The keypad</strong></a>.</td></tr><tr><td>A 16K game does not start with Altirra</td><td>Choose <strong>5200 16K ONE CHIP</strong> or <strong>TWO CHIPS</strong> in <strong>SELECT CART</strong>.</td></tr></tbody></table>
