---
description: Commodore
---

# Amiga 4000

<div align="left"><figure><img src="../../../../.gitbook/assets/image (452).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Amiga 4000** is the high-end model of the Amiga range, released by Commodore in 1992. A desktop computer built for professionals, it combined the **AGA** chipset of the Amiga 1200 with a much more powerful processor (Motorola 68040 at 25 MHz on the A4000/040, 68030 on the cheaper A4000/030), up to 16 MB of memory on the motherboard, an IDE hard drive and Zorro III expansion slots. A tower version, the A4000T, followed in 1994.

The Amiga 4000 was mainly used for video and 3D work: with the Video Toaster and LightWave 3D, it was behind the special effects of several TV series of the 1990s. For games, it runs the AGA titles of the Amiga 1200 faster, as well as the most demanding late games and demos: _Alien Breed 3D II_, _Breathless_, _Gloom Deluxe_, the Amiga ports of _Doom_ and _Quake_…

This system covers the Amiga 4000. For the classic games of the Amiga 500 and the Amiga 1200, prefer the Amiga OCS/ECS and Amiga AGA systems: their models are more compatible with these games.

{% embed url="https://en.wikipedia.org/wiki/Amiga_4000" %}

## At a glance

<table><thead><tr><th width="254"></th><th></th></tr></thead><tbody><tr><td>Games folder</td><td>📁 roms \ 📂 amiga4000</td></tr><tr><td>File extensions</td><td>.adf .adz .dms .ipf .hdf .lha .uae .rp9 .m3u .zip .7z</td></tr><tr><td>Default emulator</td><td>libretro: puae</td></tr><tr><td>BIOS</td><td>Kickstart 3.1 (A4000) required</td></tr><tr><td>Controller autoconfig</td><td>Yes (except Amiga Forever)</td></tr><tr><td>RetroAchievements</td><td>No</td></tr><tr><td>Netplay</td><td>No</td></tr><tr><td>Save state manager (ES)</td><td>libretro cores, Amiberry</td></tr></tbody></table>

## Which emulator to choose?

| Emulator                     | Strengths                                                                                  | Limits                                         |
| ---------------------------- | ------------------------------------------------------------------------------------------ | ---------------------------------------------- |
| **libretro: puae** (default) | Reliable, all formats, virtual keyboard, Pad2Key                                           | No JIT: slower for 3D games                    |
| libretro: amiberry           | Recent UAE engine, WHDLoad and .rp9 support, Pad2Key                                       |                                                |
| amiberry                     | Standalone version: JIT enabled by default, choice of model, CPU and memory, Amiberry menu | 2 players                                      |
| winuae                       | The reference Amiga emulator, the most accurate                                            | 2 players                                      |
| amigaforever                 | Plays the .rp9 packages of Cloanto's commercial Amiga Forever                              | Amiga Forever must be installed, no autoconfig |

## BIOS

### Kickstart files

The Amiga needs its system ROM, the **Kickstart**. Copy it to the `bios` folder (or `bios\amiga`).

| Kickstart             | Short name      | Amiga Forever name     | MD5 (short name)                 | Used for                                    |
| --------------------- | --------------- | ---------------------- | -------------------------------- | ------------------------------------------- |
| Kickstart 3.1 (A4000) | kick40068.A4000 | amiga-os-310-a4000.rom | 9bdedde6a4f33555b4a270c8ca53297d | **Required** – Amiga 4000                   |
| Kickstart 1.3 (A500)  | kick34005.A500  | amiga-os-130.rom       | 82a21c1890cae844b3df741f2762d48d | Optional – some WHDLoad games (lr-amiberry) |
| Kickstart 3.1 (A1200) | kick40068.A1200 | amiga-os-310-a1200.rom | 646773759326fbac3b2311fd8c8793ee | Optional – some WHDLoad games (lr-amiberry) |
| Amiga Forever key     | rom.key         |                        |                                  | Optional – encrypted Amiga Forever ROMs     |

{% hint style="info" %}
RetroBat checks that the Kickstart 3.1 (A4000) is present. The other files are listed as OPTIONAL.
{% endhint %}

### Which file name should I use?

* The **short names** (`kick40068.A4000`…) work with every emulator: use them if you are not sure.
* Amiberry, lr-amiberry and WinUAE also accept the **Amiga Forever** names (`amiga-os-310-a4000.rom`…) and the usual TOSEC names.
* The Amiga Forever ROMs are encrypted: copy the **rom.key** file supplied with Amiga Forever next to them.

### Choosing the Amiga model

