---
description: Doom3
---

# Doom III

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/f55c99c10d6ab0fc36ebe3d33576050178c66501/art/logos/boom3-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/f55c99c10d6ab0fc36ebe3d33576050178c66501/art/logos/boom3.svg" alt="" width="375"></picture><figcaption></figcaption></figure></div>

Game engine to play Doom 3 and Resurrection of Evil.

{% embed url="https://docs.libretro.com/library/boom3/" %}

{% embed url="https://dhewm3.org/" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>Libretro: boom3</li><li>Libretro: boom3_xp</li><li>dhewm3</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> doom3</td></tr><tr><td><strong>File extension</strong></td><td>.boom3 .game</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

### Boom3:

boom3 allows you to choose between 2 controller layouts from RetroBat menu.

<table><thead><tr><th width="205">Retrobat Button</th><th>Classic</th><th>Modern</th></tr></thead><tbody><tr><td>START</td><td>Show/Hide Menu</td><td>Show/Hide Menu</td></tr><tr><td>SELECT</td><td>Show/Hide Map</td><td>Show/Hide Map</td></tr><tr><td>D-PAD</td><td>D-PAD</td><td>D-PAD</td></tr><tr><td>Left analog stick</td><td></td><td>X-axis: strafe<br>Y-axis: move forwards and backwards</td></tr><tr><td>Reft analog stick</td><td>Control Mouse cursor (in menu)</td><td>Look.<br>Control Mouse cursor (in menu)</td></tr><tr><td><img src="../../../.gitbook/assets/image (48).png" alt=""></td><td>Run</td><td>Quick save</td></tr><tr><td><img src="../../../.gitbook/assets/image (30).png" alt=""></td><td>Use</td><td>Menu cancel</td></tr><tr><td><img src="../../../.gitbook/assets/image (16).png" alt=""></td><td>Fire</td><td>Menu select</td></tr><tr><td><img src="../../../.gitbook/assets/image (50).png" alt=""></td><td>Strafe</td><td>Quick load</td></tr><tr><td>L1</td><td>Strafe Left</td><td>Previous Weapon</td></tr><tr><td>R1</td><td>Strafe Right</td><td>Next Weapon</td></tr><tr><td>L2</td><td>Previous Weapon</td><td>Use</td></tr><tr><td>R2</td><td>Next Weapon</td><td>Fire</td></tr><tr><td>L3</td><td></td><td>Toggle run</td></tr><tr><td>R3</td><td></td><td>180 turn</td></tr></tbody></table>

### Dhewm3:

<table><thead><tr><th width="205">Retrobat Button</th><th>Action</th></tr></thead><tbody><tr><td>D-PAD</td><td>Forward<br>Backward<br>Move left and right</td></tr><tr><td>Left analog stick</td><td>Forward<br>Backward<br>Move left and right</td></tr><tr><td>Reft analog stick</td><td>Look up/down<br>Left/Right</td></tr><tr><td><img src="../../../.gitbook/assets/image (48).png" alt=""></td><td>Speed</td></tr><tr><td><img src="../../../.gitbook/assets/image (30).png" alt=""></td><td>Move Up</td></tr><tr><td><img src="../../../.gitbook/assets/image (16).png" alt=""></td><td>Move Down</td></tr><tr><td><img src="../../../.gitbook/assets/image (50).png" alt=""></td><td>Zoom</td></tr><tr><td>L1</td><td>Impulse 13</td></tr><tr><td>R1</td><td>Fire</td></tr><tr><td>L2</td><td>Impulse 15</td></tr><tr><td>R2</td><td>Impulse 14</td></tr></tbody></table>

## Specific system information

### Dhewm3File organization

Boom3 and Dhewm3 need a file with the extension .boom3 to be placed in the `roms\doom3` folder of your RetroBat installation. (dhewm3 also accepts .game extension)

The .boom3 (or .game) must point to the subfolder and pak000.pk4 file:

<div align="left"><figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure></div>

Boom3 and dhewm3 require original .pk4 files from the Doom3 game and the Resurrection of Evil addon, you'll need the game data from a Doom3 installation patched to 1.3.1. Specifically, you'll need the following .pk4 files (base folder contains the original game data, d3xp contains the Resurrection of Evil game data):

```
└── roms/
    └── boom3/
        ├── Doom 3.boom3
        ├── Doom 3 - Resurrection of evil.boom3
        ├── base/
        │   ├── pak000.pk4
        │   ├── pak001.pk4
        │   ├── pak002.pk4
        │   ├── pak003.pk4
        │   ├── pak004.pk4
        │   ├── pak005.pk4
        │   ├── pak006.pk4
        │   ├── pak007.pk4
        │   └── pak008.pk4
        └── d3xp/
            ├── pak000.pk4 
            └── pak001.pk4
```

### Dhewm3: run custom command lines

With dhewm3 emulator, it is possible to run specific user-defined command lines, to do so, open the rom file with a txt editor and add the command lines to be added in a second line:

<div align="left"><figure><img src="https://i.imgur.com/Q5kMZIt.png" alt=""><figcaption></figcaption></figure></div>

In the example above, RetroBat will run the bloodmod and add the following commands:

```
+set com_allowconsole 1 +set g_gib_power 100 +set g_gib_shadows 1
```

