---
description: Nintendo
---

# Nintendo 64

<div align="left"><figure><img src="../../../../.gitbook/assets/image (644).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Nintendo 64** is Nintendo's 64-bit home console, released in Japan in June 1996, in North America in September 1996 and in Europe in March 1997. It keeps cartridges and introduces a controller with an analog stick, four controller ports, the Rumble Pak (vibration) and the Expansion Pak (extra memory).

Its library includes Super Mario 64, The Legend of Zelda: Ocarina of Time and Majora's Mask, Mario Kart 64, GoldenEye 007, Perfect Dark, Banjo-Kazooie, Donkey Kong 64, Super Smash Bros., Pokémon Stadium, F-Zero X…

Games for the **64DD** disk drive (Japan only) have their own system in RetroBat, [**Nintendo 64 Disk Drive**](nintendo-64-disk-drive.md) (`roms\n64dd`).

{% embed url="https://en.wikipedia.org/wiki/Nintendo_64" %}

## At a glance

<table><thead><tr><th width="245.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\n64</code></td></tr><tr><td><strong>Extensions</strong></td><td>.v64 .z64 .n64 .zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mupen64plus_next</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, RMG, Gopher64, BizHawk; Project64 and ares with hotkeys; Simple64 from its menu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, Gopher64, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                                  | For whom?                  | Strengths                                                                                                                         | Limits                                                |
| ----------------------------------------- | -------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| **libretro: mupen64plus\_next** (default) | Everyone                   | Very compatible, three graphics engines (GLideN64, ParaLLEl-RDP, Angrylion), HD textures, widescreen, RetroAchievements, netplay. | —                                                     |
| **libretro: parallel\_n64**               | Vulkan graphics card users | Accurate ParaLLEl-RDP rendering by default, easy Transfer Pak, RetroAchievements, netplay.                                        | Vulkan recommended.                                   |
| **mupen64** (RMG)                         | Mupen64Plus users          | Rosalie's Mupen GUI: GLideN64, ParaLLEl or Angrylion, HD textures, Transfer Pak, Raphnet and GameCube adapters.                   | No RetroAchievements.                                 |
| **gopher64**                              | Curious players            | Recent and accurate emulator, RetroAchievements, VRU (Hey You, Pikachu!).                                                         | —                                                     |
| **simple64**                              | Simple64 users             | Accurate ParaLLEl rendering, Raphnet adapter.                                                                                     | No RetroAchievements. Only the Exit hotkey is set up. |
| **ares**                                  | Purists                    | Very accurate emulation.                                                                                                          | No RetroAchievements. Save states with hotkeys.       |
| **bizhawk: Ares64**, **Mupen64Plus**      | BizHawk users              | Two emulations to choose from, RetroAchievements, save states in the RetroBat menu.                                               | —                                                     |
| **project64**                             | Project64 users            | Historic Windows emulator, HD textures, Raphnet adapter.                                                                          | No RetroAchievements. Save states with hotkeys.       |

**If in doubt, keep libretro: mupen64plus\_next.**

## BIOS

The Nintendo 64 has no BIOS: no file is needed.

## Which game format?

<table><thead><tr><th width="160.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.z64</strong></td><td>Cartridge image, in the original byte order.</td></tr><tr><td><strong>.v64</strong>, <strong>.n64</strong></td><td>Same content, with the bytes in another order (copiers of the time): emulators read them too.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive).</td></tr><tr><td><strong>.decomp</strong></td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

## Controls

RetroBat sets up the controllers automatically for all emulators, up to four players. Default layout:

| RetroBat controller | Nintendo 64 |
| ------------------- | ----------- |
| Left stick          | Stick       |
| D-pad               | D-pad       |
| SOUTH               | A           |
| WEST                | B           |
| L2                  | Z           |
| L1 / R1             | L / R       |
| Right stick         | C buttons   |
| START               | START       |

With a controller without triggers (L2 / R2), Z moves to L1 (libretro cores).

Each emulator offers several layouts:

| Emulators                          | Option                                      | Layouts                                                                                                                                                                        |
| ---------------------------------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| libretro cores                     | **CONTROLS > BUTTON LAYOUT**                | **STANDARD** (default), **XBOX**                                                                                                                                               |
| ares, BizHawk                      | **CONTROLS > CONTROLLER LAYOUT**            | **Z=LEFT-TRIGGER** (default), **Z=RIGHT-TRIGGER**, **XBOX**                                                                                                                    |
| RMG, Project64, Simple64, Gopher64 | **CONTROLS > CONTROLLER LAYOUT P1** (to P4) | **C-BUTTONS=RIGHT-STICK Z=LEFT-TRIGGER** (default), **C-BUTTONS=FACE Z=LEFT-TRIGGER**, **C-BUTTONS=RIGHT-STICK Z=RIGHT-TRIGGER**, **C-BUTTONS=FACE Z=RIGHT-TRIGGER**, **XBOX** |

