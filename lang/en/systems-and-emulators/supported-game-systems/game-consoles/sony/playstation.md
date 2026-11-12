---
description: Sony
---

# PlayStation

<div align="left"><figure><img src="../../../../.gitbook/assets/image (494).png" alt=""><figcaption></figcaption></figure></div>

## Presentation

The **PlayStation** was released in December 1994 in Japan, then in 1995 in the United States and Europe. It was born from a CD drive project for the Super Nintendo, dropped by Nintendo and taken over by Sony to make its own console.

With its CD-ROM games and 3D graphics, it changed the face of video games and attracted an older audience. It sold more than 100 million units. Final Fantasy VII, Gran Turismo, Metal Gear Solid, Tekken, Resident Evil and Crash Bandicoot started there. The DualShock controller, with its two analog sticks and rumble, arrived in 1997.

{% embed url="https://en.wikipedia.org/wiki/PlayStation_(console)" %}

## At a glance

<table><thead><tr><th width="239"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\psx</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .img .mdf .pbp .toc .cbn .m3u .ccd .chd .zip .7z .iso .cso .squashfs .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mednafen_psx_hw</td></tr><tr><td><strong>BIOS</strong></td><td><code>psxonpsp660.bin</code> (or <code>ps1_rom.bin</code>, or <code>scph5500.bin</code>, <code>scph5501.bin</code>, <code>scph5502.bin</code>)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, DuckStation, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, DuckStation, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores (mednafen_psx_hw, pcsx_rearmed)</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores, DuckStation, Mednafen</td></tr></tbody></table>

## Which emulator to choose?

| Emulator                                  | For whom?                                   | Strengths                                                                                                          | Limits                           |
| ----------------------------------------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------- |
| **libretro: mednafen\_psx\_hw** (default) | Everyone                                    | Very compatible, increased resolution, perspective correction (PGXP), custom textures, RetroAchievements, netplay. | Heavier than the other cores.    |
| **duckstation**                           | Those who prefer a standalone emulator      | Fast, many graphical enhancements, RetroAchievements, rewind.                                                      | No netplay.                      |
| **libretro: swanstation**                 | Those who want DuckStation inside RetroArch | Derived from DuckStation, with RetroAchievements.                                                                  | No netplay.                      |
| **libretro: pcsx\_rearmed**               | Low-end PCs                                 | Light, with RetroAchievements and netplay.                                                                         | Fewer graphical enhancements.    |
| **mednafen**                              | Accuracy seekers                            | Accurate emulation.                                                                                                | No `.chd`, no RetroAchievements. |
| **bizhawk** (Nymashock, Octoshock)        | Tool-assisted speedrun (TAS)                | Recording and analysis tools.                                                                                      | No `.chd`.                       |

**If in doubt, keep libretro: mednafen\_psx\_hw.**

## BIOS

A BIOS is required. RetroBat looks for the files at the root of the `bios` folder, in this order:

<table><thead><tr><th width="69">Order</th><th width="156.5">File</th><th width="216">Origin</th><th>MD5</th></tr></thead><tbody><tr><td>1</td><td><code>psxonpsp660.bin</code></td><td>PlayStation BIOS from the PSP, all regions</td><td><code>c53ca5908936d412331790f4426c6c33</code></td></tr><tr><td>2</td><td><code>ps1_rom.bin</code></td><td>PlayStation BIOS from the PS3, all regions</td><td><code>81bbe60ba7a3d1cea1d48c14cbcc647b</code></td></tr><tr><td>3</td><td><code>scph5500.bin</code></td><td>Japanese PlayStation</td><td><code>8dd7d5296a650fac7319bce665a6a53c</code></td></tr><tr><td>3</td><td><code>scph5501.bin</code></td><td>American PlayStation</td><td><code>490f666e1afb15b7362b406ed1cea246</code></td></tr><tr><td>3</td><td><code>scph5502.bin</code></td><td>European PlayStation</td><td><code>32736f17079d0b2b7024407c39bd3050</code></td></tr></tbody></table>

