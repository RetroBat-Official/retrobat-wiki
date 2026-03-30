---
description: Sony
---

# PlayStation

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/psx-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/psx.svg" alt=""></picture><figcaption></figcaption></figure></div>

Console de jeu - Durée de jeu: 1994 - 2006

{% embed url="https://fr.wikipedia.org/wiki/PlayStation" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro: mednafen_psx_hw</li><li>libretro: swanstation</li><li>libretro: pcsx_rearmed</li><li>duckstation</li><li>mednafen</li><li>bizhawk: Nymashock</li><li>bizhawk: Octoshock</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> psx</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .img .mdf .pbp .toc .cbn .m3u .ccd .chd .zip .7z .iso .cso .squashfs</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-mednafen : OUI<br>lr-swanstation : OUI<br>lr-pcsx-rearmed : OUI<br>Duckstation : OUI<br>Mednafen : NON<br>BizHawk : OUI</td><td>lr-mednafen : OUI<br>lr-swanstation : NON<br>lr-pcsx-rearmed : OUI<br>Duckstation : NON<br>Mednafen : NON<br>BizHawk : NON</td><td>lr-mednafen : OUI<br>lr-swanstation : OUI<br>lr-pcsx-rearmed : OUI<br>Duckstation : OUI<br>Mednafen : OUI<br>BizHawk : OUI</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="187">Fichier BIOS</th><th width="162">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>psxonpsp660.bin</td><td><code>\bios</code></td><td>c53ca5908936d412331790f4426c6c33</td></tr><tr><td>scph5500.bin</td><td><code>\bios</code></td><td>8dd7d5296a650fac7319bce665a6a53c</td></tr><tr><td>scph5501.bin</td><td><code>\bios</code></td><td>490f666e1afb15b7362b406ed1cea246</td></tr><tr><td>scph5502.bin</td><td><code>\bios</code></td><td>32736f17079d0b2b7024407c39bd3050</td></tr><tr><td>scph7001.bin</td><td><code>\bios</code></td><td>1e68c231d0896b7eadcad1d7d8e76129</td></tr></tbody></table>

## Contrôles

### Schéma de contrôles:

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/psx.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Schéma alternatif:

Afin de pouvoir utiliser les gâchettes analogiques pour les jeux de course, il est possible d'utiliser un schéma de contrôles alternatif en activant cette option:

<div align="left"><figure><img src="https://i.imgur.com/vD1Jcqk.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/psx_triggers_rstick.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Afin de pouvoir utiliser les gâchettes, il est nécessaire de changer le schéma de contrôle dans le jeu, en passant l'accélération et le freinage sur le stick analogique droit.

Seul le contrôleur analogique est compatible avec ce schéma.
{% endhint %}

## Information spécifique au système

### Jeux multi-disques

Utiliser un fichier `.m3u` pour les jeux multi-disques.&#x20;

Le fichier m3u doit contenir une ligne par disque du jeu, par exemple pour le jeu Chrono Cross:

<div align="left"><figure><img src="https://i.imgur.com/GGRxCI4.png" alt=""><figcaption><p>List of files</p></figcaption></figure></div>

Dans le fichier m3u, lister les noms exacts des fichiers `.cue`  des disques du jeu:

<div align="left"><figure><img src="https://i.imgur.com/ZzJ7Ldj.png" alt=""><figcaption></figcaption></figure></div>

### Textures personnalisées

#### Libretro-mednafen\_psx\_hw

Le cœur mednafen\_psx\_hw permet l'utilisation de packs de textures "customs" pour remplacer les textures originales du jeu.

Pour utiliser un pack de textures, placer le pack dans le dosisier `\roms\psx` dans un sous-dossier portant le même nom que le fichier du jeu suivi de "-texture-replacements", par exemple:

* Pour le fichier de jeu `Final Fantasy VII (USA).iso`, le dossier du pack de texture doit être nommé `Final Fantasy VII (USA)-texture-replacements`
* Pour le fichier de jeu `Chrono Cross.fr.m3u`, le dossier du pack de texture doit être nommé  `Chrono Cross.fr-texture-replacements`

<div align="left"><figure><img src="https://i.imgur.com/GdXSRWK.png" alt=""><figcaption></figcaption></figure></div>

Une fois le dossier du pack de textures correctement nommé et positionné, activer l'option dans Retrobat :

<figure><img src="../../../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Configuration avancée du système > rendu visuel</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Textures personnalisées activées</p></figcaption></figure>

Il est également nécessaire d'utiliser le driver vidéo VULKAN et de définir une résolution supérieure à la résolution native 1X:

<figure><img src="../../../../.gitbook/assets/image (11).png" alt=""><figcaption><p>options avancés > Pilotes</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

#### **Duckstation**

L'émulateur Duckstation permet de charger des textures personnalisées.

RetroBat n'impose pas d'emplacement pour le placement des packs de textures pour Duckstation, l'emplacement par défaut est dans le dossier `\emulators\duckstation\textures`, mais le répertoire peux être modifié depuis les paramètres de l'émulateur :

<figure><img src="../../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

Une fois que le pack de textures est placé, activer l'option dans RetroBat dans le menu **OPTIONS AVANCÉES > RENDU VISUEL** :

<figure><img src="../../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>
