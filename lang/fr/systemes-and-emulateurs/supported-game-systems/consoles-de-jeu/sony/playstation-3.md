---
description: Sony
---

# Playstation 3

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/ps3-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/ps3.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Console de jeu - Durée de jeu: 2006 - 2017

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_3" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>rpcs3</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> ps3</td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .ps3 .iso .7z .zip .rar .squashfs</td></tr></tbody></table>

<table><thead><tr><th width="187">Fichier BIOS</th><th width="109">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>PS3UPDAT.PUP</td><td><code>\bios</code></td><td>95307e1b51d3bcc33a274db91488d29f</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>OUI</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="187">Fichier BIOS</th><th width="109">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>PS3UPDAT.PUP</td><td><code>\bios</code></td><td>95307e1b51d3bcc33a274db91488d29f</td></tr></tbody></table>

#### Installation automatique du firmware

Au premier lancement d'un jeu PS3 avec l'émulateur rpcs3 depuis Retrobat, si le fichier PS3UPDAT.PUP présent dans le dossier \bios de Retrobat, l'émulateur vous proposera automatiquement d'installer le firmware. Une fois l'installation terminée, vous pouvez quitter Rpcs3 et relancer le jeu depuis Retrobat.

<div align="left">

<figure><img src="https://i.imgur.com/1ovzizA.png" alt=""><figcaption></figcaption></figure>

</div>

#### Installation manuelle du firmware

Lancer l'éxecutable rpcs3.exe dans le dossier `\emulators\rpcs3` et sélectionner **install firmware**

<div align="left">

<figure><img src="https://i.imgur.com/18HE0DC.png" alt=""><figcaption></figcaption></figure>

</div>

Choisir le fichier **PS3UPDAT.PUP** pour démarrer l'installation du firmware.

La version installée du Firmware apparait dans le log en bas de l'écran de l'émulateur:

<div align="left">

<figure><img src="https://i.imgur.com/JFjxamH.png" alt=""><figcaption></figcaption></figure>

</div>

## Contrôles

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans rpcs3:

* Contrôleurs XInput
* Dualshocks & DualSense
* Nintendo Switch Pro
{% endhint %}

| RetroBat                                                                           | Playstation 3           |
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

## Information spécifique au système

### Ajouter les jeux

Il existe 2 formats de jeux pour la PS3: les disques Blu-Ray et les jeux PSN (PlayStation Network):

* Les jeux ayant une ID commençant par la lettre 'B' sont des jeux Blu-Ray.
* Les jeux ayant une ID commençant par la lettre 'N' sont des jeux dématérialisés (PS Store)

<div align="left">

<figure><img src="https://i.imgur.com/EsmEoB4.png" alt=""><figcaption></figcaption></figure>

</div>

Les jeux au format Blu-ray disc peuvent être placés directement dans le dossier  `\roms\ps3`, les jeux dématérialisés doivent être placés dans le dossier `\emulators\rpcs3\dev_hdd0\game` de votre installation RetroBat.

{% hint style="danger" %}
Les jeux PSN doivent être décryptés pour pouvoir être lus par RPCS3.
{% endhint %}

#### Ajouter un jeu Blu-ray

Copier simplement le dossier du jeu dans le dossier `\roms\ps3` de votre installation RetroBat et renommer le dossier avec une extension .ps3:

<div align="left">

<figure><img src="https://i.imgur.com/E98BUs9.png" alt=""><figcaption></figcaption></figure>

</div>

Le jeu sera directement disponible dans RetroBat.

#### Ajouter un jeu PSN

Une fois que l'émulateur est configuré, que le jeu est ajouté et qu'il fonctionne correctement lorsqu'il est lancé depuis l'émulateur, créer un fichier m3u et le placer dans le dossier `\roms\ps3` .

Le fichier m3u doit pointer vers le fichier **EBOOT.BIN** se trouvant dans le dossier du jeu dans le répertoire `\emulators\rpcs3\dev_hdd0\game`, ci-dessous un exemple pour le jeu BulletStorm:

<div align="left">

<figure><img src="https://i.imgur.com/E1igTL6.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/LmL6NUh.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
L'outil BATGUI permet la création automatique des m3u. Se référer à la section [BATGUI ](../../../../utilisation-avancee/batgui.md)du wiki.
{% endhint %}
