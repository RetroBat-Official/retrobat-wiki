# Zinc



<div align="left">

<figure><img src="https://github.com/fabricecaruso/es-theme-carbon/blob/master/art/logos/zinc.png?raw=true" alt=""><figcaption></figcaption></figure>

</div>

Emulateur des systèmes arcade Playstation.

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>PSXMame</li><li>zinc</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span>zinc</td></tr><tr><td><strong>Extensions</strong></td><td>.zip</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>OUI</td></tr></tbody></table>

## Bios

Pas de BIOS requis.

## Contrôles

## Contrôles - PSXMame

<table><thead><tr><th width="266">Retrobat</th><th>PSXMame</th></tr></thead><tbody><tr><td>START</td><td>Start</td></tr><tr><td>SELECT</td><td>Select / COIN</td></tr><tr><td>D-PAD</td><td>D-PAD</td></tr><tr><td>Stick analogique gauche</td><td>Joystick gauche</td></tr><tr><td>Stick analogique droit</td><td>Joystick droit</td></tr><tr><td><img src="../../../.gitbook/assets/image (32).png" alt=""></td><td>Bouton 4</td></tr><tr><td><img src="../../../.gitbook/assets/image (19).png" alt=""></td><td>Bouton 1</td></tr><tr><td><img src="../../../.gitbook/assets/image (6).png" alt=""></td><td>Bouton 2</td></tr><tr><td><img src="../../../.gitbook/assets/image (34).png" alt=""></td><td>Bouton 3</td></tr><tr><td>L1</td><td>Bouton 5</td></tr><tr><td>R1</td><td>Bouton 6</td></tr><tr><td>L2</td><td></td></tr><tr><td>R2</td><td></td></tr><tr><td>L3 + R3</td><td>Menu Service (joueur 1)</td></tr></tbody></table>

## Contrôles - ZINC

Il existe 2 possibilités pour la configuration des contrôleurs ZINC.

### Configuration automatique

Pour activer la configuration automatique, sélectionner l'option "DYNAMIQUE" dans les options avancées du système (section CONTRÔLES).

3 profils sont disponibles :

* Street Fighter
* Soul Edge
* Tekken

### Configuration à l'aide de fichiers prédéfinis

Pour activer la configuration depuis un fichier personnalisé, sélectionner l'option "FICHIER PREDEFINI" dans les options avancées du système (section CONTRÔLES).

Il est possible d'utiliser un profil de contrôleur pour chaque jeu, pour cela, modifier le fichier .cfg du jeu (ou en créer un si il n'existe pas) qui se trouve dans le dossier `\emulators\zinc\cfg`, et nommer le de sorte à ce que le nom du fichier commence par l'ID du jeu.

RetroBat sélectionne automatiquement le premier fichier présent et commençant par l'ID du jeu.



{% hint style="danger" %}
L'émulateur zinc ne supporte pas le pad directionnel, les mouvements s'effectuent à l'aide du stick gauche de la manette.
{% endhint %}

## Informations spécifiques au système

### ROMs

{% hint style="danger" %}
PSXMame et Zincn'utilisent pas le même ROMset, les jeux fonctionnant dans un émulateur ne fonctionnent pas dans l'autre.
{% endhint %}

La liste des jeux compatibles est disponible [ICI](https://emulation.gametechwiki.com/index.php/ZiNc).

Les fichiers de jeu (.zip) ne doivent être ni dézippés, ni renommés.

Certains jeux nécessitent des fichiers CHD, ils doivent être placés dans un sous-dossier du dossier des roms et nommés comme le fichier zip du jeu:

<div align="left">

<figure><img src="https://i.imgur.com/w68hUHc.png" alt=""><figcaption></figcaption></figure>

</div>
