---
description: Sony
---

# PlayStation Portable

<div align="left"><figure><img src="../../../../.gitbook/assets/image (557).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **PlayStation Portable** (PSP) is Sony's first handheld console. It was released in December 2004 in Japan, in March 2005 in the United States and in September 2005 in Europe. It stands out with its large 4.3-inch widescreen display (480x272), power close to the PlayStation 2, Wi-Fi and a Sony-specific medium, the **UMD**, a small optical disc in a cartridge.

Several models followed: PSP-1000, PSP Slim & Lite (2000), PSP-3000, the **PSP Go** (2009) with no UMD drive and downloaded games, then the PSP Street (E1000) in 2011. The PSP sold about 80 million units and its production ended in 2014. Notable games include Monster Hunter Freedom Unite, God of War: Chains of Olympus, Crisis Core: Final Fantasy VII, Metal Gear Solid: Peace Walker, Grand Theft Auto: Liberty City Stories, Patapon and LocoRoco.

RetroBat uses **PPSSPP**, a mature open-source emulator that runs almost the whole library, as a standalone emulator or as a libretro core.

{% embed url="https://en.wikipedia.org/wiki/PlayStation_Portable" %}

## At a glance

<table><thead><tr><th width="239"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\psp</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .cso .pbp .elf .prx .chd .zip .7z .squashfs .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>ppsspp</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, PPSSPP</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, PPSSPP</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores (ppsspp)</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="173.25">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>ppsspp</strong> (default)</td><td>Latest PPSSPP version, many settings (hardware texture filters, MSAA, PPSSPP shaders), Vulkan, OpenGL or Direct3D 11.</td><td>No decorations (bezels).</td></tr><tr><td><strong>libretro: ppsspp</strong></td><td>RetroArch features (shaders, decorations, rewind, netplay).</td><td>Fewer settings than the standalone version.</td></tr></tbody></table>

Both versions share the same memory stick (`saves\psp`): game saves, DLC, custom textures and cheat codes are used by both.

## BIOS

The PSP needs no BIOS: PPSSPP emulates the console system itself.

The libretro core uses system files (PSP fonts, compatibility database), provided with RetroBat in `bios\PPSSPP`. There is nothing to add.

### Console language

The game language is the one of the emulated console:

* by default, it is the RetroBat language;
* the **EMULATION > LANGUAGE** option forces a language: English, French, German, Spanish, Italian, Dutch, Portuguese, Japanese, simplified or traditional Chinese, Korean or Russian.

A game that does not exist in the selected language is displayed in its default language, often English.

## Which game format should I use?

<table><thead><tr><th width="214">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.iso</strong></td><td>UMD disc image.</td></tr><tr><td><strong>.cso</strong></td><td>Compressed image, smaller than the ISO.</td></tr><tr><td><strong>.chd</strong></td><td>Compressed image, as for the other disc-based systems.</td></tr><tr><td><strong>.pbp</strong></td><td>Downloaded game (PlayStation Store, PSP Go) or homebrew (<code>EBOOT.PBP</code>).</td></tr><tr><td><strong>.elf</strong>, <strong>.prx</strong></td><td>Homebrews and development programs.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong>, <strong>.squashfs</strong></td><td>Archive of a single game, extracted at launch.</td></tr><tr><td><strong>.decomp</strong></td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

`.cso` and `.chd` are the recommended formats to save space.

PlayStation games sold for the PSP ("PSone Classics", as `.pbp`) are not read by PPSSPP: put them in the PlayStation system (`roms\psx`).

## Controls

### Automatic configuration

RetroBat automatically configures controllers for both emulators. The **AUTOCONFIGURE CONTROLLERS** option disables this configuration to keep the one made in PPSSPP.

<table><thead><tr><th width="266.5">PSP</th><th>Controller</th></tr></thead><tbody><tr><td>Cross</td><td>SOUTH</td></tr><tr><td>Circle</td><td>EAST</td></tr><tr><td>Square</td><td>WEST</td></tr><tr><td>Triangle</td><td>NORTH</td></tr><tr><td>L, R</td><td>L1, R1</td></tr><tr><td>SELECT, START</td><td>SELECT, START</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>Analog stick</td><td>Left stick</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (558).png" alt="" width="225"><figcaption></figcaption></figure></div>

