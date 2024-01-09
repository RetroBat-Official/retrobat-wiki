---
description: prBoom
---

# Doom

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/prboom.svg" alt=""><figcaption></figcaption></figure>

</div>

Game engine to play Doom, Doom II, Doom Ultimate, Final Doom and other Doom IWAD mods.

{% embed url="https://docs.libretro.com/library/prboom/" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>Libretro: prboom</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> prboom</td></tr><tr><td><strong>File extension</strong></td><td>.wad .iwad .pwad</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

PrBoom allows you to choose between 2 controller layouts from RetroBat menu.

<table><thead><tr><th width="205">Retrobat Button</th><th>Classic</th><th>Modern</th></tr></thead><tbody><tr><td>START</td><td>Show/Hide Menu</td><td>Show/Hide Menu</td></tr><tr><td>SELECT</td><td>Show/Hide Map</td><td>Show/Hide Map</td></tr><tr><td>D-PAD</td><td>D-PAD</td><td>D-PAD</td></tr><tr><td>Left analog stick</td><td></td><td>X-axis: strafe<br>Y-axis: move forwards and backwards</td></tr><tr><td>Reft analog stick</td><td></td><td>X-axis: look left/right</td></tr><tr><td><img src="../../../.gitbook/assets/image (43).png" alt=""></td><td>Run</td><td>Quick save</td></tr><tr><td><img src="../../../.gitbook/assets/image (25).png" alt=""></td><td>Use</td><td>Menu cancel</td></tr><tr><td><img src="../../../.gitbook/assets/image (11).png" alt=""></td><td>Fire</td><td>Menu select</td></tr><tr><td><img src="../../../.gitbook/assets/image (45).png" alt=""></td><td>Strafe</td><td>Quick load</td></tr><tr><td>L1</td><td>Strafe Left</td><td>Previous Weapon</td></tr><tr><td>R1</td><td>Strafe Right</td><td>Next Weapon</td></tr><tr><td>L2</td><td>Previous Weapon</td><td>Use</td></tr><tr><td>R2</td><td>Next Weapon</td><td>Fire</td></tr><tr><td>L3</td><td></td><td>Toggle run</td></tr><tr><td>R3</td><td></td><td>180 turn</td></tr></tbody></table>

## Specific system information

### File organization

PrBoom can load wad, iwad, and pwad files.&#x20;

WAD and IWAD files are "`Internal Where's All the Data`" files, meaning they are used to run the game.

PWAD files are patches, they need the main game WAD/IWAD file to run.

Hereunder is the recommendation for the organization of your prboom folder:

<pre><code>└── roms\
    └── prboom\
        ├── doom\
<strong>        │   └── doom.wad
</strong>        └── doom 2\
        │   └── doom2.wad
        └── Doom Ultimate\
        │   └── doomu.wad
</code></pre>

If you are going to use pwad files, they will have to be placed in a subfolder inside the main wad game folder:

<pre><code>└── roms\
    └── prboom\
        ├── doom\
<strong>        │   └── doom.wad
</strong>        │   └── Episode 5 - Sigil\
        │           └── SIGIL.pwad
        └── Doom 2\
            └── doom2.wad
            └── Goldeneye\
                    └── goldeneye.pwad        
</code></pre>
