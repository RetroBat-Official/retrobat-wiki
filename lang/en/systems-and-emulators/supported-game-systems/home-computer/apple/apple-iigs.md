---
description: Apple
---

# Apple IIGS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (588).png" alt="" width="540"><figcaption></figcaption></figure></div>

### Overview

The **Apple IIGS** is the last model of the Apple II line. Released in 1986, it is built around a 16-bit 65C816 processor, a 4,096-color palette and the 32-voice Ensoniq sound chip, the same one found in the brand's synthesizers. It remains compatible with Apple II software and reads 800 KB 3.5-inch floppy disks. Production ended in 1992.

Its games include **Dungeon Master**, **Silpheed**, **Zany Golf**, **The Immortal**, **Rastan**, **Arkanoid II**, **Out of This World**, **Wolfenstein 3D**, **Xenocide** and **Dragon Wars**.

RetroBat offers three emulators: **GSplus** (default), the **mame** libretro core and **MAME**.

{% embed url="https://en.wikipedia.org/wiki/Apple_IIGS" %}

### At a glance

<table><thead><tr><th width="234"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\apple2gs</code></td></tr><tr><td><strong>Extensions</strong></td><td>.2mg .woz .m3u .hdv .zip</td></tr><tr><td><strong>Default emulator</strong></td><td>gsplus</td></tr><tr><td><strong>BIOS</strong></td><td>Apple IIGS ROM in <code>bios</code>: <code>APPLE2GS.ROM</code> (or <code>ROM</code>, <code>ROM.01</code>, <code>ROM.03</code>) for GSplus, <code>apple2gs.zip</code> for MAME</td></tr><tr><td><strong>Controller setup</strong></td><td>GSplus: the first controller acts as the joystick; MAME: PadToKey</td></tr><tr><td><strong>Save states</strong></td><td>mame libretro core</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>mame libretro core</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>votrsc01a.zip</code> and MAME software lists</td></tr></tbody></table>

### Which emulator should I use?

<table><thead><tr><th width="149.5">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>gsplus</strong> (default)</td><td>Light and fast, mounts every disk of a <code>.m3u</code> at once, hard disks, scanlines.</td><td>Cannot read <code>.woz</code> files. No save states managed by RetroBat.</td></tr><tr><td><strong>libretro: mame</strong></td><td>Reads <code>.woz</code> files, save states, RetroArch shaders and hotkeys, MAME software lists.</td><td>Needs <code>apple2gs.zip</code>. No automatic controller setup.</td></tr><tr><td><strong>mame</strong></td><td>Same emulation as the mame core, as a standalone emulator.</td><td>Needs <code>apple2gs.zip</code>. No automatic controller setup.</td></tr></tbody></table>

### BIOS

<table><thead><tr><th width="197">Emulator</th><th width="377.5">Files</th><th>Folder</th></tr></thead><tbody><tr><td>GSplus</td><td>Apple IIGS ROM (ROM 01 or ROM 03) under one of these names: <code>ROM</code>, <code>ROM.01</code>, <code>ROM.03</code> or <code>APPLE2GS.ROM</code></td><td><code>bios</code></td></tr><tr><td>MAME, mame core</td><td><code>apple2gs.zip</code>; <code>votrsc01a.zip</code> optional</td><td><code>bios</code></td></tr></tbody></table>

When several ROMs are present, GSplus takes the first one found in the order `ROM`, `ROM.01`, `ROM.03`, `APPLE2GS.ROM`. The `APPLE2GS.ROM` file checked by RetroBat has the md5 `20a0334c447cb069a040ae5be1d938df`.

The MAME software lists (`apple2gs_flop_clcracked.xml`, `apple2gs_flop_misc.xml`, `apple2gs_flop_orig.xml`) go in `bios\mame\hash`.

<details>

<summary>Content of apple2gs.zip</summary>

```
"apple2gs.zip"
- "341-0728" size="131072" crc="8d410067" sha1="c0f4704233ead14cb8e1e8a68fbd7063c56afd27"
- "341-0748" size="131072" crc="18190283" sha1="c70576869deec92ca82c78438b1d5c686eac7480"
- "341s0632-2.bin" size="4096" crc="e1c11fb0" sha1="141d18c36a617ab9dce668445440d34354be0672"
- "344s0047.bin" size="16384" crc="2d541944" sha1="5a5a77c8ec45632aea1a57cd9c9257f7f6e44668"
```

</details>

### Which game format?

<table><thead><tr><th width="165.25">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.2mg</strong></td><td>3.5-inch floppy (800 KB) or hard disk image. The most common format.</td></tr><tr><td><strong>.woz</strong></td><td>Faithful copy of the floppy, copy protection included. Only read by MAME and the mame core.</td></tr><tr><td><strong>.hdv</strong></td><td>ProDOS hard disk image.</td></tr><tr><td><strong>.m3u</strong></td><td>List of the disks of a multi-disk game.</td></tr><tr><td><strong>.zip</strong></td><td>Archive holding the game image.</td></tr></tbody></table>