**PPSSPP**:

* The PSP has a single player: up to 4 controllers are configured and all of them control the console.
* PPSSPP reads controllers in three ways: XInput (Xbox controllers), HID (DualShock 4, DualSense, Switch Pro) and DirectInput (other controllers, arcade sticks). The **DRIVERS > ENABLE XINPUT DEVICES**, **ENABLE DIRECTINPUT DEVICES** and **ENABLE HID DEVICES** options are enabled by default. Only disable one if a controller is detected twice or does not respond.
* **CONTROLS > FORCE CONTROLLER INDEX** manually selects player 1's controller, if it is not recognized.
* **CONTROLS > USE O TO CONFIRM (EAST)** confirms with Circle instead of Cross in the system menus, as on Japanese consoles.
* **CONTROLS > USE MOUSE** allows using the mouse in PPSSPP.
* **GAMEPADS BEFORE ARCADE STICKS** gives the first slot to gamepads.

**libretro core**: the **CONTROLS > CONFIRMATION BUTTON** option selects **CROSS** or **CIRCLE** to confirm.

### Hotkeys

**PPSSPP**

| Hotkey                     | Action                     | Keyboard  |
| -------------------------- | -------------------------- | --------- |
| **HOTKEY + START**         | Exit                       | ESC       |
| **HOTKEY + WEST**          | Save state                 | F2        |
| **HOTKEY + NORTH**         | Load state                 | F4        |
| **HOTKEY + UP** / **DOWN** | Next / previous slot       | F7 / F6   |
| **HOTKEY + SOUTH**         | Pause with the PPSSPP menu | F1        |
| **HOTKEY + L3**            | Pause without menu         | P         |
| **HOTKEY + R3**            | Screenshot                 | F8        |
| **HOTKEY + LEFT**          | Rewind (**REWIND** option) | BACKSPACE |
| **HOTKEY + RIGHT**         | Fast forward               | L         |
| —                          | Frame advance              | K         |
| —                          | Fullscreen                 | F         |