| Layout                                                          | Diagram                                                                                                                                             |
| --------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| libretro cores, **STANDARD**                                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64.png?raw=true" alt="" data-size="original">                    |
| Other emulators, default layout                                 | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" data-size="original">         |
| **Z=RIGHT-TRIGGER** / **C-BUTTONS=RIGHT-STICK Z=RIGHT-TRIGGER** | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_zr.png?raw=true" alt="" data-size="original">      |
| **C-BUTTONS=FACE Z=LEFT-TRIGGER**                               | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_face_zl.png?raw=true" alt="" data-size="original"> |
| **C-BUTTONS=FACE Z=RIGHT-TRIGGER**                              | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_face_zr.png?raw=true" alt="" data-size="original"> |
| **XBOX** (all emulators)                                        | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64_xbox.png?raw=true" alt="" data-size="original">               |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (646).png" alt=""><figcaption></figcaption></figure></div>

### Hotkeys

libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

ares, BizHawk and Project64 use the RetroBat hotkeys:

| Action               | Controller         | Keyboard    |
| -------------------- | ------------------ | ----------- |
| Exit                 | HOTKEY + START     | `Esc`       |
| Pause                | HOTKEY + SOUTH     | `P`         |
| Save state           | HOTKEY + WEST      | `F2`        |
| Load state           | HOTKEY + NORTH     | `F4`        |
| Previous / next slot | HOTKEY + Down / Up | `F6` / `F7` |
| Rewind (if enabled)  | HOTKEY + Left      | `Backspace` |
| Fast forward (hold)  | HOTKEY + Right     | `L`         |
| Screenshot           | HOTKEY + R3        | `F8`        |
| Fullscreen           | HOTKEY + L3        | `F`         |

Project64 has no hotkey to change the slot.

RMG (mupen64) has its own hotkeys, on the SELECT button:

| Action                  | Controller                 | Keyboard |
| ----------------------- | -------------------------- | -------- |
| Exit                    | SELECT + START             | `Esc`    |
| Pause                   | SELECT + SOUTH             | `P`      |
| Save state              | SELECT + WEST              | `F2`     |
| Load state              | SELECT + NORTH             | `F4`     |
| Previous / next slot    | SELECT + Down / Up         |          |
| Speed 50% / 100% / 250% | SELECT + Left / L1 / Right |          |
| Screenshot              | SELECT + R3                | `F8`     |
| Fullscreen              | SELECT + L3                |          |

Gopher64:

| Action                | Controller     | Keyboard           |
| --------------------- | -------------- | ------------------ |
| Exit                  | HOTKEY + START | `Esc` (fullscreen) |
| Pause                 | HOTKEY + SOUTH | `Alt` + `P`        |
| Save state            | HOTKEY + WEST  | `F5`               |
| Load state            | HOTKEY + NORTH | `F7`               |
| Rewind (if enabled)   | HOTKEY + Left  | `F6`               |
| Fast forward (toggle) | HOTKEY + Right | `Alt` + `F`        |

With Simple64, only HOTKEY + START (exit) is set up: save states are made from its menu.

## Folders

<table><thead><tr><th width="310.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores: game saves</td><td><code>saves\n64</code></td></tr><tr><td>libretro cores: save states</td><td><p><code>saves\n64\libretro.&#x3C;core></code> </p><p>(e.g. <code>saves\n64\libretro.mupen64plus_next</code>)</p></td></tr><tr><td>RMG, Simple64: game saves</td><td><code>saves\n64\sram</code></td></tr><tr><td>RMG: save states</td><td><code>saves\n64\mupen64</code></td></tr><tr><td>Simple64: save states</td><td><code>saves\n64\state</code></td></tr><tr><td>Gopher64: game saves and save states</td><td><code>saves\n64\gopher64</code></td></tr><tr><td>Project64: game saves and save states</td><td><p><code>saves\n64\project64</code></p><p><code>saves\n64\project64\sstates</code></p></td></tr><tr><td>ares: game saves and save states</td><td><code>saves\n64\ares</code></td></tr><tr><td>BizHawk: game saves</td><td><code>saves\n64\bizhawk</code></td></tr><tr><td>HD textures</td><td><code>bios\Mupen64plus\hires_texture</code> and <code>bios\Mupen64plus\cache</code> (mupen64plus_next core, RMG), <code>saves\n64\project64\hires_texture</code> (Project64)</td></tr><tr><td>Recognized N64 controllers</td><td><code>system\resources\inputmapping\n64Controllers.json</code></td></tr><tr><td>Screenshots</td><td><p><code>screenshots\mupen64</code></p><p><code>screenshots\Simple64</code></p><p><code>screenshots\project64</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\n64</code></p></td></tr></tbody></table>

