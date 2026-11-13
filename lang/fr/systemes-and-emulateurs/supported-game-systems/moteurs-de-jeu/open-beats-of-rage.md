---
description: Senile Team
---

# Open Beats Of Rage

<div align="left"><figure><img src="../../../.gitbook/assets/image (583).png" alt="" width="530"><figcaption></figcaption></figure></div>

## Présentation

**Beats of Rage** est un jeu de combat à défilement créé en 2003 par Senile Team, en hommage à Streets of Rage. Son code source est publié l'année suivante, et la communauté en fait un moteur de jeu complet : **OpenBOR** (Open Beats of Rage).

Depuis, des centaines de jeux amateurs ont été réalisés avec OpenBOR, souvent inspirés de Streets of Rage, Final Fight, Double Dragon ou des jeux d'arcade de Capcom. Chaque jeu est livré dans un fichier `.pak` qui contient ses graphismes, ses sons et ses scripts.

Le moteur a beaucoup évolué, et chaque jeu a été écrit pour une version précise d'OpenBOR. RetroBat propose le core **AnyBOR**, qui réunit de nombreuses versions du moteur et choisit automatiquement la bonne, et le programme **OpenBOR** lui-même.

{% embed url="https://fr.wikipedia.org/wiki/Beats_of_Rage" %}

## En bref

