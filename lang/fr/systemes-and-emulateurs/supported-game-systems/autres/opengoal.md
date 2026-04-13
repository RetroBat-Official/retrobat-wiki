# OpenGOAL

<div align="left"><figure><img src="https://github.com/fabricecaruso/es-theme-carbon/blob/master/art/logos/opengoal.png?raw=true" alt=""><figcaption></figcaption></figure></div>

Moteur de jeu Jak & Daxter 1 et 2

{% embed url="https://opengoal.dev/" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>opengoal</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> opengoal</td></tr><tr><td><strong>Extension</strong></td><td>.opengoal</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

A configurer dans le jeu.

## Information spécifique au système

### Installer le jeu dans l'émulateur

OpenGOAL nécessite un dump du jeu original PS2 au format .iso, celui-ci doit être extrait dans le dossier de l'émulateur à l'aide de l'extracteur inclu.

#### Etape 1: télécharger l'émulateur

Télécharger la dernière version depuis le lien ci-dessous:

{% embed url="https://github.com/open-goal/jak-project/releases" %}

Choisir la version windows : `opengoal-windows-vX.X.X.zip`

#### Etape 2: extraire les fichiers de l'émulateur

Extraire les fichiers de l'émulateur précédemment téléchargé dans le dossier `\emulators\opengoal` de votre installation RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/piA0EnZ.png" alt=""><figcaption></figcaption></figure></div>

#### **Etape 3 : Extraire les fichiers de jeu**

C'est la partie compliquée, il est nécessaire de lancer une ligne de commande pour décompiler le jeu:

* Créer un fichier texte dans le même dossier que le fichier "extractor.exe" et le nommer: "jakExtract.txt"
* Dans le fichier texte, renseigner la ligne suivante:

```
start extractor -g GAME "PATH-TO-GAME-ISO"
```

Remplacer GAME par jak1, jak2 ou jak3 selon le jeu à décompiler.

Remplacer PATH-TO-GAME-ISO avec le chemin complet vers l'ISO du jeu à décompiler.

Example:

```
start gk -g jak2 "C:\retrobat\roms\ps2\Jak2.iso"
```

* Modifier l'extension du fichier par .bat

Lancer le fichier .bat pour début l'extraction de l'ISO du jeu afin de permettre le lancement d'OpenGOAL (l'extraction prend plusieurs minutes).

**Etape 4 : Créer le fichier dans le dossier roms\opengoal**

Créer un fichier .txt vide dans le dossier \roms\opengoal de votre installation RetroBat et écrire le nom du jeu dans le fichier:

* `jak1` pour jak and Daxter 1
* `jak2` pour jak and Daxter 2

<div align="left"><figure><img src="https://i.imgur.com/mGUXHzk.png" alt=""><figcaption></figcaption></figure></div>

Sauvegarder le(s) fichier(s) avec l'extension "**.opengoal".**
