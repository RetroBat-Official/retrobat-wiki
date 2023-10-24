---
description: MAME Team
---

# MAME

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/mame-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/mame.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Émulateur multi-arcade - Année de création: 1997

{% embed url="https://fr.wikipedia.org/wiki/MAME" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>Libretro: mame</li><li>Libretro: mame2016</li><li>Libretro: mame2010</li><li>Libretro: mame2003_plus</li><li>Libretro: mame2003</li><li>Libretro: mame2003_midway</li><li>Libretro: mame2000</li><li>mame64</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> mame</td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr></tbody></table>

## Bios

Selon le [type de romset](../../arcade-guide.md#type-de-romset) utilisé, il est possible qu'il soit nécessaire d'ajouter des fichiers bios pour pouvoir démarrer certains jeux :

* **Full non-merged** : le BIOS est inclus dans le zip du jeu, pas besoin de fichier additionnel.
* **Non-merged** : certains BIOS partagés par plusieurs jeux doivent être placés dans le dossier des  jeux.
* **Split** : les fichiers BIOS sont requis.
* **Merged** : le BIOS est inclus dans le zip du jeu, pas besoin de fichier additionnel.

{% hint style="info" %}
Se référer au [guide arcade](../../arcade-guide.md#type-de-romset) pour plus d'informations.
{% endhint %}

**Ci-dessous des fichiers contenant la liste non-exhaustive des BIOS MAME (basé sur le romset 0.255):**

{% file src="../../../.gitbook/assets/MAME 0.255 ROMs (bios-devices).xml" %}

Les BIOS additionnels doivent être placés à la racine du dossier \bios de votre installation RetroBat.



## Emplacement des dossiers utilisés par MAME

**Rompath**: \bios ainsi que le dossier du jeu

**Samples**: \bios\mame\samples

**Cfg**: \bios\mame\cfg

**Ini**: \bios\mame\ini

**Hash**: \bios\mame\hash

**Artworks**: \saves\mame\artwork

**Cheats**: \cheats\mame

**Ctrl**: \saves\mame\ctrlr



## Contrôles

### Sticks Arcade

La correspondance des boutons est disponible dans la [notice](http://retrobat.ovh/notice/notice.pdf).

<div align="left">

<figure><img src="https://i.imgur.com/kXBcdsB.png" alt=""><figcaption></figcaption></figure>

</div>

### Correspondance des touches

| Retrobat                                       | Arcade |
| ---------------------------------------------- | ------ |
| START                                          | START  |
| SELECT                                         | COIN   |
| Stick analogique gauche                        | Stick  |
| Stick analogique droit                         |        |
| D-PAD                                          | Stick  |
| ![](<../../../.gitbook/assets/image (32).png>) | 3      |
| ![](<../../../.gitbook/assets/image (19).png>) | 1      |
| ![](<../../../.gitbook/assets/image (6).png>)  | 2      |
| ![](<../../../.gitbook/assets/image (34).png>) | 4      |
| L1                                             | 5      |
| R1                                             | 6      |
| L2                                             |        |
| R2                                             |        |
| L3                                             |        |
| R3                                             |        |

## Informations spécifiques au système

### Versions des romsets&#x20;

Se référer à la [section "romsets"](../../arcade-guide.md#type-de-romset) du guide arcade.

### Fichiers CHD ou IMG

Se référer à la [section "CHD"](../../arcade-guide.md#fichiers-chd-ou-img) du guide arcade.

### **Fichiers samples**

Se référer à la [section "samples"](../../arcade-guide.md#samples) du guide arcade.

### Menu "Service"

Appuyer sur L3 et R3 pour accéder au menu service.

## Problèmes connus et solutions

### RetroBat affiche uniquement un écran noir lors du lancement d'un jeu avec le core libretro:mame

Le core libretro:mame est limité dans le nombre de caractères utilisable pour les dossiers de jeux lorsqu'un jeu est lancé par ligne de commande. Cette limite n'existe pas avec MAME standalone.

Afin de corriger le problème, assurez-vous que le chemin d'installation de RetroBat n'est pas trop "long".

Par exemple le chemin `C:\Emulation\Multi Emulators\FrontEnd\Tout-en-un\This is top\RetroBat version 5.3` est beaucoup trop long.
