# Structure du répertoire RetroBat

Une fois RetroBat installé, le dossier d'installation contient les dossiers et fichiers suivants :

<div align="left"><figure><img src="../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="210.25">Dossier / fichier</th><th>Contenu</th></tr></thead><tbody><tr><td><code>bios</code></td><td>Fichiers BIOS et firmwares</td></tr><tr><td><code>cheats</code></td><td>Fichiers de triche</td></tr><tr><td><code>decorations</code></td><td>Vos propres décorations (bezels)</td></tr><tr><td><code>emulationstation</code></td><td>Interface de RetroBat (EmulationStation) et sa configuration</td></tr><tr><td><code>emulators</code></td><td>Émulateurs</td></tr><tr><td><code>library</code></td><td>Magazines et manuels</td></tr><tr><td><code>records</code></td><td>Enregistrements vidéo de vos parties</td></tr><tr><td><code>roms</code></td><td>Vos jeux</td></tr><tr><td><code>saves</code></td><td>Sauvegardes et sauvegardes instantanées</td></tr><tr><td><code>screenshots</code></td><td>Captures d'écran</td></tr><tr><td><code>sounds</code></td><td>Sons de déblocage des RetroAchievements</td></tr><tr><td><code>system</code></td><td>Fichiers internes de RetroBat et ressources par défaut</td></tr><tr><td><code>user</code></td><td>Vos fichiers de personnalisation</td></tr><tr><td><code>RetroBat.exe</code></td><td>Lance RetroBat</td></tr><tr><td><code>retrobat.ini</code></td><td>Réglages généraux de RetroBat (vidéo d'intro, démarrage automatique, détection de la langue…)</td></tr></tbody></table>

{% hint style="warning" %}
Les dossiers signalés comme « internes » ci-dessous sont gérés par RetroBat et peuvent être écrasés lors des mises à jour. Placez vos propres fichiers dans les dossiers prévus pour cela (`decorations`, `user`, etc.).
{% endhint %}

## Dossier « bios »

C'est ici que doivent être placés les BIOS et firmwares de tous les systèmes, à quelques exceptions près.

{% hint style="info" %}
Sauf indication contraire, les fichiers BIOS se placent directement à la racine du dossier `bios`. Certains émulateurs utilisent leur propre sous-dossier (par exemple `bios\pcsx2\bios`, `bios\dc`, `bios\mame`…) : ces sous-dossiers sont créés par l'installeur.

Les BIOS nécessaires et leur emplacement sont indiqués dans la page de chaque système, dans la section [Systèmes compatibles](../systemes-and-emulateurs/supported-game-systems/). Voir aussi [Ajouter les BIOS](ajouter-les-bios.md).
{% endhint %}

## Dossier « cheats »

Ce dossier contient les fichiers de triche (« cheats ») utilisés par les émulateurs compatibles, lorsque l'option de triche est activée. Il contient un sous-dossier par émulateur (`retroarch`, `pcsx2`, `duckstation`, `mame`…).

## Dossier « decorations »

Ce dossier est vide après l'installation. Il permet d'ajouter vos propres décorations (bezels) : elles seront disponibles dans RetroBat en plus des décorations fournies par défaut dans `system\decorations`.

## Dossier « emulationstation »

Ce dossier contient les exécutables de l'interface de RetroBat (EmulationStation) et d'emulatorLauncher, le programme qui configure et lance les émulateurs. La structure est la suivante :

<div align="left"><figure><img src="../.gitbook/assets/image (259).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Les fichiers de configuration de RetroBat (`es_settings.cfg`, `es_input.cfg`, `es_systems.cfg`…) et les fichiers de logs se trouvent dans ce dossier et dans son sous-dossier `.emulationstation`.
{% endhint %}

### Sous-dossier « .emulationstation »

#### collections

