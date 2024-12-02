---
description: Microsoft
---

# Windows

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/windows.svg" alt=""><figcaption></figcaption></figure></div>

Computer Operating System - Lifespan: 1992 - now

{% embed url="https://en.wikipedia.org/wiki/Microsoft_Windows" %}

## Information

Windows games don't need any emulator to function, they can be run natively from the RetroBat interface.



<table data-header-hidden><thead><tr><th width="167"></th><th></th></tr></thead><tbody><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> windows</td></tr><tr><td><strong>File extension</strong></td><td>.exe .bat .cmd .lnk .game .url .pc .win .windows .wine .7z .zip .rar .wsquashfs</td></tr></tbody></table>

## Controls

The controllers configurations are done in-game or in Steam.

## System Features

### Adding a game

Create a text file with the full path to the game executable and save the file with the ".game" extension, place the file in the following folder:   `\roms\windows`

<div align="left"><figure><img src="../../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure></div>

### Adding a Steam game

Simply place the Steam Game shortcut url file in the `roms\windows` folder of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/QBLRBGX.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
If RetroBat menu music is playing while the game is still running, apply the method described [here](https://wiki.retrobat.org/systems-and-emulators/supported-game-systems/others/windows#what-to-do-if-retrobat-music-is-heard-in-the-background-while-playing)
{% endhint %}

### Adding a game from EPIC Game Store

Simply place the EPIC Game shortcut url file in the `roms\windows` folder of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/rh6uCHs.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
If RetroBat menu music is playing while the game is still running, apply the method described [here](https://wiki.retrobat.org/systems-and-emulators/supported-game-systems/others/windows#what-to-do-if-retrobat-music-is-heard-in-the-background-while-playing)
{% endhint %}

### Adding an Amazon Game

Simply place the Amazon Game shortcut url file in the `roms\windows` folder of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/mW5Xme7.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
If RetroBat menu music is playing while the game is still running, apply the method described [here](https://wiki.retrobat.org/systems-and-emulators/supported-game-systems/others/windows#what-to-do-if-retrobat-music-is-heard-in-the-background-while-playing)
{% endhint %}

### Adding a Microsoft Gamepass game

Locate the game installation folder on the computer (usually in `C:\XboxGames`).

Open the "**Content**" folder and find the game executable file:

<div align="left"><figure><img src="../../../.gitbook/assets/image (46) (1).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
It is also possible to run the game and press CTRL+ALT+DEL to find the game executable through the task manager.
{% endhint %}

Create a shortcut to this executable file (_right click > send to > Desktop (shortcut)_)

Cut the shortcut and paste it into the `roms\windows` folder of the RetroBat installation.

You can rename the shortcut if desired.

{% hint style="warning" %}
If RetroBat menu music is playing while the game is still running, apply the method described [here](https://wiki.retrobat.org/systems-and-emulators/supported-game-systems/others/windows#what-to-do-if-retrobat-music-is-heard-in-the-background-while-playing)
{% endhint %}

### Adding a Microsoft Gamepass game (UWP format)

From the XBOX app, create a desktop shortcut:

<div align="left"><figure><img src="https://i.imgur.com/ZHP8OUv.png" alt=""><figcaption></figcaption></figure></div>

Cut and paste the shortcut into the `roms\windows` folder:

<div align="left"><figure><img src="https://i.imgur.com/CTOgYjI.png" alt=""><figcaption></figcaption></figure></div>

Then, right-click on the shortcut and retrieve the UWP application name:

<div align="left"><figure><img src="https://i.imgur.com/SQzxKUS.png" alt=""><figcaption></figcaption></figure></div>

Next : create a text file with your favorite text editor and write the app name inside the file:

<div align="left"><figure><img src="https://i.imgur.com/bly0vZ8.png" alt=""><figcaption></figcaption></figure></div>

Finally, save the file in the same folder as the game shortcut with the '.uwp' file extension:

<div align="left"><figure><img src="https://i.imgur.com/iWX2oXO.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
This second part (the uwp file) is necessary, else RetroBat will not wait for the game to finish and the music from the front-end will be heard during the game.
{% endhint %}

### Adding an UBISOFT game (Ubisoft Connect)

{% hint style="info" %}
You need to ensure that the Ubisoft Connect Launcher is set to automatically login, else the login window might appear.
{% endhint %}

Create a .bat file with a scrapable name for your game.

You have 2 possibilities, quit Ubisoft Connect at the end of each game or not, both work since emulationstation is waiting on the end of the execution of the script to reactivate.

The solution without switching off Unbisoft Connect launches the games faster since the connection step is no longer required once launched for the first time, same if Ubisoft Connect is launched when Windows starts.

This is code of your .bat file **with Ubisoft Connect kill**:

```batch
@echo OFF

REM HERE MODIFY YOUR UBISOFT APPID:
START uplay://launch/00000/0

TIMEOUT /t 30
:RUNNING

REM HERE YOU MUST ENTER THE Right NAME of THE EXECUTABLE, FOR EXAMPLE: "MyGame.exe"
tasklist|findstr "MyGame.exe" > nul

IF %errorlevel%==1 timeout /t 5 & taskkill /F /IM upc.exe /T & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

This is code of your .bat file **without Ubisoft Connect kill**:

```batch
@echo OFF

REM HERE MODIFY YOUR UBISOFT APPID:
START uplay://launch/00000/0

TIMEOUT /t 30
:RUNNING

REM HERE YOU MUST ENTER THE Right NAME of THE EXECUTABLE, FOR EXAMPLE: "MyGame.exe"
tasklist|findstr "MyGame.exe" > nul

IF %errorlevel%==1 timeout /t 5 & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

**All you need is to inquire Ubisoft game launch command and executable name, proceed as follows:**

Open Ubisoft Connect, then select your installed game and choose to "Create desktop shortcut":

<div align="left"><figure><img src="https://i.imgur.com/BlqMJIB.png" alt=""><figcaption></figcaption></figure></div>

Right-click the created shortcut and retrieve the launch command from the shortcut properties:

<div align="left"><figure><img src="https://i.imgur.com/MmzV6ec.png" alt=""><figcaption></figcaption></figure></div>

Next find the game executable as follows:

From Ubisoft Connect, open Game details and go to properties:

<div align="left"><figure><img src="https://i.imgur.com/rdBgCA7.png" alt=""><figcaption></figcaption></figure></div>

Click the "Open folder" button in the Local files section and find the game executable name:

<div align="left"><figure><img src="https://i.imgur.com/CT9qODE.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Alternatively you could run the game and open the task manager to find the executable name.
{% endhint %}

Next, report these two pieces of information in your.bat file as follows:

<div align="left"><figure><img src="https://i.imgur.com/BAx77xx.png" alt=""><figcaption></figcaption></figure></div>

Finally save the bat file in the `roms\windows` folder of your RetroBat installation.

### What to do if RetroBat music is heard in the background while playing ?

This usually happens when RetroBat was not able to detect the actual game process (executable) of the game, it might be caused by:

* the game having a launcher before the actual game process starts
* RetroBat not being able to find the executable in Steam, Epic or Amazon databases

In such case, the solution is to detect the actual game executable by running the game outside of RetroBat:

* Run the game
* Wait to be actually in-game
* Press CTRL + ALT + DEL to open task explorer
* Find the actual executable name of the game process:

<div align="left"><figure><img src="https://i.imgur.com/XXTVidn.png" alt=""><figcaption></figcaption></figure></div>

* Create a text file near the game shortcut (in roms\windows folder) and paste the process name inside the file (without the .exe extension):

<div align="left"><figure><img src="https://i.imgur.com/gWOi36k.png" alt=""><figcaption></figcaption></figure></div>

* Save the file and name it exactly the same as the game shortcut, change the extension to ".gameexe":

<div align="left"><figure><img src="https://i.imgur.com/Wr1vqVP.png" alt=""><figcaption></figcaption></figure></div>

RetroBat will now wait for the process specified within the file to stop to return to the gamelist !

{% hint style="info" %}
The .gameexe file method is compatible with shortcuts (.lnk) and .url files.
{% endhint %}
