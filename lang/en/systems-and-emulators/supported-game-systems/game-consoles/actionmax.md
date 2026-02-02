---
description: Worlds of Wonder
---

# Actionmax

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/actionmax.svg" alt="" width="375"><figcaption></figcaption></figure></div>

Game console - Date of release: 1987

{% embed url="https://en.wikipedia.org/wiki/Action_Max" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>hypseus</li><li>singe2</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> actionmax</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.actionmax</td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="245">Retroachievements</th><th width="200">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>hypseus: YES<br>singe2: YES</td></tr></tbody></table>

## BIOS

No BIOS required.

## Controls

TBD

## Specific system information

### Add Actionmax games to Hypseus - zip method

Get the latest zip roms here:\
[https://github.com/DirtBagXon/hypseus\_singe\_data/tree/master/00-zip-roms](https://github.com/DirtBagXon/hypseus_singe_data/tree/master/00-zip-roms)

Use the following folder structure (example for 38ambushalley):

```
└── roms/
    └── actionmax/
        ├── roms/
        │   └── actionmax.zip
        └── vldp/
            └── actionmax/
                ├── 38ambushalley.actionmax
                ├── 38ambushalley.dat
                ├── 38ambushalley.m2v
                ├── 38ambushalley.ogg
                ├── 38ambushalley.txt
                ├── video_actionmaxintro.dat
                ├── video_actionmaxintro.m2v
                ├── video_menu.dat
                └── video_menu.m2v
```

Place the game video and audio files in the `vldp\actionmax` subfolder.

Create an empty file and name it with the name of the game and the extension .actionmax in the `roms\actionmax\vldp\actionmax` folder (here `38ambushalley.actionmax`).

<div align="left"><figure><img src="https://i.imgur.com/4qrVoz7.png" alt=""><figcaption></figcaption></figure></div>

### Add Actionmax games to Hypseus - old method

ActionMax games are compatible with Hypseus emulator but they require a very specific folder structure.

All Actionmax games must be located inside `roms\actionmax\actionmax.hypseus` folder with the following content:

```
+---38ambushalley
|       video_38ambushalley.dat
|       video_38ambushalley.m2v
|       video_38ambushalley.ogg
|       
+---bluethunder
|       video_bluethunder.m2v
|       video_bluethunder.ogg
|       
+---hydrosub2021
|       video_hydrosub2021.m2v
|       video_hydrosub2021.ogg
|       
+---popsghostly
|       video_popsghostly.m2v
|       video_popsghostly.ogg
|       
+---sonicfury
        video_sonicfury.m2v
        video_sonicfury.ogg
|
|   38ambushalley.singe
|   38ambushalley.txt
|   bluethunder.singe
|   bluethunder.txt
|   emulator.singe
|   font_bluestone.ttf
|   font_chemrea.ttf
|   font_led_real.ttf
|   framework.singe
|   hydrosub2021.singe
|   hydrosub2021.txt
|   popsghostly.singe
|   popsghostly.txt
|   sonicfury.singe
|   sonicfury.txt
|   sound_actionmax.wav
|   sound_asteadyaimiscritical.wav
|   sound_badhit.wav
|   sound_gameover.wav
|   sound_getreadyforaction.wav
|   sound_goodhit.wav
|   sound_gunshot.wav
|   sprite_38ambushalley.png
|   sprite_actionmax.png
|   sprite_actionmax_orig.png
|   sprite_bluethunder.png
|   sprite_bullet.png
|   sprite_crosshair.png
|   sprite_hydrosub2021.png
|   sprite_lightoff.png
|   sprite_lighton.png
|   sprite_popsghostly.png
|   sprite_sonicfury.png
|   video_actionmaxintro.dat
|   video_actionmaxintro.m2v
|   video_actionmaxintro.ogg
|   video_menu.dat
|   video_menu.m2v
|   video_menu.ogg
```

Create an empty file and name it with the name of the game and the extension .actionmax in the `roms\actionmax` folder (eg. `38ambushalley.actionmax`).

<div align="left"><figure><img src="https://i.imgur.com/5k9KBcS.png" alt=""><figcaption></figcaption></figure></div>