By default, RetroBat emulates an **Amiga 4000/040 with Kickstart 3.1**, 2 MB of Chip RAM and 8 MB of Fast RAM. The options (EMULATION submenu) let you adjust it:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (453).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="169.5">Emulator</th><th>Option</th><th>Choices</th></tr></thead><tbody><tr><td>lr-puae</td><td>MODEL</td><td>A4000/030, A4000/040</td></tr><tr><td>lr-amiberry</td><td>MODEL</td><td>A4000/030, A4000/040</td></tr><tr><td>Amiberry</td><td>MODEL / CPU / Z3 FAST RAM</td><td>A4000/040 or /030, 68030 to 68060, Zorro III RAM up to 64 MB</td></tr><tr><td>WinUAE</td><td>CPU / ENABLE JIT / USE FPU</td><td>68040 or 68030, JIT and FPU</td></tr></tbody></table>

## Game formats

### Formats

<table><thead><tr><th width="156.5">Format</th><th>Description</th></tr></thead><tbody><tr><td>.adf</td><td>Standard floppy disk image (.adz: compressed .adf, .dms: DiskMasher archive)</td></tr><tr><td>.ipf</td><td>Copy-protected floppy image (SPS). Needs the <code>capsimg.dll</code> plugin, supplied with RetroBat in <code>bios</code></td></tr><tr><td>.lha</td><td><strong>WHDLoad</strong> game: a floppy game installed to run from a hard drive, without disk swapping</td></tr><tr><td>.hdf</td><td>Hard disk image, for example a Workbench installation</td></tr><tr><td>.uae</td><td>UAE configuration file (your own settings), Amiberry and WinUAE</td></tr><tr><td>.rp9</td><td>Amiga Forever package (Amiga Forever, lr-amiberry)</td></tr><tr><td>.m3u</td><td>Multi-disk game</td></tr><tr><td>.zip / .7z</td><td>Compressed disk images</td></tr></tbody></table>

{% hint style="success" %}
For a simple experience, prefer the **WHDLoad** versions (.lha) of the games: they start straight away, load faster and do not ask you to swap disks.
{% endhint %}

### Multi-disk games

Use a .m3u file to group the disks of a game. Example for _Alien Breed 3D II_: create `Alien Breed 3D II.m3u` in the `roms\amiga4000` folder with this content:

```
Alien Breed 3D II (Disk 1).adf
Alien Breed 3D II (Disk 2).adf
Alien Breed 3D II (Disk 3).adf
Alien Breed 3D II (Disk 4).adf
```

Changing disk:

* **libretro cores**: use the disk hotkeys (HOTKEY + L1 to eject/insert, HOTKEY + L2/R2 to select the previous/next disk), or the virtual keyboard menu.
* **Amiberry**: the first disks go to the floppy drives (**FLOPPY DRIVES** option, up to 4), the others to the disk swapper of the Amiberry menu.
* **WinUAE**: also finds the next disks by itself when they are named "Disk 1", "Disk 2"…

## Controls

### Controller autoconfiguration

The Amiga has two ports: the **joystick** is in port 2 and the **mouse** in port 1. RetroBat follows this layout: player 1's controller goes to port 2 and your PC mouse to port 1.

| Emulator             | Autoconfig | Players |
| -------------------- | ---------- | ------- |
| lr-puae, lr-amiberry | Yes        | 2       |
| Amiberry             | Yes        | 2       |
| WinUAE               | Yes        | 2       |
| Amiga Forever        | No         |         |

Your PC keyboard works as the Amiga keyboard with every emulator.

### Default layout

| Amiga                | libretro cores | Amiberry |
| -------------------- | -------------- | -------- |
| Joystick             | D-pad          | D-pad    |
| Fire button 1 (red)  | SOUTH          | SOUTH    |
| Fire button 2 (blue) | EAST           | EAST     |
| Space bar            | NORTH          |          |
| Mouse                | Analog sticks  | PC mouse |
| Mouse buttons        | L2 / R2        | PC mouse |
| Virtual keyboard     | SELECT         | SELECT   |
| Emulator menu        |                | R3       |

<div align="left"><figure><img src="../../../../.gitbook/assets/image.png" alt="" width="225"><figcaption></figcaption></figure></div>

### Useful control options

<table><thead><tr><th width="133.25">Emulator</th><th>Option</th><th>Description</th></tr></thead><tbody><tr><td>lr-puae</td><td>PAD BUTTON LAYOUT</td><td>Other button layouts (jump on a button…)</td></tr><tr><td>lr-puae</td><td>MOUSE CONTROL</td><td>Which sticks control the mouse</td></tr><tr><td>Amiberry</td><td>PORT 1 DEVICE / PORT 2 DEVICE</td><td>Mouse, joystick (player 2) or nothing in each port</td></tr><tr><td>Amiberry</td><td>SWAP JOYSTICK PORTS</td><td>For the few games that want the joystick in port 1</td></tr><tr><td>Amiberry</td><td>MENU BUTTON / VIRTUAL KEYBOARD BUTTON</td><td>Change the buttons that open the menu and the virtual keyboard</td></tr><tr><td>WinUAE</td><td>SWAP JOYSTICK PORTS / SECOND CONTROLLER</td><td>Swap the ports, put player 2 in port 1</td></tr></tbody></table>

