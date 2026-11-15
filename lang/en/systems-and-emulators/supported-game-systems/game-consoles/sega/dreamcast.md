---
description: Sega
---

# Dreamcast

<div align="left"><figure><img src="../../../../.gitbook/assets/image (577).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Dreamcast** is Sega's last home console. It was released in November 1998 in Japan, then in September 1999 in the United States and in October 1999 in Europe. It is built around a Hitachi SH-4 processor and a NEC PowerVR2 graphics chip, and reads its games from **GD-ROMs**, Sega-specific discs of about 1 GB.

It was the first console sold with a modem, to play and browse online. Its controller takes the **VMU**, a memory card with a small screen, and the **Puru Puru Pack** (rumble). Despite very good games, the console sold about 9 million units, and Sega stopped its production in 2001 to focus on making games. Notable games include Shenmue, Soulcalibur, Jet Set Radio, Crazy Taxi, Sonic Adventure, Phantasy Star Online, Skies of Arcadia and Resident Evil Code: Veronica.

RetroBat offers four emulators: the **flycast** libretro core (default), the standalone **Flycast**, **Redream** and **Demul**.

{% embed url="https://en.wikipedia.org/wiki/Dreamcast" %}

## In short

<table><thead><tr><th width="226.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\dreamcast</code></td></tr><tr><td><strong>Extensions</strong></td><td>.mds .mdf .cue .cdi .gdi .chd .m3u</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: flycast</td></tr><tr><td><strong>BIOS</strong></td><td><code>dc_boot.bin</code> and <code>dc_flash.bin</code> in <code>bios\dc</code></td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, Flycast</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, Flycast</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores, Flycast, Demul</td></tr><tr><td><strong>Wheels</strong></td><td>Flycast</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>dc.zip</code> in <code>bios\dc</code> (Demul)</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="152">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: flycast</strong> (default)</td><td>Very good compatibility. Save states, RetroAchievements, RetroArch shaders and hotkeys. Custom textures, higher resolution, VMU shown on screen.</td><td>—</td></tr><tr><td><strong>flycast</strong></td><td>Same base as the core, with its own menus. RetroAchievements, save states, online play (GGPO, DCNet).</td><td>Does not read <code>.m3u</code> nor <code>.mds</code> / <code>.mdf</code>.</td></tr><tr><td><strong>redream</strong></td><td>Simple and light, good compatibility.</td><td>Resolution above native reserved to the paid version (Redream key). No save states handled by RetroBat.</td></tr><tr><td><strong>demul</strong></td><td>Long-standing emulator, also used for arcade (Naomi, Atomiswave).</td><td>Less compatible for the Dreamcast, needs <code>dc.zip</code>. Does not read <code>.m3u</code>.</td></tr></tbody></table>

If a game has issues with the flycast core, try the standalone Flycast, then Redream.

## BIOS

<table><thead><tr><th width="145.25">File</th><th width="115.25">Folder</th><th width="160.5">Used by</th><th>MD5</th></tr></thead><tbody><tr><td><code>dc_boot.bin</code></td><td><code>bios\dc</code></td><td>flycast (core and standalone)</td><td><code>e10c53c2f8b90bab96ead2d368858623</code></td></tr><tr><td><code>dc_flash.bin</code></td><td><code>bios\dc</code></td><td>flycast (core and standalone)</td><td><code>0a93f7940c455905bea6e392dfde92a4</code></td></tr><tr><td><code>dc.zip</code></td><td><code>bios\dc</code></td><td>Demul (optional for the others)</td><td>see below</td></tr></tbody></table>

The flycast core and the standalone Flycast both read the BIOS from `bios\dc`. Their **EMULATION > HLE BIOS** (core) or **EMULATION > USE HLE BIOS** (Flycast) option replaces the BIOS with an emulation: it lets you play without a BIOS, but with lower compatibility.

Redream does not use the files of `bios\dc`.

`dc.zip` is the BIOS in MAME format, needed by Demul. It contains:

```
1_01d_01.bin   e10c53c2f8b90bab96ead2d368858623
1_01d_02.bin   a5c6a00818f97c5e3e91569ee22416dc
1_004_01.bin   37c921eb47532cae8fb70e5d987ce91c
1_011_01.bin   eafca1eed2d7f76c487e940597c2a786
```

### Console language and region

Games use the language of the emulated console. Set it with **EMULATION > LANGUAGE** (flycast core, Flycast, Redream), and the region with **EMULATION > REGION** (Demul: **EMULATION > DREAMCAST REGION**). **VIDEO > VIDEO FORMAT** chooses NTSC or PAL.

## Which game format?

