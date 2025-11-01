---
description: Nintendo
---

# Switch

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/switch.svg" alt=""><figcaption></figcaption></figure></div>

Console de jeu hybride - durée de vie: 2017 - aujourd'hu

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_Switch" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>citron</li><li>ryujinx</li><li>eden</li><li>sudachi</li><li>suyu</li><li>yuzu</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> switch</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.nso .nro .nca .xci .nsp .kip</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td><p>Ryujinx : OUI</p><p>Eden : OUI<br>Citron : OUI</p><p>Sudachi : OUI<br>Suyu : OUI<br>Yuzu : OUI</p></td></tr></tbody></table>

## Emulateur

### Ryujinx

Copier les fichiers de l'émulateur Ryujinx dans le dossier `emulators\ryujinx` de l'installation RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/KSvr9sk.png" alt=""><figcaption></figcaption></figure></div>

### Citron, Eden, Sudachi, Yuzu, Suyu

Copier les fichiers de l'émulateur dans le dossier `emulators\citron` (ou eden, suyu, yuzu, sudachi), puis créer le sous-dossier "user":

<div align="left"><figure><img src="https://i.imgur.com/h7HVNfj.png" alt=""><figcaption></figcaption></figure></div>



### Emplacement des fichiers

<table><thead><tr><th width="276">Données</th><th>Chemin (relatif au dossier RetroBat)</th></tr></thead><tbody><tr><td>Données utilisateur de l'émulateur</td><td><strong>Ryujinx</strong>: saves\switch\ryujinx\portable<br><strong>Eden, Yuzu, Suyu, Sudachi, Citron :</strong> <br>emulators\&#x3C;emulator name>\user</td></tr><tr><td>Fichier de configuration</td><td><strong>Ryujinx</strong>: saves\switch\ryujinx\portable\Config.json<br><strong>Eden, Yuzu, Suyu, Sudachi, Citron :</strong> <br>emulators\&#x3C;emulator name>\user\config\qt-config.ini</td></tr></tbody></table>

Pour les émulateurs Citron, Sudachi, Eden, Yuzu et Suyu, il est possible de mettre en commun les dossiers SDMC, LOAD, NAND dans le dossier `saves\switch` de l'installation RetroBat.

Pour cela, activer l'option suivante:

<div align="left"><figure><img src="https://i.imgur.com/0BBXub2.png" alt=""><figcaption></figcaption></figure></div>



## BIOS

Il est nécessaire d'extraire le firmware et le fichier `prod.keys` de votre console Nintendo SWITCH et de les placer dans des répertoires dédiés selon l'émulateur:

### Ryujinx

Placer le fichier prod.keys dans le dossier `\saves\switch\ryujinx\portable\system`

Installer le firmware directement depuis l'émulateur, en utilisant le fichier "Configure Ryujinx.bat" pour lancer Ryujinx ou en lançant Ryujinx depuis le menu RetroBat.

{% hint style="danger" %}
Cette étape est impérative pour le bon fonctionnement de l'émulateur.

Si le fichier "Configure Ryujinx.bat" n'existe pas dans le dossier `emulators\ryujinx`, vous pouvez le retrouver dans le dossier `system\templates\ryujinx` et le copier dans le dossier de l'émulateur.
{% endhint %}

<div align="left"><figure><img src="https://i.imgur.com/CVXr1y7.png" alt=""><figcaption><p>Tools > Install Firmware</p></figcaption></figure></div>

### Eden, Sudachi, Suyu, Yuzu et Citron

Placer prod.keys dans le dossier `\emulators\`<mark style="color:purple;">`<émulateur>`</mark>`\user\keys`

Placer les fichiers .nca du firmware dans le dossier `\emulators\`<mark style="color:purple;">`<émulateur>`</mark>`\user\nand\system\Contents\registered`

## Contrôles

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans les émulateurs Switch:

* Contrôleurs XInput
* Dualshocks & DualSense
* Nintendo Switch Pro
{% endhint %}

| RetroBat                                                                           | Switch                      |
| ---------------------------------------------------------------------------------- | --------------------------- |
| START                                                                              | +                           |
| SELECT / BACK                                                                      | -                           |
| D-PAD                                                                              | D-PAD                       |
| Stick analogique gauche                                                            | Stick analogique gauche     |
| Stick analogique droit                                                             | Stick analogique droit      |
| ![A](<../../../../.gitbook/assets/image (20).png>)                                 | <p>B<br>Ou A si inversé</p> |
| ![B](<../../../../.gitbook/assets/image (7).png>)                                  | <p>A<br>Ou B si inversé</p> |
| <img src="../../../../.gitbook/assets/image (35).png" alt="" data-size="original"> | <p>X<br>Ou Y si inversé</p> |
| <img src="../../../../.gitbook/assets/image (33).png" alt="" data-size="line">     | <p>Y<br>Ou X si inversé</p> |
| LB (L1)                                                                            | L                           |
| RB (R1)                                                                            | R                           |
| L2                                                                                 | ZL                          |
| R2                                                                                 | ZR                          |
| L3                                                                                 | L3                          |
| R3                                                                                 | R3                          |

L'option pour inverser les boutons se trouve ici:

<div align="left"><figure><img src="https://i.imgur.com/vy1VRvy.png" alt=""><figcaption></figcaption></figure></div>

### Installer les mises à jour et les DLC des jeux

Tous les émulateurs permettent l'installation de mises à jour et de DLC pour vos jeux.&#x20;

Les mises à jour et les DLC des jeux sont des fichiers au format .nsp que vous devez extraire de votre console SWITCH.

#### Ryujinx

Depuis la liste de jeux dans Ryujinx, effectuer un clic droit sur le jeu et choisir **Manage Title Updates** ou **Manage DLC**

<div align="left"><figure><img src="https://i.imgur.com/uRMjmAE.png" alt=""><figcaption></figcaption></figure></div>

Dans l'écran suivant, rechercher le fichier .nsp sur votre ordinateur, le sélectionner et sauvegarder pour lancer l'installation:

<div align="left"><figure><img src="https://i.imgur.com/Vk2lwA3.png" alt=""><figcaption></figcaption></figure></div>

#### Eden, Citron, Sudachi, Suyu, Yuzu

Aller dans `Files > Install Files to NAND...`

<div align="left"><figure><img src="https://i.imgur.com/B6jQIqZ.png" alt=""><figcaption></figcaption></figure></div>

Dans l'écran suivant, rechercher le fichier .nsp sur votre ordinateur, le sélectionner et sauvegarder pour lancer l'installation.
