---
description: OpenLara
---

# Tomb Raider

<div align="left"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCgoewyw8Sagl6SNUMrCG%2Fuploads%2FEz8si9RfyUg6Yc3vzCUS%2F1526141_794a5.png?alt=media&#x26;token=c4d72829-7e6b-49e6-80e0-d28755ed99bc" alt=""><figcaption></figcaption></figure></div>

Game engine to play Tomb Raider.

{% embed url="https://docs.libretro.com/library/openlara/" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>Libretro: openlara</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> openlara</td></tr><tr><td><strong>File extension</strong></td><td>.croft</td></tr><tr><td><strong>Group</strong></td><td>ports</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

| Retrobat                                           | OpenLara               |
| -------------------------------------------------- | ---------------------- |
| START                                              | START                  |
| SELECT                                             | INVENTORY              |
| D-PAD                                              | D-PAD                  |
| Left analog stick                                  |                        |
| Right analog stick                                 |                        |
| ![](<../../../.gitbook/assets/image (48).png>)     | Jump                   |
| ![](<../../../.gitbook/assets/image (30).png>)     | Action : shoot / catch |
| ![](<../../../.gitbook/assets/image (16) (1).png>) | Roll                   |
| ![](<../../../.gitbook/assets/image (50).png>)     | Draw weapon            |
| L1                                                 |                        |
| R1                                                 | Walk                   |
| L2                                                 | Crouch                 |
| R2                                                 | Dash                   |

## Specific system information

### Game files

Create a .croft file in the `roms\openlara` folder of your RetroBat directory.

In the file, fill the path to the level / file to launch, OpenLara core accepts the following file formats : **.phd, .psx, .phd**

The file hereunder will run the "gym" level of Tomb Raider 1:

<div align="left"><figure><img src="https://i.imgur.com/yRgQBth.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Once a level is launched, it is possible to go to the game main menu and start as if the game was launched on original hardware.
{% endhint %}

### File organization

{% hint style="info" %}
So far, the core only supports Tomb Raider 1.
{% endhint %}

Here is an example of a working folder structure:

```
└── roms\
    └── openlara\
        └── *.croft
        └── Tomb Raider\
               └── audio\
               │      └── 1\
               │           └── XXX.ogg ou track_XX.ogg
               │      └── 2\
               │           └── track_XX.ogg et MAIN.SFX
               │      └── 3\
               │           └── track_XX.ogg et MAIN.SFX
               └── level\
               |      └── 1\
               |           └── *.PNG et *.PHD ou *.PSX ou *.SAT
               │      └── 2\
               │           └── *.PNG et *.TR2 ou *.PSX
               │      └── 3\
               │           └── *.PNG et *.TR2 ou *.PSX
               └── video\
                      └── 1\
                           └── *.RPL ou *.FMV
                      └── 2\
                           └── *.RPL ou *.FMV
                      └── 3\
                           └── *.RPL ou *.FMV
```