### Games that need the keyboard

Many Amiga games use the keyboard (space bar, F1-F10 keys, answers in adventure games…). With the libretro cores, use **Pad2Key** to map keys on your controller, or the virtual keyboard (SELECT).

### Hotkeys

**libretro cores**: [standard RetroBat hotkeys](../../../../navigation/hotkeys.md).

| Hotkey         | Amiberry   | WinUAE | Amiga Forever |
| -------------- | ---------- | ------ | ------------- |
| HOTKEY + START | Quit       | Quit   |               |
| HOTKEY + WEST  | Save state |        |               |
| HOTKEY + NORTH | Load state |        |               |

The Amiberry menu opens with R3 or F12, the WinUAE menu with F12.

## Folders

<table><thead><tr><th width="140.75">Emulator</th><th>Content</th><th>Folder</th></tr></thead><tbody><tr><td>lr-puae</td><td>Saves</td><td><code>saves\amiga4000</code></td></tr><tr><td>lr-amiberry</td><td>Saves</td><td><code>saves\amiga4000\LR-amiberry</code></td></tr><tr><td>libretro</td><td>Save states</td><td><code>saves\amiga4000\libretro.&#x3C;core></code></td></tr><tr><td>Amiberry</td><td>Save states, disk saves, NVRAM</td><td><code>saves\amiga4000\amiberry</code></td></tr><tr><td>Amiberry</td><td>Screenshots</td><td><code>screenshots\amiberry</code></td></tr><tr><td>Amiberry</td><td>Your .uae configurations</td><td><code>emulators\amiberry\Configurations</code></td></tr><tr><td>WinUAE</td><td>Save states</td><td><code>saves\amiga4000\winuae</code></td></tr><tr><td>WinUAE</td><td>Disk saves / WHDLoad saves</td><td><code>saves\amiga4000\winuae\saveimages</code> / <code>saves\amiga4000\winuae\whdload</code></td></tr><tr><td>WinUAE</td><td>Screenshots / videos</td><td><code>screenshots\winuae</code> / <code>records\winuae</code></td></tr></tbody></table>

## Guides

### Playing WHDLoad games

WHDLoad games (.lha) start automatically with every emulator except Amiga Forever: RetroBat or the emulator prepares the hard drive environment. With Amiberry, the **WHDLOAD: SPLASH SCREEN** and **WHDLOAD: WAIT FOR BUTTON** options show the WHDLoad screen before the game; with lr-puae, use **WHDLOAD SPLASH SCREEN**.

### JIT and FPU

* **JIT** speeds up the processor emulation a lot and is what makes the Amiga 4000 fast in 3D games. It is enabled by default with Amiberry (**ENABLE JIT**), and can be enabled with WinUAE (**ENABLE JIT**). It is not compatible with cycle-exact emulation.
* The **FPU** (math coprocessor) is needed by some 3D games and demos. It is built into the 68040 and enabled by default with Amiberry and WinUAE. With the 68030, Amiberry adds a 68882 by default; with WinUAE, enable **USE FPU**. The Amiberry **FPU** option lets you change or remove it.

### Using your own .uae configuration

Amiberry and WinUAE start the **.uae** files you put in `roms\amiga4000` as they are: RetroBat does not change them. This lets you prepare a precise configuration (graphics card, Zorro III memory, hard drives) for Workbench or for a demanding game.

## Known issues

| Problem                                                | Solution                                                                                                                 |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| "Kickstart not found" or black screen                  | Copy kick40068.A4000 (Kickstart 3.1 A4000) to the bios folder.                                                           |
| Amiga Forever ROMs do not work                         | Copy rom.key next to them.                                                                                               |
| .ipf games do not start                                | Check that capsimg.dll is in the bios folder.                                                                            |
| An older game does not start, freezes or runs too fast | The 68040 is too fast or not compatible: use the A4000/030 model, or put the game in the Amiga 1200 or Amiga 500 system. |
| A 3D game is too slow                                  | Use Amiberry, or enable the JIT with WinUAE.                                                                             |
| A 3D game crashes or shows a math error                | The game needs the FPU: keep the 68040, or enable USE FPU (WinUAE) / FPU (Amiberry) with the 68030.                      |
| The joystick does not respond in a game                | The game wants the joystick in port 1: enable SWAP JOYSTICK PORTS (Amiberry, WinUAE).                                    |
| The game needs the keyboard                            | Use your PC keyboard, the virtual keyboard (SELECT) or Pad2Key.                                                          |
