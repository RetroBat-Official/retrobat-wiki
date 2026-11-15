---
description: Apple
---

# Apple II

<div align="left"><figure><img src="../../../../.gitbook/assets/image (587).png" alt="" width="424"><figcaption></figcaption></figure></div>

### Overview

The **Apple II** is one of the first personal computers sold in large numbers. Designed by Steve Wozniak, it was released in 1977, followed by the Apple II Plus (1979), the Apple //e (1983, then its "Enhanced" version in 1985) and the //c and //c Plus portables. Production ended in 1993. Its software ships on 5.25-inch floppy disks, read by the Disk II drive.

Its library is huge: **Lode Runner**, **Karateka**, **Prince of Persia**, **Ultima**, **Wizardry**, **Choplifter**, **The Oregon Trail**, **Castle Wolfenstein**, **Conan**, and many recent European demos.

RetroBat offers seven emulators: **AppleWin** (default), **POM2**, **Mednafen**, **BizHawk**, the **applewin** and **mame** libretro cores, and **MAME**.

{% embed url="https://en.wikipedia.org/wiki/Apple_II" %}

### At a glance

<table><thead><tr><th width="210.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\apple2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nib .do .po .dsk .woz .m3u .hdv .zip</td></tr><tr><td><strong>Default emulator</strong></td><td>applewin</td></tr><tr><td><strong>BIOS</strong></td><td>None for AppleWin and the applewin core</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic: Mednafen, applewin core; AppleWin uses the Windows controller; POM2, BizHawk, MAME: PadToKey</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk (managed by RetroBat)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>mame libretro core</td></tr><tr><td><strong>Optional BIOS</strong></td><td>POM2 ROMs in <code>bios\pom2</code>, Mednafen and BizHawk ROMs, MAME archives in <code>bios</code></td></tr></tbody></table>

### Which emulator should I use?

<table><thead><tr><th width="183.25">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>applewin</strong> (default)</td><td>The reference on Windows: very compatible, built-in ROMs, many screen types.</td><td>Cannot read <code>.zip</code> files. Save states not managed by RetroBat. Settings stored in the Windows registry.</td></tr><tr><td><strong>pom2</strong></td><td>Recent emulator: //e, //c, //c Plus and PAL (50 Hz) models for European demos, CRT filters, disk turbo, mouse as paddles.</td><td>Needs the ROMs in <code>bios\pom2</code>. One disk mounted at a time, no save states.</td></tr><tr><td><strong>mednafen</strong></td><td>Apple II, II+ and //e, controller set up automatically.</td><td>Needs its ROMs in <code>bios</code>. Cannot read <code>.zip</code> files.</td></tr><tr><td><strong>bizhawk</strong></td><td>Save states managed by RetroBat, RetroAchievements.</td><td>Needs <code>AppleIIe.rom</code> and <code>AppleIIe_DiskII.rom</code>. Keyboard only. Cannot read <code>.zip</code> files.</td></tr><tr><td><strong>libretro: applewin</strong></td><td>AppleWin inside RetroArch: save states, shaders, disk swapping, expansion cards.</td><td>—</td></tr><tr><td><strong>libretro: mame</strong>, <strong>mame</strong></td><td>MAME software lists, many expansion cards.</td><td>Need the MAME archives. No automatic controller setup.</td></tr></tbody></table>

### BIOS

**AppleWin** and the **applewin core** have their ROMs built in: nothing to install. The other emulators need their own files, all in `bios`:

