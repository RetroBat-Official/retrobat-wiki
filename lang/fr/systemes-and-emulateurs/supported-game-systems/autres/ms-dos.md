---
description: Microsoft
---

# DOS

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/pc.svg" alt=""><figcaption></figcaption></figure>

</div>

Système d'exploitation - Durée de vie : 1981 - 2000

{% embed url="https://fr.wikipedia.org/wiki/MS-DOS" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>Libretro : dosbox_pure</li><li>dosbox</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> dos</td></tr><tr><td><strong>Extensions</strong></td><td>.dosbox .pc .dos .dosz .zip .m3u8 .bat .cmd</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

Les jeux DOS utilisent une souris et un clavier.&#x20;

La fonctionnalité [pad2key ](../../../controleurs/pad2key.md)permet l'utilisation d'une manette.

Il est possible que dans certains jeux des notifications apparaissent, demandant d'appuyer sur des boutons d'une manette (il existait une manette officielle destinée à être branchée sur le port série de l'ordinateur), si c'est le cas, utiliser la correspondance suivante :

Bleu = ![North button (X SNES)](https://wiki.batocera.org/\_media/wiki:north.png?w=20\&tok=be3bd1), Rouge = ![West button (Y SNES)](https://wiki.batocera.org/\_media/wiki:west.png?w=20\&tok=aee81f), Jaune = ![South button (B SNES)](https://wiki.batocera.org/\_media/wiki:south.png?w=20\&tok=c3eef3) Vert= ![East button (A SNES)](https://wiki.batocera.org/\_media/wiki:east.png?w=20\&tok=2276b1).

## Information spécifique au système

### Jeux au format zip

DOSBox peut charger des fichiers directement depuis une archive **ZIP** sans extraction préalable.

### Démarrer un jeu

Le premier écran affiché lors du lancement d'un jeu avec DOSBOX permet de sélectionner l'exécutable à utiliser pour lancer le jeu. Cet écran est navigable avec une manette. Il est possible de définir un exécutable par défaut en appuyant sur la croix directionnel DROITE, permettant ainsi d'éviter cet écran lors de la prochaine exécution du jeu.

<div align="left">

<figure><img src="https://i.imgur.com/Ykgv1UU.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Si le jeu ne contient qu'un seul exécutable cet écran n'apparaîtra pas.
{% endhint %}

### Monter un jeu sur les lecteurs A ou D <a href="#mount-zip-as-a-or-d-drive" id="mount-zip-as-a-or-d-drive"></a>

Certains jeux nécessitent d'être montés sur un lecteur de disquette (A:) ou un lecteur cd-rom (D), pour cela renommer le fichier `.ZIP` en `.D.ZIP` ou .`A.ZIP` (pour utiliser respectivement les lecteurs D ou A).

### Multi-disque

Utiliser un fichier `.m3u8`.
