# Commander Genius

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/421cec038116fe7b6711fa35683470884a28ed55/art/logos/cgenius.svg" alt=""><figcaption></figcaption></figure></div>

Game engine to play Commander Keen games.

{% embed url="https://clonekeenplus.sourceforge.io/" %}

## Information

<table data-header-hidden><thead><tr><th width="240"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>cgenius</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> cgenius</td></tr><tr><td><strong>File extension</strong></td><td>.cgenius</td></tr><tr><td><strong>Saves location</strong></td><td><em>emulators\cgenius\save</em><br>Copied to <em>saves\cgenius</em></td></tr></tbody></table>

## BIOS

No BIOS required.

## Controls

<table><thead><tr><th width="246">Retrobat</th><th>Commander Keen</th></tr></thead><tbody><tr><td>START</td><td>Help</td></tr><tr><td>SELECT</td><td>Back</td></tr><tr><td>D-PAD</td><td>Directions</td></tr><tr><td><img src="../../../.gitbook/assets/image (48).png" alt=""></td><td>Run</td></tr><tr><td><img src="../../../.gitbook/assets/image (30).png" alt=""></td><td>Jump</td></tr><tr><td><img src="../../../.gitbook/assets/image (16).png" alt=""></td><td>Fire</td></tr><tr><td><img src="../../../.gitbook/assets/image (50).png" alt=""></td><td>Pogo</td></tr><tr><td>L1</td><td>Status</td></tr><tr><td>R1</td><td>Camlead</td></tr><tr><td>Hotkey + <img src="../../../.gitbook/assets/image (48).png" alt=""></td><td>Quicksave</td></tr><tr><td>Hotkey + <img src="../../../.gitbook/assets/image (50).png" alt=""></td><td>Quickload</td></tr></tbody></table>

## System Features

### Cgenius configuration file

By default, RetroBat will use the cgenius.cfg file located within the `\emulators\cgenius\` folder of the RetroBat installation in order to apply game settings.

However, if you previously installer cgenius without RetroBat, it is possible that the settings files already exist in your user documents folder. If this is the case, this will render RetroBat settings ineffective.

To prevent this issue from happening, you can simply delete the cgenius files located in your user\documents folder.

### Game files organization

The engine requires the games to be located in a "**games**" subfolder inside the `roms\cgenius` folder .

For RetroBat to detect the game, create in the individual game folder a text file and change the extension to ".cgenius".

The folder organization is the following:

```
└── roms\
    └── cgenius\
        └── games\
            ├── keen1\
            │   └── ...
            │   └── Commander Keen.cgenius
            └── keen2\
            │   └── ...
            │   └── Commander Keen 2.cgenius
            └── keen7\
            │   └── ...
            │   └── Commander Keen 7.cgenius
```

### How to add a game

The files can be downloaded from the engine itself:

#### **Run cgenius.exe from the emulators\cgenius folder:**

<div align="left"><figure><img src="https://i.imgur.com/AzAGLU1.png" alt="" width="375"><figcaption></figcaption></figure></div>

#### Click on "+ MORE":

<div align="left"><figure><img src="https://i.imgur.com/kytdlOg.png" alt="" width="375"><figcaption></figcaption></figure></div>

#### Select the game and click "download"

The game will be downloaded within the emulators\cgenius\games folder:

<div align="left"><figure><img src="https://i.imgur.com/ZZdiAKJ.png" alt=""><figcaption></figcaption></figure></div>

#### Copy the last folder (KeenDreams in the example) to the roms\cgenius\games folder:

<div align="left"><figure><img src="https://i.imgur.com/tqAORuQ.png" alt=""><figcaption></figcaption></figure></div>

#### Create an empty .cgenius file in the game folder:

<div align="left"><figure><img src="https://i.imgur.com/DYoPbqt.png" alt=""><figcaption></figcaption></figure></div>