## Guides

### Using an N64 controller

RetroBat recognizes these controllers and applies a suitable layout (libretro cores, RMG, Simple64, ares, BizHawk):

* Nintendo Switch Online N64 controller;
* 8BitDo N64 controller;
* original controller with the Mayflash or Raphnet adapter;
* N64-style USB controllers detected as "SWITCH CO.LTD. Usb Controller".

If the layout is not applied, enable **CONTROLS > USE N64-LIKE CONTROLLER**. For a controller with two triggers, **SPECIAL CONTROLLERS > N64 TRIGGER INVERT** puts Z on the right trigger.

{% hint style="info" %}
With the Mayflash adapter, plug the controllers from right to left: controller 1 is the one in port 4 (or port 2 on a two-controller adapter).
{% endhint %}

Another controller can be added to `n64Controllers.json`.

**Raphnet adapter in direct access** (the original controller is read without conversion):

<table><thead><tr><th width="169">Emulator</th><th>Option</th></tr></thead><tbody><tr><td>RMG</td><td><strong>DRIVERS > INPUT > RAPHNET ADAPTATOR</strong></td></tr><tr><td>Simple64</td><td><strong>DRIVERS > INPUT > RAPHNET ADAPTATOR</strong></td></tr><tr><td>Project64</td><td><strong>DRIVERS > USE RAPHNET ADAPTER</strong></td></tr></tbody></table>

RMG also accepts the official GameCube adapter: **DRIVERS > INPUT > GAMECUBE ADAPTER**.

### Controller extensions (Controller Pak, Rumble Pak, Transfer Pak)

The N64 controller takes one extension: memory card (Controller Pak), vibration (Rumble Pak) or Transfer Pak, which reads a Game Boy cartridge (Pokémon Stadium 1 and 2, Mario Golf, Mario Tennis, Perfect Dark). Choose it per player:

| Emulator               | Option                                          | Choices                                                              |
| ---------------------- | ----------------------------------------------- | -------------------------------------------------------------------- |
| mupen64plus\_next core | **EMULATION > P1 CONTROLLER EXTENSION** (to P4) | **MEMORY** (player 1 default), **RUMBLE**, **TRANSFER**              |
| parallel\_n64 core     | **CONTROLS > P1 CONTROLLER EXTENSION** (to P4)  | **MEMORY**, **RUMBLE PACK**, **TRANSFER**, **BIO SENSOR** (player 1) |
| RMG                    | **CONTROLS > P1 CONTROLLER EXTENSION** (to P4)  | **MEMORY PACK**, **RUMBLE PACK**, **TRANSFER PACK** (player 1)       |
| Simple64               | **CONTROLS > P1 CONTROLLER EXTENSION** (to P4)  | **MEMORY** (default), **RUMBLE PACK**, **TRANSFER PACK**             |
| BizHawk                | **CONTROLS > P1 CONTROLLER EXTENSION** (to P4)  | **MEMORY**, **RUMBLE PACK**                                          |

**Transfer Pak:**

* **parallel\_n64 core**: put the Game Boy cartridge (`.gb` or `.gbc`) and its save (`.sav`) next to the N64 game, with the same name.
* **RMG**: choose **TRANSFER PACK** for player 1, then **TRANSFER PACK SYSTEM** (GB or GBC). In **TRANSFER PACK ROM** and **TRANSFER PACK SAVE FILE**, type the first characters of the cartridge name (searched in `roms\gb` or `roms\gbc`) and of its save (searched in `saves\gb` or `saves\gbc`).

### Expansion Pak

The Expansion Pak doubles the console memory. Donkey Kong 64 and The Legend of Zelda: Majora's Mask require it, other games use it for a better picture. It is on by default. Only turn it off if a game asks for it: **EMULATION > DISABLE EXPANSION PACK** (Gopher64), **DISABLE 4MB RAM PACK** (Simple64), **ENABLE 4MB RAM PACK** (ares).

### Graphics engine and resolution

