# Old computers - MAME/MESS - launch arguments

MAME (MESS) can emulate a huge variety of old computers. These computers often do require specific command lines to be used in order to attach devices, change RAM size, autoboot content, etc.

Though RetroBat has integrated several options directly available from it's interface, we have left users with the ability to add their own command lines for specific systems or games.

As an example, RetroBat can launch the TI99 system in MAME with the following arguments:

<mark style="background-color:$warning;">`ti99_4a`</mark>` ``-ioport peb -ioport:peb:slot2 32kmem -ioport:peb:slot4 speechadapter -ioport speechsyn -cart alpiner`

## Computer models

The first command launched represents the Computer Model (<mark style="background-color:$warning;">`ti99_4a`</mark>)

When a computer has multiple models (e.g. Camputers Lynx models 48K, 96K or 128K), RetroBat usually offers the option to select the computer model to emulate, the option can be found in the **ADVANCED SETTINGS > EMULATION** menu:

<div align="left"><figure><img src="../.gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
The BIOS of the model must be in the bios\ folder (or bios\mess\\).
{% endhint %}

## Expansion slots

The second part of the command example represents additional slots or devices that can be enabled for a computer (`-ioport peb -ioport:peb:slot2 32kmem -ioport:peb:slot4 speechadapter -ioport speechsyn`)

RetroBat has selected a few important devices and slots for several computer models, these are located in the **ADVANCED SETTINGS > EXPANSION SLOTS** menu:

<div align="left"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
If a slot/device is missing, you can ask the RetroBat team to add the option to RetroBat, or use the [additional command line](old-computers-mame-mess-launch-arguments.md#additional-command-line-arguments) guide below.
{% endhint %}

## Media Type

Old computers could accept multiple media types (diskette, cartridge, rom...), this is illustrated in the example with the last part of the command line before the game name (`-cart`)

RetroBat will automatically detect the media type based on the extension of the game filen, however, it is possible to force the media type, the option can be found in the **ADVANCED SETTINGS > EMULATION** menu:

<div align="left"><figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

## Autoboot command and delay

Some computers need a command typed at launch. RetroBat uses the first source available, in this order:

1. **Autorun file:** a file with the same name as the game and the `.autorun` extension, in the game folder. Line 1 is the boot command, line 2 (optional) the delay in seconds (3 by default). For `3DBRICK.dsk`, a `3DBRICK.autorun` file gives: `-autoboot_command "LOADM\"3DBRICK\":EXEC\r" -autoboot_delay 5`

<div align="left"><figure><img src="../.gitbook/assets/image (419).png" alt=""><figcaption></figcaption></figure></div>

2. **LUA script:** a script named after the software list of the media (for example `bbcb_flop.lua`), in `bios\mame\autoboot_scripts`. Used when **ADVANCED SETTINGS > EMULATION > TRY TO AUTOBOOT** is set to **FROM LUA SCRIPT**, and by default for BBC Micro, Camputers Lynx, CD-i, CreatiVision, Electron, Odyssey², TVC 64 and VG 5000.
3. **MAME hash file:** the boot command written in the MAME software list (`bios\mame\hash`), when **TRY TO AUTOBOOT** is set to **FROM HASH FILE**.

<div align="left"><figure><img src="../.gitbook/assets/image (420).png" alt=""><figcaption></figcaption></figure></div>

4. **ROM name brackets (BBC Micro):** with **TRY TO AUTOBOOT** set to **FROM ROM NAME BRACKETS**, the text between brackets is used as the file to run: `Elite [ELITE].ssd` launches `chain"ELITE"`.
5. **Internal logic:** RetroBat applies built-in commands by system and media type. For example, the Oric uses `CLOAD""\n`.

## Joystick Type

Example of command line argument for apple2: `-gameio joy`

Some computers could use different types of controller devices, the option to enable/change the controller type connected can usually be found in the **ADVANCED SETTINGS > CONTROLS** menu:

<div align="left"><figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
If a controller type is missing, you can ask the RetroBat team to add the option to RetroBat, or use the [additional command line](old-computers-mame-mess-launch-arguments.md#additional-command-line-arguments) guide below.
{% endhint %}

## Other options

<table><thead><tr><th width="319">Option (ADVANCED SETTINGS > EMULATION)</th><th>Use</th></tr></thead><tbody><tr><td><strong>FORCE SOFTLIST</strong></td><td>Forces the use of a MAME software list (from <code>bios\mame\hash</code>) instead of the media type detected from the extension.</td></tr><tr><td><strong>USE FULL ROM PATH</strong></td><td>Sends the full path of the game to MAME instead of its name only.</td></tr><tr><td><strong>ADD USER DISK</strong> (FM Towns)</td><td>Inserts a floppy disk in addition to the CD: a blank disk, or a system disk named after the game (<code>.hdm</code>) placed in <code>saves\mame\fmtowns</code>.</td></tr></tbody></table>

**Multi-disk games (.m3u):** for Apple II and Apple IIGS, the first two disks of the `.m3u` file are inserted in drives 1 and 2. For the other systems, only a single-disk `.m3u` is supported.

## Additional command line arguments

Additionnaly, it is possible to add custom command line arguments to the already existing arguments.

Arguments can be added either for a machine type/computer model, or for a specific game.

The files explained hereunder need to be placed in the same folder as the game rom that is launched.

### Adding command line for a specific game

RetroBat will check if a file, with the same name as the game rom file and with extension .commands, exists.

If this is the case, RetroBat will read the file, and add each line as an additional argument when launching the game:

<div align="left"><figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

As an example, the above file will work for the **alpiner.zip** game file, and will add the following command line:&#x20;

```
-cart "C:\retrobat\bios\ti99\Extended Basic v110.rpk"
```

### Adding command line for a computer/machine

RetroBat will check if a file, with the same name as the computer model rom file and with extension .commands, exists.

If this is the case, RetroBat will read the file, and add each line as an additional argument when launching a game for the machine:

<div align="left"><figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

With the same example as above, this file would add the following command line for any game launched for the ti99\_4a machine:

```
-cart "C:\retrobat\bios\ti99\Extended Basic v110.rpk"
```

{% hint style="info" %}
The two files do not add up: when a game has its own `.commands` file, the machine file is ignored for this game. The machine file is named after the model actually launched (for example `ti99_4a.commands`, or the model chosen in **MODEL TO EMULATE**).
{% endhint %}
