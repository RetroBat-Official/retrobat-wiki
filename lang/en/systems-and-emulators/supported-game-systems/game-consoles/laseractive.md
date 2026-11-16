---
description: Pioneer
---

# Pioneer LaserActive

<div align="left"><figure><img src="../../../.gitbook/assets/image (595).png" alt="" width="480"><figcaption></figcaption></figure></div>

## Overview

The **LaserActive** is a Pioneer LaserDisc player released in 1993 (CLD-A100). It becomes a game console with modules inserted at the front, the "PACs":

* the **Mega-LD PAC** (Sega) plays Mega-LD discs, as well as Mega Drive cartridges and Mega-CD discs;
* the **LD-ROM² PAC** (NEC) plays LD-ROM² discs, as well as PC Engine HuCards and CD-ROM² discs.

LaserActive games mix the analog LaserDisc video with the game data: high-quality full-motion video, interactive movies, shooters over video backgrounds. About 24 Mega-LD and 14 LD-ROM² games were released, such as **Pyramid Patrol**, **Hyperion**, **Triad Stone**, **J.B. Harold: Blue Chicago Blues** (Mega-LD) or **Vajra** and **Road Prosecutor** (LD-ROM²).

Emulation is recent: ares is the first emulator to run the Mega-LD (2025), then the LD-ROM². RetroBat offers **ares** with two cores, one per PAC (**MegaLD** by default, **NecLD**), and the **geargrafx** libretro core (LD-ROM² only).

Mega Drive, Mega-CD and PC Engine games are launched from their own systems: this system is only for LaserActive discs.

{% embed url="https://en.wikipedia.org/wiki/LaserActive" %}

## At a glance

<table><thead><tr><th width="235.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\laseractive</code></td></tr><tr><td><strong>Extensions</strong></td><td>.mmi</td></tr><tr><td><strong>Default emulator</strong></td><td>ares (MegaLD)</td></tr><tr><td><strong>BIOS</strong></td><td>Required, one per PAC (see below)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, every emulator</td></tr><tr><td><strong>Save states</strong></td><td>geargrafx core; ares with hotkeys (not managed by RetroBat)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>geargrafx core (LD-ROM²)</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>syscard1.pce</code>, <code>gexpress.pce</code> in <code>bios</code> (some LD-ROM² games)</td></tr></tbody></table>

## Which emulator should I use?

The core depends on the disc: a Mega-LD disc only runs with **MegaLD**, an LD-ROM² disc only with **NecLD** or **geargrafx**. LD-ROM² games must therefore be set to one of these two cores.

<table><thead><tr><th width="182">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>ares: MegaLD</strong> (default)</td><td>Only Mega-LD emulator. Every Mega-LD game dumped so far is playable.</td><td>Mega-LD discs only. Save states not managed by RetroBat.</td></tr><tr><td><strong>ares: NecLD</strong></td><td>Original LD-ROM² emulation, by the author of the Mega-LD emulation.</td><td>LD-ROM² discs only. Save states not managed by RetroBat.</td></tr><tr><td><strong>libretro: geargrafx</strong></td><td>LD-ROM² in RetroArch: save states managed by RetroBat, shaders, netplay.</td><td>LD-ROM² discs only.</td></tr></tbody></table>

## BIOS

Each PAC has its own BIOS: place the one for the PAC of your games (or both) in `bios\laseractive`.

**Mega-LD PAC (ares MegaLD)**: the BIOS matching the disc region (US or Japan) is required.

<table><thead><tr><th>File</th><th width="134.5">Region</th><th>Folder</th></tr></thead><tbody><tr><td><code>[BIOS] LaserActive PAC-S10 (US) (v1.04).bin</code></td><td>US</td><td><code>bios\laseractive</code></td></tr><tr><td><code>[BIOS] LaserActive PAC-S1 (Japan) (v1.05).bin</code></td><td>Japan</td><td><code>bios\laseractive</code></td></tr></tbody></table>

