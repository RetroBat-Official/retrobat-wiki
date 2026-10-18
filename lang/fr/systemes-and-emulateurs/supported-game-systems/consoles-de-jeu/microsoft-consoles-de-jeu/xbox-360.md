---
description: Microsoft
---

# Xbox 360

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/xbox360.svg" alt=""><figcaption></figcaption></figure></div>

Console de jeu - Durée de vie : 2005 - 2016

{% embed url="https://fr.wikipedia.org/wiki/Xbox_360" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>xenia-canary</li><li>xenia-edge</li><li>xenia-manager</li><li>xenia</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> xbox360</td></tr><tr><td><strong>Extensions</strong></td><td>.iso .xex .xcp .zar .m3u .xbox360 .decomp</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>NON</td></tr></tbody></table>

## Bios

Pas de BIOS spécifique requis pour les jeux Xbox 360 avec les émulateurs xenia / xenia-canary.

## Contrôles

Xenia n'a pas de fonctionnalité pour configurer les contrôleurs mais offre une compatibilité native avec de nombreux modèles de contrôleurs.

Depuis les options Retrobat du système Xbox 360, sélectionner l'option correspondant à votre type de contrôleur:

* XBOX CONTROLLER pour les manettes Xbox (modèles Xbox 360 et plus récents)
* KEYBOARD pour le clavier
* AUTRE pour tous les autres types de manettes (NINTENDO, DualShocks, etc.)

## Information spécifique du système

### Emplacement des fichiers

<table><thead><tr><th width="254">Fichier(s)</th><th>Chemin (relatif au dossier RetroBat)</th></tr></thead><tbody><tr><td>Content path</td><td>saves\xbox360\xenia</td></tr></tbody></table>

### Ajout d'un jeu XBLA (Xbox Live Arcade)

Les jeux Xbox360 **XBLA** (**XB**ox **L**ive **A**rcade) se présentent sous la forme d'une succession de répertoire, qui se termine par un fichier sans extension.

A titre d'exemple pour le jeu _Banjo Tooie_, le chemin d'accès au fichier est le suivant :

**\Banjo Tooie\58410955\000D0000\ABB9CAB336175357D09F2D922735D23C62F90DDD**

Pour que Retrobat soit capable de lancer le jeu, il faut créer un fichier **\*.m3u** qui doit être placé à la racine du répertoire`\roms\xbox360`.

<div align="left"><figure><img src="https://i.imgur.com/tfzS8Rt.png" alt=""><figcaption><p>Example for Banjo Tooie</p></figcaption></figure></div>

Le contenu du fichier .m3u doit être le suivant :

```
\Banjo Tooie\58410955\000D0000\ABB9CAB336175357D09F2D922735D23C62F90DDD
```

### Utiliser Xenia Manager

Pour utiliser Xenia Manager, sélectionner "xenia-manager" comme émulateur dans les options avancées du système:

<div align="left"><figure><img src="https://i.imgur.com/3m5DSxP.png" alt=""><figcaption></figcaption></figure></div>

Lorsque xenia manager est utilisé, RetroBat va automatiquement vérifier si il existe un fichier de configuration spécifique pour le jeu, la recherche s'effectue dans le fichier "games.json" qui se situe dans le dossier `emulators\xenia-manager\Config` de l'installation RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/aT4Hy35.png" alt=""><figcaption></figcaption></figure></div>

Si le fichier de configuration existe pour le jeu, RetroBat utilisera la configuration personnalisée du jeu plutôt que les options définies dans l'interface RetroBat.
