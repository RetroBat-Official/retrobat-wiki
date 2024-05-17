---
description: Nokia
---

# N-Gage

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/db9685d44d41fa27f869daaba3ab446395ff3485/art/logos/ngage-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/db9685d44d41fa27f869daaba3ab446395ff3485/art/logos/ngage.svg" alt="" width="563"></picture><figcaption></figcaption></figure>

</div>

Portable Game Console - Lifespan: 2003 - 2006

{% embed url="https://en.wikipedia.org/wiki/N-Gage_(device)" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>eka2l1</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> ngage</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.ngage .symbian</td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>YES</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="187">Bios file</th><th width="327">Folder</th><th>md5</th></tr></thead><tbody><tr><td>SYM.ROM</td><td><code>bios\eka2l1\data\roms\NEM-4</code></td><td></td></tr></tbody></table>

{% hint style="info" %}
ROM must installed in the emulator first in order to be able to launch a game from RetroBat.
{% endhint %}

## Controls

| RetroBat key                                                                       | N-Gage key                                         |
| ---------------------------------------------------------------------------------- | -------------------------------------------------- |
| START                                                                              | Right softkey                                      |
| SELECT / BACK                                                                      | Left softkey                                       |
| D-PAD                                                                              | D-PAD                                              |
| Left analog stick                                                                  |                                                    |
| Right analog stick                                                                 | <p>Up : 0<br>Left : 7<br>Down : 8<br>Right : 9</p> |
| ![A](<../../../../.gitbook/assets/image (30).png>)                                 | 4                                                  |
| ![B](<../../../../.gitbook/assets/image (16).png>)                                 | 5                                                  |
| <img src="../../../../.gitbook/assets/image (50).png" alt="" data-size="original"> | 2                                                  |
| <img src="../../../../.gitbook/assets/image (48).png" alt="" data-size="line">     | 1                                                  |
| L1                                                                                 | 3                                                  |
| R1                                                                                 | 6                                                  |
| L2                                                                                 | Star (\*)                                          |
| R2                                                                                 | Diese (#)                                          |
| L3                                                                                 | Middle softkey                                     |
| R3                                                                                 | Green softkey                                      |

## Specific system information

### First launch / emulator configuration

Before starting to use the emulator, it is necessary to setup the Nokia N-Gage device within the emulator.

{% hint style="info" %}
A copy of the N-Gage NEM-4 rom file is necessary to perform these steps, RetroBat does not provide that file.
{% endhint %}

From the RetroBat menu, launch the EKA2L1 emulator:

<div align="left">

<figure><img src="https://i.imgur.com/8uq6sZD.png" alt=""><figcaption></figcaption></figure>

</div>

In the Emulator, click on "settings menu" and set the `\bios\eka2l1\data` path as the **Emulator Data Path:**

<div align="left">

<figure><img src="https://i.imgur.com/53xZy3q.png" alt=""><figcaption></figcaption></figure>

</div>

Close the settings window and choose File > Install > Device:

<div align="left">

<figure><img src="https://i.imgur.com/w7FrdQV.png" alt=""><figcaption></figcaption></figure>

</div>

Point to the **SYM.ROM** file that should be placed in the `\bios\eka2l1\data\roms\NEM-4` folder of your RetroBat installation:

<div align="left">

<figure><img src="https://i.imgur.com/BWnvG0i.png" alt=""><figcaption></figcaption></figure>

</div>

Click on "install":

<div align="left">

<figure><img src="https://i.imgur.com/qCh5nxP.png" alt=""><figcaption></figcaption></figure>

</div>

You can now quit the emulator.



### Accepted game formats

#### N-GAGE games

True N-Gage games in "folder" format (containing System > Apps subfolder) are compatible.

Here is an example of game format the way it needs to appear in the `\roms\ngage` folder of your RetroBat installation:

<div align="left">

<figure><img src="https://i.imgur.com/wUcyu53.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Do not forget to rename the game folder to make it end with ".ngage", else it will not be recognized by RetroBat.
{% endhint %}

#### Other symbian games

Symbian games need to be installed first within the emulator:

<div align="left">

<figure><img src="https://i.imgur.com/cPdweb3.png" alt=""><figcaption></figcaption></figure>

</div>

Once the game is installed for the correct device, retrieve the "Application Name" from the emulator:

<div align="left">

<figure><img src="https://i.imgur.com/ZHR11OX.png" alt=""><figcaption><p>The app name here is "cakarting"</p></figcaption></figure>

</div>

Finally, create a .txt file with notepad and paste the application name inside the file:

<div align="left">

<figure><img src="https://i.imgur.com/9YkL68x.png" alt=""><figcaption></figcaption></figure>

</div>

Save the file with the `.symbian` extension.

{% hint style="danger" %}
In some cases, the application name is different from the name displayed in EKA2L1 main window.

In such cases, a deep dive in the `retrobat\bios\eka2l1\data\drives\e` folder is required to find the application name.
{% endhint %}

### Emulated devices

The following devices / Symbian OS can be selected from RetroBat:

<figure><img src="https://i.imgur.com/OENxwSZ.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Before using a device, you need to install the firmware of the selected device in the emulator.
{% endhint %}