<table><thead><tr><th width="279"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\openbor</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pak .exe</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: anybor</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (sauf versions spécifiques d'OpenBOR)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                     | Points forts                                                                                                                                            | Limites                                                                                             |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| **libretro: anybor** (défaut) | Contient une trentaine de versions du moteur et choisit automatiquement celle du jeu. Sauvegardes instantanées, macros des coups spéciaux, vibrations.  | —                                                                                                   |
| **openbor**                   | Le moteur OpenBOR officiel, version récente fournie par RetroBat.                                                                                       | Les jeux écrits pour une ancienne version peuvent mal fonctionner. Pas de sauvegardes instantanées. |
| **openbor-specific-version**  | Lance le jeu avec une version d'OpenBOR que vous avez installée vous-même (voir [Guides](open-beats-of-rage.md#utiliser-une-version-precise-dopenbor)). | Manettes et réglages à configurer dans OpenBOR.                                                     |

Gardez **anybor** : c'est le plus simple, puisqu'il trouve seul la version du moteur. Si un jeu ne fonctionne pas, essayez de forcer sa version (voir [Guides](open-beats-of-rage.md#choisir-la-version-du-moteur-anybor)), puis l'émulateur **openbor**.

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

<table><thead><tr><th width="112.75">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.pak</strong></td><td>Le jeu complet en un seul fichier. Le format le plus courant.</td></tr><tr><td><strong>.exe</strong></td><td>Jeu livré avec son propre exécutable OpenBOR, dans un dossier qui contient aussi ses données (dossier <code>data</code> ou dossier <code>Paks</code>).</td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes avec anybor et openbor. Les versions spécifiques d'OpenBOR (**openbor-specific-version**) se configurent dans OpenBOR.

| Manette RetroBat                    | anybor (disposition AUTO)             | openbor, et anybor en disposition OPENBOR STANDALONE |
| ----------------------------------- | ------------------------------------- | ---------------------------------------------------- |
| Croix directionnelle / stick gauche | Déplacement                           | Déplacement                                          |
| OUEST                               | Attaque                               | Attaque                                              |
| SUD                                 | Saut                                  | Saut                                                 |
| EST                                 | Spécial                               | Attaque 2                                            |
| NORD                                | Attaque 2                             | Spécial                                              |
| L1                                  | Attaque 3                             | Attaque 4                                            |
| R1                                  | Attaque 4                             | Attaque 3                                            |
| L2, R2, L3, R3                      | Coups spéciaux du personnage (macros) | —                                                    |
| START                               | START                                 | START                                                |
| HOTKEY                              | —                                     | Échap (menu d'OpenBOR)                               |

* L'option **CONTRÔLES > DISPOSITION DES BOUTONS** d'anybor choisit la disposition : automatique, ou **OPENBOR STANDALONE** pour retrouver les boutons de l'émulateur openbor.
* Avec anybor, **CONTRÔLES > MACROS DES COUPS SPÉCIAUX** place sur L2, R2, L3 et R3 les coups spéciaux du personnage, quand le jeu les décrit (activé par défaut).
* Avec anybor, **CONTRÔLES > UTILISER LE STICK GAUCHE COMME D-PAD** (activé par défaut) et **CONTRÔLES > ACTIVER LES VIBRATIONS** règlent le stick gauche et les vibrations.

### Raccourcis

anybor utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../navigation/hotkeys.md)).

Avec openbor :

<table><thead><tr><th width="128.25">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY</strong></td><td>Menu d'OpenBOR (pause, quitter)</td><td>ÉCHAP</td></tr><tr><td>—</td><td>Capture d'écran</td><td>F12</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="306.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes (anybor)</td><td><code>saves\openbor</code></td></tr><tr><td>Sauvegardes instantanées (anybor)</td><td><code>saves\openbor\libretro.anybor</code></td></tr><tr><td>Sauvegardes (openbor)</td><td><code>saves\openbor</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots</code></td></tr><tr><td>Configuration d'openbor</td><td><code>emulators\openbor\config.ini</code></td></tr><tr><td>Versions spécifiques d'OpenBOR</td><td><code>emulators\openbor\&#x3C;numéro de version></code></td></tr></tbody></table>

## Guides

### Ajouter un jeu

1. Copiez le fichier `.pak` du jeu dans `roms\openbor`.
2. Mettez à jour la liste des jeux de RetroBat.
3. Lancez le jeu.

### Jeu livré avec son exécutable

Certains jeux sont distribués avec leur propre `OpenBOR.exe`. Copiez tout le dossier du jeu dans `roms\openbor`, par exemple `roms\openbor\Mon jeu\OpenBOR.exe`, et mettez à jour la liste des jeux : c'est l'exécutable qui apparaît dans RetroBat.

* Avec **anybor**, RetroBat charge les données du jeu (`data\models.txt` ou le premier `.pak` du dossier `Paks`) sans lancer l'exécutable.
* Avec **openbor**, RetroBat lance l'exécutable fourni.

### Choisir la version du moteur (anybor)

anybor détecte la version du moteur d'après les données du jeu. Si la détection se trompe :

* Indiquez la version entre crochets à la fin du nom du fichier, par exemple `Mon jeu [4086].pak`. C'est la même indication que pour openbor-specific-version.
* Ou choisissez la version dans **ÉMULATION > VERSION DU MOTEUR**.

La documentation du jeu, ou la page où vous l'avez téléchargé, indique en général la version d'OpenBOR utilisée.

### Utiliser une version précise d'OpenBOR

1. Téléchargez la version d'OpenBOR voulue et placez-la dans un dossier nommé avec son numéro de version, par exemple `emulators\openbor\4153\OpenBOR.exe`.
2. Ajoutez ce numéro entre crochets à la fin du nom du jeu : `Mon jeu [4153].pak`.
3. Choisissez l'émulateur **openbor-specific-version** pour ce jeu.

RetroBat copie le jeu dans le dossier `Paks` de cette version avant de la lancer (les autres fichiers de ce dossier sont supprimés), puis le retire à la fin de la partie. Les manettes et les réglages se font dans OpenBOR.

### Autres options utiles

| Option                                       | Effet                                                                                                                                      |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **ÉMULATION > VERSION DU MOTEUR** (anybor)   | Force la version d'OpenBOR utilisée pour le jeu.                                                                                           |
| **VIDÉO > ADAPTER POUR TV CRT 4:3** (anybor) | Place les jeux en haute résolution ou en écran large dans une image 640x480 avec des bandes noires. Utile seulement sur une TV cathodique. |
| **SHADERS** (openbor)                        | Filtres d'image d'OpenBOR : Bilinear, HQ2X, Scanlines…                                                                                     |
| **RAPPORT D'ASPECT** (openbor)               | **STRETCH** étire l'image sur tout l'écran.                                                                                                |
| **DÉCORATIONS** (openbor)                    | Affiche un habillage autour de l'image.                                                                                                    |

## Problèmes connus

| Problème                                                | Solution                                                                                                              |
| ------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Le jeu plante, s'affiche mal ou ne démarre pas          | Il demande une autre version du moteur : indiquez-la dans le nom du fichier (`[4086]`) ou dans **VERSION DU MOTEUR**. |
| Un jeu `.exe` ne se lance pas avec anybor               | Le dossier du jeu doit contenir `data\models.txt` ou un dossier `Paks` avec un fichier `.pak`.                        |
| Les boutons ne correspondent pas à ceux d'openbor       | Réglez **DISPOSITION DES BOUTONS** sur **OPENBOR STANDALONE**.                                                        |
| Avec openbor-specific-version, la manette ne répond pas | RetroBat ne configure pas les versions spécifiques : réglez les touches dans le menu d'OpenBOR.                       |