<table><thead><tr><th width="180.75">Emulator</th><th width="399.25">Files</th><th>Folder</th></tr></thead><tbody><tr><td>POM2</td><td>ROM of the chosen machine and of its character generator, plus <code>disk2.rom</code> and <code>diskii_p6.rom</code> (see below)</td><td><code>bios\pom2</code></td></tr><tr><td>Mednafen</td><td><code>apple2-asoft-auto.rom</code>, <code>apple2-int-auto.rom</code>, <code>disk2-13boot.rom</code>, <code>disk2-13seq.rom</code>, <code>disk2-16boot.rom</code>, <code>disk2-16seq.rom</code></td><td><code>bios</code></td></tr><tr><td>BizHawk</td><td><code>AppleIIe.rom</code>, <code>AppleIIe_DiskII.rom</code></td><td><code>bios</code></td></tr><tr><td>MAME, mame core</td><td><code>apple2ee.zip</code> and <code>apple2e.zip</code> (Apple //e Enhanced, default model), <code>apple2.zip</code>, <code>apple2p.zip</code>, <code>a2diskiing.zip</code>, <code>d2fdc.zip</code>, <code>votrsc01a.zip</code>; <code>a2cffa2.zip</code> for <code>.hdv</code> hard disks</td><td><code>bios</code></td></tr></tbody></table>

The MAME software lists (`apple2_cass.xml`, `apple2_flop_clcracked.xml`, `apple2_flop_misc.xml`, `apple2_flop_orig.xml`) go in `bios\mame\hash`.

**POM2 ROMs** (POM2 names):

| Machine                      | System ROM                                               | Character ROM                                 |
| ---------------------------- | -------------------------------------------------------- | --------------------------------------------- |
| Apple //e Enhanced (default) | `apple2e.rom`                                            | `apple2e_char.rom`                            |
| Apple ]\[                    | `apple2o.rom` or `apple2.rom`                            | `apple2_char.rom`                             |
| Apple ]\[+                   | `apple2p.rom` or `apple2.rom`                            | `apple2_char.rom`                             |
| Apple //e Unenhanced         | `apple2e_unenh.rom` or `342-0135-b.64.rom`               | `apple2e_char_2k.rom` or `342-0133-a.chr.rom` |
| Apple //c                    | `apple2c-32Kv0.rom`, `apple2c-16K.rom` or `3420033a.256` | `apple2e_char.rom`                            |
| Apple //c Plus               | `apple2cp.rom` or `apple2c-plus.rom`                     | `apple2e_char.rom`                            |

Every machine also needs `diskii_p6.rom`, and all but the //c models need `disk2.rom`. RetroBat copies the ROMs from `bios\pom2` into the POM2 folder and shows the name of the missing file when a ROM is not found.

### Which game format?

<table><thead><tr><th width="209">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.woz</strong></td><td>Faithful copy of the floppy, copy protection included. The safest format for protected games.</td></tr><tr><td><strong>.dsk</strong>, <strong>.do</strong>, <strong>.po</strong></td><td>5.25-inch floppy images (DOS 3.3 or ProDOS order).</td></tr><tr><td><strong>.nib</strong></td><td>"Nibble" 5.25-inch floppy image.</td></tr><tr><td><strong>.hdv</strong></td><td>ProDOS hard disk image.</td></tr><tr><td><strong>.m3u</strong></td><td>List of the disks of a multi-disk game.</td></tr><tr><td><strong>.zip</strong></td><td>Only POM2 and MAME read archives.</td></tr></tbody></table>

### Controls

#### Setup per emulator

The Apple II is mostly played with the keyboard. To play with a controller, create a **PadToKey** profile (see the [**PadToKey**](../../../../controllers/pad2key.md) page). The Apple II game port takes a two-button analog joystick, or two paddles.

* **AppleWin**: the first Windows controller acts as the joystick (otherwise the keyboard arrows). **CONTROLS > PLAYER 1 JOYSTICK TYPE** / **PLAYER 2**: joystick, keyboard (arrows or numeric keypad) or mouse.
* **applewin core**: **CONTROLS > PLAYER 1 DEVICE**: controller with the d-pad (default), controller with the analog stick (progressive movement, for paddles), or mouse as paddles. **KEYBOARD TYPE**: ASCII (default) or the machine's original keyboard. **KEYBOARD FOCUS** gives the whole keyboard to the game (Scroll Lock toggles it).
* **Mednafen**: controller set up automatically, SOUTH / EAST = buttons 1 / 2, L1 = paddle resistance selection. **CONTROLS > CONTROLLER TYPE**: joystick (analog stick), gamepad (d-pad) or Atari joystick.
* **POM2**: **CONTROLS > CONTROLLER FOR THE GAME PORT** picks the controller (automatic by default). **MOUSE DRIVES THE PADDLES** for Arkanoid, Breakout and paddle games, **PADDLE MOUSE RANGE**, **STICK DEAD ZONE**.
* **BizHawk**: Apple //e keyboard only.
* **MAME, mame core**: **CONTROLS > JOYSTICK TYPE** (Apple, Sirius / Atari for the Apple II Plus, Gizmo).

#### Hotkeys

**libretro cores, Mednafen, BizHawk, MAME**: RetroBat default hotkeys (save, load, screenshot…). For more details, see the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

**AppleWin, POM2**

<table><thead><tr><th width="274">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr></tbody></table>

AppleWin keeps its own keyboard keys: `F11` / `F12` save and load a snapshot (not managed by RetroBat).

### Writing to floppy disks

Many Apple II games save your progress directly on their floppy. RetroBat never changes the files in `roms\apple2`. The **EMULATION > ALLOW GAMES TO WRITE TO DISK IMAGES** option (AppleWin, applewin core, POM2, Mednafen, BizHawk) decides what happens:

<table><thead><tr><th width="284">Choice</th><th>Effect</th></tr></thead><tbody><tr><td><strong>NO (READ ONLY)</strong> (default)</td><td>The floppy is write-protected: the game cannot save.</td></tr><tr><td><strong>YES (WORKING COPY IN SAVES)</strong></td><td>The game runs on a copy of the floppy, created on first launch in <code>saves\apple2\&#x3C;emulator></code> and then reused: progress is kept between sessions.</td></tr><tr><td><strong>YES AND RESET THE DISK</strong></td><td>Starts again from the original floppy (the old copy is kept as <code>.bak</code>).</td></tr></tbody></table>

Mednafen and BizHawk keep the changes in their own files instead of a copy of the floppy: the reset sets them aside the same way.

### Folders

| Content                                       | Folder                                                   |
| --------------------------------------------- | -------------------------------------------------------- |
| ROMs (POM2)                                   | `bios\pom2`                                              |
| ROMs (Mednafen, BizHawk, MAME)                | `bios`                                                   |
| AppleWin: working copies of the floppies      | `saves\apple2\applewin`                                  |
| AppleWin: configuration                       | Windows registry (`HKEY_CURRENT_USER\SOFTWARE\AppleWin`) |
| applewin core: working copies of the floppies | `saves\apple2`                                           |
| applewin core: save states                    | `saves\apple2\libretro.applewin`                         |
| POM2: working copies of the floppies          | `saves\apple2\pom2`                                      |
| POM2: configuration                           | `emulators\pom2\POM2\state.cfg`                          |
| Mednafen: floppy changes                      | `saves\apple2` (`<game>.<n>.afd.gz`, `<game>.0.ahd.gz`)  |
| BizHawk: floppy changes                       | `saves\apple2\bizhawk` (`<game>.SaveRAM`)                |
| BizHawk: save states                          | `saves\apple2\bizhawk\sstates\AppleII`                   |
| MAME software lists                           | `bios\mame\hash`                                         |

### Guides

#### Multi-disk games

Create a `.m3u` file in `roms\apple2`, with one line per floppy, in order:

```
Ultima IV (Disk 1).woz
Ultima IV (Disk 2).woz
```

* **AppleWin** and **MAME** load the first two floppies in drives 1 and 2.
* **applewin core**: swap disks with the RetroArch hotkeys; **EMULATION > USE BOTH FLOPPY DRIVES** loads the first two in drives 1 and 2, **M3U START DISK** resumes from the last disk used.
* **POM2** mounts a single disk: **EMULATION > DISC NUMBER (M3U)** picks the one to boot, the others are swapped from the game menu.

#### European demos (50 Hz)

Some demos and a few European programs were written for a PAL Apple //e. Pick a PAL model in POM2 (**EMULATION > MACHINE TYPE**), or set **EMULATION > VIDEO REFRESH RATE** to 50 Hz with the applewin core.

#### Hard disks (.hdv)

AppleWin and the applewin core read `.hdv` files through the slot 7 hard disk controller (enabled by default). With MAME and the mame core, add `a2cffa2.zip` to `bios` and choose **EMULATION > FORCE MEDIA TYPE > Hard Drive Image**: RetroBat then installs the CFFA 2.0 card in slot 7.

#### Other useful options

<table><thead><tr><th width="355.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > MACHINE TYPE</strong></td><td>Apple II model (AppleWin, applewin core, POM2).</td></tr><tr><td><strong>VISUAL RENDERING > SCREEN TYPE</strong></td><td>RGB color, composite (period color bleeding), TV, or green / amber / white monochrome monitor.</td></tr><tr><td><strong>VISUAL RENDERING > SCANLINES</strong> (applewin core), <strong>CRT EFFECTS</strong> (POM2)</td><td>Look of a cathode-ray tube.</td></tr><tr><td><strong>EXPANSION SLOTS > SLOT 4</strong> (applewin core), <strong>SLOT 4 SOUND CARD</strong> (POM2)</td><td>Mockingboard sound card (default), Phasor, mouse card…</td></tr><tr><td><strong>EMULATION > DISK TURBO</strong> (POM2)</td><td>Much faster loading.</td></tr><tr><td><strong>EMULATION > CHARACTER ROM</strong> (POM2)</td><td>French, British, German… character set.</td></tr></tbody></table>

### Known issues

<table><thead><tr><th width="347.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game shows a write error or does not keep progress</td><td>Enable <strong>EMULATION > ALLOW GAMES TO WRITE TO DISK IMAGES</strong>.</td></tr><tr><td>A <code>.zip</code> does not start with AppleWin, Mednafen or BizHawk</td><td>These emulators cannot read archives: unzip the game, or use POM2.</td></tr><tr><td>POM2 says "Missing POM2 ROM"</td><td>Add the listed ROM to <code>bios\pom2</code>.</td></tr><tr><td>A protected game does not boot</td><td>Use the <code>.woz</code> version of the game.</td></tr><tr><td>The game does not react to the controller</td><td>Create a PadToKey profile, or check the emulator's joystick type.</td></tr></tbody></table>
