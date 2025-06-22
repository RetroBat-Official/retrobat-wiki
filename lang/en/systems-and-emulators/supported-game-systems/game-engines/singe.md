# Singe

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/fb69ee3e5daf0db1c90d85d4a743edf1cc8a1843/art/logos/singe.svg" alt="" width="375"><figcaption></figcaption></figure></div>

Laserdisc Game Engine

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>hypseus</li><li>singe2</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> singe</td></tr><tr><td><strong>File extension</strong></td><td>.hypseus .zip</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

| Retrobat Button                                | Hypseus    |
| ---------------------------------------------- | ---------- |
| START                                          | START 1    |
| SELECT                                         | COIN 1     |
| D-PAD                                          | DIRECTIONS |
| Left analog stick                              | DIRECTIONS |
| ![](<../../../.gitbook/assets/image (48).png>) | SKILL 1    |
| ![](<../../../.gitbook/assets/image (30).png>) | BUTTON 1   |
| ![](<../../../.gitbook/assets/image (16).png>) | BUTTON 2   |
| ![](<../../../.gitbook/assets/image (50).png>) | SKILL 2    |
| L1                                             | SKILL 3    |
| R1                                             | BUTTON 3   |
| L3                                             | SERVICE    |
| R3                                             | TEST       |

## Specific system information

### Add SINGE game (zip method)

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

### Add SINGE game (old method)

You can also use the old method of a .daphne folder by following this guide:

[Adding SINGE games](../arcade/daphne-laserdisc.md#adding-singe-games-with-hypseus)