<table><thead><tr><th width="157.75">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.chd</strong></td><td>Compressed format, the most convenient. Read by all four emulators.</td></tr><tr><td><strong>.gdi</strong></td><td>Full copy of the GD-ROM (<code>.gdi</code> file and its tracks). Read by all four emulators.</td></tr><tr><td><strong>.cdi</strong></td><td>Burnable CD image (independent games, modified versions).</td></tr><tr><td><strong>.cue</strong></td><td>CD image with <code>.bin</code> tracks (flycast core, Flycast).</td></tr><tr><td><strong>.mds</strong> / <strong>.mdf</strong></td><td>Alcohol 120% images (Demul).</td></tr><tr><td><strong>.m3u</strong></td><td>Multi-disc games (see <a href="dreamcast.md#multi-disc-games">Guides</a>): flycast core and Redream only. With Redream, RetroBat launches the disc chosen in <strong>EMULATION > M3U DISC NUMBER</strong> (the first one by default).</td></tr></tbody></table>

`.zip` and `.7z` archives are not supported.

## Controls

### Automatic configuration

RetroBat configures the controllers automatically for the four emulators, up to 4 players.

<table><thead><tr><th width="217.75">Dreamcast</th><th>Controller</th></tr></thead><tbody><tr><td>A</td><td>SOUTH</td></tr><tr><td>B</td><td>EAST</td></tr><tr><td>X</td><td>WEST</td></tr><tr><td>Y</td><td>NORTH</td></tr><tr><td>L and R triggers</td><td>L2, R2</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>D-pad, analog stick</td><td>D-pad, left stick</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (578).png" alt="" width="225"><figcaption></figcaption></figure></div>

* **CONTROLS > USE R1 AND L1** puts the L and R triggers on L1 and R1 (all four emulators).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (579).png" alt="" width="225"><figcaption></figcaption></figure></div>

* **Flycast**: **CONTROLS > PLAYER 1 CONTROLLER TYPE** (to 4) chooses the device (controller, light gun, keyboard, mouse, arcade stick, Samba de Amigo maracas, fishing rod, racing controller…), and **PLAYER 1 EXTENSION** (to 4) what is plugged into the controller (VMU, Puru Puru, microphone).
* **flycast core**: **CONTROLS > CONTROLLER TYPE** chooses the device for all players. Each controller has a VMU and a Puru Puru Pack.
* **Demul**: **PLAYER 1 EXTENSION** (to 4) adds a Puru Puru Pack or a microphone.
* **Redream**: **CONTROLS > USE REDREAM CONTROLLER CONFIGURATION** lets Redream configure the controllers itself.

### Light guns

Light gun games (The House of the Dead 2, Confidential Mission…) work with the flycast core (up to 4 guns), Flycast (2 guns, 4 with DemulShooter) and Demul (1 gun, 2 with DemulShooter). For the options and buttons, see the [**Gun controls**](../../../../controllers/gun_controls.md) page.

### Wheels

Flycast supports wheels (**WHEELS > ENABLE WHEEL**). **WHEELS > USE RACING CONTROLLER** emulates Sega's racing controller. The flycast core also supports wheels, but RetroBat does not provide its mapping file yet. For the supported wheels, see the [**Wheels**](https://app.gitbook.com/s/Cgoewyw8Sagl6SNUMrCG/controleurs/supported-controllers/volants) page.

### Hotkeys

The flycast core uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

**Flycast**

<table><thead><tr><th width="202">Hotkey</th><th width="204.25">Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td>Escape</td></tr><tr><td><strong>HOTKEY + SOUTH</strong></td><td>Flycast menu</td><td>F1</td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Load state</td><td>F4</td></tr><tr><td><strong>HOTKEY + RIGHT</strong></td><td>Fast forward (hold)</td><td>L</td></tr><tr><td><strong>HOTKEY + R3</strong></td><td>Screenshot</td><td>F8</td></tr></tbody></table>

Flycast has no hotkey to change the save state slot.

**Redream**

<table><thead><tr><th width="271.5">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr></tbody></table>

**Demul**

<table><thead><tr><th width="185.75">Hotkey</th><th>Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td></td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Demul save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Demul load state</td><td>F4</td></tr></tbody></table>

Demul save states stay in Demul: they do not show up in the save state manager.

## Folders

<table><thead><tr><th width="335.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>BIOS (flycast core, Flycast)</td><td><code>bios\dc</code></td></tr><tr><td>flycast core: VMUs</td><td><code>bios\dc</code> (<code>vmu_save_*.bin</code> files)</td></tr><tr><td>flycast core: save states</td><td><code>saves\dreamcast\libretro.flycast</code></td></tr><tr><td>Custom textures (flycast core, Flycast)</td><td><code>bios\dc\textures\&#x3C;game ID></code></td></tr><tr><td>Flycast: VMUs</td><td><code>saves\dreamcast\flycast\vmu</code></td></tr><tr><td>Flycast: save states</td><td><code>saves\dreamcast\flycast\sstates</code> (copied from <code>saves\dreamcast\reicast\states</code>)</td></tr><tr><td>Flycast: configuration</td><td><code>emulators\flycast\emu.cfg</code></td></tr><tr><td>Redream: configuration and saves</td><td><code>emulators\redream</code></td></tr><tr><td>Demul: saves (NVRAM)</td><td><code>saves\dreamcast\demul</code></td></tr><tr><td>Demul: configuration</td><td><code>emulators\demul\Demul.ini</code></td></tr></tbody></table>