* One file is enough: `psxonpsp660.bin` works for all regions.
* With the `scph` files, you need the one matching the region of the game.
* The **EMULATION > USE SCPH LEGACY BIOS** option forces the use of the `scph` files (mednafen\_psx\_hw, swanstation, Mednafen, BizHawk).
* DuckStation picks one of the BIOS files in the `bios` folder by itself. The **EMULATION > FORCE BIOS** option imposes one.
* pcsx\_rearmed can start without a BIOS, but with lower compatibility.
* With the libretro cores, the **EMULATION > OVERRIDE BIOS PATH** option makes RetroArch look for the BIOS files in another folder.

The **SKIP BIOS** option skips the console boot animation.

## Which game format?

<table><thead><tr><th width="281.5">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.chd</strong></td><td>Recommended: a single compressed file per disc. Not supported by Mednafen and BizHawk.</td></tr><tr><td><strong>.cue</strong> (+ <code>.bin</code>)</td><td>Classic image. Launch the <code>.cue</code> and keep the <code>.bin</code> files next to it.</td></tr><tr><td>.pbp</td><td>Format of PlayStation games on the PSP. Can hold several discs.</td></tr><tr><td>.m3u</td><td>List of the discs of a multi-disc game (see <a href="playstation.md#multi-disc-games">Guides</a>).</td></tr><tr><td>.iso .img .mdf .ccd .toc .cbn .cso</td><td>Other disc images.</td></tr><tr><td>.zip .7z .squashfs</td><td>Compressed game, extracted or mounted before launch.</td></tr><tr><td>.decomp</td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong> page</a>.</td></tr></tbody></table>

## Controls

### Automatic configuration

RetroBat configures controllers automatically for all emulators. Buttons are placed as on the PlayStation controller: **SOUTH** = Cross, **EAST** = Circle, **WEST** = Square, **NORTH** = Triangle.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (495).png" alt="" width="225"><figcaption></figcaption></figure></div>

Useful options, in **CONTROLS**:

| Option                               | Effect                                                                                                                                                         |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **PLAYER 1 CONTROLLER TYPE** (to 4)  | Emulated controller: digital, DualShock, neGcon, mouse… Some old games only recognize the digital controller.                                                  |
| **USE TRIGGERS TO BRAKE/ACCELERATE** | <p>Puts throttle and brake on the triggers (Gran Turismo…).<br><img src="../../../../.gitbook/assets/image (496).png" alt=""></p>                              |
| **FORCE ANALOG STICKS**              | mednafen\_psx\_hw: keeps the DualShock in analog mode.                                                                                                         |
| **ANALOG/DIGITAL TOGGLE COMBO**      | mednafen\_psx\_hw, swanstation: button combination that switches the DualShock between analog and digital (L1 + R1 + START by default with mednafen\_psx\_hw). |

With DuckStation, the **Guide** button of the controller is the Analog button.

**Multitap**: with the libretro cores and DuckStation, it is enabled automatically on port 1 from 3 controllers, and on both ports from 6. With mednafen\_psx\_hw and swanstation, it is disabled when light guns are enabled. With Mednafen, set **CONTROLS > USE MULTITAP**.

### Light guns

Turn on **GUNS > ENABLE GUN**: the trigger is on the left click, button A on the right click and button B on the middle click. The emulated gun is the GunCon. For the Justifier: **GUN TYPE** with mednafen\_psx\_hw and Mednafen, **PLAYER 1 CONTROLLER TYPE** set to **JUSTIFIER** with DuckStation.

With DuckStation, **MAP GUN TO PLAYER 2** plugs the GunCon into port 2, as Die Hard Trilogy requires.

### Hotkeys

Hotkeys are on the same buttons with all emulators.

