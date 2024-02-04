---
description: Sega
---

# Dreamcast

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/dreamcast-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/dreamcast.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Console de jeu - Durée de vie: 1998 - 2001

{% embed url="https://fr.wikipedia.org/wiki/Dreamcast" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>Libretro: flycast</li><li>flycast</li><li>redream</li><li>demul</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> dreamcast</td></tr><tr><td><strong>Extensions</strong></td><td>.mds .mdf .cue .cdi .gdi .chd .m3u</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-flycast : OUI<br>Flycast : NON<br>Redream : NON<br>Demul : NON</td><td>lr-flycast : NON<br>Flycast : NON<br>Redream : NON<br>Demul : NON</td><td>lr-flycast : OUI<br>Flycast : OUI<br>Redream : OUI<br>Demul : OUI</td></tr></tbody></table>

## Bios

<table><thead><tr><th width="160.55555555555557">Fichier BIOS</th><th width="155">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>dc_boot.bin</td><td><code>\bios\dc</code></td><td>e10c53c2f8b90bab96ead2d368858623</td></tr><tr><td>dc_flash.bin</td><td><code>\bios\dc</code></td><td>0a93f7940c455905bea6e392dfde92a4</td></tr><tr><td>dc.zip</td><td><code>\bios\dc</code></td><td>Voir ci-dessous (pour demul uniquement)</td></tr></tbody></table>

{% hint style="info" %}
Pour Flycast standalone, les fichiers BIOS doivent être placés dans le dossier `emulators\flycast\data`.
{% endhint %}

#### Contenu du fichier BIOS

```
dc.zip
- 1_01d_01.bin "E10C53C2F8B90BAB96EAD2D368858623"
- 1_01d_02.bin "A5C6A00818F97C5E3E91569EE22416DC"
- 1_004_01.bin "37C921EB47532CAE8FB70E5D987CE91C"
- 1_011_01.bin "EAFCA1EED2D7F76C487E940597C2A786"
```

## Contrôles

| Retrobat                                          | Dreamcast        |
| ------------------------------------------------- | ---------------- |
| START                                             | START            |
| D-PAD                                             | D-PAD            |
| Stick analogique gauche                           | Stick analogique |
| Stick analogique droit                            |                  |
| ![](<../../../../.gitbook/assets/image (32).png>) | X                |
| ![](<../../../../.gitbook/assets/image (19).png>) | A                |
| ![](<../../../../.gitbook/assets/image (6).png>)  | B                |
| ![](<../../../../.gitbook/assets/image (34).png>) | Y                |
| L1                                                |                  |
| R1                                                |                  |
| L2                                                | L1               |
| R2                                                | R1               |
| L3                                                |                  |
| R3                                                |                  |

<div align="left">

<figure><img src="https://i.imgur.com/g71xmgZ.png" alt=""><figcaption></figcaption></figure>

</div>

## Information spécifique au système

### Jeux multi-disques

Utiliser un fichier m3u pour gérer les jeux multi-disques.

Ci-dessous un exemple pour le jeu _Alone In The Dark_:

<div align="left">

<figure><img src="https://i.imgur.com/LUmmLpf.png" alt=""><figcaption></figcaption></figure>

</div>

Créer un fichier `Alone in the dark The new nightmare.m3u` contenant les données suivantes et le sauvegarder dans le dossier `/roms/dreamcast`:

<div align="left">

<figure><img src="https://i.imgur.com/9dQJhD9.png" alt=""><figcaption></figcaption></figure>

</div>

Retrobat détecte le fichier m3u et masque automatiquement les fichiers individuels .gdi de la liste des jeux.

### Textures "custom"

Le coeur Flycast permet l'utilisation de packs de textures "custom".

Le pack de textures doit être placé dans le dossier `\bios\dc\textures\`:

<div align="left">

<figure><img src="https://i.imgur.com/65bX2kT.png" alt=""><figcaption></figcaption></figure>

</div>

Une fois le pack de textures placé dans le bon dossier, depuis Retrobat activer les **CUSTOM TEXTURES** dans [**CONFIGURATION AVANCEE DU SYSTEME**](../../../../navigation/view-options.md#configuration-avancees-du-systeme) ou dans [**CONFIGURATION AVANCEE DU JEU**](../../../../navigation/game-options.md#configuration-avancee-du-jeu).

<div align="left">

<figure><img src="https://i.imgur.com/ppkZ9bw.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/qVMX2Ly.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/SbsPMz1.png" alt=""><figcaption></figcaption></figure>

</div>
