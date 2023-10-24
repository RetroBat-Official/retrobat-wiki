---
description: Amstrad
---

# Amstrad CPC

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/amstradcpc-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/amstradcpc.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Micro-ordinateurs - durée de vie : 1984 - 1990

{% embed url="https://fr.wikipedia.org/wiki/Amstrad_CPC" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro : cap32</li><li>libretro : crocods</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> amstradcpc</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.dsk .sna .tap .cdt .voc .m3u .zip .7z</td><td></td></tr></tbody></table>

## Fonctionnalités

| Succès Rétro | Parties en Réseau |
| ------------ | ----------------- |
| OUI          | OUI               |

## BIOS

Aucun BIOS nécessaire.

## Contrôles

Les cores crocods et cap32 permettent de sélectionner les types de contrôleurs suivants:

* JOYSTICK
* KEYBOARD (utiliser la fonction Game Focus en complément)
* LIGHTGUN (cap32 uniquement)

| Retrobat                                       | Amstrad CPC  |
| ---------------------------------------------- | ------------ |
| START                                          | RETURN       |
| SELECT                                         | SPARE        |
| D-PAD                                          | D-PAD        |
| Stick analogique gauche                        | D-PAD        |
| Stick analogique droit                         |              |
| ![](<../../../.gitbook/assets/image (32).png>) |              |
| ![](<../../../.gitbook/assets/image (19).png>) | Fire 2       |
| ![](<../../../.gitbook/assets/image (6).png>)  | Fire 1       |
| ![](<../../../.gitbook/assets/image (34).png>) |              |
| L1                                             | cap32: CTRL  |
| R1                                             | cap32: INTRO |
| L2                                             | cap32: F1    |
| R2                                             | cap32: F2    |
| L3                                             |              |
| R3                                             |              |

## Information spécifique au système

### Modifier la ligne de commande pour Cap32

Le core Cap32 possède une fonctionnalité "autorun" qui permet d'entrer automatiquement la ligne de commande de lancement du jeu lors du démarrage. Il est toutefois possible, dans certains cas, que la mauvaise ligne de commande soit envoyée par le core.&#x20;

Pour palier ce problème, il est possible de forcer l'utilisation d'une ligne de commande spécifique dans un fichier m3u:

* Créer un fichier .m3u, avec à l'intérieur \
  \- la ligne de commande a exécuter\
  \- le nom du fichier

**Exemple** :

```
#COMMAND:RUN"COMMANDO.BIN
Commando (Europe).dsk
```

Dans cet exemple, RetroBat va demander à l'émulateur de lancer le jeu nommé "Commando (Europe).dsk" puis de taper la ligne de commande `RUN"COMMANDO.BIN`

Démarrez ensuite a partir du fichier .m3u en sélectionnant le core Cap32
