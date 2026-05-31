---
description: Amstrad
---

# Amstrad CPC

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/amstradcpc-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/amstradcpc.svg" alt=""></picture><figcaption></figcaption></figure></div>

Micro-ordinateurs - durée de vie : 1984 - 1990

{% embed url="https://fr.wikipedia.org/wiki/Amstrad_CPC" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro : cap32</li><li>libretro : crocods</li><li>capriceforever</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> amstradcpc</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.dsk .sna .tap .cdt .voc .m3u .zip .7z</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-cap32 : OUI<br>lr-crocods : NON<br>capriceforever : NON</td><td>lr-cap32 : OUI<br>lr-crocods : OUI<br>capriceforever : NON</td><td>lr-cap32 : OUI<br>lr-crocods : OUI<br>capriceforever : OUI</td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire.

## Contrôles

Les cores crocods et cap32 permettent de sélectionner les types de contrôleurs suivants:

* JOYSTICK
* KEYBOARD (utiliser la fonction Game Focus en complément)
* LIGHTGUN (cap32 uniquement)

| Retrobat                                              | Amstrad CPC  |
| ----------------------------------------------------- | ------------ |
| START                                                 | RETURN       |
| SELECT                                                | SPARE        |
| D-PAD                                                 | D-PAD        |
| Stick analogique gauche                               | D-PAD        |
| Stick analogique droit                                |              |
| ![](<../../../.gitbook/assets/image (33).png>)        |              |
| ![](<../../../.gitbook/assets/image (20) (1).png>)    | Fire 2       |
| ![](<../../../.gitbook/assets/image (7) (1) (1).png>) | Fire 1       |
| ![](<../../../.gitbook/assets/image (35).png>)        |              |
| L1                                                    | cap32: CTRL  |
| R1                                                    | cap32: INTRO |
| L2                                                    | cap32: F1    |
| R2                                                    | cap32: F2    |
| L3                                                    |              |
| R3                                                    |              |

### Remplacement de la configuration Libretro-Cap32

RetroBat permet d'automatiser le remap des touches pour libretro-Cap32 à partir d'un fichier JSON.

Le fichier JSON est situé dans le dossier `system\resources\inputmapping` de votre installation RetroBat et est nommé **libretro\_cap32.json.**

A l’intérieur de ce fichier, il est possible de forcer une configuration de touches spécifique par jeu, qui sera automatiquement identifié par RetroBat en fonction des noms de fichiers répertoriés dans la section « Roms » du fichier JSON, ou grâce à la normalisation du nom de fichier et de la valeur « Name » du fichier JSON :\
\
![](<../../../.gitbook/assets/image (7) (1).png>)

Dans l'exemple ci-dessus, si le jeu BombJack est lancé depuis RetroBat, les boutons L2, R2 et Select de la manette seront automatiquement assignés aux touches 1, 2 et J du clavier:

<div align="left"><figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
N'hesitez pas à partager votre propre fichier de reconfiguration avec la team RetroBat.

Au cas ou vous mettez a jour ce fichier avec vos propres réglages, placez votre version du fichier dans le répertoire <kbd>user\inputmapping</kbd> de votre installation RetroBat, sino il sera écrasé à la mise a jour suivante.
{% endhint %}

### Clavier virtuel

**cap32** : Preser START + ![](<../../../.gitbook/assets/image (33).png>) pour afficher le clavier virtuel.

## Information spécifique au système

### Forcer des arguments de ligne de commande pour Cap32

Le core Cap32 possède une fonctionnalité "autorun" qui permet d'entrer automatiquement des arguments de ligne de commande lors du démarrage. Il est toutefois possible, dans certains cas, que la mauvaise ligne de commande soit envoyée par le core.&#x20;

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
