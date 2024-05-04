---
description: Nintendo
---

# Nintendo 3DS

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/3ds-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/3ds.svg" alt="" width="563"></picture><figcaption></figcaption></figure>

</div>

Console de jeu portable - Durée de vie : 2011 - 2020

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_3DS" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro : citra</li><li>lime3ds</li><li>citra</li><li>citra-canary</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> 3ds</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.3ds .3dsx .elf .axf .cci .cxi .app .3DS .3DSX .ELF .AXF .CCI .CXI .APP</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>lr-citra : OUI<br>Lime3DS: OUI<br>Citra (&#x26;canary) : OUI</td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire.

## Contrôles

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans limes3ds/citra standalone:

* Contrôleurs XInput
* Dualshocks & DualSense
* Nintendo Switch Pro
{% endhint %}

{% hint style="info" %}
L'écran tactile de la 3DS est difficilement émulable, la meilleure solution est de connecter une souris.

Le core libretro peut simuler l'utilisation du touchscreen avec le stick droit de la manette, mais le mouvement n'est pas optimisé.
{% endhint %}

| RetroBat                                                                           | 3DS                    |
| ---------------------------------------------------------------------------------- | ---------------------- |
| START                                                                              | START                  |
| SELECT                                                                             | SELECT                 |
| D-PAD                                                                              | D-PAD                  |
| Stick analogique gauche                                                            | Stick gauche           |
| Stick analogique droit                                                             | touchscreen ou c-stick |
| ![A](<../../../../.gitbook/assets/image (19).png>)                                 | B                      |
| ![B](<../../../../.gitbook/assets/image (6).png>)                                  | A                      |
| <img src="../../../../.gitbook/assets/image (34).png" alt="" data-size="original"> | X                      |
| <img src="../../../../.gitbook/assets/image (32).png" alt="" data-size="line">     | Y                      |
| L1                                                                                 | L                      |
| R1                                                                                 | R                      |
| L2                                                                                 | ZL                     |
| R2                                                                                 | ZR                     |
| L3                                                                                 | Home                   |
| R3                                                                                 | Clic sur le curseur    |
| SOURIS                                                                             | Touch Screen et appui  |

## Information spécifique au système

### Textures personnalisées

Les émulateurs Lime3DS et Citra permet l'utilisation de packs de textures personnalisés.

Les textures doivent être copiées dans le dossier `\emulators\`<mark style="color:purple;">`<émulateur>`</mark>`\User\Load\Textures\<gameID>`, par exemple pour le jeu Super Mario 3D Land:

<div align="left">

<figure><img src="https://i.imgur.com/6dLxUWC.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Pour le core libretro, les textures sont à positionner dans le dossier:

`\saves\3ds\citra\Load\Textures\<gameID>`
{% endhint %}

Le nom du dossier dans lequel il faut copier les textures peut être retrouvé en effectuant un clic-droit sur le jeu dans l'interface de l'émulateur, puis en sélectionnant l'option "Ouvrir l'emplacement personnalisé des textures".

<div align="left">

<figure><img src="https://i.imgur.com/kT4RLmY.png" alt=""><figcaption></figcaption></figure>

</div>

Une fois le pack de textures correctement copié, activer les textures personnalisées dans RetroBat:

<div align="left">

<figure><img src="https://i.imgur.com/HMiSQ1r.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/6OUlief.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/89Ed74U.png" alt=""><figcaption></figcaption></figure>

</div>
