---
description: Nintendo
---

# Nintendo 64

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/n64.svg" alt=""><figcaption></figcaption></figure>

</div>

Console de jeu - Durée de vie : 1996 - 2002

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_64" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro: mupen64plus next</li><li>libretro: parallel</li><li>mupen64 (RMG)</li><li>simple64</li><li>ares</li><li>project64</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> n64</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.v64 .z64 .n64 .wad .zip .7z </td><td></td></tr></tbody></table>

## Fonctionnalités

| Succès Rétro | Parties en Réseau |
| ------------ | ----------------- |
| OUI          | NON               |

## BIOS

Aucun BIOS nécessaire.

## Contrôles

| RetroBat                                                                           | Nintendo 64                                                |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| START                                                                              | START                                                      |
| SELECT / BACK                                                                      |                                                            |
| D-PAD                                                                              | D-PAD                                                      |
| Stick analogique gauche                                                            | Stick analogique                                           |
| Stick analogique droit                                                             | C-Boutons                                                  |
| ![A](<../../../../.gitbook/assets/image (19).png>)                                 | <p>A<br>Mode C: c-bas</p>                                  |
| ![B](<../../../../.gitbook/assets/image (6).png>)                                  | Mode C: c-droite                                           |
| <img src="../../../../.gitbook/assets/image (34).png" alt="" data-size="original"> | Mode C: c-haut                                             |
| <img src="../../../../.gitbook/assets/image (32).png" alt="" data-size="line">     | <p>B<br>Mode C: c-gauche</p>                               |
| LB (L1)                                                                            | L                                                          |
| RB (R1)                                                                            | R                                                          |
| LT (L2)                                                                            | Z                                                          |
| RT (R2)                                                                            | Mode C (remplace les boutons A, B, X, Y par les boutons C) |
| L-Click (L3)                                                                       |                                                            |
| R-Click (R3)                                                                       |                                                            |

<div align="left">

<figure><img src="https://i.imgur.com/NZ91mQ9.png" alt=""><figcaption></figcaption></figure>

</div>

## Information spécifique au système

### Textures custom

Le coeur mupen64plus next permet l'utilisation de textures "custom".

Le pack de textures "custom" doit être placé dans le dossier `bios\Mupen64Plus\cache\` si le pack est au format .htc ou .hts.

<div align="left">

<figure><img src="https://i.imgur.com/H878WjR.png" alt=""><figcaption></figcaption></figure>

</div>

Si le pack de textures est au format décompressé (dossier contenant des fichiers .png), il doit être placé dans le dossier `bios\Mupen64Plus\hires_texture\`.

<div align="left">

<figure><img src="https://i.imgur.com/1sqG9H4.png" alt=""><figcaption></figcaption></figure>

</div>

Les packs de textures au format htc ou hts doivent être nommés `GAMEID"__HIRESTEXTURES.hts` ou .htc (par exemple: `MARIOKART64_HIRESTEXTURES.htc`).

Les dossiers des packs de textures décompressés doivent être nommés comme le GAMEID (par exemple  `MARIOKART64`).

Une fois le pack placé dans le bon dossier, activer **CUSTOM TEXTURES** dans Retrobat.

<div align="left">

<figure><img src="https://i.imgur.com/jBt3sjA.png" alt=""><figcaption><p>Configuration avancée du système</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/hzikBUa.png" alt=""><figcaption><p>Visual Rendering</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/TXJ3fti.png" alt=""><figcaption></figcaption></figure>

</div>

Choisir RICE pour les packs au formats htc ou hts.&#x20;

Choisir CACHE pour les packs décompressés.

{% hint style="info" %}
Au premier lancement d'un jeu avec un pack au format décompressé, Mupen64Plus-next génère un fichier .hts dans le dossier`CACHE` de l'émulateur, au prochain lancement du jeu il sera possible de sélectionner RICE au lieu de CACHE, et accélérer ainsi le temps de lancement du jeu.
{% endhint %}
