---
description: Sega
---

# Saturn

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/saturn.svg" alt=""><figcaption></figcaption></figure></div>

Console de jeu - Durée de vie: 1994 - 2000

{% embed url="https://fr.wikipedia.org/wiki/Saturn_(console_de_jeux_vid%C3%A9o)" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>libretro: kronos</li><li>libretro: mednafen saturn</li><li>libretro: yabasanshiro</li><li>mednafen</li><li>bizhawk: saturnus</li><li>yabasanshiro</li><li>kronos</li><li>ssf</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> saturn</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .cue .toc .m3u .ccd .chd .iso .cso .mds .chd .squashfs</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-kronos : OUI<br>lr_mednafen : OUI<br>lr-yabasanshiro : OUI<br>Mednafen : NON<br>BizHawk : OUI<br>Yabasanshiro : NON<br>Kronos : NON<br>SSF : NON</td><td>lr-kronos : OUI<br>lr_mednafen : OUI<br>lr-yabasanshiro : NON<br>Mednafen : NON<br>BizHawk : NON<br>Yabasanshiro : NON<br>Kronos : NON<br>SSF : NON</td><td>lr-kronos : OUI<br>lr_mednafen : OUI<br>lr-yabasanshiro : OUI<br>Mednafen : OUI<br>BizHawk : OUI<br>Yabasanshiro : OUI<br>Kronos : OUI<br>SSF : OUI</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="266">Fichier BIOS</th><th width="140">Dossier</th><th width="341">MD5</th></tr></thead><tbody><tr><td>saturn_bios.bin</td><td>\bios</td><td>af5828fdff51384f99b3c4926be27762</td></tr><tr><td>mpr-17933.bin</td><td>\bios</td><td>3240872c70984b6cbfda1586cab68dbe</td></tr><tr><td>sega_101.bin</td><td>\bios</td><td>85ec9ca47d8f6807718151cbcca8b964</td></tr><tr><td>mpr-18811-mx.ic1</td><td>\bios</td><td></td></tr><tr><td>mpr-19367-mx.ic1</td><td>\bios</td><td></td></tr><tr><td>saturn_bios.bin</td><td>\bios\kronos</td><td>af5828fdff51384f99b3c4926be27762</td></tr></tbody></table>

## Contrôles

### Schéma de contrôles standard:

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Inversion des gâchettes:

Il est possible d'inverser les gâchettes et les boutons L/R avec l'option suivante:

<div align="left"><figure><img src="https://i.imgur.com/lpAcAex.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_invert_triggers.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Autres schémas de contrôles:

Des schémas de contrôles alernatifs sont disponibles avec l'option suivante:

<div align="left"><figure><img src="https://i.imgur.com/Ui2uKWH.png" alt=""><figcaption></figcaption></figure></div>

| Option                 | Schéma de contrôle                                                                                                                                        |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| L/R pour Y/Z           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_yz.png?raw=true" alt="" data-size="original">                 |
| L/R pour Y/Z (inversé) | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_yz_invert_triggers.png?raw=true" alt="" data-size="original"> |
| L/R pour X/Z           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_xz.png?raw=true" alt="" data-size="original">                 |
| L/R pour X/Z (inversé) | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_xz_invert_triggers.png?raw=true" alt="" data-size="original"> |

### Utiliser une manette de type Saturn

RetroBat détecte et configure automatiquement les manettes de type "Saturn" suivantes:

* 8Bitdo M30

Pour cela, activer l'option suivante:

<div align="left"><figure><img src="https://i.imgur.com/1KFcEBs.png" alt=""><figcaption></figcaption></figure></div>

Le mapping des manettes Saturn est géré par le fichier "**saturnControllers.json**" situé dans le répertoire `\system\resources\inputmapping` de l'installation RetroBat, il est possible d'ajouter d'autres manettes dans ce fichier pour automatiquement configurer votre contrôleur.

## Information spécifique au système

### Jeux multi-disques

Utiliser un fichier m3u pour gérer les jeux multi-disques.

Ci-dessous un exemple pour le jeu _Panzer Dragoon Saga_:&#x20;

<div align="left"><figure><img src="https://i.imgur.com/o3QZPs0.png" alt=""><figcaption></figcaption></figure></div>

Créer le fichier `Panzer Dragoon Saga.m3u` avec le contenu suivant et sauvegarder le fichier m3u dans le dossier `/roms/saturn` :

<div align="left"><figure><img src="https://i.imgur.com/gy9LuLH.png" alt=""><figcaption></figcaption></figure></div>
