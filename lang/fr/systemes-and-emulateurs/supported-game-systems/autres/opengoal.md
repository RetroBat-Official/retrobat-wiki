# OpenGOAL

<div align="left"><figure><img src="https://github.com/fabricecaruso/es-theme-carbon/blob/master/art/logos/opengoal.png?raw=true" alt=""><figcaption></figcaption></figure></div>

Moteur de jeu Jak\&Daxter 1, 2 et 3.

{% embed url="https://opengoal.dev/" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulateur</strong></td><td><ul><li>opengoal</li></ul></td></tr><tr><td><strong>Dossier de jeu</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> opengoal</td></tr><tr><td><strong>Extensions</strong></td><td>.opengoal</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

A configurer dans le jeu.

## Information spécifique au système

### Installer le jeu dans l'émulateur

OpenGOAL nécessite un dump du jeu original PS2 au format .iso, celui-ci doit être extrait dans le dossier de l'émulateur à l'aide de l'extracteur inclu.

#### Étape 1 : télécharger l'émulateur

Télécharger la dernière version depuis le lien ci-dessous:

{% embed url="https://github.com/open-goal/jak-project/releases" %}

Choisir la version windows : `opengoal-windows-vX.X.X.zip`

#### Étape 2 : extraire les fichiers de l'émulateur

Extraire les fichiers de l'émulateur précédemment téléchargé dans le dossier `\emulators\opengoal` de votre installation RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/piA0EnZ.png" alt=""><figcaption></figcaption></figure></div>

#### **Étape 3 : Extraire les fichiers de jeu**

C'est là que ça se complique : vous devez lancer l'extractor à l'aide d'une commande.

* Créez un fichier texte dans le même dossier que le fichier extractor.exe, nommez-le « jakExtract.txt ».
* Dans le fichier, renseigner:

```
start extractor -g JEU "CHEMIN-VERS-GAME-ISO"
```

Remplacer JEU par jak1, jak2 ou jak3, selon le jeu à extraire.

Remplacer CHEMIN-VERS-GAME-ISO par le chemin complet vers le fichier iso à extraire.

Exemple:

```
start extractor -g jak2 "C:\retrobat\roms\ps2\Jak2.iso"
```

* Changer l'extension du fichier de .txt à .bat

Enfin, lancer le fichier .bat pour extraire automatiquement le jeu afin de permettre son lancement avec OpenGOAL (le processus d'extraction peut prendre plusieurs minutes).

#### **Étape 4 :** Créer le fichier de lancement pour RetroBat

Créer un fichier .txt dans le dossier `\roms\opengoal` de votre dossier RetroBat et renseigner le nom du jeu à lancer:

* `jak1` pour jak and Daxter 1
* `jak2` pour jak and Daxter 2
* `jak3` pour jak and Daxter 3

<div align="left"><figure><img src="https://i.imgur.com/mGUXHzk.png" alt=""><figcaption></figcaption></figure></div>

Sauvegarder le(s) fichier(s) avec l'extension "**.opengoal".**