These hotkeys can be changed. For more details, see the [**Hotkeys**](../../../../navigation/hotkeys.md#customizing-hotkeys) page.

**libretro core**: the ppsspp core uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

## Folders

| Content                                         | Folder                                                         |
| ----------------------------------------------- | -------------------------------------------------------------- |
| Emulated memory stick, shared by both emulators | `saves\psp`                                                    |
| Game saves                                      | `saves\psp\SAVEDATA`                                           |
| Game DLC and updates                            | `saves\psp\GAME\<game ID>`                                     |
| Custom textures                                 | `saves\psp\TEXTURES\<game ID>`                                 |
| Cheat codes                                     | `saves\psp\Cheats`                                             |
| PPSSPP: save states (managed by RetroBat)       | `saves\psp\ppsspp`                                             |
| PPSSPP: save states (emulator folder)           | `saves\psp\PPSSPP_STATE`                                       |
| PPSSPP: screenshots                             | `saves\psp\SCREENSHOT`                                         |
| PPSSPP: configuration                           | `saves\psp\SYSTEM\ppsspp.ini`, `saves\psp\SYSTEM\controls.ini` |
| libretro: save states                           | `saves\psp\libretro.ppsspp`                                    |
| libretro: core system files                     | `bios\PPSSPP`                                                  |

A game ID (for example `ULES01213`) is shown by PPSSPP in the game information, and on the box or the UMD disc.

## Guides

### DLC and updates

Game DLC and updates go in `saves\psp\GAME`, in a folder named after the game ID, for example `saves\psp\GAME\ULES01213`. Both emulators read them.

### Custom textures

PPSSPP can replace the textures of a game with high-definition textures.

1. Put the texture pack in `saves\psp\TEXTURES`, in a folder named after the game ID (for example `TEXTURES\ULES01213`).
2. Enable the **VISUAL RENDERING > CUSTOM TEXTURES** option.

### Cheat codes

Both emulators read CWCheat codes in `saves\psp\Cheats`, one file per game named after the game ID (for example `ULES01213.ini`).

1. Put the cheat file in `saves\psp\Cheats`. With PPSSPP, you can also put the `cheat.db` database there and import codes from the PPSSPP cheat menu.
2. Enable the **EMULATION > ENABLE CHEATS** option.
3. With PPSSPP, open the in-game menu (**HOTKEY + SOUTH**), then **Cheats**, and tick the codes to use. The libretro core uses the codes marked as active in the file (`_C1` line).

With the libretro core, codes are disabled in RetroAchievements hardcore mode.

### Per-game shaders (PPSSPP)

The **SHADER SET** option applies a PPSSPP shader to all games. For a single game, you can chain several shaders:

1. Next to the game, create a text file with the same name and the `.shaderlist` extension, for example `roms\psp\Patapon.shaderlist` for `Patapon.iso`.
2. Write one PPSSPP shader name per line (for example `FXAA`, then `Vignette`).

This file takes priority over the SHADER SET option.

### Other useful options

**PPSSPP**

<table><thead><tr><th width="341.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Increases the rendering resolution (up to x10). The native resolution is 480x272.</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>16:9 (PSP screen, default), 4:3, 1:1 or <strong>STRETCH</strong>.</td></tr><tr><td><strong>INTEGER SCALING</strong></td><td>Scales the picture by whole numbers only, for sharp pixels.</td></tr><tr><td><strong>EMULATION > REWIND</strong></td><td>Enables rewind (<strong>HOTKEY + LEFT</strong>).</td></tr><tr><td><strong>VIDEO > FRAMESKIP</strong> / <strong>FRAMESKIP TYPE</strong></td><td>Skips frames to gain speed, with a fixed number or automatically.</td></tr><tr><td><strong>VISUAL RENDERING > TEXTURE UPSCALING FILTER</strong> and <strong>TEXTURE UPSCALING</strong></td><td>Smooths upscaled textures. "HARDWARE" filters are faster but only work with Vulkan: RetroBat switches to Vulkan if the video driver is left on default.</td></tr><tr><td><strong>VISUAL RENDERING > ANTI-ALIASING (MSAA)</strong></td><td>Smooths the edges of 3D objects.</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td>VULKAN (default), OPENGL or DIRECT3D 11.</td></tr></tbody></table>

**libretro core**

| Option                                   | Effect                                                                                |
| ---------------------------------------- | ------------------------------------------------------------------------------------- |
| **EMULATION > PERFORMANCE MODE**         | Fast, Balanced or Accurate: sets several speed and accuracy options at once.          |
| **EMULATION > CPU MODE**                 | Recompiler (JIT, default), IR interpreter or interpreter, slower but more compatible. |
| **EMULATION > IGNORE BAD MEMORY ACCESS** | Can fix some crashes.                                                                 |

## Known issues

<table><thead><tr><th width="324">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>A PlayStation game in <code>.pbp</code> does not start</td><td>PPSSPP does not read PlayStation games: put it in <code>roms\psx</code>.</td></tr><tr><td>A controller does not respond, or is detected twice (PPSSPP)</td><td>Disable one of the <strong>DRIVERS > ENABLE XINPUT / DIRECTINPUT / HID DEVICES</strong> options, or select the controller with <strong>FORCE CONTROLLER INDEX</strong>.</td></tr><tr><td>Graphics bugs or black screen</td><td>Change the video driver (<strong>DRIVERS > VIDEO</strong>), or try the other emulator.</td></tr><tr><td>"Core system files missing" message (libretro core)</td><td>The <code>bios\PPSSPP</code> files are missing: reinstall the BIOS files provided with RetroBat.</td></tr><tr><td>The game is not in the right language</td><td>Select the language with <strong>EMULATION > LANGUAGE</strong>.</td></tr><tr><td>Rewind does nothing (PPSSPP)</td><td>Enable <strong>EMULATION > REWIND</strong>.</td></tr><tr><td>Cheat codes do not work</td><td>Enable <strong>ENABLE CHEATS</strong> and tick the codes in the PPSSPP menu. With the libretro core, they are disabled in hardcore mode.</td></tr><tr><td>The game is slow</td><td>Lower the <strong>INTERNAL RESOLUTION</strong>, or use <strong>FRAMESKIP</strong>.</td></tr></tbody></table>
