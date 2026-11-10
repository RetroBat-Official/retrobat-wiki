---
description: Commodore
---

# Amiga 1200

<div align="left"><figure><img src="../../../../.gitbook/assets/image (448).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Amiga 1200** is a home computer released by Commodore in 1992. It succeeded the Amiga 500 with a faster processor (Motorola 68020), 2 MB of memory and above all the new **AGA** chipset: 256 colours on screen out of 16.8 million, which brought Amiga graphics into the 1990s. It came with Kickstart 3.0, then 3.1.

The Amiga 1200 was the last popular Amiga before Commodore's bankruptcy in 1994. It received enhanced versions of many games and AGA-only titles: _Banshee_, _Alien Breed 3D_, _Gloom_, _Super Stardust_, _Simon the Sorcerer_, _The Settlers II_, _Pinball Fantasies AGA_, _Theme Park_, _Uridium 2_… With an accelerator board and a hard drive, it is also the reference machine for **WHDLoad** games.

This system (Amiga AGA) covers the Amiga 1200. The Amiga 4000 and the CD32, which also use the AGA chipset, have their own pages.

{% embed url="https://en.wikipedia.org/wiki/Amiga_1200" %}

## At a glance

|                         |                                                       |
| ----------------------- | ----------------------------------------------------- |
| Games folder            | 📁 roms \ 📂 amiga1200                                |
| File extensions         | .adf .adz .dms .ipf .hdf .lha .uae .rp9 .m3u .zip .7z |
| Default emulator        | libretro: puae                                        |
| BIOS                    | Kickstart 3.1 (A1200) required                        |
| Controller autoconfig   | Yes (except Amiga Forever)                            |
| RetroAchievements       | No                                                    |
| Netplay                 | No                                                    |
| Save state manager (ES) | libretro cores, Amiberry                              |

## Which emulator to choose?

| Emulator                     | Strengths                                                                                              | Limits                                         |
| ---------------------------- | ------------------------------------------------------------------------------------------------------ | ---------------------------------------------- |
| **libretro: puae** (default) | Reliable, all formats, virtual keyboard, Pad2Key                                                       |                                                |
| libretro: amiberry           | Recent UAE engine, WHDLoad and .rp9 support, Pad2Key                                                   |                                                |
| amiberry                     | Standalone version: very good compatibility, choice of model, CPU and memory, light pen, Amiberry menu | 2 players                                      |
| winuae                       | The reference Amiga emulator, the most accurate                                                        | 2 players                                      |
| amigaforever                 | Plays the .rp9 packages of Cloanto's commercial Amiga Forever                                          | Amiga Forever must be installed, no autoconfig |

## BIOS

### Kickstart files

The Amiga needs its system ROM, the **Kickstart**. Copy it to the `bios` folder (or `bios\amiga`).

| Kickstart             | Short name      | Amiga Forever name     | MD5 (short name)                 | Used for                                    |
| --------------------- | --------------- | ---------------------- | -------------------------------- | ------------------------------------------- |
| Kickstart 3.1 (A1200) | kick40068.A1200 | amiga-os-310-a1200.rom | 646773759326fbac3b2311fd8c8793ee | **Required** – Amiga 1200                   |
| Kickstart 1.3 (A500)  | kick34005.A500  | amiga-os-130.rom       | 82a21c1890cae844b3df741f2762d48d | Optional – some WHDLoad games (lr-amiberry) |
| Kickstart 3.1 (A600)  | kick40063.A600  | amiga-os-310-a600.rom  | e40a5dfb3d017ba8779faba30cbd1c8e | Optional – some WHDLoad games (lr-amiberry) |
| Amiga Forever key     | rom.key         |                        |                                  | Optional – encrypted Amiga Forever ROMs     |

{% hint style="info" %}
RetroBat checks that the Kickstart 3.1 (A1200) is present. The other files are listed as OPTIONAL.
{% endhint %}

### Which file name should I use?

* The **short names** (`kick40068.A1200`…) work with every emulator: use them if you are not sure.
* Amiberry, lr-amiberry and WinUAE also accept the **Amiga Forever** names (`amiga-os-310-a1200.rom`…) and the usual TOSEC names.
* The Amiga Forever ROMs are encrypted: copy the **rom.key** file supplied with Amiga Forever next to them.

### Choosing the Amiga model

By default, RetroBat emulates an **Amiga 1200 with Kickstart 3.1**. The options (EMULATION submenu) let you adjust the memory and the processor:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (451).png" alt=""><figcaption></figcaption></figure></div>

| Emulator    | Option                               | Choices                                                             |
| ----------- | ------------------------------------ | ------------------------------------------------------------------- |
| lr-puae     | MODEL                                | A1200 (2M Chip), A1200 (2M Chip + 8M Fast)                          |
| lr-amiberry | MODEL                                | A1200 original (2M Chip), A1200 (2M Chip + 8M Fast)                 |
| Amiberry    | MODEL / CPU / FAST RAM / Z3 FAST RAM | A1200 with or without Fast RAM, 68020 to 68040, Fast RAM up to 8 MB |
| WinUAE      | FAST RAM / ENABLE JIT / USE FPU      | Fast RAM (enabled by default), JIT and FPU for 3D games             |

## Game formats

### Formats

| Format     | Description                                                                                         |
| ---------- | --------------------------------------------------------------------------------------------------- |
| .adf       | Standard floppy disk image (.adz: compressed .adf, .dms: DiskMasher archive)                        |
| .ipf       | Copy-protected floppy image (SPS). Needs the `capsimg.dll` plugin, supplied with RetroBat in `bios` |
| .lha       | **WHDLoad** game: a floppy game installed to run from a hard drive, without disk swapping           |
| .hdf       | Hard disk image                                                                                     |
| .uae       | UAE configuration file (your own settings), Amiberry and WinUAE                                     |
| .rp9       | Amiga Forever package (Amiga Forever, lr-amiberry)                                                  |
| .m3u       | Multi-disk game                                                                                     |
| .zip / .7z | Compressed disk images                                                                              |