The VMUs of the flycast core and of Flycast are synchronized at each launch: the most recent file is copied to the other folder, so you get your saves with both. For one VMU per game, use **EMULATION > SAVE FILES** (core) or **EMULATION > PER GAME VMU** (Flycast).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (582).png" alt=""><figcaption></figcaption></figure></div>

## Guides

### Multi-disc games

1. Create a text file in `roms\dreamcast`, with the `.m3u` extension (for example `Alone in the Dark - The New Nightmare.m3u`).
2. Write one line per disc, in order, with the path of each disc from the folder of the `.m3u` file:

```
Alone in the Dark - The New Nightmare (Disc 1).gdi
Alone in the Dark - The New Nightmare (Disc 2).gdi
```

<div align="left"><figure><img src="../../../../.gitbook/assets/image (581).png" alt=""><figcaption></figcaption></figure></div>

3. Update the game list: RetroBat hides the discs and only shows the `.m3u` file.

With the flycast core, change disc with the RetroArch disc hotkeys. With Redream, choose the disc to launch with **EMULATION > M3U DISC NUMBER**.

### Custom textures

1. Copy the texture pack to `bios\dc\textures\<game ID>`: the folder is used by both the flycast core and Flycast. The folder name (game ID) comes with the pack.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (580).png" alt="" width="267"><figcaption></figcaption></figure></div>

2. Enable **VISUAL RENDERING > CUSTOM TEXTURES** for the system or the game.

### Playing online with Flycast

Flycast can connect to the online game servers brought back by the community (Phantasy Star Online, Quake III Arena…) with **NETWORK > USE DCNET**. **NETWORK > NETWORK TYPE** also lets you play online with **GGPO** (fighting games) or by emulating the link cable (**BATTLE CABLE**). **NETWORK > HOST GAME** and **NETWORK > SERVER** set who hosts the game.

This online play is specific to Flycast: it does not use RetroBat netplay.

### Other useful options

<table><thead><tr><th width="346.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Raises the rendering resolution (flycast core, Flycast, Demul; Redream: paid version above native resolution).</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>Flycast, Redream, Demul: 4:3, 16:9 or stretched.</td></tr><tr><td><strong>VISUAL RENDERING > WIDESCREEN HACK</strong> / <strong>WIDESCREEN PATCHES</strong></td><td>16:9 display: the hack widens the picture of every game (with glitches), the patches fix the compatible games.</td></tr><tr><td><strong>VIDEO > EMULATED CABLE TYPE</strong></td><td>VGA, RGB or composite. Some games refuse the VGA cable.</td></tr><tr><td><strong>VISUAL RENDERING > ALPHA SORTING</strong></td><td>Fixes badly displayed transparencies in some games.</td></tr><tr><td><strong>EMULATION > SHOW VMU SCREEN</strong></td><td>flycast core: shows the VMU screen in a corner of the picture.</td></tr><tr><td><strong>EMULATION > GD-ROM FAST LOADING</strong></td><td>flycast core: speeds up loading, may break some games.</td></tr></tbody></table>

## Known issues

| Issue                                                               | Solution                                                                                      |
| ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| The game does not start with the flycast core or Flycast            | Check `dc_boot.bin` and `dc_flash.bin` in `bios\dc`, then try another emulator.               |
| Demul does not start                                                | Check that `dc.zip` is in `bios\dc`.                                                          |
| A multi-disc game does not launch with Flycast or Demul             | These emulators do not read `.m3u` files: use the flycast core or Redream.                    |
| Black screen or unstable picture at startup                         | Change **VIDEO > EMULATED CABLE TYPE** (some games only work in RGB or composite).            |
| The triggers do not respond on a controller without analog triggers | Enable **CONTROLS > USE R1 AND L1**.                                                          |
| Redream saves do not show up in Flycast                             | Redream keeps its VMUs in its own folder: only the flycast core and Flycast share their VMUs. |
| Redream stays at native resolution                                  | Higher resolution needs a Redream key (paid version).                                         |

The **Naomi** and the **Atomiswave**, arcade boards close to the Dreamcast, have their own pages: see the [**Sega Naomi**](../../arcade/sega/sega-naomi.md)**,** [**Sega Naomi 2**](../../arcade/sega/sega-naomi-2.md) and [**Atomiswave**](../../arcade/atomiswave.md) pages.
