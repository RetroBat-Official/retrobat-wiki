# Structure du répertoire RetroBat

Une fois RetroBat installé, le répertoire contient les dossiers et fichiers suivants  :

<div align="left"><figure><img src="https://i.imgur.com/12l87Hk.png" alt=""><figcaption></figcaption></figure></div>

## Répertoire "bios"&#x20;

Ce répertoire est celui où doivent être placés (à de rares exceptions près) les bios et firmware de tous les systèmes.

Vous trouverez plus de précisions sur les fichiers de bios sur chaque [page individuelle de système](https://wiki.retrobat.org/v/francais/systemes-and-emulateurs/supported-game-systems).&#x20;

## Répertoire "cheats"

Ce répertoire est celui destiné à recevoir les fichiers de triche "cheats" pour les émulateurs compatibles. Les cheats peuvent être utilisés en activant l'option "ENABLE CHEATS" des émulateurs compatibles.

## Répertoire "decorations"

Ce répertoire est vide par défaut. Il permet de stocker des fichiers "décorations" (bezels) qui pourront être utilisés ensuite par RetroBat, en supplément des décorations fournies par défaut dans le dossier `system\decorations`.

## Répertoire "emulationstation"

Ce répertoire contient les principaux exécutables utilisés par l'interface EmulationStation de RetroBat ainsi que l'exécutable utilisé pour lancer les émulateurs. La structure est la suivante:

<div align="left"><figure><img src="https://i.imgur.com/vAXEckR.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Les fichiers de configuration de RetroBat (es\_systems.cfg, es\_input.cfg, ...) ainsi que les logs se trouvent dans ce dossier et ses sous-dossiers.
{% endhint %}

### Dossier ".emulationstation"

#### collections

Dans le sous-dossier "collections" vous trouverez les fichiers stockés par ES lorsque vous créez une [collection éditable](https://wiki.retrobat.org/v/francais/navigation/game-collections#collections-editables). Ces fichiers, nommés à l'identique des collection avec l'extension `.cfg`, contiennent la liste des différents jeux composant chaque collection ainsi que leur emplacement.

#### music

RetroBat permet l'utilisation de fichier audio aux formats `.mp3` ,`.ogg` ,`.wav` et `.flac`, ainsi que d'autres formats audio.\
Une musique peut être changée en appuyant sur le stick gauche de la manette `[L3]`, ou depuis le menu d'Accès Rapide. \
Lors de la navigation dans la vue système, un appui sur la touche `[SELECT]` de votre manette ouvre le menu d'Accès Rapide, où il est possible de choisir l'option **PASSER A LA MUSIQUE SUIVANTE**.

<figure><img src="https://i.imgur.com/EzBUwvn.png" alt=""><figcaption></figcaption></figure>

Les fichiers audios ajoutés dans le dossier /music seront joués de façon aléatoire.

Il est également possible d'utiliser un dossier par système, de façon à jouer une musique spécifique lors de la navigation d'un système en particulier. Pour cela, il est nécessaire de créer un sous-dossier, nommé exactement comme le dossier de la rom correspondant au système (que vous pouvez retrouver dans le fichier `es-systems.cfg`), et mettre les fichiers audios dedans.

NB : en activant l'option "JOUER SEULEMENT LES MUSIQUES PAR SYSTÈMES", RetroBat jouera toutes les musiques situées dans le sous-dossier du système dans lequel vous naviguez (par exemple /music/3do/), mais pas les musiques situées dans les autres sous-dossiers.

Les fichiers présents dans le dossier /music/ seront joués aléatoirement pour n'importe quel système (que vous ayez activé ou non l'option de musique par système).

Si vous désactivez l'option "JOUER SEULEMENT LES MUSIQUES PAR SYSTÈMES", RetroBat jouera aléatoirement les musiques situées dans le répertoire /music/ mais également dans chacun de ses sous-dossiers.

<figure><img src="https://i.imgur.com/PM1IiXI.png" alt=""><figcaption></figcaption></figure>

#### scripts

EmulationStation supporte l'utilisation de scripts externes et d'exécutable pour le lancement de programmes ou d'actions spécifiques, selon certains évènements.

#### themes

Les thèmes téléchargés via le menu TÉLÉCHARGEMENT DE CONTENU seront stockés dans ce répertoire. Vous pouvez également en placer manuellement ici.

#### themesettings

Ici vous trouverez les réglages des thèmes. Lorsqu'un thème est sélectionné, et que des modifications sont appliqués à celui-ci via le menu de thème, les réglages sont sauvegardés à l'intérieur de ce dossier, nommé à l'identique du thème avec l'extension `.cfg`.

#### video

Dans ce dossier vous pouvez placer des vidéos qui pourront être utilisés comme intro (ou "vidéo de démarrage"), avant que RetroBat ne se lance.\
Vous pouvez utiliser [BatGui](https://wiki.retrobat.org/v/francais/utilisation-avancee/batgui#gerer-le-fichier-retrobat.ini) pour configurer ces vidéos d'intro facilement.



## Répertoire "emulators"

Dans ce répertoire se trouvent tous les émulateurs utilisés.

Retroarch est fourni par défaut lors de l'installation de RetroBat. Pour tous les autres émulateurs, ils seront téléchargés quand vous en aurez besoin, en lançant un jeu utilisant cet émulateur, ou en lançant celui-ci directement depuis le menu système RetroBat.

{% hint style="info" %}
Certains émulateurs ne sont pas fournis automatiquement par Retrobat.&#x20;

Les émulateurs suivants doivent être téléchargés par vos soins et placés dans les dossiers correspondants :

* Yuzu (& early-access)
* Ryujinx
* PICO-8
* 3DSen
* TeknoParrot
{% endhint %}

## Répertoire "library"

Ce répertoire peut être utilisé pour y placer des revues digitales, qui apparaîtront dans le système "Library" et pourront être consultés avec Retrobat en utilisant le core libretro **imageviewer**.

## Répertoire "records"

Ce répertoire est le répertoire de destination pour l'enregistrement des vidéos de gameplay générés par certains utilisateurs quand la fonction "enregistrement" est activée.

## Répertoire "roms"

Il s'agit du répertoire où les roms de jeux devront être copiés, chaque jeu devant être mis dans le sous-dossier du système correct correspondant au jeu, et possédant une extension acceptée par l'émulateur de ce système.

Vous trouverez plus de précisions sur les extensions acceptées sur chaque [page individuelle de système](https://wiki.retrobat.org/v/francais/systemes-and-emulateurs/supported-game-systems).&#x20;

## Répertoire "saves"

Ce répertoire contient les sauvegardes de jeu, également si vous utilisez la fonctionnalité de sauvegarde en jeu issu de l'émulateur pour enregistrer votre progression.

## Répertoire "screenshots"

Ce répertoire contient toutes les captures d'écran prises durant la session de jeu.

{% hint style="info" %}
Si vous constatez qu'une sauvegarde ou une capture d'écran ne s'enregistre pas dans le bon répertoire, merci de prendre contact avec la team RetroBat qui fera le nécessaire pour corriger au plus vite.
{% endhint %}

## Répertoire "sounds"

Ce répertoire est utilisé pour y stocker les sons qui pourront être utilisés pour le déblocage des RetroAchievements, les fichiers présents dans ce dossier sont automatiquement listés dans l'interface RetroBat :

<div align="left"><figure><img src="https://i.imgur.com/JRHEcpL.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Les fichiers sonores doivent être au format .ogg pour pouvoir être utilisés par RetroArch.
{% endhint %}

## Répertoire "system"

Ce dossier contient plusieurs fichiers de configuration RetroBat ainsi que des "assets" fournies par défaut avec RetroBat (shaders, decorations...), la structure est la suivante:

<div align="left"><figure><img src="https://i.imgur.com/aQODkzO.png" alt=""><figcaption></figcaption></figure></div>

### Dossier "decorations"

Ce dossier contient les décorations (bezels) fournis par défaut avec RetroBat.

### Dossier "es\_menu"

Ce dossier contient les raccourcis vers les exécutables des émulateurs utilisés dans le système "RetroBat" du menu principal.

### Dossier "loadingscreens"

Ce dossier peut être utilisé pour placer des vidéos (format .mp4) qui seront lues par RetroBat lors du lancement d'un jeu, à la place du zoom sur la pochette du jeu.

Il est possible de définir une vidéo par système en nommant la vidéo du nom du système (ex. gamecube.mp4).\
\
Des exemples de vidéos de chargement se trouvent dans le dossier system\templates\loadingscreen.

### Dossier "padtokey"

Ce dossier contient les fichier [padtokey ](../controleurs/pad2key.md#fichier-pad2key)fournis par défaut avec RetroBat.

### Dossier "resource"

Dans le sous-dossier "inputmapping", il est possible de trouver les fichiers d'autoconfiguration utilisés par RetroBat pour certains systèmes:

<div align="left"><figure><img src="https://i.imgur.com/cxjYSok.png" alt=""><figcaption></figcaption></figure></div>

### Dossier "shaders"

Ce dossier contient les shaders (filtres vidéos) fournis par défaut avec RetroBat.

### Dossier "tattos"

Ce dossier contient les "tatouages", schémas de contrôles pour différents systèmes.

### Dossier "templates"

Ce dossier contient les fichiers d'origine de RetroBat tels qu'ils sont à l'installation, si un fichier a été modifié ou effacé par erreur, il peut être récupéré dans ce dossier.

## Répertoire "user"

Ce dossier peut être utilisé pour stocker les tattoos, fichiers inputmapping et la clé APIkey Steam.
