---
description: Nintendo
---

# Nintendo 64

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/n64.svg" alt=""><figcaption></figcaption></figure></div>

Console de jeu - Durée de vie : 1996 - 2002

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_64" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro: mupen64plus next</li><li>libretro: parallel</li><li>mupen64 (RMG)</li><li>simple64</li><li>ares</li><li>bizhawk: Ares64</li><li>bizhawk: Mupen64Plus</li><li>project64</li><li>gopher64</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> n64</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.v64 .z64 .n64 .wad .zip .7z</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-mupen64 : OUI<br>lr-parallel : OUI<br>RMG : NON<br>Simple64 : NON<br>Ares : NON<br>BizHawk : OUI<br>Project64 : NON<br>Gopher64: NON</td><td>lr-mupen64 : OUI<br>lr-parallel : OUI<br>RMG : NON<br>Simple64 : NON<br>Ares : NON<br>BizHawk : NON<br>Project64 : NON<br>Gopher64: NON</td><td>lr-mupen64 : OUI<br>lr-parallel : OUI<br>RMG : OUI<br>Simple64 : OUI<br>Ares : OUI<br>BizHawk : OUI<br>Project64 : OUI<br>Gopher64: OUI</td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire.

## Contrôles

### Libretro (Mupen64plus\_next et parallel)

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Mupen64 (RMG), Simple64, Project64, Ares etBizhawk

Pour Mupen64 RMG, Simple64 et Project64, il existe 5 schémas de contrôle en fonction des options sélectionnées ici:

<div align="left"><figure><img src="https://i.imgur.com/DkLUs4h.png" alt=""><figcaption></figcaption></figure></div>

Ares et Bizhawk en proposent 3:

<div align="left"><figure><img src="https://i.imgur.com/HKiieSd.png" alt=""><figcaption></figcaption></figure></div>

Les cinq schémas sont:

| Option                                                                                                          | Schéma                                                                                                                                              |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Default<br>(C-BUTTONS=RIGHT-STICK Z=LEFT-TRIGGER)<br><br><strong>Ares/Bizhawk</strong><br>Z=LEFT-TRIGGER</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" data-size="original">         |
| C-BUTTONS=FACE Z=LEFT-TRIGGER                                                                                   | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_face_zl.png?raw=true" alt="" data-size="original"> |
| <p>C-BUTTONS=RIGHT-STICK Z=RIGHT-TRIGGER<br><br><strong>Ares/Bizhawk</strong><br>Z=RIGHT-TRIGGER</p>            | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_zr.png?raw=true" alt="" data-size="original">      |
| C-BUTTONS=FACE Z=RIGHT-TRIGGER                                                                                  | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_face_zr.png?raw=true" alt="" data-size="original"> |
| XBOX                                                                                                            | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64_xbox.png?raw=true" alt="" data-size="original">               |

### Gopher64

Gopher64 ne propose que le schéma par défaut assigné automatiquement par l'émulateur.

### Utiliser une manette N64

RetroBat détecte et configure automatiquement les manettes N64 suivantes:

* Manette originale avec adaptateur Raphnet
* Manette originale avec adaptateur Mayflash
* Manette N64 Nintendo Switch Online (incompatible avec RetroArch, fonctionne uniquement sur les émulateurs "standalone")

De plus, RMG Mupen64 et Simple64 permettent d'utiliser la fonctionnalité d'accès direct au contrôleur pour l'adaptateur Raphnet, pour cela il est nécessaire de modifier le pilote des manettes dans RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/6ZCeSOE.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Il est important de connecter les manettes de droite à gauche sur l'adaptateur Mayflash, la manette 1 étant celle connectée au port 4 (ou 2 pour les adaptateurs 2 manettes) de l'adaptateur.
{% endhint %}

Le mapping des manettes N64 est géré par le fichier "**n64Controllers.json**" situé dans le répertoire `\system\resources\inputmapping` de l'installation RetroBat, il est possible d'ajouter d'autres manettes dans ce fichier pour automatiquement configurer votre contrôleur.

## Information spécifique au système

### Textures custom

Le coeur mupen64plus next permet l'utilisation de textures "custom".

Le pack de textures "custom" doit être placé dans le dossier `bios\Mupen64Plus\cache\` si le pack est au format .htc ou .hts.

<div align="left"><figure><img src="https://i.imgur.com/H878WjR.png" alt="" width="375"><figcaption></figcaption></figure></div>

Si le pack de textures est au format décompressé (dossier contenant des fichiers .png), il doit être placé dans le dossier `bios\Mupen64Plus\hires_texture\`.

<div align="left"><figure><img src="https://i.imgur.com/1sqG9H4.png" alt="" width="375"><figcaption></figcaption></figure></div>

Les packs de textures au format htc ou hts doivent être nommés `GAMEID"__HIRESTEXTURES.hts` ou .htc (par exemple: `MARIOKART64_HIRESTEXTURES.htc`).

Les dossiers des packs de textures décompressés doivent être nommés comme le GAMEID (par exemple  `MARIOKART64`).

Une fois le pack placé dans le bon dossier, activer **CUSTOM TEXTURES** dans Retrobat.

<div align="left"><figure><img src="https://i.imgur.com/63zt74D.png" alt=""><figcaption><p>Configuration avancée du système</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/h5dF0BV.png" alt=""><figcaption><p>Visual Rendering</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/po34PIR.png" alt=""><figcaption></figcaption></figure></div>

Choisir RICE pour les packs au formats htc ou hts.&#x20;

Choisir CACHE pour les packs décompressés.

{% hint style="info" %}
Au premier lancement d'un jeu avec un pack au format décompressé, Mupen64Plus-next génère un fichier .hts dans le dossier`CACHE` de l'émulateur, au prochain lancement du jeu il sera possible de sélectionner RICE au lieu de CACHE, et accélérer ainsi le temps de lancement du jeu.
{% endhint %}
