---
description: Nintendo
---

# Nintendo 3DS

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/3ds-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/3ds.svg" alt="" width="563"></picture><figcaption></figcaption></figure></div>

Console de jeu portable - Durée de vie : 2011 - 2020

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_3DS" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>azahar</li><li>citra</li><li>mandarine</li></ul><ul><li>libretro-citra</li><li>bizhawk: encore</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> 3ds</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.3ds .3dsx .z3dsx .cia .zcia .elf .axf .cci .zcci .cxi .zcxi .app .m3u .zip .7z .squashfs</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="210">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>Azahar: OUI<br>Citra: OUI<br>Mandarine : OUI<br>lr-citra : OUI<br>BizHawk : OUI</td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire.

## Contrôles

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans azahar/citra/mandarine standalone :

* Contrôleurs XInput
* Dualshocks & DualSense
* Nintendo Switch Pro
{% endhint %}

{% hint style="info" %}
L'écran tactile de la 3DS est difficilement émulable, la meilleure solution est de connecter une souris.

Il est possible de simuler l'utilisation du touchscreen avec le stick droit de la manette, mais le mouvement n'est pas optimisé.
{% endhint %}

### Schéma de contrôle standard

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

L'option ci-dessous permet d'inverser les boutons pour correspondre au schéma XBOX:

<div align="left"><figure><img src="https://i.imgur.com/AKH8PsS.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_revert.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Gestion de l'écran tactile:

Selon l'émulateur, les options ci-dessous permettent de modifier le schéma de contrôle pour simuler les mouvements sur l'écran tactile à l'aide du stick analogique de droite.

#### Azahar, Citra et Mandarine

Utiliser l'option ci-dessous:

<div align="left"><figure><img src="https://i.imgur.com/nMNPq87.png" alt=""><figcaption></figcaption></figure></div>

| Option                     | Schéma de contrôles                                                                                                                                   |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sans inversion des boutons | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick.png?raw=true" alt="" data-size="original">        |
| Avec inversion des boutons | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick_revert.png?raw=true" alt="" data-size="original"> |

#### Libretro-citra et Bizhawk

Utiliser l'option ci-dessous:

<div align="left"><figure><img src="https://i.imgur.com/QR10lnB.png" alt=""><figcaption></figcaption></figure></div>

| Option                                         | Schéma de contrôle                                                                                                                                    |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>C-STICK ET POINTEUR<br>(sans inversion)</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick.png?raw=true" alt="" data-size="original">        |
| <p>C-STICK ET POINTEUR<br>(avec inversion)</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick_revert.png?raw=true" alt="" data-size="original"> |
| <p>POINTEUR<br>(sans inversion)</p>            | <img src="../../../../.gitbook/assets/3ds_stylus.png" alt="" data-size="original">                                                                    |
| <p>POINTEUR<br>(avec inversion)</p>            | <img src="../../../../.gitbook/assets/3ds_stylus_cstick.png" alt="" data-size="original">                                                             |
| C-STICK                                        | Identique au schéma standard                                                                                                                          |

## Information spécifique au système

### Emplacement des données

<table><thead><tr><th width="254">Données</th><th>Chemin (relatif au dossier RetroBat)</th></tr></thead><tbody><tr><td>nand path</td><td>saves\3ds\&#x3C;emulator>\nand</td></tr><tr><td>sdmc path</td><td>saves\3ds\&#x3C;emulator>\sdmc</td></tr><tr><td>config file</td><td>emulators\&#x3C;emulator>\user\config\qt-config.ini</td></tr></tbody></table>

### Lancer des applications installées dans la NAND

Pour lancer un jeu qui a été installé dans la mémoire de la NAND de la console, il est possible d'utiliser un fichier .m3u pointant vers le fichier .app du jeu.

Exemple de jeu installé dans la NAND:

<div align="left"><figure><img src="https://i.imgur.com/QTV0dld.png" alt=""><figcaption></figcaption></figure></div>

Créer un raccourci en cliquant avec le bouton droit sur le jeu depuis l'émulateur:

<div align="left"><figure><img src="https://i.imgur.com/rTA8IEw.png" alt=""><figcaption></figcaption></figure></div>

Depuis le bureau Windows, effectuer un clic droit > propriétés, puis copier le contenu du raccourci dans un fichier .txt (ne garder que la dernière partie du chemin de l'application, sans les ""):

<div align="left"><figure><img src="https://i.imgur.com/o7E5uFQ.png" alt=""><figcaption></figcaption></figure></div>

Sauvegarder le fichier avec l'extension .m3u et le placer dans roms\3ds:

<div align="left"><figure><img src="https://i.imgur.com/g2xUhcm.png" alt=""><figcaption></figcaption></figure></div>

### Textures personnalisées

Les émulateurs Lime3DS et Citra permet l'utilisation de packs de textures personnalisés.

Les textures doivent être copiées dans le dossier `\emulators\`<mark style="color:purple;">`<émulateur>`</mark>`\User\Load\Textures\<gameID>`, par exemple pour le jeu Super Mario 3D Land:

<div align="left"><figure><img src="https://i.imgur.com/6dLxUWC.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Pour le core libretro, les textures sont à positionner dans le dossier:

`\saves\3ds\citra\Load\Textures\<gameID>`
{% endhint %}

Le nom du dossier dans lequel il faut copier les textures peut être retrouvé en effectuant un clic-droit sur le jeu dans l'interface de l'émulateur, puis en sélectionnant l'option "Ouvrir l'emplacement personnalisé des textures".

<div align="left"><figure><img src="https://i.imgur.com/kT4RLmY.png" alt=""><figcaption></figcaption></figure></div>

Une fois le pack de textures correctement copié, activer les textures personnalisées dans RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/HMiSQ1r.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/6OUlief.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/89Ed74U.png" alt=""><figcaption></figcaption></figure></div>
