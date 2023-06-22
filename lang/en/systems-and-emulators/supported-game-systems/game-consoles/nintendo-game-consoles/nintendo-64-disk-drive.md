---
description: Nintendo
---

# Nintendo 64 Disk Drive

<div align="left">

<figure><img src="https://hyperspin-fe.com/siteuploads/downloads/screenshots/monthly_2018_03/5ab59a08f060d_Nintendo64dd.png.37360958cf54c2250cba823a58c0fad2.png" alt=""><figcaption></figcaption></figure>

</div>

Game Console - Lifespan: 1999- 2001

{% embed url="https://en.wikipedia.org/wiki/64DD" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: mupen64plus next</li><li>libretro: parallel_n64 (only for full NDD games)</li><li>project64</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> n64dd</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.v64 .z64 .n64 .ndd</td><td></td></tr></tbody></table>

## BIOS

<table data-header-hidden><thead><tr><th width="206"></th><th width="533"></th><th data-hidden></th></tr></thead><tbody><tr><td>IPL_JAP.n64<br>Japan</td><td><strong>location:</strong> \bios\Mupen64plus<br><strong>md5:</strong> <code>8d3d9f294b6e174bc7b1d2fd1c727530</code></td><td></td></tr><tr><td>IPL_USA.n64<br>USA</td><td><strong>location:</strong> \bios\Mupen64plus<br><strong>md5:</strong> <code>37c36e4286d36892a9fc70eafe4104be</code></td><td></td></tr><tr><td>IPL_DEV.n64<br>Development Kit</td><td><strong>location:</strong> \bios\Mupen64plus<br><strong>md5:</strong> </td><td></td></tr></tbody></table>

## Controls

Same as [N64](nintendo-64.md#controls)

## Specific System Information

### Running Games with Mupen64plus\_next core

There are two types of games on the Nintendo 64DD, full games and game expansions.&#x20;

In order to get n64dd games running successfully, it is required to have **two files per game**.&#x20;

* a .n64 or .z64 game rom
* a .ndd file (which contains the hard drive part of the game)

Both files need to have the exact same filename and in the case of the n64dd .ndd file, it must have a double extension with the same extension than the n64 rom file, added before its own extension.

#### Running a n64dd game extension

In the case of game expansion like the one in the example below, the n64 game is the actual ROM file for which the n64dd .ndd file is the expansion.&#x20;

Example filenames with the expansion "F-Zero X Expansion Kit":

* Rename n64dd .ndd file\
  `F-Zero X - Expansion Kit (Japan).ndd`\
  to\
  `F-Zero X - Expansion Kit (Japan).n64.ndd`
* Rename n64 rom file\
  `F-Zero X (Japan).n64`\
  &#x20;to \
  `F-Zero X - Expansion Kit (Japan).n64`
* Run expansion with\
  `F-Zero X - Expansion Kit (Japan).n64`

Now from RetroBat:&#x20;

* [Select the right BIOS](nintendo-64-disk-drive.md#bios-selection)
* Launch the .n64 (or .z64) file, not the .ndd file:

<div align="left">

<figure><img src="https://i.imgur.com/dlLRJ9Q.png" alt=""><figcaption></figcaption></figure>

</div>

#### Running a n64dd full game

For the full games, you also always need two files, so the n64dd .ndd file of the full game and another n64 rom of any title that you just need to rename (pick any game from the same region as the full ndd game).\


Example with the full game "SimCity 64":

* Rename `SimCity 64 (Japan).ndd` to `SimCity 64 (Japan).n64.ndd`
* Pick any n64 roms file and rename it `SimCity 64 (Japan).n64`
* Then run `SimCity 64 (Japan).n64` in RetroBat.

Now from RetroBat:&#x20;

* [Select the right BIOS](nintendo-64-disk-drive.md#bios-selection)
* Launch the .n64 (or .z64) file, not the .ndd file:

<div align="left">

<figure><img src="https://i.imgur.com/PaYnyTC.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="warning" %}
WARNING: the core is very picky with the .ndd dump used.

If you notice that the running game is the one from the "fake .n64 or .z64 rom used", it usually means that you are not using a correct .ndd file dump.
{% endhint %}

### Running Games with parallel\_n64 core

Parallel\_n64 core can run directly .ndd files, however it is only possible to run full N64DD games as of now (such as SimCity64), game extensions will not run with this core.

Just place the full .ndd game in your `\roms\n64dd` folder, select the parallel\_n64 core in RetroBat and the [right BIOS](nintendo-64-disk-drive.md#bios-selection), and launch the .ndd game.

### BIOS selection

Althrough only commercialized in Japan, US games are available for the n64dd system, as well as prototypes using a specific "dev" BIOS.

The right BIOS can be selected directly in Retrobat Games Options menu, per game.

<div align="left">

<figure><img src="https://i.imgur.com/htqkK3Q.png" alt=""><figcaption><p>Advanced System Options / Emulation / BIOS</p></figcaption></figure>

</div>