| Emulator                 | Option                                                                                       | Effect                                                                                                                                                                |
| ------------------------ | -------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| mupen64plus\_next core   | **EMULATION > GFX PLUGIN**                                                                   | **GLIDEN64 (HLE)**: fast, enhancements (resolution, HD textures); **PARALLEL-RDP (LLE)**: accurate, needs Vulkan; **ANGRYLION (SOFTWARE)**: very accurate, very slow. |
| mupen64plus\_next core   | **GLIDE PLUGIN > INTERNAL RESOLUTION**, **PARALLEL PLUGIN > INTERNAL RESOLUTION (PARALLEL)** | Render resolution of each engine.                                                                                                                                     |
| parallel\_n64 core       | **VIDEO > GFX PLUGIN**                                                                       | ParaLLEl-RDP by default (Vulkan); GLideN64, Angrylion, Glide64, glN64, Rice.                                                                                          |
| RMG                      | **DRIVERS > GFX PLUGIN** and **INTERNAL RESOLUTION**                                         | GLideN64, ParaLLEl or Angrylion.                                                                                                                                      |
| Gopher64, Simple64, ares | **INTERNAL RESOLUTION** / **VIDEO > QUALITY**                                                | Render resolution.                                                                                                                                                    |

### Widescreen

Some games show in 16:9 with a hack (2D games are stretched):

| Emulator               | Option                                                                               |
| ---------------------- | ------------------------------------------------------------------------------------ |
| mupen64plus\_next core | **VISUAL RENDERING > WIDESCREEN HACK** (**ADJUSTED (16:9)** or **STRETCHED (16:9)**) |
| parallel\_n64 core     | **VIDEO > WIDESCREEN HACK**                                                          |
| RMG                    | **GAME ASPECT RATIO > 16:9**                                                         |
| Gopher64, Simple64     | **VIDEO > STRETCH TO SCREEN**                                                        |

Bezels are turned off with these settings (mupen64plus\_next core, RMG).

### HD textures

Texture packs replace the original textures.

| Emulator               | Folder                                                                                                 | Option                                                                                                 |
| ---------------------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| mupen64plus\_next core | `bios\Mupen64plus\cache` (`.htc` / `.hts` packs), `bios\Mupen64plus\hires_texture` (folders of `.png`) | **VISUAL RENDERING > CUSTOM TEXTURES**: **RICE** for `.htc` / `.hts`, **CACHE** for a folder of `.png` |
| RMG                    | `bios\Mupen64plus\hires_texture`                                                                       | **VISUAL RENDERING > CUSTOM TEXTURES**                                                                 |
| Project64              | `saves\n64\project64\hires_texture`                                                                    | **VISUAL RENDERING > CUSTOM TEXTURES**                                                                 |

The pack is named after the internal game name: for example `MARIOKART64_HIRESTEXTURES.htc`, or a `MARIOKART64` folder. With mupen64plus\_next, a folder pack is converted to `.hts` in `cache` at the first launch: then choose **RICE**, the game starts faster.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (645).png" alt=""><figcaption></figcaption></figure></div>

### Other useful options

| Emulator                    | Option                               | Effect                                                            |
| --------------------------- | ------------------------------------ | ----------------------------------------------------------------- |
| mupen64plus\_next core      | **EMULATION > PERFORMANCE MODE**     | Faster, but less accurate and with more latency.                  |
| mupen64plus\_next core, RMG | **VISUAL RENDERING > CROP OVERSCAN** | Hides the black borders around the picture (depends on the game). |
| Gopher64                    | **CONTROLS > EMULATE VRU**           | Microphone of Hey You, Pikachu! and Densha de GO! 64.             |
| Gopher64                    | **EMULATION > OVERCLOCK CPU**        | Smoother in games that slow down.                                 |

## Known issues

| Issue                                             | Solution                                                                                                                                                             |
| ------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Black screen or crash with ParaLLEl-RDP           | This engine needs a Vulkan-compatible graphics card: choose GLideN64.                                                                                                |
| Donkey Kong 64 or Majora's Mask does not start    | Check that the Expansion Pak is not turned off.                                                                                                                      |
| No vibration                                      | Choose the Rumble Pak in **P1 CONTROLLER EXTENSION** (see [**Controller extensions**](nintendo-64.md#controller-extensions-controller-pak-rumble-pak-transfer-pak)). |
| The N64 controller does not have the right layout | See [**Using an N64 controller**](nintendo-64.md#using-an-n64-controller).                                                                                           |
| A `.ndd` game does not show up                    | 64DD games go in `roms\n64dd`.                                                                                                                                       |
