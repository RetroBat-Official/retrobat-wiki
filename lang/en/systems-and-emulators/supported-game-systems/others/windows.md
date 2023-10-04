---
description: Microsoft
---

# Windows

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/windows.svg" alt=""><figcaption></figcaption></figure>

</div>

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

<div align="left">

<figure><img src="../../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

</div>

### Adding a Steam game

Simply place the Steam Game shortcut url file in the `roms\windows` folder of your RetroBat installation:

<div align="left">

<figure><img src="https://i.imgur.com/QBLRBGX.png" alt=""><figcaption></figcaption></figure>

</div>

### Adding a game from EPIC Game Store

Simply place the EPIC Game shortcut url file in the `roms\windows` folder of your RetroBat installation:

<div align="left">

<figure><img src="https://i.imgur.com/rh6uCHs.png" alt=""><figcaption></figcaption></figure>

</div>

### Adding an Amazon Game

Simply place the Amazon Game shortcut url file in the `roms\windows` folder of your RetroBat installation:

<div align="left">

<figure><img src="https://i.imgur.com/mW5Xme7.png" alt=""><figcaption></figcaption></figure>

</div>

### Adding a Microsoft Gamepass game

Locate the game installation folder on the computer (usually in `C:\XboxGames`).

Open the "**Content**" folder and find the game executable file:

<div align="left">

<figure><img src="../../../.gitbook/assets/image (46) (1).png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
It is also possible to run the game and press CTRL+ALT+DEL to find the game executable through the task manager.
{% endhint %}

Create a shortcut to this executable file (_right click > send to > Desktop (shortcut)_)

Cut the shortcut and paste it into the `roms\windows` folder of the RetroBat installation.

You can rename the shortcut if desired.

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

<div align="left">

<figure><img src="https://i.imgur.com/BlqMJIB.png" alt=""><figcaption></figcaption></figure>

</div>

Right-click the created shortcut and retrieve the launch command from the shortcut properties:

<div align="left">

<figure><img src="https://i.imgur.com/MmzV6ec.png" alt=""><figcaption></figcaption></figure>

</div>

Next find the game executable as follows:

From Ubisoft Connect, open Game details and go to properties:

<div align="left">

<figure><img src="https://i.imgur.com/rdBgCA7.png" alt=""><figcaption></figcaption></figure>

</div>

Click the "Open folder" button in the Local files section and find the game executable name:

<div align="left">

<figure><img src="https://i.imgur.com/CT9qODE.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Alternatively you could run the game and open the task manager to find the executable name.
{% endhint %}

Next, report these two pieces of information in your.bat file as follows:

<div align="left">

<figure><img src="https://i.imgur.com/BAx77xx.png" alt=""><figcaption></figcaption></figure>

</div>

Finally save the bat file in the `roms\windows` folder of your RetroBat installation.
