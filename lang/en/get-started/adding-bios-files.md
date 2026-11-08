# Adding BIOS files

Some emulators require BIOS files to work correctly.

## What is a BIOS?

The BIOS (sometimes called firmware) is the internal program of a real console or computer: it starts the machine, manages the memory cards, the language, the disc drive… Many emulators need a copy of it to start games, for example PlayStation 1 and 2, Sega Saturn, Neo Geo CD or many old computers.

Other systems do not need any BIOS: the emulator replaces it. The page of each system tells you if a BIOS is needed.

{% hint style="warning" %}
BIOS files are copyrighted. RetroBat does not include them, and the RetroBat team cannot distribute them. You must dump them from your own hardware.
{% endhint %}

## Where to put the BIOS files

As a general rule, BIOS files must be copied to the `bios` folder of RetroBat, for example `C:\RetroBat\bios\`.

<div align="left"><figure><img src="../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
* File names must exactly match the names expected by RetroBat (for example `scph5501.bin`). If your file has another name, rename it.
* Some systems need their BIOS in a subfolder or another location. The page of each system, in the Supported Game Systems section, tells you where and lists the required BIOS.
* BIOS expected as a `.zip` file (for example `adam.zip`) must be copied as they are, without extracting them.
* Windows hides file extensions by default: a file shown as `scph5501.bin` can actually be named `scph5501.bin.bin`. Enable **View > File name extensions** in the Explorer to check.
{% endhint %}

## Checking the BIOS

RetroBat can check your BIOS files: open the [MAIN MENU](../navigation/main-menu.md), go to [GAME SETTINGS](../navigation/main-menu.md#game-settings), then select **MISSING BIOS CHECK** in the **BIOS SETTINGS** group.

<div align="left"><figure><img src="../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure></div>

The result lists, for each system, the BIOS files that need your attention:

* **MISSING** ![](<../.gitbook/assets/image (212).png>) : the file was not found.
* **INVALID** ![](<../.gitbook/assets/image (213).png>) : the file is present, but its checksum (MD5) does not match any known version. It may still work: test the system to make sure.
* **OPTIONAL**: the file is not needed to launch the games (another accepted version is already present, or it is only used by some games or emulators).

The **Installed systems** tab only shows the systems that have games, the **All** tab shows every system.

<div align="left"><figure><img src="../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure></div>

## Check before launching a game

By default, RetroBat also checks the BIOS when you launch a game. If a BIOS of the system is **MISSING**, this message appears:

**WARNING: THE SYSTEM HAS MISSING BIOS FILE(S) AND THE GAME MAY NOT WORK CORRECTLY. DO YOU WANT TO LAUNCH IT ANYWAY?**

* **YES** launches the game anyway (useful if you use an emulator that does not need this BIOS).
* **NO** goes back to the game list.

{% hint style="info" %}
INVALID and OPTIONAL files never show this message.
{% endhint %}

To disable this check for all systems, turn off **CHECK BIOS FILES BEFORE RUNNING A GAME** in **GAME SETTINGS > BIOS SETTINGS**.

## Common problems

<table><thead><tr><th width="290.25">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>The BIOS is in the folder, but still MISSING</td><td>Check the subfolder given on the page of the system, and the exact name of the file. Check that the extension is not doubled (<code>.bin.bin</code>).</td></tr><tr><td>The BIOS is INVALID</td><td>It is another version than the expected one. Test a game: if it starts, you can keep it.</td></tr><tr><td>The warning appears, but the game works</td><td>You use an emulator that does not need this BIOS, or another accepted BIOS. Choose YES, or disable the check.</td></tr><tr><td>A zipped BIOS is not found</td><td>Do not extract it: copy the .zip as it is.</td></tr><tr><td>The game does not start (black screen, error) although no BIOS is missing</td><td>The BIOS may be the wrong version for the emulator. Check the page of the system.</td></tr></tbody></table>
