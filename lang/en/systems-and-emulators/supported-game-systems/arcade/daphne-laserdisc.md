# LaserDisc

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/daphne.svg" alt=""><figcaption></figcaption></figure></div>

Arcade - First LaserDisc game release : 1983

{% embed url="http://www.daphne-emu.com/site3/index_hi.php" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>hypseus</li><li>daphne</li><li>singe2</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> daphne</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.daphne .hypseus .7z .rar .squashfs</td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="245">Retroachievements</th><th width="200">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>hypseus: YES<br>daphne: NO<br>singe2: YES</td></tr></tbody></table>

## BIOS

No BIOS required to play DAPHNE or SINGE games.

## Controls

### Gamepad controls&#x20;

<table><thead><tr><th width="311">Action</th><th>Gamepad Button</th></tr></thead><tbody><tr><td>Directional movement</td><td>D-PAD or Left analog stick</td></tr><tr><td>COIN 1</td><td>SELECT</td></tr><tr><td>START 1</td><td>START</td></tr><tr><td>Button 1</td><td>A (SOUTH)</td></tr><tr><td>Button 2</td><td>B (EAST)</td></tr><tr><td>Button 3</td><td>R1 (RIGHT SHOULDER)</td></tr><tr><td>Skill 1</td><td>Y (WEST)</td></tr><tr><td>Skill 2</td><td>X (NORTH)</td></tr><tr><td>Skill 3</td><td>L1 (LEFT SHOULDER)</td></tr><tr><td>SERVICE</td><td>L3 (LEFT STICK)</td></tr><tr><td>TEST</td><td>R3 (RIGHT STICK)</td></tr></tbody></table>



### Keyboard controls:

<table><thead><tr><th width="265">Action</th><th>Keyboard Hypseus</th><th>Keyboard Daphne</th></tr></thead><tbody><tr><td>Directional movement</td><td>ARROW Keys</td><td>ARROW Keys or 8,4,2,6</td></tr><tr><td>COIN 1</td><td>5</td><td>5 or c</td></tr><tr><td>COIN 2</td><td>6</td><td>6</td></tr><tr><td>START 1</td><td>1</td><td>1</td></tr><tr><td>START 2</td><td>2</td><td>2</td></tr><tr><td>Button 1</td><td>LEFT CONTROL</td><td>LEFT CTRL or SPACE</td></tr><tr><td>Button 2</td><td>LEFT ALT</td><td>LEFT ALT</td></tr><tr><td>Button 3</td><td>SPACE</td><td>LEFT SHIFT</td></tr><tr><td>Skill 1</td><td>LEFT SHIFT</td><td>/</td></tr><tr><td>Skill 2</td><td>Z</td><td>*</td></tr><tr><td>Skill 3</td><td>X</td><td>-</td></tr><tr><td>SERVICE</td><td>9</td><td>9</td></tr><tr><td>TEST</td><td>F2</td><td>F2</td></tr><tr><td>RESET</td><td>0</td><td>F3</td></tr><tr><td>Screenshot</td><td>F12</td><td>F12</td></tr><tr><td>Quit</td><td>ESC</td><td>ESC or q</td></tr><tr><td>Pause</td><td>P</td><td>P</td></tr><tr><td>Console</td><td>BACKLASH</td><td></td></tr><tr><td>Title</td><td>T</td><td>t</td></tr></tbody></table>

## Specific system information

### Adding Daphne Games

Daphne games consist of 2 parts

* a folder containing the **videos**, \*.**dat** and \*.**txt** files of the games
* a .zip file in the **roms** folder

To add Daphne games, your games folders must be placed in "**\roms\daphne**" folder by adding **.daphne** at the end.

For example, your game folder "**lair**" (Dragon's Lair) must be renamed to **lair.daphne**

```
roms\
└─ daphne\
   ├─ roms\
   │  └─ lair.zip
   └─ lair.daphne\
      └─ lair.dat
      └─ lair.m2v
      └─ lair.ogg
      └─ lair.txt
```

Once the game added, it is listed twice in Retrobat, as both the zip and the .daphne folder are detected.

<div align="left"><figure><img src="https://i.imgur.com/crqriZ1.png" alt=""><figcaption><p>lair appears twice</p></figcaption></figure></div>

You can use use the [**VIEW OPTIONS**](../../../navigation/view-options.md) to hide the `.zip` extension for the system by pressing **SELECT**

<div align="left"><figure><img src="https://i.imgur.com/dQngpx5.png" alt=""><figcaption></figcaption></figure></div>

Navigate to [**VIEW CUSTOMIZATION**](../../../navigation/view-options.md#view-options) and FILE EXTENSIONS

<div align="left"><figure><img src="https://i.imgur.com/JT7AqDc.png" alt=""><figcaption></figcaption></figure></div>

Untick .zip extension

<div align="left"><figure><img src="https://i.imgur.com/B38zdIa.png" alt=""><figcaption></figcaption></figure></div>

### Adding SINGE Games (with Hypseus)

SINGE games include the famous AMERICAN LASER GAMES and a few other titles.

The process is similar as for Daphne games but there is no zip file to place in the roms folder and the folder extension must be _.hypseus_. In addition, 2 files need to be present in your `<game>.hypseus` folder:

* `<game>.singe`
* `<game>.txt`

**T**he structure of the game folder should look like this:

<div align="left"><figure><img src="https://i.imgur.com/VDq2Pc8.png" alt=""><figcaption></figcaption></figure></div>

### Simple games folders structure (Hypseus)

To make things easier, you can use the assets available on the Hypseus Github.

{% embed url="https://github.com/DirtBagXon/hypseus_singe_data/" %}

At first, download the content of the repository above,

<figure><img src="https://i.imgur.com/dEGyFs9.gif" alt=""><figcaption></figcaption></figure>

&#x20;and extract the zip on a temporary folder.

<div align="left"><figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure></div>

For the exemple, we will use the game Astroboy, in 00-singe2 sub-folder :

<div align="left"><figure><img src="https://i.imgur.com/cbDJNRN.png" alt=""><figcaption></figcaption></figure></div>

Inside the game folder, you will find a text file that contain the information about which file is missing, and where it have to be place. In this exemple, you have to place the file `astroboy.m2v` in the folder `Video`.

<div align="left"><figure><img src="https://i.imgur.com/gobNmnZ.png" alt=""><figcaption></figcaption></figure></div>

After adding the required files (could be `.m2v` file, or `.ogg` and `.m2v` files), you must rename your folder by adding .daphne at the end of the folder name (in our exemple : `Astroboy.hypseus`) and move this folder to the `/roms/daphne/` folder

<div align="left"><figure><img src="https://i.imgur.com/50BvfM1.png" alt=""><figcaption></figcaption></figure></div>

### Use custom command lines (Hypseus)

It is possible to use a custom command file to force command line to hypseus emulator, to do so, create a text file in the rom folder and add all command lines required within the file:

<div align="left"><figure><img src="https://i.imgur.com/lVcsfdd.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/5ctmvZB.png" alt=""><figcaption></figcaption></figure></div>

Finally: rename the file with the .commands extension, the name of the file must match exactly the name of the game folder (without the .singe or .daphne extension).

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