### Controls

#### Setup per emulator

The Apple IIGS is played with the keyboard, the mouse and a two-button analog joystick. For keyboard keys, create a **PadToKey** profile (see the [**PadToKey**](../../../../controllers/pad2key.md) page).

* **GSplus**: the first connected controller acts as the joystick (analog stick and two buttons). The Apple IIGS mouse follows the PC mouse. **CONTROLS > SWAP PADDLES** and **INVERT PADDLES** for the few games that expect the axes the other way round.
* **MAME, mame core**: **CONTROLS > JOYSTICK TYPE** (Apple or Gizmo).

#### Hotkeys

**mame core, MAME**: RetroBat default hotkeys (save, load, screenshot…). For more details, see the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

**GSplus**

<table><thead><tr><th width="215.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr></tbody></table>

On the keyboard, `F4` opens the GSplus configuration menu.

### Writing to floppy disks

With GSplus, the **EMULATION > ALLOW GAMES TO WRITE TO DISK IMAGES** option decides whether a game can save on its floppy:

<table><thead><tr><th width="279">Choice</th><th>Effect</th></tr></thead><tbody><tr><td><strong>NO (READ ONLY)</strong> (default)</td><td>The floppy is write-protected: the game cannot save.</td></tr><tr><td><strong>YES (WORKING COPY IN SAVES)</strong></td><td>The game runs on a copy of the floppy, created on first launch in <code>saves\apple2gs\gsplus</code> and then reused: progress is kept between sessions.</td></tr><tr><td><strong>YES AND RESET THE DISK</strong></td><td>Starts again from the original floppy (the old copy is kept as <code>.bak</code>).</td></tr></tbody></table>

The files in `roms\apple2gs` are never changed.

### Folders

<table><thead><tr><th width="324">Content</th><th>Folder</th></tr></thead><tbody><tr><td>ROMs</td><td><code>bios</code></td></tr><tr><td>MAME software lists</td><td><code>bios\mame\hash</code></td></tr><tr><td>GSplus: working copies of the floppies</td><td><code>saves\apple2gs\gsplus</code></td></tr><tr><td>GSplus: configuration</td><td><code>emulators\gsplus\config.txt</code></td></tr><tr><td>GSplus: screenshots</td><td><code>screenshots</code></td></tr><tr><td>mame core: save states</td><td><code>saves\apple2gs\libretro.mame</code></td></tr></tbody></table>

### Guides

#### Multi-disk games

Create a `.m3u` file in `roms\apple2gs`, with one line per floppy, in order. The images must be in the same folder as the `.m3u`. Example for Silpheed:

* **GSplus** mounts every floppy at once: the game finds the next disk by itself, nothing to do.
* **MAME** and the **mame core** load the first two floppies in the two 3.5-inch drives.

#### The game does not boot with GSplus

GSplus picks the drive from the image size: 5.25-inch floppies go to slot 6, 3.5-inch floppies and hard disks to slot 7. If a game refuses to boot, try another choice in **EMULATION > DISK SLOT**.

#### Other useful options

<table><thead><tr><th width="347.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>VISUAL RENDERING > SCANLINES</strong> (GSplus)</td><td>Look of a cathode-ray tube, from light to strong.</td></tr><tr><td><strong>VISUAL RENDERING > IGNORE ASPECT RATIO</strong> (GSplus)</td><td>Picture stretched to the whole screen.</td></tr><tr><td><strong>VISUAL RENDERING > BLACK AND WHITE</strong> (GSplus)</td><td>Monochrome monitor display.</td></tr><tr><td><strong>EMULATION > RAM SIZE</strong> (MAME)</td><td>From 1 to 8 MB.</td></tr><tr><td><strong>EXPANSION SLOTS</strong> (MAME)</td><td>Mockingboard sound card, 4play joystick card, MIDI card.</td></tr></tbody></table>

### Known issues

| Issue                                                | Solution                                                                  |
| ---------------------------------------------------- | ------------------------------------------------------------------------- |
| A `.woz` does not start with GSplus                  | GSplus cannot read this format: pick the mame core or MAME for this game. |
| GSplus starts on an empty screen or without a system | Check the Apple IIGS ROM in `bios` (see [**BIOS**](apple-iigs.md#bios)).  |
| A game refuses to boot with GSplus                   | Change **EMULATION > DISK SLOT**.                                         |
| The game does not keep progress                      | Enable **EMULATION > ALLOW GAMES TO WRITE TO DISK IMAGES** (GSplus).      |
