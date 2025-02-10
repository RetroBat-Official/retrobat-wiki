---
description: TeknoGods
---

# TeknoParrot

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/teknoparrot.svg" alt=""><figcaption></figcaption></figure></div>

Emulateur d'arcade basé sur l'architecture PC

{% embed url="https://teknogods.github.io/index.html" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>teknoparrot</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> teknoparrot</td></tr><tr><td><strong>Extension</strong></td><td>.teknoparrot .parrot .game .7z .zip .rar</td></tr></tbody></table>

## Bios

Aucune BIOS nécessaire.

## Contrôles

La configuration automatique des contrôles pour les manettes et les pistolets est possible depuis la version 7.0.0.0 de RetroBat.

Le fichier **teknoparrot.yml** situé dans le dossier `system\resources\inputmapping` contient les règles de mapping pour chaque jeu, il peut être mis à jour si vous souhaitez modifier le mapping pour un jeu.

Exemple pour spiderman:

```
spiderman:
  Coin1: select # P2 COINS
  P1Button6: leftshoulder # P1 COINS
  P1ButtonStart: start # P1 START / ACTION
  P2ButtonStart: start # P2 START / ACTION
  Service1: r3 # Test Select
  Test: l3 # Test Menu
```

Les jeux de tir peuvent avoir 2 mappings, un premier pour jouer à la manette et un second pour jouer au pistolet ou à la souris:

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

L'ID de bouton à utiliser pour le mapping peut être récupéré dans le fichier de profil du jeu dans le dossier `emulators\teknoparrot\GameProfiles` folder:

<div align="left"><figure><img src="https://i.imgur.com/c9Vtv43.png" alt=""><figcaption></figcaption></figure></div>

## Informations spécifiques au système

### ROMs

La liste des jeux compatibles est disponible [ICI](https://teknogods.github.io/compatibility.html).

### Ajouter TeknoParrot à Retrobat

Télécharger l'émulateur depuis le site officiel : [https://teknoparrot.com/](https://teknoparrot.com/)

Dézipper l'émulateur dans le dossier **\emulators\teknoparrot**

<div align="left"><figure><img src="https://i.imgur.com/rQlbFKQ.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Il est possible que votre antivirus s'emballe, restez calme, il s'agit de faux-positifs.&#x20;

Configurez une exception pour le dossier TeknoParrot.
{% endhint %}

Démarrer **TeknoParrotUi.exe** une première fois, effectuer toutes les mises à jour demandées:

<div align="left"><figure><img src="https://i.imgur.com/liUVclK.png" alt=""><figcaption></figcaption></figure></div>

Placer les jeux TeknoParrot dans le dossier **\roms\teknoparrot**

<div align="left"><figure><img src="https://i.imgur.com/wqTsWOQ.png" alt=""><figcaption></figcaption></figure></div>

Le dossier de jeu TeknoParrot doit être renommé en ajoutant **.teknoparrot** **.parrot** or **.game**

Par exemple, le dossier du jeu _Mario Kart : Arcade GP DX_ doit être nomm&#xE9;**:**&#x20;

* `MKDX.teknoparrot`,&#x20;
* ou `MKDX.parrot`
* ou `MKDX.game`

**IMPORTANT**, le nom du dossier du jeu doit correspondre EXACTEMENT au nom visible pour le fichier json correspondant au jeu dans le dossier **\emulators\teknoparrot\Metadata** ou au fichier .xml du profil du jeu dans le dossier **\emulators\teknoparrot\GameProfiles**

<div align="left"><figure><img src="https://i.imgur.com/6BBrvM8.png" alt=""><figcaption></figcaption></figure></div>