{% hint style="success" %}
For a simple experience, prefer the **WHDLoad** versions (.lha) of the games: they start straight away, load faster and do not ask you to swap disks.
{% endhint %}

### Multi-disk games

Use a .m3u file to group the disks of a game. Example for _Simon the Sorcerer_: create `Simon the Sorcerer.m3u` in the `roms\amiga1200` folder with this content:

```
Simon the Sorcerer (Disk 1).adf
Simon the Sorcerer (Disk 2).adf
Simon the Sorcerer (Disk 3).adf
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

| Emulator | Option                                  | Description                                                    |
| -------- | --------------------------------------- | -------------------------------------------------------------- |
| lr-puae  | PAD BUTTON LAYOUT                       | Other button layouts (jump on a button…)                       |
| lr-puae  | MOUSE CONTROL                           | Which sticks control the mouse                                 |
| Amiberry | PORT 1 DEVICE / PORT 2 DEVICE           | Mouse, joystick (player 2) or nothing in each port             |
| Amiberry | SWAP JOYSTICK PORTS                     | For the few games that want the joystick in port 1             |
| Amiberry | MENU BUTTON / VIRTUAL KEYBOARD BUTTON   | Change the buttons that open the menu and the virtual keyboard |
| WinUAE   | SWAP JOYSTICK PORTS / SECOND CONTROLLER | Swap the ports, put player 2 in port 1                         |

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

### Light pen

Amiberry emulates a **light pen** (or a **Trojan Phazer** gun) with your mouse or your light gun: enable **ENABLE GUN** (GUNS submenu) and choose the **GUN TYPE**.

## Folders

| Emulator    | Content                        | Folder                                                                 |
| ----------- | ------------------------------ | ---------------------------------------------------------------------- |
| lr-puae     | Saves                          | `saves\amiga1200`                                                      |
| lr-amiberry | Saves                          | `saves\amiga1200\LR-amiberry`                                          |
| libretro    | Save states                    | `saves\amiga1200\libretro.<core>`                                      |
| Amiberry    | Save states, disk saves, NVRAM | `saves\amiga1200\amiberry`                                             |
| Amiberry    | Screenshots                    | `screenshots\amiberry`                                                 |
| Amiberry    | Your .uae configurations       | `emulators\amiberry\Configurations`                                    |
| WinUAE      | Save states                    | `saves\amiga1200\winuae`                                               |
| WinUAE      | Disk saves / WHDLoad saves     | `saves\amiga1200\winuae\saveimages` / `saves\amiga1200\winuae\whdload` |
| WinUAE      | Screenshots / videos           | `screenshots\winuae` / `records\winuae`                                |

## Guides

### Playing WHDLoad games

WHDLoad games (.lha) start automatically with every emulator except Amiga Forever: RetroBat or the emulator prepares the hard drive environment. With Amiberry, the **WHDLOAD: SPLASH SCREEN** and **WHDLOAD: WAIT FOR BUTTON** options show the WHDLoad screen before the game; with lr-puae, use **WHDLOAD SPLASH SCREEN**.

### Fast RAM, JIT and FPU

* **Fast RAM** is extra memory used by many WHDLoad games. A few original floppy games refuse to start with it: choose the model without Fast RAM (lr-puae, lr-amiberry, Amiberry) or disable **FAST RAM** (WinUAE).
* **JIT** speeds up the processor emulation a lot, useful for 3D games (_Alien Breed 3D_, _Gloom_). It is not compatible with cycle-exact emulation and can break some older games: **ENABLE JIT** (Amiberry, WinUAE).
* The **FPU** (math coprocessor) is needed by some late 3D games: **FPU** (Amiberry), **USE FPU** (WinUAE).

### Using your own .uae configuration

Amiberry and WinUAE start the **.uae** files you put in `roms\amiga1200` as they are: RetroBat does not change them. This lets you prepare a precise configuration (memory, accelerator board, hard drives) for a game or for Workbench.

### Improving accuracy

* **Amiberry**: **ACCURACY** option, CYCLE EXACT for demos and timing-sensitive games (needs a fast PC).
* **WinUAE**: **CYCLE EXACT** option.
* **lr-puae**: **CPU COMPATIBILITY** option.

## Known issues

<table><thead><tr><th width="334">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>"Kickstart not found" or black screen</td><td>Copy kick40068.A1200 (Kickstart 3.1 A1200) to the bios folder.</td></tr><tr><td>Amiga Forever ROMs do not work</td><td>Copy rom.key next to them.</td></tr><tr><td>.ipf games do not start</td><td>Check that capsimg.dll is in the bios folder.</td></tr><tr><td>A floppy game does not start or freezes</td><td>Disable the Fast RAM (see Guides).</td></tr><tr><td>A 3D game is too slow</td><td>Enable the JIT (Amiberry, WinUAE).</td></tr><tr><td>The joystick does not respond in a game</td><td>The game wants the joystick in port 1: enable SWAP JOYSTICK PORTS (Amiberry, WinUAE).</td></tr><tr><td>The game asks for another disk</td><td>Use a .m3u file, or the WHDLoad version of the game.</td></tr><tr><td>The game needs the keyboard</td><td>Use your PC keyboard, the virtual keyboard (SELECT) or Pad2Key.</td></tr></tbody></table>
