# LaserDisc

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/daphne.svg" alt=""><figcaption></figcaption></figure>

</div>

Arcade - First LaserDisc game release : 1983

{% embed url="http://www.daphne-emu.com/site3/index_hi.php" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>hypseus</li><li>daphne</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> daphne</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.daphne .actionmax .7z .zip .rar .squashfs</td><td></td></tr></tbody></table>

## BIOS

No BIOS required to play DAPHNE or SINGE games.

## Controls

### Gamepad controls&#x20;

Gamepad controls are enabled through pad2key files provided with Retrobat installation:

<table><thead><tr><th width="311">Action</th><th>Gamepad Button</th></tr></thead><tbody><tr><td>Directional movement</td><td>D-PAD or Left analog stick</td></tr><tr><td>COIN 1</td><td>SELECT</td></tr><tr><td>START 1</td><td>START</td></tr><tr><td>Button 1</td><td>A</td></tr><tr><td>Button 2</td><td>B</td></tr><tr><td>Button 3</td><td>R2</td></tr><tr><td>Skill 1</td><td>Y</td></tr><tr><td>Skill 2</td><td>X</td></tr><tr><td>Skill 3</td><td>L2</td></tr><tr><td>SERVICE</td><td>HOTKEY + B</td></tr><tr><td>TEST</td><td></td></tr><tr><td>RESET</td><td>HOTKEY + X</td></tr><tr><td>Screenshot</td><td></td></tr><tr><td>Quit</td><td>HOTKEY + START</td></tr><tr><td>Pause</td><td>HOTKEY + A</td></tr><tr><td>Console</td><td></td></tr><tr><td>Title</td><td>HOTKEY + Y</td></tr></tbody></table>

**NOTE:** Right Analog stick simulates mouse



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

<div align="left">

<figure><img src="https://i.imgur.com/crqriZ1.png" alt=""><figcaption><p>lair appears twice</p></figcaption></figure>

</div>

You can use use the [**VIEW OPTIONS**](../../../navigation/view-options.md) to hide the `.zip` extension for the system by pressing **SELECT**

<div align="left">

<figure><img src="https://i.imgur.com/dQngpx5.png" alt=""><figcaption></figcaption></figure>

</div>

Navigate to [**VIEW CUSTOMIZATION**](../../../navigation/view-options.md#view-options) and FILE EXTENSIONS

<div align="left">

<figure><img src="https://i.imgur.com/JT7AqDc.png" alt=""><figcaption></figcaption></figure>

</div>

Untick .zip extension

<div align="left">

<figure><img src="https://i.imgur.com/B38zdIa.png" alt=""><figcaption></figcaption></figure>

</div>

### Adding SINGE Games

SINGE games include the famous AMERICAN LASR GAMES and a few other titles.

The process is similar as for Daphne games but there is no zip file to place in the roms folder. In addition, 2 files need to be present in your `<game>.daphne` folder:

* `<game>.singe`
* `<game>.txt`

**T**he structure of the game folder should look like this:

<div align="left">

<figure><img src="https://i.imgur.com/QPFt4jZ.jpg" alt=""><figcaption></figcaption></figure>

</div>
