# Doom

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/prboom.svg" alt=""><figcaption></figcaption></figure></div>

Game engine to play most games using the original Doom engine.

{% embed url="https://github.com/UZDoom/uzdoom" %}

{% embed url="https://zdoom.org/index" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>uzdoom</li><li>gzdoom</li><li>libretro : prboom</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> doom</td></tr><tr><td><strong>File extension</strong></td><td>.wad .iwad .pwad .pk3 .ipk3 .gzdoom .uzdoom</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

Controls must be configured within the emulator.

### PRBoom

<table><thead><tr><th width="205">Retrobat Button</th><th>Classic</th><th>Modern</th></tr></thead><tbody><tr><td>START</td><td>Show/Hide Menu</td><td>Show/Hide Menu</td></tr><tr><td>SELECT</td><td>Show/Hide Map</td><td>Show/Hide Map</td></tr><tr><td>D-PAD</td><td>D-PAD</td><td>D-PAD</td></tr><tr><td>Left analog stick</td><td></td><td>X-axis: strafe<br>Y-axis: move forwards and backwards</td></tr><tr><td>Reft analog stick</td><td></td><td>X-axis: look left/right</td></tr><tr><td><img src="../../../.gitbook/assets/image (48).png" alt=""></td><td>Run</td><td>Quick save</td></tr><tr><td><img src="../../../.gitbook/assets/image (30).png" alt=""></td><td>Use</td><td>Menu cancel</td></tr><tr><td><img src="../../../.gitbook/assets/image (16) (1).png" alt=""></td><td>Fire</td><td>Menu select</td></tr><tr><td><img src="../../../.gitbook/assets/image (50).png" alt=""></td><td>Strafe</td><td>Quick load</td></tr><tr><td>L1</td><td>Strafe Left</td><td>Previous Weapon</td></tr><tr><td>R1</td><td>Strafe Right</td><td>Next Weapon</td></tr><tr><td>L2</td><td>Previous Weapon</td><td>Use</td></tr><tr><td>R2</td><td>Next Weapon</td><td>Fire</td></tr><tr><td>L3</td><td></td><td>Toggle run</td></tr><tr><td>R3</td><td></td><td>180 turn</td></tr></tbody></table>

## Specific system information

### List of supported games

The list of games supported by UZDoom & GZDoom can be found here:

{% embed url="https://zdoom.org/wiki/IWAD" %}

### Using your own command line arguments

RetroBat allows for using your own command line arguments with the emulator.

To do so, create a .txt file and fill one argument per line:

<div align="left"><figure><img src="https://i.imgur.com/hr7OEao.png" alt=""><figcaption></figcaption></figure></div>

Save the file with the ".uzdoom" or ".gzdoom" extension and place it in the `roms\doom` folder.

### Running mods

The method above also allows you also to start modded games.&#x20;

To do so, precise which game the mod will use (the mian iwad file), and which mod you want to start (pwad games), with the full path to the different files.\
\
An exemple, using "10 sectors" mod :\
\
![](<../../../.gitbook/assets/image (54).png>)\
\
then, starting the games using the file `"10sector.gzdoom"` will start the according mod.

{% hint style="info" %}
To cumulate multiple mods, just add lines to the file with the paths to the other mods to launch.
{% endhint %}

### File organization (PRBoom)

PrBoom can load wad, iwad, and pwad files.&#x20;

WAD and IWAD files are "`Internal Where's All the Data`" files, meaning they are used to run the game.

PWAD files are patches, they need the main game WAD/IWAD file to run.

Hereunder is the recommendation for the organization of your prboom folder:

<pre><code>└── roms\
    └── doom\
        ├── doom\
<strong>        │   └── doom.wad
</strong>        └── doom 2\
        │   └── doom2.wad
        └── Doom Ultimate\
        │   └── doomu.wad
</code></pre>

If you are going to use pwad files, they will have to be placed in a subfolder inside the main wad game folder:

<pre><code>└── roms\
    └── doom\
        ├── doom\
<strong>        │   └── doom.wad
</strong>        │   └── Episode 5 - Sigil\
        │           └── SIGIL.pwad
        └── Doom 2\
            └── doom2.wad
            └── Goldeneye\
                    └── goldeneye.pwad        
</code></pre>
