# Adding BIOS files

Some emulators require BIOS files to work correctly.

{% hint style="warning" %}
BIOS files are copyrighted and are therefore not included with RetroBat. The team cannot legally distribute them: you need to dump them from your own original hardware.
{% endhint %}

## Location

As a general rule, BIOS files must be copied to the `bios` folder of RetroBat, for example `C:\RetroBat\bios\`.

<div align="left"><figure><img src="../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
* File names must match **exactly** the names expected by RetroBat (e.g. `scph5501.bin`). Do not rename them.
* Some systems need their BIOS files in a subfolder or in another location. This is specified on each system's page in the [Supported Game Systems](../systems-and-emulators/supported-game-systems/) section, along with the list of required BIOS files.
{% endhint %}

## Missing BIOS check

RetroBat can check your BIOS files: open the [MAIN MENU](../navigation/main-menu.md), go to [GAME SETTINGS](../navigation/main-menu.md#game-settings), then select **MISSING BIOS CHECK** in the **BIOS SETTINGS** group.

<div align="left"><figure><img src="../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure></div>

The result lists, for each system, the BIOS files that need your attention:

* **Missing** ![](<../.gitbook/assets/image (212).png>) : the file was not found.
* **Invalid** ![](<../.gitbook/assets/image (213).png>) : the file is present, but its checksum (MD5) does not match any known version. It may still work: test the system to make sure.

<div align="left"><figure><img src="../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
By default, RetroBat also checks the BIOS files when you start a game. If a BIOS file is missing for the system, a warning is displayed and you can choose to launch the game anyway.

This check can be disabled with the **CHECK BIOS FILES BEFORE RUNNING A GAME** option, in the same **BIOS SETTINGS** group.
{% endhint %}