RetroBat also accepts older versions, when the previous one is missing: `[BIOS] LaserActive PAC-S10 (US) (v1.02).bin`, `[BIOS] LaserActive PAC-S1 (Japan) (v1.02).bin` and `[BIOS] LaserActive PAC-S1 (Japan) (v1.01).bin`.

**LD-ROM² PAC (ares NecLD, geargrafx core)**: one of these files is enough.

<table><thead><tr><th width="326">File</th><th width="174.5">Region</th><th>Folder</th></tr></thead><tbody><tr><td><code>[BIOS] LaserActive PAC-N10 (US) (v1.02).bin</code></td><td>US</td><td><code>bios\laseractive</code></td></tr><tr><td><code>[BIOS] LaserActive PAC-N1 (Japan) (v1.02).bin</code></td><td>Japan</td><td><code>bios\laseractive</code></td></tr><tr><td><code>[BIOS] LaserActive PCE-LP1 (Japan) (v1.02).bin</code></td><td>Japan (PAC sold by NEC)</td><td><code>bios\laseractive</code></td></tr></tbody></table>

The geargrafx core uses the same files: RetroBat copies them to the root of `bios` under the names the core expects (`pac-n10.bin`, `pac-n1.bin`, `pce-lp1.bin`).

**Optional BIOS (ares NecLD, geargrafx core)**: some LD-ROM² games need a PC Engine card inserted in the console.

| File           | Description                    | Folder |
| -------------- | ------------------------------ | ------ |
| `syscard1.pce` | System Card 1.0 (PC Engine CD) | `bios` |
| `gexpress.pce` | Games Express                  | `bios` |

With the geargrafx core, **EMULATION > CDROM BIOS** selects the System Card used by these games: SYSTEM CARD 1 by default if `syscard1.pce` is present, otherwise SYSTEM CARD 3 (`syscard3.pce`).

## Which game format?

<table><thead><tr><th width="149">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.mmi</strong></td><td>Mixed Media Image: one file per disc side, with the video, the sound and the game data. It is the only format read by ares and geargrafx.</td></tr></tbody></table>

* Files are very large: 28 to 36 GB per side for most games, more for some.
* The format is already compressed: do not put it in a `.zip` or `.7z` archive.
* Put the games on an **SSD**: a regular hard drive is too slow to read the video without stutter.
* A recent mid-range PC is enough to play at full speed.

## Controls

### Automatic setup

**Mega-LD PAC (ares MegaLD)**: 6-button Mega Drive controller.

<table><thead><tr><th width="249">RetroBat controller</th><th>Mega Drive</th></tr></thead><tbody><tr><td>WEST / SOUTH / EAST</td><td>A / B / C</td></tr><tr><td>L1 / NORTH / R1</td><td>X / Y / Z</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>MODE</td></tr><tr><td>D-pad</td><td>D-pad</td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (597).png" alt="" width="225"><figcaption></figcaption></figure></div>

**LD-ROM² PAC (ares NecLD, geargrafx core)**: PC Engine controller.

<table><thead><tr><th width="230.25">RetroBat controller</th><th>PC Engine</th></tr></thead><tbody><tr><td>EAST / SOUTH</td><td>I / II</td></tr><tr><td>START</td><td>RUN</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>D-pad</td><td>D-pad</td></tr></tbody></table>

With the geargrafx core, **CONTROLS > CONTROLLER TYPE** selects the controller: PC ENGINE PAD (default), AVENUE PAD 3 or AVENUE PAD 6. **CONTROLS > USE TURBO-TAP** plugs in the multitap.

<div align="left"><figure><img src="../../../.gitbook/assets/image (596).png" alt="" width="225"><figcaption></figcaption></figure></div>

### Hotkeys

ares uses the RetroBat hotkeys (through PadToKey):

