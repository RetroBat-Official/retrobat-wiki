# OpenGOAL

<div align="left"><figure><img src="https://github.com/fabricecaruso/es-theme-carbon/blob/master/art/logos/opengoal.png?raw=true" alt=""><figcaption></figcaption></figure></div>

Game engine to play Jak & Daxter 1 and 2.

{% embed url="https://opengoal.dev/" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>opengoal</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> opengoal</td></tr><tr><td><strong>File extension</strong></td><td>.opengoal</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

Controls must be configured within the emulator.

## Specific system information

### Install game in the emulator

OpenGOAL requires a dump of the PS2 game to run correctly, the iso file needs to be extracted with the extractor program provided with the emulator.

**Step 1 : download the emulator**

Download the emulator from the following link:

{% embed url="https://github.com/open-goal/jak-project/releases" %}

Select the windows version : `opengoal-windows-vX.X.X.zip`

#### Step 2 : extract the files

Extract the files from the downloaded archive in the `\emulators\opengoal` folder of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/piA0EnZ.png" alt=""><figcaption></figcaption></figure></div>

#### **Step 3 : Extract the game files**

This is the tricky part, you need to run extractor with a command.

* Create a text file in the same folder as the extractor.exe file, and name it: "jakExtract.txt"
* Inside the file, write the following:

```
start extractor -g GAME "PATH-TO-GAME-ISO"
```

Replace GAME with either jak1, jak2 or jak3.

Replace PATH-TO-GAME-ISO with the full path to the corresponding game iso file.

Example:

```
start gk -g jak2 "C:\retrobat\roms\ps2\Jak2.iso"
```

* Change the file extension to .bat

This will automatically extract the game iso to make it work with OpenGOAL (the extraction process might take some time).

**Step 4 : Create the rom file**

Create an empty .txt file in the \roms\opengoal folder of your RetroBat installation and put the name of the game inside the file:

* `jak1` for jak and Daxter 1
* `jak2` for jak and Daxter 2

<div align="left"><figure><img src="https://i.imgur.com/mGUXHzk.png" alt=""><figcaption></figcaption></figure></div>

Save the text file with the "**.opengoal**" extension.