| Action                     | libretro cores     | DuckStation        | Mednafen           | BizHawk            | Keyboard (DuckStation, BizHawk) |
| -------------------------- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------------------- |
| **Quit**                   | HOTKEY + START     | HOTKEY + START     | HOTKEY + START     | HOTKEY + START     | ESC                             |
| Save state                 | HOTKEY + WEST      | HOTKEY + WEST      | HOTKEY + WEST      | HOTKEY + WEST      | F2                              |
| Load state                 | HOTKEY + NORTH     | HOTKEY + NORTH     | HOTKEY + NORTH     | HOTKEY + NORTH     | F4                              |
| Next / previous slot       | HOTKEY + UP / DOWN | HOTKEY + UP / DOWN | HOTKEY + UP / DOWN | HOTKEY + UP / DOWN | F7 / F6                         |
| Screenshot                 | HOTKEY + R3        | HOTKEY + R3        | HOTKEY + R3        | HOTKEY + R3        | F8                              |
| Rewind                     | HOTKEY + LEFT      | HOTKEY + LEFT      | HOTKEY + LEFT      | HOTKEY + LEFT      | BACKSPACE                       |
| Fast forward               | HOTKEY + RIGHT     | HOTKEY + RIGHT     | HOTKEY + RIGHT     | HOTKEY + RIGHT     | L                               |
| Emulator menu              | HOTKEY + SOUTH     | HOTKEY + SOUTH     | —                  | —                  | F1 (DuckStation)                |
| Pause                      | —                  | HOTKEY + L3        | HOTKEY + SOUTH     | HOTKEY + SOUTH     | P                               |
| Fullscreen                 | —                  | —                  | HOTKEY + L3        | HOTKEY + L3        | F                               |
| Open / close the disc tray | HOTKEY + L1        | —                  | HOTKEY + L1        | —                  | —                               |
| Select the disc            | —                  | HOTKEY + R1        | HOTKEY + R2        | —                  | F11 (DuckStation)               |
| Previous / next disc       | HOTKEY + L2 / R2   | HOTKEY + L2 / R2   | —                  | —                  | F9 / F10 (DuckStation)          |

## Folders

| Content                           | Folder                                                     |
| --------------------------------- | ---------------------------------------------------------- |
| Games                             | `roms\psx`                                                 |
| BIOS                              | `bios`                                                     |
| Memory cards of libretro cores    | `saves\psx`                                                |
| DuckStation memory cards          | `saves\psx\duckstation\memcards`                           |
| Mednafen memory cards             | `saves\psx` (backup copies in `saves\psx\mednafen\backup`) |
| BizHawk memory cards              | `saves\psx\bizhawk`                                        |
| Save states of libretro cores     | `saves\psx\libretro.<core>`                                |
| DuckStation save states           | `saves\psx\duckstation`                                    |
| BizHawk save states               | `saves\psx\bizhawk\sstates\<core>`                         |
| Mednafen save states              | `saves\psx\mednafen\sstates`                               |
| mednafen\_psx\_hw custom textures | `roms\psx\<game file name>-texture-replacements`           |
| DuckStation custom textures       | `emulators\duckstation\textures\<game ID>\replacements`    |
| Cheats of libretro cores          | `cheats\retroarch`                                         |
| DuckStation cheats                | `cheats\duckstation`                                       |
| Mednafen cheats                   | `cheats\mednafen`                                          |
| BizHawk cheats                    | `cheats\bizhawk\psx`                                       |
| Screenshots of libretro cores     | `screenshots`                                              |
| DuckStation screenshots           | `screenshots\duckstation`                                  |
| Mednafen screenshots              | `screenshots\mednafen`                                     |
| BizHawk screenshots               | `screenshots\bizhawk\psx`                                  |
| DuckStation per-game settings     | `emulators\duckstation\gamesettings`                       |
| DuckStation patches               | `emulators\duckstation\patches`                            |
| DuckStation covers                | `emulators\duckstation\covers`                             |
| DuckStation configuration         | `emulators\duckstation\settings.ini`                       |

Each emulator has its own memory cards: a save made with one does not show up in another.

Only mednafen\_psx\_hw and DuckStation support custom textures.