<table><thead><tr><th width="203.25">Action</th><th width="222">Controller</th><th>Keyboard</th></tr></thead><tbody><tr><td>Exit</td><td>HOTKEY + START</td><td><code>Esc</code></td></tr><tr><td>Pause</td><td>HOTKEY + SOUTH</td><td><code>P</code></td></tr><tr><td>Save state</td><td>HOTKEY + WEST</td><td><code>F2</code></td></tr><tr><td>Load state</td><td>HOTKEY + NORTH</td><td><code>F4</code></td></tr><tr><td>Previous / next slot</td><td>HOTKEY + Down / Up</td><td><code>F6</code> / <code>F7</code></td></tr><tr><td>Rewind (if enabled)</td><td>HOTKEY + Left</td><td><code>Backspace</code></td></tr><tr><td>Fast forward (hold)</td><td>HOTKEY + Right</td><td><code>L</code></td></tr><tr><td>Screenshot</td><td>HOTKEY + R3</td><td><code>F8</code></td></tr><tr><td>Fullscreen</td><td>HOTKEY + L3</td><td><code>F</code></td></tr></tbody></table>

The geargrafx core uses the RetroArch hotkeys.

For more details, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="259">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\laseractive</code></td></tr><tr><td>BIOS</td><td><code>bios\laseractive</code> (and <code>bios</code> for <code>syscard1.pce</code> and <code>gexpress.pce</code>)</td></tr><tr><td>ares: saves</td><td><code>saves\laseractive\ares</code></td></tr><tr><td>geargrafx core: saves</td><td><code>saves\laseractive</code></td></tr><tr><td>geargrafx core: save states</td><td><code>saves\laseractive\libretro.geargrafx</code></td></tr><tr><td>ares: screenshots</td><td><code>screenshots\ares</code></td></tr></tbody></table>

## Guides

### Changing disc side (ares)

Some games span several sides (**J.B. Harold: Blue Chicago Blues**, for example), with one `.mmi` file per side. ares has no hotkey to change side:

1. When the game asks you to flip the disc, switch to windowed mode with HOTKEY + L3 (or `F`).
2. In the ares menu bar, open **LaserActive (SEGA PAC) > Change Side** (or **LaserActive (NEC PAC) > Change Side**) and select the requested side.
3. Go back to fullscreen with HOTKEY + L3.

### LD-ROM² PAC region (geargrafx)

**EMULATION > LASERACTIVE REGION** selects the BIOS used: JAPAN (`PAC-N1` or `PCE-LP1`) or US (`PAC-N10`). By default, the core chooses automatically.

**VIDEO > LASERACTIVE ASPECT RATIO** changes the picture format: 4:3 by default, or 1:1 PAR, 16:9 DAR, 16:10 DAR.

## Known issues

<table><thead><tr><th width="354">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>An LD-ROM² disc does not start</td><td>The game is launched with the MegaLD core (default): select the NecLD or geargrafx core for this game.</td></tr><tr><td>ares asks for the "Mega LD - BIOS (US)" or "(Japan)" firmware</td><td>The Mega-LD BIOS for the disc region is missing in <code>bios\laseractive</code>.</td></tr><tr><td>ares NecLD asks for the "PAC-N10 (US)" or "PAC-N1 (Japan)" firmware</td><td>No LD-ROM² BIOS in <code>bios\laseractive</code>: any of the three files is enough.</td></tr><tr><td>ares NecLD asks for the "System-Card 1.0" or "Games Express" firmware, or the geargrafx core does not start the game</td><td>This LD-ROM² game needs the matching PC Engine card: place <code>syscard1.pce</code> or <code>gexpress.pce</code> in <code>bios</code>.</td></tr><tr><td>The video stutters</td><td>Put the games on an SSD and do not compress them.</td></tr><tr><td>The game asks you to flip the disc</td><td>See <strong>Changing disc side</strong> in <a href="laseractive.md#changing-disc-side-ares"><strong>Guides</strong></a>.</td></tr></tbody></table>
