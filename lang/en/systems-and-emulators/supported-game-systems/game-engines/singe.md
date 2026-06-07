# Singe

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/fb69ee3e5daf0db1c90d85d4a743edf1cc8a1843/art/logos/singe.svg" alt="" width="375"><figcaption></figcaption></figure></div>

Laserdisc Game Engine

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>hypseus</li><li>singe2</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> singe</td></tr><tr><td><strong>File extension</strong></td><td>.hypseus .zip</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

| Retrobat Button                                    | Hypseus    |
| -------------------------------------------------- | ---------- |
| START                                              | START 1    |
| SELECT                                             | COIN 1     |
| D-PAD                                              | DIRECTIONS |
| Left analog stick                                  | DIRECTIONS |
| ![](<../../../.gitbook/assets/image (48).png>)     | SKILL 1    |
| ![](<../../../.gitbook/assets/image (30).png>)     | BUTTON 1   |
| ![](<../../../.gitbook/assets/image (16) (1).png>) | BUTTON 2   |
| ![](<../../../.gitbook/assets/image (50).png>)     | SKILL 2    |
| L1                                                 | SKILL 3    |
| R1                                                 | BUTTON 3   |
| L3                                                 | SERVICE    |
| R3                                                 | TEST       |

## Specific system information

### Add SINGE/SINGE2 game (zip method)

This is the easiest method to add SINGE games with hypseus emulator, however, not all games are available in zip yet.

Get the latest zip file for the game here:\
[https://github.com/DirtBagXon/hypseus\_singe\_data/tree/master/00-zip-roms](https://github.com/DirtBagXon/hypseus_singe_data/tree/master/00-zip-roms)

Create the following structure:

```
roms\
└─ singe\
   ├─ roms\
   │  └─ timegal.zip
   ├─ vldp\
      └─ timegal\
         ├─ timegal.dat
         ├─ timegal.m2v
         ├─ timegal.ogg
         └─ timegal.txt
```

Place the zip file in singe\roms folder.

Place the framework file and media files in vldp game subfolder.

### Add SINGE/SINGE2 Games (folder method - old)

To add SINGE games, your game folders must be placed in "**\roms\singe**" folder by adding **.hypseus** at the end.

2 files need to be present in your `<game>.hypseus` folder:

* `<game>.singe`
* `<game>.txt`

**T**he structure of the game folder should look like this:

<div align="left"><figure><img src="https://i.imgur.com/55vdoKB.png" alt=""><figcaption></figcaption></figure></div>

### Simple games folders structure (Hypseus)

To make things easier, you can use the assets available on the Hypseus Github.

{% embed url="https://github.com/DirtBagXon/hypseus_singe_data/" %}

At first, download the content of the repository above,

<figure><img src="https://i.imgur.com/dEGyFs9.gif" alt=""><figcaption></figcaption></figure>

&#x20;and extract the zip on a temporary folder.

<div align="left"><figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure></div>

For the exemple, we will use the game Asterix, in 00-singe2 sub-folder :

<div align="left"><figure><img src="https://i.imgur.com/cbDJNRN.png" alt=""><figcaption></figcaption></figure></div>

Inside the game folder, you will find a text file that contain the information about which file is missing, and where it have to be place. In this exemple, you have to place the file `asterix.m2v` in the **Video** folder.

<div align="left"><figure><img src="https://i.imgur.com/iN4Evfi.png" alt=""><figcaption></figcaption></figure></div>

After adding the required files (`.m2v` file, or `.ogg` and `.m2v` files), rename your folder by adding .hypseus at the end of the folder name (in our exemple : `Asterix.hypseus`) and move this folder to the `/roms/singe/` folder:

<div align="left"><figure><img src="https://i.imgur.com/f29wlp8.png" alt=""><figcaption></figcaption></figure></div>

### Use custom command lines (Hypseus)

It is possible to use a custom command file to force command line to hypseus emulator, to do so, create a text file in the rom folder and add all command lines required within the file:

<div align="left"><figure><img src="https://i.imgur.com/AuIQeoE.png" alt=""><figcaption></figcaption></figure></div>

Finally: rename the file with the .commands extension, the name of the file must match exactly the name of the game folder (without the .hypseus extension).

### Adding SINGE2 games (singe2 emulator)

Singe2 emulator does not support games in the same format as hypseus format.

Only games listed on the emulator webpage can be used:

{% embed url="https://kangaroopunch.com/view/ShowSoftware?id=7" %}

You can download these games, add the video/sound files required, and rename the folder with a .singe extension to use these games with the SINGE2 emulator:

<div align="left"><figure><img src="https://i.imgur.com/0iDxyWG.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/7dDJtAe.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
It is very important to KEEP the game folder name as downloaded from the website !
{% endhint %}

