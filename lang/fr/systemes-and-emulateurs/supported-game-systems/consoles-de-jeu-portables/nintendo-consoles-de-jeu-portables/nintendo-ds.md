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

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro: melonds DS</li><li>libretro : desmume</li><li>libretro : desmume2015</li><li>libretro : melonds</li><li>melonds</li><li>bizhawk: melonDS</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> nds</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.nds .bin .zip .7z</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-melondsds : OUI<br>lr-desmume : OUI<br>lr-desmume2015 : OUI<br>lr-melonds : OUI<br>MelonDS : NON<br>Ares : NON<br>BizHawk : OUI</td><td>lr-melondsds : NON<br>lr-desmume : OUI<br>lr-desmume2015 : OUI<br>lr-melonds : NON<br>MelonDS : NON<br>Ares : NON<br>BizHawk : NON</td><td>lr-melondsds : OUI<br>lr-desmume : OUI<br>lr-desmume2015 : OUI<br>lr-melonds : OUI<br>MelonDS : OUI<br>Ares : OUI<br>BizHawk : OUI</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="187">Fichier BIOS</th><th width="98">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>firmware.bin</td><td><code>\bios</code></td><td>145eaef5bd3037cbc247c213bb3da1b3</td></tr><tr><td>bios7.bin</td><td><code>\bios</code></td><td>df692a80a5b1bc90728bc3dfc76cd948</td></tr><tr><td>bios9.bin</td><td><code>\bios</code></td><td>a392174eb3e572fed6447e956bde4b25</td></tr><tr><td>dsi_bios9.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_bios7.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_firmware.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_nand.bin</td><td><code>\bios</code></td><td></td></tr></tbody></table>

## Contrôles

En dehors de l'émulateur standalone MelonDS, tous les émulateurs permettent de simuler l'écran tactile avec le joystick droit, cette option doit être activée dans les options avancées du système > contrôles:

<div align="left">

<figure><img src="https://i.imgur.com/3SNiUdQ.png" alt=""><figcaption></figcaption></figure>

</div>

| Option / émulateur                  | Schéma de contrôles                                                                                                                                    |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| lr-melondsds                        | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melondsds.png?raw=true" alt="" data-size="original">             |
| <p>lr-desmume<br>lr-desmume2015</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds.png?raw=true" alt="" data-size="original">                       |
| lr-melonds                          | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds.png?raw=true" alt="" data-size="original">               |
| MelonDS standard                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds_standalone.png?raw=true" alt="" data-size="original">    |
| MelonDS (stick gauche)              | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds_standalone_ls.png?raw=true" alt="" data-size="original"> |
| BizHawk standard                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_bizhawk.png?raw=true" alt="" data-size="original">               |
| BizHawk (souris)                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_bizhawk_mouse.png?raw=true" alt="" data-size="original">         |

## Information spécifique au système

### Lancer des jeux DSi

Le core libretro melonDS\_DS permet de lancer la nativement les jeux DSiWare.

Pour MelonDS et libretro:melonDS, RetroBat permet de lancer des fichiers "nand" DSi (.bin) (cela permet notamment de jouer à des jeux de type DSiware, qui étaient installés directement dans la mémoire de la console).

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
