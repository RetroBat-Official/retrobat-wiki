---
description: Nintendo
---

# Nintendo 3DS

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/3ds-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/3ds.svg" alt="" width="563"></picture><figcaption></figcaption></figure></div>

Console de jeu portable - Durée de vie : 2011 - 2020

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_3DS" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>azahar</li><li>libretro-azahar</li><li>mandarine</li><li>citra</li><li>bizhawk: encore</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> 3ds</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.3ds .3dsx .z3dsx .cia .zcia .elf .axf .cci .zcci .cxi .zcxi .app .m3u .zip .7z .squashfs</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="210">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td><p>Azahar : OUI</p><p>lr-azahar : OUI</p><p>Mandarine : OUI<br>Citra : OUI<br>BizHawk : OUI</p></td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire.

## Contrôles

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

Selon l'émulateur, et les options définies depuis le menu RetroBat, la souris ou le stick droit permettent de simuler les mouvements sur l'écran tactile.

Azahar, Mandarine et Citra permettent également de sélectionner un profil tactile spécifique, créer depuis l'émulateur : &#x20;

<figure><img src="../../../../.gitbook/assets/2026-03-28_09h25_33.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Vous devez vous souvenir du nom du profil crée et le renseigner dans RetroBat
{% endhint %}

### Disposition de boutons supplémentaires

D'autres configurations de boutons sont disponibles selon les émulateurs, elles sont disponibles depuis le menu Configuration avancée du système > Contrôles :&#x20;

<figure><img src="../../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>



| Option                                                                                                                        | Schéma de contrôles                                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Stick de droite comme pointeur d'écran tactile</strong><br><br>Libretro-Azahar<br>Bizhawk</p>                      | <img src="../../../../.gitbook/assets/image (46).png" alt="" data-size="original">                                                                    |
| <p><strong>Stick de droite comme pointeur d'écran tactile (inversé)</strong><br><br>Libretro-Azahar<br>Bizhawk</p>            | <img src="../../../../.gitbook/assets/image (45).png" alt="" data-size="original">                                                                    |
| <p><strong>Stick de droite comme C-stick et pointeur d'écran tactile</strong><br><br>Libretro-Azahar<br>Bizhawk</p>           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick.png?raw=true" alt="" data-size="original">        |
| <p><strong>Stick de droite comme C-stick et pointeur d'écran tactile (inversé)</strong><br><br>Libretro-Azahar<br>Bizhawk</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick_revert.png?raw=true" alt="" data-size="original"> |

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
