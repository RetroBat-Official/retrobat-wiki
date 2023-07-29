---
description: Microsoft
---

# Xbox

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/xbox.svg" alt=""><figcaption></figcaption></figure>

</div>

Console de jeu - Durée de vie : 2001 - 2006

{% embed url="https://fr.wikipedia.org/wiki/Xbox" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>xemu</li><li>cxbx</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> xbox</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.xbe .iso</td><td></td></tr></tbody></table>

{% hint style="info" %}
les fichiers .iso doivent être au format xiso.
{% endhint %}

{% hint style="danger" %}
CXBX nécessite "dokan" afin de pouvoir monter les images .iso.

Vous pouvez télécharger dokan ici:\
[https://github.com/dokan-dev/dokany/releases](https://github.com/dokan-dev/dokany/releases)
{% endhint %}

## Fonctionnalités

| Succès Rétro | Parties en Réseau |
| ------------ | ----------------- |
| NON          | NON               |

## BIOS

<table><thead><tr><th width="196">Fichier BIOS</th><th width="162">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>mcpx_1.0.bin</td><td><code>\bios</code></td><td>d49c52a4102f6df7bcf8d0617ac475ed</td></tr><tr><td>Complex_4627.bin</td><td><code>\bios</code></td><td>39cee882148a87f93cb440b99dde3ceb</td></tr><tr><td>xbox_hdd.qcow2</td><td><code>\saves\xbox</code></td><td></td></tr></tbody></table>

## Contrôles

| RetroBat                                                                           | Xbox                           |
| ---------------------------------------------------------------------------------- | ------------------------------ |
| START                                                                              | START                          |
| SELECT / BACK                                                                      | Back                           |
| D-PAD                                                                              | D-PAD                          |
| Stick analogique gauche                                                            | Stick analogique gauche        |
| Stick analogique droit                                                             | Stick analogique droit         |
| ![A](<../../../../.gitbook/assets/image (19).png>)                                 | A                              |
| ![B](<../../../../.gitbook/assets/image (6).png>)                                  | B                              |
| <img src="../../../../.gitbook/assets/image (34).png" alt="" data-size="original"> | Y                              |
| <img src="../../../../.gitbook/assets/image (32).png" alt="" data-size="line">     | X                              |
| L1                                                                                 | L1 (blanc)                     |
| R1                                                                                 | R1 (noir)                      |
| L2                                                                                 | LT                             |
| R2                                                                                 | RT                             |
| L3                                                                                 | Bouton du stick gauche (thumb) |
| R3                                                                                 | Bouton du stick droit (thumb)  |

## Information spécifique du système

### Problème de langue en jeu

Si vos jeux sont tous en allemand ou en anglais, il est possible que ce soit lié au fait que votre fichier eeprom n'est pas défini sur la bonne langue. L'émulateur utilise le langage inscrit dans le fichier eeprom.

Il est recommandé de définir correctement la langue sur votre Xbox originale et ensuite d'extraire à nouveau le BIOS.&#x20;

Une autre solution consiste à éditer le fichier eeprom situé dans le répertoire `/saves/xbox/` du dossier Retrobat avec l'outil disponible [ici (Original Xbox EEPROM Editor crée par Ernegien)](https://github.com/Ernegien/XboxEepromEditor) pour changer les réglages de l'eeprom Xbox.
