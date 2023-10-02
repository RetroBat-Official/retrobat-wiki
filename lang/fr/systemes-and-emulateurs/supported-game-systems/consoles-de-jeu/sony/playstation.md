---
description: Sony
---

# PlayStation

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/psx.svg" alt=""><figcaption></figcaption></figure>

</div>

Console de jeu - Durée de jeu: 1994 - 2006

{% embed url="https://fr.wikipedia.org/wiki/PlayStation" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro: mednafen_psx_hw</li><li>libretro: swanstation</li><li>libretro: pcsx_rearmed</li><li>duckstation</li><li>mednafen</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> psx</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .img .mdf .pbp .toc .cbn .m3u .ccd .chd .zip .7z .iso .cso</td><td></td></tr></tbody></table>

## Fonctionnalités

| Succès Rétro               | Parties en Réseau |
| -------------------------- | ----------------- |
| OUI (inculant Duckstation) | NON               |

## BIOS

<table><thead><tr><th width="187">Fichier BIOS</th><th width="162">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>scph1001.bin</td><td><code>\bios</code></td><td>dc2b9bf8da62ec93e868cfd29f0d067d</td></tr><tr><td>scph5500.bin</td><td><code>\bios</code></td><td>8dd7d5296a650fac7319bce665a6a53c</td></tr><tr><td>scph5501.bin</td><td><code>\bios</code></td><td>490f666e1afb15b7362b406ed1cea246</td></tr><tr><td>scph5502.bin</td><td><code>\bios</code></td><td>32736f17079d0b2b7024407c39bd3050</td></tr><tr><td>scph7001.bin</td><td><code>\bios</code></td><td>1e68c231d0896b7eadcad1d7d8e76129</td></tr></tbody></table>

## Contrôles

RetroBat permet la configuration automatique pour tous les émulateurs PSX: libretro & Duckstation.

| RetroBat                                                                           | Playstation             |
| ---------------------------------------------------------------------------------- | ----------------------- |
| START                                                                              | START                   |
| SELECT                                                                             | SELECT                  |
| D-PAD                                                                              | D-PAD                   |
| Stick analogique gauche                                                            | Stick analogique gauche |
| Stick analogique droit                                                             | Stick analogique droit  |
| ![A](<../../../../.gitbook/assets/image (19).png>)                                 | Croix                   |
| ![B](<../../../../.gitbook/assets/image (6).png>)                                  | Rond                    |
| <img src="../../../../.gitbook/assets/image (34).png" alt="" data-size="original"> | Triangle                |
| <img src="../../../../.gitbook/assets/image (32).png" alt="" data-size="line">     | Carré                   |
| L1                                                                                 | L1                      |
| R1                                                                                 | R1                      |
| L2                                                                                 | L2                      |
| R2                                                                                 | R2                      |
| L3                                                                                 | L3                      |
| R3                                                                                 | R3                      |

<div align="left">

<figure><img src="https://i.imgur.com/9sz2VFM.png" alt=""><figcaption></figcaption></figure>

</div>

## Information spécifique au système

### Jeux multi-disques

Utiliser un fichier `.m3u` pour les jeux multi-disques.&#x20;

Le fichier m3u doit contenir une ligne par disque du jeu, par exemple pour le jeu Chrono Cross:

<div align="left">

<figure><img src="https://i.imgur.com/GGRxCI4.png" alt=""><figcaption><p>List of files</p></figcaption></figure>

</div>

Dans le fichier m3u, lister les noms exacts des fichiers `.cue`  des disques du jeu:

<div align="left">

<figure><img src="https://i.imgur.com/ZzJ7Ldj.png" alt=""><figcaption></figcaption></figure>

</div>



### Textures personnalisées

Le coeur mednafen\_psx\_hw permet l'utilisation de packs de textures "customs" pour remplacer les textures originales du jeu.

Pour utiliser un pack de textures, placer le pack dans le dosisier `\roms\psx` dans un sous-dossier portant le même nom que le fichier du jeu suivi de "-texture-replacements", par exemple:

* Pour le fichier de jeu `Final Fantasy VII (USA).iso`, le dossier du pack de texture doit être nommé `Final Fantasy VII (USA)-texture-replacements`
* Pour le fichier de jeu `Chrono Cross.fr.m3u`, le dossier du pack de texture doit être nommé  `Chrono Cross.fr-texture-replacements`

<div align="left">

<figure><img src="https://i.imgur.com/GdXSRWK.png" alt=""><figcaption></figcaption></figure>

</div>

Une fois le dossier du pack de textures correctement nommé et positionné, activer l'option dans Retrobat:

<div align="left">

<figure><img src="https://i.imgur.com/aYOKr3Y.png" alt=""><figcaption><p>Configuration avancée > Visual Rendering > Custom textures</p></figcaption></figure>

</div>

Il est également nécessaire d'utiliser le driver vidéo VULKAN et de définir une résolution supérieure à la résolution native 1X:

<div align="left">

<figure><img src="https://i.imgur.com/zrGr0gu.png" alt=""><figcaption><p>Configuration avancée > Drivers, sélectionner VULKAN</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/IAXDrdW.png" alt=""><figcaption><p>Configuration avancée > Résolution Interne supérieure à 1X</p></figcaption></figure>

</div>
