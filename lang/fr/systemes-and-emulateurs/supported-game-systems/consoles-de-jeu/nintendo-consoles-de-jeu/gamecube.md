---
description: Nintendo
---

# GameCube

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/gc-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/gc.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Console de jeu - Durée de vie : 2001 - 2007

{% embed url="https://fr.wikipedia.org/wiki/GameCube" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>dolphin</li><li>libretro: dolphin</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> gamecube</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.gcz .iso .ciso .wbfs .wad .rvz .wia .m3u</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>Dolphin : NON<br>lr-dolphin : NON</td><td>Dolphin : NON<br>lr-dolphin : NON</td><td>Dolphin : OUI<br>lr-dolphin : OUI</td></tr></tbody></table>

| Succès Rétro | Parties en Réseau |
| ------------ | ----------------- |
| NON          | NON               |

## BIOS

Les BIOS ne sont pas nécessaires pour lancer des jeux Gamecube, mais certains sont requis pour améliorer le support de certains jeux au niveau graphiques ou encore des polices de caractères pour les textes des jeux.

<table data-header-hidden><thead><tr><th width="169">File</th><th width="625">Location &#x26; MD5</th><th data-hidden>MD5 Hash</th></tr></thead><tbody><tr><td><code>IPL.bin</code><br>Europe</td><td><p>Emplacement: <code>\emulators\dolphin-emu\User\GC\EUR</code></p><p>Emplacement libretro: <code>\saves\dolphin\User\GC\EUR</code><br>md5: <code>0cdda509e2da83c85bfe423dd87346cc</code></p></td><td></td></tr><tr><td><code>IPL.bin</code><br>Japan</td><td><p>Emplacement: <code>\emulators\dolphin-emu\User\GC\JAP</code></p><p>Emplacement libretro: <code>\saves\dolphin\User\GC\JAP</code><br>md5: <code>fc924a7c879b661abc37cec4f018fdf3</code></p></td><td></td></tr><tr><td><code>IPL.bin</code><br>USA</td><td><p>Emplacement: <code>\emulators\dolphin-emu\User\GC\USA</code></p><p>Emplacement libretro: <code>\saves\dolphin\User\GC\USA</code><br>md5: <code>019e39822a9ca3029124f74dd4d55ac4</code></p></td><td></td></tr></tbody></table>

## Dossiers

### Sauvegardes

Par défaut, Dolphin génère des sauvegardes au format "dossier CGI" à l'emplacement suivant:

`saves\dolphin\User\GC\EUR`

<div align="left">

<figure><img src="https://i.imgur.com/EGlIpe4.png" alt=""><figcaption></figcaption></figure>

</div>

Le sous-dossier de la région peut être modifié avec [le paramétrage](../../../../navigation/configuration-des-systemes-et-des-jeux.md) ci-dessous:

<div align="left">

<figure><img src="https://i.imgur.com/GuYVNfl.png" alt=""><figcaption></figcaption></figure>

</div>

Il est possible également de configurer Dolphin afin d'utiliser des fichiers SRAM (ancienne méthode, un fichier correspond à une carte mémoire de Gamecube) plutôt que des dossiers CGI:

<div align="left">

<figure><img src="https://i.imgur.com/lHnvqau.png" alt=""><figcaption></figcaption></figure>

</div>

Dans ce cas, le fichier de sauvegarde sera stocké dans le dossier :

`saves\dolphin\User\GC\`

## Contrôles

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans Dolphin:

* Contrôleurs XInput
* Dualshock 4 et Dualsense
* Nintendo Switch Pro
* Contrôleur original Gamecube avec un adaptateur Gamecube
{% endhint %}

| RetroBat key                                                                       | GameCube key             |
| ---------------------------------------------------------------------------------- | ------------------------ |
| START                                                                              | START                    |
| D-PAD                                                                              | D-PAD                    |
| Analog Stick - Left                                                                | Analog Stick - Left      |
| Analog Stick - Right                                                               | Analog Stick  - C-Stick  |
| ![A](<../../../../.gitbook/assets/image (19).png>)                                 | B                        |
| ![B](<../../../../.gitbook/assets/image (6).png>)                                  | A                        |
| <img src="../../../../.gitbook/assets/image (34).png" alt="" data-size="original"> | X                        |
| <img src="../../../../.gitbook/assets/image (32).png" alt="" data-size="line">     | Y                        |
| RB (R1)                                                                            | Z                        |
| LT (L2)                                                                            | L                        |
| RT (R2)                                                                            | R                        |

{% hint style="info" %}
Il est possible d'activer la fonction "RUMBLE" dans les options avancées.
{% endhint %}

## Information spécifique au système

### Jeux multi-disques

Utiliser un fichier `.m3u` pour les jeux multi-disques.&#x20;

Le fichier m3u doit contenir une ligne par disque du jeu, par exemple pour le jeu Baten Kaitos:

<div align="left">

<figure><img src="https://i.imgur.com/Hh12kWj.png" alt=""><figcaption></figcaption></figure>

</div>

Dans le fichier m3u, lister les noms exacts des fichiers des disques du jeu et sauvegarder:

<div align="left">

<figure><img src="https://i.imgur.com/aBZpJ4W.png" alt=""><figcaption></figcaption></figure>

</div>

### Textures "custom"

Il est possible d'utiliser des textures "custom" avec l'émulateur Dolphin.

Les packs de textures doivent être placés dans le dossier `\saves\dolphin\User\Load\Textures`.

<div align="left">

<figure><img src="https://i.imgur.com/jJm7Htu.png" alt=""><figcaption></figcaption></figure>

</div>

Le nom du dossier du pack de textures doit être strictement identique au **Game ID** du jeu, le Game ID est disponible depuis Dolphin en affichant les propriétés du jeu.

<div align="left">

<figure><img src="https://i.imgur.com/wWaNFxC.png" alt=""><figcaption></figcaption></figure>

</div>

Une fois le pack de textures correctement nommé et placé dans le bon dossier, activer les  **CUSTOM TEXTURES** dans Retrobat.

<div align="left">

<figure><img src="https://i.imgur.com/R5SWtvS.png" alt=""><figcaption><p>Options d'affichage > Configuration avancée du système</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/K5NInuR.png" alt=""><figcaption><p>Visual Rendering</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/UPixWDa.png" alt=""><figcaption><p>Custom Textures</p></figcaption></figure>

</div>