## Guides

### Multi-disc games

1. Put all the discs of the game in `roms\psx`.
2. Create a text file named after the game with the `.m3u` extension, for example `Final Fantasy VII.m3u`.
3. Write the name of each disc in it, one per line:

```
Final Fantasy VII (Disc 1).chd
Final Fantasy VII (Disc 2).chd
Final Fantasy VII (Disc 3).chd
```

4. Launch the `.m3u` file. When the game asks for the next disc, use the disc change hotkeys.

With libretro cores: **HOTKEY + L1** opens the tray, **HOTKEY + R2** selects the next disc, **HOTKEY + L1** closes the tray.

With the `.m3u` file, the same memory card is used for all discs.

### Memory cards: one per game or one for all

| Emulator          | Default                                 | Option                             |
| ----------------- | --------------------------------------- | ---------------------------------- |
| DuckStation       | One card per game                       | **EMULATION > MEMORY CARD TYPE**   |
| mednafen\_psx\_hw | One card per game                       | **EMULATION > USE SHARED MEMCARD** |
| swanstation       | One card per game, handled by RetroArch | **EMULATION > MEMORY CARD 1 TYPE** |

A shared card lets games that read the saves of another game find them.

### Custom textures

Two emulators load texture packs, each with its own pack format and its own folder.

**libretro: mednafen\_psx\_hw**

1. In `roms\psx`, create a folder named after the game file followed by `-texture-replacements`. For `My game.chd`, the folder is `My game-texture-replacements`.
2. Copy the textures of the pack into it.
3. Turn on **VISUAL RENDERING > CUSTOM TEXTURES**.

**DuckStation**

1. Create the folder `emulators\duckstation\textures\<game ID>\replacements`, for example `emulators\duckstation\textures\SLUS-00594\replacements`. The ID is the serial number of the game.
2. Copy the textures of the pack into it.
3. Turn on **VISUAL RENDERING > CUSTOM TEXTURES**. The **PREFETCH CUSTOM TEXTURES** option loads them all at startup, to avoid stutter in game.

### Cheats

| Emulator       | How to                                                                                |
| -------------- | ------------------------------------------------------------------------------------- |
| libretro cores | RetroArch menu (**HOTKEY + SOUTH**), cheats section. Files are in `cheats\retroarch`. |
| DuckStation    | Put the files in `cheats\duckstation`, then enable the codes in DuckStation.          |
| Mednafen       | Turn on **EMULATION > ENABLE CHEATS**. Files are in `cheats\mednafen`.                |
| BizHawk        | Files are in `cheats\bizhawk\psx`.                                                    |

## Known issues

| Issue                                            | Solution                                                                                                                                                                   |
| ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| The game does not start, BIOS not found          | Put `psxonpsp660.bin` at the root of `bios`, or the `scph` file of the game region.                                                                                        |
| A `.chd` does not start with Mednafen or BizHawk | These emulators do not read this format: change emulator or use a `.cue` image.                                                                                            |
| Sticks do not respond                            | The game expects analog mode: use the L1 + R1 + START combo (mednafen\_psx\_hw) or the Guide button (DuckStation). Conversely, some old games need the digital controller. |
| The game asks for disc 2                         | Use an `.m3u` file and the disc change hotkeys (see [Guides](playstation.md#multi-disc-games)).                                                                            |
| Netplay is not offered                           | Only the mednafen\_psx\_hw and pcsx\_rearmed cores offer it.                                                                                                               |
| My saves are gone after changing emulator        | Each emulator has its own memory cards (see [Folders](playstation.md#folders)).                                                                                            |
| Custom textures do not show up                   | Check the folder, which is not the same for mednafen\_psx\_hw and DuckStation (see [Guides](playstation.md#custom-textures)), and that the pack is made for this emulator. |
| The player 3 controller does not respond         | The multitap is only enabled from 3 connected controllers, and the game must support it. With Mednafen, set **USE MULTITAP**.                                              |
