---
description: Nintendo
---

# Nintendo DS

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/nds.svg" alt=""><figcaption></figcaption></figure>

</div>

Console de jeu portable - Durée de vie : 2004- 2011

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_DS" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro : desmume</li><li>libretro : desmume2015</li><li>libretro : melonds</li><li>melonds</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> nds</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.nds .bin .zip .7z</td><td></td></tr></tbody></table>

## Fonctionnalités

| Retroachievements | NetPlay                  |
| ----------------- | ------------------------ |
| OUI               | OUI (uniquement DesMUme) |

## BIOS

<table><thead><tr><th width="187">Fichier BIOS</th><th width="98">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>firmware.bin</td><td><code>\bios</code></td><td>145eaef5bd3037cbc247c213bb3da1b3</td></tr><tr><td>bios7.bin</td><td><code>\bios</code></td><td>df692a80a5b1bc90728bc3dfc76cd948</td></tr><tr><td>bios9.bin</td><td><code>\bios</code></td><td>a392174eb3e572fed6447e956bde4b25</td></tr><tr><td>dsi_bios9.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_bios7.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_firmware.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_nand.bin</td><td><code>\bios</code></td><td></td></tr></tbody></table>

## Contrôles

{% hint style="info" %}
Le stylet peut être émulé soit par la souris, soit par le stick analogique droit de la manette (le choix est disponible dans les fonctions avancées > contrôles).
{% endhint %}

| RetroBat                                                                           | Nintendo DS                                                                             |
| ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| START                                                                              | START                                                                                   |
| SELECT                                                                             | SELECT                                                                                  |
| D-PAD                                                                              | D-PAD                                                                                   |
| Left analog stick                                                                  |                                                                                         |
| Right analog stick                                                                 | Ecran tactile (stylet)                                                                  |
| ![A](<../../../../.gitbook/assets/image (19).png>)                                 | B                                                                                       |
| ![B](<../../../../.gitbook/assets/image (6).png>)                                  | A                                                                                       |
| <img src="../../../../.gitbook/assets/image (34).png" alt="" data-size="original"> | X                                                                                       |
| <img src="../../../../.gitbook/assets/image (32).png" alt="" data-size="line">     | Y                                                                                       |
| L1                                                                                 | L                                                                                       |
| R1                                                                                 | R                                                                                       |
| L2                                                                                 | DesMUme: Fermeture du couvercle                                                         |
| R2                                                                                 | <p>DesMUme: Appui sur l'écran tactile<br>MelonDS: Changer la disposition de l'écran</p> |
| L3                                                                                 | <p>DesMUme: Activer le Microphone<br>MelonDS: Fermeture du couvercle</p>                |
| R3                                                                                 | DesMUme: Changer la disposition de l'écran                                              |

<div align="left">

<figure><img src="https://i.imgur.com/5Fa7LxI.png" alt=""><figcaption></figcaption></figure>

</div>

## Information spécifique au système

### Lancer des jeux DSi

RetroBat permet de lancer des fichiers "nand" DSi (.bin) avec les émulateurs libretro:melonDS et melonDS (cela permet notamment de jouer à des jeux de type DSiware, qui étaient installés directement dans la mémoire de la console).

Pour cela, il est nécessaire de disposer d'un fichier "nand" de la console et de déposer ce fichier '.bin' dans le dossier `roms\nds` de votre installation RetroBat. Lors du lancement de ce type de fichier, RetroBat va automatiquement lancer le menu d'accueil de la console et monter le fichier "nand", permettant ainsi de sélectionner les jeux installés sur cette "nand":

#### Exemple d'un fichier "NAND":

<div align="left">

<figure><img src="https://i.imgur.com/gzpnw8S.png" alt=""><figcaption></figcaption></figure>

</div>

Lors du lancement depuis RetroBat, l'émulateur charge directement le menu de la console:

<div align="left">

<figure><img src="https://i.imgur.com/m2XG9ZQ.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/CUHgynR.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/sPQNh6q.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Noter que melonDS permet le lancement direct d'un fichier "nand" sans aucun prérequis,  libretro:melonds par contre, nécessite la présence d'au moins 1 fichier de jeu .nds dans le dossier `roms\nds` (la présence d'un jeu est nécessaire pour permettre à RetroArch de charger le core libretro).
{% endhint %}

### Comment ajouter des jeux à un fichier "nand" ?

Seul l'émulateur melonDS permet de modifier un fichier "nand" en ajoutant ou supprimant des jeux, pour cela, procéder comme suit

* Exécuter melonDS (`emulators\melonds`)
* Naviguer dans config > emu settings, puis dans l'onglet DSi-mode :

<div align="left">

<figure><img src="https://i.imgur.com/KlcN2nS.png" alt=""><figcaption></figcaption></figure>

</div>

* Cliquer sur "Browse..." et sélectionner le chemin vers le fichier "nand" à modifier, puis cliquer sur "OK"
* Fermer le menu et naviguer vers system > Manage DSi titles

<div align="left">

<figure><img src="https://i.imgur.com/z8t4zHy.png" alt=""><figcaption></figcaption></figure>

</div>

* Dans le prochain écran, il est possible de supprimer ou d'ajouter des titres sur la "nand"

<div align="left">

<figure><img src="https://i.imgur.com/1Y5RUtd.png" alt=""><figcaption></figcaption></figure>

</div>

* Presser "import title..." puis, dans l'écran suivant, sélectionner le jeu à installer sur la "nand"

<div align="left">

<figure><img src="https://i.imgur.com/tGcMnSu.png" alt=""><figcaption></figcaption></figure>

</div>

* Confirmer en pressant "OK", le jeu est désormais installé dans la "nand" et est disponible lorsque la "nand" est chargée depuis RetroBat

{% hint style="danger" %}
Les fichiers "nand" sont très sensibles et peuvent rapidement être corrompus en cas de fausse manipulation, ils ont notamment une limite de taille. Si lors du lancement d'un fichier nand melonDS affiche un écran noir, cela signifie que le fichier nand est invalide.
{% endhint %}
