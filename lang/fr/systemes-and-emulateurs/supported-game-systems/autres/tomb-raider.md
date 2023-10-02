---
description: OpenLara
---

# Tomb Raider

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/55ff14aa79c95ecc70133072e6ac19fed3555b56/art/logos/openlara.svg" alt="" width="375"><figcaption></figcaption></figure>

</div>

Moteur de jeu permettant de jouer à Tomb Raider.

{% embed url="https://docs.libretro.com/library/openlara/" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>Libretro : openlara</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> openlara</td></tr><tr><td><strong>Extensions</strong></td><td>.croft</td></tr><tr><td><strong>Group</strong></td><td>ports</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

| Retrobat                                       | OpenLara                  |
| ---------------------------------------------- | ------------------------- |
| START                                          | START                     |
| SELECT                                         | Inventaire                |
| D-PAD                                          | D-PAD                     |
| Left analog stick                              |                           |
| Right analog stick                             |                           |
| ![](<../../../.gitbook/assets/image (32).png>) | Sauter                    |
| ![](<../../../.gitbook/assets/image (19).png>) | Action : tirer / attraper |
| ![](<../../../.gitbook/assets/image (6).png>)  | Rouler                    |
| ![](<../../../.gitbook/assets/image (34).png>) | Sortir arme               |
| L1                                             |                           |
| R1                                             | Marcher (garder enfoncé)  |
| L2                                             | S'accroupir               |
| R2                                             | Sprinter                  |

## Information spécifique au système

### Fichiers de jeux

Créer un fichier .croft dans le dossier `roms\openlara` de l'installation RetroBat.

Dans ce fichier, renseigner le chemin vers le fichier à lancer, les fichiers suivants sont acceptés par le core OpenLara : **.phd, .psx, .phd**

Par exemple le fichier ci-dessous lancera le niveau "gym" de Tomb Raider 1:

<div align="left">

<figure><img src="https://i.imgur.com/yRgQBth.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Une fois un niveau lancé, il est possible de revenir au menu du jeu Tomb Raider pour démarrer le jeu.
{% endhint %}

### Organisation du dossier de jeu

{% hint style="info" %}
Seul Tomb Raider 1 est supporté actuellement.
{% endhint %}

Voici un exemple d'une structure de fichier fonctionnelle:

```
└── roms\
    └── openlara\
        └── *.croft
        └── Tomb Raider\
               └── audio\
               │      └── 1\
               │           └── XXX.ogg ou track_XX.ogg
               │      └── 2\
               │           └── track_XX.ogg et MAIN.SFX
               │      └── 3\
               │           └── track_XX.ogg et MAIN.SFX
               └── level\
               |      └── 1\
               |           └── *.PNG et *.PHD ou *.PSX ou *.SAT
               │      └── 2\
               │           └── *.PNG et *.TR2 ou *.PSX
               │      └── 3\
               │           └── *.PNG et *.TR2 ou *.PSX
               └── video\
                      └── 1\
                           └── *.RPL ou *.FMV
                      └── 2\
                           └── *.RPL ou *.FMV
                      └── 3\
                           └── *.RPL ou *.FMV
```
