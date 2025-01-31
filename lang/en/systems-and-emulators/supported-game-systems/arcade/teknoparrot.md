---
description: TeknoGods
---

# TeknoParrot

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/teknoparrot.svg" alt=""><figcaption></figcaption></figure></div>

PC-based arcade games emulator

{% embed url="https://teknogods.github.io/index.html" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>teknoparrot</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> teknoparrot</td></tr><tr><td><strong>File extension</strong></td><td>.teknoparrot .parrot .game .7z .zip .rar</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

Controls are automatically configured since RetroBat version 7.0.0.0 for gamepads and guns.

The file **teknoparrot.yml** located in `system\resources\inputmapping` is the file providing the default mapping for each game, it can be updated if you need a different mapping for a game.



Example for spiderman:

```
spiderman:
  Coin1: select # P2 COINS
  P1Button6: leftshoulder # P1 COINS
  P1ButtonStart: start # P1 START / ACTION
  P2ButtonStart: start # P2 START / ACTION
  Service1: r3 # Test Select
  Test: l3 # Test Menu
```

Gun games can have 2 mappings, one to play with the gamepad and one for using mouse/lightgun:

```
hotd4:
  Analog0: rightstickleft # Player 1 Gun X
  Analog2: rightstickup # Player 1 Gun Y
  Analog4: rightstickleft # Player 2 Gun X
  Analog6: rightstickup # Player 2 Gun Y
  Coin1: select # Coin 1
  Coin2: select # Coin 2
  P1Button1: righttrigger # Player 1 Gun Trigger
  P1Button2: lefttrigger # Player 1 Reload
  P1Button3: leftshoulder # Player 1 Grenade
  P1ButtonStart: start # Player 1 Start
  P2Button1: righttrigger # Player 2 Gun Trigger
  P2Button2: lefttrigger # Player 2 Reload
  P2Button3: leftshoulder # Player 2 Grenade
  P2ButtonStart: start # Player 2 Start
  Service1: r3 # Service 1
  Test: l3 # Test

hotd4_gun:
  Coin1: kb_5 # Coin 1
  Coin2: kb_6 # Coin 2
  mouseleft_1: P1Button1 # P1 Left Trigger
  mouseleft_2: P2Button1 # P2 Left Trigger
  mousemiddle_1: P1Button3 # P1 Grenades
  mousemiddle_2: P2Button3 # P2 Grenades
  mouseright_1: P1Button2 # P1 Right Trigger
  mouseright_2: P2Button2 # P2 Right Trigger
  P1ButtonStart: kb_1 # P1 Start
  P2ButtonStart: kb_2 # P2 Start
  Service1: kb_S # Service
  Test: kb_T # Test
```

The id to use for the controls can be found in the game profile file in `emulators\teknoparrot\GameProfiles` folder:

<div align="left"><figure><img src="https://i.imgur.com/c9Vtv43.png" alt=""><figcaption></figcaption></figure></div>

## Specific system information

### ROMs

The list of compatible games can be found [HERE](https://teknogods.github.io/compatibility.html).

### Adding TeknoParrot emulator to Retrobat

To add **Teknoparrot** games, you must first download the Teknoparrot "emulator" from its official website (and not elsewhere): [https://teknoparrot.com/](https://teknoparrot.com/)

Then, unzip the file you just downloaded in **\emulators\teknoparrot:**

<div align="left"><figure><img src="https://i.imgur.com/rQlbFKQ.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Your antivirus will surely panic, keep cool, these are false positives, so make sure that your antivirus authorizes the detected files.
{% endhint %}

Launch the TeknoParrotUi.exe for the first time, it will most certainly ask for several updates: do them, **all.**

<div align="left"><figure><img src="https://i.imgur.com/liUVclK.png" alt=""><figcaption></figcaption></figure></div>

Place your Teknoparrot games in **\roms\teknoparrot**

<div align="left"><figure><img src="https://i.imgur.com/wqTsWOQ.png" alt=""><figcaption></figcaption></figure></div>

The folders name of your Teknoparrot games must be renamed to **.teknoparrot** **.parrot** or **.game**

For example, the game folder of _Mario Kart: Arcade GP DX_ must be rename&#x64;**:**&#x20;

* `MKDX.teknoparrot`,&#x20;
* or `MKDX.parrot`
* or `MKDX.game`

**Important detail**, the folders name must correspond to the name of the json file for the game in the Teknoparrot "**Metadata**" folder located in **\emulators\teknoparrot\Metadata**

<div align="left"><figure><img src="https://i.imgur.com/6BBrvM8.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
You can also use the .xml game profile file name in the **\emulators\teknoparrot\GameProfiles** folder.
{% endhint %}
