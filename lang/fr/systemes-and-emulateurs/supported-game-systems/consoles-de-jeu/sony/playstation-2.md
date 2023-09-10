---
description: Sony
---

# PlayStation 2

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/ps2.svg" alt=""><figcaption></figcaption></figure>

</div>

Console de jeu - Durée de jeu: 2000 - 2013

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_2" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>pcsx2</li><li>pcsx2-16</li><li>play</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> ps2</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .cso .bin .mdf .gz .chd</td><td></td></tr></tbody></table>

## Fonctionnalités

| Succès Rétro                    | Parties en Réseau |
| ------------------------------- | ----------------- |
| OUI (uniquement avec PCSX2 1.7) | NON               |

## BIOS

<table><thead><tr><th width="196">Fichier BIOS</th><th width="113">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>SCPH30004R.bin</td><td><code>\bios</code></td><td>28922c703cc7d2cf856f177f2985b3a9</td></tr><tr><td>SCPH30004R.MEC</td><td><code>\bios</code></td><td>3faf7c064a4984f53e2ef5e80ed543bc</td></tr><tr><td>scph39001.bin</td><td><code>\bios</code></td><td>d5ce2c7d119f563ce04bc04dbc3a323e</td></tr><tr><td>scph39001.MEC</td><td><code>\bios</code></td><td>3faf7c064a4984f53e2ef5e80ed543bc</td></tr><tr><td>EROM.BIN</td><td><code>\bios</code></td><td>9a9e8ed7668e6adfc8f7766c08ab9cd0</td></tr><tr><td>rom1.bin</td><td><code>\bios</code></td><td>44552702b05697a14ccbe2ca22ee7139</td></tr><tr><td>ROM2.BIN</td><td><code>\bios</code></td><td>b406d05922dac2eaf3c2e68157b1b468</td></tr></tbody></table>

### Autres BIOS acceptés

<table><thead><tr><th width="413">Fichier BIOS</th><th width="555">Dossier</th></tr></thead><tbody><tr><td>SCPH-39004_BIOS_V7_EUR_160.BIN</td><td><code>\bios</code></td></tr><tr><td>SCPH-39001_BIOS_V7_USA_160.BIN</td><td><code>\bios</code></td></tr><tr><td>SCPH-70000_BIOS_V12_JAP_200.BIN</td><td><code>\bios</code></td></tr></tbody></table>

### Logique de détermination du BIOS

Tous les BIOS doivent exister dans le dossier `\bios` à la racine de l'installation RetroBat, il est toutefois possible de spécifier un BIOS différent du BIOS par défaut en le copiant dans le dossier `\bios\pcsx2\bios`.

## Contrôles

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans pcsx2:

* Contrôleurs XInput
* Dualshocks & DualSense
* Nintendo Switch Pro
{% endhint %}

| RetroBat                                                                           | Playstation 2           |
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

### Textures personnalisées

L'émulateur PCSX2 permet l'utilisation de packs de textures "customs" pour remplacer les textures originales du jeu.

Pour utiliser un pack de textures, placer le pack dans le dosisier `\bios\pcsx2\textures` dans un sous-dossier portant l'ID du jeu:

<div align="left">

<figure><img src="https://i.imgur.com/nOBWsbc.png" alt=""><figcaption></figcaption></figure>

</div>

Les fichiers de textures doivent être copiées dans un sous-dossier nommé "replacements":

<div align="left">

<figure><img src="https://i.imgur.com/H7dUscl.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Pour connaître l'ID du jeu, il est possible d'utiliser la méthode suivante:

démarrer l'éxecutable de l'émulateur depuis le dossier`\emulators\pcsx2` et lancer le jeu en activant l'option "dump textures", PCSX2 créera automatiquement le dossier des textures pour le jeu en question dans `\bios\pcsx2\textures`.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/hHyR18f.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/6IeWCXM.png" alt=""><figcaption></figcaption></figure>

</div>

Une fois le pack de textures placé dans le bon dossier et pour le bon ID jeu, configurer Retrobat pour lancer le jeu en utilisant les textures personnalisées avec l'option **CUSTOM TEXTURES** depuis le sous-menu **VISUAL RENDERING** dans le menu [**Configuration Avancée du Système**](../../../../navigation/view-options.md#configuration-avancees-du-systeme) ou le menu [**Configuration Avancée du Jeu**](../../../../navigation/game-options.md#configuration-avancee-du-jeu) :

<div align="left">

<figure><img src="https://i.imgur.com/yx1qPkB.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/ijtLUEf.png" alt=""><figcaption></figcaption></figure>

</div>

### Jeux multi-disques

PCSX2 ne supporte pas l'utilisation de fichiers m3u pour les jeux multi-disques.

<div align="left">

<figure><img src="https://i.imgur.com/5n2VsbQ.png" alt=""><figcaption></figcaption></figure>

</div>

Pour changer de disques dans PCSX2, il est nécessaire de procéder comme suit dans l'interface de PCSX2:

Lorsque le jeu demande de changer de disque, accéder au menu PCSX2 avec la combinaison SELECT + ![A](<../../../../.gitbook/assets/image (19).png>) de votre manette, et sélectionner "**Change Disc**"

<div align="left">

<figure><img src="https://i.imgur.com/fihyt1U.png" alt=""><figcaption></figcaption></figure>

</div>

Dans l'écran suivant, sélectionner le disque suivant et confirmer avec ![A](<../../../../.gitbook/assets/image (19).png>)

<div align="left">

<figure><img src="https://i.imgur.com/leMX1Ob.png" alt=""><figcaption></figcaption></figure>

</div>