Ce dossier est créé par EmulationStation lorsque vous créez votre première [collection éditable](../navigation/game-collections.md#collections-editables). Chaque collection est enregistrée dans un fichier `.cfg` portant son nom, qui liste les jeux qu'elle contient avec leur emplacement.

#### music

Les fichiers audio placés dans ce dossier sont joués comme musique de fond dans l'interface. RetroBat accepte les formats `.mp3`, `.ogg`, `.wav` et `.flac`, ainsi que d'autres formats moins courants.

Pour passer à la musique suivante, appuyez sur le stick gauche (`[L3]`), ou utilisez le menu d'Accès Rapide : dans la Vue Système, appuyez sur `[SELECT]` et choisissez **PASSER À LA MUSIQUE SUIVANTE**.

<div align="left"><figure><img src="../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure></div>

Les musiques sont jouées de façon aléatoire.

Vous pouvez aussi jouer des musiques spécifiques à chaque système. Créez un sous-dossier nommé exactement comme le dossier `roms` du système (par exemple `music\snes`), et placez-y vos fichiers audio.

* Avec l'option **JOUER SEULEMENT LES MUSIQUES PAR SYSTÈMES** **activée**, RetroBat joue les musiques du système que vous parcourez (par exemple `music\3do`) et celles placées directement dans `music`, mais pas celles des autres systèmes.
* Avec cette option **désactivée**, RetroBat joue au hasard n'importe quelle musique de `music` et de tous ses sous-dossiers.

<div align="left"><figure><img src="../.gitbook/assets/image (261).png" alt=""><figcaption></figcaption></figure></div>

#### scripts

EmulationStation peut exécuter vos propres scripts ou programmes lors de certains événements. Placez-les dans le sous-dossier correspondant à l'événement :

<table><thead><tr><th width="137.75">Sous-dossier</th><th>Événement</th></tr></thead><tbody><tr><td><code>game-start</code></td><td>Lancement d'un jeu</td></tr><tr><td><code>game-end</code></td><td>Fermeture d'un jeu</td></tr><tr><td><code>quit</code></td><td>Fermeture de RetroBat</td></tr><tr><td><code>reboot</code></td><td>Redémarrage de l'ordinateur depuis RetroBat</td></tr><tr><td><code>shutdown</code></td><td>Arrêt de l'ordinateur depuis RetroBat</td></tr><tr><td><code>sleep</code></td><td>Mise en veille de l'ordinateur</td></tr><tr><td><code>wake</code></td><td>Sortie de veille de l'ordinateur</td></tr></tbody></table>

#### themes

Les thèmes téléchargés via le menu **TÉLÉCHARGEMENT DE CONTENU** sont stockés dans ce dossier. Vous pouvez aussi y copier des thèmes manuellement.

#### themesettings

Ce dossier contient les réglages propres à chaque thème. Lorsque vous personnalisez un thème depuis le menu des thèmes, ses réglages sont enregistrés ici, dans un fichier `.cfg` portant le nom du thème.

#### video

Placez ici des vidéos pour les utiliser comme intro (« vidéo de démarrage ») avant le lancement de RetroBat. Vous pouvez configurer facilement ces vidéos avec [BatGui](../utilisation-avancee/batgui.md) ou dans [`retrobat.ini`](../utilisation-avancee/retrobat.ini.md).

## Dossier « emulators »

Ce dossier contient les émulateurs.

RetroArch est fourni avec RetroBat. Tous les autres émulateurs sont téléchargés automatiquement la première fois que vous lancez un jeu qui en a besoin, ou lorsque vous les lancez depuis le menu système RetroBat.

{% hint style="info" %}
Pour des raisons légales ou techniques, certains émulateurs ne peuvent pas être téléchargés automatiquement par RetroBat. Vous devez les télécharger vous-même et les placer dans le dossier correspondant :

* Émulateurs Switch
* PICO-8
* 3DSen
* TeknoParrot
{% endhint %}

## Dossier « library »

Ce dossier permet de stocker des magazines ou des manuels. Ils apparaissent dans RetroBat dans un système « Library » et peuvent être consultés avec le core libretro **imageviewer**.

## Dossier « records »

Ce dossier reçoit les vidéos de vos parties enregistrées par les émulateurs compatibles avec l'enregistrement vidéo. Les vidéos sont enregistrées dans `records\output`, les réglages d'enregistrement dans `records\config`.

## Dossier « roms »

C'est ici que vous copiez vos jeux. Chaque jeu doit être placé dans le dossier de son système (par exemple `roms\snes`) et avoir une extension acceptée par l'émulateur. Ces dossiers sont créés par l'installeur.

Plus d'informations dans la page de chaque système, dans la section [Systèmes compatibles](../systemes-and-emulateurs/supported-game-systems/), et dans [Ajouter des jeux](adding-a-game.md).

## Dossier « saves »

Ce dossier contient vos sauvegardes de jeu (sauvegardes en jeu et sauvegardes instantanées), classées par système puis par émulateur (par exemple `saves\psx\duckstation`).

## Dossier « screenshots »

Ce dossier contient les captures d'écran prises pendant vos parties.

{% hint style="info" %}
Si une sauvegarde ou une capture d'écran n'est pas enregistrée dans le bon dossier, merci de le signaler à l'équipe RetroBat pour qu'elle puisse le corriger.
{% endhint %}

## Dossier « sounds »

Le sous-dossier `sounds\retroachievements` contient les sons joués lors du déblocage d'un RetroAchievement. Les fichiers copiés à cet endroit apparaissent automatiquement dans l'option **SON DE DÉBLOQUAGE** des réglages RetroAchievements :

<div align="left"><figure><img src="../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Les fichiers doivent être au format `.ogg` et placés dans `sounds\retroachievements`, et non à la racine de `sounds`.
{% endhint %}

## Dossier « system »

Ce dossier contient des fichiers de configuration de RetroBat et les ressources fournies par défaut (décorations, shaders…). La structure est la suivante :

<div align="left"><figure><img src="../.gitbook/assets/image (263).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Le contenu de ce dossier est remplacé lors des mises à jour de RetroBat. Ne le modifiez pas : utilisez les dossiers `user` et `decorations` pour vos propres fichiers.
{% endhint %}

### Sous-dossiers « configgen », « download », « modules », « scripts » et « tools »

Fichiers internes de RetroBat (installation, mise à jour, modules de lancement, outils utilisés par RetroBat). Ils n'ont pas à être modifiés.

### Sous-dossier « decorations »

Les décorations (bezels) fournies par défaut avec RetroBat.

### Sous-dossier « es\_menu »

Les raccourcis vers les émulateurs affichés dans le système « RetroBat », qui permet de lancer directement les émulateurs.

### Sous-dossier « loadingscreens »

Ce dossier n'est pas créé par l'installeur : créez-le si vous voulez afficher une courte vidéo (`.mp4`) au lancement d'un jeu, à la place de l'effet de zoom sur l'image du jeu.

RetroBat cherche la vidéo dans cet ordre, et lit la première trouvée :

| Fichier                                        | Lu pour                    |
| ---------------------------------------------- | -------------------------- |
| `loadingscreens\<système>\<nom de la rom>.mp4` | Un jeu précis              |
| `loadingscreens\<système>\<système>.mp4`       | Tous les jeux d'un système |
| `loadingscreens\<système>.mp4`                 | Tous les jeux d'un système |
| `loadingscreens\default.mp4`                   | Tous les jeux              |

Par exemple, `loadingscreens\gamecube.mp4` est lu pour tous les jeux GameCube.

Des exemples de vidéos sont fournis dans `system\templates\loadingscreens`.

### Sous-dossier « padtokey »

Les fichiers [padtokey](../controleurs/pad2key.md) fournis par défaut avec RetroBat.

#### Sous-dossier « resources »

Ressources utilisées par RetroBat. Le sous-dossier `inputmapping` contient les fichiers qui servent à configurer automatiquement les contrôles pour certains émulateurs ou certains types de manettes.

<div align="left"><figure><img src="../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Ces fichiers sont écrasés lors des mises à jour de RetroBat. Pour conserver vos versions modifiées, copiez-les dans le dossier `user\inputmapping`.
{% endhint %}

### Sous-dossier « shaders »

Les shaders (filtres vidéo) fournis par défaut avec RetroBat.

### Sous-dossier « tattoos »

Les schémas de contrôles (« tattoos ») fournis par défaut pour plusieurs systèmes.

### Sous-dossier « templates »

La version d'origine des fichiers de configuration de RetroBat, tels qu'ils sont à l'installation. Si un fichier a été supprimé ou abîmé, vous pouvez recopier sa version d'origine depuis ce dossier vers son dossier de destination.

## Dossier « user »

Ce dossier contient vos fichiers de personnalisation, qui sont conservés lors des mises à jour de RetroBat :

| Sous-dossier   | Contenu                                                                                                                                                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `apikey`       | Votre clé API Steam (fichier `steam.apikey`)                                                                                                                 |
| `customratio`  | Ratios d'image personnalisés pour les cores libretro : `<système>_customratio.txt` (tout le système) ou `<système>_<nom de la rom>_customratio.txt` (un jeu) |
| `inputmapping` | Vos fichiers inputmapping modifiés                                                                                                                           |
| `padtokey`     | Vos propres fichiers padtokey                                                                                                                                |
| `tattoos`      | Vos propres schémas de contrôles (sous-dossiers `default` et `games`)                                                                                        |
