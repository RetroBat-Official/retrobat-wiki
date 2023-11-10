---
description: Boom3
---

# Doom III

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/f55c99c10d6ab0fc36ebe3d33576050178c66501/art/logos/boom3-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/f55c99c10d6ab0fc36ebe3d33576050178c66501/art/logos/boom3.svg" alt="" width="375"></picture><figcaption></figcaption></figure>

</div>

Moteur de jeu permettant de jouer à Doom 3 et son extension Resurrection of Evil.

{% embed url="https://docs.libretro.com/library/boom3/" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>Libretro: boom3</li><li>Libretro: boom3_xp</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> boom3</td></tr><tr><td><strong>Extensions</strong></td><td>.boom3</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire

## Contrôles

boom3 permet de sélectionner 2 schémas de contrôles, accessibles depuis le menu RetroBat.

| Retrobat                                       | Classic                     | Modern                                                      |
| ---------------------------------------------- | --------------------------- | ----------------------------------------------------------- |
| START                                          | Afficher / masquer le menu  | Afficher / masquer le menu                                  |
| SELECT                                         | Afficher / masquer la carte | Afficher / masquer la carte                                 |
| D-PAD                                          | D-PAD                       | D-PAD                                                       |
| Left analog stick                              |                             | <p>X-axe: déplacement latéral<br>Y-axe: Avancer/reculer</p> |
| Right analog stick                             |                             | X-axe: regarder à gauche et droite                          |
| ![](<../../../.gitbook/assets/image (32).png>) | Courir                      | Sauvegarde rapide                                           |
| ![](<../../../.gitbook/assets/image (19).png>) | Utiliser                    | Menu : annuler                                              |
| ![](<../../../.gitbook/assets/image (6).png>)  | Tirer                       | Menu : sélectionner                                         |
| ![](<../../../.gitbook/assets/image (34).png>) | Mitrailler                  | Chargement rapide                                           |
| L1                                             | Mitrailler à gauche         | Arme précédente                                             |
| R1                                             | Mitrailler à droite         | Arme suivante                                               |
| L2                                             | Arme précédente             | Utiliser                                                    |
| R2                                             | Arme suivante               | Tirer                                                       |
| L3                                             |                             | Courir                                                      |
| R3                                             |                             | Se retourner (180°)                                         |

## Information spécifique au système

### Organisation des fichiers de jeux

Boom3 nécessite la présence d'un fichier avec l'extension .boom3 dans le répertoire `roms\boom3` de l'installation RetroBat.

Le fichier .boom3 doit être un fichier texte dont l'extension aura été modifié. Le contenu du fichier doit être le chemin relatif vers le fichier pak000.pk4 du jeu original ou de l'extension:

<div align="left">

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FexdzL60ZuqPLldz2AYta%2Fuploads%2FP31aMYrLpmnCQ2eJozzc%2Fimage.png?alt=media&#x26;token=a290eee5-756f-49f4-be6d-f9bef7de1b27" alt=""><figcaption></figcaption></figure>

</div>

Boom3 nécessite les fichiers .pk4 originaux issus du jeu Doom3 et de son extension Resurrection of Evil. Vous aurez besoin des données de jeu d'une installation de Doom3 patché en version 1.3.1, spécifiquement des fichiers .pk4 suivants (le dossier _base_ contient les données du jeu standard, le dossier _d3xp_ contient les données de jeu de l'extension Resurrection of Evil):

```
└── roms/
    └── boom3/
        ├── Doom 3.boom3
        ├── Doom 3 - Resurrection of evil.boom3
        ├── base/
        │   ├── pak000.pk4
        │   ├── pak001.pk4
        │   ├── pak002.pk4
        │   ├── pak003.pk4
        │   ├── pak004.pk4
        │   ├── pak005.pk4
        │   ├── pak006.pk4
        │   ├── pak007.pk4
        │   └── pak008.pk4
        └── d3xp/
            ├── pak000.pk4 
            └── pak001.pk4
```
